---
title: setVisible (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 485d9843-5907-49e4-971b-0e86f3bd1eb8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d005ad5f4ed5a2d272a3866b5ff0bfd8a07d16fc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387233"
---
# <a name="setvisible-client-api-reference"></a>setVisible (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setVisible-description.md](./includes/setVisible-description.md)] 

## <a name="syntax"></a>Cú pháp

`tabObj.setVisible(bool);`

## <a name="parameter"></a>Tham số

|Tên|Loại|Bắt buộc|Mô tả|
|--|--|--|--|
|bool|Boolean|Có|Specify **true** to show the tab; **false** to hide the tab.|

## <a name="remarks"></a>Chú thích

Another way to hide a tab is to hide all the sections within it. If all the sections within a tab are not visible, the tab will not be visible.

### <a name="related-topics"></a>Chủ đề liên quan

[getVisible](getVisible.md)



