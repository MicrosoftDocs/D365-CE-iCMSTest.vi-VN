---
title: getFormat (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e5f97552-4a48-4bf9-b460-6105442e2e6b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e32b057e9812a2b55104e8811adaaf2fee515efd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387299"
---
# <a name="getformat-client-api-reference"></a>getFormat (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Returns a string value that represents formatting options for the attribute. 

## <a name="attribute-types-supported"></a>Attribute types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getAttribute(arg).getFormat()`

## <a name="return-value"></a>Giá trị trả lại

This method will return one of the following **string** values or "null":

- ngày
- ngày giờ
- duration
- email
- language
- không
- Điện thoại 
- văn bản
- textarea
- tickersymbol
- timezone
- url

> [!NOTE]
> This format information generally represents the format options of the application field. Format options for Boolean fields are not provided.

The following table lists the format string values to expect for each type of attribute schema type and format option.

| Application Field Type | Tùy chọn định dạng | Attribute Type | Format Value|
|----------------------------|-------------------|--------------------|------------------|
| Date and Time              | Chỉ Ngày         | ngày giờ           | ngày             |
| Date and Time              | Date and Time     | ngày giờ           | ngày giờ         |
| Số Nguyên               | Khoảng thời gian          | số nguyên            | duration         |
| Single Line of Text        | Email            | chuỗi             | email            |
| Số Nguyên               | Language          | optionset          | language         |
| Số Nguyên               | Không có              | số nguyên            | không             |
| Single Line of Text        | Khu vực văn bản         | chuỗi             | textarea         |
| Single Line of Text        | Text              | chuỗi             | văn bản             |
| Single Line of Text        | Ký hiệu Chứng khoán     | chuỗi             | tickersymbol     |
| Single Line of Text        | Số điện thoại             | chuỗi             | Điện thoại             |
| Số Nguyên               | Múi giờ         | optionset          | timezone         |
| Single Line of Text        | Url               | chuỗi             | url 
