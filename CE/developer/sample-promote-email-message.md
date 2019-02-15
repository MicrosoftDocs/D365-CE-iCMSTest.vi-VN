---
title: 'Sample: Promote an email message to Dynamics 365 for Customer Engagement apps| MicrosoftDocs'
description: This sample shows how to create an email activity instance from the specified email message in Dynamics 365 for Customer Engagement by using the DeliverPromoteEmailRequest message
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 69763a0a-af67-48b8-adf2-470c1cdf6196
caps.latest.revision: 22
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fc132afcc60361118a34105b27a1a7969a1b7e56
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387372"
---
# <a name="sample-promote-an-email-message-to-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="fc306-103">Sample: Promote an email message to Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="fc306-103">Sample: Promote an email message to Dynamics 365 for Customer Engagement apps</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="fc306-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="fc306-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="fc306-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span><span class="sxs-lookup"><span data-stu-id="fc306-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="fc306-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="fc306-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
    
## <a name="requirements"></a><span data-ttu-id="fc306-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="fc306-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="fc306-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="fc306-108">Demonstrates</span></span>  
 <span data-ttu-id="fc306-109">This sample shows how to create an email activity instance from the specified email message in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] by using the <xref:Microsoft.Crm.Sdk.Messages.DeliverPromoteEmailRequest> message.</span><span class="sxs-lookup"><span data-stu-id="fc306-109">This sample shows how to create an email activity instance from the specified email message in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] by using the <xref:Microsoft.Crm.Sdk.Messages.DeliverPromoteEmailRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fc306-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="fc306-110">Example</span></span>  
 [!code-csharp[Activities#DeliverPromoteEmail](../snippets/csharp/CRMV8/activities/cs/deliverpromoteemail.cs#deliverpromoteemail)]  
  
### <a name="see-also"></a><span data-ttu-id="fc306-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="fc306-111">See also</span></span>  
 <span data-ttu-id="fc306-112">[Sample Code for Activity](sample-code-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="fc306-112">[Sample Code for Activity](sample-code-activity-entities.md) </span></span>  
 <span data-ttu-id="fc306-113">[E-mail Activity Entities](email-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="fc306-113">[E-mail Activity Entities](email-activity-entities.md) </span></span>  
 <span data-ttu-id="fc306-114">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="fc306-114">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="fc306-115">[Sample: Send an Email Using a Template](sample-send-email-template.md) </span><span class="sxs-lookup"><span data-stu-id="fc306-115">[Sample: Send an Email Using a Template](sample-send-email-template.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.DeliverPromoteEmailRequest>
