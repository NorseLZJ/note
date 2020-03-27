#### MySQL 8.0 dateTime 
* err : Incorrect datetime value  
    * 1 SHOW VARIABLES LIKE 'sql_mode';     
    Result: ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION    
    Option: Remove NO_ZERO_IN_DATE,NO_ZERO_DATE   
    * 2 set GLOBAL SQL_MODE='ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION';  
    * 3 [From](https://stackoverflow.com/questions/35565128/mysql-incorrect-datetime-value-0000-00-00-000000)