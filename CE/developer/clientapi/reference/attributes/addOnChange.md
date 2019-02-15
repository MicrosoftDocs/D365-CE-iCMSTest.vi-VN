---
title: addOnChange (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about the attribute addOnchange method to set a function to be called when the attribute value is changed.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9f3b2fed-fde5-46e4-8c59-43aa51aa82df
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 618f353e679cf0f6f220b0eaec77fb961f86c735
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385792"
---
# <a name="addonchange-client-api-reference"></a>addOnChange (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Sets a function to be called when the **OnChange** event occurs.

## <a name="attribute-types-supported"></a>Attribute types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).addOnChange(myFunction)`

## <a name="parameters"></a>Tham số

| Parameter Name| Loại| Mô tả  |
| --------|-----------| -----|
|myFunction| Function reference| Specifies the function to be executed on the attribute **OnChange** event. The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.|


### <a name="related-topics"></a>Chủ đề liên quan

[removeOnChange](removeOnChange.md)

[Attribute OnChange Event](../events/attribute-onchange.md)





