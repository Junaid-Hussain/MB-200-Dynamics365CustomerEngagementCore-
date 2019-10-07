Module 13: Managing Data
=======================

## Lesson 5: Practice Lab – Import data

Scenario
--------

You are a functional consultant working on the Fabrikam project. Your client
wants you to import some data in the their CDS environment. Specifically, they
have some data to import into an existing Knowledge Assessment entity. You
choose to leverage Power Query to transform the data and complete the import.

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

Exercise 2 – Import Data
------------------------

In this exercise, you will import Knowledge Assessment records into your CDS
environment.

### Task 1 – Load Excel file to OneDrive

In this task, you will Load then Knowledge Assessments Excel file to your
OneDrive. You can choose many data sources to use with Power Query, but Excel
was the one you chose.

1.  Navigate to <https://web.powerapps.com/> and make sure you are NOT in the
    default environment.

2.  Click on the **Waffle** button in the upper left corner to change
    applications and select **OneDrive**.

3.  Click **Upload** and select **Files**.

4.  Select the **Knowledge Assessments** file located in the resources folder
    and click **Open**.

### Task 2 – Create Data Integration Project

In this task, you will create a new data integration project and transform the
table

1.  Navigate to <https://web.powerapps.com/> and make sure you are NOT in the
    default environment.

2.  Expand **Data** and select **Data Integration**.

3.  Click **+ New Data Integration Project**.

4.  Select **Excel**.

5.  Click **Browse**.

6.  Pick your admin account.

7.  Select the **Knowledge Assessments** file you uploaded to OneDrive and click
    **Open**.

8.  Click **Next**.

9.  Select the **Knowledge Assessment** table and click **Next**.

10. Click **Transform Table** and select **Use First Row as Headers**.

### Task 3 – Manage and Transform Columns

In this task, you will remove unwanted columns, split the End Date column,
change the year from 2019 to 2020, and then merge back together.

1.  Select the first three columns that have **(Do Not Modify)** in header.

2.  Click **Manage Columns** and select **Remove Columns**.

3.  Select the **End Date** column.

4.  Click **Transform Columns**, click **Split Column**, and select **By
    Delimiter**.

5.  Select **Advanced**.

6.  Select **Custom** for **Separator**.

7.  Type /

8.  Enter **3** for **Number of Columns.**

9.  Click **OK**.

10. Select the **End Date.3** column.

11. Click **Transform Column** and select **Replace Values**.

12. Enter **2019** for **Value to Find**.

13. Enter **2020** for **Replace with** and click **OK**.

14. Select all three **End Date** columns. Select **End Date.1 first**, then
    **End Date.2**, and then **End Date.3**.

15. Click **Transform Columns** and select **Merge Columns**.

16. Select **Custom** for **Separator**.

17. Enter **/** and click **OK**.

18. Double click on the **Merged** column and rename it **End Date**.

19. Click **Next**.

20. Select **Load to Existing Entity**.

21. Select **cr123_Knowledge Assessment**. The prefix will be different your
    entity.

22. Map **Difficulty** to **cr123_Difficulty**.

23. Map **End Date**, **Start Date**, and **Title** to their corresponding
    fields.

24. Check the **Delete Rows that No Longer Exist….** checkbox and click
    **Next**.

25. Click **Create**.

26. Wait for the loading to complete. The Load Status will indicate Completed.

27. Click **Done**.

28. You will now have one project in the list. Click on the More Commands button
    **…** and select **Rename**.

29. Enter **Knowledge Assessment Project** and click **Rename**.

### Task 4– Test Your Work

1.  Select **Entities**.

2.  Locate and click to open the **Knowledge Assessment** entity.

3.  Select the **Data** tab.

4.  You should see all the imported **Knowledge Assessments**.

5.  Select **Apps** and click to open the **Fabrikam Assessments** application.

6.  The imported data should show up in the application.

7.  Close the **Fabrikam Assessment** application.

8.  Select **Apps** and click to open the **Knowledge Admin** application.

9.  Click on the **Site Map** button and select **Assessments**.

10. The imported **Knowledge Assessments** should be on this view.

11. Click to open one of the **Knowledge Assessments** you imported.

12. Locate the **Days Remaining** field in the header and make sure it has a
    calculated value.
