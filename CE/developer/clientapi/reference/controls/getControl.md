---
title: getControl (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 34715e1f-35c0-4b7f-971e-e0a6518f0722
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4f0188a2475e08873bc4c01d58121e1ea219cc2a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387004"
---
# <a name="getcontrol-client-api-reference"></a>getControl (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Gets a control on the form. 

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg);`

The **formContext.getControl(arg)** method is a shortcut method to access **formContext.ui.controls.get**.

## <a name="parameter"></a>Tham số

**arg**: Optional. You can access a control on a form by passing an argument as either the **name** or the **index valu**e of the control on a form. For example: `formContext.getControl("firstname")` or `formContext.getControl(0)`


## <a name="return-value"></a>Giá trị trả lại

**Type**: Object or Object collection.

**Description**: Object if you use the method with parameter; object collection if you use the method without any parameters.



### <a name="related-topics"></a>Chủ đề liên quan

[formContext](../../clientapi-form-Context.md)



