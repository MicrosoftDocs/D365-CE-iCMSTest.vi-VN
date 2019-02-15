---
title: removeOption (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 09fd288c-d687-4976-b708-29a466fc35b1
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d571691e848b7aaffc2fc2f8463d3b3eec9f386e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388061"
---
# <a name="removeoption-client-api-reference"></a>removeOption (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Removes an option from a control. 

## <a name="control-types-supported"></a>Control types supported

optionset, multiselectoptionset

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).removeOption(value);`

## <a name="parameters"></a>Tham số

|Tên | Loại | Bắt buộc | Mô tả|
|--|--|--|--|
|giá trị |Số |Có|The value of the option you want to remove.|

### <a name="related-topics"></a>Chủ đề liên quan

[addOption](addOption.md)

[clearOptions](clearOptions.md)

 


