## SQL语句分类：
* DDL数据定义语言——创建或删除 CREATE创建 DROP删除 ALTER修改
* DML数据操纵语言——查询或变更 SELECT查询 INSET插入新数据 UPDATA更新 DELETE删除
* DCL数据控制语言——确认或取消之前的变更 COMMIT确认变更 ROLLBACK取消变更 GRANT赋予权限 REVOKE取消权限

单表查询
select - from table
select * from table
select * from table where 加条件
select * from table order by - limit - (升序)/ oreder by - desc limit - (降序)

多表联立查询
select * from table1 as...
   left join table2 as...
   on table1.id=table2.id
   
## DDL数据定义语言
1. 创建数据库  CREATE database;
2. 创建表      CREATE table;
3. 删除表      DROP table;
4. 表定义的更新 
   增加一列——ADD column
            ALTER table ADD column name datatype;
   删除一列——DROP column
            ALTER table DROP column name;
   变更表名——RENAME
            ALTER table RENAME tablename1 to tablename2;
  
## DML数据操纵语言


## Exampple
### ex.获取第n高的薪水
* IFNULL() 函数用于判断第一个表达式是否为 NULL，如果为 NULL 则返回第二个参数的值，如果不为 NULL 则返回第一个参数的值
  格式：IFNULL(expression, alt_value)
* limit n,m 限制返回的行数。可以有两个参数，第一个参数n为起始行，从 0 开始；第二个参数m为返回的总行数
  注意：limit()方法中不能参与运算，可以预先设定set
* 筛选值时注意加distinct，保证唯一性
