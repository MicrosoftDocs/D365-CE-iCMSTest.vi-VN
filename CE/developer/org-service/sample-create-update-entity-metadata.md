---
title: 'Sample: Create and update entity metadata (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to create a custom entity by using the CreateEntityRequest message. It also uses the CreateAttributeRequest to add several different types of attributes to the entity.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 237c75a2-cae5-467b-b894-ab0f7572e7f9
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 63e691c9d2121bfe9489d06f535c6d3003206c8f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388448"
---
# <a name="sample-create-and-update-entity-metadata"></a>Sample: Create and update entity metadata

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. Download the sample: [Work with entity metadata](https://code.msdn.microsoft.com/Samples-of-entities-916efa41). 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create a custom entity by using the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest> message. It also uses the <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> to add several different types of attributes to the entity.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[entities#CreateUpdateEntityMetadata](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata.cs#createupdateentitymetadata)]  
  
### <a name="see-also"></a>Xem thêm  
 [Customize entity metadata](../customize-entity-metadata.md)   
 [Sample: Create a Custom Activity Entity](sample-create-custom-activity-entity.md)   
 [Extend the Metadata Model for Dynamics 365 for Customer Engagement](use-organization-service-metadata.md)   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesResponse>
