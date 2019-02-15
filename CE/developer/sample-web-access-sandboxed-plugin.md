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
# <a name="sample-web-access-from-a-sandboxed-plug-in"></a>Sample: Web access from a sandboxed plug-in

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]
Download the sample: [Work with plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]

## <a name="requirements"></a>Yêu cầu  
 This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. 
  
 Register the compiled plug-in to run in the sandbox on the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server.  
  
## <a name="demonstrates"></a>Chứng tỏ  
 Demonstrates how to code a plug-in that has Web (network) access and be registered in the sandbox.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Plug-ins#WebClientPlugin](../snippets/csharp/CRMV8/plug-ins/cs/webclientplugin.cs#webclientplugin)]  
  
### <a name="see-also"></a>Xem thêm  
 [Plug-in Development](plugin-development.md)   
 [Write a Plug-in](write-plugin.md)   
 [Plug-in Isolation, Trust, and Statistics](plugin-isolation-trusts-statistics.md)   
 <xref:Microsoft.Xrm.Sdk.IPlugin>   
 <xref:Microsoft.Xrm.Sdk.ITracingService>
