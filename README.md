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
<div align="center">
    <img src="./Screenshots%26Recordings/1.%20Architecture%20Diagram/Azure%20Deployment%20Diagram.png" alt="Azure Deployment Diagram" width="800">
</div>

<h1>Setup & Configuration</h1>

<h2>Resource Group</h2>
This is straightforward, I will choose the subscription and name the resource group. Making the resource group first will allow me to organize all other components into one group.
<div align="center">
<img src="Screenshots%26Recordings/2.%20Setup%20%26%20Configuration/1.%20Resource%20Group/Resource%20Group%20Creation%201.png" width="500">
</div>

<h2>Virtual Network</h2>
For the virtual network, there will be 4 subnets that will represent different departments such as IT, HR, finance, and sales. Each department will have their own network while still being as a whole and communicate with each other when necessary. For this enterprise, we will use a class B private IP address 172.16.0.0/12. Here are the subnets that will be used for each department:
<li>HR (172.16.0.0/24)</li>
<li>IT (172.16.1.0/24)</li>
<li>Finance (172.16.2.0/24)</li>
<li>Sales (172.16.3.0/24)</li>
<li>Azure Bastion (172.16.4.0/22)</li>
For azure, the cidr is not the same as the other departments because it can be used for all of the departments combined assuming there are 250 employees for each department that needs Bastion to remote access in a secure way.

<h2>Network Security Groups</h2>
For NSGs, there will be 2 created for the sake of this project. One will be for Azure Bastion and the other will be for the virtual machine.

<h2>Virtual Machine Deployment</h2>
To deploy a virtual machine, this is where I take all of the components that I made in my resource group and I start implementing it into the virtual machine.

<h2>Deployment Test</h2>
After Setting up all the components that are needed, now it is time to see if the virtual machine can be connected and used.
