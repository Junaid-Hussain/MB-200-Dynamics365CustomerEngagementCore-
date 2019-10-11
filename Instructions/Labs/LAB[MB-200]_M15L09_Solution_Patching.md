Module 15: Manage Solutions
==========================

## Practice Lab - Solution patching

Scenario
--------

As a functional consultant at Contoso, you’ve been asked to help create an app
that tracks customers current problems. In these practices on solutions, you
will create a solution to track all your components, export and import into
production, and then go through a maintenance cycle using patches to update the
deployed solution. In this practice, you will be doing the following:

-   Create a patch

-   Import a patch

-   Create a new version

-   Upgrade a solution

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

Exercise 2 – Solution Patching and Versioning
---------------------------------------------

In this exercise, you will clone a patch and a new version of the solution from
the Contoso Customer Problems solution.

### Task 1 – Create Patch 

In this task, you will clone a patch solution from the Contoso Customer Problems
solution.

1.  Navigate to https://web.powerapps.com

2.  Make sure you have the **Development** environment selected.

3.  Select **Solutions**.

4.  Locate and click to open the **Contoso Customer Problems** solution you
    created.

5.  Click on the **…** button.

6.  Click **Clone** and select **Clone a Patch**.

7.  The minor version of the solution will be incremented.

8.  Change the Display Name to **Contoso Customer Problems Patch** and Click
    **Save**.

9.  Navigation to **Solutions.**

10. Click to open the **Contoso Customer Problems Patch** solution.

11. Click **Add Existing**.

12. Click **Other** and select **Option Set**.

13. Search for the **Customer Challenge Level** option set and select it.

14. Click **Add**.

15. Click to open the **Customer Challenge Level** you added to the patch
    solution.

16. Click **Add New Item**.

17. Enter **Medium** and click **Save**.

18. Click **Publish** and wait for the publishing to complete.

19. Click **Export** and select **As Managed.**

20. Save the solution in your machine.

21. Click **Export** again and select **As Unmanaged**.

### Task 2 – Import Patch

In this task, you will import the Patch solution into your Sales environment.

1.  Navigate to https://web.powerapps.com

2.  Make sure you have the Sales environment selected. You should have three
    environments, the Development, one with the name Org Name (default), and one
    with the name Org Name (orgname). You must select the **Org Name (orgname)**
    environment.

3.  Select **Solutions**.

4.  Click **Import**.

5.  Click Browse.

6.  Select the **Managed Patch** solution you exported and click **Open**.

7.  Click **Next**.

8.  Click **Import**.

9.  Wait for the import to complete.

10. Click **Close**. Refresh the page, and you should see both base solution and
    the patch solution.

### Task 3 – Create a New Version

In this task, you will create a new version of the Contoso Customer Problems
solution.

1.  Navigate to https://web.powerapps.com

2.  Make sure you have the **Development** environment selected.

3.  Select **Solutions**.

    **Note:** You should have both the base and patch solutions listed here.

4.  Select the **Contoso Customer Problems** solution you created.

5.  Click on the **…** button.

6.  Click **Clone** and select **Clone Solution**.

7.  The version will be incremented. Click **Save**.

    **Note:** The patch solution will now get rolled up into the new version of
    the base solution.

8.  Click to open the **Contoso Customer Problems** solution.

9.  Click to open the **Account** entity.

10. Select the **Forms** tab.

11. Click to open the **Main** form.

12. Locate the Challenge Last Updated field and select it.

13. Click **Remove**.

14. Click **Save**.

15. Click **Publish**.

16. Click **Save and Close**.

17. Click **Done**.

18. Select the **Fields** tab.

19. Select the **Challenge Last Updated** field and click **Delete Field**.

20. Click **Save Entity**.

21. Click **Contoso Customer Problems**.

22. Click **Publish All Customizations** and wait for the publishing to
    complete.

23. Click **Export** and select **As Managed**.

24. Save the solution on your machine.

25. Click **Export** again and select **As Unmanaged**.

26. Save the solution on your machine.

### Task 4 – Upgrade Solution 

In this task, you will import the new version of the Contoso Customer Challenge
solution as an upgrade.

1.  Navigate to https://web.powerapps.com

2.  Make sure you have the Sales environment selected. You should have three
    environments, the Development, one with the name Org Name (default), and one
    with the name Org Name (orgname). You must select the Org Name (orgname)
    environment.

3.  Select **Solutions**.

    **Note:** both the patch and base solutions should be listed.

4.  Click **Import**.

5.  Click **Browse**.

6.  Select **ContosoCustomerProblems_1_1_0_0_managed.zip** and click **Open**.

7.  Click **Next**.

8.  Click **Next** again.

9.  Click **Import** and wait for the import to complete.

10. Click **Apply Solution Upgrade** and wait for the solution upgrade to
    complete.

11. Click **Close**.

12. Refresh the page.

    **Note:** The patch and base solution will now get rolled up into the new
    version of the solution.
