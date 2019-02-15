---
title: formContext.data (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about working with data on the form using client API.
ms.date: 08/08/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 32e8d1d0-4093-4588-a517-2930eec34dce
author: KumarVivek
ms.author: kvivek
manager: annbe
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a0b714bfce91a643940fc2abb85b411ebb7700ce
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387325"
---
# <a name="formcontextdata-client-api-reference"></a>formContext.data (Client API reference)

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

Provides properties and methods to work with the data on a form.

![formContext Data object model](../../media/ClientAPI-formContext-data-Model.png)

## <a name="properties"></a>Thuộc tính

|Tên|Mô tả|
|--|--|
|attributes|Collection of non-entity data on the form. Items in this collection are of the same type as the attributes collection, but they are not attributes of the form entity. <br/>More information: [Collections](collections.md)<br/>**NOTE:** This is supported only for [Unified Interface](../../../admin/about-unified-interface.md) clients.|
|thực thể|Provides methods to retrieve information specific to the record displayed on the page, the save method, and a collection of all the attributes included on the form. Attribute data is limited to attributes represented by fields on the form. <br/>More information: [formContext.data.entity](formContext-data-entity.md)|
|process|Provides objects and methods to interact with the business process flow data on a form.<br/>More information: [formContext.data.process](formContext-data-process.md)|


## <a name="methods"></a>Phương pháp 

|                       Tên                       |                                                       Mô tả                                                        |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
|    [addOnLoad](formContext-data/addOnload.md)    |    [!INCLUDE[formContext-data/includes/addOnLoad-description.md](formContext-data/includes/addOnLoad-description.md)]    |
|   [getIsDirty](formContext-data/getIsDirty.md)   |   [!INCLUDE[formContext-data/includes/getIsDirty-description.md](formContext-data/includes/getIsDirty-description.md)]   |
|      [isValid](formContext-data/isValid.md)      |      [!INCLUDE[formContext-data/includes/isValid-description.md](formContext-data/includes/isValid-description.md)]      |
|      [refresh](formContext-data/refresh.md)      |      [!INCLUDE[formContext-data/includes/refresh-description.md](formContext-data/includes/refresh-description.md)]      |
| [removeOnLoad](formContext-data/removeOnLoad.md) | [!INCLUDE[formContext-data/includes/removeOnLoad-description.md](formContext-data/includes/removeOnLoad-description.md)] |
|         [save](formContext-data/save.md)         |         [!INCLUDE[formContext-data/includes/save-description.md](formContext-data/includes/save-description.md)]         |

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.data.entity](formContext-data-entity.md)

[formContext.data.process](formContext-data-process.md)




