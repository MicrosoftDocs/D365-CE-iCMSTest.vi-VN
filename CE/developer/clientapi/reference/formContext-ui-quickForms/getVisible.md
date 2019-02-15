---
title: getVisible (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 72c7ec48-1d27-499c-b56c-b7a449a347b8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0320d9fdbc60838a17b43d9603df528f346dde60
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385489"
---
# <a name="getvisible-client-api-reference"></a>getVisible (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getVisible-description.md](./includes/getVisible-description.md)]

>[!NOTE]
>If the containing **section** or **tab** for this control isn’t visible, this method can still return **true**. To make certain that the control is actually visible; you need to also check the visibility of the containing elements.

## <a name="syntax"></a>Cú pháp

`quickViewControl.getVisible();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean.

**Description**: true if the control is visible; false otherwise.

### <a name="related-topics"></a>Chủ đề liên quan

[setVisible](setVisible.md)

[formContext.ui.quickForms](../formContext-ui-quickForms.md)



