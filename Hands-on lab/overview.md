### **Nerdio Manager for MSPs**

## **Overview**

Contoso IT consulting services, headquartered in Los Angeles, California, is one among the top IT companies in the country and it is located throughout North America. These locations continue to grow through acquisition. The nature of their business requires a high level of security of Personal Identifiable Information (PII) for their employees.

## **Hands-on Labs Scenario**

Contoso IT consulting services has grown rapidly and this has created a new challenge. Contoso has a requirement for providing it's staff with a secured environment to access their work application and also certain staff required access to a fully managed desktop that is goverened by policies. Contoso wants their resources to provide more control and flexibility over the computing environment. They want their resources to be highly available.

Recently contoso is experiencing a huge rise in supporting their remote working staff, essentially staff that is working from home and because Contoso does not have a capacity to provide such huge number of managed physical computers and the Board of Directors has been unwilling to increase capital expenditures for new equipment. Contoso has been evaluating the value of the public cloud and views Microsoft Azure as an excellent option to maintain availability and increase scalability of resources to the organization. Contoso have decided to use Nerdio Manager for MSP  which is an automation and management solution hosted in Azure marketplace.

Contoso have decided to use Azure virtual desktop which is the cloud Desktop-as-a-Service (DaaS) offered by Nerdio as part of Azure and Microsoft 365.

They need your help to configure the infrastructure and deploy a solution. You need to choose the right approach to set up and deploy the solution on Nerdio manager. However, you will be doing it in phases as the development and testing progress.
 
## **Lab Context**

In this hands-on lab, you will implement an Azure Virtual Desktop (formerly Windows Virtual Desktop) Infrastructure creating an account in  Nerdio Manager portal and learn how-to setup a working AVD environment end-to-end in a typical Enterprise model. At the end of the lab, attendees will have deployed an Azure Active Directory Tenant that is running on Azure. Azure Active Directory (Azure AD) is Microsoft’s enterprise cloud-based identity and access management (IAM) solution.

You will also deploy the Azure infrastructure for the Azure Virtual Desktop Tenant(s), Host pool which is  a collection of one or more identical virtual machines (VMs), also known as session hosts within Azure Virtual Desktop environments. A default Application group will be created which is a collection of remote applications that you can present to a user or group of users. You will publish desktops and remote apps with the help of application group. You will be configuring FSLogix for user profile solution which stores a complete user profile in a single container. You will be configuring windows server machine to run QuickBooks Database Manager. You will be configuring Autoscaling to reduce the cost effectively . You will be configuring back up for the session hosts and FSLogix file share for recovery incase of a diaster. You will be cobfiguring NAT gateway for the virtul netowork to simplify outbound Internet connectivity. Finally, you will explore on Cost Estimator and Monitoring for the Azure Virtual Desktop infrastructure.

## **Lab 1: Lab 1: Create NMM Account**

In this lab with the help of Nerdio Manager for MSPs(NMM) and Azure portal, you'll create a Nerdio account and explore the resources deployed by NMM. NMM manages Multi-tenant Azure Virtual Desktop and Windows 365 Deployment, Management, and Optimization Platform for Managed Service Providers.

You will be creating an account using already deployed Azure active directory domain service(AAD DS) instance and other required resources. Since Contoso is already using an AAD DS Service, AAD DS Service will provide Identity and Authentication service.

## **Lab 2: Create Desktop Image and Host pool**

In this lab we will deploy a Azure Virtual Desktop host pool for pooled desktops. This is a set of computers or hosts which operate on an as-needed basis. In a pooled configuration we will be hosting multiple non-persistent sessions, with no user profile information stored locally. This is where FSLogix Profile Containers provide the users profile to the host dynamically. This provides the ability for an organization to fully utilize the compute resources on a single host and lower the total overhead, cost, and number of remote workstations.

## **Lab 3: Create users and assign users to security groups**
    
In this lab, you'll be creating new users in your NMM Account and assigning them to different Azure AD security groups.
    



Click on the **Next** button present in the bottom-right corner of this lab guide.
