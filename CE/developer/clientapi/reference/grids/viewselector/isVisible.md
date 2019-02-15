---
title: isVisible (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d22cd046-064c-47ef-9e46-5cc4c8b6e280
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7e6b825078d268ebc1f1c9644b1fb4febe811511
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387164"
---
# <a name="isvisible-client-api-reference"></a>isVisible (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/isVisible-description.md](./includes/isVisible-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only grid

## <a name="syntax"></a>Cú pháp

`viewSelector.isVisible();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: true if visible; false otherwise.

## <a name="remarks"></a>Chú thích

If the subgrid control is not configured to display the view selector, calling this method on the **ViewSelector** returned by the GridControl.getViewSelector method will throw an error.

To get the `viewSelector` object, see [ViewSelector](../viewselector.md).



