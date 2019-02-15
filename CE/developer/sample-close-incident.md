---
title: 'Sample: Close an incident (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample code demonstrates how to process and close an incident (case) with a case resolution.
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
- processing and closing incidents (cases), service entities sample
- sample for closing incidents (cases)
ms.assetid: 748ac902-3ba5-456c-ab91-aece8947131a
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6a66a945a5a63d55da0d33a81115d6a1f81510cd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387020"
---
# <a name="sample-close-an-incident"></a><span data-ttu-id="5c8aa-103">Sample: Close an incident</span><span class="sxs-lookup"><span data-stu-id="5c8aa-103">Sample: Close an incident</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5c8aa-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="5c8aa-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="5c8aa-105">[Download the Service samples](https://code.msdn.microsoft.com/Service-Samples-f42adf82).</span><span class="sxs-lookup"><span data-stu-id="5c8aa-105">[Download the Service samples](https://code.msdn.microsoft.com/Service-Samples-f42adf82).</span></span>   

## <a name="prerequisites"></a><span data-ttu-id="5c8aa-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="5c8aa-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="5c8aa-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="5c8aa-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="5c8aa-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="5c8aa-108">Demonstrates</span></span>  
 <span data-ttu-id="5c8aa-109">This sample shows how to process and close an incident (case) with a case resolution.</span><span class="sxs-lookup"><span data-stu-id="5c8aa-109">This sample shows how to process and close an incident (case) with a case resolution.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5c8aa-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="5c8aa-110">Example</span></span>  
 [!code-csharp[Service#CloseAnIncident](../snippets/csharp/CRMV8/service/cs/closeanincident.cs#closeanincident)]  
  
### <a name="see-also"></a><span data-ttu-id="5c8aa-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5c8aa-111">See also</span></span>  
 <span data-ttu-id="5c8aa-112">[Incident (Case) Entities](incident-case-entities.md) </span><span class="sxs-lookup"><span data-stu-id="5c8aa-112">[Incident (Case) Entities](incident-case-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.CloseIncidentRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.IsValidStateTransitionRequest>
