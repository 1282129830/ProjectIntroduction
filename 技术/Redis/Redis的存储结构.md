#### Redis支持的数据类型

> String(字符串)

string类型是二进制安全的。意思是redis的string可以包含任何数据。比如jpg图片或者序列化的对象 。

string类型是Redis最基本的数据类型，一个键最大能存储512MB。

> Hash(哈希)

Redis hash 是一个键值(key=>value)对集合。

Redis hash是一个string类型的field和value的映射表，hash特别适合用于存储对象。

> List(列表)

Redis 列表是简单的字符串列表，按照插入顺序排序。可以添加一个元素到列表的左边或者右边

> Set(无序集合)

集合是通过哈希表实现的。

> SortedSet(有序集合)

每个元素都会关联一个double类型的分数，redis正是通过分数来为集合中的成员进行从小到大的排序。

SortedSet的成员是唯一的,但分数(score)却可以重复。