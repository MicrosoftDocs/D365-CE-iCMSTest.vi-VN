---
title: Form OnSave Event (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
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
ms.openlocfilehash: b35c2c8cc8bd7d893b1262b065a83e2b69153e57
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388813"
---
# <a name="form-onsave-event-client-api-reference-in-dynamics-365-for-customer-engagement-apps"></a>Form OnSave Event (Client API reference) in Dynamics 365 for Customer Engagement apps

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

The `OnSave` event occurs when:
- The user clicks the **Save** icon in the lower right corner of the form, even when there is no changed data to be saved.
- Code executes the [formContext.data.entity.save](../formContext-data-entity/save.md) method, even when there is no changed data to be saved.
- The user navigates away from the form and there is unsaved data in the form.
- The auto-save option is enabled, 30 seconds after data has changed and there is unsaved data in the form.
- Code executes the [formContext.data.save](../formContext-data/save.md) method and there is unsaved data in the form.
- Code executes the [formContext.data.refresh](../formContext-data/refresh.md) method passing a true value as the first parameter and there is unsaved data in the form.

To determine which button was clicked to perform the save, use the getSaveMode method.

You can cancel the save action by using the preventDefault method within the event arguments object. The preventDefault method which is accessible by using the getEventArgs method that is part of the execution context. Execution context is automatically passed to the form event handler.

### <a name="related-topic"></a>Related topic
[Grid OnSave Event](grid-onsave.md)  