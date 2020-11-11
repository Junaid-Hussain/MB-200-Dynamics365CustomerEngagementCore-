---
lab:
    title: 'Lab: Creating Tables and Columns'
    module: 'Module 2: Data Model'
---

Module 2: Data Model
====================

## Lesson 2: Practice Lab – Creating tables and Columns

Scenario
--------

You are a functional consultant for your organization Contoso. You are assigned
to work on a project for your client Fabrikam. Fabrikam would like to encourage
their employees to continuously learn.  They want to build an application that
allow a small set of employees to create knowledge assessments and then make
them available to all employees to test their knowledge.  The employees need to
be able to pick an assessment and quickly complete it in just a few minutes. In
this practice, you will be creating a data model to support the applications.

Working with the client, you have determined the following basic needs for
storing data:

-   A Knowledge Assessment Table will represent the actual assessment and
    contain one or more questions in an Table Knowledge Question

-   A Knowledge Test Result Table will track when employees take an assessment

-   The employee who took the assessment will be tracked using the existing
    Common Data Model (CDM) User Table

-   The CDM Feedback Table will be used to allow employees to express their
    opinions on the assessment

After consulting with your Solution Architect, you have come up with the
following data model. When you are done with this module, you will have created
the entities, Columns and relationship to implement the following data model, **as shown in the Lab Resources as Image[MB-200]_M02L02_Creating_Entities_Fields.png**.

In this practice, you will be creating the entities and Columns. Later, when we
discuss relationships you will come back and add the relationships between the
entities. Relationships in the above drawing are the lines connecting the
entities and labeled as 1:N and N:1. The entities that are white with black
writing are standard CDM entities that we will be re-using.

Exercise 1 – Create the Knowledge Assessment Table
---------------------------------------------------

In this exercise, you will be creating the Knowledge Assessment Table and its
Columns. Knowledge Assessment will be a new custom Table you create.

### Task 1 – Create an Table

1.  Navigate to <https://make.powerapps.com>.

2.  Make sure you are in the **Practice** environment you created.

3.  Select **Solutions**.

4.  Click to open the **Common Data Services Default Solution**.

5.  Click **New** and select **Table**.

6.  Enter **Knowledge Assessment** for **Display Name**. Enter **Title** for **Display Name** in the Primary Field section. 

8.  Click **Done**. It may take a few minutes for your Table to be created.

9. With the **Column** tab selected, click **Add Column**.

10. Enter **Start Date** for **Display Name** and select **Date Only** for
    **Data Type**.

11. Click **Advanced Options** and make sure **User Local** is selected for
    **Behavior**.

12. Click **Done**.

13. Click **Add Column** again.

14. Enter **End Date** for **Display Name** and select **Date Only** for **Data Type**.

15. Click **Advanced Options** and make sure **User Local** is selected for
    **Behavior**.

16. Click **Done.**

17. You will now add an **Choice** type filed. Click **Add Column**.

18. Enter **Difficulty** for **Display Name** and select **Choice** for
    **Data Type**.

19. Click on the **Choice** dropdown and select **+New Choice**.

20. Enter **Beginner** for **Item 1** and click **Add New Item**.

21. Enter **Intermediate** for **Item 2** and click **Add New Item**.

22. Enter **Advanced** for **Item 3** and click **Save**.

23. Select **Beginner** for the **Default Value** and click **Done**.

25. Click **Save Table** at the bottom of the screen.

### Task 2 – Create a calculated Column

1.  Click **Add Column**.

2.  Enter **Days Remaining** for **Display Name** and select **Whole Number**
    for **Data Type**.

3.  Click **Advanced Options**.

4.  Enter **0** for **Minimum Value** and **1000** for **Maximum Value**.

5.  Click **+Add** next to **Calculated or Rollup**. Click **+Calculation.**

6.  Click **Save**. A pop-up window should appear allowing you to configure the calculation.

9.  Click **Add Action**.

10. Enter *DIFFINDAYS(NOW(), crXXX_enddate)* and click on the checkmark. Note
    that crXXX is environment dependent and the name of your environment will be different. To find your environment-specific designation, type **cr** and wait
    for the field to auto filter to your environment.

11. Click the check box.

12. Click **Save and Close**.

13. Click **Done**.

Exercise 2 – Create the Knowledge Question Table
-------------------------------------------------

In this exercise, you will be creating the Knowledge Question Table and its
Columns.

### Task 1 – Create an Table

1.  Go back to <https://make.powerapps.com> and make sure you are in your
    **Practice** environment.

2.  Select **Solutions**.

3.  Open the **Common Data Services Default Solution**.

4.  Click **+New** and select **Table**.

5.  Enter **Knowledge Question** for Display Name.

6.  Navigate to the **Primary Field** section.

7.  Change the **Display Name** to **Question**. The **Name** field should also automatically update to **Question.** Click **Done**.

8.  Make sure the **Column** tab is selected and click **Add Column**.

9.  Enter **Answer 1** for **Display Name**, select **Text** for **Data Type**
    and click **Done**.

10. Add **3** more with values below:

    - Name: **Answer 2**, Data Type: **Text**.

    - Name: **Answer 3**, Data Type: **Text**.

    - Name: **Answer 4**, Data Type: **Text**.

14. Click **Add Column**.

15. Enter **Answer 1 Points** for **Display Name**, select **Whole Number** for
    **Data Type** and click **Done**.

16. Add 3 more filed with values below. These will store the points awarded if
    someone picks this answer.

    - Name **Answer 2 Points** Data Type **Whole Number**.

    - Name **Answer 3 Points** Data Type **Whole Number**.

    - Name **Answer 4 Points** Data Type **Whole Number**.

    - Click **Save Table**.

**Note:** There are many ways you could model the answers depending on the complexity of your requirements. The approach shown here is simplified for practice purposes to focus on demonstrating how to work with the Table creation process.

Exercise 3 – Create the Knowledge Test Result Table
----------------------------------------------------

In this exercise, you will be creating the Knowledge Test Result Table and its
Columns.

### Task 1 – Create an Table

1.  On the navigation menu, click **Common Data Services Default Solution** to return to the solution.

2.  Click **+New** and select **Table**.

3.  Enter **Knowledge Test Result** for **Display Name** and click **Done**.

4.  Click **Add Column**.

5.  Enter **Total Points** for **Display Name** and select **Whole Number** for
    **Data Type**.

6.  Click **Done**.

7.  Click **Save Table**.

Exercise 5 – Add existing Tables to the solution
--------------------------------------------------

In this exercise, you will be adding the existing Tables Feedback and User.
This ensures when relationships are created later between theses Tables they
will be tracked as part of the solution.

### Task 1 – Add existing Tables

1.  From the navigation menu, click **Common Data Services Default Solution** to return to the solution.

2.  Click **Add Existing** and select **Table**.

3.  Select the **Feedback** and **User** Tables and click **Next**.

4.  Leave the **Include All Components** and **Include Table Metadata**
    unchecked and click **Add**.

5.  Your solution will now have **5 Tables** and **1 Choice** in addition to your apps.

6.  Click **Publish All Customizations**.
