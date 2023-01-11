# Daily-Diary
# TRAINING AND INTERNSHIP PROGRAMME :point_down:

:arrow_right: **Date : 12-JULY-2022** 

### Learning new Things

- In the morning we have meeting with HS Rai Sir(mentor of our training).
- He gave us the instructions and welcome us in the SDC(Software developement Centre)
- He told us to work on the things:
- Linux, Apache, Mysql & Mariadb , php.


:arrow_right: **Date : 13-JULY-2022** 

- Today I started working on learning about LAMP.
- I go through the documentation https://www.javatpoint.com/what-is-lamp.

### What I learn Today:-

- Linux: Linux started in 1991. It sets the foundation for the stack model. All other layers are run on top of this layer.
  It is an open-source and free operating system. It is endured partly because it's flexible, and other operating systems are harder to configure.
     
- Apache: The second layer consists of web server software, typically Apache Web Server. This layer resides on top of the Linux layer.
  Apache HTTP Server is a free web server software package made available under an open-source license. It used to be known as Apache Web Server when it     was created in 1995.
    
- MySQL: MySQL is a relational database management system used to store application data. It is an open-source and keeps all the data in a format that       can easily be queried with the SQL language.
    
- PHP: The scripting layer consists of PHP and other similar web programming languages.
  The PHP open-source scripting language works with Apache to create dynamic web pages. We cannot use HTML to perform dynamic processes such as pulling       data out of a database.


:arrow_right: **Date : 14-JULY-2022** 


- Today I learn a lot of stuff related to linux, different operating systems.
- I go through the documentation which is provided at https://www.guru99.com/install-linux.html and learn about the linux distrubutions.
- I also learn theoretically how to install linux in our laptop or pc but there is a lot of difference to learn theoratically and perform practically.
- I got so many error while installing the linux even my window is destroyed due to some lack of information.
- Now I have no operating system in my pc.
- After a lot of struggle when I am unable to find the the solution of this then I decide to this tommorow in the presence of some expert who is having some knowledge of linux and the stuff related to distributions.

:arrow_right: **Date : 15-JULY-2022** 

- In the morning Pranvir help me to resolve the errors which I got during the installation of linux.
- Now I have Ubuntu linux distribution in my pc.
- This took my whole day and I learn a lot of things like how to install linux in our laptop practically.

:arrow_right: **Date : 16-JULY-2022** 

### Saturday

:arrow_right: **Date : 17-JULY-2022** 

### Sunday

:arrow_right: **Date : 18-JULY-2022** 

- Today Rai Sir added our whole team in the google group and told us to go through the documentation http://www.slideshare.net/sandeepkmadaan/mailing-guidelines 
- I read all the guide lines which is mentioned in the mailing guidelines.
- I Read about the frappe framework, its functionalities and advantage along with its installation process.

:arrow_right: **Date : 19-JULY-2022** 

- Today the day started with the meeting which we have with our mentors and our SDC senoirs. They all shared their experiences and also gave a brief direction about our work.
- I learn a lot things from them.
- Today we all send our first mail in greatdeveloper group.
- In the mail we describe our skills and our intrests.

:arrow_right: **Date : 20-JULY-2022** 

- Today I started work on installing the frappe framework in our laptop.
- For installing this I go go through the following steps:-

## Guide-to-Install-Frappe-ERPNext-in-Ubuntu-22.04-LTS
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


:arrow_right: **Date : 21-JULY-2022** 

- I get a lot of errors in the installation of frappe framework in my pc which is mentioned in the mails.
- A lot of errors is solved by searching a lot of errors are resolved by ourself also.
- Today I successfullly install the frappe framework in our laptop.

:arrow_right: **Date : 22-JULY-2022** 

- Today our task is to create library management system in our laptop by learning through the frappe documentation https://frappeframework.com/
- In the library Management System we have to do the following things:-

We will build a simple Library Management System in which the Librarian can log in and manage Articles and Memberships. We will build the following models:

- Article: A Book or similar item that can be rented.
- Library Member: A user who is subscribed to a membership.
- Library Transaction: An Issue or Return of an article.
- Library Membership: A document that represents an active membership of a Library Member.
- Library Settings: Settings that define values like Loan Period and the maximum number of articles that can be issued at a time.

:arrow_right: **Date : 23-JULY-2022** 

### Saturday

:arrow_right: **Date : 24-JULY-2022** 

### Sunday

:arrow_right: **Date : 25-JULY-2022** 

- Today I learn how we can create our site and app in frappe folder:-
- Commands which use to create app is
```
bench new-app {app_name}
```
- For creating new site
```
bench new-site {site_name}
```
### Today I complete the following steps of Library Management System:-

- Frappe Framework Tutorial
- Install and Setup Bench
- Create an App
- Create a Site
- Create a DocType
- DocType Features

:arrow_right: **Date : 26-JULY-2022** 

### Today I completed the pending steps of library management system

- Controller Methods
- Types of DocType
- Form Scripts
- Web View Pages
- Today I complete the library management system and decide to give the presentation on it.

:arrow_right: **Date : 27-JULY-2022** 

- Today after the presentation Rai Sir give me a task to understand the chat-app which is created in the frappe-framework v13. 
- As I searched a lot but I am unable to find the solution how we can download the prebuild apps in our laptop.
- At this stage Tanveer help me and give me a hint that we can install prebuild apps by the following commands:-
```
bench get-app {app_name}
bench --site {site_name} install-app {app_name}
```

:arrow_right: **Date : 28-JULY-2022** 

- Today my work is to understand the chat-app ,which doctypes are created and all the stuff related to this.
- First I install the chat-app in our laptop and see all the files which is created in the chat-app.
- During the exploratoin I learned a new thing which is user and roles in the frappe framework.
- From the above I learned how we can give different roles and different roles permissions to different users.

:arrow_right: **Date : 29-JULY-2022** 

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

:arrow_right: **Date : 30-JULY-2022** 

- Today seminar off because our Infosys SP & DSE Exam
- Prepare for Exam

:arrow_right: **Date : 31-JULY-2022** 

### Sunday

:arrow_right: **Date : 01-AUGUST-2022** 

- Today Satinder Sir gave us a work to get a backup from an server which is at CC1 lab.
- We(me and Tanveer) are selected to do this task.
- First we open the CPU and get the Hard Drive from that CPU after that we connected that Hard Drive to another pc and take the backup files which is useful.

:arrow_right: **Date : 02-AUGUST-2022** 

- There is one another file in the hard disk which is a script which is user to create the users automatically.
- We take the backup of the file and send the script to the Rai Sir.

:arrow_right: **Date : 03-AUGUST-2022** 

- Implement education domain in test server (gne11.gndec.ac.in)
- Create Programs, Courses
- Allot room according to course, Programs and So on.

:arrow_right: **Date : 04-AUGUST-2022** 

- As all are not reading the mails properly so Sir assign Komal to give a brief representation on the mails guidelines.
- All are prepared themselves for the presentation because Sir told us that they can ask any question to anyone regarding the mails and guidelines.
- In the evening Komalpreet gave their presentation.   

:arrow_right: **Date : 05-AUGUST-2022** 

- Today I will try explore my chat-app work.
- In this I am exploring the doctypes created by the chat app.
- How chat-app works for non user or website user.

:arrow_right: **Date : 06-AUGUST-2022** 

- Saturday seminar
- understand the use of make command
- how we can write script of it

:arrow_right: **Date : 07-AUGUST-2022** 

### Sunday

:arrow_right: **Date : 08-AUGUST-2022** 

- getting error when i'm using context script
- search the solution for it.
- work on fee structure on education domain.

:arrow_right: **Date : 09-AUGUST-2022** 

- Today I explore how we can edit homepage and login page.
- I am also work on how we can give appropriate roles to different users.
- In the evening there is a presentation given by tanveer on LMS.

:arrow_right: **Date : 10-AUGUST-2022** 

- Today I explore How can we me make users in bulk.
- It is a very simple process to do so.
- First go to the user list click on import data.
- Click on get csv and select the fields according to your needs.
- After that create put all the data in csv file and upload it.

:arrow_right: **Date : 11-AUGUST-2022** 

### Raksha Bandhan

:arrow_right: **Date : 12-AUGUST-2022** 

- Work on Student Fees
- Generate Fee Slip

:arrow_right: **Date : 13-AUGUST-2022** 


- Deepak gave a presentation on fees and admission and I make a report of it.
- Presentation on virtual environment given by Tavleen Kaur [ 2nd year CSE ]
- Understand what is fet.

:arrow_right: **Date : 14-AUGUST-2022** 

### Sunday

:arrow_right: **Date : 15-AUGUST-2022** 

### Independence Day

:arrow_right: **Date : 16-AUGUST-2022** 

- Work on Accounting
- Leaving Certificate
- Lead Management

:arrow_right: **Date : 17-AUGUST-2022** 

- HR Module
- Student Applicant
- Sales Management 
- Assets Management
- Explore about SSO Implementation, LDAP installation and Configuration.

:arrow_right: **Date : 18-AUGUST-2022** 

- Explore HR Module
- Show the fetched values of the mentor-mentee on the webpage with the use of context script
- start work on new project WMS Construction and MAintenance Cell
- Add the Load More button on the right side of the page on the frappe
- Add search button on the webpage of the mentor mentee

:arrow_right: **Date : 19-AUGUST-2022** 

- Create and design the table of the user of the webpage on https://gne11.gndec.ac.in/user 
- Discuss the workflow of CMC 
- start work on CMC and also work to design the flow chart of the CMC so we can easily understand its depth

:arrow_right: **Date : 20-AUGUST-2022** 

- Discuss working on the workflow of CMC with Rai sir & Satinderpal sir.
- Design flowcharts with the use of mermaid editor.
- Discuss some topics of NSPS Project.

:arrow_right: **Date : 21-AUGUST-2022** 

### Sunday

:arrow_right: **Date : 22-AUGUST-2022** 

- find the admission fee in erp.gndec.ac.in
- And did some other works related to projects.
- Lived the webpage from the public_html [ Home Directory ] https://gne2.gndec.ac.in/

:arrow_right: **Date : 23-AUGUST-2022** 

- Argusoft pre-placement talks starts at 8:30 AM
- Then exam at 12'o clock.

:arrow_right: **Date : 24-AUGUST-2022** 

- I have created all the courses again and also putt the subjects in each category.This task took complete one day.
- Add the items in the warehouse 
- Raghu Sir gave a presentation on EMS(Event Management System)

:arrow_right: **Date : 25-AUGUST-2022** 

- Today Satinder sir given a task to me and jasjit to find the information from database regarding to the NSPS grade report. 
- A grade report is contains the fields of `Name of course` , `Email address` , `Course grade` etc.
- We explore this and search some sql queries.

:arrow_right: **Date : 26-AUGUST-2022** 

- Today we learnt first about the sql queries and watched one tutorial for it and explore about the general log file and error log file.
- We also explore what is the importance of all these files.
- After wacthed the tutorial got some idea and executed some queries.

:arrow_right: **Date : 27-AUGUST-2022** 

- Finally we took our first step towards the task. To complete the task (grade report),firstly i install local moodle on my system and it take some time.Then i started working on it and explore the feature of it ,because it was my first time to do something on moodle.

:arrow_right: **Date : 28-AUGUST-2022** 

## SUNDAY

:arrow_right: **Date : 29-AUGUST-2022** 

- In order to accomplished our task ,we need user(student) name,grade,id,couse name.So start exploring the moodle database to get the valuses from the       moodle database tables.
- mdl_grade_grades: In this table we get the id,rawgrademax,finalgrade. mdl_user: In this table we get the firstname of user,last name of user,username. 
- mdl_course: In this we get id of course,fullname,shortname.

:arrow_right: **Date : 30-AUGUST-2022** 

- we had a discussion with our mentor releted the values and we set the final table ,to make single final query. 
- The final table that we have to make contain the feild of uasername,firstname,lastname,course name,id.

:arrow_right: **Date : 31-AUGUST-2022** 

- We succesfilly make the query with the help of Satinder sir, and at last sir tell us to check the final output, is it was actually meet with our requirement. 
- At that time it was correct but when we test it by adding more courses then it was not giving the update couse and update grade of user.

:arrow_right: **Date : 01-SEPTEMBER-2022** 

- Today I started on my old work which is exploring chat app.
- Chat is the commmuncation software where people interact with others through the text messages. 
- The Chat is a tool, which allows you to send and receive messages to other Users within your ERPNext account.
- This tool can be used to maintain internal communications within your oganization. 

:arrow_right: **Date : 02-SEPTEMBER-2022** 

- Today I explore about the features of chat app which are described below.
1. Lightweighted .
2. Drak mode support.
3. Provide admin , guest and user view.
4. Responsive
5. Interface

- How to installed?

By following below commands -
```
bench get -app chat
bench --site sitename install -app cha
```

:arrow_right: **Date : 03-SEPTEMBER-2022** 

- Explore the doctypes created in chat-app.

1. Chat room
2. Chat message
3. Chat profile
4. Chat setting
5. Chat user setting 

:arrow_right: **Date : 03-SEPTEMBER-2022** 

### Chat room

Chat room is the space where user inetract with others (Admin , System
user) by the text messages. Chat room can be created by the 3 ways :
- By guest
- By Direct
- By group -

### Chat message

It is the space where text are sent between people. Every message that
has been sent by a User gets reflected in the Chat Message List.

### Chat profile 

Chat profile show you a list of all the active
profiles in your ERPNext account with whom you can start a chat.To
start a new chat, simply type the name of the User in the search bar
of chatbox and start communicating.

### Chat setting 

In chat setting can set the timing to enable the chat.
Can allowed roles to the users. - Can attached the file with whom
you want to communicate.

### Chat user setting 

This setting shows at the user end where user
can enable the notificaton tone and message tone etc. 

:arrow_right: **Date : 04-SEPTEMBER-2022** 

### SUNDAY

:arrow_right: **Date : 05-SEPTEMBER-2022** 

- Tommorow is my presentation on chat-app.
- I create a ppt of my presentation.
- Also prepare myself for presentation.

:arrow_right: **Date : 06-SEPTEMBER-2022** 

- Today I gave the presentation on the chat-app
- The presentation was good.
- Komalpreet creates the report of my presentation.
- I learn a lot of things from my presentation. 

:arrow_right: **Date : 07-SEPTEMBER-2022** 

- Try to find the solution of question asked on my yesterday seminar.
- The questions asked in the seminar is also writen below.

### Question Asked

- Why we select the users in chat room one by one?
- What is token?
- How the feature of version14 chat app is useful for us?
- Is video can be send?
- why file cannot be send greater then 5MB size?
- Can user customized their messages after sent once as in whatsapp
- We can delete the message at both send even after delivered? 

:arrow_right: **Date : 08-SEPTEMBER-2022** 

- Today I create github pages for chat-app
- Also help Komal in making their report.

:arrow_right: **Date : 09-SEPTEMBER-2022** 

- Today We start a ndew Project named CMC( Construction & Maintenance Cell).
- First of all we need to understand the structure of CMC.
- The CMC will be a company under NSET, parallel to GNDEC. 
- IMO it must be a service based company. 
- It will have sales, purchase, stock, accounting etc.

:arrow_right: **Date : 10-SEPTEMBER-2022** 

- H.S.Rai Sir gave me work on the review of Rocket Chat. 
- I study the features and some limitations of it and make a review of rocket chat. 
- The link of my review is given below https://docs.google.com/document/d/1WKhkTgy72CwMBhADG4SiyCu4MwHimEZ0fR4rJh1T6zQ/edit?usp=sharing




***********************************************************************************************************************************

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

