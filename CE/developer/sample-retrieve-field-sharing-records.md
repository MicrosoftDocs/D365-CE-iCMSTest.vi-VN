---
title: 'Sample: Retrieve field sharing records (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: 'The sample shows how to retrieve the PrincipalObjectAttributeAccess (field sharing) records for an entity. '
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- secured field-access records sample, retrieving
- PrincipalObjectAttributeAccess entity sample, using to enable field security
- using the PrincipalObjectAttributeAccess entity to enable field security
- retrieving secured field-access records, sample
ms.assetid: 5b23d413-c69a-4568-a490-09454362417b
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7bea225244a8ac723e879ddbfc0b6c3fb53aff49
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388232"
---
# <a name="sample-retrieve-field-sharing-records"></a>Sample: Retrieve field sharing records

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample here [Work with Field security entities](https://code.msdn.microsoft.com/Work-with-Field-Security-a18489bf)  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="example"></a>Ví dụ  
 This sample shows how to retrieve the `PrincipalObjectAttributeAccess` (field sharing) records for an entity.  
  
 [!code-csharp[FieldSecurity#RetrieveUserSharedAttributePermissions1](../snippets/csharp/CRMV8/fieldsecurity/cs/retrieveusersharedattributepermissions1.cs#retrieveusersharedattributepermissions1)]  
  
### <a name="see-also"></a>Xem thêm  
 [How Field Security Can Be Used to Control Access to Field Values in Dynamics 365 for Customer Engagement apps](security-dev/use-field-security-control-access-field-values.md)   
 [Field Security Entities](field-security-entities.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
