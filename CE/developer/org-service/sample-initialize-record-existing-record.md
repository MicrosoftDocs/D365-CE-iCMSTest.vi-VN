---
title: 'Sample: Initialize a record from an existing record (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to use the IOrganizationService.InitializeFromRequest message to create new records from an existing record
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1d0d6df3-e905-4b63-beaa-3f72f73bfa17
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e2b96d1f5054aa65bb12b1723cc37e2f61ade13d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385898"
---
# <a name="sample-initialize-a-record-from-an-existing-record"></a>Sample: Initialize a record from an existing record

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7). 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
-   [Full Sample – C#](sample-initialize-record-existing-record.md#full_C)  
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to use the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Crm.Sdk.Messages.InitializeFromRequest> message to create new records from an existing record.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[StrongTypes#InitializeFrom1](../../snippets/csharp/CRMV8/strongtypes/cs/initializefrom1.cs#initializefrom1)]  
  
<a name="full_C"></a>   
## <a name="full-sample--c"></a>Full Sample – C#  
 [!code-csharp[StrongTypes#InitializeFrom](../../snippets/csharp/CRMV8/strongtypes/cs/initializefrom.cs#initializefrom)]  
  
### <a name="see-also"></a>Xem thêm  
 [Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md)   
 [Sample: Retrieve license information](sample-retrieve-license-information.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.InitializeFromRequest>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*>
