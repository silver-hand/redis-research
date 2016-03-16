# 使用源代码安装
    redis 官方网站redis.io
## 下载源代码
    源代码的下载地址：http://redis.io/download
下载的版本尽量是最近的稳定版本

## 解压缩

    tar xzvf redis-x.y.z.tar.gz

## 编译

    cd redis-x.y.z
    make
    make install

## 命令介绍
make install 之后，/user/local/bin下目录下会多些可执行文件，分别是redis-server、redis-cli、redis-benchmark、redis-check-aof 、redis-check-dump。作用如下：

- redis-server：Redis服务器的daemon启动程序
- redis-cli：Redis命令行操作工具。也可以用telnet根据其纯文本协议来操作
- redis-benchmark：Redis性能测试工具，测试Redis在当前系统下的读写性能
- redis-check-aof：数据修复
- redis-check-dump：检查导出工具
- redis-sentinel:指向redis-server的软链接

## 配置redis
简单配置一下就可以启动redis了
### 系统参数的修改
    - echo vm.overcommit_memory=1 >> /etc/sysctl.conf
    - sysctl vm.overcommit_memory=1
使用字段的含义：
  0，表示内核将检查是否有足够的可用内存供应用进程使用；如果有足够的可用内存，内存申请允许；否则，内存申请失败，并把错误返回给应用进程。
  1，表示内核允许分配所有的物理内存，而不管当前的内存状态如何。
  2，表示内核允许分配超过所有物理内存和交换空间总和的内存。

### 修改redis配置
打开redis.conf

- daemonize：是否以后台daemon方式运行

- pidfile：pid文件位置

- port：监听的端口号

- timeout：请求超时时间

- loglevel：log信息级别

- logfile：log文件位置
databases：开启数据库的数量

- save \* \*：保存快照的频率，第一个\*表示多长时间，第二个\*表示执行多少次写操作。在一定时间内执行一定数量的写操作时，自动保存快照。可设置多个条件。

- rdbcompression：是否使用压缩

- dbfilename：数据快照文件名（只是文件名，不包括目录）

- dir：数据快照的保存目录（这个是目录）

- appendonly：是否开启appendonlylog，开启的话每次写操作会记一条log，这会提高数据抗风险能力，但影响效率。

- appendfsync：appendonlylog如何同步到磁盘（三个选项，分别是每次写都强制调用fsync、每秒启用一次fsync、不调用fsync等待系统自己同步）

## 启动redis
$redis-server redis.conf

## 检查redis是否启动
    ps -ef|grep redis

## 检查redis 监听端口
    netstat -anp|grep redis

## 安装后测试
  
