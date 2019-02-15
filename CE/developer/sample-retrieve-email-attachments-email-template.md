---
title: 'Sample: Retrieve email attachments for an email template (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to retrieve email attachments associated with an email template by using the IOrganizationService.QueryBase) method
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
- sample for retrieving email attachments associated with email templates, activity entities
- activity entities samples, retrieving email attachments associated with email templates
ms.assetid: 4efd5301-9f7b-426d-b2f8-54c71ed04585
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 57e30430975c0cb6c0e7a43f9b9f5e9330508619
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386785"
---
# <a name="sample-retrieve-email-attachments-for-an-email-template"></a><span data-ttu-id="6fa9f-103">Sample: Retrieve email attachments for an email template</span><span class="sxs-lookup"><span data-stu-id="6fa9f-103">Sample: Retrieve email attachments for an email template</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6fa9f-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="6fa9f-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="6fa9f-105">Download the complete sample from [Sample: Work with Templates](https://code.msdn.microsoft.com/Templates-Samples-1759ff39).</span><span class="sxs-lookup"><span data-stu-id="6fa9f-105">Download the complete sample from [Sample: Work with Templates](https://code.msdn.microsoft.com/Templates-Samples-1759ff39).</span></span>    
 
## <a name="prerequisites"></a><span data-ttu-id="6fa9f-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="6fa9f-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="6fa9f-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="6fa9f-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="6fa9f-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="6fa9f-108">Demonstrates</span></span>  
 <span data-ttu-id="6fa9f-109">This sample shows how to retrieve email attachments associated with an email template by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="6fa9f-109">This sample shows how to retrieve email attachments associated with an email template by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="6fa9f-110">method.</span><span class="sxs-lookup"><span data-stu-id="6fa9f-110">method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6fa9f-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="6fa9f-111">Example</span></span>  
 [!code-csharp[Templates#GetEmailTemplateAttachments](../snippets/csharp/CRMV8/templates/cs/getemailtemplateattachments.cs#getemailtemplateattachments)]  
  
### <a name="see-also"></a><span data-ttu-id="6fa9f-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6fa9f-112">See also</span></span>  
 <span data-ttu-id="6fa9f-113">[E-Mail Attachments](email-activity-entities.md#E-MailAttachments) </span><span class="sxs-lookup"><span data-stu-id="6fa9f-113">[E-Mail Attachments](email-activity-entities.md#E-MailAttachments) </span></span>  
 <span data-ttu-id="6fa9f-114">[Template Entity](entities/template.md) </span><span class="sxs-lookup"><span data-stu-id="6fa9f-114">[Template Entity](entities/template.md) </span></span>  
 <span data-ttu-id="6fa9f-115">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="6fa9f-115">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="6fa9f-116">[Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="6fa9f-116">[Sample Code for Recurring Appointments](sample-code-schedule-appointment-entities.md) </span></span>  
 <span data-ttu-id="6fa9f-117">[Sample: Convert a Fax to a Task](sample-convert-fax-task.md) </span><span class="sxs-lookup"><span data-stu-id="6fa9f-117">[Sample: Convert a Fax to a Task](sample-convert-fax-task.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
