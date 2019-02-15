---
title: 'Sample: Retrieve time zone information (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to retrieve time zone information.
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
- retrieving time zone information, time zone entities
- time zone entities, retrieving time zone information
ms.assetid: 3df3e8c5-ff20-40c7-8ea8-e91001daebd1
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5da51210c8a4f7e2d58d072e0242827be6a85b45
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387133"
---
# <a name="sample-retrieve-time-zone-information"></a><span data-ttu-id="a1bbe-103">Sample: Retrieve time zone information</span><span class="sxs-lookup"><span data-stu-id="a1bbe-103">Sample: Retrieve time zone information</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a1bbe-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="a1bbe-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="a1bbe-105">Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span><span class="sxs-lookup"><span data-stu-id="a1bbe-105">Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="a1bbe-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="a1bbe-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="a1bbe-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="a1bbe-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="a1bbe-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="a1bbe-108">Demonstrates</span></span>  
 <span data-ttu-id="a1bbe-109">This sample shows how to retrieve time zone information.</span><span class="sxs-lookup"><span data-stu-id="a1bbe-109">This sample shows how to retrieve time zone information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a1bbe-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="a1bbe-110">Example</span></span>  
 [!code-csharp[BusinessManagement#WorkingWithTimeZones](../snippets/csharp/CRMV8/businessmanagement/cs/workingwithtimezones.cs#workingwithtimezones)]  
  
### <a name="see-also"></a><span data-ttu-id="a1bbe-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a1bbe-111">See also</span></span>  
 <span data-ttu-id="a1bbe-112">[Time Zone Entities](time-zone-entities.md) </span><span class="sxs-lookup"><span data-stu-id="a1bbe-112">[Time Zone Entities](time-zone-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.GetAllTimeZonesWithDisplayNameRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.GetTimeZoneCodeByLocalizedNameRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.UtcTimeFromLocalTimeRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.LocalTimeFromUtcTimeRequest>
