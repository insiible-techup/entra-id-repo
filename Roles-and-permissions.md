# Roles and Permissions in entra id

It defines who can access what resources and perform specific actions within a system.

## Roles

Roles group users according to their job functions or positions within an organization.  

A role has a collection of predefined permissions related to specific tasks or responsibilities.  

## Permissions

Permissions are specific actions or operations that users can perform within a system. They determine the level of access and control a user has over various resources.  

Examples of permissions include:  

- **Read**: Ability to view data or resources  
- **Write**: Ability to create or modify data  
- **Delete**: Ability to remove data or resources  
- **Execute**: Ability to run specific functions or processes  

## Built-in Roles

Microsoft Entra ID provides about 60 built-in roles with predefined sets of permissions.  

These roles fall into three main categories:  

1. **Microsoft Entra ID-specific roles**: Manage resources within Microsoft Entra ID (e.g., User Administrator, Application Administrator, Groups Administrator).  
2. **Service-specific roles**: Manage features within specific Microsoft services (e.g., Exchange Administrator, Intune Administrator, SharePoint Administrator).  
3. **Cross-service roles**: Span multiple services, including **Global Administrator** and **Global Reader** roles that are honored across all Microsoft 365 services.  

## Custom Roles

For more granular control, Microsoft Entra ID supports **custom roles**, allowing organizations to create role definitions tailored to their specific needs.  

Custom roles require a **Microsoft Entra ID P1** license. 
