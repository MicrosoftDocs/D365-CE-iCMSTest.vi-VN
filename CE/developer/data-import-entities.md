---
title: Data import entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Lists the data import entities used to create data maps, configure and run data imports, and log failure information.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- data import entities, for configuring and running data imports
- data import entities, for creating data maps
- creating data maps; and configuring and running data imports, entities for
- entities for data importing
- data import entities
- data import entities, for obtaining logs for information about data import failures
ms.assetid: e18c1e40-0c9a-417b-a7de-3c13b68128ca
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 941afd2d90d377d25f5621922fbba9cb3e50b996
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387359"
---
# <a name="data-import-entities"></a>Data import entities

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

The [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] data import entities are used to create data maps, configure and run data imports, and log failure information.  

 The following table lists the entities that are used to configure, run, and log failures for import operations.  

|Entity name (display name)|Mô tả|  
|----------------------------------|-----------------|  
|import (data import)|Status and ownership information for the import job.|  
|importfile (import source file)|Logical source file.|  
|importlog (import log)|Failure reason and other detailed information for a record that failed to import.|  

 The following table lists the entities that are used for creating data maps.  


|                    Entity name (display name)                     |                                                                                                                      Mô tả                                                                                                                       |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                       importmap (data map)                        |                                                                                                           Data map that is used for import.                                                                                                            |
|                  columnmapping (column mapping)                   |                                                           Mapping between a column in the source file and a target attribute in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].                                                           |
|                  lookupmapping (lookup mapping)                   |       Mapping between a column in the source file, or an output of a complex transformation and a target attribute of type <xref:Microsoft.Xrm.Sdk.EntityReference>. Used in conjunction with column mapping or complex transformation mapping.        |
|                   ownermapping (owner mapping)                    |                                                             Mapping between a user specified in the source file and a user in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].                                                             |
|                picklistmapping (picklist mapping)                 | Mapping between a column in the source file and a target attribute of <xref:Microsoft.Xrm.Sdk.OptionSetValue>, Boolean, state, or status type in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)]. Used in conjunction with column mapping. |
|          transformationmapping (transformation mapping)           |                                                                                                            Complex transformation mapping.                                                                                                             |
| transformationparametermapping (transformation parameter mapping) |                                                                                           Parameter mapping that is used in complex transformation mapping.                                                                                            |

### <a name="see-also"></a>Xem thêm  
 [Import Data in Dynamics 365 for Customer Engagement](import-data.md)   
 [Import Entity](entities/import.md)   
 [ImportFile Entity](entities/importfile.md)   
 [ImportLog Entity](entities/importlog.md)   
 [ImportMap Entity](entities/importmap.md)   
 <!-- jdaly These links will have content when we re-gen docs after bug 689487 is checked in. START --> [ColumnMapping Entity](entities/columnmapping.md)   
 [LookupMapping Entity](entities/lookupmapping.md)   
 [OwnerMapping Entity](entities/ownermapping.md)   
 [PicklistMapping Entity](entities/picklistmapping.md)   
 [TransformationMapping Entity](entities/transformationmapping.md)    
 [TransformationParameterMapping Entity](entities/transformationparametermapping.md)   
 <!-- jdaly These links will have content  when we re-gen docs after bug 689487 is checked in. END --> [Sample: Export and Import a Data Map](sample-export-import-data-map.md)   
