
### MySQL

* LIKE  
SELECT field_name from table where LIKE '%val%';  
% (通配符)任意多个字符包含0个字符   
  
* BETWEEN AND  
SELECT field_name FORM table where field_name BETWEEN start AND num;  

* IN  
SELECT field_name FORM table WHERE field_name IN('str',...);  

* DISTINCT (去重)  
SELECT DISTINCT field_name FORM table ;  

* ORDER BY 排序  (ASC升序 DESC降序)  
SELECT * from tab_name where cond ORDER BY field_name;  

* LENGTH (长度函数)  
SELECT  LENGTH(last_name) NameLen 
FROM employees
RDER BY NameLen DESC;   # ORDER BY 支持起别名  
ORDER BY 可以支持单个字段，多个字段，表达式，函数，别名  

#### 函数  
* 单行函数 concat,length,ifnull ...  
* 分组函数  
* 数学函数   round,ceil,floor,truncate,mod   
* 日期函数 now,curdate,curtime,sto_to_date,date_format,


