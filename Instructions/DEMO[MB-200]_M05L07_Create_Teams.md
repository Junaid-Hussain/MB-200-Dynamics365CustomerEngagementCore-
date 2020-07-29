---
lab:
    title: 'Lab: Create teams'
    module: 'Module 5: Security'
---

Module 5: Security
==================
### Practice Lab – Create teams

Scenario
--------

You are a functional consultant for your organization Contoso. You are assigned
to work on a project for your client Fabrikam. You will be continuing your work
on the model-driven Knowledge Admin app. In this practice, you will be creating
teams and business units.

Fabrikam will use a combination of teams and business units to organize access
to records. We have one group to manage North America sales, and another to
manage EMEA sales, they share a manager. Sometimes we have elite salespeople
that have global access for read on account entities regardless of their
business unit.

Exercise 1 – Teams and Business Units
-------------------------------------

### Task 1 – Create Business Units

In this task, you will create two business units, one for North America and one
for EMEA.

1.  Navigate to <https://admin.powerplatform.microsoft.com>

2.  Select the **Environments**.

3.  Select the **Practice** environment and click **Settings**.

4.  Locate the **Users + Permissions** section and click **Business Units.**

5.  Click **New**.

6.  Enter **North America** for **Name** and click **Save and New**.

7.  Enter **EMEA** for **Name** and click **Save and Close**.

8.  Close the **Business Units** window. Do not close the **Settings** page.

### Task 2 – Add Users to Business Unit

In this task, you will move User One to EMEA business unit and move User Two to
North America.

1.  Locate the **Users + Permissions** section and click **Users**.

2.  Select **User One** and click **Change Business Unit**. If you do not see
    **Change Business Unit** in the command bar, then change the **1** at the
    end of your URL to a **0** and press enter. You should now be able to select
    **User One** and click **Change Business Unit**.

3.  Select **EMEA** and click **OK**.

4.  Select **User Two** and click **Change Business Unit**.

5.  Select **North America** and click **OK**.

6.  Close the **Users** window. Do not close the **Settings** window.

### Task 3 – Assign Security Roles

You have to re-assign security roles when you move Users from one business unit
to another. In this task, you will assign the Knowledge Assessment User role to
each User One and User Two.

1.  Locate the **Users + Permissions** section and click **Users**.

2.  Select **User One** and click **Manage Roles**. If you do not see **Manage
    Roles** in the command bar, then change the **1** at the end of your URL to
    a **0** and press enter. You should now be able to select **User One** and
    click **Manage Roles.**

3.  Select **Knowledge Assessment User** and click **OK**.

4.  Select **User Two** and click **Manage Roles**.

5.  Select **Knowledge Assessment User** and click **OK**.

6.  Close the **Users** window. Do not close the **Settings** window.

### Task 4 – Create Team

In this task, you will create a new team.

1.  Locate the **Users + Permissions** section and click **Teams**.

2.  Click **+New**.

3.  Enter **Global Team** for **Name**.

4.  Select your **org** name for the **Business Unit.**

5.  Select the admin user you are logged in as for **Administrator**.

6.  Click **Save and Close**.

7.  Close the **Teams** window. Do not close the **Settings** window.

### Task 5 – Create Security Role

In this task, you will create a security role that will get Organization level
Read privilege to all Accounts.

1.  Locate the **Users + Permissions** section and click **Security Roles**.

2.  Click **New**.

3.  Enter **Elite Salespeople** for **Role Name**.

4.  Select the **Core Records** tab.

5.  Locate the **Account** entity and click on the **Read** circle four times.
    This security role will now get organization level **Read** privilege to all
    **Accounts**.

6.  Click **Save and Close**.

7.  Close the **Security Roles** window. Do not close the **Settings** window.

### Task 6 – Add User to Team

In this task, you will assign the Elite Salespeople security to the Global Team
and then add User One to the Global Team.

1.  Locate the **Users + Permissions** section and click **Teams**.

2.  Ensure that you are looking at the **All Teams** view

3.  Select the **Global Team** and click **Manage Roles**.

4.  If **Manage Roles** does not appear in the command bar, then select the
    **Settings** symbol from the black **Navigation Bar.** Click **Advanced
    Settings** and navigate to **Teams** by clicking on **Security** and then
    **Teams.** Then, Select the **Global Team** and click **Manage Roles**.

5.  Select **Elite Salespeople** and click **OK**.

6.  Select the **Global Team** again and click **Add Members**.

7.  Click on the lookup button.

8.  Select **User One** and click on the **Select** button.

9.  Click **Add**.

10. Click **OK**.

11. Close the Teams window.
