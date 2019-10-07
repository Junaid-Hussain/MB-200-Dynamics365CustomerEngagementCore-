Module 12: Integration with Office
=================================

## Lesson 4: Practice Lab – Configure document sharing

Scenario
--------

You are a functional consultant for your organization Contoso. You are working
on the integrations for a project for your client Fabrikam and need to set up
the SharePoint integration. In this lab, you will enable SharePoint document
management, upload a document and set alerts.

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

Exercise 2 – Save Documents to SharePoint
-----------------------------------------

In this exercise, you will configure SharePoint integration to allow uploading
and viewing documents related to an entity. In this example, you will be
uploading the certificates you created in the Microsoft Word document generation
and associating them with the Knowledge Assessment entity record.

### Task 1 – Enable SharePoint Document Management

In this task, you will configure document management for the Knowledge
Assessment entity

1.  Navigate to <https://admin.powerplatform.microsoft.com/>

2.  Select **Environments.**

3.  Select … **Open Environment.**

4.  Navigate to **Settings-\>Solutions.**

5.  Select **Knowledge Assessment Solution**.

6.  Expand **Entities**.

7.  Locate and select **Knowledge Assessment** entity.

8.  Check the **Document Management** option on the entity properties.

9.  Click **Save**.

10. Click **Publish**.

11. Close the solution explorer.

12. Navigate to **Settings -\> Document Management**.

13. Click **SharePoint Sites**.

14. Flow the wizard and click **Finish**.

15. Select **Document Management Settings**.

16. Review the currently selected entities.

17. Locate **Knowledge Assessment** and select it.

18. Click **Next**.

19. We are not going to configure it based on a single entity, click **Next**.

20. Click **OK** to continue creation of Document Libraries.

21. When Status are either **Succeeded** or Already exists click the **Finish**
    button.

### Task 2 – Upload a document

In this task, you will upload a document related to a Knowledge Assessment
entity

1.  Navigate to <https://web.powerapps.com/>

2.  Confirm that the environment selector in the upper right corner is NOT in
    the default environment. You should see an environment name like
    Contoso(crm\*\*\*) and not Contoso(Default).

3.  Select **Apps**.

4.  Locate the **Knowledge Admin** Model-Driven application and click to open.

5.  Click on the **Site Map** button and select **Assessment**.

6.  Open one of the assessment records.

7.  Select the **Related** tab.

8.  Select **Documents**

9.  Click **Upload**

10. Upload a test document either Microsoft Word or Microsoft Excel. You could
    upload the documents you generated in the previous practice.

### Task 3 – Work with the uploaded document

In this task, you can see some of the options on an uploaded document

1.  Click on the document you just uploaded – if it is Microsoft Word or
    Microsoft Excel it should launch in the online version of the tools.

2.  On the left side of the document list, check the row on the document you
    just uploaded.

3.  Notice the command bar options change – You can Edit, Delete, Check Out,
    Check In, Edit Properties, Discard Checkout and Open Location.

4.  Click the **Check Out** – This reserves the document for you.

5.  Select the document again and click **Edit**, make a couple of minor changes
    and close the tab.

6.  Click **Check In.**

7.  Select **No** to retain your check in and click **OK**.

### Task 4 – Set Alerts

In this task, you set an alert for the Documents folder and test the alerts.

1.  Click the **Open Location** button – this will open the SharePoint document
    library. From here you can perform any of the other SharePoint commands that
    aren’t exposed in the model-driven app.

2.  Select the document you uploaded

3.  Click on the … button and select **Alert Me.**

4.  Click **OK**.

5.  Close all the **SharePoint** browser tabs.

6.  Back in the **Knowledge Management** app.

7.  Edit the document, make a change.

8.  If you check Outlook.Office365.com you should have an alert notification.
