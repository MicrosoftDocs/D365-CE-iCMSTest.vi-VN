---
title: 'Sample: Convert a fax to a task (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs'
description: This sample shows how to create a task for a fax by using the IOrganizationService.Entity) method
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f82fe3eb-1867-4edb-869d-58081f38d653
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 647961b1c8d8ed9664d72768a5266759451870d8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388635"
---
# <a name="sample-convert-a-fax-to-a-task"></a><span data-ttu-id="43ebe-103">Sample: Convert a fax to a task</span><span class="sxs-lookup"><span data-stu-id="43ebe-103">Sample: Convert a fax to a task</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="43ebe-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="43ebe-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="43ebe-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span><span class="sxs-lookup"><span data-stu-id="43ebe-105">Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="43ebe-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="43ebe-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]

## <a name="requirements"></a><span data-ttu-id="43ebe-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="43ebe-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="43ebe-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="43ebe-108">Demonstrates</span></span>  
 <span data-ttu-id="43ebe-109">This sample shows how to create a task for a fax by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="43ebe-109">This sample shows how to create a task for a fax by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="43ebe-110">method.</span><span class="sxs-lookup"><span data-stu-id="43ebe-110">method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="43ebe-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="43ebe-111">Example</span></span>  
 [!code-csharp[Activities#ConvertFaxToTask](../snippets/csharp/CRMV8/activities/cs/convertfaxtotask.cs#convertfaxtotask)]  
  
### <a name="see-also"></a><span data-ttu-id="43ebe-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="43ebe-112">See also</span></span>  
 <span data-ttu-id="43ebe-113">[Sample Code for Activity](sample-code-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="43ebe-113">[Sample Code for Activity](sample-code-activity-entities.md) </span></span>  
 <span data-ttu-id="43ebe-114">[Fax Entity](entities/fax.md) </span><span class="sxs-lookup"><span data-stu-id="43ebe-114">[Fax Entity](entities/fax.md) </span></span>  
 <span data-ttu-id="43ebe-115">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="43ebe-115">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 [<span data-ttu-id="43ebe-116">Sample: Promote an Email Message to Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="43ebe-116">Sample: Promote an Email Message to Dynamics 365 for Customer Engagement apps</span></span>](sample-promote-email-message.md)
