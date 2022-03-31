# Lab 2: Create Desktop Image and Host pool

## Overview

Host pools are groups of Azure VMs that "host" the Azure Virtual Desktops that end users log into. All VMs in the host pool share a set of configuration options: VM size, base image, AD domain, user profile storage location, etc. Nerdio Manager for MSP supports four different types of host pools. The four types vary by the "desktop experience." The types of host pools are: 
* Multi User Desktop (Pooled)
* Multi User RemoteApp (Pooled)
* Single User Desktop (Pooled)
* Single User Desktop (Personal)

In this lab, you'll be creating a desktop image and a host pool in your NMM Acount.

## Exercise 1: Create Desktop Image

In this exercise, you'll be creating a Desktop Image as per the specifications in your NMM Account.

1. From the NMM portal, Click on **Accounts** *(1)* from the side blade and click on **Manage** *(2)* on your default NMM Account which you created in Lab 1.

   ![](media/2s1.png)
   
1. Select **DESKTOP IMAGES** *(1)* from the side blade and click on **Add from Azure library** *(1)* to create a new image.

   ![](media/2s2.png)
   
1. Provide the following details to create the new desktop image.

   - **NAME**: *AVDImage (1)*
   - **AZURE IMAGE**: *Windows 10 (21H1) EVD + Office ProPlus - Gen2 (mutlsession) (2)*
   - **VM SIZE**: *D4s_v4 (4C/16GB/Standard) (3)*
   - **OS DISK**: *128GB (E10/Standard SSD) (4)*
   - Check ***Join to AD*** *(5)*
   - Click on ***OK*** *(6)*

   ![](media/2ss3.png)
   
   >**NOTE**: Image creation will take 40 - 45 minutes. Please wait untill it completes.
   
1. Once the image creation is completed. You'll be able to see the image in the Desktop image side blade.

   ![](media/2ss4.png)
   
## Exercise 2: Create Host Pool

In this exercise, you'll be creating a Multi User Desktop (Pooled) AVD Host Pool as per the specifications in your NMM Account.

1. From the NMM portal, Click on **Accounts** *(1)* from the side blade and click on **Manage** *(2)* on your default NMM Account which you created in Lab 1.

   ![](media/2s1.png)
   
1. From your NMM account home page, Expand the **AVD** *(1)* drop down and Select **Hostpool** *(2)*.

   ![](media/2s5.png)
   
1. Click on **Add host pool** to create a new host pool.

   ![](media/2s6.png)
   
1. Provide the following details to create the new host pool.

   - **NAME**: *AVD-HP-01 (1)*
   - **DESKTOP EXPERIENCE**: Select *Multi user desktop (pooled) (2)*
   - **DIRECTORY**: Select the *default Azure AD DS (3)* from the drop down
   - **FSLOGIX**: *Default profile (default) (4)* from the drop down

   ![](media/2ss7.png)
   
   - **NEW WORKSPACE**: *AVD-WS-01 (5)*
   - **NAME PREFIX**: *AVD-SH (6)*
   - **DESKTOP IMAGE**: Select *AVDImage (7)* from the drop down
   - **VM SIZE**: *D4s_v4 (4C/16GB/Standard) (8)*
   - **OS DISK**: *128GB (E10/Standard SSD) (9)*
   - **QUICK ASSIGN**: Leave it to default *(10)*
   - Click on ***OK*** *(11)*

   ![](media/2ss8.png)

   In **Manage AUTO-SCALE AVD-HP-01** page, Leave all the options to **default** and click on **Save**.
   
   ![](media/2ss9.png)
   
   ![](media/2ss10.png)
   
1. Once the host pool completes. You'll be able to see the **AVD-HP-01** in the host pool side blade. Click on **Manage** *(1)*.

   ![](media/2ss11.png)
   
1. From **AVD-HP-01** host pool page, Click on **Add Session host** to compute instance to the host pool.

   ![](media/2s12.png)
   
1. Provide the following details to add new session hosts to the host pool.

   - **HOST POOL**: *2 (1)*
   - **NAME PREFIX**: *AVD-SH (2)*
   -  **DESKTOP IMAGE**: Select *AVDImage (3)* from the drop down
   - **VM SIZE**: *D4s_v4 (4C/16GB/Standard) (4)*
   - **OS DISK**: *128GB (E10/Standard SSD) (5)*
   - **Process hosts in groups of**: *1 (6)*
   - **Number of failures before aborting**: *1 (7)*
   - Click on ***OK*** *(8)*

   ![](media/2ss13.png)
   
   >**NOTE**: **Session hosts** creation will take around 30 - 40 minutes to complete. Please wait untill it completes.
   
 1. Once the session hosts creation completes, You'll be able to see the session hosts in the host pool.

    ![](media/2ss14.png)
    
 1. Click on the Next button present in the bottom-right corner of this lab guide.
   
