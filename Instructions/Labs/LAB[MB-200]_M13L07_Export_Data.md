---
lab:
    title: 'Lab: Export data'
    module: 'Module 13: Managing Data'
---

Module 13: Managing Data
=======================

## Lesson 7: Practice Lab – Export data

Scenario
--------

You are a functional consultant working on the Fabrikam project. Your client
wants to export some data form the CDS environment. In this practice, you will
see two ways to accomplish the task.

**Important Note:** This lab will provide you with an actual Office 365 tenant
and licenses for the Power Platform applications you will be using in this
course. You will only be provided with one tenant for the practice labs in this
course. The settings and actions you take within this tenant do not roll-back or
reset, whereas the virtual machine you are provided with does reset each time
you close the lab session. Please be aware that Office 365 is evolving all the time. The
instructions in this document may be different from what you experience in your
actual Office 365 tenant. It is also possible to experience a delay of several
minutes before the virtual machine has network connectivity to begin the labs.

Exercise 1 - Acquire Tenant Information and Connect
---------------------------------------------------

**Note:** If you have already completed a practice recently, the virtual machine
might pick up where you left off and you will not need to login again.  In that
case you can skip ahead to exercise two and resume.

### Task 1 – Connect to the Power platform administration portal

1.  On Virtual machine MB200-Dynamics_Lab, sign in as Admin with the password
    Pa55w.rd if you are not already logged in.

2.  Outside the VM in the online lab interface click Files and choose D365
    Credentials. This will allocate an Office 365 tenant for you to use in these
    labs.  It will display the admin email and password for your tenant.  You
    should copy this information to notepad or similar for your reference.

3.  In MB200-Dynamics_Lab launch Microsoft Edge from the taskbar. By default,
    the browser opens Office 365. Use the O365 credentials you just acquired in
    the previous step to login.

4.  Navigate in the browser to the Power platform admin portal at
    [https://admin.Powerplatform.microsoft.com](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fadmin.Powerplatform.microsoft.com&data=02%7C01%7Cv-juya%40microsoft.com%7C4be5a28c6f1e41eefee808d687ae2dc7%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636845580068684293&sdata=cLrD%2FhTDb5sRbajtFR9RrztfyTDCo0xGS4k8FSxTaIc%3D&reserved=0)

Exercise 2 – Export Data
------------------------

In this exercise, you will export data from the maker port and from Model-Driver
application.

### Task 1 – Portal Export

In this task, you will export data from the maker portal.

1.  Navigate to <https://web.powerapps.com/> and make sure you are NOT in the
    default environment.

2.  Expand **Data** and select **Entities**.

3.  Locate and click to open the **Knowledge Assessments** entity.

4.  Click **Export Data**.

5.  Wait for the data to be exported.

6.  Click **Download Exported Data.**

7.  Save the exported data on your local machine.

8.  Open the folder the data was downloaded to.

9.  Right click on the exported zip file and extracted.

10. Open the exported **CSV** file.

11. You should see all the exported **Knowledge Assessment** records.

12. Close the **CSV** file.

13. You may delete the exported file.

### Task 2 – Model-Driven Export

In this task, you will export data from Model-Driven application.

1.  Navigate to <https://web.powerapps.com/> and make sure you are NOT in the
    default.

2.  Select **Apps**.

3.  Locate and click to open the **Knowledge Admin** application.

4.  Click on the **Site Map** button and select **Assessments**.

5.  Click **Export to Excel**.

6.  Save the exported fie to your local machine.

7.  Open the folder the data was exported to.

8.  Open the exported Excel file.

9.  You should see all the exported **Knowledge Assessment** records.

10. Close the Excel file.

11. You may delete the exported file.
