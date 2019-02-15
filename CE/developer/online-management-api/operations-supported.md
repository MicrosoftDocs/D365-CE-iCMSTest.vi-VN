---
title: Operations supported by Online Management API for Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Provides information about the operations you can perform using the Online Management API to manage your Customer Engagement instances.
ms.date: 11/16/2018
ms.service: crm-online
ms.topic: conceptual
ms.assetid: 63600a55-a1f0-491f-83f6-b3252566d27e
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 31cc78f15c50d8fc66c4b51b2af8e30d106f5dfd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388628"
---
# <a name="operations-supported-by-online-management-api"></a>Operations supported by Online Management API 

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

You can perform most of the instance-related operations using the API that you can do using the [Dynamics 365 for Customer Engagement apps Admin Center](https://technet.microsoft.com/library/dn659834.aspx). The API also lets you perform some additional operations such as using tenant application identities to create/manage instances and retrieving service versions (releases) for instances.

For a quick start sample on how to authenticate and execute operations using Online Management API, see [Quick Start Sample: Retrieve instances in your tenant](sample-quick-start.md).

## <a name="create-retrieve-and-delete-instances"></a>Create, retrieve, and delete instances
You can perform the following core operations on instances:

|Thao tác  |Mô tả  |Rest API   |
|----------|--------------|-----------|
|Create instance  |Create an instance in your tenant. While creating an instance, you can specify the type of instance (Production, Sandbox, Support, Preview, Trial) to create among other things. |[Provision Instance](/rest/api/admin.services.crm.dynamics.com/provisioninstance)   |
|Retrieve instance  |Retrieve all instances or retrieve a specific instance in your tenant. |[Get Instances](/rest/api/admin.services.crm.dynamics.com/getinstances)<br /> <br />[Get Instance](/rest/api/admin.services.crm.dynamics.com/getinstance)  |
|Xóa phiên bản  |Delete an instance in your tenant.<br/>You can delete Customer Enagegement Sandbox instances to recover the licenses and storage space or to prevent them from being used by mistake. <br/>To delete a production instance, you must first switch to a Sandbox instance and then delete the Sandbox instance. More information: [Switch an instance](https://technet.microsoft.com/library/dn896590.aspx)|[Delete Instance](/rest/api/admin.services.crm.dynamics.com/deleteinstance)|


## <a name="back-up-and-restore-instances"></a>Back up and restore instances
You can perform the following operations to back up and restore instances:

|Thao tác  |Mô tả  |Rest API   |
|----------|--------------|-----------|
|Retrieve instance backup  |Retrieve all backups of an instance or retrieve a specific backup by specifying the restore point. |[Get Instance Backups](/rest/api/admin.services.crm.dynamics.com/getinstancebackups)<br /> <br />[Get Instance Backup](/rest/api/admin.services.crm.dynamics.com/getinstancebackup)   |
|Back up instance  |Back up an instance in your tenant. |[Backup Instance](/rest/api/admin.services.crm.dynamics.com/backupinstance)|
|Restore instance  |Restore an instance in your tenant. |[Restore Instance](/rest/api/admin.services.crm.dynamics.com/restoreinstance)|

## <a name="other-instance-related-operations"></a>Other instance-related operations
The following additional operations related to Customer Engagement instances are available. Some of these operation provide you information about things that are supported for Customer Engagement that helps you in performing core instance operations. For example, you can retrieve information about all the supported templates for creating a Customer Engagement instance, and then use one of the templates to create a new Customer Engagement instance.

|Thao tác  |Mô tả  |Rest API   |
|----------|--------------|-----------|
|Retrieve information about instance types  |Retrieve information about all the instance types in Customer Engagement or about a specific instance type. A Customer Engagement instance can be one of the following types: Production, Sandbox, Support, Preview, Trial. |[Get Instance Types Info](/rest/api/admin.services.crm.dynamics.com/getinstancetypesinfo)<br /> <br />[Get Instance Type Info](/rest/api/admin.services.crm.dynamics.com/getinstancetypeinfo)   |
|Retrieve templates  |Retrieves the templates supported for creating/provisioning a Customer Engagement instance. The four types of templates that you can choose from while provisioning an instance are: **Sales**, **Customer Service**, **Field Service**, and **Project Service Automation**.|[Get Templates](/rest/api/admin.services.crm.dynamics.com/gettemplates)|
|Apply users  |Force applies a user to a Customer Engagement instance. |[Apply User](/rest/api/admin.services.crm.dynamics.com/instances/applyuser)|
|Retrieve service versions (releases)  |Retrieves information about all the supported releases for Customer Engagement. |[Get Service Versions](/rest/api/admin.services.crm.dynamics.com/getserviceversions)|
|Retrieve currencies  |Retrieves information about all the supported currencies and regions for Customer Engagement. |[Get Currencies](/rest/api/admin.services.crm.dynamics.com/getcurrencies)|
|Retrieve languages  |Retrieves information about all the supported languages for Customer Engagement. |[Get Languages](/rest/api/admin.services.crm.dynamics.com/getlanguages)|
|Retrieve operation status  |Retrieves status of any operation that you perform using the API. |[Get Operation Status](/rest/api/admin.services.crm.dynamics.com/getoperationstatus)|
|Retrieve notifications  |Retrieves all notifications from the Notification service. |[Get All Notifications](/rest/api/admin.services.crm.dynamics.com/notification/getallnotifications)|
|Post user notifications  |Posts user notifications to the Notification service. |[Post User Notification](/rest/api/admin.services.crm.dynamics.com/notification/postusernotification)|
|Update Admin Mode setting  |Controls a Customer Engagement instance admin mode settings. If you put admin mode for a Customer Engagement instance, only administrator can access the instance. This is helpful for installing large updates to an instance, and you don't want users to access the instance until the update is complete. Restoring an instance results in enabling Admin Mode for the restored instance.|[Update Instance Admin Mode](/rest/api/admin.services.crm.dynamics.com/updateinstanceadminmode)|

## <a name="tenant-application-identity-related-operations"></a>Tenant Application Identity-related operations

A tenant appication identity enables you to authorize an app on your behalf by using server-to-server (S2S) authentication to perform operations on Customer Engagement instances. More information: [Build web applications using Server-to-Server (S2S) authentication](https://msdn.microsoft.com/library/mt790168.aspx)

Application identity hs to be created before it can be registered with the Online Management API.

|Thao tác  |Mô tả  |Rest API   |
|----------|--------------|-----------|
|Create tenant application identity  |Registers a tenant application identity to be used with Online Management API.|[Create Tenant Application Identity](/rest/api/admin.services.crm.dynamics.com/createtenantapplicationidentity)|
|Retrieve tenant application identity  |Retrieves tenant application identies registered with Online Management API.|[Get Tenant Application Identity](/rest/api/admin.services.crm.dynamics.com/gettenantapplicationidentity)|
|Enable or disable tenant application identity  |Enables or disables tenant application identies registered with Online Management API.|[Enable Tenant Application Identity](/rest/api/admin.services.crm.dynamics.com/enabletenantapplicationidentity)<br/>[Disable Tenant Application Identity](/rest/api/admin.services.crm.dynamics.com/disabletenantapplicationidentity)|

### <a name="related-topics"></a>Related Topics  

[Get started with Online Management API](get-started-online-management-api.md)

[Authenticate to use Online Management API](authentication.md)

[Online Management API Reference](/rest/api/admin.services.crm.dynamics.com)
