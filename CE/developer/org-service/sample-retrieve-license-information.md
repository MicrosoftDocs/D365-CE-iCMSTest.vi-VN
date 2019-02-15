---
title: 'Sample: Retrieve license information (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to use the IDeploymentService.RetrieveDeploymentLicenseTypeRequest message and the IOrganizationService.RetrieveLicenseInfoRequest message to retrieve information about licenses
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 7c8bd1ce-59e0-4884-b7bf-e809d7fd0b75
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
ms.openlocfilehash: 0ff0b135805ccaa70a39af3dfbb3f203a7cea22b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386520"
---
# <a name="sample-retrieve-license-information"></a>Sample: Retrieve license information

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).   

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
 [Full Sample – C#](sample-initialize-record-existing-record.md#full_C)  
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to use the <xref:Microsoft.Xrm.Sdk.Deployment.IDeploymentService>.<xref:Microsoft.Crm.Sdk.Messages.RetrieveDeploymentLicenseTypeRequest> message and the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Crm.Sdk.Messages.RetrieveLicenseInfoRequest> message to retrieve information about licenses.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[StrongTypes#License1](../../snippets/csharp/CRMV8/strongtypes/cs/license1.cs#license1)]  
  
<a name="full_C"></a>   
## <a name="full-sample--c"></a>Full Sample – C#  
 [!code-csharp[StrongTypes#License](../../snippets/csharp/CRMV8/strongtypes/cs/license.cs#license)]  
  
### <a name="see-also"></a>Xem thêm  
 [Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md)   
 <xref:Microsoft.Xrm.Sdk.Deployment.IDeploymentService>   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveDeploymentLicenseTypeRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveLicenseInfoRequest>
