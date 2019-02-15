---
title: formContext.data.entity (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 32e8d1d0-4093-4588-a517-2930eec34dce
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 652dcc4f0c4b6c19c026f3d045299660f82e603e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388617"
---
# <a name="formcontextdataentity-client-api-reference"></a>formContext.data.entity (Client API reference)

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

Provides properties and methods to retrieve information specific to the record displayed on the page, the save method, and a collection of all the attributes included in the form. Attribute data is limited to attributes represented by fields on the form.

## <a name="properties"></a>Thuộc tính

|Tên|Mô tả|
|--|--|
|attributes|Collection of attributes for a record displayed on the form. <br/>More information: [Collections](collections.md) and [Attributes](attributes.md).

## <a name="methods"></a>Phương pháp

|                                      Tên                                       |                                                                          Mô tả                                                                           |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                [addOnSave](formContext-data-entity/addOnSave.md)                |                [!INCLUDE[formContext-data-entity/includes/addOnSave-description.md](formContext-data-entity/includes/addOnSave-description.md)]                |
|               [getDataXml](formContext-data-entity/getDataXml.md)               |               [!INCLUDE[formContext-data-entity/includes/getDataXml-description.md](formContext-data-entity/includes/getDataXml-description.md)]               |
|            [getEntityName](formContext-data-entity/getEntityName.md)            |            [!INCLUDE[formContext-data-entity/includes/getEntityName-description.md](formContext-data-entity/includes/getEntityName-description.md)]            |
|       [getEntityReference](formContext-data-entity/getEntityReference.md)       |       [!INCLUDE[formContext-data-entity/includes/getEntityReference-description.md](formContext-data-entity/includes/getEntityReference-description.md)]       |
|                    [getId](formContext-data-entity/getId.md)                    |                    [!INCLUDE[formContext-data-entity/includes/getId-description.md](formContext-data-entity/includes/getId-description.md)]                    |
|               [getIsDirty](formContext-data-entity/getIsDirty.md)               |               [!INCLUDE[formContext-data-entity/includes/getIsDirty-description.md](formContext-data-entity/includes/getIsDirty-description.md)]               |
| [getPrimaryAttributeValue](formContext-data-entity/getPrimaryAttributeValue.md) | [!INCLUDE[formContext-data-entity/includes/getPrimaryAttributeValue-description.md](formContext-data-entity/includes/getPrimaryAttributeValue-description.md)] |
|                  [isValid](formContext-data-entity/isValid.md)                  |                  [!INCLUDE[formContext-data-entity/includes/isValid-description.md](formContext-data-entity/includes/isValid-description.md)]                  |
|             [removeOnSave](formContext-data-entity/removeOnSave.md)             |             [!INCLUDE[formContext-data-entity/includes/removeOnSave-description.md](formContext-data-entity/includes/removeOnSave-description.md)]             |
|                     [save](formContext-data-entity/save.md)                     |                     [!INCLUDE[formContext-data-entity/includes/save-description.md](formContext-data-entity/includes/save-description.md)]                     |

### <a name="related-topics"></a>Chủ đề liên quan

[Understand Xrm object model](../understand-clientapi-object-model.md)

[Controls (Client API reference)](controls.md)




