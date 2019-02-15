---
title: 'Sample: Validate and execute a saved query (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to use the IOrganizationService.ValidateSavedQueryRequest message to validate a FetchXML query, and then use the IOrganizationService.ExecuteByIdSavedQueryRequest message to execute the query.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 87672d8e-4a55-4a4b-a78a-9e534473b007
caps.latest.revision: 17
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3c59c30ecb5bfee1c6336cc8a036d4ee177ac9cf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388623"
---
# <a name="sample-validate-and-execute-a-saved-query"></a>Sample: Validate and execute a saved query

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
 [Full Sample – C#](sample-initialize-record-existing-record.md#full_C)  
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to use the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Crm.Sdk.Messages.ValidateSavedQueryRequest> message to validate a FetchXML query, and then use the<xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Crm.Sdk.Messages.ExecuteByIdSavedQueryRequest> message to execute the query.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Query#UserQueryAndSavedQuery1](../../snippets/csharp/CRMV8/query/cs/userqueryandsavedquery1.cs#userqueryandsavedquery1)]  
  
<a name="full_C"></a>   
## <a name="full-sample--c"></a>Full Sample – C#  
 [!code-csharp[Query#UserQueryAndSavedQuery](../../snippets/csharp/CRMV8/query/cs/userqueryandsavedquery.cs#userqueryandsavedquery)]  
  
### <a name="see-also"></a>Xem thêm  
 [Build Queries with FetchXML](build-queries-fetchxml.md)   
 [Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.ValidateSavedQueryRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.ExecuteByIdSavedQueryRequest>
