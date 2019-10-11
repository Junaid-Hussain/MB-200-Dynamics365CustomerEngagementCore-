Module 15: Manage Solutions
==========================
## Practice Lab – Import and export solutions

Scenario
--------

As a functional consultant at Contoso, you’ve been asked to help create an app
that tracks customers current problems. In these practices on solutions, you
will create a solution to track all your components, export and import into
production, and then go through a maintenance cycle using patches to update the
deployed solution. In this practice, you will be doing the following:

-   Export a solution

-   Import a solution

-   Test an imported solution


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

Note: If you have already completed a practice recently, the virtual machine
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

Exercise 2 – Export and Import a Solution
-----------------------------------------

In this exercise, you will export the Contoso Customer Problems solution from
the Development environment and import it to the Contoso Sales environment.

### Task 1 – Export Solution 

In this task, you will export both a managed and an unmanaged copy of the
Contoso Customer Problems solution.

1.  Navigate to https://web.powerapps.com

2.  Make sure you have the **Development** environment selected.

3.  Select **Solutions**.

4.  Locate and click to open the **Contoso Customer Problems** solution you
    created.

5.  Click **Export** and select **As Managed**.

6.  Save the Solution on your machine.

7.  Click **Export** again and select **As Unmanaged**.

8.  Save the solution on your machine

### Task 2 – Import Solution

In this task, you will import the manage version of the Contoso Customer
Problems solution to your Sales environment.

1.  Navigate to https://web.powerapps.com

2.  should have three environments, the Development, one with the name Org Name
    (default), and one with the name Org Name (onrgname). You must select the
    **Org Name (onrgname)** environment.

3.  Select **Solutions**.

4.  Click **Import**.

5.  Click **Browse**.

6.  Select the **Managed** solution you exported and click **Open**.

7.  Click **Next**.

8.  Click **Import**.

9.  Wait for the import to complete.

10. Click **Close**.

### Task 3 – Test the Imported Solution

In this task, you will test the imported solution.

1.  Select **Apps**. You should see the **Contoso Customer Challenges**
    application.

2.  Click to open the **Contoso Customer Challenges** application.

3.  **My Active Accounts** view should load.

4.  Click **+ New**.

5.  Enter **Test Account** for **Account Name** and click **Save**.

6.  Click **Related** and select **Problems**.

7.  Click **+ Add New Problem**.

8.  Enter **Test Problem** for **Name**, select **High** for **Level**, and
    click **Save**.
