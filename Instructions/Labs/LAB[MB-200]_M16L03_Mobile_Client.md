---
lab:
    title: 'Lab: Install the mobile client'
    module: 'Module 16: Additional Considerations'
---

Module 16: Additional Considerations
===================================
## Practice Lab – Install the mobile client

Scenario
--------

As a functional consultant at Contoso, you’ve been asked to help create an app
that tracks customers current problems. In these practices on solutions, you
will create a solution to track all your components, export and import into
production, and then go through a maintenance cycle using patches to update the
deployed solution. In this practice, you will be doing the following:

-   Install the mobile application

-   Practice navigating within the application

-   Qualify a lead and close an opportunity

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

Exercise 2 – Install Dynamics 365 for Mobile
--------------------------------------------

In this exercise, you will install the Dynamics 365 for Mobile application and
use it.

### Task 1 – Install Application 

In this task, you go to your app store and install the Dynamics 365 for Mobile
application and use it.

1.  Go to the app store of your mobile platform.

2.  Search for **Dynamics 365**.

3.  Locate and select **Microsoft Dynamics 365**.

4.  Click **Install**.

5.  Wait for the installation to complete and **Launch** the application.

6.  Provide your Microsoft Dynamics 365 URL
    [https://[YourOrg].crm.dynamics.com/](https://[YourOrg].crm.dynamics.com/)

7.  Provide your login information and sign in.

8.  You will be presented with a list of published apps.

9.  Locate and click on the **Sales Hub** application.

10. The **Sales Activity Social Dashboard** will load.

### Task 2 – Navigation

1.  Click on the menu button and select **Opportunities**.

2.  Click on the … icon and then click the **Select** button.

3.  Check the checkbox of a few records.

4.  Click on the **Select** button again. The checkboxes will disappear.

5.  Click on the … button and then click **Sort**.

6.  Select **Est. Revenue**. The view will be sorted accordingly.

7.  Click on the … button and then click **Show Chart**.

8.  The **Top Customers** chart will load.

9.  Click on the **Top Customers**. Available charts for the Opportunity will be
    listed here.

10. Scroll to and select the **Opportunity by Pipeline Phase** chart.

11. Click **Expand Chart**. An expanded view of the chart will load.

12. Click **Close**.

13. Click on the … button and then click the **Hide Chart** button.

14. Click **Select** again.

15. Check the checkbox of one record.

16. Click on the **…** button again and see what actions you can take when you
    have a record selected.

17. Click on the **Home** button.

18. Click on the **Search** button.

19. Search for **Jim**.

20. The result should return one **Contact** and one **Opportunity**. You may
    have to scroll to the right to see the second record.

21. Click on the **Filter With** dropdown and select **Opportunity**.

22. Click on the back button.

### Task 3 – Lead to Close

In this task, you will create a lead, qualify it, and process the opportunity that will be created for the lead. 
-----------------------------------------------------------------------------------------------------------------

1.  Click on the navigation button and select **Leads**.

2.  Click on the … button and click **+ New**

3.  Enter **Mobile Test** for **Topic**, enter **Jane** for **First Name**,
    **Doe** for **Last Name**, and click **Save**.

4.  Click on the … button and select **Qualify**.

5.  An **Opportunity** and a **Contact** will be created from the **Lead**.

6.  Go to the **Business Process Flow** and click on the arrow button to move to
    the right. **The Business Process** Flow will advance to the next stage of
    the **Opportunity**.

7.  Click on the **Develop** stage, click the checkbox **Identify Stakeholders**
    and **Identify Competitors** to mark the steps complete.

8.  Click **Next Stage**.

9.  The **Business Process Flow** will advance to the **Propose** stage.

10. Click on the Propose stage and mark all of the steps complete.

11. Click **Next Stage**.

12. The **Business Process Flow** will advance to the **Close** stage.

13. Click on the **Close Stage** and mark all the steps complete.

14. Click **Finish**.

15. Click on the **Close as Won** button located on the command bar.

16. Enter **200,000** for **Actual Revenue** and click **OK**.

17. The **Opportunity** will close.
