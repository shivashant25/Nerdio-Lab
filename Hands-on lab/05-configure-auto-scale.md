# Lab 5: Configure Auto Scaling

## Overview

The autoscale feature lets you scale your AVD Host Pools up or down to optimize deployment costs. Based on your needs, you can make a scaling plan based on time of day, specific days of the week, and session limits per session host. In this lab, you'll be configuring auto-scaling of the AVD host pool in your NMM Account. 

## Exercise 1: Configure Auto Scaling

In this exercise, We'll be configuring auto-scaling of an existing AVD Host Pool in your NMM Account.  
   
1. In NMM portal, Click on **AVD** *(1)* and Select **Host Pools** *(2)*.

   ![](media/2s5.png)
   
1. Click on **Manage** next to the AVD-HP-01 host pool.

   ![](media/2ss11.png)
   
1. Verify that the two session hosts exists under the AVD-HP-01 host pool.

   ![](media/2ss14.png)
    
   >**NOTE**: If Session hosts are still deploying. Wait till the deployment completes.

1. Click on Host Pools on the left-hand side blade *(1)*, then click onthe  manage hosts button and navigate to **Auto-Scale> configure** *(2)*.

   ![](media/5s1.png)
   
1. Under **HOST POOL SIZING**, Set **Base host pool capacity** to ```3``` *(1)* and set **Burst beyond base capacity** to ```1``` *(2)*. Under **SCALING LOGIC**, Set **Stop or remove (scale in) hosts only from:**```7 p.m.``` to ```6 a.m.```. Select your time zone *(4)*.

   ![](media/5s2.png)
   
1. Under **PRE-STAGE HOSTS**, provide the following details, then Click on **Save** *(6)*.

   - **Toggle** the switch On next to **PRE-STAGE HOSTS**.
   - Timezone: **Select your default time zone** *(2)*
   - Work days: **Monday-Friday** *(3)*
   - Start of work hours: **7 a.m.** *(4)*
   - Hosts to be active by start of work hours: **2** *(5)*

   ![](media/5s3.png)
   
1. Click on the **Next** button present in the bottom-right corner of this lab guide.



