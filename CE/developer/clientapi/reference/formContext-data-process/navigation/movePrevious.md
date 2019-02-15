---
title: movePrevious (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 649fe7b0-016d-409f-ba3c-b14e0f1953e0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 536fc17d8e4970726651a6bf910c2d14bc80f488
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386332"
---
# <a name="moveprevious-client-api-reference"></a>movePrevious (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/movePrevious-description.md](./includes/movePrevious-description.md)]

You can also move to a previous stage in a different entity.

## <a name="syntax"></a>Cú pháp

`formContext.data.process.movePrevious(callbackFunction);`

## <a name="parameters"></a>Tham số

<table style="width:100%">
<tr>
<th>Tên</th>
<th>Loại</th>
<th>Bắt buộc</th>
<th>Mô tả</th>
</tr>
<tr>
<td>callbackFunction</td>
<td>Hàm</td>
<td>Không</td>
<td>A function to call when the operation is complete. This callback function is passed one of the following string values to indicate the status of the operation:
<table>
<tr>
<th>Value</th>
<th>Reason</th>
</tr>
<tr>
<td>success</td>
<td>The operation succeeded.</td>
</tr>
<tr>
<td>crossEntity</td>
<td>The previous stage is for a different entity.</td>
</tr>
<tr>
<td>beginning</td>
<td>The active stage is the first stage of the active path.</td>
</tr>
<tr>
<td>invalid</td>
<td>The operation failed because the selected stage isn’t the same as the active stage.</td>
</tr>
<tr>
<td>dirtyForm</td>
<td>This value will be returned if the data in the page is not saved.</td>
</tr>
</table>
</td>
</tr>
</table>

>[!IMPORTANT]
>This method can only be used when the selected stage and the active stage are the same. When your code is initiated from the [OnStageChange](../../events/onstagechange.md) event, the current stage will be selected. When your code is initiated from the [OnStageSelected](../../events/onstageselected.md) event, you should use the [getActiveStage](../activestage/getActiveStage.md) method to verify that the selected stage is also the active stage. For any other form event, it isn’t possible to determine which stage is currently selected. For best results, this method should only be used in code that is called in functions initiated by the [OnStageChange](../../events/onstagechange.md) and [OnStageSelected](../../events/onstageselected.md) events.

## <a name="remarks"></a>Chú thích

This methods will cause the [OnStageChange](../../events/onstagechange.md) event to occur.

### <a name="related-topics"></a>Chủ đề liên quan

[moveNext](moveNext.md)

[formContext.data.process](../../formContext-data-process.md)
 


