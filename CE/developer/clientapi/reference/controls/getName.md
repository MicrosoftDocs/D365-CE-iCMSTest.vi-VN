---
title: getName (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: cacd309c0853370ecd55725bf892249f9e313cfd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387458"
---
# <a name="getname-client-api-reference"></a>getName (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns the name assigned to the control.

>[!NOTE]
>The name assigned to a control is not determined until the form loads. Changes to the form may change the name assigned to a given control. 

## <a name="control-types-supported"></a>Control types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).getName();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: The name of the control.

### <a name="related-topics"></a>Chủ đề liên quan

[Kiểm soát](../controls.md)

