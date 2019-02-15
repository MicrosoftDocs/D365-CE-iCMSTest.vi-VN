---
title: formContext.ui.tabs (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about working with processes in Customer Engagement using client API.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1888a882-7dfc-41a8-9bb4-d693d6046666
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 117512b080f9b36e8f4e84f2ca8e65443144fd90
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385558"
---
# <a name="formcontextuitabs-client-api-reference"></a>formContext.ui.tabs (Client API reference)

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

Thẻ là nhóm các phần trên một trang. It contains properties and methods to manipulate tabs as well as access to sections within the tab through the sections collection.

You can retrieve a tab object (say **tabObj**) by using the following example code:

```JavaScript
var tabObj = formContext.ui.tabs.get(arg);
```

## <a name="properties"></a>Thuộc tính

- **Sections**: The sections collection provides access to sections within the tab. See [Collections (Client API reference)](collections.md) for information about methods to access the sections in the collection. See [formContext.ui section](formContext-ui-sections.md) for information about the properties and methods of the section objects in the collection.

## <a name="methods"></a>Phương pháp

|                                Tên                                 |                                                                  Mô tả                                                                   |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
|    [addTabStateChange](formcontext-ui-tabs/addTabStateChange.md)    |    [!INCLUDE[formcontext-ui-tabs/includes/addTabStateChange-description.md](formcontext-ui-tabs/includes/addTabStateChange-description.md)]    |
|      [getDisplayState](formcontext-ui-tabs/getDisplayState.md)      |      [!INCLUDE[formcontext-ui-tabs/includes/getDisplayState-description.md](formcontext-ui-tabs/includes/getDisplayState-description.md)]      |
|             [getLabel](formcontext-ui-tabs/getLabel.md)             |             [!INCLUDE[formcontext-ui-tabs/includes/getLabel-description.md](formcontext-ui-tabs/includes/getLabel-description.md)]             |
|              [getName](formcontext-ui-tabs/getName.md)              |              [!INCLUDE[formcontext-ui-tabs/includes/getName-description.md](formcontext-ui-tabs/includes/getName-description.md)]              |
|            [getParent](formcontext-ui-tabs/getParent.md)            |            [!INCLUDE[formcontext-ui-tabs/includes/getParent-description.md](formcontext-ui-tabs/includes/getParent-description.md)]            |
|           [getVisible](formcontext-ui-tabs/getVisible.md)           |           [!INCLUDE[formcontext-ui-tabs/includes/getVisible-description.md](formcontext-ui-tabs/includes/getVisible-description.md)]           |
| [removeTabStateChange](formcontext-ui-tabs/removeTabStateChange.md) | [!INCLUDE[formcontext-ui-tabs/includes/removeTabStateChange-description.md](formcontext-ui-tabs/includes/removeTabStateChange-description.md)] |
|      [setDisplayState](formcontext-ui-tabs/setDisplayState.md)      |      [!INCLUDE[formcontext-ui-tabs/includes/setDisplayState-description.md](formcontext-ui-tabs/includes/setDisplayState-description.md)]      |
|             [setFocus](formcontext-ui-tabs/setFocus.md)             |             [!INCLUDE[formcontext-ui-tabs/includes/setFocus-description.md](formcontext-ui-tabs/includes/setFocus-description.md)]             |
|             [setLabel](formcontext-ui-tabs/setLabel.md)             |             [!INCLUDE[formcontext-ui-tabs/includes/setLabel-description.md](formcontext-ui-tabs/includes/setLabel-description.md)]             |
|           [setVisible](formcontext-ui-tabs/setVisible.md)           |           [!INCLUDE[formcontext-ui-tabs/includes/setVisible-description.md](formcontext-ui-tabs/includes/setVisible-description.md)]           |

### <a name="related-topics"></a>Chủ đề liên quan

[formcontext.ui.tabs](formcontext-ui-tabs.md)

[formContext](../clientapi-form-context.md)

