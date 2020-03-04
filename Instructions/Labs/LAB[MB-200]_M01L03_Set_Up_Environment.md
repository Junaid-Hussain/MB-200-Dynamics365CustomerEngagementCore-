---
lab:
    title: 'Lab: Set up environment'
    module: 'Module 1: Power Platform Overview'
---

Module 1: Power Platform Overview
=================================
## Important notice re: tenants - temporary workaround

As of January 23, 2020, WWL is unable to provide students with pre-provisioned Dynamics 365 access, and is working on a solution that should be available in the next 4-6 weeks. As a workaround, we are recommending using Dynamics 365 Trial accounts. Each student will be responsible for requesting these. To help students in getting the Dynamics 365 tenants (including Marketing), M365 tenants will be provided through the Authorized Lab Hosters. This is a short-term solution and we will keep all stakeholders including Learning Partners and MCTs updated as progress is made and advise as a more permanent solution timeline for pre-provisioning Dynamics 365 access for lab use is established. Please work with your Authorized Lab Hoster for provisioning of the M365 Tenants for the students and follow the instructions below to use the M365 tenant to secure a Dynamics 365 trial for your appropriate application.
 
1. Using your provided M365 credentials, log into https://admin.microsoft.com/ and accept the terms.
2. Once you’ve logged in successfully, access https://trials.dynamics.com/. Select the applicable application for your course.
3. Under “Work email,” enter the email address from the M365 credentials. Under “phone number,” enter your own phone number.
4. Select Get Started.
5. You will be prompted to enter your password for the on.microsoft.com account. Enter the password provided for the M365 tenant.
6. If you are prompted to accept terms and conditions, accept them. Your environment may take a few minutes to provision.

## Practice Lab – Set up environment

Scenario
--------

You are a functional consultant for your organization Contoso. You have been
asked to prepare an environment for a proof of concept your company is building
for Fabrikam. You will be preparing two environments; one that has only Common
Data Model core entities and another that has the Dynamics 365 for Sales
application installed.

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

Exercise 2 – Configure a Dynamics 365 Application
-------------------------------------------------

In this exercise, you will be making another new environment, one that has the
Dynamics 365 for Sales app installed.

### Task 1 – Create a Dynamics 365 environment

1.  Go back to <https://admin.Powerplatform.microsoft.com>

2.  Expand **Admin Centers** and select **Dynamics 365**.

3.  Select **Instance to Configure** from the list and click **Configure.**

4.  Select only the **Sales app** in the "Choose which applications you want to preinstall" section.

5.  Enter **SalesPractice** for URL if available (or enter a different URL).

6.  Click **Configure**.  

It will take few minutes to create the environment. You may proceed to exercise four while the environment is being created.

Exercise 3 – Review Settings and Configure
------------------------------------------

In this exercise, you will be reviewing settings, enabling an additional
currency, and enabling auditing.

### Task 1 – Explore the settings

1.  Go back to <https://admin.Powerplatform.microsoft.com> and select
    **Environments**.

2.  Select the **Contoso** environment (that does not say **(Default)**) by clicking on its name when it is
    underlined and click **Settings** in the upper right-hand corner. T

3.  Explore the different areas in **Settings** that you are interested in but
    **do not make any changes.**

### Task 2 – Enable an additional currency

1.  Locate the **Business** section of the **Settings** and click
    **Currencies**.

2.  Click **New**.

3.  Click on the **Currency Code** lookup.

4.  Select **Germany Euro** and click **Add**.

5.  Enter **0.88** for **Currency Conversion** and click **Save and Close**.

6.  You should see both **USD** and **EUR** listed in your **Currencies**.

7.  Close the currencies tab. Do not close the Settings tab.

### Task 3 – Enable auditing 

1.  Locate the **Product** section of the **Settings** and click **Features**.

2.  Locate the **Auditing** section and turn on **Start Auditing.**

3.  Click **Save** in the lower left corner. You may have to scroll to see it.


Exercise 4 – Explore the environments
-------------------------------------

In this exercise, you will be exploring the environments you created and explore
them.

### Task 1 – Explore the Practice environment

1.  Navigate to <https://make.powerapps.com/>

2.  Select **Apps**.

3.  You should see the sample applications.

4.  Click the **Asset Checkout** sample application.

5.  The **Asset Checkout** application will load.

6.  Explore and familiarize yourself with the application.

### Task 2 – Explore the Dynamics 365 environment

1.  Go back to <https://make.powerapps.com/>

2.  Change your environemnt to the Sales environment.

3.  Select **Apps.**

4.  Click on the **Sales Hub** application.

5. In the upper right corner, select the **Gear Icon** and choose **Advanced Settings.**

6.  Navigate to **Settings | Data Management.**

7.  Click **Sample Data**.

8.  You can confirm that sample data is already installed if you have the option
    to **Remove Sample Data.** If sample data is not installed, click **Install Sample Data**.

9.  If installing, wait for the installation to start and click **Close**.

10.  Close the **Advanced Settings** tab.

11.  Return to the tab with the **Sales Hub** application and refresh your browser.

12. Click on **Accounts** in the left navigation. If you don't see data, wait for a short time and refresh again. The sample data install can sometimes take a few minutes.

13. Explore and familiarize yourself with the application. 
