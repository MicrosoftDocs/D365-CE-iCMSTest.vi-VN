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
# <a name="sample-close-an-incident"></a>Sample: Close an incident

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Service samples](https://code.msdn.microsoft.com/Service-Samples-f42adf82).   

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to process and close an incident (case) with a case resolution.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Service#CloseAnIncident](../snippets/csharp/CRMV8/service/cs/closeanincident.cs#closeanincident)]  
  
### <a name="see-also"></a>Xem thêm  
 [Incident (Case) Entities](incident-case-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.CloseIncidentRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.IsValidStateTransitionRequest>
