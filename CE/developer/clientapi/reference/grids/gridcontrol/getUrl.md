---
title: getUrl (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: f2023d7d-5877-4436-abe6-e81ca68b8ec0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 952e8bb90d2e81988657e980217d6f97a8a2e903
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386370"
---
# <a name="geturl-client-api-reference"></a>getUrl (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getUrl-description.md](./includes/getUrl-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`gridContext.getUrl(client);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|client|Số|Không|Indicates the client type. Bạn có thể chỉ định một trong các giá trị sau:<br/>0: Browser<br/>1: MobileApplication|

## <a name="return-value"></a>Giá trị trả lại

**Type**: String

**Description**: The Url of the current grid control.

## <a name="remarks"></a>Chú thích

To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).



