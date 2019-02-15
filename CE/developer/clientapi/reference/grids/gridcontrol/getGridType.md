---
title: getGridType (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a441c08c-df32-433e-b666-4253f2cf878c
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4fd2e200b5b48456e3c89b058b480ec91710c479
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386773"
---
# <a name="getgridtype-client-api-reference"></a>getGridType (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getGridType-description.md](./includes/getGridType-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`var gridType = gridContext.getGridType();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: Returns one of the following values:

|Value |Mô tả |
|--|--|
|1|HomePageGrid|
|2|Subgrid|

## <a name="remarks"></a>Chú thích

To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext). 


