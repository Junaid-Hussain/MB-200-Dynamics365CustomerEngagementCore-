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

Exercise 1 – Exchange Online Setup
----------------------------------

In this exercise, you will setup service profile, email, and folder tracking.

### Task 1 – Setup Sever Profile

In this task, you will be verifying the server profile settings and changing
other e-mail settings to turn off e-mail tracking tokens and turn on
folder-level tracking.

1.  Navigate to https://admin.powerplatform.microsoft.com/.

2.  Select **Environments**.

3.  Select **your** environment, [your alias] Practice, and click **Settings**.

4.  Expand the **Email** section and click **Email Settings**.

5.  Make sure **Microsoft Exchange Online** is selected for **Server Profile**.

6.  Make sure **Sever-Side Synchronization or Email Router** is selected for
    **Incoming Email**.

7.  Make sure **Sever-Side Synchronization or Email Router** is select for
    **Outgoing Email**.

8.  Select **Sever-Side Synchronization** for **Appointments, Contacts, and
    Tasks**.

9.  Set **People Can Send Emails** with **Unresolved Recipients** to **On**.

10. Click **Save**.

11. Go to the navigation menu and click **Settings**.

12. Expand the **Email** section and select **Email Tracking**.

13. Set **Use Tracking Tokens** to **Off**.

14. Set **Folder-Level Tracking** to **On**.

15. Click **Save**.

16. Go to the navigation menu and click **Settings**. DO NOT navigate
    away from this page.

### Task 2 – Setup Mailbox

In this task, you will be enabling e-mail for your user.

1.  Go to the **Email** section and select **Mailboxes**.

12. Double click to open your user record. (It should be the only one in the view.) 

13. Make note of your user's email address.

14. Select **Server-Side Synchronization** for **Appointments, Contacts, and
    Tasks**.

15. Click **Save**.

16. Click **Actions > Approve Email.**

17. Click **OK**.

18. Click **Test & Enable Mailbox**.

19. Click **OK**.

20. Refresh the page until the test succeeds. Select the **Alerts** tab to read through the alerts.

21. Close the mailbox.
