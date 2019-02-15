---
title: setActiveStage (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9c40a770-f4cb-4230-8893-0527f8472825
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ed51f7f759398a8e4d6286d2dbcb942c8d1c1dea
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385660"
---
# <a name="setactivestage-client-api-reference"></a>setActiveStage (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setActiveStage-description.md](./includes/setActiveStage-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.process.setActiveStage(stageId, callbackFunction);`

## <a name="parameters"></a>Tham số

<table style="width:100%">
<tr>
<th>Tên</th>
<th>Loại</th>
<th>Bắt buộc</th>
<th>Mô tả</th>
</tr>
<tr>
<td>stageId</td>
<td>Chuỗi</td>
<td>Có</td>
<td>The ID of the completed stage for the entity to make the active stage. </td>
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
<td>invalid</td>
<td>There are three reasons why this value may be returned:
<ul>
<li>The <em>stageId</em> parameter is a non-existent stage ID value.</li>
<li>The active stage isn’t the selected stage.</li>
<li>The record hasn’t been saved yet.</li>
</ul>
</td>
</tr>
<tr>
<td>unreachable</td>
<td>The stage exists on a different path.</td>
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
>This method can only be used when the selected stage and the active stage are the same. When your code is initiated from the [OnStageChange](../../events/onstagechange.md) event, the current stage will be selected. When your code is initiated from the [OnStageSelected](../../events/onstageselected.md) event, you should use the [getActiveStage](getActiveStage.md) method to verify that the selected stage is also the active stage. For any other form event, it isn’t possible to determine which stage is currently selected. For best results, this method should only be used in code that is called in functions initiated by the [OnStageChange](../../events/onstagechange.md) and [OnStageSelected](../../events/onstageselected.md) events.

### <a name="related-topics"></a>Chủ đề liên quan

[getActiveStage](getActiveStage.md)

[formContext.data.process](../../formContext-data-process.md)
 


