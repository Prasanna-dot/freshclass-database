# freshclass-database

```syntax
CREATE DATABASE freshclass;
```

## students
```syntax
 CREATE TABLE Students(Id int PRIMARY KEY AUTO_INCREMENT, Firstname varchar(100) NOT NULL, Lastname varchar(100) NOT NULL, StudId char(6) NOT NULL UNIQUE, Squadname varchar(20) NOT NULL, Department varchar(40) DEFAULT 'Technology', Gender char(5) NOT NULL, DOB date NOT NULL, Email varchar(100) NOT NULL UNIQUE, City varchar(50) NOT NULL, Phoneno int NOT NULL, Password char(10) NOT NULL, Github varchar(255), Slack varchar(255));
```

| Field      | Type         | Null | Key | Default    | Extra          |
|:-----------|:-------------|:-----|:----|:-----------|:---------------|
| Id         | int          | NO   | PRI | NULL       | auto_increment |
| Firstname  | varchar(100) | NO   |     | NULL       |                |
| Lastname   | varchar(100) | NO   |     | NULL       |                |
| StudId     | varchar(6)   | NO   | UNI | NULL       |                |
| Squadname  | varchar(20)  | NO   |     | NULL       |                |
| Department | varchar(40)  | YES  |     | Technology |                |
| Gender     | varchar(5)   | NO   |     | NULL       |                |
| DOB        | date         | NO   |     | NULL       |                |
| Email      | varchar(100) | NO   | UNI | NULL       |                |
| City       | varchar(50)  | NO   |     | NULL       |                |
| Phoneno    | int          | NO   |     | NULL       |                |
| Password   | varchar(10)  | NO   |     | NULL       |                |
| Github     | varchar(255) | YES  |     | NULL       |                |
| Slack      | varchar(255) | YES  |     | NULL       |                |

## coaches
```syntax
 CREATE TABLE Coaches(Id int PRIMARY KEY AUTO_INCREMENT, Firstname varchar(100) NOT NULL, Lastname varchar(100) NOT NULL, StudId char(6) NOT NULL UNIQUE, Gender char(5) NOT NULL, DOB date NOT NULL, Email varchar(100) NOT NULL UNIQUE, City varchar(50) NOT NULL, Phoneno int NOT NULL, Password char(10) NOT NULL);
```

| Field     | Type         | Null | Key | Default | Extra          |
|:----------|:-------------|:-----|:----|:--------|:---------------|
| Id        | int          | NO   | PRI | NULL    | auto_increment |
| Firstname | varchar(100) | NO   |     | NULL    |                |
| Lastname  | varchar(100) | NO   |     | NULL    |                |
| StudId    | char(6)      | NO   | UNI | NULL    |                |
| Gender    | char(5)      | NO   |     | NULL    |                |
| DOB       | date         | NO   |     | NULL    |                |
| Email     | varchar(100) | NO   | UNI | NULL    |                |
| City      | varchar(50)  | NO   |     | NULL    |                |
| Phoneno   | int          | NO   |     | NULL    |                |
| Password  | char(10)     | NO   |     | NULL    |                |

## schedules
```syntax
CREATE TABLE Schedules(Classname varchar(20) NOT NULL, SchaeduleDate date NOT NULL, StartTime time NOT NULL, EndTime time NOT NULL);
```
| Field         | Type        | Null | Key | Default | Extra |
|:--------------|:------------|:-----|:----|:--------|:------|
| Classname     | varchar(20) | NO   |     | NULL    |       |
| SchaeduleDate | date        | NO   |     | NULL    |       |
| StartTime     | time        | NO   |     | NULL    |       |
| EndTime       | time        | NO   |     | NULL    |       |

## attendence
```syntax
CREATE TABLE Attendence(Id int, AttendenceDate date NOT NULL, Attendence tinyint(1) NOT NULL, FOREIGN KEY(Id) REFERENCES Students(Id));
```

| Field          | Type       | Null | Key | Default | Extra |
|:---------------|:-----------|:-----|:----|:--------|:------|
| Id             | int        | YES  | MUL | NULL    |       |
| AttendenceDate | date       | NO   |     | NULL    |       |
| Attendence     | tinyint(1) | NO   |     | NULL    |       |


## assignment
```syntax
CREATE TABLE assignment(Subjectname varchar(20) NOT NULL, SubmissionDate date NOT NULL);
```

| Field          | Type        | Null | Key | Default | Extra |
|:---------------|:------------|:-----|:----|:--------|:------|
| Subjectname    | varchar(20) | NO   |     | NULL    |       |
| SubmissionDate | date        | NO   |     | NULL    |       |

## chat
```syntax
CREATE TABLE Chat(Id int, Chats varchar(1000) NOT NULL, FOREIGN KEY(Id) REFERENCES Students(Id));
```
| Field | Type          | Null | Key | Default | Extra |
|:------|:--------------|:-----|:----|:--------|:------|
| Id    | int           | YES  | MUL | NULL    |       |
| Chats | varchar(1000) | NO   |     | NULL    |       |
