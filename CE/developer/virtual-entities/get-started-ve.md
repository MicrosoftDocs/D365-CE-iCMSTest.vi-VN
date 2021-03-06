---
title: Get started with virtual entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 14c5fbbc-98db-4e49-b245-2c84c1cd11cd
author: jimdaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e9df717f01e5ceed63bc6a41025d802d78f1b775
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387052"
---
# <a name="get-started-with-virtual-entities"></a>Get started with virtual entities

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

Starting with the [!INCLUDE[pn-crm-9-0-0-online](../../includes/pn-crm-9-0-0-online.md)], virtual entities enable the integration of data residing in external systems by seamlessly representing that data as entities in Dynamics 365 for Customer Engagement apps, without replication of data and often without custom coding. The initial implementation of this feature provides just read-only support for such entities, and has a number of other limitations described in the section [Limitations of Virtual Entities](#limitations-of-virtual-entities) below. Besides these limitations, virtual entities behave the same as other custom entities. 

Virtual entities replace previous client-side and server-side approaches to integrating external data, which required customized code and suffered from numerous limitations, including imperfect integration, data duplication, or extensive commitment of development resources.  In addition, for administrators and system customizers, the use of virtual entities greatly simplifies administration and configuration.

This section discusses the implications of virtual entities for developers. For more information about managing virtual entities from the user interface, see [Create and edit virtual entities](../../customize/create-edit-virtual-entities.md). 

## <a name="virtual-entities-data-providers-and-data-sources"></a>Virtual entities, data providers and data sources
A virtual entity is a definition of an entity in the [!INCLUDE[pn-dynamics365](../../includes/pn-dynamics-365.md)] for Customer Engagement apps platform metadata without the associated physical tables for entity instances created in the [!INCLUDE[pn-dynamics365](../../includes/pn-dynamics-365.md)] for Customer Engagement apps database. Instead during runtime, when an entity instance is required, its state is dynamically retrieved from the associated external system. Each virtual entity type is associated with a *virtual entity data provider* and (optionally) some configuration information from an associated *virtual entity data source*. 

A data provider is a particular type of [!INCLUDE[pn-dynamics365](../../includes/pn-dynamics-365.md)] [plugin](../plugin-development.md), which is registered against CRUD events that occur in the platform. This initial release only supports READ operations. 

The following data providers ship with [!INCLUDE[pn-crm-9-0-0-online](../../includes/pn-crm-9-0-0-online.md)]:
- An [OData v4](http://www.odata.org/documentation/) provider is included with the service and is installed by default.
- An [Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db) (formerly _Microsoft Document DB_) provider is available from [AppSource](https://appsource.microsoft.com).

Additional providers will be made available by Microsoft, its partners, or other third parties. If a data provider cannot be found for your external data source, you can develop a _custom virtual entity data provider_; for more information, see [Virtual entity data providers](custom-ve-data-providers.md).

## <a name="virtual-entity-creation-and-mapping"></a>Virtual entity creation and mapping
Initially, defining a virtual entity is the same as defining a custom entity: you specify the entity, attributes, and relationships for the new virtual entity type. However, additionally, you then connect the virtual entity to a data provider to manage data retrieval. The custom entity type and its fields must be mapped to the corresponding data in the external data source.  For example, a virtual entity might be represented as a row in an external relational database, and each of its fields might correspond to a column in that row.  (Note that these external data names are often different than their corresponding virtual entity names.) A specific, required mapping occurs for the entity ID field: the data provider must be able to provide this GUID and associate it to the external record that represents this entity instance. The most direct way to achieve this is to actually use GUIDs as primary keys in the external data source.  

In this example, a corresponding virtual entity data source would also be provided to supply user and connection information for the external database.

## <a name="limitations-of-virtual-entities"></a>Limitations of Virtual Entities
In this release, there are some limitations to virtual entities that you need to be aware of when evaluating whether you can use virtual entities with your external data.
- Data is read-only. The virtual entity feature doesn’t support pushing changes made in [!INCLUDE[pn-dynamics365](../../includes/pn-dynamics-365.md)] for Customer Engagement apps back to the external system.
- Only organization-owned entities are supported. The security filtering applied to user-owned entities is not supported. Access to the virtual entity data can be turned on or off for individual users based on their security role. Field-level security is not supported.
- It must be possible to model the external data as a [!INCLUDE[pn-dynamics365](../../includes/pn-dynamics-365.md)] for Customer Engagement apps entity. This means:
  - All entities in the external data source must have an associated GUID primary key.  
  - All entity properties must be represented as [!INCLUDE[pn-dynamics365](../../includes/pn-dynamics-365.md)] for Customer Engagement apps attributes. You can use simple types representing text, numbers, optionsets, dates, images, and lookups. 
  - You must be able to model any entity relationships in [!INCLUDE[pn-dynamics365](../../includes/pn-dynamics-365.md)] for Customer Engagement apps.
  - An attribute on a virtual entity cannot be calculated or rollup.  Any desired calculations must be done on the external side, possibly within or directed by the data provider.

- Auditing and change tracking is not supported.  These may be implemented within the external data store.
- Virtual entities cannot be enabled for queues.
- Offline caching of values is not supported for virtual entities.
- A virtual entity cannot represent an activity and do not support business process flows.
- Once created, a virtual entity cannot be changed to be a standard (non-virtual) entity.  The reverse is also true: a standard entity cannot be converted into a virtual entity.

<!-- TODO: Make bulleted list into table.  Make more complete by reviewing API modification tables. -->

For more information about how these limitations are reflected in the [!INCLUDE[pn-dynamics365](../../includes/pn-dynamics-365.md)] for Customer Engagement apps API, see [API considerations of virtual entities](api-considerations-ve.md). 
