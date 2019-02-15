---
title: getTotalRecordCount (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 8305f0cb-9959-4429-a721-a864ade4cd35
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0a10f8e6129f25bf5bd1bcaddd5f417e0d783887
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387635"
---
# <a name="gettotalrecordcount-client-api-reference"></a>getTotalRecordCount (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getTotalRecordCount-description.md](./includes/getTotalRecordCount-description.md)]

- When the Dynamics 365 for Outlook client isn’t connected to the server, this number is limited to those records that the user has selected to take offline.
- For Dynamics 365 for Customer Engagement mobile clients, this method will return the number of records in the subgrid.

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`var filteredRecordCount = gridContext.getGrid().getTotalRecordCount();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: Total number of records that match the filter criteria of the view.

## <a name="remarks"></a>Chú thích

To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).

See [Collections (Client API reference)](../../collections.md) for information on the methods available to access data in a collection.