# SPRACTICE

create database school
use school
create table student_info(S_ID INT identity primary key,
S_NAME VARCHAR(70),
S_ROLL_NO INT ,
S_SUBJECT VARCHAR(80),
S_ADDRESS VARCHAR(90),
S_FATHER_NAME VARCHAR(60))

INSERT INTO  student_info values('UPASANA',21,'SCIENCE','HAWELI','MR_VIRAJ'),
('RUHH',56,'MATH','AMROHA','MR_MANUJ'),
('NAINA',22,'DRAWING','DELHI','MR_MANAV'),
('KUHI',12,'SOCIAL ','GURUGAUN','MR_RAJEEV'),
('YUVRAAJ',33,'ENGLISH','NOIDA','MR_UMANG')


CREATE table department_info5
(D_ID INT IDENTITY PRIMARY KEY,
D_NO INT,
D_BUILDING VARCHAR(90),
D_HEAD VARCHAR(80),
S_ID INT  FOREIGN KEY REFERENCES student_info(S_ID)
)
select * from department_info5
select * from student_info

INSERT INTO department_info5 VALUES
(11,'CS','RANJAN KUMAR',4),
(13,'MG','NITISH ROY',3),
(14,'DB','MOHINI AULAKH',2),
(15,'HR','ANMOL AARYA',1) 

DROP DATABASE SCHOOL

select s.S_NAME,D.D_HEAD from
 Student_info s
 join department_info5 d on s.S_ID=d.S_ID
 --------self join---------------
 select s.S_NAME,d.S_ADDRESS from student_info s ,student_info d where s.S_ID= d.S_ID

 select s.S_FATHER_NAME,s.S_SUBJECT,d.D_HEAD,d.D_BUILDING FROM student_info s INNER JOIN  department_info5 d   on s.S_ID=d.S_ID

 SELECT S_FATHER_NAME FROM Student_info FULL JOIN department_info5 ON Student_info .S_ID=department_info5.S_ID

 SELECT* INTO STUDENT1 FROM student_info
 SELECT * FROM STUDENT1
 SELECT TOP 2 * FROM student_info
 SELECT TOP 80 PERCENT *FROM student_info

 SELECT S_FATHER_NAME FROM student_info
 UNION ALL
 SELECT  D_BUILDING FROM department_info5

 SELECT * FROM student_info WHERE S_FATHER_NAME like'%J' 

 ---------------------------INNER JOIN-------------------------------
 SELECT * FROM student_info  as a INNER JOIN department_info5 as b  on A.S_ID=B.S_ID

 -----------------------------------LEFT JOIN------------------------------------------
  SELECT * FROM student_info  as a LEFT JOIN department_info5 as b  on A.S_ID=B.S_ID

  ------------------------------------------RIGHT JOIN---------------------------
    SELECT * FROM student_info  as a RIGHT JOIN department_info5 as b  on A.S_ID=B.S_ID
	---------------------------------------FULL JOIN------------------------------------------

    SELECT * FROM student_info  as a FULL JOIN department_info5 as b  on A.S_ID=B.S_ID
	-----------------------------------------SELF JOIN-------------------------------
   select s.S_NAME,d.S_ADDRESS from student_info s ,student_info d where s.S_ID= d.S_ID


   --------------------------------------CROSS JOIN--------------------------------------

    SELECT * FROM student_info    CROSS JOIN  department_info5


-----------------------------------SINGLE TABLE CROSS JOIN-------------------------------
	 SELECT * FROM student_info  as a CROSS JOIN student_info






 

 SELECT * FROM student_info


 ALTER VIEW STUDENT_VI 
 AS 
 
 SELECT * FROM department_info5
 DELETE    FROM department_info5   WHERE D_ID=2


SELECT * FROM STUDENT_VI


