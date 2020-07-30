---
lab:
    title: 'Lab: Solution components'
    module: 'Module 15: Manage Solutions'
---

Module 15: Manage Solutions
==========================
## Practice Lab – Solution components


Scenario
--------

As a functional consultant at Contoso, you’ve been asked to help create an app
that tracks customers current problems. In these practices on solutions, you
will create a solution to track all your components, export and import into
production, and then go through a maintenance cycle using patches to update the
deployed solution. In this practice, you will be doing the following:

-   Add an option set

-   Add an existing entity

-   Add a new entity

-   Create a new application


Exercise 1 – Add Components
---------------------------

In this exercise, you will add components to the solution you created.

### Task 1 – Add Option Set 

In this task, you will add an option set for customer challenge level to the
solution you created.

1.  Navigate to https://make.powerapps.com.

2.  Make sure you have the **Development** environment selected.

3.  Select **Solutions**.

4.  Locate and click to open the **Contoso Customer Problems** solution you
    created.

5.  Click **+ New**.

6.  Click Other and select **Option Set**.

7.  Enter **Customer Challenge Level** for **Display Name**.

8.  Click Add **New Item**.

9.  Type **High** and click **Add New Item** again.

10. Type **Low** and click **Save**. DO NOT navigate away from this page.

### Task 2 – Add Existing Entity

In this task, you will add the account entity to the solution you created, add
new fields to the entity, and add the field to the main form.

1.  Click **Add Existing** and select **Entity**.

2.  Locate and select the **Account** entity.

3.  Click **Next**.

4.  Click **Select Components**.

5.  Select the **Forms** tab.

6.  Select the **Account** main form and click **Add**.

7.  Click **Add** again.

8.  Click on the **Account** entity you just added to the solution.

9.  You should have the **Fields** tab selected.

10. Click **+ Add Field**.

11. Enter **Challenge Last Updated** for **Display Name**.

12. Select **Date and Time** for **Data Type** and click **Done**.

13. Click **Save Entity**.

14. Select the **Forms** tab.

15. Click to open the **Main** Acccount form.

16. Select the **Summary** tab.

17. Go to the **Field Explorer** and double click on the **Challenge Last
    Updated** field you created.

18. Click **Save**.

19. Click **Publish**.

20. Click the back arrow.

21. Click **Done**.

### Task 3 – Add New Entity Challenge Entity

In this task, you will add a new entity to the solution and created many-to-one
relationship between the problem and account entity.

1.  Navigate to https://web.powerapps.com

2.  Make sure you have the **Development** environment selected.

3.  Select **Solutions**.

4.  Click to open the **Contoso Customer Problems** solution.

5.  Click **New** and select **Entity**.

6.  Enter **Problem** for **Name** and **Problems** for **Plural Name**.

7.  Click **Next**.

8.  Click on the **Primary Name** field.

9.  Change the **Display Name** to **Name**, change the **Name** to **Name** and
    click **Done**.

10. Click **Save Entity**.

11. Click **Add Field**.

12. Enter **Level** for **Display Name** and select **Option Set** for **Data
    Type**.

13. Click on the **Option Set** drop down.

14. Select the **Customer Challenge Level** you created.

15. Click **Done**.

16. Click **Save Entity**.

17. Select the **Forms** tab.

18. Click to open the **Main Information** form.

19. Add the **Level** field to the form.

20. Click **Save**.

21. Click **Publish**.

22. Click **Save and Close**.

23. Click **Done**.

24. Select the **Relationships** tab.

25. Click **Add Relationship** and select **Many-to-One**.

26. Select **Account** for the **Related Entity** and click **Done**.

27. Click **Save Entity**.

28. Above the tabs will read Solutions \> Contoso Customer Problems \> Problem.
    Click **Contoso Customer Problems**.

29. Click **Publish All Customizations**.

### Task 4 – Create New Application

In this task, you will create a new Model-Driven application.

1.  Navigate to https://web.powerapps.com

2.  Make sure you have the **Development** environment selected.

3.  Select **Solutions**.

4.  Click to open the **Contoso Customer Problems** solution.

5.  Click **+ New**.

6.  Click **App** and select **Model-Driven**.

7.  Select **Apps**.

8.  Click **Create an App** and select **Model-Driven**.

9.  Enter **Contoso Customer Challenges** for **Name**.

10. Click **Done**.

11. Click **Edit Site Map**.

12. Select the **New Area**.

13. Select the **Properties** tab.

14. Enter **Challenges** for **Title**.

15. Select the **New Group**.

16. Go to the Properties tab and enter **Customers** for **Title**.

17. Select the **New Subarea**.

18. Go to the **Properties** tab and select **Entity** for **Type**.

19. Select **Account** for **Entity**.

20. Click **Save**.

21. Click **Publish**.

22. Click **Save and Close**.

23. Select **Forms**.

24. Select the **Account** entity.

25. Go to the **Components** tab and uncheck the **All** checkbox.

26. Make sure the **Account** checkbox is checked.

27. Click **Save**.

28. Click **Publish**.

29. Click **Play**.

30. Click **New**.

31. Enter **New Account** for **Account Name** and click **Save**.

32. Click on the **Related** tab and select **Problems**.

33. Click **Add New Problem**.

34. Enter **New Problem** for **Name**.

35. Select **Low** for **Level** and click **Save and Close**.
