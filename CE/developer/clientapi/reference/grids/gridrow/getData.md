---
title: getData (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 3040281a08a324b5a237a713467ed692b5f6ace4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385969"
---
# <a name="getdata-client-api-reference"></a>getData (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getData-description.md](./includes/getData-description.md)]

As this is deprecated, you should use **GridRow.data**.

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`gridRow.getData();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: [GridRowData](../gridrowdata.md)

## <a name="remarks"></a>Chú thích

To get the `gridRow` object, see [GridRow](../gridrow.md). 

