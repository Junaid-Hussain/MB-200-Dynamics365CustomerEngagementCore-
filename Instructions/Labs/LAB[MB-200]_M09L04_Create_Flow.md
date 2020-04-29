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
Microsoft Power Automate flow. In this lab, you will create a flow to run weekly and
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

### Task 1 – Connect to the Power Platform administration portal

1.  On Virtual machine MB200-Dynamics_Lab, sign in as Admin with the password
    Pa55w.rd if you are not already logged in.

2.  Outside the VM in the online lab interface click Files and choose D365
    Credentials. This will allocate an Office 365 tenant for you to use in these
    labs.  It will display the admin email and password for your tenant.  You
    should copy this information to notepad or similar for your reference.

3.  In MB200-Dynamics_Lab launch Microsoft Edge from the taskbar. By default,
    the browser opens Office 365. Use the O365 credentials you just acquired in
    the previous step to login.

4.  Navigate in the browser to the Power Platform admin portal at https://admin.Powerplatform.microsoft.com.

Exercise 2 – Create Microsoft Power Automate
-----------------------------------

In this exercise, you will create a flow that will run once a week. This flow
will check if there are Knowledge Assessment with End Date of today or older and
deactivate them.

### Task 1 – Create a flow

2.  Make sure you have your **Practice** environment selected.

3.  Select **Solutions** and click to open the **Common Data Services Default Solution.**

4.  Locate the Name column and make a note of the name **Prefix**. The prefix
    will look like **crXXX_**.

5.  From the lefthand menu, select **Flows.**

6.  Click **+ New** and select **+ Automated - From Blank**.

7.  The pop-up will show common triggers that you can easily select to jumpstart your flow configuration. Scroll through the options, but do not select anything. When you are ready, press **Skip.**

8. In the box that says **Search connectors and triggers**, type **Recurrence.** Select the **Recurrence** option from the **Triggers** tab.

9. Select **+ New step.**

10. Select **Common Data Service** from the connection options.

11. Select **List records.** 

12. In the **Environment** box, start typing your unique alias for the lab. Select your **Practice** environment when it shows up.

13. Select **Knowledge Assessments** for Entity.

14. Click on **Show advanced options.**

16. Select the **Filter Query** field and type **crXXX_enddate lt** and replace
    crXXX_ with your unique prefix.

17. Select the **Expression** of the **Dynamics Content** pane.

18. Type **utcNow()** and click **OK.**

19. Click on the **… Menu** button of the step and select **Rename**.

20. Rename the step **Get Assessments**.

21. Click **+ New Step**.

22. Click on **Common Data Service** and select **Update a Record**.

23. Select your **Practice** environment for **Environment**, select **Knowledge Assessments**
    for **Entity Name**, and select the **Record Identifier** field.

24. Select **Knowledge Assessment** from the **Dynamic Content** pane.

25. **Apply to Each** step will be added and **Value** will be selected for Output. Click on **Update a record** and then click **Show Advanced Options**.

26. Locate the **Status Value** option set and select **Inactive**.

27. Click on the **… Menu** button of the step and select **Rename**.

28. Rename the step **Deactivate Assessment**.

29. Scroll up and click on the name of the flow by clicking **Untitled.**

30. Rename the flow **Deactivate Old Assessments**.

31. Click **Save**. Don’t navigate away from the flow.

### Task 2 – Test your flow

1.  Start a new Browser window and navigate to https://make.powerapps.com.

2.  Make sure you are in your **Practice** environment.

3.  Select **Apps** and click to open the **Knowledge Admin model-driven application**.

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

14. **Test Assessment** should now be missing from the view.

15. Click on the view name and select the **Inactive Knowledge Assessments**
    view.

16. The deactivated record will now be in this view.

17. Go back to flow and click **Edit**.

18. Click on the Recurrence step.

19. Change the **Recurrence** from **Minute** to **Week**.

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
