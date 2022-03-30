# Lab 9: Create server and application

## **Overview**

NMM Partner API allows MSPs to automate various actions in NMM via API that they can do via the NMM portal. For examples, MSPs can create & manage host pools, hosts, desktop images all via the API.

## Exercise 1: Create server instance

1. From the NMM portal, Click on **Accounts** *(1)* from the side blade and click on **Manage** *(2)* on your default NMM Account which you created in Lab 1.

   ![](media/2s1.png)
   
1. Select **SERVERS** from the side blade.

   ![](media/9s1.png)
   
1. From the **SERVERS** *(1)* page, Click on **Add server** *(2)*.

   ![](media/9s2.png)
   
1. In **ADD SERVER** window, Please provide the details mentioned below to create a new server machine.

   - **NAME**: *AVDserver (1)*
   - **AZURE IMAGE**: *Windows server 2019 (2)*
   - **VM SIZE**: *DS1_v2 (1C/3.5GB/Standard) (3)*
   - **OS DISK**: *128GB (E10/Standard SSD) (4)*
   - Check ***Join to AD*** *(5)*
   - Click on ***OK*** *(6)*
   
   ![](media/9s3.png)
   
1. Once the creation completes, You'll be able see the new server in the **SERVERS** page.

   ![](media/9s4.png)
