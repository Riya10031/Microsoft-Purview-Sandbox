# Lab 09 - Investigation of  Data Loss Prevention Alerts 

## Lab Overview
The main goal of the investigation stage is for the assigned owner to correlate evidence, determine the cause and full impact of the alert and decide on a remediation plan. The assigned owner is responsible for deeper investigation and remediation of the alert. The primary alert investigation tools are the Microsoft 365 Defender portal and the DLP alert management dashboard. You might also use Activity explorer to investigate alerts. You can also share alerts with other users in your organization.

## Lab scenario

In this lab the task involves navigating to the Microsoft Purview portal, specifically the DLP section, and exploring the generated alerts. The goal is to provide insights into investigating DLP alerts, understanding the available information, and utilizing tools like the DLP alert management dashboard and Activity Explorer for a comprehensive analysis.

## Lab objectives

In this lab, you will complete the following tasks:

+ Task 1 : Investigation of  Data Loss Prevention Alerts

## Estimated timing: 60 minutes

## Architecture diagram
![](../media/archi-6.png)


### Task 1 : Investigation of  Data Loss Prevention Alerts

In this task you'll explore on investigating dlp alerts in Microsoft Purview.

1. In **Microsoft Edge**, navigate to **[compliance mirosoft com](https://compliance.microsoft.com/)**.

1. In the **Microsoft Purview** portal, in the left navigation pane, expand **Data loss prevention** and select **Alerts** and notice alerts have been generated you can view details for each alerts

   ![](../media/cc19.png)

1. Choose filters to refine the list of alerts. Choose Customize columns to list the properties you want to see. You can also choose to sort the alerts in ascending or descending order in any column.

1. In preview, you see severity column with the values of Low, Medium, High and None.

1. Select any one alerts and review information and click on **View details** to verify the alerts.

     ![](../media/cc20.png)

1. Select the Events tab to view all of the events associated with the alert. You can choose a particular event to view its details. For a list of some of the available event details, select one alert to check the details.

1. Select  **Overview** tab page for the alert. The overview page provides a summary:

   - of what happened
   - who performed the actions that caused the policy match
   - information about the matched policy, and more

1. Select **Events** tab and access the following tab to review the details:

   - Event Details
   - Classifiers that detected a match
   - Metadata associated with the event

1. Back on **Alerts** page and click on one of the alerts and select the User activity summary tab to see all of the exfiltration activities the user has engaged in up to the past 120 days.

   >**Note**: Users must be in scope of an insider risk management policy to see the User activity summary tab.

1. After you investigate the alert, After you take the required action for the alert, set the status of the alert to Resolved.

    ![](../media/lab12-image8.png)

    ![](../media/lab12-image(9).png)

    >**Note**: You Investigated the alert in the DLP alert management dashboard and also explored on  Activity explorer to investigate alerts. You can also share alerts with other users in your organization.

### Conclusion:
The investigation of DLP alerts is a critical step in the data security lifecycle. It empowers organizations to respond effectively to potential threats, enhance data protection policies, and educate users on proper data handling practices. The ability to mark alerts as resolved signifies that appropriate actions have been taken to address the identified issues.


### Review
During this lab, you've gained knowledge on the process of Investigating the Data Loss Prevention Alerts

### You have successfully completed the lab

### Click on next to continue with the next lab
