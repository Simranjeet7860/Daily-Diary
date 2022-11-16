# Daily-Diary
# TRAINING AND INTERNSHIP PROGRAMME :point_down:


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

