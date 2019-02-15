---
title: Define alternate keys for an entity (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The topic explains about how to create alternate keys for an entity. Alternate keys can be created programmatically or by using the customization tools
ms.custom: ''
ms.date: 10/22/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: fb4a93d6-590b-4913-96f7-25d351dc52ab
caps.latest.revision: 23
author: mayadumesh
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7dee1f35b69ee630e4367d30b9b1ff9ef15c24c6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386616"
---
# <a name="define-alternate-keys-for-an-entity"></a>Define alternate keys for an entity

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

All [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps records have unique identifiers defined as GUIDs. These are the primary key for each entity. When you need to integrate with an external data store, you might be able to add a column to the external database tables to contain a reference to the unique identifier in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps. This allows you to have a local reference to link to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps record. However, sometimes you can’t modify the external database. With alternate keys you can now define an attribute in a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps entity to correspond to a unique identifier (or unique combination of columns) used by the external data store. This alternate key can be used to uniquely identify a record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps in place of the primary key. You must be able to define which attributes represent a unique identity for your records. Once you identify the attributes that are unique to the entity, you can declare them as alternate keys through the customization user interface (UI) or in the code. This topic provides information about defining alternate keys in the data model.  

<a name="BKMK_Declare"></a>

## <a name="create-alternate-keys"></a>Create alternate keys  

You can create alternate keys programmatically or by using the customizations tools. For more information about using the customization tools, see [Define alternate keys to reference CRM records](https://technet.microsoft.com/library/29e53691-0b18-4fde-a1d0-7490aa227898.aspx).  

To define alternate keys programmatically, you first have to create an object of type <xref:Microsoft.Xrm.Sdk.Metadata.EntityKeyMetadata> (or use <xref href="Microsoft.Dynamics.CRM.EntityKeyMetadata?text=EntityKeyMetadata EntityType" /> if working with Web API). This class contains the key attributes. Once the key attributes are set, you can use `CreateEntityKey` to create the keys for an entity. This message takes the entity name and `EntityKeyMetadata` values as input to create the key.  

You should be aware of the following constraints when creating alternate keys:  

- **Valid attribute types in key definitions**  

   Only attributes of the following types can be included in alternate key definitions:  


  |      Attribute Type         |    Tên Hiển thị     |
  |-----------------------------|---------------------|
  | DecimalAttributeMetadata    |   Số Thập phân    |
  | IntegerAttributeMetadata    |    Số Nguyên     |
  | StringAttributeMetadata     | Một dòng văn bản |
  | DateTimeAttributeMetadata   |      Thời gian ngày      |
  | LookupAttributeMetadata     |       Tra cứu        |
  | PicklistAttributeMetadata   |      Danh sách chọn       |
  
 - **Attributes must be valid for create and update**  

   Each attribute used in a key must support both create and update. More information: [Valid operations on attributes](introduction-entity-attributes.md#valid-operations-on-attributes)
   
- **Attributes must not have Field-level security applied**  

- **Attributes must not be logical or inherited**  

   Most logical and inherited attributes are configured as read-only. However, many of the attributes that contain address information in entities such as Account and Contact are logical and cannot be used in a key, even though they are writable. More information: [Logical attributes](introduction-entity-attributes.md#logical-attributes)
   
- **Kích thước khóa hợp lệ**  

   Khi một khóa được tạo, hệ thống xác thực rằng nền tảng có thể hỗ trợ khóa đó, trong đó tổng kích thước khóa không vi phạm giới hạn chỉ mục dựa trên SQL như 900 byte/khóa và 16 cột/khóa. Nếu kích thước khóa không thỏa mãn giới hạn, thông báo lỗi sẽ hiển thị. 

- **Maximum number of alternate key definitions for an entity**  

   There can be a maximum of 5 alternate key definitions for an entity in a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance.  

- **Special characters in key value**

  Nếu dữ liệu trong một trường được sử dụng trong một khóa thay thế chứa một trong các ký tự sau `<`,`>`,`*`,`%`,`&`,`:`,`\\` thì bản vá hoặc hành động upsert sẽ không hoạt động.  If you only need uniqueness then this approach will work, but if you need to use these keys as part of data integration then it is best to create the key on fields that won't have data with those characters.

<a name="BKMK_crud"></a>   

## <a name="retrieve-and-delete-alternate-keys"></a>Retrieve and delete alternate keys  

If you need to retrieve or delete alternate keys, you can use the customization UI to do this, without writing any code. However, the SDK provides the following two messages to programmatically retrieve and delete alternate keys.  

|Message request class|Mô tả|  
|---------------------------|-----------------|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityKeyRequest>|Retrieves the specified alternate key.|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteEntityKeyRequest>|Deletes the specified alternate key.|  

To retrieve all the keys for an entity, use the new <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.Keys> property of `EntityMetadata` (<xref href="Microsoft.Dynamics.CRM.EntityMetadata?text=EntityMetadata EntityType" /> or <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata> class). It gets an array of keys for an entity.  

<a name="BKMK_index"></a>   

## <a name="monitor-index-creation-for-alternate-keys"></a>Monitor index creation for alternate keys  

Alternate keys use database indexes to enforce uniqueness and optimize lookup performance. If there are lots of existing records in a table, index creation can be a lengthy process. You can increase the responsiveness of the customization UI and solution import by doing the index creation as a background process. The `EntityKeyMetadata.AsyncJob` property (<xref href="Microsoft.Dynamics.CRM.EntityKeyMetadata?text=EntityKeyMetadata EntityType" /> or <xref:Microsoft.Xrm.Sdk.Metadata.EntityKeyMetadata>) refers to the asynchronous job that is doing the index creation. The `EntityKeyMetadata.EntityKeyIndexStatus` property specifies the status of the key as its index creation job progresses. The status could be any of the following:  

- Pending  
- Đang Tiến hành  
- Hoạt động  
- Không thành công  

When an alternate key is created using the API, if the index creation fails, you can drill into details about the cause of the failure, correct the problems, and reactivate the key request using the `ReactivateEntityKey` (<xref href="Microsoft.Dynamics.CRM.ReactivateEntityKey?text=ReactivateEntityKey Action" /> or <xref:Microsoft.Xrm.Sdk.Messages.ReactivateEntityKeyRequest> message).  

If the alternate key is deleted while an index creation job is still pending or in progress, the job is cancelled and the index is deleted.  

### <a name="see-also"></a>Xem thêm  
 [Using alternate keys](use-alternate-key-create-record.md)<br />
 [Use change tracking to synchronize data with external systems](use-change-tracking-synchronize-data-external-systems.md)<br />
 [Use Upsert to insert or update a record](use-upsert-insert-update-record.md)