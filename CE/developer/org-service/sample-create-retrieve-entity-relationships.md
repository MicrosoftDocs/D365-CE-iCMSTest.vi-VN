---
title: 'Sample: Create and retrieve entity relationships (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to verify that entities are eligible to participate in an entity relationship and then creates a 1:N and an N:N entity relationship.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 2e1eafb6-18f3-40e3-820c-5e0d0f6a2bf3
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 38b9061b255cd393bdd88cdce9ae8591c943555f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387711"
---
# <a name="sample-create-and-retrieve-entity-relationships"></a>Sample: Create and retrieve entity relationships

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the sample: [Work with entity relationships](https://code.msdn.microsoft.com/Samples-of-entity-218db099).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to verify that entities are eligible to participate in an entity relationship and then creates a 1:N and an N:N entity relationship.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[relationships#WorkWithRelationships](../../snippets/csharp/CRMV8/relationships/cs/workwithrelationships.cs#workwithrelationships)]  
  
### <a name="see-also"></a>Xem thêm  
 [Use the Organization service with Dynamics 365 for Customer Engagement apps metadata](use-organization-service-metadata.md)   
 [Customize Entity Relationship Metadata](../customize-entity-relationship-metadata.md)   
 [Create Entity Relationships](create-retrieve-entity-relationships.md)   
 [Sample: Dump Entity Relationship Information to a File](sample-dump-entity-relationship-information-file.md)
