---
lab:
    title: 'Lab: Build a World template'
    module: 'Module 12: Integration with Office'
---

Module 12: Integration with Office
=================================

## Lesson 2: Practice Lab – Build a Word template

Scenario
--------

You are a functional consultant for Contoso building a knowledge assessment
application for you client Fabrikam. You need to configure a template so that
managers can easily generate a certificate of completion to give users after
achieving a passing score. In this lab, you will create a certificate of
completion through a Word template and update that Word template to the app.

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

Exercise 2 – Word Template
--------------------------

In this exercise, you create a Microsoft Word template for the Test Result
entity, this document will generate certificate of completion.

### Task 1 – Create Knowledge Test Result

In this task, you will create a Knowledge Test Result record

1.  Navigate to <https://web.powerapps.com/environments>

2.  Using the Environment selector in the upper right make sure you are NOT in
    the Default environment. You should be set to something like
    Contoso(crm\*\*\*) and not Contoso (Default).

3.  Select **Apps**.

4.  Locate and click on the **Knowledge Admin** application.

5.  Click on the **Site Map** button and select **Knowledge Test Results**.

6.  Click **New**.

7.  Enter **Result for Template** for Primary Name.

8.  Click on the **Knowledge Assessment** lookup field and select any record.

9.  Enter **960** for **Total Points** and click **Save**. DO NOT navigate away
    from this page.

### Task 2 – Create Template

In this task, you will create the template. You will do this by downloading the
starting template for the entity. You will also enable to Developer menu in
Microsoft Word.

1.  Click on the **Word Template** button locate on the command bar and select
    **Download Template**.

2.  Make sure **Knowledge Test Result** is selected for Entity.

3.  Go to the N:1 Relationship dropdown and click on chevron button.

4.  Select **Knowledge Assessment** and **User
    (user_crxxx_knowledgetestresult)** where xxx will be some numbers.

5.  Click **Download**.

6.  Wait for the template to be downloaded and click then click **Open**.

7.  Click **Enable Editing**.

8.  Click **File** and select **Options**.

9.  Select **Customize Ribbon**.

10. In the **Main Tabs** section locate and check the **Developer** checkbox.

11. Click **OK**.

12. Select the **Developer** tab and click XML Mapping Pane.

13. Click on the **Custom XML Parts** dropdown and select the **URL** with the
    Word **Template** and the entity name in it.

14. You are now ready to build the template.

### Task 3 – Build Template

In this task, you will build a basic certificate and insert data from CDS.

1.  Select the **Layout** tab, click **Orientation** and select **Landscape**.

2.  Click **Margins** and select **Normal 1” 1” 1” 1”.**

3.  Select the **Insert** tab, click **Text Box** and select **Simple Text Box**

4.  Select the **Format** tab, click **Shape Fill** and select **No Fill**.

5.  Click **Shape Outline** and select **No Outline**.

6.  Select the **Home** tab and select **Align Center.**

7.  Replace the placeholder text with **Certificate of Completion**.

8.  Select the text and select **Old English Text MT** for **Font**.

9.  Change the **Font Size** to **72**

10. Resize the **Textbox** to fill the page horizontally.

11. Select the **Format** tab, click **Text Effect**, click **Transform**, and
    select **Arch**.

12. Select the **Insert** tab, click **Text Box** and select **Simple Text
    Box**.

13. Select the **Format** tab, click **Shape Fill** and select **No Fill**.

14. Click **Shape Outline** and select **No Outline**.

15. Select the **Home** tab and select **Align Center.**

16. Replace the with **This certificate was presented to:**

17. Select the text and change the **Font Size** to **18**.

18. Place your cursor at the end of the text and press the **\<Enter \>** key.

19. Go to the **XML Mapping** pane and expand the entity.

20. Expand the **User** entity.

21. Locate the **fullname** field and right click on it.

22. Click **Insert Content Control** and select **Plain Text**.

23. Select the text of the control and change the **Font** to **Castellar**.

24. Change the **Font Size** to **24**.

25. Insert another **Simple Text Box** and place it below the **Full Name**.

26. Set the **Fill** of the new textbox to **No Fill**.

27. Set the **Outline** of the new textbox to **No Outline**.

28. Set the alignment of the new textbox **Align Center**.

29. Replace the text of the new textbox with **For completing the**

30. Go to the **XML Mapping** pane and expand the **Knowledge Assessment**
    entity.

31. Right click on the **Title** field, click **Insert Content Control**, and
    select **Plain Text.**

32. Place your cursor in front of the **Title** control and type **with** .

33. Go to the **XML Mapping** pane and go to the **Knowledge Test Result**
    entity.

34. Right click on the **Total Points** field, click **Insert Content Control**,
    and select **Plain Text.**

35. Place your cursor in front of the **Total Points** control and type **total
    points** .

36. Press the **\<Enter\>** key.

37. Type **Completion Date:** and press the \<Enter\> key.

38. Go to the **XML Mapping** pane and go to the **Knowledge Test Result**
    entity.

39. Right click on the **Created-On** field, click **Insert Content Control**,
    and select **Plain Text.**

40. Select the **Insert** tab and click **Picture**.

41. Locate and select the **Badge.png** file located in the resources folder.

42. Place the image below the **Created-On** control and center it.

43. Click **File** and click **Save**.

44. Enter **Assessment Certificate** for name and click **Save**. remember where
    you are saving your template.

Exercise 3 – Uploading and Using Word Template
----------------------------------------------

In this exercise, you will upload the template you created and test it.

### Task 1 – Upload Template

In this task, you will upload the template you created

1.  Go to your **Knowledge Admin** Model-Driven application.

2.  Click on the **Site Map** button and select **Knowledge Test Results**.

3.  Open the **Knowledge Test Result** record you created.

4.  Click on the **Word Template** button located on the command bar and select
    **Upload Template**.

5.  Click **Browse**.

6.  Select the template you created and click **Open**.

7.  Click **Upload**.

### Task 2 – Use Word Template

In this task, you will test the template you created

1.  Click on the **Word Template** button located on the command bar and select
    the **Assessment Certificate** template you uploaded.

2.  Click Open.

3.  Your certificate will open. Make sure the certificate looks like the image
    in Lab Resources labeled **IMAGE[MB-200]_M12L02_Build_Word_Template.png.**
