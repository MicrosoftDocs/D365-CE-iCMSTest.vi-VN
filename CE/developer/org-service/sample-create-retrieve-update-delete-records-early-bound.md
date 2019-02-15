---
title: 'Sample: Create, retrieve, update, and delete records (early bound) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to create, retrieve, update, and delete operations on an account using the early bound class. This sample uses IOrganizationService.Entity), IOrganizationService.ColumnSet), IOrganizationService.Entity) and IOrganizationService.Guid)
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: fef4451b-a749-4db4-a8cf-08e577dff2d8
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- sample for creating; retrieving; updating; and deleting records (early bound)
- early-bound class samples, creating; retrieving; updating; and deleting records (early bound) sample
- samples for early-bound classes, creating; retrieving; updating; and deleting records (early bound) sample
- creating; retrieving; updating; and deleting records (early bound) sample, early-bound class samples
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e5315d8f2e662cc5924f45e5d404cf09613701f6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386195"
---
# <a name="sample-create-retrieve-update-and-delete-records-early-bound"></a>Sample: Create, retrieve, update, and delete records (early bound)

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create, retrieve, update, and delete operations on an account using the early bound class. This sample uses the following common methods:  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[StrongTypes#CRUDOperations](../../snippets/csharp/CRMV8/strongtypes/cs/crudoperations.cs#crudoperations)]  
  
### <a name="see-also"></a>Xem thêm  
 [Use the Early Bound Entity Classes](use-early-bound-entity-classes-code.md)   
 [Sample: Associate Records (Early Bound)](sample-associate-records-early-bound.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 [Sample: Create, Retrieve, Update and Delete (CRUD) Using Property Bag (Loosely-typed)](sample-create-retrieve-update-delete-late-bound.md)
