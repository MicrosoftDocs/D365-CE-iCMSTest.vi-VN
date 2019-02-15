---
title: Configure Exchange folder-level tracking rules (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Learn how to configure Exchange folder-level tracking rules
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 4cd28905-1af7-42aa-a9d8-27c271dfcb8c
caps.latest.revision: 17
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 253a2d319245a5645bfa0c0065fd0bbf5f570aa7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385793"
---
# <a name="configure-exchange-folder-level-tracking-rules"></a><span data-ttu-id="8e2dc-103">Configure Exchange folder-level tracking rules</span><span class="sxs-lookup"><span data-stu-id="8e2dc-103">Configure Exchange folder-level tracking rules</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8e2dc-104">Configure folder-level tracking rules to map a [!INCLUDE[pn_Microsoft_Exchange](../includes/pn-microsoft-exchange.md)] inbox folder to a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps record so that all the emails in the [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] folder get automatically tracked against the mapped record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-104">Configure folder-level tracking rules to map a [!INCLUDE[pn_Microsoft_Exchange](../includes/pn-microsoft-exchange.md)] inbox folder to a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps record so that all the emails in the [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] folder get automatically tracked against the mapped record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span> <span data-ttu-id="8e2dc-105">Folder-level tracking of emails will work only if:</span><span class="sxs-lookup"><span data-stu-id="8e2dc-105">Folder-level tracking of emails will work only if:</span></span>  

- <span data-ttu-id="8e2dc-106">The folder-level tracking feature is enabled for your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-106">The folder-level tracking feature is enabled for your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance.</span></span> <span data-ttu-id="8e2dc-107">You can enable folder-level tracking by using the web client or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)].</span><span class="sxs-lookup"><span data-stu-id="8e2dc-107">You can enable folder-level tracking by using the web client or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="8e2dc-108">[Configure folder-level tracking](../admin/configure-outlook-exchange-folder-level-tracking.md)</span><span class="sxs-lookup"><span data-stu-id="8e2dc-108">[Configure folder-level tracking](../admin/configure-outlook-exchange-folder-level-tracking.md)</span></span>  

- <span data-ttu-id="8e2dc-109">The folder that you are tracking is under the **Inbox** folder in [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)].</span><span class="sxs-lookup"><span data-stu-id="8e2dc-109">The folder that you are tracking is under the **Inbox** folder in [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)].</span></span> <span data-ttu-id="8e2dc-110">Emails in the folders that are not under the **Inbox** folder won’t be tracked.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-110">Emails in the folders that are not under the **Inbox** folder won’t be tracked.</span></span>  

<a name="Create"></a>   
## <a name="create-and-manage-folder-level-tracking-rules"></a><span data-ttu-id="8e2dc-111">Create and manage folder-level tracking rules</span><span class="sxs-lookup"><span data-stu-id="8e2dc-111">Create and manage folder-level tracking rules</span></span>  
 <span data-ttu-id="8e2dc-112">Use the [MailboxTrackingFolder Entity](entities/mailboxtrackingfolder.md) to programmatically configure and manage your folder-level tracking rules.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-112">Use the [MailboxTrackingFolder Entity](entities/mailboxtrackingfolder.md) to programmatically configure and manage your folder-level tracking rules.</span></span> <span data-ttu-id="8e2dc-113">To set up a tracking rule, use the following attributes.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-113">To set up a tracking rule, use the following attributes.</span></span>  


|                                   <span data-ttu-id="8e2dc-114">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="8e2dc-114">Attribute</span></span>                                   |                                                                                                                                                                                                                <span data-ttu-id="8e2dc-115">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8e2dc-115">Description</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  [<span data-ttu-id="8e2dc-116">ExchangeFolderId</span><span class="sxs-lookup"><span data-stu-id="8e2dc-116">ExchangeFolderId</span></span>](entities/mailboxtrackingfolder.md#BKMK_ExchangeFolderId)  | <span data-ttu-id="8e2dc-117">Specify the [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] folder ID that you want to map.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-117">Specify the [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] folder ID that you want to map.</span></span> <span data-ttu-id="8e2dc-118">You can use the [!INCLUDE[pn_Exchange_Web_Services_EWS](../includes/pn-exchange-web-services-ews.md)] to retrieve the ID of a folder under your Inbox folder.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-118">You can use the [!INCLUDE[pn_Exchange_Web_Services_EWS](../includes/pn-exchange-web-services-ews.md)] to retrieve the ID of a folder under your Inbox folder.</span></span> <span data-ttu-id="8e2dc-119">For more information, see [MSDN: How to: Work with folders by using EWS in Exchange](https://msdn.microsoft.com/library/office/dn535504.aspx).</span><span class="sxs-lookup"><span data-stu-id="8e2dc-119">For more information, see [MSDN: How to: Work with folders by using EWS in Exchange](https://msdn.microsoft.com/library/office/dn535504.aspx).</span></span> <span data-ttu-id="8e2dc-120">This is a required attribute.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-120">This is a required attribute.</span></span> |
|         [<span data-ttu-id="8e2dc-121">MailboxId</span><span class="sxs-lookup"><span data-stu-id="8e2dc-121">MailboxId</span></span>](entities/mailboxtrackingfolder.md#BKMK_MailboxId)         |                                                                                                                                         <span data-ttu-id="8e2dc-122">Specify the mailbox ID in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] that you want to create the rule for.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-122">Specify the mailbox ID in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] that you want to create the rule for.</span></span> <span data-ttu-id="8e2dc-123">This is a required attribute.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-123">This is a required attribute.</span></span>                                                                                                                                          |
| [<span data-ttu-id="8e2dc-124">RegardingObjectId</span><span class="sxs-lookup"><span data-stu-id="8e2dc-124">RegardingObjectId</span></span>](entities/mailboxtrackingfolder.md#BKMK_RegardingObjectId) |                                                                                                       <span data-ttu-id="8e2dc-125">Set the regarding object in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps that you want the specified [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] folder to be mapped to.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-125">Set the regarding object in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps that you want the specified [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] folder to be mapped to.</span></span> <span data-ttu-id="8e2dc-126">This is an optional attribute.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-126">This is an optional attribute.</span></span>                                                                                                       |

 <span data-ttu-id="8e2dc-127">The following sample code shows how you can create a folder-level tracking rule.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-127">The following sample code shows how you can create a folder-level tracking rule.</span></span>  

```csharp  
// Create a folder-level tracking rule  
MailboxTrackingFolder newTrackingFolder = new MailboxTrackingFolder();  

// Set the required attributes  
newTrackingFolder.ExchangeFolderId = "123456"; // Sample value. Retrieve this value using Exchange Web Services (EWS)  
newTrackingFolder.MailboxId = new EntityReference(Mailbox.EntityLogicalName, _mailboxId);  

// Set the optional attributes  
newTrackingFolder.RegardingObjectId = new EntityReference(Account.EntityLogicalName, _accountId);  
newTrackingFolder.RegardingObjectId.Name = _accountName;  
newTrackingFolder.ExchangeFolderName = "Sample Exchange Folder";  

// Execute the request to create the rule   
_folderTrackingId = _serviceProxy.Create(newTrackingFolder);  
Console.WriteLine("Created folder-level tracking rule for '{0}'.\n", _mailboxName);  
```  

 <span data-ttu-id="8e2dc-128">You can create a maximum of 25 folder-level tracking rules per mailbox.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-128">You can create a maximum of 25 folder-level tracking rules per mailbox.</span></span> <span data-ttu-id="8e2dc-129">The folder ID of the [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] folder can’t be validated at the time of creating the mapping using SDK.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-129">The folder ID of the [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] folder can’t be validated at the time of creating the mapping using SDK.</span></span> <span data-ttu-id="8e2dc-130">However, as soon as you create a mapping rule, and if the folder ID is invalid, it will show up in the UI in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to indicate that the mapping is invalid.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-130">However, as soon as you create a mapping rule, and if the folder ID is invalid, it will show up in the UI in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to indicate that the mapping is invalid.</span></span>  

 <span data-ttu-id="8e2dc-131">Any manual changes done to the regarding object in the tracked activity records, created in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps as a result of the folder-level tracking rule, will be overridden the next time server-side synchronization occurs.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-131">Any manual changes done to the regarding object in the tracked activity records, created in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps as a result of the folder-level tracking rule, will be overridden the next time server-side synchronization occurs.</span></span> <span data-ttu-id="8e2dc-132">For example, if you have set up a mapping between the `Adventure Works` folder and the `Adventure Works` account, all the emails in the `Adventure Works`[!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] folder will be tracked as activities in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] with the regarding set to the `Adventure Works` account record.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-132">For example, if you have set up a mapping between the `Adventure Works` folder and the `Adventure Works` account, all the emails in the `Adventure Works`[!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] folder will be tracked as activities in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] with the regarding set to the `Adventure Works` account record.</span></span> <span data-ttu-id="8e2dc-133">If you change the regarding of some activities to any other record, it will automatically be overridden the next time server-side synchronization occurs.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-133">If you change the regarding of some activities to any other record, it will automatically be overridden the next time server-side synchronization occurs.</span></span>  

<a name="Retrieve"></a>   
## <a name="retrieve-folder-level-tracking-rules-for-a-mailbox"></a><span data-ttu-id="8e2dc-134">Retrieve folder-level tracking rules for a mailbox</span><span class="sxs-lookup"><span data-stu-id="8e2dc-134">Retrieve folder-level tracking rules for a mailbox</span></span>  
 <span data-ttu-id="8e2dc-135">You can retrieve all the folder-level tracking rules for a mailbox by using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveMailboxTrackingFoldersRequest> message.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-135">You can retrieve all the folder-level tracking rules for a mailbox by using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveMailboxTrackingFoldersRequest> message.</span></span> <span data-ttu-id="8e2dc-136">Pass the mailbox ID for which you want to retrieve the rules in the <xref:Microsoft.Crm.Sdk.Messages.RetrieveMailboxTrackingFoldersRequest>.<xref:Microsoft.Crm.Sdk.Messages.RetrieveMailboxTrackingFoldersRequest.MailboxId></span><span class="sxs-lookup"><span data-stu-id="8e2dc-136">Pass the mailbox ID for which you want to retrieve the rules in the <xref:Microsoft.Crm.Sdk.Messages.RetrieveMailboxTrackingFoldersRequest>.<xref:Microsoft.Crm.Sdk.Messages.RetrieveMailboxTrackingFoldersRequest.MailboxId></span></span> <span data-ttu-id="8e2dc-137">property, and execute the message.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-137">property, and execute the message.</span></span>  

 <span data-ttu-id="8e2dc-138">The following sample code shows how you can retrieve folder-level tracking rules for a mailbox.</span><span class="sxs-lookup"><span data-stu-id="8e2dc-138">The following sample code shows how you can retrieve folder-level tracking rules for a mailbox.</span></span>  

```csharp  
// Retrieve the folder mapping rules for a mailbox  
RetrieveMailboxTrackingFoldersRequest req = new RetrieveMailboxTrackingFoldersRequest  
{  
    MailboxId = _mailboxId.ToString()  
};  

RetrieveMailboxTrackingFoldersResponse resp = (RetrieveMailboxTrackingFoldersResponse_serviceProxy.Execute(req);  
Console.WriteLine("Retrieved folder-level tracking rules for {0}:", _mailboxName);  
int n = 1;  
foreach (var folderMapping in resp.MailboxTrackingFolderMappings)  
{  
    Console.WriteLine("\tRule {0}: '{1}' is mapped to '{2}'.",   
        n, folderMapping.ExchangeFolderName, folderMapping.RegardingObjectName);  
    n++;  
}  
```  

### <a name="see-also"></a><span data-ttu-id="8e2dc-139">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8e2dc-139">See also</span></span>  
 <xref href="Microsoft.Dynamics.CRM.RetrieveMailboxTrackingFolders?text=RetrieveMailboxTrackingFolders Function" /><br />
 [<span data-ttu-id="8e2dc-140">MailboxTrackingFolder Entity</span><span class="sxs-lookup"><span data-stu-id="8e2dc-140">MailboxTrackingFolder Entity</span></span>](entities/mailboxtrackingfolder.md)<br />
 [<span data-ttu-id="8e2dc-141">Mailbox Entity</span><span class="sxs-lookup"><span data-stu-id="8e2dc-141">Mailbox Entity</span></span>](entities/mailbox.md)<br />
 [<span data-ttu-id="8e2dc-142">Đặt cấu hình theo dõi cấp thư mục</span><span class="sxs-lookup"><span data-stu-id="8e2dc-142">Configure folder-level tracking</span></span>](../admin/configure-outlook-exchange-folder-level-tracking.md)<br />
 [<span data-ttu-id="8e2dc-143">Server-side Synchronization Entities</span><span class="sxs-lookup"><span data-stu-id="8e2dc-143">Server-side Synchronization Entities</span></span>](server-side-synchronization-entities.md)<br />
