---
title: getSelectedStage (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: ac9a8c97-ad4d-4ed8-8eb0-51b2693253dc
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: cc1d2ad2282f29a7917ddf6c9f36b7c340d2e28e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388580"
---
# <a name="getselectedstage-client-api-reference"></a>getSelectedStage (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getSelectedStage-description.md](./includes/getSelectedStage-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.process.getSelectedStage();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Stage. 

**Description**: The currently selected stage. See [Stage methods](../formContext-data-process.md#stage-methods) for the methods to access the properties of the stage returned.

### <a name="related-topics"></a>Chủ đề liên quan

[getActiveStage (Client API reference)](activestage/getActiveStage.md)

[formContext.data.process](../formContext-data-process.md)
 


