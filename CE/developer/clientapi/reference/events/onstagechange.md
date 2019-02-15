---
title: OnStageChange Event (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 0c85fe34-1368-4d0d-87eb-4109206ce4f7
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c2bb36670cd638e20a89016f9743c36c23ad7621
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388445"
---
# <a name="onstagechange-event-client-api-reference"></a><span data-ttu-id="8b91a-102">OnStageChange Event (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="8b91a-102">OnStageChange Event (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8b91a-103">This event occurs when the stage of a business process flow control changes.</span><span class="sxs-lookup"><span data-stu-id="8b91a-103">This event occurs when the stage of a business process flow control changes.</span></span> <span data-ttu-id="8b91a-104">This event occurs when the user clicks the **Next Stage** or **Move to previous stage** buttons in the user interface or when a developer uses the `formContext.data.process.moveNext` or `formContext.data.process.movePrevious` methods.</span><span class="sxs-lookup"><span data-stu-id="8b91a-104">This event occurs when the user clicks the **Next Stage** or **Move to previous stage** buttons in the user interface or when a developer uses the `formContext.data.process.moveNext` or `formContext.data.process.movePrevious` methods.</span></span> <span data-ttu-id="8b91a-105">You can’t cancel the stage change using code in a handler for this event.</span><span class="sxs-lookup"><span data-stu-id="8b91a-105">You can’t cancel the stage change using code in a handler for this event.</span></span>

<span data-ttu-id="8b91a-106">An execution context object is passed to event handlers for this event.</span><span class="sxs-lookup"><span data-stu-id="8b91a-106">An execution context object is passed to event handlers for this event.</span></span> <span data-ttu-id="8b91a-107">You can use the [getEventArgs](../executioncontext/getEventArgs.md) method to retrieve an object that has the following methods:</span><span class="sxs-lookup"><span data-stu-id="8b91a-107">You can use the [getEventArgs](../executioncontext/getEventArgs.md) method to retrieve an object that has the following methods:</span></span>
- <span data-ttu-id="8b91a-108">**getDirection**: Returns a string that is either “next” or “previous” to show the direction of the stage change.</span><span class="sxs-lookup"><span data-stu-id="8b91a-108">**getDirection**: Returns a string that is either “next” or “previous” to show the direction of the stage change.</span></span>
- <span data-ttu-id="8b91a-109">**getStage**: Returns a stage object.</span><span class="sxs-lookup"><span data-stu-id="8b91a-109">**getStage**: Returns a stage object.</span></span> <span data-ttu-id="8b91a-110">Except when the navigation moves to a new entity, the stage returned represents the destination stage object,that is, the next active stage.</span><span class="sxs-lookup"><span data-stu-id="8b91a-110">Except when the navigation moves to a new entity, the stage returned represents the destination stage object,that is, the next active stage.</span></span> <span data-ttu-id="8b91a-111">When the navigation moves to a new entity, the stage is the stage being navigated from, that is, the previous active stage object.</span><span class="sxs-lookup"><span data-stu-id="8b91a-111">When the navigation moves to a new entity, the stage is the stage being navigated from, that is, the previous active stage object.</span></span> <span data-ttu-id="8b91a-112">More information: [Stage methods](../formContext-data-process.md#stage-methods).</span><span class="sxs-lookup"><span data-stu-id="8b91a-112">More information: [Stage methods](../formContext-data-process.md#stage-methods).</span></span>

## <a name="methods-supported-for-this-event"></a><span data-ttu-id="8b91a-113">Methods supported for this event</span><span class="sxs-lookup"><span data-stu-id="8b91a-113">Methods supported for this event</span></span>
- <span data-ttu-id="8b91a-114">**formContext.data.process**.[addOnStageChange](../formcontext-data-process/eventhandlers/addOnStageChange.md) method to add event handlers for this event.</span><span class="sxs-lookup"><span data-stu-id="8b91a-114">**formContext.data.process**.[addOnStageChange](../formcontext-data-process/eventhandlers/addOnStageChange.md) method to add event handlers for this event.</span></span>
- <span data-ttu-id="8b91a-115">**formContext.data.process**.[removeOnStageChange](../formcontext-data-process/eventhandlers/removeOnStageChange.md) method to remove event handlers for this event.</span><span class="sxs-lookup"><span data-stu-id="8b91a-115">**formContext.data.process**.[removeOnStageChange](../formcontext-data-process/eventhandlers/removeOnStageChange.md) method to remove event handlers for this event.</span></span> 



