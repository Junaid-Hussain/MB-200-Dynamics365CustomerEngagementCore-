---
lab:
    title: 'Lab: Set up environment'
    module: 'Module 1: Power Platform Overview'
---

Module 1: Power Platform Overview
=================================

## Practice Lab – Set up environment

Scenario
--------

You are a functional consultant for your organization Contoso. You have been
asked to prepare an environment for a proof of concept your company is building
for Fabrikam. 

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
might pick up where you left off and you will not need to log in again.  In that
case you can skip ahead to exercise two and resume.

### Task 1 – Connect to the Power Platform administration portal

1.  On Virtual machine MB200-Dynamics_Lab, sign in as Admin with the password
    Pa55w.rd if you are not already logged in.

2.  Outside the VM in the online lab interface click Files and choose D365
    Credentials. This will allocate an Office 365 tenant for you to use in these
    labs.  It will display the admin email and password for your tenant.  You
    should copy this information to notepad or similar for your reference.

3.  In MB200-Dynamics_Lab launch Microsoft Edge from the taskbar. By default,
    the browser opens Office 365. Use the D365 credentials you just acquired in
    the previous step to login.

4.  Navigate in the browser to the Power Platform admin portal at
    [https://admin.Powerplatform.microsoft.com](https://admin.Powerplatform.microsoft.com).


Exercise 2 – Review Settings and Configure
------------------------------------------

In this exercise, you will be reviewing settings, enabling an additional
currency, and enabling auditing.

### Task 1 – Explore the settings

1.  Go back to <https://admin.Powerplatform.microsoft.com> and select
    **Environments**.

2.  Select your **Practice** environment. Click on the ellipses next to its name to expand the drop down menu and select **Settings.** 

3.  Explore the different areas in **Settings** that you are interested in but
    **do not make any changes yet.**

### Task 2 – Enable an additional currency

1.  Locate the **Business** section of the **Settings** and click
    **Currencies**.

2.  Click **New**.

3.  Click on the **Currency Code** lookup.

4.  Select **New Zealand tara** and click **Add**.

5.  Enter **0.61** for **Currency Conversion** and click **Save and Close**.

6.  You should now see **NZD** listed in your **Currencies**.

7.  Close the currencies tab. Do not close the Settings tab.

### Task 3 – Enable auditing 

1.  Locate the **Audit and logs** section of the **Settings** and click **Audit settings**.

2.  Locate the **Start Auditing** field and check the box.

3.  Click **OK** in the lower right corner. Close the tab.
