# BMI-Management-Sysytem
 


DATABASE MANAGEMENT SYSTEM PROJECT REPORT



NAME	REGISTRATION NO.	ROLL NO.
KARTIK BHARDWAJ	12105309	RK21PTA30

NAME:  KARTIK BHARDWAJ

SECTION:  K21PT PROGRAMME:  B. Tech CSE COURSE CODE :  INT306
PROJECT NAME : BMI MANAGEMENT SYSTEM



Submitted To:-   School of Computer Science and Engineering
                       Lovely Professional University, Phagwara
 
ACKNOWLEDGMENT
	

I would like to thank ‘Ms. Madhuri ‘mam for assigning me with this project. Through the project I can grasp more technical and have a hands-on practical experience with projects. Through it I was able to learn how a project is created and how necessary and crucial technical knowledge is. I am grateful to the faculty that has provided me with the necessary guidelines.




DATE: 16th November 2022 











TABLE OF CONTENTS

CONTENT 		PAGE NO.
1.	INTRODUCTION	……………………………………………………………..	4
2.	OBJECTIVES..........................................................................................5
3.	APPLICABILITY OF THE PROJECT	6
4.	SOURCE CODE	8
5.	RESULTS	14
6.	ADVANTAGES AND DISADVANTAGES	16
7.	CONCLUSION	18



 
INTRODUCTION

•	The present project is directed to the Bmi management system which educates the participant in nutrition and in developing a lifestyle necessary to reach and consistently maintain one's bmi index.

•	More particularly, the project provides an analysis of physical parameters such as gender, height ,weight and bmi index which determines an individualized weight control program. 


•	It is well known that a large percentage of the population is overweight. Otherwise, itis likely to be overweight and constantly trying to lose weight by experimenting with various diet programs to reduce their caloric and carbohydrate intake.
•	Maintaining a reasonable balance between the caloric intake and the energy expended during the day is necessary in order to lose weight and continue a constant weight.


•	Our database schema is consisted of three databases which records personal details , branch details and city information respectively. Database is made using SQL. We have used PLSQL for our system  where account no and transaction option is asked   


•	This software is supported to eliminate and in some cases reduce the hardships faced by this existing system. Moreover this system is designed for the particular need of the company to carry out operations in a smooth and effective manner.

OBJECTIVES
	The objective of this project is developing Bmi management system for adults between 20 – 60 years.
	This application utilizes a computer analysis of a,body mass index, basal metabolic rate, body fat percent, heart rate, exercise level and taste preferences to provide a menu of a specified number of calories to maintain a reasonable weight.
	The system provides consultation with a dietitian for a participant to recognize the deficiencies in the past diet. 
	The system further provides consultation to effect behavior modification of the participant by offering instruction in nutrition.
	Assessment of a patient should include the evaluation of body mass index (BMI), waist circumference, and overall medical risk. To estimate BMI , Body Mass Index with simple calculation using a person's height and weight. The formula is BMI = kg/m2 where kg is a person's weight in kilograms and m2 is their height in metres squared. 
Classification of BMI
Category	BMI
Underweight	<18.5 kg/m2
Normal weight	18.5-24.9 kg?m2
Over weight	25-29.9kg/m2
Obesity(Class1)	30-34.9 kg/m2
Obesity(Class2)	35-39.9 kg/m2
Extreme obesity(Class3)	 ≥40 kg/m2

 
APPLICABILTY OF THE PROJECT

1.	In this project, we will be discussing that the BMI is an essential public health tool for monitoring progress towards the Company’s target, but that its routine use in the ways recommended in these reports presents a number of difficulties. The use of the BMI in the clinical management of employees is essential.

2.	In addition, BMI may be more useful at predicting future rather than current health. Those who are healthy and overweight or obese are more likely to develop diabetes or other negative health consequences over time, according to studies.
3.	As a single measure, BMI is clearly not a perfect measure of health. But it’s still a useful starting point for important conditions that become more likely when a person is overweight or obese. In my view, it’s a good idea to know your BMI. But it’s also important to recognize its limitation.             
          
About SQL and PL/SQL used in Project

This project is made by using simple statements and query of SQL and the functions are added by using PL/SQL in this project.
SQL : SQL is a domain-specific language used in programming and designed for managing data held in a relational database management system, or for stream processing in a relational data stream management system.
•	SQL is used for creating the table .
•	We have three tables in our project which is created by using of sql.
•	We used some basics statements and query as create table, insert table , show table , where , update.
PL/SQL: PL/SQL is Oracle Corporation's procedural extension for SQL and the Oracle relational database. PL/SQL is available in Oracle Database, Times Ten in-memory database, and IBM Db2. Oracle Corporation usually extends PL/SQL functionality with each successive release of the Oracle Database







SOURCE CODE
select *from main_table;

Create table Table1(
Emp_id int ,
Emp_name varchar(20)
);
drop table Table1;
insert into Table1(Emp_id,Emp_name)select Id,Employee from main_table;
select *from Table1;

create table Table2(
Empl_id int primary key,
Emp_name varchar(20),
Department_name varchar(50)
);

drop table Table2;

insert into Table2(Empl_id,Emp_name,Department_name)select Id,Employee,Department from main_table;
select *from Table2;

Create table Table3(
Emplo_id int,
Employee_name varchar(20),
Emp_weight int,
Bmi_index int,
constraint fk foreign key(Emplo_id) references Table2(Empl_id));

drop table table3;

insert into Table3(Emplo_id,Employee_name,Emp_weight,Bmi_index)select Id,Employee,weight,bmi_index from main_table;

select *from Table3;

Create table Table4(
Emp_id int,
Emp_name varchar(50),
Emp_gender varchar(50)
);

drop table Table4;

insert into Table4(Emp_id,Emp_name,Emp_gender)select id,Employee,gender from main_table;

select *from Table4;

Create table Table5(
Emp_id int,
Emp_name varchar(50),
Bmi_index int
);
drop table Table5;
insert into Table5(Emp_id,Emp_name,Bmi_index)select id,Employee,bmi_index from main_table;
select *from table5;

Create table Table6(
Emp_id int,
Emp_name varchar(50),
Emp_height int
);
drop table Table6;
insert into table6(Emp_id,Emp_name,Emp_height)select id, employee,height from main_table;
select *from table6;


QUERIES...........


select distinct Emp_height from table6;

select *from Table5 where Emp_name='ROSS';

select Employee_name from Table3 where Emp_weight between 150 and 300;

select Emp_name from Table2 where Department_name in('Office furnishings','Appliances','Envelops');

select *from Table3 where Employee_name like'L%';

select *from Table4 where Emp_gender ='Male';
select *from Table5 where Bmi_index >4;

PLSQL.............
            DECLARE
    Height number ;
    Weight number ;
    BMI number ;
BEGIN
    Height := 1.7;
    weight := 78;
    if Height = 0 THEN
        dbms_output.put_line('ERROR');
    ELSE
        BMI := Weight / (Height*Height);
        dbms_output.put_line('BMI = '||BMI);
    END IF;
end;
PRIMARY DATA SET:







 
RESULTS










































ADVANTAGES OF 
BMI MANAGEMENT SYSTEM

•	BMI is a simple, inexpensive, and noninvasive surrogate measure of body fat. In contrast to other methods, BMI relies solely on height and weight and with access to the proper equipment, individuals can have their BMI routinely measured and calculated with reasonable accuracy

•	Furthermore, studies have shown that BMI levels correlate with body fat and with future health risks. High BMI predicts future morbidity and death. Therefore, BMI is an appropriate measure for screening for obesity and its health risks.

•	As stated, BMI helps measure the obesity rate in people. Observing the changes in BMI values helps doctors evaluate the obesity levels in people over time.

•	When the BMI of a significant population is calculated, it helps researchers gather data that can be used to examine the obesity epidemic.

•	It helps researchers determine the pattern of diet that results in obesity in a large group of people.

•	Knowing the BMI value of an individual, doctors can mitigate the health risks arising due to obesity.


DISADVANTAGES OF
     BMI MANAGEMENT SYSTEM



Much like any other body fat measurement technique, BMI is equally flawed and has drawbacks. These disadvantages include -
 
•	BMI is a simple mathematical formula that measures body fat based on your height and weight.

•	It does not take into account the source of the weight - whether it is from lean tissue or fat.

•	So, even when you have an average weight, based on the BMI value, you might fall under the overweight category.

•	BMI does not distinguish between the type of fat one carries - whether it is subcutaneous or visceral fat.

•	Subcutaneous fat is the fat that is under your skin and influences the way you look. Visceral fat is mostly hidden and is located deep in the abdomen region surrounding the internal organs. It imposes a high risk to one’s health






 
Conclusion
The BMI is the best available tool for monitoring progress in the campaign against obesity. Notwithstanding the pitfalls outlined above, a robust quality assured anonymised data collection and analysis system could provide national and local data that would inform the planning and evaluation of intervention programmes.
The use of BMI in the way proposed by the Select Committee and the USA Expert Reports presents significant challenges and gives rise to several unsubstantiated hypotheses, for example:
•	That feedback of BMI results to all employees would result in lifestyle changes and a fall in mean BMI across the whole population of Office employees.
•	
•	That the use of cut offs to identify employees whose BMI exceeds specified levels would result in more overweight and/or obese employees taking effective steps to control their weight.
•	That the benefits of any such programme would substantially exceed any harms.
•	That sufficient professional expertise can be made available to manage the inevitable increase in referrals for obesity assessment and weight control.









THANK YOU.
