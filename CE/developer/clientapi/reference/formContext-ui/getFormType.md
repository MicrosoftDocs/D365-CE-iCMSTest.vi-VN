---
title: getFormType (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 6c57db71-a76d-404c-852e-9c36a1c549ee
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 549107d174a59d394c43727c6e26e0e9024a4fad
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387331"
---
# <a name="getformtype-client-api-reference"></a>getFormType (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getFormType-description.md](./includes/getFormType-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.ui.getFormType();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number

**Description**: Form type. Returns one of the following values 

|Value |Loại biểu mẫu |
|---|---|
|0|Undefined|
|1|Tạo|
|2|Update|
|3|Read Only|
|4|Đã vô hiệu hóa|
|6|Bulk Edit|

>[!NOTE]
>Quick Create forms return 1.


### <a name="related-topics"></a>Chủ đề liên quan

[formContext.ui](../formContext-ui.md)

[formContext](../../clientapi-form-context.md)

