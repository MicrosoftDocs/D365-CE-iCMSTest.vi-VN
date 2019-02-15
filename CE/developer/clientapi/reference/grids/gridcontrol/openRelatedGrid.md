---
title: openRelatedGrid (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: b7e5e7fb60b6779edcb694283ffcb84c41f576b0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387606"
---
# <a name="openrelatedgrid-client-api-reference"></a>openRelatedGrid (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openRelatedGrid-description.md](./includes/openRelatedGrid-description.md)]

This method does nothing if the grid is not filtered based on a relationship.

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`gridContext.openRelatedGrid();`

## <a name="remarks"></a>Chú thích

To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).

### <a name="related-topics"></a>Chủ đề liên quan

[getRelationship](getRelationship.md)

[Customize entity relationship metadata](../../../../customize-entity-relationship-metadata.md) 




