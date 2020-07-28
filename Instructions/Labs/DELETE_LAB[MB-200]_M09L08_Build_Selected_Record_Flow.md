---
lab:
    title: 'Lab: Build a selected record flow'
    module: 'Module 9: Microsoft Power Automate'
---

Module 9: Microsoft Power Automate
========================

## Lesson 8: Practice Lab – Build a selected record flow

Scenario
--------

Your client Fabrikam needs the ability to create new knowledge assessments from
existing assessments without duplicating effort to populate data. In this lab,
you will create a Microsoft Power Automate to create a new assessment from an existing
assessment.

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

Exercise 2 – Create flow 
-------------------------

### Task 1 – Create flow

1.  Navigate to <https://web.powerapps.com>

2.  Select the **Practice** environment you created.

3.  Expand **Business Logic**.

4.  Select **Flows** and click **Create from Blank**.

5.  Click **Create from Blank** again.

6.  Search for **Common Data Service** and select **When a Record is Selected.**

7.  Select **Practice** for **Environment** and select **Knowledge Assessments**
    for **Entity Name**.

8.  Click **+ Add an Input**.

9.  Select **Text**.

10. Replace **Input** with **New Title**.

11. Replace **Please enter input** with **Please provide title for the new
    assessment**.

12. Click **Add an Input** again.

13. Select Yes/No.

14. Replace **Yes/No** with **Include Questions?**

15. Click on the **… Menu** button and select **Rename**.

16. Rename the step **When Assessment is Selected**.

17. Change the flow name to **Create Assessment from Existing**.

### Task 2 – Create New Assessment

1.  Click **+ New Step**.

2.  Search for **Common Data Service** and select **Create a New Record**.

3.  Click on the **… Menu** button and select **Rename**.

4.  Rename the step **Create New Assessment**.

5.  Select **Practice** for **Environment** and select **Knowledge Assessments**
    for **Entity Name**.

6.  Click the **Title** field and select **New Title** from the **Dynamic
    Content** pane.

7.  Click **Show Advanced Options**.

8.  Click on the **Difficulty Value** field and **Enter Custom Value**.

9.  Select **Difficulty Value** form the **Dynamic Content** pane.

10. Click on the **End Date** field and select **End Date** from the **Dynamic
    Content** pane.

11. Click on the **Notify Manager** field and select **Enter Custom Value**.

12. Select **Notify Manager** from the **Dynamic Content** pane.

13. Click on then **Start Date** field and select **Start Date** from the
    **Dynamic Content** pane.

14. Click **Save** to save the flow.

### Task 3 – Add Questions Condition

1.  Click **+ New Step**.

2.  Search for **Condition** and select **Condition** control.

3.  Click on the first **Choose Value** field of the **Condition**.

4.  Select **Include Questions?** From the Dynamic Content pane.

5.  Select on the second **Choose Value** field of the **Condition** and type
    **true**.

6.  Click Save to save the flow.

### Task 4 – Get Questions

1.  Select **Solutions** and click to open the **Knowledge Assessment
    Solution**.

2.  Locate the **Name** column and make a note of the prefix. The prefix will
    look like **cre7f\_**

3.  Expand **Business Logic** and select **Flows**.

4.  Select **Create Assessment from Existing** and click **Edit**.

5.  Go to the **If Yes** branch and click **Add an Action**.

6.  Search for **Common Data Service** and select **List Records**.

7.  Select **Practice** for **Environment** and select **Knowledge Questions**
    for **Entity Name**.

8.  Click **Show Advanced Options**.

9.  Click on the **Filter Query** field and type the snippet below. Replace the
    **cre7f\_** with the prefix from **step 2**.

>   \_cre7f_knowledgeassessment_value eq ''

1.  Place your cursor between ' and '

2.  Go to the **Dynamic Content** pane, search for **Knowledge Assessment**, and
    select **Knowledge Assessment** from the **When assessment is Selected**
    group.

3.  Click on the **… Menu** button and select **Rename**.

4.  Rename the step **Questions**.

5.  Click **Save** to save the flow.

### Task 5 – Create Questions

1.  Go to the **If Yes** branch and click **Add an Action** again.

2.  Search for **Common Data Service** and select **Create a New Record**.

3.  Select **Default** for **Environment** and select **Knowledge Questions**
    for **Entity Name**.

4.  Click on the **… Menu** button and select **Rename**.

5.  Rename the step **Create Question**.

6.  Click on the **Question** field and select **Question** from the Dynamic
    Content pane.

7.  **Apply to Each** step will be created for you.

8.  Click on the **Question Type Value** field and select **Enter Custom
    Value**.

9.  Select **Question Type Value** from the **Dynamic Content** pane.

10. Click **Show Advanced Options**.

11. Click **Answer 1** field and select **Answer 1** from the **Dynamic
    Content** pane.

12. Click **Answer 1 Points** field and select **Answer 1 Points** from the
    **Dynamic Content** pane.

13. Click **Answer 2** field and select **Answer 2** from the **Dynamic
    Content** pane.

14. Click **Answer 2 Points** field and select **Answer 2 Points** from the
    **Dynamic Content** pane.

15. Click **Answer 3** field and select **Answer 3** from the **Dynamic
    Content** pane.

16. Click **Answer 3 Points** field and select **Answer 3 Points** from the
    **Dynamic Content** pane.

17. Click **Answer 4** field and select **Answer 4** from the **Dynamic
    Content** pane.

18. Click **Answer 4 Points** field and select **Answer 4 Points** from the
    **Dynamic Content** pane.

19. Click on the **Scenario Description** field and select **Scenario
    Description** from the **Dynamic Content** pane.

20. Click on the **Knowledge Assessment** field, go to the **Dynamic Content**
    pane and search for **Knowledge Assessment**.

21. Select **Knowledge Assessment** from the **Create New Assessment** group.

22. Click **Save** to save the flow.

### Task 6 – Test flow

1.  Navigate to <https://web.powerapps.com>

2.  Make sure you have the **Practice** environment selected.

3.  Select **Apps** and click to open the **Knowledge Admin** application.

4.  Select **Assessments** and click to open the **Test Assessment** record.

5.  Click on the **Flow** button located in the command bar and select the
    **Create Assessment from Existing** you created.

6.  Click **Continue**.

7.  Enter **New Assessment with Questions** for **New Title**, select **Yes**
    for **Include Questions**, and click **Run Flow**.

8.  Click **Done**.

9.  Select Assessments.

10. The new assessment should be on the list of assessments. Click on the **New
    Assessment with Questions**.

11. Select the **Questions** tab.

12. You should see questions.

13. Click **Flow** and select **Create assessments from Existing** again.

14. Enter **New Assessments without Questions** for **New Title** and click
    **Run Flow**.

15. Click Done.

16. Select **Assessments**.

17. Click to open the **New Assessment without Questions** record.

18. Select the **Questions** tab.

19. This assessment will have no questions.
