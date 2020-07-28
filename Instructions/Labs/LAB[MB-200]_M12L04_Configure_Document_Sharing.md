---
lab:
    title: 'Lab: Configure document sharing'
    module: 'Module 12: Integration with Office'
---

Module 12: Integration with Office
=================================

## Lesson 4: Practice Lab – Configure document sharing

Scenario
--------

You are a functional consultant for your organization Contoso. You are working
on the integrations for a project for your client Fabrikam and need to set up
the SharePoint integration. In this lab, you will enable SharePoint document
management, upload a document and set alerts.

Exercise 2 – Save Documents to SharePoint
-----------------------------------------

In this exercise, you will configure SharePoint integration to allow uploading
and viewing documents related to an entity. In this example, you will be
uploading the certificates you created in the Microsoft Word document generation
and associating them with the Knowledge Assessment entity record.

### Task 1 – Enable SharePoint Document Management

In this task, you will configure document management for the Knowledge
Assessment entity

1.  Navigate to <https://make.powerapps.com.

2.  Ensure that you are in your **Practice** environment.

3. Select **Solutions.**

5.  Select **Common Data Services Default Solution**.

7.  Locate and select the **Knowledge Assessment** entity.

8.  Click **Settings** from the command bar. Expand **Collaboration** and hit the checkmark next to **Enable SharePoint document management.**

9.  Click **Done.**

10. Save the entity. Return to the **Common Data Services Default Solution** and click **Publish all customizations.**

11. Click the dots next to **Publish all customizations**.

12. Navigate to admin.powerplatform.com. Select your **[my prefix] Practice** environment from the list. Select **Settings** from the command bar.

13. From the **Integration** section, select **Document management settings.** Click **SharePoint Sites**.

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
