---
title: getControl (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 57eb6b4b-90c1-4d56-b4b0-a7160af17f8f
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7ebd48530ec457d1450d586131d44a526829a0bc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388134"
---
# <a name="getcontrol-client-api-reference"></a>getControl (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getControl-description.md](./includes/getControl-description.md)]

## <a name="syntax"></a>Cú pháp

`quickViewControl.getControl(arg);`

## <a name="parameter"></a>Tham số

**arg**: Optional. You can access a single control in the constituent controls collection by passing an argument as either the name or the index value of the constituent control in a quick view control. For example: `quickViewControl.getControl("firstname")` or `quickViewControl.getControl(0)`


## <a name="return-value"></a>Giá trị trả lại

**Type**: Object or Object collection.

**Description**: Object if you use the method with parameter; object collection if you use the method without any parameters.

## <a name="remarks"></a>Chú thích

After you have retrieved a constituent control in a quick view control, you can use any of the methods supported for a control in Customer Engagement on the constituent control that does not alter the constituent control data. This is because constituent controls in a quick view control are read only. For example, you can use: 

`quickViewControl.getControl(0).getAttribute()` 

For more information about methods supported for a control, see [Controls](../controls.md).

> [!IMPORTANT]
> The [getAttribute](../controls/getAttribute.md) or any data related methods on a constituent control might not work on the main form [OnLoad](../events/form-onload.md) event because the quick view form that its bound to might not have loaded completely when the main form has loaded. You must use the [isLoaded](isLoaded.md) method for the quick view control instance to help you determine if the bounded quick view form has loaded completely. 
> 
> Also, the way you retrieve constituent controls in a quick view control on forms using the new form rendering engine is different from the legacy forms. So, if you are using legacy forms and have code targeting constituent controls in a quick view control, you must update your code when you decide to use the new form rendering engine.

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.ui.quickForms](../formContext-ui-quickForms.md)



