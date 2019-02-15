---
title: 'Sample: Validate record state and set the state of the record (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample demonstrates how to validate a change of state of an entity and set a state of an entity.
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
- setting record states sample
- validating record states sample
- record states, sample for validating and setting
ms.assetid: 6b2f00ca-dbac-47d8-ab4a-0be52b72f05d
caps.latest.revision: 15
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: eb44c575e996b3e16dc1713509108439b5b7b6bc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387297"
---
# <a name="sample-validate-record-state-and-set-the-state-of-the-record"></a>Sample: Validate record state and set the state of the record

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62) 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to validate a change of state of an entity and set a state of an entity.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#ValidateAndSetState](../snippets/csharp/CRMV8/businessmanagement/cs/validateandsetstate.cs#validateandsetstate)]  
  
### <a name="see-also"></a>Xem thêm  
 [Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.IsValidStateTransitionRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>   
 [Sample: Rollup records related to a specific record](sample-rollup-records-related-specific-record.md)
