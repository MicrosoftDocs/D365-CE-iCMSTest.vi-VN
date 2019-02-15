---
title: getDisplayState (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 21368fac-d4bc-4f75-8a9c-cce098fa0b45
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5ebff46b252015e19f6b925163f67ac0bbf0f55d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386064"
---
# <a name="getdisplaystate-client-api-reference"></a>getDisplayState (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getDisplayState-description.md](./includes/getDisplayState-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.ui.process.getDisplayState();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: String.

**Description**: Returns "expanded" or "collapsed" on the web client; returns "expanded", "collapsed", or "floating" on Unified Interface.

### <a name="related-topics"></a>Chủ đề liên quan

[setDisplayState](setDisplayState.md)

[formContext.ui.process](../formContext-ui-process.md)



