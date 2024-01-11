# Lab 01 - Configure Sensitive Labels 

## Lab Overview 

Sensitivity labels are implemented to classify your organization’s data in a way that shows how sensitive the data is. This helps you reduce risks in sharing information that shouldn’t be accessible to anyone outside your organization or department. Applying sensitivity labels allows you to protect all your data easily.

## Lab scenario

In this lab, you'll configure Microsoft Purview Information Protection's Sensitivity labels which empower you to classify and secure your organization's data, ensuring that user productivity and collaboration remain unimpeded.

Microsoft Purview's Sensitivity labels are implemented to safeguard Project data. With labels like "Confidential-Finance" and "Highly-Confidential" employees effortlessly classify and share information securely. When a user mistakenly attempts to share a sensitive document, Purview intervenes, preventing potential data exposure. The organization thrives as Sensitivity labels balance robust data protection with seamless collaboration.

## Lab objectives

In this lab, you will complete the following tasks:

+ Task 1: Create sensitivity labels in Microsoft Purview

## Estimated timing: 40 minutes
  
## Architecture diagram

![](../media/purview-lab1.png)

### Task 1: Create sensitivity labels in Microsoft Purview

In this task, the focus is on creating Sensitivity labels in Microsoft Purview, a crucial step in classifying and safeguarding organizational data. The process involves accessing the Microsoft 365 admin center, navigating to the Compliance center, and utilizing Purview to define and implement Sensitivity labels.

1. If you have not already logged in to the admin center, in the address bar of Microsoft Edge enter [admin microsoft com](https://admin.microsoft.com/).

1. Sign in with your admin credentials.
   
1. In the Sign in window you will see a login screen, in that enter the following email/username and then click on **Next**. 

    * Email/Username: <inject key="AzureAdUserEmail"></inject>

1. Now enter the password and click on **Sign in**.
   
   * Password: <inject key="AzureAdUserPassword"></inject>
  
1. When prompted to stay signed in, select **Yes**. This takes you to the Microsoft 365 admin center page.

1. From the left navigation pane of the Microsoft 365 admin center, select **Show all**.

    ![](../media/sc-900-lab15-1-01.png)

1. Under Admin centers, select **Compliance**. A new browser page will open and navigate you to the Microsoft Purview welcome page.  

    ![](../media/sc-900-lab15-1-2.png)
    
    ![](../media/sc-900-lab13-01.png)

1. From the left navigation panel of the Microsoft Purview, under Solutions, Expand **Information protection**, and in the dropdown select **Overview** and review the information.

1. From the left menu select **labels** and in the **yellow** information box, indicate that **Your organization has not turned on the ability to process content in Office online files that have encrypted sensitivity labels applied and are stored in OneDrive and SharePoint**. Select **Turn on now**. Once you do this, there can be a delay for the setting to propagate through the system.

1. On **Labels** tab from the dropdown and then select **+ Create a label**.

    ![](../media/lab1-image(2).png)

1. Provide a name and description for your label. Select **Next** at the bottom of the page.

    | Setting | Action |
    | -- | -- |
    | **Name** text box | Enter **Confidential-Finance** |
    | **Display name** text box | Enter **Confidential-Finance** |
    | **Description for users** text box | Enter **Confidential-Finance Demo** | 

    !![](../media/lab1-image3.png)

1. Note the scope for this label. The scope is set to **Items**. Read the description but don’t change anything. Select **Next** at the bottom of the page.

      ![](../media/lab1-image4.png)

1. On the Choose protection settings for labeled items select the **Apply or remove encryption** and **Apply content marking**, then select **Next**.

    ![](../media/lab1-image5.png)
    
1. The Encryption window shows the configuration for the encryption settings. Review the information box under Configure encryption settings and review the configured settings. Notice how the user access to content is set to never expire. You can also assign permissions to specific users and groups By clicking on the **Assign permission**. On the **Assign permission** click on **+ Add Users or Groups**.
    
    ![](../media/lab1-image6.png)

1. Select your user name **<inject key="AzureAdUserEmail"></inject>** and click on **Add**.

1. Then back to the Assign permission page and click on **Save**.

    ![](../media/lab1-image8.png)

   >**Note**: Only selected users can interact with content that has this label applied. Under users and groups, the tenant is defined so all users in your tenant can 
   view content that has this label.

1. Click **Next** on **Encryption** window.

   ![](../media/lab1-image9.png)
   
1. On the content markings page, take note of the information box at the top of the page. Turn on the **Content Making** and select the check box for **Add a watermark**, **Add a header** and **Add a footer**.

    ![](../media/lab1-image10.png)
   
1. Select **Add a watermark**, click on **Customize text** on each and provide the **Confidential Document** text to it and click on **Save**.

    ![](../media/lab1-image11.png)
  
1. Repeat last step for **Add a header**, & **Add a footer**, and click on **Customize text** on each and provide the **Confidential Document** text to it and click on **Save**. Content markings will be applied to documents but only headers and footers will be applied to email messages. In other words, watermarks are not applied to emails.

1. The content marking associated with this label is a watermark. Select **Next** at the bottom of the page.

    ![](../media/lab1-image12.png)
      
1. You are now in the Auto-labeling for files and emails window. Turn on the **Auto-labeling for files and emails** and Read the description of auto-labelling on the top of the page and the information box below it and under **Detect content that matches these conditions** click on **+ Add condition** from the drop-down select **Content contains** then under **Group name** select **Add** drop-down select **Sensitive info type** and in **Sensitive info type** window search for credit and select the Credit card number, select **Add** from the button, select **Next** on the bottom of the page.

1. This next window defines protection settings for groups and sites that have this label applied. If this is not enabled, select **Next** at the bottom of the page.

      ![](../media/lab1-image14.png)

1. This next window is a preview feature to automatically apply this label to Azure database columns (such as SQL, Synapse, and more) that contain the sensitive info types you choose.  This feature is not enabled. Select **Next** at the bottom of the page.

     ![](../media/lab1-image15.png)
          
1. Review the settings and click on **Create label**.

   ![](../media/lab1-image16.png)
      
1. On Your sensitivity label that was created blade, select **Don't create a policy yet** and click on **Done**.

   ![](../media/lab1-image18.png)

1. Back on the **labels** blade notice newly created sensitivity labels.

   ![](../media/lab1-image17.png)

1. Repeat the same steps to create another sensitivity label with the name given below:

    | Setting | Action |
    | -- | -- |
    | **Name** text box | Enter **Highly-Confidential** |
    | **Display name** text box | Enter **Highly-Confidential** |
    | **Description for users** text box | Enter **Highly-Confidential Demo** | 
    |||

1. After creating the label, navigate to the left-side pane and select Labels to observe the list of labels you have created.

     ![](../media/demo13.png)

    >**Note**: Creating Sensitivity labels is essential for maintaining a structured approach to data protection. It allows organizations to clearly define the sensitivity level of their data, enabling the implementation of tailored security measures. This proactive approach helps prevent unauthorized access and ensures compliance with data protection policies.

    >**Note**: Once you have created sensitivity labels in the next lab you'll configure label policies and then you can start using them and learn how to manage sensitivity labels. You'll also learn to apply sensitivity labels to emails and files in upcoming labs.

### Conclusion
Creating sensitivity labels is that it empowers users and organizations to proactively manage and secure their data. By applying sensitivity labels, users can clearly classify information based on its level of sensitivity, enabling streamlined protection measures. This not only reduces the risk of unauthorized access but also fosters a culture of responsible data handling. The creation and implementation of sensitivity labels contribute significantly to enhancing data security, ensuring compliance, and promoting a structured approach to managing sensitive information within an organization.
      
### Review
During this lab, you've gained knowledge on creating and configuring sensitivity labels in Microsoft Purview.

### You have successfully completed the lab

### Click on next to continue with the next lab
