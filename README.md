# freshclass-database

```sql
CREATE DATABASE freshclass;
```

## User

```sql
CREATE TABLE User(Id int PRIMARY KEY Auto_increment,
                  FirstName varchar(100) NOT NULL, 
                  LastName varchar(100) NOT NULL, 
                  Emp_id char(6) NOT NULL, 
                  Email varchar(255) not null, 
                  DOB date NOT NULL,
                  Gender char(6) NOT NULL, 
                  Dept varchar(100) NOT NULL , 
                  Position varchar(100) NOT NULL, 
                  City varchar(100) NOT NULL, 
                  Phoneno bigint NOT NULL,
                  Password varchar(20) NOT NULL, 
                  Singup_Date timestamp default current_timestamp ,
                  check(Gender in ('Male','Female','Other'))
);
```

| Field       | Type         | Null | Key | Default           | Extra             |
|:------------|:-------------|:-----|:----|:------------------|:------------------|
| Id          | int          | NO   | PRI | NULL              | auto_increment    |
| FirstName   | varchar(100) | NO   |     | NULL              |                   |
| LastName    | varchar(100) | NO   |     | NULL              |                   |
| Emp_id      | char(6)      | NO   |     | NULL              |                   |
| Email       | varchar(255) | NO   | UNI | NULL              |                   |
| DOB         | date         | NO   |     | NULL              |                   |
| Gender      | char(6)      | NO   |     | NULL              |                   |
| Dept        | varchar(100) | NO   |     | NULL              |                   |
| Position    | varchar(100) | NO   |     | NULL              |                   |
| City        | varchar(100) | NO   |     | NULL              |                   |
| Phoneno     | bigint       | NO   |     | NULL              |                   |
| Password    | varchar(20)  | NO   |     | NULL              |                   |
| Singup_Date | timestamp    | YES  |     | CURRENT_TIMESTAMP | DEFAULT_GENERATED |


### INSERT VALUE INTO User TABLE

```sql
INSERT INTO  user(Id,Firstname,lastname,Emp_id,Email,DOB,Gender,dept,position,city,phoneno,password) values(null,'Prasanna','Venkatesh','A0001','prasanna.venkatesh@freshclass.com','2001-01-20','Male','Tech','Student','Thanjavur',9791836225,'Prasanna@2022');
```
```sql
INSERT INTO username,lastname,Emp_id,Email,DOB,Gender,dept,position,city,phoneno,password) values(2,'Chitra','Muthukumaran','E0001','chitra.muthukumaran@freshclass.com','2001-01-20','Female','Tech','coach','chennai',9791836225,'Chitra@2022');
```
```sql
INSERT INTO user(Id,Firstname,lastname,Emp_id,Email,DOB,Gender,dept,position,city,phoneno,password) values(3,'viaml','Raj','A0002','vimal.raj@freshclass.com','2001-01-20','Male','Design','Student','Pondicherry',9791836225,'Vimal@2022');
```
```sql
INSERT INTO user(Id,Firstname,lastname,Emp_id,Email,DOB,Gender,dept,position,city,phoneno,password) values(4,'kaushick','sing','A0003','kaushik.sing@fwsa.freshworks.com','2001-01-20','Male','Tech','Student','Chennai',9791836225,'Kaushick@2022');
```
```sql
INSERT INTO user(Id,Firstname,lastname,Emp_id,Email,DOB,Gender,dept,position,city,phoneno,password) values(5,'Haiden','Arulappan','A0004','haiden.arulappan@fwsa.freshworks.com','2001-01-20','Male','Tech','Student','Tirunelveli',9791836225,'Haiden@2022');
```
```sql
insert into user(Id,Firstname,lastname,Emp_id,Email,DOB,Gender,dept,position,city,phoneno,password) values(6,'deepak','Pannerselvam','A0005','deepak.pannerselvam@fwsa.freshworks.com','2001-01-20','Male','Design','Student','Chennai',9791836225,'Deepak@2022');

```
```sql
insert into user(Id,Firstname,lastname,Emp_id,Email,DOB,Gender,dept,position,city,phoneno,password) values(7,'Prasanna','Bharati','E0002','prasanna.bharati@freshclass.com','1990-05-04','Female','L&D','Coach','chennai',9791836225,'Prasanna@2022');
```
### User table with values

| Id | FirstName | LastName     | Emp_id | Email                                   | DOB        | Gender | Dept   | Position | City        | Phoneno    | Password      | Singup_Date         |
|:---|:----------|:-------------|:-------|:----------------------------------------|:-----------|:-------|:-------|:---------|:------------|:-----------|:--------------|:--------------------|
|  1 | Prasanna  | Venkatesh    | A0001  | prasanna.venkatesh@freshclass.com       | 2001-01-20 | Male   | Tech   | Student  | Thanjavur   | 9791836225 | Prasanna@2022 | 2022-03-20 08:06:48 |
|  2 | Chitra    | Muthukumaran | E0001  | chitra.muthukumaran@freshclass.com      | 2001-01-20 | Female | Tech   | coach    | chennai     | 9791836225 | Chitra@2022   | 2022-03-20 08:08:57 |
|  3 | viaml     | Raj          | A0002  | vimal.raj@freshclass.com                | 2001-01-20 | Male   | Design | Student  | Pondicherry | 9791836225 | Vimal@2022    | 2022-03-20 08:10:47 |
|  4 | kaushick  | sing         | A0003  | kaushik.sing@fwsa.freshworks.com        | 2001-01-20 | Male   | Tech   | Student  | Chennai     | 9791836225 | Kaushick@2022 | 2022-03-20 08:12:02 |
|  5 | Haiden    | Arulappan    | A0004  | haiden.arulappan@fwsa.freshworks.com    | 2001-01-20 | Male   | Tech   | Student  | Tirunelveli | 9791836225 | Haiden@2022   | 2022-03-20 08:13:01 |
|  6 | deepak    | Pannerselvam | A0005  | deepak.pannerselvam@fwsa.freshworks.com | 2001-01-20 | Male   | Design | Student  | Chennai     | 9791836225 | Deepak@2022   | 2022-03-20 08:14:03 |
|  7 | Prasanna  | Bharati      | E0002  | prasanna.bharati@freshclass.com         | 1990-05-04 | Female | L&D    | Coach    | chennai     | 9791836225 | Prasanna@2022 | 2022-03-20 08:15:56 |
