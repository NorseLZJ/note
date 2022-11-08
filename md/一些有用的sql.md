

# 删除重复行，按照某列

```sql
DELETE s1
FROM filter_md5 AS s1
         INNER JOIN filter_md5 AS s2
WHERE s1.fm_id < s2.fm_id
  AND s1.md5 = s2.md5;

```

# 给一个表添加 unique key 

```sql
alter table filter_md5
    add constraint md5_unique
        unique (md5);

-- 执行此行命令，先执行上一条命令
```
