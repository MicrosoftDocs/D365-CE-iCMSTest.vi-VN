---
title: 'Sample: Create, retrieve, update, and delete (late bound) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample demonstrates the create, retrieve, update, and delete operations on an account using the late bound Entity class
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
- sample for late-bound Entity classes, creating; retrieving; updating; and deleting (late-bound Entity classes) sample
- creating; retrieving; updating; and deleting (late-bound Entity classes) sample
- sample for creating; retrieving; updating; and deleting (late-bound Entity classes)
- late-bound Entity classes, samples
ms.assetid: 9f4f05c6-0d19-4a32-8ef3-776757c0ea86
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f481d38b9809cbe3c2e5472260aec53f12d6ff98
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385988"
---
# <a name="sample-create-retrieve-update-and-delete-late-bound"></a>Sample: Create, retrieve, update, and delete (late bound)

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample is for [!INCLUDE[pn_crm_2015_and_online_full](../../includes/pn-crm-2015-and-online-full.md)]. Download the sample: [Sample: Create, retrieve, update and delete (late bound)](https://code.msdn.microsoft.com/Sample-Create-retrieve-e183a7fb).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]

## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="example"></a>Ví dụ  
 This sample demonstrates the create, retrieve, update, and delete operations on an account using the late bound <xref:Microsoft.Xrm.Sdk.Entity> class.  
  
 [!code-csharp[DynamicEntity#CRUDOperationsDE](../../snippets/csharp/CRMV8/dynamicentity/cs/crudoperationsde.cs#crudoperationsde)]  
  
### <a name="see-also"></a>Xem thêm  
 [Use the Late Bound Entity Class in Code](use-late-bound-entity-class-code.md)   
 [Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>   
 [Sample: Create, Retrieve, Update and Delete (CRUD) Using Strong Types](sample-create-retrieve-update-delete-records-early-bound.md)
