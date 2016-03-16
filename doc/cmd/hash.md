# redis hash

## redis hash 命令

- HSET
    命令格式： HSET key field value
    作用：设置hash里的一个字段的值
    例子：HSET cdn name fastweb

- HGET
    命令格式： HGET key field
    作用：查询一个hash key 的某一个域的值
    例子： HGET cdn name
- HEXISTS
    命令格式： HEXISTS key field
    作用：查询hash key 是否存在某一个field
    例子： HEXISTS cdn name
- HGETALL
    命令格式： HGETALL key
    作用： 获取hash key的所有域和值
    例子： HGETALL cdn
- HKEYS
    命令格式: HKEYS
    作用： 获取所有hash key的所有字段
    例子： HKEYS cdn

- HDEL
    命令格式： HDEL key field
    作用：删除一个或者多个hash的field。
    例子： HDEL cdn name

- HINCRBY
    命令格式： HINCRBY key field inc
    作用：将hash中指定域的值增加给定的数字
    例子：hincrby cdn cnt 2

- HINCRBYFLOAT
    命令格式： HINCRBYFLOAT key field inc
    作用：将hash中指定域的值增加给定的浮点数字
    例子：hincrby cdn cnt 2.1

- HLEN
    命令格式：hlen key
    作用： 获取hash key里所有字段的数量
    例子： hlen cdn

- HMGET
  命令格式：HMGET key field1 ... fieldn
  作用：获取hash key 多个field的值
  例子: HMGET cdn name addr

- HMSET
    命令格式： HMSET key field1 value1 ... fieldn valuen
    作用：设置hash key 多个域的值
    例子：hmset cdn name fastweb addr beijing

- HSETNX
    命令格式： HSETNX key field value1
    作用：设置一个hash key域的值，当且该域不存在时有
    例子: HSETNX cdn name fastweb

- HSTRLEN
    命令格式: HSTRLEN key field
    作用：获取hash key 域的字符串长度
    例子：HSTRLEN cdn name

- HVALS
    命令格式：HVALS key
    作用：获取hash key的所有值
    例子：hvals cdn

- HSCANS
    命令格式： HSCANS
    作用：
    例子

## redis hash 应用场景
    redis hash是redis使用最频繁的数据结构，重要性不言而喻。主要是用作对象的多属性存储。
    比如存储一个用户对象：对象的属性包括名字，id，地址，电话，如果使用key value的形式存储，
    则需要把名字，id地址，电话序列化到一个value中，在获取对象名字时，需要获得value，并且从字符串中反序列化出名，这个过程没什么难度，但是，确实开发者增加开发时间和难度。如果是hash，可以
    的解决问题。设置不同的域和值，每次都可以轻松的获取到想得到的结果。

## redis hash实现原理
    后续添加
