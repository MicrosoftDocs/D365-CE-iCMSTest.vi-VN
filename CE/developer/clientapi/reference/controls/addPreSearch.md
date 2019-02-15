---
title: addPreSearch (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d69a432a-1d74-4782-bedd-f9f30d3d7d9c
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 81094aa272839b4dbf7b4778f80a4f4062bc6f66
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388130"
---
# <a name="addpresearch-client-api-reference"></a>addPreSearch (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Applies changes to lookups based on values current just as the user is about to view results for the lookup.

## <a name="control-types-supported"></a>Control types supported

Tra cứu

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).addPreSearch(myFunction)`

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|myFunction |Hàm |Có| The function that will be run just before the search to provide results for a lookup occurs. You can use this function to call one of the other lookup control functions and improve the results to be displayed in the lookup. The [execution context](../../clientapi-execution-context.md) is automatically passed as the first parameter to this function.|

### <a name="related-topics"></a>Chủ đề liên quan

[PreSearch event](../events/PreSearch.md)

[removePreSearch](removePreSearch.md) 


