# Daily-Diary
# TRAINING AND INTERNSHIP PROGRAMME :point_down:

All about the 6 month training and internship

 ## :arrow_right: *DAY 1 (12/07/2022)*
### *Learning new Things*


- In the morning we have meeting with HS Rai Sir(mentor of our training).
- He gave us the instructions and welcome us in the SDC(Software developement Centre)
- He told us to work on the things:
-- Linux, Apache, Mysql & Mariadb , php.


## :arrow_right: *DAY 2 (13/07/2022)*

- Today I started working on learning about LAMP.
- I go through the documentation https://www.javatpoint.com/what-is-lamp.

### What I learn Today:-

Linux: Linux started in 1991. It sets the foundation for the stack model. All other layers are run on top of this layer.
It is an open-source and free operating system. It is endured partly because it's flexible, and other operating systems are harder to configure.
     
Apache: The second layer consists of web server software, typically Apache Web Server. This layer resides on top of the Linux layer.
Apache HTTP Server is a free web server software package made available under an open-source license. It used to be known as Apache Web Server when it     was created in 1995.
    
MySQL: MySQL is a relational database management system used to store application data. It is an open-source and keeps all the data in a format that       can easily be queried with the SQL language.
    
PHP: The scripting layer consists of PHP and other similar web programming languages.
The PHP open-source scripting language works with Apache to create dynamic web pages. We cannot use HTML to perform dynamic processes such as pulling       data out of a database.


## :arrow_right: *DAY 3 (14/07/2022)*


- Today I learn a lot of stuff related to linux, different operating systems.
- I go through the documentation which is provided at https://www.guru99.com/install-linux.html and learn about the linux distrubutions.
- I also learn theoretically how to install linux in our laptop or pc but there is a lot of difference to learn theoratically and perform practically.
- I got so many error while installing the linux even my window is destroyed due to some lack of information.
- Now I have no operating system in my pc.
- After a lot of struggle when I am unable to find the the solution of this then I decide to this tommorow in the presence of some expert who is having some knowledge of linux and the stuff related to distributions.

##  :arrow_right: *DAY 4(15/07/2022)*

- In the morning Pranvir help me to resolve the errors which I got during the installation of linux.
- Now I have Ubuntu linux distribution in my pc.
- This took my whole day and I learn a lot of things like how to install linux in our laptop practically.

##  :arrow_right: *DAY 5 (16/07/2022)*

## Saturday

##  :arrow_right: *DAY 6(17/07/2022)*

## Sunday

##  :arrow_right: *DAY 7 (18/07/2022)*

- Today Rai Sir added our whole team in the google group and told us to go through the documentation http://www.slideshare.net/sandeepkmadaan/mailing-guidelines 
- I read all the guide lines which is mentioned in the mailing guidelines.
- I Read about the frappe framework, its functionalities and advantage along with its installation process.

##  :arrow_right: *DAY 8 (19/07/2022)*

- Today the day started with the meeting which we have with our mentors and our SDC senoirs. They all shared their experiences and also gave a brief direction about our work.
- I learn a lot things from them.
- Today we all send our first mail in greatdeveloper group.
- In the mail we describe our skills and our intrests.

##  :arrow_right: *DAY 9 (20/07/2022)*

- Today I started work on installing the frappe framework in our laptop.
- For installing this I go go through the following steps:-

# Guide-to-Install-Frappe-ERPNext-in-Ubuntu-22.04-LTS
A complete Guide to Install Frappe Bench in Ubuntu 22.04 LTS and install Frappe/ERPNext Application

### Pre-requisites 

      Python 3.6+
      Node.js 14+
      Redis 5                                       (caching and real time updates)
      MariaDB 10.3.x / Postgres 9.5.x               (to run database driven apps)
      yarn 1.12+                                    (js dependency manager)
      pip 20+                                       (py dependency manager)
      wkhtmltopdf (version 0.12.5 with patched qt)  (for pdf generation)
      cron                                          (bench's scheduled jobs: automated certificate renewal, scheduled backups)
      NGINX                                         (proxying multitenant sites in production)



### STEP 1 Install git
    sudo apt-get install git

### STEP 2 install python-dev

    sudo apt-get install python3-dev

### STEP 3 Install setuptools and pip (Python's Package Manager).

    sudo apt-get install python3-setuptools python3-pip

### STEP 4 Install virtualenv
    
    sudo apt-get install virtualenv
    
  CHECK PYTHON VERSION 
  
    python3 -V
  
  IF VERSION IS 3.8.X RUN
  
    sudo apt install python3.8-venv

  IF VERSION IS 3.10.X RUN
  
     sudo apt install python3.10-venv

### STEP 5 Install MariaDB

    sudo apt-get install software-properties-common
    sudo apt install mariadb-server
    sudo mysql_secure_installation
    
    
### STEP 6  MySQL database development files

    sudo apt-get install libmysqlclient-dev

### STEP 7 Edit the mariadb configuration ( unicode character encoding )

    sudo nano /etc/mysql/mariadb.conf.d/50-server.cnf

add this to the 50-server.cnf file

    
     [server]
     user = mysql
     pid-file = /run/mysqld/mysqld.pid
     socket = /run/mysqld/mysqld.sock
     basedir = /usr
     datadir = /var/lib/mysql
     tmpdir = /tmp
     lc-messages-dir = /usr/share/mysql
     bind-address = 127.0.0.1
     query_cache_size = 16M
     log_error = /var/log/mysql/error.log
    
     [mysqld]
     innodb-file-format=barracuda
     innodb-file-per-table=1
     innodb-large-prefix=1
     character-set-client-handshake = FALSE
     character-set-server = utf8mb4
     collation-server = utf8mb4_unicode_ci      
     
     [mysql]
     default-character-set = utf8mb4

Now press (Ctrl-X) to exit

    sudo service mysql restart

### STEP 8 install Redis
    
    sudo apt-get install redis-server

### STEP 9 install Node.js 14.X package

    sudo apt install curl 
    curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
    source ~/.profile
    nvm install 14.15.0  

### STEP 10  install Yarn

    sudo apt-get install npm

    sudo npm install -g yarn

### STEP 11 install wkhtmltopdf

    sudo apt-get install xvfb libfontconfig wkhtmltopdf
    

### STEP 12 install frappe-bench

    sudo -H pip3 install frappe-bench
    
    bench --version
    
### STEP 13 initilise the frappe bench & install frappe latest version 

    bench init frappe-bench 
    
    cd frappe-bench/
    bench start
    
### STEP 14 create a site in frappe bench 
    
    bench new-site dcode.com
    
    bench use dcode.com

### STEP 15 install ERPNext latest version in bench & site

    bench get-app erpnext --branch version-13
    ### OR
    bench get-app https://github.com/frappe/erpnext --branch version-13

    bench --site dcode.com install-app erpnext
    
    bench start


##  :arrow_right: *DAY 10 (21/07/2022)*

- I get a lot of errors in the installation of frappe framework in my pc which is mentioned in the mails.
- A lot of errors is solved by searching a lot of errors are resolved by ourself also.
- Today I successfullly install the frappe framework in our laptop.

## :arrow_right: *DAY 11 (22/07/2022)*

- Today our task is to create library management system in our laptop by learning through the frappe documentation https://frappeframework.com/
- In the library Management System we have to do the following things:-

We will build a simple Library Management System in which the Librarian can log in and manage Articles and Memberships. We will build the following models:

   Article: A Book or similar item that can be rented.
   
   Library Member: A user who is subscribed to a membership.
   
   Library Transaction: An Issue or Return of an article.
   
   Library Membership: A document that represents an active membership of a Library Member.
   
   Library Settings: Settings that define values like Loan Period and the maximum number of articles that can be issued at a time.

##  :arrow_right: *DAY 12 (23/07/2022)*

## Saturday

##  :arrow_right: *DAY 13(24/07/2022)*

## Sunday

## :arrow_right: *DAY 14 (25/07/2022)*

- Today I learn how we can create our site and app in frappe folder:-
- Commands which use to create app is
```
bench new-app {app_name}
```
- For creating new site
```
bench new-site {site_name}
```
- Today I complete the following steps of Library Management System:-

Frappe Framework Tutorial

Install and Setup Bench

Create an App

Create a Site

Create a DocType

DocType Features

## :arrow_right: *DAY 15 (26/07/2022)*

- Today I completed the pending steps of library management system

Controller Methods

Types of DocType

Form Scripts

Web View Pages

- Today I complete the library management system and decide to give the presentation on it.


## :arrow_right: *DAY 16 (27/07/2022)*


- Today after the presentation Rai Sir give me a task to understand the chat-app which is created in the frappe-framework v13. 
- As I searched a lot but I am unable to find the solution how we can download the prebuild apps in our laptop.
- At this stage Tanveer help me and give me a hint that we can install prebuild apps by the following commands:-
```
bench get-app {app_name}
bench --site {site_name} install-app {app_name}
```

## :arrow_right: *DAY 17 (28/07/2022)*

- Today my work is to understand the chat-app ,which doctypes are created and all the stuff related to this.
- First I install the chat-app in our laptop and see all the files which is created in the chat-app.
- During the exploratoin I learned a new thing which is user and roles in the frappe framework.
- From the above I learned how we can give different roles and different roles permissions to different users.

## :arrow_right: *DAY 18 (29/07/2022)*

- Today our whole team task is to understand the LMS(Learning Management System) in the Frappe framework.
- Reading Education Domain with fully understanding

### Setup :

- Program
- Course
- Topic
- Instructor
- Room
- Student Category
- Acadmic Term
- Acadmic year
- Education Settings

## :arrow_right: *DAY 19 (30/07/2022)*

- Today seminar off because our Infosys SP & DSE Exam
- Prepare for Exam

## :arrow_right: *DAY 20 (31/07/2022)*

## Sunday

### :arrow_right: *DAY 21 (01/08/2022)*

- Today Satinder Sir gave us a work to get a backup from an server which is at CC1 lab.
- We(me and Tanveer) are selected to do this task.
- First we open the CPU and get the Hard Drive from that CPU after that we connected that Hard Drive to another pc and take the backup files which is useful.

### :arrow_right: *DAY 22 (02/08/2022)*

- There is one another file in the hard disk which is a script which is user to create the users automatically.
- We take the backup of the file and send the script to the Rai Sir.

### :arrow_right: *DAY 23 (03/08/2022)*

- Implement education domain in test server (gne11.gndec.ac.in)
- Create Programs, Courses
- Allot room according to course, Programs and So on.

### :arrow_right: *DAY 24 (04/08/2022)*

- As all are not reading the mails properly so Sir assign Komal to give a brief representation on the mails guidelines.
- All are prepared themselves for the presentation because Sir told us that they can ask any question to anyone regarding the mails and guidelines.
- In the evening Komalpreet gave their presentation.   

### :arrow_right: *DAY 25 (05/08/2022)*

- Today I will try explore my chat-app work.
- In this I am exploring the doctypes created by the chat app.
- How chat-app works for non user or website user.

### :arrow_right: *DAY 26 (06/08/2022)*

- Saturday seminar
- understand the use of make command
- how we can write script of it

### :arrow_right: *DAY 27 (7/08/2022)*

## Sunday

### :arrow_right: *DAY 28 (08/08/2022)*


- getting error when i'm using context script
- search the solution for it.
- work on fee structure on education domain.

### :arrow_right: *DAY 29 (09/08/2022)*

- Today I explore how we can edit homepage and login page.
- I am also work on how we can give appropriate roles to different users.
- In the evening there is a presentation given by tanveer on LMS.

### :arrow_right: *DAY 30 (10/08/2022)*

- Today I explore How can we me make users in bulk.
- It is a very simple process to do so.
- First go to the user list click on import data.
- Click on get csv and select the fields according to your needs.
- After that create put all the data in csv file and upload it.

### :arrow_right: *DAY 31 (11/08/2022)*

## Raksha Bandhan

### :arrow_right: *DAY 32 (12/08/2022)*

- Work on Student Fees
- Generate Fee Slip

### :arrow_right: *DAY 33 (13/08/2022)*


- Deepak gave a presentation on fees and admission and I make a report of it.
- Presentation on virtual environment given by Tavleen Kaur [ 2nd year CSE ]
- Understand what is fet.

### :arrow_right: *DAY 34 (14/08/2022)*

## Sunday day 


### :arrow_right: *DAY 35 (15/08/2022)*

## Independence Day

### :arrow_right: *DAY 36 (16/08/2022)*

- Work on Accounting
- Leaving Certificate
- Lead Management


### :arrow_right: *DAY 37 (17/08/2022)*

- HR Module
- Student Applicant
- Sales Management 
- Assets Management
- Today I helped the rest of the team.

Like - SSO Implementation, LDAP installation and Configuration.

### :arrow_right: *DAY 38 (18/08/2022)*

- Explore HR Module
- Show the fetched values of the mentor-mentee on the webpage with the use of context script
- start work on new project WMS Construction and MAintenance Cell
- Add the Load More button on the right side of the page on the frappe
- Add search button on the webpage of the mentor mentee

### :arrow_right: *DAY 39 (19/08/2022)*

- Create and design the table of the user of the webpage on https://gne11.gndec.ac.in/user 
- Discuss the workflow of CMC 
- start work on CMC and also work to design the flow chart of the CMC so we can easily understand its depth

### :arrow_right: *DAY 40 (20/08/2022)*

#### Saturday Seminar

- Discuss working on the workflow of CMC with Rai sir & Satinderpal sir.
- Design flowcharts with the use of mermaid editor.
- Discuss some topics of NSPS Project.


### :arrow_right: *DAY 41 (21/08/2022)*

Sunday FUN - day

### :arrow_right: *DAY 42 (22/08/2022)*

- find the admission fee in erp.gndec.ac.in
- And did some other works related to projects.
- Lived the webpage from the public_html [ Home Directory ] https://gne2.gndec.ac.in/

### :arrow_right: *DAY 43 (23/08/2022)*

- Argusoft pre-placement talks starts at 8:30 AM
- Then exam at 12'o clock.

# Daily-Work (24-8-2022)

- I have created all the courses again and also putt the subjects in each category.This task took complete one day.

# Daily-Work (25-8-2022)

- Today Satinder sir given a task to me and jasjit to find the information from database regarding to the NSPS grade report. A grade report is contains the fields of `Name of course` , `Email address` , `Course grade` etc.

# Daily-Work (26-8-2022)

- Today we learnt first about the sql queries and watched one tutorial for it and explore about the general log file and error log file along what is the importance over all of these files. After wacthed the tutorial got some idea and executed some queries.

# Daily-Work (27-8-2022)

- Finally we took our first step towards the task. To complete the task (grade report),firstly i install local moodle on my system and it take some time.Then i started working on it and explore the feature of it ,because it was my first time to do something on moodle.

# Daily-Work (29-8-2022)

- In order to accomplished our task ,we need user(student) name,grade,id,couse name.So start exploring the moodle database to get the valuses from the moodle database tables.

mdl_grade_grades: In this table we get the id,rawgrademax,finalgrade.
mdl_user: In this table we get the firstname of user,last name of user,username.
mdl_course: In this we get id of course,fullname,shortname.

# Daily-Work (30-8-2022)

- Today we had a discussion with our mentor releted the values and we set the final table ,to make single final query. The final table that we have to make contain the feild of uasername,firstname,lastname,course name,id.

# Daily-Work (31-8-2022)

- We succesfilly make the query with the help of Satinder sir, and at last sir tell us to check the final output, is it was actually meet with our requirement. At that time it was correct but when we test it by adding more courses then it was not giving the update couse and update grade of user.

# Daily-Work (1-9-2022)

- Today i had a task to resolve the problem. For that i took help from my other training friends. We all start working on it and also finding the solution with diffrent diffrent approaches.

# Daily-Work (2-9-2022)

- Today i went to satinder sir to discuss the problem. Sir gave some idea about it we again start to working on it and applied several queries but didn't work anything till evening.

# Daily-Work (3-9-2022)

- On this day i try below query-

`SELECT u.firstname , u.lastname , u.email , u.username, c.fullname as course_name,  
ROUND(gg.finalgrade,2) Grade, concat(uo.url, c.id) as url FROM mdl_course AS
c JOIN  url_of_course AS uo JOIN mdl_context AS ctx ON c.id = ctx.instanceid 
JOIN mdl_role_assignments AS ra ON ra.contextid = ctx.id JOIN mdl_user 
AS u ON u.id = ra.userid JOIN mdl_grade_grades AS gg ON gg.userid = u.id JOIN 
mdl_grade_items AS gi ON gi.id = gg.itemid JOIN mdl_course_categories 
AS cc ON cc.id = c.category WHERE gi.courseid = c.id AND gi.itemtype = 'course';`

It executed successfully getting the final output which mathes with requirements.

# Daily-Work (4-9-2022)

- After this having a task to put the incremental backup so that automatically values will be fetched from the database and update on moodle (gradebook) respectively.

# Daily-Work (5-9-2022)

- Today i have a task to learnt about the incemental backup. For that i refers some tutorial from youtube and followed them. I learnt of its importance and significance.

# Daily-Work (6-9-22)

- Today @HS Rai sir give one task to me that we have to do some work on QT(Qt is cross-platform software for creating graphical user interfaces as well as cross-platform applications that run on various software and hardware platforms such as Linux, Windows). The first we have to learn about the QT how to use it and how it work. For this i install it in my system and start exploring about it.

# Daily-Work (7-9-22)

- Then we install QT creator in which we write our program to create the GUI.Qt Creator creates several files for you. The HelloWorld.qmlproject file is the project file, where the relevant project configuration is stored. This file is managed by Qt Creator, so don’t edit it yourself. Another file, HelloWorld.qml, is our application code. Open it and try to understand what the application does before you read on.


# Daily-Work ((8-10)-09-22)

- In this period we learn about the QT and run a simple program (Hello) on it.
- Beside this i am also workinfg on to get the user data from database.The question was that how to fetch the data from two table in mysql database.Because we have to fetch the user name and corresponding courses which are stored in two different tables.

# Daily-Work (14-9-22)

- Today We start a ndew Project named CMC( Construction & Maintenance Cell).First of all we need to understand the structure of CMC, The CMC will be a company under NSET, parallel to GNDEC. IMO it must be a service based company, what is your opinion, and other domains available.It will have sales, purchase, stock, accounting etc.So, It is a service based company.

# Daily-Work (15-9-22)

- Create a company at gne2 and set its domain to service. We will test over gne2.But We have a maintenance module.Here we can make others doctype related to maintenance.So, the Company Name : Construction & Maintenance Cell, Parent Company : NSET, Domain Name : Services

# Daily-Work (16-9-22)

- Create a dashboard for the maintenance request.
In which cmc user see the requests by date wise and see no. of requests per day.

# Daily-Work (17-9-22)

- In the web form, "justification for request"  field needs to be optional, not mandatory. And it needs to be "draft" upto the level of HoD, which means that HoD/OIc/Caretaker/Warden will be able to change it. No change will took place once the higher authority forwarded the request.

# Daily-Work (18-9-22)

- Today, I am working on Dashboard. Start learning about the Dashboard and make test dashboard.Becauses ,I have to make a Dadboard of all Higher Authorities like SDO,CMC -Head, HOd's of all Departments.

# Daily-Work (19-9-22)

- Today we are working on the workflow of CMC project. We made the flowchart of CMC Project.
- steps: student | employee -> HoD -> SDO -> O/Ic Incharge 
- But there migh be Student -> Caretaker -> Warden -> SDO or Lab Attendant | Lab Technician -> Lab Incharge -> HoD ... In case of rejected, all must see the status, and in case of any additional query it may be sent back from where is was forwarded.

# Daily-Work (20-9-22)

- Today i work with Satinderpal sir , sir said us to make a courses on guru.gndec.ac.in.So we make it on the site.

# Daily-Work (21-9-22)

- Solved the problem regarding the moodle like user are not enroll in the courses and their attebdance.

# Daily-Work (22-9-22)

- Beside the CMC project I also work on the NSPS project(School project).Firstly we visit the school and get the information about the courses or subject and teacher or student data of school.

# Daily-Work (23-9-22)

- According to the information we upload the courses and user in the gne1.gndec.ac.in which is official moodle site of School.

# Daily-Work ((24-29)-9-22)

- Working on gne1.gndec.ac.in and visit the school regulary.Solves the teachers problems, help them to access the gne1.gndec.ac.in and how to add the activity in it and turm the edit mode on to do some work.

# Daily-Work (30-9-22)

- Today we (I and Pranvir ) are going to implement stock items in
erp.gndec.ac.in and also creating a dashboard of SDE which is only
visible to SDE only.

# Daily-Work (1-10-22)

- We are going to add stock items to erp.gndec.ac.in and make a
dashboard for SDE which is only visible to SDE.

# Daily-Work (2-10-22)

- Today we have to fullfil the requirement that are pending that thses are disscussed with Rai sir.
- I changed the Nature of work according to the requirements.

# Daily-Work (3-10-22)

- Estimate work is done on erp.gndec.ac.in according to the requirements.

# Daily-Work (4-10-22)

- Me checked if we select items for estimate then it will also reduces in stock.
- Now our task is to create a button in the CMC request form for SDE
only in which SDE will manage the realtime stock items.

# Daily-Work (5-10-22)

- We have two options:
First:
We can add a custom button in the cmc request form using the form
script. The link which is following is:
https://frappeframework.com/docs/v13/user/en/api/form
 But here we have an issue of permissions. Because Custom button is
not a field in a doctype and in my knowledge we are only able to gives
permissions to doctype fields to show that fields to some specific
users so here we goes to our Second option

Second:
We can create a field which is of type "Button". I know this is a
silly question but how can we add links behind the Button type fields
in frappe??
I searched this on Google and found that we need to write custom
scripts to make this button working. But I didn't get the correct
syntax for this.

# Daily- Work (6-10-22)

- we checked that if we select items for estimate then it will also reduces in stock.So when our stock becomes completely empty then we need to send
quotations for required items. So now our next task is to send quotations and restore our stock again.

# Daily-Work ((7-12)-10-22)

- Today Task was to do a Company Setup. So we are going to do the company setup.The company we are going to create  is Manufacturing company.
- Our Company name is "Unique Number Ltd" under Domain "Manufacturing".
- Company (Unique Number Ltb) is successfully created on gne2. Now we are going to do our next step.
- Our next step is to define tax of a company under the section of chart of account.
- In the section of Chart and Account , we select our company and come under the source of funds section . Here we do some changes in the CGST and SGST according to requirements which come under the Duties and Taxes.
- We created incoming CGST and incoming SGST under Application of assets section in the chart of accounts for buying purposes and defined CGST and SGST under Source of funds section for selling purpose.
- We need to create a journal entry to show the amount in the chart of accounts. But when we make a general entry it shows the error which says set the fiscal year first.
- In this we firstly add the sales order which include the information
about the customer,item and delivery date.
- Sales Invoice done.Payment of this order is also done

# Daily-Work (13-10-22)

- Dashboard for principal is created on erp.gndec.ac.in
- After this we disscuss the project with sir and there many thing which are need to be add in the project like.

# Daily-Work (14-10-22)
 
 1) "new request" button in cmc request.
 7) item name in estimate automatically fetched.
 - these tasks have been completed.

# Daily-Work (15-10-22)

 2) sorting complaint number in my requests
 - Tasks is completed.

# Daily-Work (16-10-22)

- We (Me and Komalpreet) are going to make new departments which are
left and will also update the csv file accordingly and upload it in
erp.gndec.ac.in.

# Daily-Work (17-10-22)

- Employees also created successfully.On erp.gndec.ac.in
- Task was completed: Image size limit can change as we tested on gne2.gndec.ac.in.
It can be changed through the backend. To change the image size limit,
go to /sites and open "common_site_config.json".
change max_file_size: 500000.

# Daily-Work (18-10-22)

- Working on Home page.
1)  I add a nav bar.(About, Departments, Notice board, Faculties).

# Daily-Work (19-10-22)

- Working on Education Domain . 
- I work on education domain t done the project regarding the Student Enrollment.
- Firstly under stand the whole process and had meeting with sir.

# Daily-Work (20-10-22)

- Understand the Fee structure  in Edcation Domain.
- Student Enrollment Process.

# Daily-Work ((21-30)-10-22)

- Create ourses in the education domain.
- Create Fee structure (Fee component, Student Category, Program)
- Add student and instructor in the list.

# Daily-Work ( 1-11-22)

- Rai sir told us to replace the estimate by quotation.
- Our approach is that we are going to create a button named "quotation
estimate" which will be shown to the SDE. With the help of this
button, SDE will be able to handle quotations(estimate), sales order,
sales invoice(Bill).

# Daily- Work (2-11-22)

- We successfully created a quotation. Now we are going to create a
sales order of that quotations, in which we add our items which we
want. And here we also apply a Tax on items, discounts and on them.

# Daily-Work (3-11-22)

-  we can update the quotation values in the estimate table.For this sdo willlick on a button named "Quotation/Estimate" in the cmc requestform and redirect to the quotation form. And then the estimate table values will be autofetch from the quotation table.

# Daily-Work (4-11-22)

- We created 2 Doctypes named:
1) final testing
2) DemoQuotation2

We added the same child table "estimate duplicate" in both doctypes as
we mentioned above. But according to that we didn't get the results.

# Daily-Work (5-11-22)

- Make a new flowchart of CMC Estimate/Quotations according to
@Satinder sir idea .

# Daily- Work ((6-13)-11-22)

- FullFil the requirents and do some changes in the fee structure and did some work on dashboard like add some filters in the cards and chardts of dashboard.

## :arrow_right: *DATE (14/11/2022)*
### *Finds the appropriate solution for upgrading Frappe v13 to Frappe v14*

- Today my task is to find the appropriate solution for upgrading Frappe v13 to Frappe v14.
- In the morning there is a meeting with the mentors of SDC.
- After that I started work on my task.
- I find the following link from where I am getting the reference.
  https://cloud.erpgulf.com/blog/support-forum/erpnext-upgrade-from-version-13-to-version-14-ubnutu

#Steps I follow:-

1- Take backup.

2- Make sure you don't have any customization those are not committed.

3- Check python version

4- Check node version.

5- Check pip or pip3 version ( needs to be upgrade to 22.x )

6- Upgrade python
```
sudo apt install software-properties-common -y
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt install python3.10 python3.10-dev python3.10-distutils
```
Make Python 3.10 the default.
```
sudo update-alternatives --install /usr/bin/python3 python3
/usr/bin/python3.10 1
```
Make sure python command executes python3
```
sudo apt install python-is-python3
```

7 - Upgrade PIP
```
curl -sS https://bootstrap.pypa.io/get-pip.py | python3.10
pip install html5lib
pip3 install --upgrade pip
sudo apt-get remove python3-apt -y
sudo apt-get install python3-apt -y
```

At the Step 8 I am getting an error while upgrading the version of
node.Which is resolve by the command nvm install node.

Instead of following command :-

8- Upgrade Node
```
curl -sL https://deb.nodesource.com/setup_16.x | bash -
apt-get install nodejs redis-server -y
```
I am using the following commands:-
```
nvm install node
sudo apt-get install redis-server
```

9- Upgrade NPM
```
npm upgrade
sudo npm install 16
sudo npm install -g npm@8.19.1
```

10 -Move your old python env folder to env-archive, in-case anything
goes wrong, you can return to the original
```
/home/simran/frappe-bench/
mv env env-archive
(Please check your frappe bench path)
```

11- Create new virtual env for python-3.10
```
pip install virtualenv
virtualenv --python python3.10 env
env/bin/pip install -U pip
```
I was getting an error while running the second command so I created
the virtual environment by the following command:-
```
bench setup env
```

12- Change git upstream from V13 to V14
```
env/bin/pip install -e apps/frappe -e apps/erpnext
pip3 install frappe-bench
bench switch-to-branch frappe erpnext version-14
```
(This command take my half an hour and after that gave me an error so
I run the below command instead of this)
```
bench switch-to-branch version-14 frappe erpnext --upgrade
```

13- Migrate your site
```
bench --site {site_name} migrate
This command works only when the bench is start.
```
After completing all the steps I am facing the following problem:-
After completing all the steps I am facing the following problem:-
<br>
<div align="left">
<img alt="logotype" src="https://discuss.erpnext.com/uploads/default/original/3X/c/d/cd47331f398a9ad7d817584f6fd7389670705ce0.png">
</div>
<br>

This error is resolved by removing the line
"maintenance mode":1
from common_site_config.json

After completing all the steps I get the following result.
<br>
<div align="left">
<img alt="logotype" src="https://github.com/Simranjeet7860/Demo-Image/blob/main/Screenshot%20from%202022-11-14%2014-39-51.png">
</div>
<br>

 ## :arrow_right: *DATE (15/11/2022)*
### *Complete the maximum work of Quotation and Estimate in CMC Project*

1. Customize the quotation doctype. In the quotation doctype we add
the CMC Request No., Labour Cost , Grand Total(Equals to total_cost+
labour cost).

2. Add connection in CMC Doctype. When the sde clicks on Quotation
then in the Quotation form CMC Request no. automatically fetches.

3. Next problem we faced is CMC_Head unable to see the quotation. For
this we see all the roles and roles permissions  but we are unable to
find anything from that. After that we find that there is some user
permission for a user CMC Head which restricts the CMC Head to see the
quotation list.

4. We also add the custom script in Quotation doctype.( Grand Total =
total_cost+ labour cost).

  After that we discussed with Rai Sir in the evening meeting that there
  is no need to customize the quotation doctype. Instead of this I add some
  services in the item list and delete the customization that I made on
  quotation doctype.

  Pending work:-
  When total_cost(in Quotation)>total_cost(in Bill) then it shows an alert message.
  
   ## :arrow_right: *DATE (16/11/2022)*
### *Today Task*
Finish 10% of yesterday's pending work which is
When total_cost(in Quotation)>total_cost(in Bill)
then it shows an alert message.

If this task is finished on time then after that I have another task
to understand the whole chat app like how its work, doctypes created
and the logic behind all the stuff.

### Status of Tasks:-
Only first task is completed and the second task is pending.

### Work I do Today for completing the first task.
In the CMC Project we want the linking of Quotation,Sales Order and Sales Invoice with the CMC Request.

Solution:- We added one field(CMC Request no.) in the all the doctypes(Sales invoice, Sales Order and
quotation) and fetched the CMC Request No. automatically.
For this we use the connections.

When total_cost(in Quotation)>total_cost(in Bill) then it shows an
alert message.

Solution:-For this we fetch the total cost of quotation in the Sales

Invoice doctype and add the following client script in it.
```
frappe.ui.form.on('Sales Invoice', {
    refresh(frm) {
        if (frm.doc.grand_total > frm.doc.quotation_total) {
        frappe.msgprint('Your Total Cost exceeding the Estimate Cost!!!')
}
    }
})
```

