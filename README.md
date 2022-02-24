# freshclass-database

```syntax
CREATE DATABASE freshclass;
```

## students
```syntax
 CREATE TABLE Students(Id int PRIMERY KEY AUTO_INCREMENT, Firstname varchar(100) NOT NULL, Lastname varchar(100) NOT NULL, StudId char(6) NOT NULL UNIQUE, Squadname varchar(20) NOT NULL, Department varchar(40) DEFAULT 'Technology', Gender char(5) NOT NULL, DOB date NOT NULL, Email varchar(100) NOT NULL UNIQUE, City varchar(50) NOT NULL, Phoneno int NOT NULL, Password char(10) NOT NULL, Github varchar(255), Slack varchar(255));
```

## coaches
```syntax
 CREATE TABLE Coaches(Id int PRIMERY KEY AUTO_INCREMENT, Firstname varchar(100) NOT NULL, Lastname varchar(100) NOT NULL, StudId char(6) NOT NULL UNIQUE, Gender char(5) NOT NULL, DOB date NOT NULL, Email varchar(100) NOT NULL UNIQUE, City varchar(50) NOT NULL, Phoneno int NOT NULL, Password char(10) NOT NULL);
```

## attendence
```syntax
CREATE TABLE Attendence(Id int, AttendenceDate date NOT NULL, Attendence tinyint(1) NOT NULL, FOREIGN KEY(Id) REFERENCES Students(Id));
```

## schedules
```syntax
CREATE TABLE Schedules(Classname varchar(20) NOT NULL, SchaeduleDate date NOT NULL, StartTime time NOT NULL, EndTime time NOT NULL);
```

## assignment
```syntax
CREATE TABLE assignment(Subjectname varchar(20) NOY NULL, SubmissionDate date NOT NULL);
```

## chat
```syntax
CREATE TABLE Chat(Id int, Chats varchar NOT NULL, FOREIGN KEY(Id) REFERENCES Students(Id));
```