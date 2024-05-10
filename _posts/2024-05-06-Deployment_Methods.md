---
title: Windows Deployment
description: Examples of Deployment and more.
author: P@
date: 2024-05-06 12:50:00 +1000
categories: [Deployment Tools]
tags: [Deploy]
image: 
  #path: https://plus.unsplash.com/premium_photo-1669562725515-5a63ae6c8ebc?q=80&w=2080&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
  #lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  #alt: Planning of tool selection.
---

<!-- markdownlint-capture -->
<!-- markdownlint-disable -->


<!-- markdownlint-restore -->
![Desktop View](/assets/Blog Post 1/Main.png){: width="300" height="330" }

## Methods of Deployment and Configuration of Windows: 

1. Selecting a deployment tool based on the organisational environment: 

Examples: 

- In a scenario where a company needs to deploy Windows updates to a large fleet of devices efficiently, they might choose to use Microsoft Endpoint Configuration Manager (formerly SCCM) due to its robust patch management capabilities and centralized control over deployments. 


- A company with a distributed workforce and a mix of Windows, macOS, and Linux devices needs a deployment tool that offers cross-platform support and scalability. In this scenario, they opt for Microsoft Endpoint Manager (formerly Intune) due to its cloud-based management capabilities, support for multi-platform devices, and ease of scalability across geographically dispersed locations. 

 
- A medium-sized organization with a focus on standardization and centralized management of IT resources chooses Microsoft Deployment Toolkit (MDT) as its deployment tool. MDT offers advanced customization options and integration with Windows Deployment Services (WDS), allowing the organization to create standardized Windows images and automate deployment tasks efficiently while maintaining full control over the process. 


### Choosing between migrate and rebuild:  

- When upgrading from Windows 7 to Windows 10, an organization might choose the migration approach to retain user settings, applications, and data, ensuring a seamless transition for end-users.  

- In contrast, a rebuild approach might be preferred for a fresh start or when significant changes to the system configuration are necessary. 

### Selecting an Imaging and/or provisioning strategy: 

- An organization decides to implement a hybrid deployment strategy using Windows Autopilot and Configuration Manager. They use Autopilot for cloud-based provisioning of new devices and Configuration Manager for on-premises imaging and provisioning, allowing them to leverage the benefits of both approaches depending on the scenario. 

### Select a Windows edition based on requirements examples: 

- A company with stringent security and compliance requirements opts for Windows 10 Enterprise edition for its advanced security features such as BitLocker encryption, Windows Defender Application Guard, and advanced threat protection capabilities. 
 
- A small business with limited IT resources and a focus on cost-effectiveness opts for Windows 10 Pro edition for its essential productivity features and compatibility with legacy applications. While lacking some advanced security functionalities of Enterprise edition, Windows 10 Pro meets the organization's basic needs without exceeding budget constraints. 

- A large enterprise operating in highly regulated industries such as finance or healthcare prioritizes data protection and compliance. Therefore, they choose Windows 10 Enterprise edition for its comprehensive security features, including Windows Information Protection, Credential Guard, and Device Guard, ensuring compliance with industry standards and safeguarding sensitive data from cyber threats. 

### Implement subscription-based activation: 

- A company chooses to activate their Windows 10 devices using subscription-based activation through Microsoft 365 E3 or E5 licenses, ensuring seamless licensing management and access to premium features such as Windows Virtual Desktop and Microsoft Defender Advanced Threat Protection. 



| Type                    | Class         | Description                                     |
| -------------------     | ------------- |-------------------------------------------------|
| Windows Autopilot       | Modern        | Transform an existing Windows 11 installation,  |
|                         |               | join the device to Azure AD, and enroll it into |
|                         |               | a Mobile Device Management solution to complete |
|                         |               | the configuration.                              |
|                         |               |                                                 |
|--------------------     |-------------- |-------------------------------------------------|
| Windows 11 Subscription | Modern        | Upgrade the Windows edition seamlessly without  | 
|                         |               | requiring intervention or rebooting of the      |
|                         |               | device.                                         | 



| Class              | Description  
| -------------------|      
| Legacy             | Outdated methods that are still in use due to existing infrastructure or compatibility reasons.   
|--------------------|
| Modern             | Methods that leverage cloud-based technologies and modern management approaches for streamlined 
|                    | deployment and management. 
|--------------------|       
| Hybrid             | Methods that combine traditional and modern approaches, often integrating on-premises infrastructure 
|                    | with cloud-based services for flexibility and scalability. 
|--------------------|                                       
| Traditional        | Methods that follow conventional practices and are commonly used in legacy environments. 

## Dynamic Provisioning 

<span style="color:red">*What transformations are currently available with Dynamic Provisioning?*</span>.

#### Provisioning Packages 

A company deploys new laptops to its employees. Instead of manually configuring each device, the IT department creates a provisioning package using the Windows Configuration Designer. This package includes pre-configured settings, such as Wi-Fi network profiles, security policies, and installed applications. When a new laptop is received, the provisioning package is applied during the Out-of-Box Experience (OOBE), automating the setup process and ensuring consistency across all devices. 

#### Subscription Activation 

An organization decides to upgrade its Windows 11 Pro devices to Windows 11 Enterprise to access additional security and management features. Instead of purchasing separate product keys and manually entering them on each device, they opt for Windows 11 Subscription Activation. With this method, the devices are automatically upgraded to Windows 11 Enterprise by associating them with the organization's Microsoft 365 subscription. This process eliminates the need for manual intervention and simplifies license management. 

#### Azure AD Join with Automatic MDM enrollment 

A company implements a bring-your-own-device (BYOD) policy, allowing employees to use their personal devices for work purposes. To ensure these devices meet organizational security and compliance standards, the company adopts Azure AD join with automatic MDM enrollment. 
  - Employees simply need to sign in with their work or school account on their personal devices. 
  - Once signed in, the devices are automatically joined to Azure AD and enrolled into the organization's Mobile Device Management (MDM) solution, such as Microsoft Intune. 
  - MDM then configures the devices according to the organization's policies, such as enforcing encryption, applying security settings, and deploying business applications. 