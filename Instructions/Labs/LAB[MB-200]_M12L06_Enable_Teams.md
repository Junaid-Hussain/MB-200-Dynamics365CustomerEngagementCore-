---
lab:
    title: 'Lab: Enable Teams'
    module: 'Module 12: Integration with Office'
---

Module 12: Integration with Office
=================================

## Lesson 6: Practice Lab - Enable Teams

Scenario
--------

As a functional consultant at Contoso, you are tasked with configuring Teams
integration for your client Fabrikam to empower collaboration across the
company. In this lab, you will enable Teams integration and add Teams tab to the
canvas app. Next you will add a Dynamics 365 collaboration tab and with a chat
bot.

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

Exercise 2 – Integrating with Teams
-----------------------------------

### Task 1 – Enable Teams Preview

In this task, you will enable the preview of Microsoft Teams integration in your
environment. When this feature fully releases this task will no longer be
necessary.

1.  Navigate to <https://web.powerapps.com/> and make sure you are not in the
    default environment.

2.  Select **Apps**.

3.  Locate the **Sales** application and click on it.

4.  Navigate to **Settings** and select **Administration**.

5.  Select **System Settings**.

6.  Select the **Preview** tab.

7.  Check the **License Terms** checkbox.

8.  Go to the Microsoft Teams Integration Preview section and select **Yes**.

9.  Click **OK** and wait for it to complete.

10. Click **Finish**.

11. Click **OK**.

12. Close the **Sales** application.

### Task 2 – Add Teams Tab to Canvas App

In this task, you are going to add a tab that embeds a PowerApps Canvas app. You
will be hosting the Fabrikam Assessment canvas app on a tab.

1.  Navigate to https://teams.microsoft.com/

2.  Select **Teams**.

3.  Click **Create Team**.

4.  Enter **Fab Assessment** for **Team Name**, select **Private** for
    **Privacy** and click **Next**.

5.  Click **Skip**.

6.  Click **+ Add a Tab**.

7.  Search for **PowerApps** and select it.

8.  Click **Install**.

9.  Select the **Fabrikam Assessment** application and click **Save**.

10. The app should load in the tab.

11. Select **Conversations** tab.

12. Conversation will get started.

### Task 3 – Add Dynamics 365 Collaboration Tab

In this task, you will be adding a tab to show a CDS Account record and allow
interaction using the Sales Hub model-driven app.

1.  Click **+ Add a Tab**.

2.  Search for **Dynamics 365** and select it.

3.  Click **Install**.

4.  Select your **Dynamics 365 Sales** environment application.

5.  Select **Sales Hub** for Application.

6.  Click **Select**.

7.  Search for **Adventure Works** and select **Adventure Works** and click
    **Save**.

8.  Wait for the tab to load.

9.  The **Adventure Works** tab should load.

10. Select the **Conversations** tab.

11. A new conversation for **Adventure Works** should start.

### Task 4 – Chat with Dynamics 365 Bot

In this task, you will be chatting with the bot to find out what opportunity
records you have and update them using the bot.

1.  On the left navigation, select **Chat**.

2.  Click on the **New Chat** button.

3.  Type **Dynamics 365** on the **To** field and select **Dynamics 365**.

4.  The **Sales Bot** should great you.

5.  If the **Sales Bot** hasn't said Hi, type **Hello** and **Send**.

6.  After the **Sales Bot** responds click **Configure**.

7.  Select your **Organization** and click **Next**.

8.  Read the TOS and click Accept if you agree.

9.  Type **What are my opportunities** and click **Send**.

10. The **Bot** should list your opportunities.

11. Click on one of the opportunities.

12. The **Bot** will open the selected opportunity.

13. Click **Update Amount**.

14. Change the **Amount** and click **Save**.

15. The **Bot** should update the opportunity.

16. Click **Create a Post**.

17. Type **Budget amount was increased** and click **Save**. Make a note of the
    opportunity topic.

18. Click the Open Record button, it should open the **Sales Hub** model-driven
    app.

19. Locate the **Budget Amount** field and make sure it was updated.

20. Go to the **Timeline** section and make sure your post is posted.
