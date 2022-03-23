# Lab 3: Create users and groups in NMM portal

## **Overview**


## Exercise 1: Create new users for AVD

1. From the NMM portal, Click on **Accounts** *(1)* from the side blade and click on **Manage** *(2)* on your default NMM Account which you created in Lab 1.

   ![](media/2s1.png)

1. Select **USERS** *(1)* from the side blade and click on **Add users** *(2)* to create a new image.

   ![](media/3s1.png)
   
1. Provide the following details to create the new user.

   - **FIRST NAME**: *nmmuser (1)*
   - **LAST NAME**: *01 (2)*
   - **PRIMARY EMAIL ADDRESS**: *nmmuser01 (3)*
   - **USERNAME**: Check the *Make username as primary email address (4)*
   - Click on ***OK*** *(5)*

   ![](media/3s2.png)
   
1. **Copy and save** *(1)* the user's password in a notepad which you'll be using later and click on **Ok** *(2)*.

   ![](media/3s3.png)    
   
1. Similarly, Let's create another user. Select **USERS** *(1)* from the side blade and click on **Add users** *(2)* to create a new image.

   ![](media/3s4.png)
   
1. Provide the following details to create the new user.

   - **FIRST NAME**: *nmmuser (1)*
   - **LAST NAME**: *02 (2)*
   - **PRIMARY EMAIL ADDRESS**: *nmmuser02 (3)*
   - **USERNAME**: Check the *Make username as primary email address (4)*
   - Click on ***OK*** *(5)*

   ![](media/3s5.png)
   
1. **Copy and save** *(1)* the user's password in a notepad which you'll be using later and click on **Ok** *(2)*.

   ![](media/3s6.png)
   
1. Once the user creation completes. You'll be able to see new users in the **USERS** page in NMM portal.

   ![](media/3s11.png)
   
## Exercise 2: Create new group for AVD

1. From the NMM portal, Click on **Accounts** *(1)* from the side blade and click on **Manage** *(2)* on your default NMM Account which you created in Lab 1.

   ![](media/2s1.png)

1. Select **GROUPS** *(1)* from the side blade and click on **Add group** *(2)* to create a new image.

   ![](media/3s7.png)
   
1. Provide the following details to create the new group.

   - **GROUP TYPE**: *Security group (1)*
   - **NAME**: *NMM Users (2)*
   - **MEMBERS**: Select *ODL_User, nmmuser01. nmmuser02 (3)* from the drop down
   - **OWNERS**: Select *ODL_User (4)* from the drop down
   - Click on ***Save*** *(5)*
   
   ![](media/3s8.png)
   
1. Once the group creation completes. CLick on the **drop down** icon of NMM Users group and select the **Manage AVD desktops** option.

   ![](media/3s9.png)
   
1. In **DESKTOP ASSIGNMENTS** page, Select the default **AVD-HP-01** *(1)* desktop host pool and click on **Confirm** *(2)*.

   ![](media/3s10.png)
   
1. Once the Desktop assignment completes, you'll be able to see the new **NMM Users** group attached to the **AVD-HP-01** desktop host pool.

   ![](media/3s12.png)
   
   
    
