---
title: Organization service methods (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read about the set of methods that IOrganizationService web service provides that can be used to perform common operations like Create, Retrieve, RetrieveMultiple, Update and Delete on system and custom entities and on the metadata for your organization
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 34f69739-16d5-492c-bfd3-eee6772cd5eb
caps.latest.revision: 28
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a2a61005eff98c0256613872d49dced20aceecb1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388767"
---
# <a name="organization-service-methods"></a>Organization service methods

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

The <xref:Microsoft.Xrm.Sdk.IOrganizationService> interface provides a set of methods used to perform the most common operations on system and custom entities and on the metadata for your organization. These operations can also be performed by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*> method and the corresponding message.  
  
## <a name="create"></a>Tạo  
 Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*> method to create an instance (record) of any entity that supports the **Create** message, including custom entities.  
  
## <a name="retrieve"></a>Truy xuất  
 Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*> method to retrieve an instance (record) of an entity.  
  
## <a name="retrievemultiple"></a>RetrieveMultiple  
 Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method to retrieve a collection records. The query can be specified using a query expression or Fetch XML query.  
  
## <a name="update"></a>Update  
 Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*> method to update an existing record.  
  
## <a name="delete"></a>Xóa  
 Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*> method to delete an existing record.  
  
## <a name="associate"></a>Liên kết  
 Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Associate*> method to create a link between two records that participate in a relationship.  
  
## <a name="disassociate"></a>Dừng liên kết  
 Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Disassociate*> method to delete the link between two records.  
  
## <a name="execute"></a>Thực thi  
 Use the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*> method to execute a message. This includes common processing like create and delete of data records and metadata, or it can be specialized processing such as import or detect duplicates.  
  
## <a name="example"></a>Ví dụ  
 The following code shows how to use the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>, <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>, and <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*> methods using the strong types.  
  
 [!code-csharp[StrongTypes#CompoundCreateUpdate1](../../snippets/csharp/CRMV8/strongtypes/cs/compoundcreateupdate1.cs#compoundcreateupdate1)]  
  
### <a name="see-also"></a>Xem thêm  
<xref:Microsoft.Xrm.Sdk.IOrganizationService><br />
 [Use the IOrganizationService web service to read and write data or metadata](use-organization-service-read-write-data-metadata.md)<br />
 [Use messages (request and response classes) with the Execute method](use-messages-request-response-classes-execute-method.md)<br />
 [Use ExecuteMultiple to improve performance for bulk data load](use-executemultiple-improve-performance-bulk-data-load.md)<br />
 [Microsoft.Xrm.Sdk Messages](xrm-messages-organization-service.md)<br />
 [Microsoft.Crm.Sdk Messages](organization-service-messages.md)<br />
 [Authenticate users in Dynamics 365 for Customer Engagement apps](../authenticate-users.md)<br />
 [Sample: Create, Retrieve, Update and Delete (CRUD) Using Strong Types](sample-create-retrieve-update-delete-records-early-bound.md)<br />
 [Sample: Create, Retrieve, Update and Delete (CRUD) Using Property Bag (Loosely-typed)](sample-create-retrieve-update-delete-late-bound.md)
