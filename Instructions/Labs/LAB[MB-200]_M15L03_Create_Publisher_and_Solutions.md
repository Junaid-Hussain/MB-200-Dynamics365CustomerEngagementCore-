---
lab:
    title: 'Lab: Create publisher and solution'
    module: 'Module 15: Manage Solutions'
---

Module 15: Manage Solutions
====================================================================================
## Practice Lab - Create publisher and solution


Scenario
--------

As a functional consultant at Contoso, you’ve been asked to help create an app
that tracks customers current problems. In these practices on solutions, you
will create a solution to track all your components, export and import into
production, and then go through a maintenance cycle using patches to update the
deployed solution. In this practice, you will be doing the following:

-   Creating a development environment

-   Creating a Contoso publisher

-   Creating a Contoso problems solution associated with the Contoso publisher

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

Exercise 2 – Create Solution and Publisher
------------------------------------------

In this exercise, you will create a new environment, create a new publisher, and
create a new solution.

### Task 1 – Create Environment 

In this task, you will create a new environment.

1.  Navigate to https://admin.powerapps.com

2.  Click **New Environment**.

3.  Enter **Development** for **Name** and click **Create Environment**.

4.  Click **Create Database.**

5.  Select **Currency**, select **Language**, and click **Create Database**.

6.  Wait for the environment to be created. The environment name will look like
    Development(orgxxxxx) when it is completed.

### Task 2 – Create Publisher 

In this task, you will create a new publisher.

1.  Navigate to <https://web.powerapps.com>

2.  In the upper right-hand corner, click on the environment selector and chose
    the development environment created in task 1.

3.  From the far upper right-hand corner of the command bar, click on the gear
    wheel icon to open the settings menu and select **Advanced Customizations**.

4.  Go to the **Publishers** section and click **All Publishers**.

5.  Click **New**.

6.  Enter **Contoso** for **Display Name**, **Contoso** for **Name**, and
    **contoso** for **Prefix**.

7.  Click **Save and Close**.

8.  Close the Publishers browser tab.

### Task 3 – Create Solution

In this task, you will create a new solution.

1.  Navigate to <https://web.powerapps.com>

2.  Make sure you are in the **Development** environment. You can check your
    environment in the upper right-hand corner environment selector.

3.  Select **Solutions**.

4.  Click **New Solution**.

5.  Enter **Contoso Customer Problems** for **Display Name**.

6.  Select **Contoso** for **Publisher**.

7.  Enter **1** for **Version** and click **Create**.
