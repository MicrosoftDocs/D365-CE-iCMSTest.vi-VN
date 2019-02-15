---
title: OnStageSelected Event (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1ef0f11c-6188-4492-ae61-260a402223b8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a0f4a89d6642d95b14505a2c5daca9bd27cac8cf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386273"
---
# <a name="onstageselected-event-client-api-reference"></a>OnStageSelected Event (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

This event occurs when a stage of a business process flow control is selected. You can’t cancel the stage selection using code in a handler for this event.

You can use the [getEventArgs](../executioncontext/getEventArgs.md) method to retrieve an object that has the following method:

**getStage**: Returns a stage object representing the selected stage. More information: [Stage methods](../formContext-data-process.md#stage-methods).

## <a name="methods-supported-for-this-event"></a>Methods supported for this event
- **formContext.data.process**.[addOnStageSelected](../formcontext-data-process/eventhandlers/addOnStageSelected.md) method to add event handlers for this event.
- **formContext.data.process**.[removeOnStageSelected](../formcontext-data-process/eventhandlers/addOnStageSelected.md) method to remove event handlers for this event. 



