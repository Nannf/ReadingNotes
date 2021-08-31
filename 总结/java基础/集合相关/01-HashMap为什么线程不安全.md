#### HashMap为什么线程不安全

- 其实这个问题我不知道想考察什么东西，因为HashMap未采用任何同步措施，如果被发布(多个线程都可以访问)，这件事情本身从并发编程的角度考虑都不应该让它发生；
- 网上给出的答案有两个版本：
  - 1.7版本的transfer方法，因为头插法（时间复杂度O(1)）导致并发resize时，链表出现了死循环，且会丢失数据；
  - 1.8版本放弃了使用这个方法，然后在插入时，先做了key在不在这个链表中的判断，这个先判断后执行的是并发问题的典型场景，这个很容易理解；

比较难理解的是1.7版本的，现在的1.7代码已经久不可考，也没人会写并发时使用未同步的HashMap作为并发容器；

不吐槽了；

```java
void transfer(Entry[] newTable, boolean rehash) {
    int newCapacity = newTable.length;
    for (Entry<K,V> e : table) {
        while(null != e) {
            Entry<K,V> next = e.next;
            if (rehash) {
                e.hash = null == e.key ? 0 : hash(e.key);
            }
            int i = indexFor(e.hash, newCapacity);
            e.next = newTable[i];
            newTable[i] = e;
            e = next;
        }
    }
}
```

![image](https://segmentfault.com/img/remote/1460000038989243)

![image](https://segmentfault.com/img/remote/1460000038989246)

线程一 newTable[i] = e; cpu切换了时间片；

![image](https://segmentfault.com/img/remote/1460000038989245)



此时另一个线程完成了扩容。此时7.next = 3了；

![image](https://segmentfault.com/img/remote/1460000038989251)

然后切换回了线程一，接着完成刚刚没完成的替换，然后e变成了7；

然后接着循环，我们发现，此时的next，并不是线程一之前看到的5了，而是3；



![image](https://segmentfault.com/img/remote/1460000038989250)

头插法进入之后我们发现，此时的e是3，next也是三

![image](https://segmentfault.com/img/remote/1460000038989249)

接着步入上面的循环，三又作为头插法插入了3这个桶中，此时的3的next已经为null；满足了循环结束条件

![image](https://segmentfault.com/img/remote/1460000038989247)

此时问题出现，链表中出现了环，且5已经被丢失了；