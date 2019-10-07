---
lab:
    title: 'Lab: Bulk delete'
    module: 'Module 13: Managing Data'
---

Module 13: Managing Data
=======================

## Lesson 9: Practice Lab – Bulk delete

Scenario
--------

You are a functional consultant working on the Fabrikam project. Your client
wants you implement some automatic data cleanup of stale data. You have been
asked to delete any Knowledge Assessment that is over 6 months past its end
date. You will be using the Bulk Delete feature of the Common Data Service.

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

Exercise 2 – Bulk Delete
------------------------

In this exercise, you will create a bulk deletion operation that will delete all
Knowledge Assessment records with an End Date older than 6 months, this
operation will run every 7 days.

### Task 1 – Create Bulk Delete Operation

In this task, you will create a bulk deletion operation.

1.  Navigate to <https://admin.powerplatform.microsoft.com>

2.  Select **Environments**.

3.  Select your environment and click **Settings**.

4.  Go to the **Data Management** section and click **Bulk Deletion**.

5.  Click **New**.

6.  Click **Next**.

7.  Select **Knowledge Assessments** from the **Look for** dropdown.

8.  Select the **End Date** field.

9.  Select **Older than X Months**.

10. Enter **6** and click **Next**.

11. Change the **Name** to **Delete Old Assessments**.

12. Select to run **At Scheduled Times.**

13. Select today’s date for **Date** and select **10 Minutes** in to the future
    for **Time**.

14. Check the **Run this Job After Every** checkbox.

15. Select **7 Days**.

16. Check the **Send an Email…** checkbox and click **Next**.

17. Click **Submit**.

18. Wait for the job to be created. This can take few minutes, refresh the view
    after few minutes.

### Task 2 – Test Bulk Deletion

In this task, you will test the bulk delete operation you created.

1.  Navigate to <https://web.powerapps.com/> and make sure you are NOT in the
    default.

2.  Select **Apps**.

3.  Locate and click to open the **Knowledge Admin** application.

4.  Click on the **Site Map** button and select **Assessments**.

5.  Click to Open One of the **Knowledge Assessment** records.

6.  Change the **End Date** to **Seven Months** in the past.

7.  Click **Save**.

8.  You will get an email when the **Bulk Deletion** job completes.

9.  Click on the link in the email.

10. You should see the **Total** number of records deleted.
