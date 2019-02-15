---
title: getControlType (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 61ae1c58e11465fbec6b3d2a008474cfc284c95b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386719"
---
# <a name="getcontroltype-client-api-reference"></a>getControlType (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a value that categorizes controls.

## <a name="control-types-supported"></a>Control Types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`getControl(arg).getControlType();`

**Return Value**:

**Type**: String

|Giá trị trả lại |Decsription|
|--|--|
|standard|A standard control|
|iframe|An IFRAME control|
|kbsearch|A knowledge base search control|
|lookup|A lookup control|
|multiselectoptionset|A multi-select option set control|
|notes|A notes control|
|optionset|An option set control|
|quickform | A [quick view](../formContext-ui-quickForms.md) control|
|subgrid | A [subgrid](../grids.md) control|
|timercontrol | A timer control|
|timelinewall | A timeline control (for Unified Interface)|
|webresource | A web resource control|
|customcontrol: \<*namespace*>.\<*name*> | A custom control for Dynamics 365 for Customer Engagement apps mobile clients (phones and tablets)|
|customsubgrid:\<*namespace*>.\<*name*> | A custom dataset control for Dynamics 365 for Customer Engagement apps mobile clients (phones and tablets)|

### <a name="related-topics"></a>Chủ đề liên quan

[Kiểm soát](../controls.md)

[getControl](getcontrol.md)


