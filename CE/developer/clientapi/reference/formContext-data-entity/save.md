---
title: save (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a27f8267-9b24-42b7-a075-420a26db6693
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4d0988e23755397d90c91624c2b8d7fb1a3c6f5d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388181"
---
# <a name="save-client-api-reference"></a>save (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/save-description.md](./includes/save-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.entity.save(saveOption);`

## <a name="parameters"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|saveOption|Chuỗi|Không|Specify options for saving the record. If no parameter is included in the method, the record will simply be saved. This is the equivalent of using the **Save** command.<br/>You can specify one of the following values:<br/><br/>- **saveandclose**: This is the equivalent of using the **Save and Close** command.<br/><br/>- **saveandnew**: This is the equivalent of the using the **Save and New** command.|

## <a name="example"></a>Ví dụ

To open a new form after the save is completed:

`formContext.data.entity.save("saveandnew");`

### <a name="related-topics"></a>Chủ đề liên quan

[formContext.data.save](../formContext-data/save.md)

[formContext](../../clientapi-form-context.md)

