---
title: 'Sample: Rollup records related to a specific record (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: 'The sample demonstrates how to roll up opportunities by the parent account. '
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
- related records sample, rolling up
- rolling up records sample
ms.assetid: 59c8a58c-1add-4c29-915f-8aa0ae07f30c
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2a7b48017eb84044881b784cc6c07f90103921fb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386022"
---
# <a name="sample-rollup-records-related-to-a-specific-record"></a>Sample: Rollup records related to a specific record

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to roll up opportunities by the parent account.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#RollupByObject](../snippets/csharp/CRMV8/businessmanagement/cs/rollupbyobject.cs#rollupbyobject)]  
  
### <a name="see-also"></a>Xem thêm  
 [Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md)   
 <xref:Microsoft.Crm.Sdk.Messages.RollupRequest>   
 [Sample: Set and retrieve entity images](sample-set-retrieve-entity-images.md)
