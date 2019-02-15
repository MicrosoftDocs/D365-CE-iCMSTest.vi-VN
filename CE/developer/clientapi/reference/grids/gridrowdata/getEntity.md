---
title: getEntity (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1672c213-d315-48fb-b49c-47cc19d23c28
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ae23926539bbc2fbd074d29712ea4b63d8d4fb40
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386657"
---
# <a name="getentity-client-api-reference"></a>getEntity (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getEntity-description.md](./includes/getEntity-description.md)]

As this is deprecated, you should use **GridRowData.entity**.

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`gridRowData.getEntity();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: [GridEntity](../gridentity.md)

## <a name="remarks"></a>Chú thích

To get the `gridRowData` object, see [GridRowData](../gridrowdata.md). 

