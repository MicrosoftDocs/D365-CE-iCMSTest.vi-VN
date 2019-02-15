---
title: getCurrentView (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
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
ms.openlocfilehash: 7a5e469eb586a39898afa6d1e6169682eeb0d877
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386398"
---
# <a name="getcurrentview-client-api-reference"></a>getCurrentView (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getCurrentView-description.md](./includes/getCurrentView-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only grid

## <a name="syntax"></a>Cú pháp

`viewSelector.getCurrentView();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Lookup object

**Description**: The Lookup object has the following attributes:

- **entityType**: Number. The object type code for the SavedQuery (1039) or UserQuery (4230) that represents the view the user can select.
- **id**: String. The Id for the view the user can select.
- **name**: String. The name of the view the user can select.

## <a name="remarks"></a>Chú thích

If the subgrid control is not configured to display the view selector, calling this method on the `viewSelector` object will throw an error.

To get the `viewSelector` object, see [ViewSelector](../viewselector.md).



