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

Exercise 1 – Create Solution and Publisher
------------------------------------------

In this exercise, you will create a new environment, create a new publisher, and
create a new solution.

### Task 1 – Create Environment 

In this task, you will create a new environment.

1.  Navigate to https://admin.powerplatform.com and access the **Environments** tab.

2.  Click **+New**.

3.  Enter **Development** for **Name**, **Trial** for **Type**, and toggle **Create a database...** to **Yes.**

4.  Click **Save.**

5.  On the next tab, keep all fields as defualt and click **Save** again.

6.  Wait for the environment to be created. 

### Task 2 – Create Publisher 

In this task, you will create a new publisher.

1.  Navigate to <https://make.powerapps.com>

2.  In the upper right-hand corner, click on the environment selector and chose
    the development environment created in task 1.

3.  From the far upper right-hand corner of the command bar, click on the gear
    wheel icon to open the settings menu and select **Advanced Settings.**

4.  From the dropdown next to **Settings**, select **Customizations.** 

5.  Select **Publishers** and click **New**.

6.  Enter **Contoso** for **Display Name**, **Contoso** for **Name**, and
    **contoso** for **Prefix**.

7.  Click **Save and Close**.

8.  Close the Publishers browser tab.

### Task 3 – Create Solution

In this task, you will create a new solution.

1.  Navigate to <https://make.powerapps.com.

2.  Make sure you are in the **Development** environment.

3.  Select **Solutions**.

4.  Click **+New Solution**.

5.  Enter **Contoso Customer Problems** for **Display Name**.

6.  Select **Contoso** for **Publisher**.

7.  Enter **1** for **Version** and click **Create**.
