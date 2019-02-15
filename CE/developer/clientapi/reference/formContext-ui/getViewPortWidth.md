---
title: getViewPortWidth (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: f769c0cc017902a55aad2d23af011b476dd9fa10
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387691"
---
# <a name="getviewportwidth-client-api-reference"></a>getViewPortWidth (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getViewPortWidth-description.md](./includes/getViewPortWidth-description.md)]

The viewport is the area of the page containing form data. It corresponds to the body of the form and does not include the navigation, header, footer or form assistant areas of the page.

## <a name="syntax"></a>Cú pháp

`formContext.ui.getViewPortWidth();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: The viewport width in pixels. 


### <a name="related-topics"></a>Chủ đề liên quan

[getViewPortHeight](getViewPortHeight.md)

[formContext.ui](../formContext-ui.md)

[formContext](../../clientapi-form-context.md)

