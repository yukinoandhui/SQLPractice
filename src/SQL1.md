## 题目描述

查找最晚入职员工的所有信息，为了减轻入门难度，目前所有的数据里员工入职的日期都不是同一天(sqlite里面的注释为--,mysql为comment)
CREATE TABLE `employees` (
`emp_no` int(11) NOT NULL, -- '员工编号'
`birth_date` date NOT NULL,
`first_name` varchar(14) NOT NULL,
`last_name` varchar(16) NOT NULL,
`gender` char(1) NOT NULL,
`hire_date` date NOT NULL,
PRIMARY KEY (`emp_no`));





- ORDER BY 根据指定的列对结果集进行排序，默认按照升序，降序 ORDER BY DESC
- LIMIT(m, n) 从第 m + 1 行开始取 n 条记录



```mysql
select * from employees order by hire_date desc limit 0,1;
```

