---
title: setDefaultView (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 8c918cd4-d0ce-45e5-91a3-1addf11258c7
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ee8ad9e6eb3c293566479346bb64ebfb146b5617
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386393"
---
# <a name="setdefaultview-client-api-reference"></a>setDefaultView (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Sets the default view for the lookup control dialog box.

## <a name="control-types-supported"></a>Control types supported

Tra cứu

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).setDefaultView(viewId);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|viewId|Chuỗi|Có|The ID of the view to be set as the default view.|

## <a name="example"></a>Ví dụ

This **setDefaultViewSample** function will set the **account** entity form primary contact lookup default view to the **My Active Contacts** view.

```JavaScript
function setDefaultViewSample(executionContext) {
    var formContext = executionContext.getFormContext();
    formContext.getControl("primarycontactid").setDefaultView("{00000000-0000-0000-00AA-000010001003}");
}
```

### <a name="related-topics"></a>Chủ đề liên quan

[getDefaultView](getDefaultView.md) 


