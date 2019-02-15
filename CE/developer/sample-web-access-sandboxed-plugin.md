---
title: 'Sample: Web access from a sandboxed plug-in (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: 'The sample demonstrates how to code a plug-in that has Web (network) access and be registered in the sandbox. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 5cfa323a-1407-4651-a602-9f99e6370e5f
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b4307387bccd426824b375ef8eaf746b39facaf5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388190"
---
# <a name="sample-web-access-from-a-sandboxed-plug-in"></a><span data-ttu-id="91e6b-103">Sample: Web access from a sandboxed plug-in</span><span class="sxs-lookup"><span data-stu-id="91e6b-103">Sample: Web access from a sandboxed plug-in</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]
<span data-ttu-id="91e6b-104">Download the sample: [Work with plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade).</span><span class="sxs-lookup"><span data-stu-id="91e6b-104">Download the sample: [Work with plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="91e6b-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="91e6b-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]

## <a name="requirements"></a><span data-ttu-id="91e6b-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="91e6b-106">Requirements</span></span>  
 <span data-ttu-id="91e6b-107">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="91e6b-107">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> 
  
 <span data-ttu-id="91e6b-108">Register the compiled plug-in to run in the sandbox on the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server.</span><span class="sxs-lookup"><span data-stu-id="91e6b-108">Register the compiled plug-in to run in the sandbox on the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="91e6b-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="91e6b-109">Demonstrates</span></span>  
 <span data-ttu-id="91e6b-110">Demonstrates how to code a plug-in that has Web (network) access and be registered in the sandbox.</span><span class="sxs-lookup"><span data-stu-id="91e6b-110">Demonstrates how to code a plug-in that has Web (network) access and be registered in the sandbox.</span></span>  
  
## <a name="example"></a><span data-ttu-id="91e6b-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="91e6b-111">Example</span></span>  
 [!code-csharp[Plug-ins#WebClientPlugin](../snippets/csharp/CRMV8/plug-ins/cs/webclientplugin.cs#webclientplugin)]  
  
### <a name="see-also"></a><span data-ttu-id="91e6b-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="91e6b-112">See also</span></span>  
 <span data-ttu-id="91e6b-113">[Plug-in Development](plugin-development.md) </span><span class="sxs-lookup"><span data-stu-id="91e6b-113">[Plug-in Development](plugin-development.md) </span></span>  
 <span data-ttu-id="91e6b-114">[Write a Plug-in](write-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="91e6b-114">[Write a Plug-in](write-plugin.md) </span></span>  
 <span data-ttu-id="91e6b-115">[Plug-in Isolation, Trust, and Statistics](plugin-isolation-trusts-statistics.md) </span><span class="sxs-lookup"><span data-stu-id="91e6b-115">[Plug-in Isolation, Trust, and Statistics](plugin-isolation-trusts-statistics.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.IPlugin>   
 <xref:Microsoft.Xrm.Sdk.ITracingService>
