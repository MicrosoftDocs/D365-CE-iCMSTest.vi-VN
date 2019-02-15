---
title: 'Sample: Send an email (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to send an email SendEmailRequest message
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
ms.assetid: c95bec08-bdd2-420a-93aa-ee7c0f20fa16
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 46697a16c5f8b9798191a297f1c900223320a8d7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388342"
---
# <a name="sample-send-an-email"></a><span data-ttu-id="3f18f-103">Sample: Send an email</span><span class="sxs-lookup"><span data-stu-id="3f18f-103">Sample: Send an email</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3f18f-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="3f18f-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="3f18f-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span><span class="sxs-lookup"><span data-stu-id="3f18f-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3f18f-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="3f18f-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
    
## <a name="requirements"></a><span data-ttu-id="3f18f-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="3f18f-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="3f18f-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="3f18f-108">Demonstrates</span></span>  
 <span data-ttu-id="3f18f-109">This sample shows how to send an email <xref:Microsoft.Crm.Sdk.Messages.SendEmailRequest> message.</span><span class="sxs-lookup"><span data-stu-id="3f18f-109">This sample shows how to send an email <xref:Microsoft.Crm.Sdk.Messages.SendEmailRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3f18f-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="3f18f-110">Example</span></span>  
 [!code-csharp[Activities#SendEmail](../snippets/csharp/CRMV8/activities/cs/sendemail.cs#sendemail)]  
  
### <a name="see-also"></a><span data-ttu-id="3f18f-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3f18f-111">See also</span></span>  
 <span data-ttu-id="3f18f-112">[Sample Code for Activity](sample-code-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="3f18f-112">[Sample Code for Activity](sample-code-activity-entities.md) </span></span>  
 <span data-ttu-id="3f18f-113">[Sample: Create an Email Using a Template](sample-create-email-template.md) </span><span class="sxs-lookup"><span data-stu-id="3f18f-113">[Sample: Create an Email Using a Template](sample-create-email-template.md) </span></span>  
 <span data-ttu-id="3f18f-114">[E-mail Activity Entities](email-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="3f18f-114">[E-mail Activity Entities](email-activity-entities.md) </span></span>  
 <span data-ttu-id="3f18f-115">[Email Entity](entities/email.md) </span><span class="sxs-lookup"><span data-stu-id="3f18f-115">[Email Entity](entities/email.md) </span></span>  
 <span data-ttu-id="3f18f-116">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="3f18f-116">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.SendEmailRequest>
