---
title: refreshRibbon (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: dbd43d7b-c9b0-4ca5-943d-dd813d3bb049
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5794e54c34b8f69b1b656f4d27122efe3a6d2db0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387448"
---
# <a name="refreshribbon-client-api-reference"></a>refreshRibbon (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/refreshRibbon-description.md](./includes/refreshRibbon-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.ui.refreshRibbon(refreshAll);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|refreshAll|Boolean|Không|Indicates whether all the ribbon command bars on the current page are refreshed. If you specify **false**, only the page-level ribbon command bar is refreshed. If you do not specify this parameter, by default **false** is passed.|

## <a name="remarks"></a>Chú thích

 This function is typically used when a ribbon <EnableRule> (RibbonDiffXml) depends on a value in the form. After your code changes a value that is used by a rule, use this method to force the ribbon to re-evaluate the data in the form so that the rule can be applied.

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.ui](../formContext-ui.md)

[formContext](../../clientapi-form-context.md)

