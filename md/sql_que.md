
## MySQL 常见面试题
### 什么是事物，MySQL如何支持事物？
* 事物:是由一组SQL语句组成的逻辑处理单元,事物具有以下4个属性，通常简称为事物。
* a:(atomicity)原子性,事物是一个原子操作单元，事物所包含的操作要么全部成功，要么全部失败
回滚，因此事物的操作如果成功就必须要完全应用到数据库，如果操作失败则不能对数据库有任何影响.
* b:(consistent)一致性,


### mysql存储引擎
- MyIsam,InnoDB,memoryNDB,blackhold ...
    - Myisam: 不支持事物，支持表锁和全文索引，查找效率极高
    - InnoDB: 支持事物，行锁，查询性能相对比 Myisam 低
    -


- 索引
    - Btree : blance tree
    - Hash  :  
    - 优缺点：
        - 优：提高检索速度，降低磁盘的IO
        - 缺：索引需要存储，需要空间，实际上就是一张表，字段更新会有性能损耗

- 适合建索引
    - 频繁作为where条件的字段
    - 关联字段可以建索引，例如外键
    - order by col, group by col

- 不合适   
    - where 条件中用不到的字段
    - 频繁更新的字段
    - 数据值发布比较均匀的不适合，例如 true,false
    - 表的数据可以确定行数，而且数据量比较少

- 索引失效的情况
    - index(name,age) ; select * from user order by age ; select * from user where age='' and name='';
