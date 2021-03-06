---
title: formContext.ui.sections (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about working with processes in Customer Engagement using client API.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e362dfb2-cb64-49f5-b3d4-d77e813325ca
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2a301f58e0bd9b42c9ddae4b5f53c11c704d4c9d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385490"
---
# <a name="formcontextuisections-client-api-reference"></a>formContext.ui.sections (Client API reference)

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

A section contains methods to manage how it appears as well as accessing the tab that contains the section.

You can retrieve a section object (say **sectionObj**) by using the following example code:

```JavaScript
var tabObj = formContext.ui.tabs.get(arg);
var sectionObj = tabObj.sections.get(arg);
```

## <a name="properties"></a>Thuộc tính

- **Controls**: The section controls collection provides access to the controls within a section. See [Collections (Client API reference)](collections.md) for information about the methods exposed by collections. See [Controls (Client API reference)](controls.md) for information about the properties and methods exposed by the objects in this collection.


## <a name="methods"></a>Phương pháp

|                        Tên                         |                                                            Mô tả                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
|   [getLabel](formcontext-ui-sections/getLabel.md)   |   [!INCLUDE[formcontext-ui-sections/includes/getLabel-description.md](formcontext-ui-sections/includes/getLabel-description.md)]   |
|    [getName](formcontext-ui-sections/getName.md)    |    [!INCLUDE[formcontext-ui-sections/includes/getName-description.md](formcontext-ui-sections/includes/getName-description.md)]    |
|  [getParent](formcontext-ui-sections/getParent.md)  |  [!INCLUDE[formcontext-ui-sections/includes/getParent-description.md](formcontext-ui-sections/includes/getParent-description.md)]  |
| [getVisible](formcontext-ui-sections/getVisible.md) | [!INCLUDE[formcontext-ui-sections/includes/getVisible-description.md](formcontext-ui-sections/includes/getVisible-description.md)] |
|   [setLabel](formcontext-ui-sections/setLabel.md)   |   [!INCLUDE[formcontext-ui-sections/includes/setLabel-description.md](formcontext-ui-sections/includes/setLabel-description.md)]   |
| [setVisible](formcontext-ui-sections/setVisible.md) | [!INCLUDE[formcontext-ui-sections/includes/setVisible-description.md](formcontext-ui-sections/includes/setVisible-description.md)] |

### <a name="related-topics"></a>Chủ đề liên quan

[formcontext.ui.tabs](formcontext-ui-tabs.md)

[formContext](../clientapi-form-context.md)
