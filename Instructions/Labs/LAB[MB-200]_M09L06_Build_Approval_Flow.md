Module 9: Microsoft Flow
========================

## Lesson 6: Practice Lab – Build approval flow

Scenario
--------

Your client Fabrikam needs an approval process added to the model-driven
Knowledge Admin app you are building. The approval process will interact with
the user's manager to obtain an approval or rejection and handle the knowledge
assessment appropriately. In this lab, you will create a Microsoft Flow to
retrieve the appropriate manager, seek their approval and handle the record
after the manager's decision is entered.

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

Exercise 2 – Prepare the Solution 
----------------------------------

### Task 1 – Add Field to Knowledge Assessment

1.  Navigate to <https://web.powerapps.com>

2.  Select the **Practice** environment you created.

3.  Select **Solutions**.

4.  Click to open the **Knowledge Assessment Solution** you imported.

5.  Click to open the **Knowledge Assessment** entity.

6.  Click select the **Fields** tab and **+ Add Field**.

7.  Enter **Notify Manager** for **Display Name**, select **Two Options** for
    **Data Type** and click **Done**.

8.  Click **Save Entity**.

9.  Click **+ Add Field**.

10. Enter **Approval Status** for **Display Name** and select **Option Set** for
    **Data Type**.

11. Click on the **Option Set** dropdown and select **New Option Set**.

12. Enter **Waiting** for the first item and click **Add New Item**.

13. Enter **Approved** for the second item and click **Add New Item**.

14. Enter **Rejected** for the third item and click **Save**.

15. Click **Done**.

16. Click **Save Entity**.

### Task 2 – Add Field to Knowledge Assessment Form

1.  Make sure you still have the **Knowledge Assessment** selected.

2.  Select the **Forms** tab and click on the Main form.

3.  Add the **Notify Manager** field to the form.

4.  Add the **Approval Status** field to the form.

5.  Click **Save**.

6.  Click **Publish**.

7.  Click **Save and Close**.

8.  Click **Done**.

9.  Click on the solution name **Knowledge Assessment Solution** located in the
    navigation breadcrumbs.

10. Click **Publish All Customizations**.

Exercise 3 – Create Flow 
-------------------------

### Task 1 – Create Flow

1.  Navigate to <https://web.powerapps.com>

2.  Select the **Practice** environment you created.

3.  Expand **Business Logic**.

4.  Select **Flows** and click **Create from Blank**.

5.  Click **Create from Blank** again.

6.  Search for **Common Data Service** and select **When a Record is Updated
    (Preview).**

7.  Select **Practice** for **Environment**, select **Knowledge Assessments**
    for **Entity Name**, and select **Organization** for **Scope**.

8.  Click **Show Advanced Options**.

9.  Select **NotifyManager** for Attribute Filter.

10. Click on the **… Menu** button and select **Rename**.

11. Rename the step **When Assessment is Updated**.

### Task 2 – Add Condition

1.  Click **+ New Step**.

2.  Search for **Condition** and select **Condition** control.

3.  Click on the **Choose a Value** field and select **Notify Manager** from the
    **Dynamic Content** pane.

4.  Select **is Equals to** for operator.

5.  Select the last field and type **true**.

6.  Click on the **… Menu** button of the condition and select **Rename**.

7.  Rename the condition **Check Notification.**

### Task 3 – Update Waiting Assessment

1.  Click **Add an Action** of the **If Yes** branch.

2.  Search for **Common Data Service** and select **Update a Record**.

3.  Select **Practice** for **Environment**, select **Knowledge Assessments**
    for **Entity Name**, and click on the **Item Identifier** field.

4.  Select **Knowledge Assessment** from the **Dynamic Content** pane.

5.  Click **Show Advanced Options.**

6.  Locate the **Approval Status Value** field and select **Waiting**.

7.  Click on the **… Menu** button of the step and select **Rename**.

8.  Rename the step **Update Waiting Assessment**

### Task 4 – Get User

1.  Click **Add an Action** of the **If Yes** branch.

2.  Search for **Common Data Service** and select **Get Record**.

3.  Select **Practice** for **Environment**, select **Users** for **Entity
    Name**, and click on the **Item Identifier** field.

4.  Select **Created By** from the **Dynamic Content** pane.

5.  Click on the **… Menu** button of the **Get Record** step and select
    **Rename**.

6.  Rename the step **Get Created User**.

### Task 5 – Get Manager

1.  Click **Add an Action** of the **If Yes** branch again.

2.  Search for **Common Data Service** and select **Get Record**.

3.  Select **Practice** for **Environment**, select **Users** for **Entity
    Name**, click on the **Item Identifier** field.

4.  Go to the **Dynamic Content** pane, search for **Manager** and select
    **Manager** from the **Get Created User** section.

5.  Click on the **… Menu** button and select **Rename**.

6.  Rename the step **Get Manager**.

### Task 6 – Start Approval

1.  Click **Add an Action** of the **If Yes** branch.

2.  Search for **Approvals** and select **Start an Approval**.

3.  Select **Approve/Reject – First to respond** for **Approval Type**.

4.  Enter **Manager Notification Approval** for **Title**,

5.  You will usually send the approval request to a manager or other decision
    makers, but in this lab, you will select the user you are logged in as.
    Select the **Assigned To** field.

6.  Go to the **Dynamic Content** pane and click **Get Created User**.

7.  Search for **Primary Email** and select **Primary Email** from the **Get
    Created User** section.

8.  select the **Requestor** filed, go to the **Dynamics Content** pane, search
    for **Primary Email**, and select **Primary Email** from the **Get Created
    User** section.

9.  Select the Details filed, go to the **Dynamics Content** pane, search for
    **Full Name**, and select **Full Name** from the **Get Created User**
    section.

10. Add a comma after the **Full Name** and type **created an assessment that
    requires manager’s approval**.

11. Press the enter key to start a new line.

12. Type **Assessment Name:**

13. Go to the **Dynamics Content** pane, search for **Title**, and select
    **Title** from the **When Assessment is Updated** section.

14. Press enter key to start a new line.

15. Type **Manager:**

16. Go to the **Dynamics Content** pane, search for **Full Name**, and select
    **Full Name** from the **When Get Created User** section.

17. It is good practice to include a link to the record that needs the approval.
    Start a new browser window and navigate to <https://web.powerapps.com>

18. Make sure you are in the **Practice** environment.

19. Select **Apps** and click to open the **Knowledge Admin** application.

20. Select **Assessment** and click to open the **Test Assessment**.

21. Find the **Pop Out** button located in bottom left of the form and click on
    it.

22. A new window will open, copy the **URL** of the window.

23. Open a notepad and paste the URL.

24. The **URL** will look like the link below.

    https://practice.crm.dynamics.com/main.aspx?appid=97595509-8a00-458d-856d-1569b42d6282&pagetype=entityrecord&etn=cre7f_knowledgeassessment&id=540a380a-74f9-e811-a950-000d3a1bc3f6

25.	Copy everything before the last GUID.

    https://practice.crm.dynamics.com/main.aspx?appid=97595509-8a00-458d-856d-1569b42d6282&pagetype=entityrecord&etn=cre7f_knowledgeassessment&id=


26.  Go back to the Flow and select the Item Link field.

27.  Paste the **URL** you copied.

28.  Go to the **Dynamic Content** pane, search for **Knowledge Assessment** and
    select **Knowledge Assessment**.

### Task 7 – Add Condition

1.  Click **Add an Action** of the **If Yes** branch.

2.  Search for **Condition** and select **Condition** control.

3.  Click on the first Choose a Value field and select Response from the Dynamic
    Content pane.

4.  Leave **Is Equals to** as the operator.

5.  Click on the **Choose a Value** field and type **Approve**.

6.  Click on the **… Menu** button of the condition and select **Rename**.

7.  Rename the condition **Check Response**.

### Task 8 – Update Approved Assessment

1.  Click **Add an Action** of the **If Yes** branch of the **Check Response**
    condition.

2.  Search for **Common Data Service** and select **Update a Record**.

3.  Select **Practice** for **Environment**, select **Knowledge Assessments**
    for **Entity Name** and click on the **Record Identifier** field.

4.  Select **Knowledge Assessment** from the **Dynamic Content** pane.

5.  Click **Show Advanced Options**.

6.  Locate the **Approval Status Value** field and select **Approved**.

7.  Click on the **… Menu** button of the step and select **Rename**.

8.  Rename the step **Update Approved Assessment**.

### Task 9 – Update Rejected Assessment

1.  Click **Add an Action** of the **If No** branch of the **Check Response**
    condition.

2.  Search for **Common Data Service** and select **Update a Record**.

3.  Select **Default** for **Environment**, select **Knowledge Assessments** for
    **Entity Name** and click on the **Record Identifier** field.

4.  Select **Knowledge Assessment** from the **Dynamic Content** pane.

5.  Click **Show Advanced Options**.

6.  Locate the **Approval Status Value** field and select **Rejected**.

7.  Click on the **… Menu** button of the step and select **Rename**.

8.  Rename the step **Update Rejected Assessment**.

9.  Click **Save** to save the flow.

### Task 10 – Test Flow

1.  Navigate to <https://web.powerapps.com>

2.  Make sure you are in the **Practice** environment.

3.  Select **Apps** and click to open the **Knowledge Admin** application.

4.  Select **Assessment** and click to open the **Test Assessment**.

5.  Locate the **Approval Status** and make sure no value is selected.

6.  Locate the **Notify Manager** field and set it to **Yes**.

7.  Click **Save**.

8.  Click **Refresh**.

9.  Locate the **Approval Status** field and make sure it is now set to
    **Waiting**.

10. Navigate to <https://flow.microsoft.com>

11. Login if prompted.

12. Make sure you are in the **Practice** environment.

13. Select **Approvals**.

14. You should see an approval with the title **Manager Notification Approval**.
    Click on the approval tile.

15. The approval pane will open. Make sure the information in the details is
    what you expected.

16. Click on the **Link**.

17. The Knowledge Assessment record should open.

18. Close the Knowledge Assessment.

19. Click **Approve**.

20. Add **Comment** and click **Confirm**.

21. Close the approval pane.

22. Select the **History** tab.

23. The approval should show up in this list as **Approved**.

24. Go back to the **Knowledge Admin** app.

25. Refresh the Test Assessment.

26. The **Approval Status** field should be set to **Approved**.
