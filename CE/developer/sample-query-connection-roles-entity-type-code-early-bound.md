---
title: 'Sample: Query connection roles by entity type code (early bound) (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to use a query to find a connection role for an account entity by specifying an entity type code.
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
- sample for querying to find connection roles, for account entities by specifying an entity type
- querying to find connection roles for account entities by specifying an entity type, sample
ms.assetid: 84e4e68d-2e43-4fb8-843e-b878504edec5
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 87e640ad08af306904dd6180cf1c0997e678661a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387876"
---
# <a name="sample-query-connection-roles-by-entity-type-code-early-bound"></a>Sample: Query connection roles by entity type code (early bound)

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to use a query to find a connection role for an account entity by specifying an entity type code.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#QueryConnectionRolesByEntityTypeCode](../snippets/csharp/CRMV8/businessmanagement/cs/queryconnectionrolesbyentitytypecode.cs#queryconnectionrolesbyentitytypecode)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Connection Entities](sample-code-connection-entities.md)   
 [Connection Entities](connection-entities.md)   
 [Sample: Query Connections by Reciprocal Roles (Early Bound)](sample-query-connections-reciprocal-roles-early-bound.md)
