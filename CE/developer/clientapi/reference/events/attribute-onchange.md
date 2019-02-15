---
title: Attribute OnChange Event in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bc70916a06ee5ae79a5b5e7ac914857138af89fc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386630"
---
# <a name="attribute-onchange-event-client-api-reference"></a>Attribute OnChange Event (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

The `OnChange` event occurs in the following situations:
- Data in a form field has changed and focus is lost. There is an exception to this behavior that applies to Two-Option (Boolean) fields that are formatted to use radio buttons or check boxes. In these cases the event occurs immediately.
- Data changes on the server are retrieved to update a field when the form is refreshed, such as after a record is saved.
- The attribute.[fireOnchange](../attributes/fireOnChange.md) method is used.

All fields support the `OnChange` event. Data in the field is validated before and after the `OnChange` event.

The `OnChange` event does not occur if the field is changed programmatically using the attribute.[setValue](../attributes/setValue.md) method. If you want event handlers for the `OnChange` event to run after you set the value you must use the `formContext.data.entity attribute.`[fireOnchange](../attributes/fireOnChange.md) method in your code. 

> [!NOTE]
> Although the **Status** field supports the`OnChange` event, the field is read-only on the form so the event cannot occur through user interaction. Another script could cause this event to occur by using the [fireOnchange](../attributes/fireOnChange.md) method on the field.

## <a name="methods-supported-for-this-event"></a>Methods supported for this event
There are three methods you can use to work with the `OnChange` event for an attribute:
- [addOnChange](../attributes/addOnChange.md)
- [fireOnChange](../attributes/fireOnChange.md)
- [removeOnChange](../attributes/removeOnChange.md)

### <a name="related-topics"></a>Chủ đề liên quan
[attributes (Client API reference)](../attributes.md)
 



