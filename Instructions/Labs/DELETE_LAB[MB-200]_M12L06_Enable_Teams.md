---
lab:
    title: 'Lab: Enable Teams'
    module: 'Module 12: Integration with Office'
---

Module 12: Integration with Office
=================================

## Lesson 6: Practice Lab - Enable Teams

Scenario
--------

As a functional consultant at Contoso, you are tasked with configuring Teams
integration for your client Fabrikam to empower collaboration across the
company. In this lab, you will enable Teams integration and add Teams tab to the
canvas app. Next you will add a Dynamics 365 collaboration tab and with a chat
bot.

Exercise 2 – Integrating with Teams
-----------------------------------

### Task 1 – Enable Teams Preview

In this task, you will enable the preview of Microsoft Teams integration in your
environment. When this feature fully releases this task will no longer be
necessary.

1.  Navigate to <https://make.powerapps.com/>. Switch to the **Contoso** environment if you are not already in it.

2.  Select **Apps**.

3.  Locate the **Sales Hub** application and click on it.

4.  Use the site map to switch to **App Settings.**

5.  From **General settings,** select **Chat and collaborate.**

6.  Change the toggle to **Yes** and click Save.

7. Wait until you get a message saying that the update was successful. Close the **Sales** application.

### Task 2 – Add Teams Tab to Canvas App

In this task, you are going to add a tab that embeds a PowerApps Canvas app. You
will be hosting the Fabrikam Assessment canvas app on a tab.

1.  Navigate to https://teams.microsoft.com/

2.  Select **Teams**.

3.  Click **Create Team**.

4.  Enter **Fab Assessment** for **Team Name**, select **Private** for
    **Privacy** and click **Next**.

5.  Click **Skip**.

6.  Click **+ Add a Tab**.

7.  Search for **PowerApps** and select it.

8.  Click **Install**.

9.  Select the **Fabrikam Assessment** application and click **Save**.

10. The app should load in the tab.

11. Select **Conversations** tab.

12. Conversation will get started.

### Task 3 – Add Dynamics 365 Collaboration Tab

In this task, you will be adding a tab to show a CDS Account record and allow
interaction using the Sales Hub model-driven app.

1.  Click **+ Add a Tab**.

2.  Search for **Dynamics 365** and select it.

3.  Click **Install**.

4.  Select your **Dynamics 365 Sales** environment application.

5.  Select **Sales Hub** for Application.

6.  Click **Select**.

7.  Search for **Adventure Works** and select **Adventure Works** and click
    **Save**.

8.  Wait for the tab to load.

9.  The **Adventure Works** tab should load.

10. Select the **Conversations** tab.

11. A new conversation for **Adventure Works** should start.

### Task 4 – Chat with Dynamics 365 Bot

In this task, you will be chatting with the bot to find out what opportunity
records you have and update them using the bot.

1.  On the left navigation, select **Chat**.

2.  Click on the **New Chat** button.

3.  Type **Dynamics 365** on the **To** field and select **Dynamics 365**.

4.  The **Sales Bot** should great you.

5.  If the **Sales Bot** hasn't said Hi, type **Hello** and **Send**.

6.  After the **Sales Bot** responds click **Configure**.

7.  Select your **Organization** and click **Next**.

8.  Read the TOS and click Accept if you agree.

9.  Type **What are my opportunities** and click **Send**.

10. The **Bot** should list your opportunities.

11. Click on one of the opportunities.

12. The **Bot** will open the selected opportunity.

13. Click **Update Amount**.

14. Change the **Amount** and click **Save**.

15. The **Bot** should update the opportunity.

16. Click **Create a Post**.

17. Type **Budget amount was increased** and click **Save**. Make a note of the
    opportunity topic.

18. Click the Open Record button, it should open the **Sales Hub** model-driven
    app.

19. Locate the **Budget Amount** field and make sure it was updated.

20. Go to the **Timeline** section and make sure your post is posted.
