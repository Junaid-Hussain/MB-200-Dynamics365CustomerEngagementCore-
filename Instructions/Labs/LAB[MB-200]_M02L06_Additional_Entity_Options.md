---
lab:
    title: 'Lab: Additional entity options'
    module: 'Module 2: Data Model'
---

Module 2: Data Model
====================

## Lesson 6: Practice Lab – Additional entity options

Scenario
--------

You are a functional consultant for your organization Contoso. You are assigned
to work on a project for your client Fabrikam. You are working on the data model
you started in the prior practice. In this practice you are enabling some entity
options that can only be done using the classic solution explorer.

To view the data model you are building, **view  Image[MB-200]_M02L02_Creating_Entities_Fields.png in the Lab Resources**.

In this practice, you will be performing the following tasks.

1.  Enabling the Feedback option on Knowledge Assessment. This will cause the
    system to create the relationship between Knowledge Assessment and the CDM
    Feedback entity.

2.  You will enable auditing on the Knowledge Assessment entity.

3.  You will be updating the icon on the Knowledge Assessment entity, so it is
    not using the default icon.

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

4.  Navigate in the browser to the Power Platform admin portal at
    [https://admin.Powerplatform.microsoft.com].

Exercise 2 – Enable Entity Options
----------------------------------

In this exercise, you will enable the Feedback option on Knowledge Assessment as
well as enable auditing. You will then update the icon on the Knowledge
Assessment entity.

### Task 1 – Enable Feedback and Auditing Options for Knowledge Assessment

1.  Navigate to <https://make.powerapps.com/> and make sure you are in the
    **Practice** environment.

2.  Select **Solutions**.

3.  Click to open **Common Data Services Default Solution**.

4.  Click on the ellipses and select **Switch to Classic**.

5.  Expand **Entities**.

6.  Select the **Knowledge Assessment** entity.

7.  Scroll down to the to the **Communication and Collaboration** section.

8.  Select the **Feedback** checkbox. *Note:* Enabling any option with a + can not be undone, so always confirm
    before you enable any of those features that you are on the right entity and
    need the feature.

9.  Scroll down to the **Data Services** section.

10. Check the **Auditing** checkbox. *Note:* Remember auditing must be turned on at the environment settings,
    entity and field to produce any audit data. By default, fields are enabled
    for auditing.

11. Click **Save**.

12. Click **Publish all Customizations.**

