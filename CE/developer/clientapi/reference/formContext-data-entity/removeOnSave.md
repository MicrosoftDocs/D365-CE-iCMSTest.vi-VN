---
title: removeOnSave (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 14a92f7c-f4c0-475d-8797-dcbb283db37a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 31fd555f410d24a5b4faf6e1d08bddb2d69e0749
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386636"
---
# <a name="removeonsave-client-api-reference"></a>removeOnSave (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/removeOnSave-description.md](./includes/removeOnSave-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.entity.removeOnSave(myFunction)`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|myFunction|function reference|Có|The function to be removed for the **OnSave** event.

### <a name="related-topics"></a>Chủ đề liên quan

[addOnSave](addOnSave.md)

[Form OnSave event](../events/form-onsave.md)

