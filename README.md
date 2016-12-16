
#Fall16Team-1
#TPMS - CMPE 272 GROUP PROJECT UNDER THE GUIDANCE OF PROF.RAKESH RANJAN
Tyre Pressure Monitoring System using Internet of Things.


#Team Members: 
Harsh Mehta
Disha Sheth
Aishwarya Keerty
Bhavankumar Pandya 

#PROJECT DELIVERABLES
1) [Project Presentation](https://github.com/SJSU272Lab/TPMS/blob/master/Project%20presentation)
2) [Project Report](https://github.com/SJSU272Lab/TPMS/blob/master/Project%20report)

#Abstract: 
Tyre Pressure Monitoring System are safety devices installed to warn the user that atleast one or more tyres are either under or over inflated. The Transportation Recall Enhancement, Accountability, and Documentation Act dictates that vehicles in United States must include a tyre pressure monitoring system of some kind. There has been a constant surge in accidents due to uncertainty about the tyre pressure. Therefore, to  address this problem, we are proposing a simple, economic and practical solution in the form of a mobile application which alerts the user when the pressure goes down the permissible limit. This can be achieved using Sensor Technology and IOT.


The main idea is to monitor the pressure using a sensor, attached to the tyre, then push the data to the cloud servers.When the tyre pressure is below or above the required limit, push notification will be sent to the user as an alert.


#Competitive Landscape: 
Low pressure in tyres can be displayed either using indirect TPMS or direct TPMS. Indirect TPMS relies on speed sensors whereas direct TPMS relies on pressure monitoring sensors. There are very few software applications available to analyse low pressure in tyres. Most of the available systems are not economical. For example: 
Garmin Tyre pressure monitoring sensors are available at $70 per unit. 


#Differentiator: 
Our proposed solution will provide the benefits of both modern hardware and software technologies at a reasonable cost. Our application will take data from the server and alert the user when the pressure drops below the limit. 


#Technology Stack:
Programming Languages: Java, Javascript
Frameworks: Mean Stack
DB: Temporal 
Angular UI: Angular Material
Hardware: Raspberry Pi, Pressure Sensors

Database Service: AWS RDS
a) We choose RDS as our database to store sensor data. AWS Relational Database Service (RDS) is a web based database which works as a relation database system.
 
 ![image](https://cloud.githubusercontent.com/assets/22584180/21253687/61364bca-c315-11e6-9ab2-8c6849b1dbf4.png)

b) Enterprise Computing Platform: Eclipse
We write the backend of the project in Java language, front-end in Html, css and javascript. We use Eclipse as our computing platform.

![image](https://cloud.githubusercontent.com/assets/22584180/21253736/992f25ce-c315-11e6-82ff-c8db7d21d9b9.png)
 

c)  front end design: HTML, CSS, Bootstrap, jQuery

![image](https://cloud.githubusercontent.com/assets/22584180/21253753/bfcee41c-c315-11e6-94fd-13752267b9df.png)






#Activity flow diagram is added to the repository.

#PERSONAS AND USER STORIES :

#Persona 1: Car-driver
Name : XXXX XXXX
Gender : Male/Female
Primary Goal : Car driving and depending on the notification received for inappropriate tyre pressure,take proper action.


#Persona 2: Car-owner
Name : XXXX XXXX
Gender : Male/Female
Primary Goal : Depending on the notification received for inappropriate tyre pressure,take proper action.


#User Story 1 : 
As a car driver, I can register and then login to the mobile application to receive notification at proper time and thus avoid accidents.


#User Story 2 : 
As a car driver, I can receive notifications for lower tyre pressure and take appropriate action for the tyre.


#User Story 3 : 
As a car owner, I can register and then login to the application to receive and track notifications to notify the car driver.


#User Story 4 : 
As a car owner, I can receive notifications for lower tyre pressure and inform and instruct the driver to take proper action outside the system.



#FLOW DIAGRAM


![image](https://cloud.githubusercontent.com/assets/22584180/21253769/d966796c-c315-11e6-8e30-aca6811b3ea0.png)




Above diagram shows the complete flow of data in the application. 
Virtual Sensors try to monitors the tyre pressure and once the pressure reduces below certain value, the notification is sent to the driver on his mobile application.

He also will be able to track down the sensors using web application. He will be able to work add new sensors, configure them to suit his needs.

We have used AWS RD5 service for storing the user database.

![image](https://cloud.githubusercontent.com/assets/22584180/21253800/0fda6486-c316-11e6-9949-2474eaba1327.png)


#SEQUENCE DIAGRAM
![image](https://cloud.githubusercontent.com/assets/22584180/21253820/341fd5a6-c316-11e6-8579-237852d56f92.png)

#DATABASE DESIGN
Tables

- User_master
Column name
type
length
constraint
user_id
int
11
Primary key
user_fname
Varchar
255 
no
user_lname
Varchar
255
no
user_status
Varchar
255
no
NUMBER_SENSORs
Varchar
255
no
user_email
Varchar
255
no
user_password
Varchar
255
no
phone
Varchar
255
no
Address
Varchar
255
no
city
Varchar
255
no
zipcode
Varchar
255
no
state
Varchar
255
no
user_type
Varchar
255
no
creation_date
timestamp
current_timestamp
no
last_login_date
timestamp
null
no

- Sensor_master

Column name
type
length
constraint
sensor_id
varchar
255
primary_key
user_id
int
11
foreign_key
latitude
varchar
255
no
longitude
varchar
255
no
sensor_status
varchar
255
no
public_ip
varchar
255
no
private_ip
varchar
255
no
creation_date
timestamp
null
no
sensor_tag_key
varchar
255
no
sensor_tag_name
varchar
255
no
sensor_tag_value
varchar
255
no
hub_id
varchar
255
no

- Hub_master

Column name
type
length
constraint
hub_id
int
11
primary_key
no_of_server
Int 
11
no
hub_status
varchar
255
no
cpu_utilization
varchar
255
no

- Temp_data

Column name
Type 
length
constraint
sensor_id
varchar
255
Foreign key

temp
int
11
no
sensor_tag_value
varchar
255
no
sensor_status
varchar
255
no
time_stamp
timestamp
null
no
user_id
varchar
255
no

- Utilization

sensor_id
varchar
255
Foreign key
cput_data
int
11
no
date
timestamp
null
no














#MOBILE APPLICATION SCREENSHOTS


![image](https://cloud.githubusercontent.com/assets/22584180/21253891/b3d8548a-c316-11e6-8c5f-2650b29bad9f.png)  ![image](https://cloud.githubusercontent.com/assets/22584180/21253899/bbc4987a-c316-11e6-8864-355e33aaf8fc.png)






















#WEB-APPLCATION
 
 ![image](https://cloud.githubusercontent.com/assets/22584180/21253965/1743b8fc-c317-11e6-9474-9dd0bf820358.png)


![image](https://cloud.githubusercontent.com/assets/22584180/21253973/20de3a72-c317-11e6-9c81-598d367896cf.png)


![image](https://cloud.githubusercontent.com/assets/22584180/21253977/27c83342-c317-11e6-9da1-f46232c90b95.png)



![image](https://cloud.githubusercontent.com/assets/22584180/21253985/34c77bb6-c317-11e6-9c29-a7605af0fa01.png)

 
 
  
 
 
 
  
 
  
 
 

