---
title: getCategory (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 2849a9e1-b2fb-464c-8fc7-90b0df027c86
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0729f6861804036ca1abba59f3c20ec107ed3262
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385525"
---
# <a name="getcategory-client-api-reference"></a>getCategory (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getCategory-description.md](./includes/getCategory-description.md)]

## <a name="syntax"></a>Cú pháp

`var stageCategoryNumber = stageObj.getCategory().getValue();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Number. 

**Description**: Here is the list of possible values.

|Value |Mô tả|
|--|--|
|0|Bao gồm|
|1|Phát triển|
|2|Đề xuất|
|3|Đóng|
|4|Identify|
|5|Research|
|6|Resolve|

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.data.process](../../formContext-data-process.md)
 


