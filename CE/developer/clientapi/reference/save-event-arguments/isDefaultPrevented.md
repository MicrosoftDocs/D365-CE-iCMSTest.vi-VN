---
title: isDefaultPrevented (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9a8802ad-80aa-4386-a192-573280587546
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 06c0f34f4971ad95c31ff9c2377f499d6198003f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386728"
---
# <a name="isdefaultprevented-client-api-reference"></a>isDefaultPrevented (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/isDefaultPrevented-description.md](./includes/isDefaultPrevented-description.md)]

## <a name="syntax"></a>Cú pháp

`executionContext.getEventArgs().isDefaultPrevented();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: **true** if the save event has been canceled because the preventDefault method was used; **false** otherwise.


### <a name="related-topics"></a>Chủ đề liên quan

[getSaveMode](getSaveMode.md)

[preventDefault](preventDefault.md)

