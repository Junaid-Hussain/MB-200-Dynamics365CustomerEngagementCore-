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

**Important Note:** This lab will provide you with an actual Dynamics 365 tenant
and licenses for the Power Platform applications you will be using in this
course. Please be aware that the Power Platform is evolving all the time. The
instructions in this document may be different from what you experience in your
actual tenant. It is also possible to experience a delay of several
minutes before the virtual machine has network connectivity to begin the labs.


Exercise 1 – Review Settings and Configure
------------------------------------------

In this exercise, you will be reviewing settings, enabling an additional
currency, and enabling auditing.

### Task 1 – Explore the settings

1.  Go back to <https://admin.Powerplatform.microsoft.com> and log in with your user credentials.

2. Select **Environments** and click **+New.**

    - For **Name**, enter **[my initials] Practice.** (Example: AJ Practice.)
    
    - For **Type**, select **Trial.**
    
    - Change the toggle on **Create a database for this environment?** to **Yes.**
    
    - Leave all other selections as default and click **Next.**
    
    - On the next tab, leave all selections to default and click **Save** again.
    

3. Your **Practice** environment should now show in the list of Environments. You may also see other students' environments in this list with their individual prefixes; only work within your Practice environment.

4. Your environment may take a few minutes to provision. Refresh the page if needed. When your environemnt is prepared, select your **Practice** environment by clicking on the ellipses next to its name to expand the drop down menu and select **Settings.** 

3.  Explore the different areas in **Settings** that you are interested in but do not make any changes yet. 

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

3.  Click **Save** in the lower right corner. Close the tab.
