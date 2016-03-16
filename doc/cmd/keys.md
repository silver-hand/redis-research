# redis keys

#redis keys 命令

- DEL
    命令格式：DEL key
    作用：删除一个key
    例子： DEL key-cdn

- DUMP key
    命令格式： DUMP key
    作用：导出key的值
    例子： dump key-cdn

- EXISTS
    命令格式： EXISTS key
    作用：测试key是否存在
    例子：EXISTS key-cdn

- EXPIRE
    命令格式： EXPIRE key seconds
    作用：设置一个key的过期时间
    例子：EXPIRE key-cdn 2

- EXPIREAT
    命令格式： EXPIREAT key timestamp
    作用： 设置一个unix时间戳过期时间
    例子： EXPIREAT key-cdn 140023230

- KEYS
    命令格式：keys parttern
    作用：查找所有符合模式的key
    例子：KEYS key*

- MIGRATE
    命令格式：MIGRATE
    作用：
    例子

- MOVE
    命令格式： move key db
    作用：将key 从一个数据库移动当指定的数据库中
    例子 move key-cdn 2

- object
    命令格式： object subcmd [args]
    作用：检查内部再分配对象
    例子：

- PERSIST
    命令格式： PERSIST key
    作用：移除key的过期时间
    例子： PERSIST key-cdn

- PEXPIRE
    命令格式： PEXPIRE key milsec
    作用：设置key的过期时间为微妙
    例子：PEXPIRE key-cdn 300

- PEXPIREAT
    命令格式： PEXPIREAT key mil-sectimestamp
    作用：设置key的过期时间为unix微妙的时间戳
    例子

- pttl
    命令格式： pttl key
    作用：获取key有效的毫秒数
    例子：

- RANDOMKEY
    命令格式：RANDOMKEY
    作用：返回随机key
    例子：

- RENAME
    命令格式：RENAME key newname
    作用：重命名一个key
    例子：

- RENAMENX
    命令格式： RENAMENX key newname
    作用：重命名key，当key存在时有效
    例子：

- RESTORE
    命令格式：
    作用：
    例子：

- SORT
    命令格式：
    作用：
    例子：

- TTL
    命令格式：
    作用：
    例子：

- TYPE
    命令格式：
    作用：
    例子：

- WAIT
    命令格式：
    作用：、
    例子

- SCAN
    命令格式：
    作用：
    例子：

## 应用场景
    应用比较少
