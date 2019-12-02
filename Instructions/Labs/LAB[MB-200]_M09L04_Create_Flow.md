---
lab:
    title: 'Lab: Create a flow'
    module: 'Module 9: Microsoft Power Automate'
---

Module 9: Microsoft Power Automate 
========================

## Lesson 4: Practice Lab – Create a flow

Scenario
--------

As a functional consultant at Contoso, you are you continuing to work on a
model-driven Knowledge Admin app for your client Fabrikam. Your client has
requested an automation that should run weekly without user involvement. You
can’t schedule a workflow without custom code so you will need to use a
Microsoft Power Automate. In this lab, you will create a flow to run weekly and
test the flow.

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

Exercise 2 – Create Microsoft Power Automate
-----------------------------------

In this exercise, you will create a flow that will run once a week. This flow
will check if there are Knowledge Assessment with End Date of today or older and
deactivate them.

### Task 1 – Create a flow

1.  Navigate to <https://web.powerapps.com>

2.  Make sure you have the **Practice** environment selected.

3.  Select **Solutions** and click to open the **Knowledge Assessment
    Solution**.

4.  Locate the Name column and make a note of the name **Prefix**. The prefix
    will look like **cre7f_**

5.  Expand **Business Logic** and select **Flows**.

6.  Click **+ New** and select **Create from Blank**.

7.  Click **Create from Blank** again.

8.  Select your **Country/Region** and click **Get Started**.

9.  Make sure you are in the **Practice** environment you created.

10. Search for **Recurrence** and select **Recurrence Schedule**.

11. Enter **1** for **Interval** and select **Minute** for **Frequency**. You
    will usually run this type Flow every daily or weekly.

12. Click **+ New Step**.

13. Search for **Common Data Service** and select **List Records**.

14. Select **Practice** for **Environment** and **Knowledge Assessments** for
    **Entity Name**.

15. Click on **Show advanced options**.

16. Select the **Filter Query** field and type **cre7f_enddate lt** and replace
    cre7f\_ with your prefix from step 4 of this task.

17. Select the **Expression** of the **Dynamics Content** pane.

18. Type **utcNow()** and click **OK.**

19. Click on the **… Menu** button of the step and select **Rename**.

20. Rename the step **Get Assessments**.

21. Click **+ New Step**.

22. Search for **Common Data Service** and select **Update a Record**.

23. Select **Practice** for **Environment**, select **Knowledge Assessments**
    for **Entity Name**, and select the **Record Identifier** field.

24. Select **Knowledge Assessment** from the **Dynamic Content** pane.

25. **Apply to Each** step will be added and **Value** will be selected for
    Output. Click **Show Advanced Options**.

26. Locate the **Status Value** option set and select **Inactive**.

27. Click on the **… Menu** button of the step and select **Rename**.

28. Rename the step **Deactivate Assessment**.

29. Scroll up and click on the **Name** of the flow.

30. Rename the flow **Deactivate Old Assessments**.

31. Click **Save**. Don’t navigate away from the flow.

### Task 2 – Test your flow

1.  Start a new Browser window and navigate to <https://web.powerapps.com>

2.  Make sure you are in the **Practice** environment.

3.  Select **Apps** and click to open the **Knowledge Admin** application.

4.  Select **Assessments** and click to open the **Test Assessment**.

5.  Locate the **End Date** field and select today’s date.

6.  Click **Save**.

7.  Go back to the flow you created.

8.  Click **Test**.

9.  Select **Using Data from Previous Runs.**

10. Select the latest run and click **Save & Test**.

11. The flow should run and succeed.

12. Go back to the **Knowledge Admin** application.

13. Select **Assessments**.

14. The **Active Knowledge Assessments** view should be empty.

15. Click on the view name and select the **Inactive Knowledge Assessments**
    view.

16. The deactivated record will now be in this view.

17. Go back to flow and click **Edit**.

18. Click on the Recurrence step.

19. Change the **Recurrence** from **Minute** to **Week** the

20. Click **Save**.

21. Go back to the **Knowledge Admin** application.

22. Select **Assessments**.

23. Click on the view name and select the **Inactive Knowledge Assessments**
    view.

24. Click to open the **Test Assessment** record.

25. Click **Activate**.

26. Confirm activation.

27. Change the **End Date** to one month from today.

28. Click **Save**.
