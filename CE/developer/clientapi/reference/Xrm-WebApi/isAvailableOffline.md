---
title: isAvailableOffline (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 12/18/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: ea9eacc0-2e31-49f4-a329-dcdf430a5a7e
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 776a21a77781ae016ea1f8a8f39c2d3ac79fded2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387506"
---
# <a name="isavailableoffline-client-api-reference"></a>isAvailableOffline (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/isAvailableOffline-description.md](./includes/isAvailableOffline-description.md)] 

## <a name="syntax"></a>Cú pháp

`Xrm.WebApi.offline.isAvailableOffline(entityLogicalName);`

## <a name="parameters"></a>Tham số

<table style="width:100%">
<tr>
<th>Tên</th>
<th>Loại</th>
<th>Bắt buộc</th>
<th>Mô tả</th>
</tr>
<tr>
<td>entityLogicalName</td>
<td>Chuỗi</td>
<td>Có</td>
<td>Logical name of the entity. For example: &quot;account&quot;.</td>
</tr>

</table>

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean.

**Description**: true if the entity is present in user’s profile and is currently available for use in offline mode; otherwise false.

[Xrm.WebApi.offline](offline.md)

[Xrm.WebApi](../xrm-webapi.md)




