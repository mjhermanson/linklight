# Exercise 3 - Creating and Running a Job Template

A job template is a definition and set of parameters for running an Ansible job. Job templates are useful to execute the same job many times.


## Creating a Job Template

### Step 1:

Select TEMPLATE

### Step 2:

Click on ADD ![Add button](at_add.png), and select JOB TEMPLATE

### Step 3:

Complete the form using the following values

NAME | Install MSSQL on Windows
-----|-------------------------
DESCRIPTION|Template for the windows playbook
JOB TYPE|Run
INVENTORY|Ansible Workshop Inventory
PROJECT|Ansible Workshop Project
PLAYBOOK|exercises/windows-mssql.yml
MACHINE CREDENTIAL|Ansible Windows Credential
LIMIT|windows
OPTIONS|- [x] Enable Privilege Escalation

<!--![Job Template Form](at_jt_detail.png) -->

### Step 4:

Click SAVE ![Save button](at_save.png) and then select ADD SURVEY ![Add](at_addsurvey.png)

### Step 5:

Complete the survey form with following values

PROMPT|Target hostname
------|------------------------------------------------
DESCRIPTION|hostname of server
ANSWER VARIABLE NAME|limit
ANSWER TYPE|Text
MINIMUM/MAXIMUM LENGTH| Use the defaults
DEFAULT ANSWER| windows

<!-- ![Survey Form](at_survey_detail.png) -->


### Step 6:

Select ADD ![Add button](at_add.png)

### Step 7:

Select SAVE ![Add button](at_save.png)

### Step 8:

Back on the main Job Template page, select SAVE ![Add button](at_save.png) again.

## Running a Job Template

Now that you've sucessfully creating your Job Template, you are ready to launch it.
Once you do, you will be redirected to a job screen which is refreshing in realtime
showing you the status of the job.


### Step 1:

Select TEMPLATES

---
**NOTE**
Alternatively, if you haven't navigated away from the job templates creation page, you can scroll down to see all existing job templates

---

### Step 2:

Click on the rocketship icon ![Launch button](at_launch_icon.png) for the *Install MSSQL on Windows*

### Step 3:

When prompted, enter your desired test message

<!-- ![Survey Prompt](at_survey_prompt.png) -->

### Step 4:

Select LAUNCH <!-- ![Survey launch button](at_survey_launch.png) -->

### Step 5:

Sit back, watch the magic happen!

This job will execute the tasks in the MSSQL role in the project. This will go through the installation of MSSQL Developer Edition 2017. 

You can use the variables in this role to manage the configuration lifecycle of the database in the same manner os the code. For example, if you are introducing a code change that will require more resources on the database, you can make that change in git repo and let ansible role out the changes. 


## End Result
At this point in the workshop, you've experienced the core functionality of Ansible Tower.  But wait... there's more! You've just begun to explore the possibilities of Ansible Core and Tower.  Take a look at the resources page in this guide to explore some more features.



---

[Click Here to return to the Ansible Lightbulb - Ansible Tower Workshop](../README.md)
