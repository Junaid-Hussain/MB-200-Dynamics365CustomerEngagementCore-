---
lab:
    title: 'Lab: Set up Exchange'
    module: 'Module 11: Introduction to Integration'
---

Module 11: Introduction to Integration
=====================================

Lesson 4: Practice Lab – Set up Exchange

Scenario
--------

You are a functional consultant for your organization Contoso. You are working
on the integrations for a project for your client Fabrikam and need to set up
exchange for email integration. In this lab, you will configure server profile
settings, enable mailboxes, send a test email, and configure folder tracking.

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
might pick up where you left off and you will not need to login again.  In that
case you can skip ahead to exercise two and resume.

### Task 1 – Connect to the Power platform administration portal

1.  On Virtual machine MB200-Dynamics_Lab, sign in as Admin with the password
    Pa55w.rd if you are not already logged in.

2.  Outside the VM in the online lab interface click Files and choose D365
    Credentials. This will allocate an Office 365 tenant for you to use in these
    labs.  It will display the admin email and password for your tenant.  You
    should copy this information to notepad or similar for your reference.

3.  In MB200-Dynamics_Lab launch Microsoft Edge from the taskbar. By default,
    the browser opens Office 365. Use the O365 credentials you just acquired in
    the previous step to login.

4.  Navigate in the browser to the Power platform admin portal at
    [https://admin.Powerplatform.microsoft.com](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fadmin.Powerplatform.microsoft.com&data=02%7C01%7Cv-juya%40microsoft.com%7C4be5a28c6f1e41eefee808d687ae2dc7%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636845580068684293&sdata=cLrD%2FhTDb5sRbajtFR9RrztfyTDCo0xGS4k8FSxTaIc%3D&reserved=0)

Exercise 2 – Exchange Online Setup
----------------------------------

In this exercise, you will setup service profile, email, and folder tracking.

### Task 1 – Setup Sever Profile

In this task, you will be verifying the server profile settings and changing
other e-mail settings to turn off e-mail tracking tokens and turn on
folder-level tracking.

1.  Navigate to <https://admin.powerplatform.microsoft.com/>

2.  Select **Environments**.

3.  Select your environment and click **Settings**.

4.  Go to the **Email** section and click **Email Settings**.

5.  Make sure **Microsoft Exchange Online** is selected for **Server Profile**.

6.  Make sure **Sever -Side Synchronization or Email Router** is select for
    **Incoming Email**.

7.  Make sure **Sever -Side Synchronization or Email Router** is select for
    **Outgoing Email**.

8.  Select **Sever-Side Synchronization** for **Appointments, Contacts, and
    Tasks**.

9.  Set **People Can Send Emails** with **Unresolved Recipients** to **On**.

10. Click **Save**.

11. Go to the navigation breadcrumbs and click **Settings**.

12. Go to the **Email** section and select **Email Tracking**.

13. Set **Use Tracking Tokens** to **Off**.

14. Set **Folder-Level Tracking** to **On**.

15. Click **Save**.

16. Go to the navigation breadcrumbs and click **Settings**. DO NOT navigate
    away from this page.

### Task 2 – Setup Mailbox

In this task, you will be enabling e-mail for both your admin user and the test
user.

1.  Go to the **Email** section and select **Mailboxes**.

2.  Change the view to **All Mailboxes**.

3.  Double click to open the admin mailbox.

4.  Select **Server-Side Synchronization** for **Appointments, Contacts, and
    Tasks**.

5.  Click **Save**.

6.  Click **Approve Email.**

7.  Click **OK**.

8.  Click **Test & Enable Mailbox**.

9.  Click **OK**.

10. Refresh the page until the test succeeds.

11. Close the mailbox.

12. Double click to open the **Test User** mailbox.

13. Make note of the Test User’s e-mail address you will need it in the next
    task

14. Select **Server-Side Synchronization** for **Appointments, Contacts, and
    Tasks**.

15. Click **Save**.

16. Click **Approve Email.**

17. Click **OK**.

18. Click **Test & Enable Mailbox**.

19. Click **OK**.

20. Refresh the page until the test succeeds.

21. Close the mailbox.

### Task 3 – Send Test Email from Dynamics 365

In this task, now that e-mail has been configured, we will send a test e-mail.

1.  Navigate to <https://web.powerapps.com>

2.  Select **Apps**

3.  Select **Sales Hub**

4.  In the upper right corner click the + to show **Quick Create** entity list

5.  Select **Activities -\> Email**

6.  Input the **Test Users** e-mail in the **To**, a subject and a description
    of your choice and click **Send**

7.  From your own personal e-mail, also send an e-mail to Test User with a
    subject Request for Quote

### Task 4 – Check e-mail received and setup folder for tracking

In this task, now that e-mail has been configured, we will send a test e-mail

1.  Keeping your current browser window, open a new one using the in-private
    option. This will allow you to have both admin and test users logged in. If
    you are not familiar with how to launch an InPrivate session review
    <https://support.microsoft.com/en-us/help/4026200/microsoft-edge-browse-inprivate>

2.  Navigate to https://outlook.office365.com/

3.  Login with the **Test User**.

4.  Select your **Time Zone** and click **Save**.

5.  You should see your two e-mails

6.  Click **More**.

7.  Right click on the **Inbox** and select **Create New Subfolder**.

8.  Enter **Contoso** and \<ENTER\>

9.  Hover over the **Contoso** folder and click **Add to Favorites**.

### Task 5 – Configure Folder Tracking

In this task, you will configure the folder tracking rule.

1.  Still logged in with the test user, open a new tab and Navigate to
    https://web.powerapps.com

2.  Select **Apps**

3.  Select **Sales Hub**.

4.  Navigate to **Accounts**.

5.  Click **+ New**.

6.  Enter **Contoso Inc.** for **Account Name** and click **Save**.

7.  Click the “Gear icon” in the upper right corner and select **Personalization
    Settings**.

8.  Select the **Email** tab.

9.  Click **Configure Folder Tracking Rules.**

10. Click **+ New Folder Mapping**.

11. Select **Contoso** for **Exchange Folder**, select **Contoso Inc.** for
    **Regarding Record in Dynamics 365** and click **Save**.

12. Close the **Folder-Level Tracking** popup.

13. Click **OK**.

14. Go to the **Outlook** browser tab.

15. Drag the **Test Email** from the **Inbox** to the **Contoso** folder.

16. Go back to your **Dynamics 365**.

17. Go to the **Timeline** section and make sure the Email was tracked against
    the **Contoso Inc.** record. **Note:** You may have to refresh the browser
    if you were still on the Contoso record.
