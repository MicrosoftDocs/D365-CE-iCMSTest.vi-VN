---
title: 'Sample: Create a reciprocal connection role (early bound) (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample code demonstrates how to create the reciprocal connection roles.
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
- creating reciprocal connection roles, sample
- sample for creating reciprocal connection roles
ms.assetid: 768e2422-e725-4de4-85c9-17dff24ee69c
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bd1d524e043b4e038f08bd083665bf0f941a8007
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388145"
---
# <a name="sample-create-a-reciprocal-connection-role-early-bound"></a>Sample: Create a reciprocal connection role (early bound)

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. [Download the Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create the reciprocal connection roles. It creates a connection role for an account and a connection role for a contact, and then makes them reciprocal by associating them with each other.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#CreateReciprocalConnectionRole](../snippets/csharp/CRMV8/businessmanagement/cs/createreciprocalconnectionrole.cs#createreciprocalconnectionrole)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Connection Entities](sample-code-connection-entities.md)   
 [Connection Entities](connection-entities.md)   
 [Sample: Update a Connection Role (Early Bound)](sample-update-connection-role-early-bound.md)
