# redis list

## list命令介绍

- BLPOP
    命令格式：BLPOP key
    作用：删除队列第一个元素，或阻塞到一个可以用的元素，是LPOP的阻塞模式
    例子：

- BRPOP
    命令格式：BRPOP key
    作用：删除队列最有一个元素，或阻塞到一个可以用的元素，是LPOP的阻塞模式
    例子：

- BRPOPLPUSH
    命令格式： BRPOPLPUSH skey dkey timeout
    作用：从队列skey弹出一个值插入到dkey队列尾部，或者阻塞到一个可用的值
    例子：

- LINDEX
    命令格式：LINDEX key index
    作用： 通过其索引获得列表的某一个值
    例子：

- LINSERT
    命令格式：LINSERT BEFORE|AFTER pv value
    作用：在队列的一个之前或之后插入一个值
    例子：

- LLEN
    命令格式：LLEN key
    作用：获取列表的长度
    例子：

- LPOP
    命令格式：LPOP key
    作用：从队列左边出队一个元素
    例子：

- LPUSH
    命令格式：LPUSH key value
    作用：从队列左边入队一个元素
    例子：

- LPUSHX
    命令格式： LPUSHX key value
    作用：当队列存在时，从左边入队一个元素
    例子：

- LRANGE
    命令格式：LRANGE key start stop
    作用：从列表中获取指定范围的元素
    例子：

- LREM
    命令格式： LREM key count value
    作用：从列表中删除元素
    例子：

- LSET
    命令格式：LSET key index value
    作用：设置队列里一个元素的值
    例子：

- LTRIM
    命令格式： LTRIM key start stop
    作用：删除指定范围内的值
    例子：

- RPOP
    参见LPOP

- RPOPLPUSH
    BRPOPLPUSH非阻塞形式

- RPUSH
    参加LPUSH

- RPUSHX
    参见 LPUSHX

## list的应用
    list是redis重要的数据结构之一，应用场景非常多。
    使用list，可以轻松的实现消息队列的功能。可以利用push操作，将任务存在list中，然后worker
    调用pop，将任务取出执行。
### 实现方式
    redis list实现为一个双向链表，既可以支持反向查询，也可以支持遍历，不会带来额外的内存开销
    RPOPLPUSH s d，该命令是原子时间内，执行两个动作，从s链表最后弹出元素，插入到d链表首部。
    并返回给客户端该元素。如果s d相同。则是把元素从首部移动到尾部。

## list实现原理
    后续再添加
