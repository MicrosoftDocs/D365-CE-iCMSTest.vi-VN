---
title: getActiveStage (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 57a17f91-38f2-4666-bd23-0b7c63b0516f
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4f62bd97a99ff81fa4d5ce2fb1747e0942ea5132
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386778"
---
# <a name="getactivestage-client-api-reference"></a>getActiveStage (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getActiveStage-description.md](./includes/getActiveStage-description.md)]

## <a name="syntax"></a>Cú pháp

`formContext.data.process.getActiveStage();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Stage. 

**Description**: The currently active stage. See [Stage methods](../../formContext-data-process.md#stage-methods) for the methods to access the properties of the stage returned.

### <a name="related-topics"></a>Chủ đề liên quan

[setActiveStage)](setActiveStage.md)

[getSelectedStage (Client API reference)](../getSelectedStage.md)

[formContext.data.process](../../formContext-data-process.md)
 


