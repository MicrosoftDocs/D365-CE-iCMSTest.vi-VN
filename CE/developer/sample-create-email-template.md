---
title: 'Sample: Create an email using a template (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to instantiate an email record by using the InstantiateTemplateRequest message
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 4a17a1b0-c111-4575-ae70-802b79a2c6ae
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a5aaff7f540ce8b3e0bea8934d2e3d9a907eb9a5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388253"
---
# <a name="sample-create-an-email-using-a-template"></a><span data-ttu-id="dbae9-103">Sample: Create an email using a template</span><span class="sxs-lookup"><span data-stu-id="dbae9-103">Sample: Create an email using a template</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="dbae9-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="dbae9-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="dbae9-105">Download the complete sample from [Sample: Work with Templates](https://code.msdn.microsoft.com/Templates-Samples-1759ff39).</span><span class="sxs-lookup"><span data-stu-id="dbae9-105">Download the complete sample from [Sample: Work with Templates](https://code.msdn.microsoft.com/Templates-Samples-1759ff39).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="dbae9-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="dbae9-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="dbae9-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="dbae9-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="dbae9-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="dbae9-108">Demonstrates</span></span>  
 <span data-ttu-id="dbae9-109">This sample shows how to instantiate an email record by using the <xref:Microsoft.Crm.Sdk.Messages.InstantiateTemplateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="dbae9-109">This sample shows how to instantiate an email record by using the <xref:Microsoft.Crm.Sdk.Messages.InstantiateTemplateRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dbae9-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="dbae9-110">Example</span></span>  
 [!code-csharp[Templates#CreateEmailUsingTemplate](../snippets/csharp/CRMV8/templates/cs/createemailusingtemplate.cs#createemailusingtemplate)]  
  
### <a name="see-also"></a><span data-ttu-id="dbae9-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="dbae9-111">See also</span></span>  
 <span data-ttu-id="dbae9-112">[Sample Code for Activity](sample-code-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="dbae9-112">[Sample Code for Activity](sample-code-activity-entities.md) </span></span>  
 <span data-ttu-id="dbae9-113">[EMail Activity Entities](email-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="dbae9-113">[EMail Activity Entities](email-activity-entities.md) </span></span>  
 <span data-ttu-id="dbae9-114">[Email Entity](entities/email.md) </span><span class="sxs-lookup"><span data-stu-id="dbae9-114">[Email Entity](entities/email.md) </span></span>  
 <span data-ttu-id="dbae9-115">[Template Entity](entities/template.md) </span><span class="sxs-lookup"><span data-stu-id="dbae9-115">[Template Entity](entities/template.md) </span></span>  
 <span data-ttu-id="dbae9-116">[Sample: Work with Activity Party Records](sample-work-activity-party-records.md) </span><span class="sxs-lookup"><span data-stu-id="dbae9-116">[Sample: Work with Activity Party Records](sample-work-activity-party-records.md) </span></span>  
 <span data-ttu-id="dbae9-117">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="dbae9-117">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.InstantiateTemplateRequest>
