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