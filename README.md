# Azure-Infrastructure-Deployment

<h1>Project Objectives</h1>
<li>Create and configure an Azure resource group</li>
<li>Build a virtual network (vnet)</li>
<li>Divide the network into multiple subnets for different departments</li>
<li>Configure Azure Bastion for secure remote access to virtual machines</li>
<li>Deploy and configure a virtual machine</li>
<li>Implement network security groups</li>
<li>Validate network connectivity and security</li>
<li>Repeat the process but faster using terraform <b>(Coming Soon)</b></li>

<h1>Architecture Diagram</h1>
Here is a visual idea of what is being done:


<h1>Setup & Configuration</h1>

<h2>Resource Group</h2>
This is straightforward, I will choose the subscription and name the resource group. Making the resource group first will allow me to organize all other components into one group.

<h2>Virtual Network</h2>
For the virtual network, there will be 4 subnets that will represent different departments such as IT, HR, finance, and sales. Each department will have their own network while still being as a whole and communicate with each other when necessary. For this enterprise, we will use a class B private IP address 172.16.0.0/16. Here are the subnets that will be used for each department:
<li>HR</li>
<li>IT</li>
<li>Finance</li>
<li>Sales</li>

<h2>Network Security Groups</h2>

<h2>Virtual Machine Deployment</h2>
