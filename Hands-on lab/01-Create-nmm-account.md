# Lab 1: Create NMM Account

## **Overview**

NMM Partner API allows MSPs to automate various actions in NMM via API that they can do via the NMM portal. For examples, MSPs can create & manage host pools, hosts, desktop images all via the API.

## Exercise 1: Create Groups in Azure AD.

1. Navigate to the Azure portal, then search for *Azure Active Directory* in the search bar and select **Azure Active Directory** from the suggestions.

    ![](media/ss4.png)
    
2. You will be directed towards the Azure Active Directory **Overview** window.

    ![](media/ss5.png)
    
3. Click on the **Groups** tab under the **Manage** blade.

    ![](media/ss6.png)
    
4. Click on the **New Group**.

    ![](media/ss7.png)
    
5. Select the *Group type* as **Security**, name it **Standard AVD** and click on **Create**.

    ![](media/ss8.png)

6. Repeat the steps **4 & 5** to create a new group named **AVD QuickBooks Users**.

7. Now in the Groups window that comes up, under *All Groups*, you will be able see the two newly created groups named **Standard AVD** and **AVD QuickBooks Users**.

    ![](media/ss9.png)


## Exercise 2: Getting started with NMM

1. On the **Azure portal** search for **Resource groups** in the search bar (1) and select **Resource groups** (2) from the suggestions.

   ![](media/s10.png)
   
1. Select **mrg-nmm-[unique]** from the list of reosurce groups which is a dynamic RG created during creation NMM resource. It contains all the required resources.

   ![](media/ss1.png)
   
1. Select the **App service** from the list of resources.

   ![](media/ss2.png)
   
1. From the App service page, Select the **URL** of the web page to access the Nerdio portal.

   ![](media/ss3.png)
   
1. From the Web page, **Copy** *(1)* the PowerShell command which you'll be using it later and click on **Launch Azure Cloud Shell** *(2)*
 
   ![](media/s4.1.png)
   
1. Once the Cloud Shell launches, Click on **Show advanced settings** to configure a new storage account.
    
   ![](media/s5.png)
   
1. Use existing **JumpVM-RG** for the resource group. Create new storage account as **Storage[Deploymentid]** and blob storage as **blob**.

   ![](media/s6.png)
   
1. Once the Cloud Shell is configured, Paste the **PowerShell command** which you copied earlier and press enter.

   ![](media/s7.png)

   >**NOTE**: The execution of the command will take 5 - 10 minutes to complete. Wait till the execution completes.

1. Go to the web page and refresh the web page. Click on **Accept** to provide the neccessary permissions.

   ![](media/s8.png)
   
1. Please provide the following details in the registartion page

   - **Company**: Select the default subscription *(1)*
   - **Name**: odl_user_{deploymentid} *(2)*
   - **Email**: **<inject key="Username" />** *(3)*
   - **Country**: Select your country *(4)*
   
   Click on **Register**.
   
   ![](media/s9.png)
   
1. Once registered, You'll land up in **NMM portal**. Click on **Add account** to create new NMM account.

   ![](media/s11.png)
   
1. Provide the following details to create the account.

   **A. STEP 1: LINK TO CUSTOMER'S AZURE AD ACCOUNT**
   
   - **Grant access to Azure AD Tenant**: Click on *Connect (1)*. Login into your Azure account and click on **Accept** to provide the neccessary permission.

     ![](media/s12.1.png)
     
     ![](media/s12.png)
     
   - **Account name**: Leave it to default value *(2)*
   - **Desktop deployment model**: Select *Azure Virtual Desktop (3)* 
   - **Select subscription**: Select the default subscription from the drop down *(4)*
   - **Indicate your Active Directory setup**: Select *Use Existing Azure AD DS* from the drop down *(5)*
   
   Select **Save & next** *(6)* and wait till the configuration completes.
   
   ![](media/s13.png)
   
   **B. STEP 2: NETWORKING**
   
   - **Select Azure region**: *East US (1)*
   - **Select or create Resource Group**: *AVD-RG (2)*
   - **Select network**: *aadds-subnet(10.0.0.0/24) (3)*
   
   Select **Save & next** *(4)* and wait till the configuration completes.
   
   ![](media/s14.png)
   
   **C. STEP 3: ACTIVE DIRECTORY - EXISTING AZURE AD DS**
   
   - **Domain name**: NAME OF THE AD DS
   - **Domain admin user (must have domain join rights)**: <inject key="Username" />
   - **Domain admin password**: <inject key="Password" />

   Select **Save & next** *(4)* and wait till the configuration completes.
   
   ![](media/s15.png)
   
   **D. STEP 4: FSLOGIX STORAGE**
   
   Select **Create new Azure Files share** and provide the following details to create new storage account for FSLogix.
   
   ![](media/s16.png)
   
   - **Storage account**: fslogix{deploymentid}
   - **Resourec group**: *AVD-RG*
   - **Location**: *East US*
   - **Performance**: *Premium*
   - **File Share name**: *fsprofilestore*
   - **Provisioned capacity(GiB)**: *100*
   - **Permissions (SMB Share Contributor)**: <inject key="Username" />
   - Click on *OK*

   ![](media/s17.png)
   
   Select **Save & done** and wait till the configuration completes.
   
   ![](media/s18.png)
  
1. Once the storage account is created. You'll be able to see your NMM account in the Accounts blade.

   ![](media/s19.png)

1. Click on the Next button present in the bottom-right corner of this lab guide.
