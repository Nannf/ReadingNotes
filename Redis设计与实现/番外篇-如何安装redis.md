1. ```
   wget http:``//download.redis.io/releases/redis-5.0.7.tar.gz
   ```

2. tar -zvxf redis-5.0.7.tar.gz
3. mv /root/redis-5.0.7 /usr/local/redis
4. make（这步会出问题）
5. make PREFIX=/usr/local/redis install
6. vi redis.conf
   1. daemonize yes
   2. bind 127.0.0.1 注释掉
   3. protected-mode no
   4. requirepass 自己的密码
   5. 设置开机启动
      1. vi /etc/rc.d/rc.local
      2. /usr/local/redis-5.0.0/bin/redis-server  /usr/local/redis-5.0.0/etc/redis.conf
   6. 启动
      1. ./redis-server /usr/local/redis-5.0.0/etc/redis.conf
   7. 关闭服务器防火墙
7. redis-cli登录到redis后台
8. auth “自己的密码”