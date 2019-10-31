---
lab:
    title: 'Lab: Install app'
    module: 'Module 14: Manage Instances and Applications'
---

Module 14: Manage Instances and Applications
===========================================
## Practice Lab – Install app

Scenario
--------

As a functional consultant at Contoso, you’ve been asked to help set up the
Dynamics 365 environment within the test tenant. In the last practice, you did
the first run configuration to provision the environment. In this practice, you
will be installing the Dynamics 365 for Sales application.

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

Exercise 2 – Install Sales App and Import Solution
--------------------------------------------------

In this exercise, you will install the Dynamics 365 Sales Application into your
trial organization, install sample data, and import a solution.

### Task 1 – Install App 

In this task, you install the Dynamics 365 Sales Application into your
organizations and install the sample data.

1.  Navigate to https://admin.powerplatform.microsoft.com

2.  Expand the **Admin Center** section.

3.  Locate and click **Dynamics 365**.

4.  Select your environment (there should only be one there)

5.  Click the small blue “edit” icon next to the word **Solutions**.

6.  Open the applications tab.

7.  Locate and select **Dynamics 365 Sales Application**.

8.  Click **Install**.

9.  Read the **Terms of Service** and click **Install**, if you agree.

10. Wait for the solution to be installed. To check the status, refresh the page
    and check the **Status** column. (**Note:** The installation of the Dynamics 365 Sales Application solution must complete before you can continue to the next step or task.)

11.  Navigate to https://web.powerapps.com

12.  Check the environment selector in the upper right corner to make sure you
    are **NOT** in the **Default** environment. You should have something like
    Contoso (crm\*) and not Contoso (Default). If you are in the default
    environment, select the other environment before continuing.

13.  Select **Apps** and click to open the **Sales** application.

14.  Navigate to **Settings** and select **Data Management**.

15.  Click **Sample Data**.

16.  Click Install **Sample Data**.

17.  Wait for the installation to start.

18.  Click **Close**.

19.  Close the Sales application.

### Task 2 – Import Solution 

In this task, you will import the Knowledge Assessment solution.

1.  Navigate to <https://web.powerapps.com>

2.  Check the environment selector in the upper right corner to make sure you
    are **NOT** in the **Default** environment. You should have something like
    Contoso (crm\*) and not Contoso (Default). If you are in the default
    environment, select the other environment before continuing.

3.  Select **Solutions** and click **Import**.

4.  Click **Browse**.

5.  Select the **Knowledge Assessment Solution** located in the resources folder
    and click **Open**.

6.  Click **Next**.

7.  Click **Import**. If prompted, allow pops ups.

8.  Wait for the import to complete.

9.  Click **Publish All.**

10. Click **Close**.

11. Select **Apps**.

12. You should see two more applications, **Fabrikam Assessment,** and
    **Knowledge Admin**.
