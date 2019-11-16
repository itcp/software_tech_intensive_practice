

\# 创建数据库

```sql
CREATE DATABASE exercise DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;
use exercise;
source exercise.sql;
```



\# 库表操作

```sql
# --备份库
mysqldump -u root -p --default-character-set=utf8 exercise > exercise_11-01.sql

# --备份表
mysqldump -u root -p exercise student --default-character-set=utf8 | gzip > tab_student.sql.gz;

# --删除表
drop table student;

# --创建表 
CREATE TABLE `student`(
	`s_id` VARCHAR(20),
	`s_name` VARCHAR(20) NOT NULL DEFAULT '',
	`s_birth` VARCHAR(20) NOT NULL DEFAULT '',
	PRIMARY KEY(`s_id`)
);

# --增加一个字段，设好数据类型，且不为空，添加注释
alter table student add `s_sex` VARCHAR(10) NOT NULL COMMENT '性别'; 

# --查看表结构
desc student;

# --查看表结构详细信息
select * from information_schema.columns where TABLE_SCHEMA='exercise' and TABLE_NAME='student';
```





\# 数据基本操作语句 

```sql
#-- 删除
delete from student where s_name='王菊';

#-- 写入
insert into student values('08' , '王菊' , '1990-01-20' , '男');
insert into student (s_id, s_name, s_birth, s_sex) 
values('08' , '王菊' , '1990-01-20' , '男');

# -- 更新
update student set s_sex='女' where s_name='王菊';

＃ --查询
select * from student where s_name='王菊';
```



[查询与统计进阶](查询与统计进阶.md)



