---
title: 'Sample: Create, retrieve, update, and delete an email attachment (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to create, retrieve, update, and delete email attachments using methods such as IOrganizationService.Entity, IOrganizationService.ColumnSet, IOrganizationService.Entity, IOrganizationService.Guid
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- sample for creating; retrieving; updating; and deleting email attachments, activity entities
- activity entities samples, creating; retrieving; updating; and deleting email attachments
ms.assetid: 918c0b7e-2850-40c5-8333-5dad6d83b850
caps.latest.revision: 22
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ec1b862cafb6d003b875ae5774f68369e08b631e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386735"
---
# <a name="sample-create-retrieve-update-and-delete-an-email-attachment"></a><span data-ttu-id="08579-103">Sample: Create, retrieve, update, and delete an email attachment</span><span class="sxs-lookup"><span data-stu-id="08579-103">Sample: Create, retrieve, update, and delete an email attachment</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="08579-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="08579-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="08579-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span><span class="sxs-lookup"><span data-stu-id="08579-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span></span>   

## <a name="prerequisites"></a><span data-ttu-id="08579-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="08579-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="08579-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="08579-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="08579-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="08579-108">Demonstrates</span></span>  
 <span data-ttu-id="08579-109">This sample shows how to create, retrieve, update, and delete email attachments using the following methods:</span><span class="sxs-lookup"><span data-stu-id="08579-109">This sample shows how to create, retrieve, update, and delete email attachments using the following methods:</span></span>  
  
-   <span data-ttu-id="08579-110"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="08579-110"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span>  
  
-   <span data-ttu-id="08579-111"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span><span class="sxs-lookup"><span data-stu-id="08579-111"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span></span>  
  
-   <span data-ttu-id="08579-112"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="08579-112"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span>  
  
-   <span data-ttu-id="08579-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="08579-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span>  
  
## <a name="example"></a><span data-ttu-id="08579-114">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="08579-114">Example</span></span>  
 [!code-csharp[Activities#CRUDEmailAttachments](../snippets/csharp/CRMV8/activities/cs/crudemailattachments.cs#crudemailattachments)]  
  
### <a name="see-also"></a><span data-ttu-id="08579-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="08579-115">See also</span></span>  
 <span data-ttu-id="08579-116">[Sample Code for Activity Entities](sample-code-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="08579-116">[Sample Code for Activity Entities](sample-code-activity-entities.md) </span></span>  
 <span data-ttu-id="08579-117">[EMail Activity Entities](email-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="08579-117">[EMail Activity Entities](email-activity-entities.md) </span></span>  
 <span data-ttu-id="08579-118">[Sample: Retrieve Email Attachments for an Email Template](sample-retrieve-email-attachments-email-template.md) </span><span class="sxs-lookup"><span data-stu-id="08579-118">[Sample: Retrieve Email Attachments for an Email Template](sample-retrieve-email-attachments-email-template.md) </span></span>  
 <span data-ttu-id="08579-119">[ActivityMimeAttachment Entity](entities/activitymimeattachment.md) </span><span class="sxs-lookup"><span data-stu-id="08579-119">[ActivityMimeAttachment Entity](entities/activitymimeattachment.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
