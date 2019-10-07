---
lab:
    title: 'Lab: Duplicate detection'
    module: 'Module 13: Managing Data'
---

Module 13: Managing Data
=======================

## Lesson 3: Practice Lab – Duplicate detection

Scenario
--------

You are a functional consultant working on the Fabrikam project. Your client
wants to make users aware of potential duplicates when creating contacts and you
have been tasked with implementing duplicate detection. In this practice, you
will create and modify duplicate detection rules.

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

Exercise 2 – Edit Existing Duplicate Detection Rules
----------------------------------------------------

In this exercise, you will customize an existing rule named Contacts with the
same business phone number to refine its criteria. You will also deactivate the
Accounts with the same website rule because Fabrikam found that too often they
created accounts for different locations that had the same website.

### Task 1 – Customize Duplicate Detection Rule

It is very common for multiple Contacts that have the same business phone
number, but the Contact with same business phone number duplicate detection rule
tags these Contacts as duplicates.

In this task, you will enhance the Contact with the same business phone number
rule by adding criteria to match of last name.

1.  Navigate to https://admin.powerplatform.microsoft.com

2.  Select **Environments**.

3.  Select your environment and click **Open Environment**.

4.  Navigate to **Sales -\> Data Management**.

5.  Click **Duplicate Detection Rules**.

6.  Locate and click to open the **Contact with the Same Business Phone
    Number**.

7.  Click **Unpublish**.

8.  Click **OK**.

9.  Locate the **Duplicate Detection Rule Criteria** section and click
    **Select**.

10. Locate and select **Last Name**.

11. Select **Exact Match** for **Criteria**.

12. Change the name to **Contacts with the same business phone number and last
    name**.

13. Change the Description to **Detects contact records that have the same value
    in the Business Phone field and the last name filed**.

14. Click **Save**.

15. Click **Publish**.

16. Click **OK**.

17. Click **Close**. DO NOT navigate away from this page.

### Task 2 – Unpublish Duplicate Detection Rule

It is very common for different locations of the same account to have the same
website, the Accounts with the same website rule is not useful because it will
detect these accounts as duplicates.

In this task, you unpublish the Accounts with the same website rule.

1.  Locate and click to open the **Accounts with the same Websites** rule.

2.  Click **Unpublish**.

3.  Click **OK**.

4.  Click **Save and Close**. DO NOT navigate away from this page.

Exercise 3 – Create New Duplicate Detection Rules
-------------------------------------------------

In this exercise, you will create a new duplicate detection rule that will mark
a Contact as duplicate if it has the same last name, the same first 3 letters of
the first name, and the same last 10 letters of the email.

### Task 1 – Create Duplicate Detection Rule

1.  While still on the Duplicate Detection Rules, click **New**.

2.  Enter **Contacts with the same last name, similar first name, and similar
    email** for **Name**.

3.  Select **Contact** for **Base Record Type** and **Contact** for the
    **Matching Record Type**.

4.  Click **Select**.

5.  Locate and select the **Last Name** field.

6.  Select **Exact Match** for **Criteria**.

7.  Click **Select** again.

8.  Locate and select the **First Name** field.

9.  Select **Same First Characters** for **Criteria** and enter **3** for **No.
    of Characters**.

10. Click **Select** one more time.

11. Locate and select the **Email** field.

12. Select **Same Last Characters** for **Criteria** and enter **10** for **No.
    of Characters**.

13. Click **Save**.

14. Click **Publish**.

15. Click **OK**.

16. Click **Close**.

### Task 2 – Test Duplicate Detection Rule

In this task, you will test the Contacts with the same business phone number and
last name rule.

1.  Navigate to **Sales \| Contacts**.

2.  Click **New**.

3.  Click on the **First Name** field.

4.  Enter **Joe** for **First Name**, **New** for **Last Name** and click
    **Done**.

5.  Enter **123-123-1234** for **Business Phone** and click **Save**.

6.  Click **New** again.

7.  Click on the **First Name** field.

8.  Enter **Jim** for **First Name**, **New** for **Last Name** and click
    **Done**.

9.  Enter **123-123-1234** for **Business Phone** and click **Save**.

10. The new record will be detected as a duplicate. Click **Cancel**.

11. Click on the **First Name** field again, change the **Last Name** to
    **Doe**, and click **Done**.

12. Click **Save**.

13. The record will be saved.

>   You may test the other duplicate detection rules if you like.
