---
title: moveNext (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 97640c6a-816b-4d18-9b0b-e79411787c1a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e2114249ea3b291a3990aeae929dee4673b5f4e8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388389"
---
# <a name="movenext-client-api-reference"></a>moveNext (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/moveNext-description.md](./includes/moveNext-description.md)]

You can also move to a next stage in a different entity. 

## <a name="syntax"></a>Cú pháp

`formContext.data.process.moveNext(callbackFunction);`

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
<td>The next stage is for a different entity.</td>
</tr>
<tr>
<td>end</td>
<td>The active stage is the last stage of the active path.</td>
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

[movePrevious](movePrevious.md)

[formContext.data.process](../../formContext-data-process.md)
 


