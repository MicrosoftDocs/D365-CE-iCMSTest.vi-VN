---
title: getViewPortHeight (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e19af732-01e8-4853-b81c-40d79192cea2
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b1315f80a72b1bbf844ab1c7f383fd5a8a8f3c61
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387071"
---
# <a name="getviewportheight-client-api-reference"></a>getViewPortHeight (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getViewPortHeight-description.md](./includes/getViewPortHeight-description.md)]

The viewport is the area of the page containing form data. It corresponds to the body of the form and does not include the navigation, header, footer or form assistant areas of the page.

## <a name="syntax"></a>Cú pháp

`formContext.ui.getViewPortHeight();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: The viewport height in pixels. 


### <a name="related-topics"></a>Chủ đề liên quan

[getViewPortWidth](getViewPortWidth.md)

[formContext.ui](../formContext-ui.md)

[formContext](../../clientapi-form-context.md)

