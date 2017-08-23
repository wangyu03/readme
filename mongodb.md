### 服务器配置
- `mkdir -p mongodb/{mongo,mlog}`rout下面创建
- `apt-get install mongodb -y`
- `touch /root/config/mongodb.conf`
- `vim /etc/iptables.rules`,`  A INPUT -p tcp -m tcp --dport 27017 -j DROP`
- ` mongod -f /root/config/mongodb.conf`启动


- mongodb.conf
```
port=27017 #指定端口
fork=true #后台运行
dbpath=/root/mongodb/mongo #规定数据库的位置
logpath=/root/mongodb/mlog/mongodb.log #规定数据库的日志文件
#slave=true #声明从
#source=123.207.172.26:27018 #规定从属于哪个ip  注意：ip是主服务器的  最好用内网ip
# bind_ip=127.0.0.1,192.168.0.4 #允许的地址 为了安全
nohttpinterface=true #禁止http访问
```