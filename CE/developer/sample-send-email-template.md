---
title: 'Sample: Send an email using a template (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to send an email message by using a template using the SendEmailFromTemplateRequest message
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
- sample for sending email messages, activity entities
- activity entities samples, sending email messages
ms.assetid: d5e9b6e6-abf1-4d27-bed0-df2cd1006487
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8b5cb00172028d146d0be6348ba79533ba328fc1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387921"
---
# <a name="sample-send-an-email-using-a-template"></a><span data-ttu-id="15ad4-103">Sample: Send an email using a template</span><span class="sxs-lookup"><span data-stu-id="15ad4-103">Sample: Send an email using a template</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="15ad4-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="15ad4-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="15ad4-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span><span class="sxs-lookup"><span data-stu-id="15ad4-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="15ad4-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="15ad4-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="15ad4-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="15ad4-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="15ad4-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="15ad4-108">Demonstrates</span></span>  
 <span data-ttu-id="15ad4-109">This sample shows how to send an email message by using a template using the <xref:Microsoft.Crm.Sdk.Messages.SendEmailFromTemplateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="15ad4-109">This sample shows how to send an email message by using a template using the <xref:Microsoft.Crm.Sdk.Messages.SendEmailFromTemplateRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="15ad4-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="15ad4-110">Example</span></span>  
 [!code-csharp[Activities#SendEmailUsingTemplate](../snippets/csharp/CRMV8/activities/cs/sendemailusingtemplate.cs#sendemailusingtemplate)]  
  
### <a name="see-also"></a><span data-ttu-id="15ad4-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="15ad4-111">See also</span></span>  
 <span data-ttu-id="15ad4-112">[Sample Code for Activity](sample-code-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="15ad4-112">[Sample Code for Activity](sample-code-activity-entities.md) </span></span>  
 <span data-ttu-id="15ad4-113">[Sample: Send an Email](sample-send-email.md) </span><span class="sxs-lookup"><span data-stu-id="15ad4-113">[Sample: Send an Email](sample-send-email.md) </span></span>  
 <span data-ttu-id="15ad4-114">[E-mail Activity Entities](email-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="15ad4-114">[E-mail Activity Entities](email-activity-entities.md) </span></span>  
 <span data-ttu-id="15ad4-115">[Template Entity](entities/template.md) </span><span class="sxs-lookup"><span data-stu-id="15ad4-115">[Template Entity](entities/template.md) </span></span>  
 <span data-ttu-id="15ad4-116">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="15ad4-116">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.SendEmailFromTemplateRequest>
