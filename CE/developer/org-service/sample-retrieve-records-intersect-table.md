---
title: 'Sample: Retrieve records from an intersect table (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to retrieve records from an intersect table
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
- intersect entities sample, retrieving records for many-to-many relationships by using intersect entities
- sample for retrieving records in many-to-many (N:N) relationships by using intersect entities
- sample for retrieving records from intersect tables
- retrieving records for many-to-many (N:N) relationships by using intersect entities sample
- retrieving records from intersect tables sample
- retrieving records for many-to-many (N:N) relationships by using intersect entities, sample
ms.assetid: a46636f6-a77d-4afc-93fa-10621f0f839f
caps.latest.revision: 20
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b3c006f31b745560888c6f727e15bb5df912d2dd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387411"
---
# <a name="sample-retrieve-records-from-an-intersect-table"></a>Sample: Retrieve records from an intersect table

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).   

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="example"></a>Ví dụ  
 This sample shows how to retrieve records from an intersect table:  
  
 [!code-csharp[Query#RetrieveRecordsFromAnIntersectTable](../../snippets/csharp/CRMV8/query/cs/retrieverecordsfromanintersecttable.cs#retrieverecordsfromanintersecttable)]  
  
### <a name="see-also"></a>Xem thêm  
 [Retrieve Records for Many-To-Many Relationships using Intersect Entities](retrieve-records-many-to-many-relationships-intersect-entities.md)   
 [Build Queries with FetchXML](build-queries-fetchxml.md)   
 [Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>   
 <xref:Microsoft.Xrm.Sdk.Query.FetchExpression>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>
