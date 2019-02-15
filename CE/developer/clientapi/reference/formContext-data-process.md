---
title: formContext.data.process (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about working with processes in Customer Engagement using client API.
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 32e8d1d0-4093-4588-a517-2930eec34dce
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5091c321c92dbe2d9459fde8d62975ea3850308f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386717"
---
# <a name="formcontextdataprocess-client-api-reference"></a><span data-ttu-id="85d42-103">formContext.data.process (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="85d42-103">formContext.data.process (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="85d42-104">Provides events, methods, and objects to interact with the business process flow data on a form.</span><span class="sxs-lookup"><span data-stu-id="85d42-104">Provides events, methods, and objects to interact with the business process flow data on a form.</span></span> <span data-ttu-id="85d42-105">See [formContext.ui.process (Client API reference)](formContext-ui-process.md) for methods to interact with the business process flow control on the form.</span><span class="sxs-lookup"><span data-stu-id="85d42-105">See [formContext.ui.process (Client API reference)](formContext-ui-process.md) for methods to interact with the business process flow control on the form.</span></span>

## <a name="process-events-and-event-handler-methods"></a><span data-ttu-id="85d42-106">Process events and event handler methods</span><span class="sxs-lookup"><span data-stu-id="85d42-106">Process events and event handler methods</span></span>

<span data-ttu-id="85d42-107">Use the following events and event handler methods to write scripts for business process flows.</span><span class="sxs-lookup"><span data-stu-id="85d42-107">Use the following events and event handler methods to write scripts for business process flows.</span></span>

|<span data-ttu-id="85d42-108">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="85d42-108">Event</span></span> | <span data-ttu-id="85d42-109">Event handler methods</span><span class="sxs-lookup"><span data-stu-id="85d42-109">Event handler methods</span></span>|
|--|--|
|[<span data-ttu-id="85d42-110">OnProcessStatusChange</span><span class="sxs-lookup"><span data-stu-id="85d42-110">OnProcessStatusChange</span></span>](events/onprocessstatuschange.md)|[<span data-ttu-id="85d42-111">addOnProcessStatusChange</span><span class="sxs-lookup"><span data-stu-id="85d42-111">addOnProcessStatusChange</span></span>](formContext-data-process/eventhandlers/addOnProcessStatusChange.md)<br/>[<span data-ttu-id="85d42-112">removeOnProcessStatusChange</span><span class="sxs-lookup"><span data-stu-id="85d42-112">removeOnProcessStatusChange</span></span>](formContext-data-process/eventhandlers/removeOnProcessStatusChange.md)|
|[<span data-ttu-id="85d42-113">OnStageChange</span><span class="sxs-lookup"><span data-stu-id="85d42-113">OnStageChange</span></span>](events/OnStageChange.md)|[<span data-ttu-id="85d42-114">addOnStageChange</span><span class="sxs-lookup"><span data-stu-id="85d42-114">addOnStageChange</span></span>](formContext-data-process/eventhandlers/addOnStageChange.md)<br/>[<span data-ttu-id="85d42-115">removeOnStageChange</span><span class="sxs-lookup"><span data-stu-id="85d42-115">removeOnStageChange</span></span>](formContext-data-process/eventhandlers/removeOnStageChange.md)|
|[<span data-ttu-id="85d42-116">OnStageSelected</span><span class="sxs-lookup"><span data-stu-id="85d42-116">OnStageSelected</span></span>](events/OnStageSelected.md)|[<span data-ttu-id="85d42-117">addOnStageSelected</span><span class="sxs-lookup"><span data-stu-id="85d42-117">addOnStageSelected</span></span>](formContext-data-process/eventhandlers/addOnStageSelected.md)<br/>[<span data-ttu-id="85d42-118">removeOnStageSelected</span><span class="sxs-lookup"><span data-stu-id="85d42-118">removeOnStageSelected</span></span>](formContext-data-process/eventhandlers/removeOnStageSelected.md)|

## <a name="active-process-methods"></a><span data-ttu-id="85d42-119">Active Process methods</span><span class="sxs-lookup"><span data-stu-id="85d42-119">Active Process methods</span></span>

<span data-ttu-id="85d42-120">Use these methods to retrieve information about the active process and set a different process as the active process.</span><span class="sxs-lookup"><span data-stu-id="85d42-120">Use these methods to retrieve information about the active process and set a different process as the active process.</span></span>


|                                      <span data-ttu-id="85d42-121">Tên</span><span class="sxs-lookup"><span data-stu-id="85d42-121">Name</span></span>                                      |                                                                                 <span data-ttu-id="85d42-122">Mô tả</span><span class="sxs-lookup"><span data-stu-id="85d42-122">Description</span></span>                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85d42-123">getActiveProcess</span><span class="sxs-lookup"><span data-stu-id="85d42-123">getActiveProcess</span></span>](formcontext-data-process/activeprocess/getActiveProcess.md) | [!INCLUDE[formcontext-data-process/activeprocess/includes/getActiveProcess-description.md](formcontext-data-process/activeprocess/includes/getActiveProcess-description.md)] |
| [<span data-ttu-id="85d42-124">setActiveProcess</span><span class="sxs-lookup"><span data-stu-id="85d42-124">setActiveProcess</span></span>](formcontext-data-process/activeprocess/setActiveProcess.md) | [!INCLUDE[formcontext-data-process/activeprocess/includes/setActiveProcess-description.md](formcontext-data-process/activeprocess/includes/setActiveProcess-description.md)] |

## <a name="process-methods"></a><span data-ttu-id="85d42-125">Process methods</span><span class="sxs-lookup"><span data-stu-id="85d42-125">Process methods</span></span> 

<span data-ttu-id="85d42-126">A process contains the data for a business process flow.</span><span class="sxs-lookup"><span data-stu-id="85d42-126">A process contains the data for a business process flow.</span></span> <span data-ttu-id="85d42-127">Use the methods to access properties of the process.</span><span class="sxs-lookup"><span data-stu-id="85d42-127">Use the methods to access properties of the process.</span></span>


|                             <span data-ttu-id="85d42-128">Tên</span><span class="sxs-lookup"><span data-stu-id="85d42-128">Name</span></span>                             |                                                                     <span data-ttu-id="85d42-129">Mô tả</span><span class="sxs-lookup"><span data-stu-id="85d42-129">Description</span></span>                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|      [<span data-ttu-id="85d42-130">getId</span><span class="sxs-lookup"><span data-stu-id="85d42-130">getId</span></span>](formcontext-data-process/process/getId.md)      |      [!INCLUDE[formcontext-data-process/process/includes/getId-description.md](formcontext-data-process/process/includes/getId-description.md)]      |
|    [<span data-ttu-id="85d42-131">getName</span><span class="sxs-lookup"><span data-stu-id="85d42-131">getName</span></span>](formcontext-data-process/process/getName.md)    |    [!INCLUDE[formcontext-data-process/process/includes/getName-description.md](formcontext-data-process/process/includes/getName-description.md)]    |
|  [<span data-ttu-id="85d42-132">getStages</span><span class="sxs-lookup"><span data-stu-id="85d42-132">getStages</span></span>](formcontext-data-process/process/getStages.md)  |  [!INCLUDE[formcontext-data-process/process/includes/getStages-description.md](formcontext-data-process/process/includes/getStages-description.md)]  |
| [<span data-ttu-id="85d42-133">isRendered</span><span class="sxs-lookup"><span data-stu-id="85d42-133">isRendered</span></span>](formcontext-data-process/process/isRendered.md) | [!INCLUDE[formcontext-data-process/process/includes/isRendered-description.md](formcontext-data-process/process/includes/isRendered-description.md)] |

## <a name="processinstance-methods"></a><span data-ttu-id="85d42-134">ProcessInstance methods</span><span class="sxs-lookup"><span data-stu-id="85d42-134">ProcessInstance methods</span></span>

<span data-ttu-id="85d42-135">Use these methods to retrieve information about all the process instances for an entity record and to set a process instance as the active instance.</span><span class="sxs-lookup"><span data-stu-id="85d42-135">Use these methods to retrieve information about all the process instances for an entity record and to set a process instance as the active instance.</span></span>


|                                       <span data-ttu-id="85d42-136">Tên</span><span class="sxs-lookup"><span data-stu-id="85d42-136">Name</span></span>                                       |                                                                           <span data-ttu-id="85d42-137">Mô tả</span><span class="sxs-lookup"><span data-stu-id="85d42-137">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|      [<span data-ttu-id="85d42-138">getProcessInstances</span><span class="sxs-lookup"><span data-stu-id="85d42-138">getProcessInstances</span></span>](formContext-data-process/getProcessInstances.md)      |      [!INCLUDE[formcontext-data-process/includes/getProcessInstances-description.md](formcontext-data-process/includes/getProcessInstances-description.md)]      |
| [<span data-ttu-id="85d42-139">setActiveProcessInstance</span><span class="sxs-lookup"><span data-stu-id="85d42-139">setActiveProcessInstance</span></span>](formContext-data-process/setActiveProcessInstance.md) | [!INCLUDE[formcontext-data-process/includes/setActiveProcessInstance-description.md](formcontext-data-process/includes/setActiveProcessInstance-description.md)] |

## <a name="instance-methods"></a><span data-ttu-id="85d42-140">Instance methods</span><span class="sxs-lookup"><span data-stu-id="85d42-140">Instance methods</span></span> 

<span data-ttu-id="85d42-141">A process instance contains the data for an instance of the business process flow.</span><span class="sxs-lookup"><span data-stu-id="85d42-141">A process instance contains the data for an instance of the business process flow.</span></span> <span data-ttu-id="85d42-142">Use the methods to access properties of the process instance.</span><span class="sxs-lookup"><span data-stu-id="85d42-142">Use the methods to access properties of the process instance.</span></span>


|                                  <span data-ttu-id="85d42-143">Tên</span><span class="sxs-lookup"><span data-stu-id="85d42-143">Name</span></span>                                   |                                                                           <span data-ttu-id="85d42-144">Mô tả</span><span class="sxs-lookup"><span data-stu-id="85d42-144">Description</span></span>                                                                            |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   [<span data-ttu-id="85d42-145">getInstanceId</span><span class="sxs-lookup"><span data-stu-id="85d42-145">getInstanceId</span></span>](formcontext-data-process/instance/getInstanceId.md)   |   [!INCLUDE[formcontext-data-process/instance/includes/getInstanceId-description.md](formcontext-data-process/instance/includes/getInstanceId-description.md)]   |
| [<span data-ttu-id="85d42-146">getInstanceName</span><span class="sxs-lookup"><span data-stu-id="85d42-146">getInstanceName</span></span>](formcontext-data-process/instance/getInstanceName.md) | [!INCLUDE[formcontext-data-process/instance/includes/getInstanceName-description.md](formcontext-data-process/instance/includes/getInstanceName-description.md)] |
|       [<span data-ttu-id="85d42-147">getStatus</span><span class="sxs-lookup"><span data-stu-id="85d42-147">getStatus</span></span>](formcontext-data-process/instance/getStatus.md)       |       [!INCLUDE[formcontext-data-process/instance/includes/getStatus-description.md](formcontext-data-process/instance/includes/getStatus-description.md)]       |
|       [<span data-ttu-id="85d42-148">setStatus</span><span class="sxs-lookup"><span data-stu-id="85d42-148">setStatus</span></span>](formcontext-data-process/instance/setStatus.md)       |       [!INCLUDE[formcontext-data-process/instance/includes/setStatus-description.md](formcontext-data-process/instance/includes/setStatus-description.md)]       |

## <a name="active-stage-methods"></a><span data-ttu-id="85d42-149">Active Stage methods</span><span class="sxs-lookup"><span data-stu-id="85d42-149">Active Stage methods</span></span>

<span data-ttu-id="85d42-150">Use these methods to retrieve information about the active stage and set a different stage as the active stage.</span><span class="sxs-lookup"><span data-stu-id="85d42-150">Use these methods to retrieve information about the active stage and set a different stage as the active stage.</span></span>


|                                   <span data-ttu-id="85d42-151">Tên</span><span class="sxs-lookup"><span data-stu-id="85d42-151">Name</span></span>                                   |                                                                             <span data-ttu-id="85d42-152">Mô tả</span><span class="sxs-lookup"><span data-stu-id="85d42-152">Description</span></span>                                                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85d42-153">getActiveStage</span><span class="sxs-lookup"><span data-stu-id="85d42-153">getActiveStage</span></span>](formcontext-data-process/activestage/getActiveStage.md) | [!INCLUDE[formcontext-data-process/activestage/includes/getActiveStage-description.md](formcontext-data-process/activestage/includes/getActiveStage-description.md)] |
| [<span data-ttu-id="85d42-154">setActiveStage</span><span class="sxs-lookup"><span data-stu-id="85d42-154">setActiveStage</span></span>](formcontext-data-process/activestage/setActiveStage.md) | [!INCLUDE[formcontext-data-process/activestage/includes/setActiveStage-description.md](formcontext-data-process/activestage/includes/setActiveStage-description.md)] |

## <a name="stage-methods"></a><span data-ttu-id="85d42-155">Stage methods</span><span class="sxs-lookup"><span data-stu-id="85d42-155">Stage methods</span></span> 

<span data-ttu-id="85d42-156">A stage contains the data for a stage in a business process flow.</span><span class="sxs-lookup"><span data-stu-id="85d42-156">A stage contains the data for a stage in a business process flow.</span></span> <span data-ttu-id="85d42-157">Use the methods to access properties of the stage.</span><span class="sxs-lookup"><span data-stu-id="85d42-157">Use the methods to access properties of the stage.</span></span>

|                                       <span data-ttu-id="85d42-158">Tên</span><span class="sxs-lookup"><span data-stu-id="85d42-158">Name</span></span>                                       |                                                                              <span data-ttu-id="85d42-159">Mô tả</span><span class="sxs-lookup"><span data-stu-id="85d42-159">Description</span></span>                                                                               |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           [<span data-ttu-id="85d42-160">getCategory</span><span class="sxs-lookup"><span data-stu-id="85d42-160">getCategory</span></span>](formcontext-data-process/stage/getCategory.md)           |           [!INCLUDE[formcontext-data-process/stage/includes/getCategory-description.md](formcontext-data-process/stage/includes/getCategory-description.md)]           |
|         [<span data-ttu-id="85d42-161">getEntityName</span><span class="sxs-lookup"><span data-stu-id="85d42-161">getEntityName</span></span>](formcontext-data-process/stage/getEntityName.md)         |         [!INCLUDE[formcontext-data-process/stage/includes/getEntityName-description.md](formcontext-data-process/stage/includes/getEntityName-description.md)]         |
|                 [<span data-ttu-id="85d42-162">getId</span><span class="sxs-lookup"><span data-stu-id="85d42-162">getId</span></span>](formcontext-data-process/stage/getId.md)                 |                 [!INCLUDE[formcontext-data-process/stage/includes/getId-description.md](formcontext-data-process/stage/includes/getId-description.md)]                 |
|               [<span data-ttu-id="85d42-163">getName</span><span class="sxs-lookup"><span data-stu-id="85d42-163">getName</span></span>](formcontext-data-process/stage/getName.md)               |               [!INCLUDE[formcontext-data-process/stage/includes/getName-description.md](formcontext-data-process/stage/includes/getName-description.md)]               |
| [<span data-ttu-id="85d42-164">getNavigationBehavior</span><span class="sxs-lookup"><span data-stu-id="85d42-164">getNavigationBehavior</span></span>](formcontext-data-process/stage/getNavigationBehavior.md) | [!INCLUDE[formcontext-data-process/stage/includes/getNavigationBehavior-description.md](formcontext-data-process/stage/includes/getNavigationBehavior-description.md)] |
|             [<span data-ttu-id="85d42-165">getStatus</span><span class="sxs-lookup"><span data-stu-id="85d42-165">getStatus</span></span>](formcontext-data-process/stage/getStatus.md)             |             [!INCLUDE[formcontext-data-process/stage/includes/getStatus-description.md](formcontext-data-process/stage/includes/getStatus-description.md)]             |
|              [<span data-ttu-id="85d42-166">getSteps</span><span class="sxs-lookup"><span data-stu-id="85d42-166">getSteps</span></span>](formcontext-data-process/stage/getSteps.md)              |              [!INCLUDE[formcontext-data-process/stage/includes/getSteps-description.md](formcontext-data-process/stage/includes/getSteps-description.md)]              |

## <a name="step-methods"></a><span data-ttu-id="85d42-167">Step methods</span><span class="sxs-lookup"><span data-stu-id="85d42-167">Step methods</span></span>

<span data-ttu-id="85d42-168">A step contains the data for a step in a stage in a business process flow.</span><span class="sxs-lookup"><span data-stu-id="85d42-168">A step contains the data for a step in a stage in a business process flow.</span></span> <span data-ttu-id="85d42-169">Use the methods to access properties of the step.</span><span class="sxs-lookup"><span data-stu-id="85d42-169">Use the methods to access properties of the step.</span></span>


|                             <span data-ttu-id="85d42-170">Tên</span><span class="sxs-lookup"><span data-stu-id="85d42-170">Name</span></span>                              |                                                                    <span data-ttu-id="85d42-171">Mô tả</span><span class="sxs-lookup"><span data-stu-id="85d42-171">Description</span></span>                                                                     |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85d42-172">getAttribute</span><span class="sxs-lookup"><span data-stu-id="85d42-172">getAttribute</span></span>](formcontext-data-process/step/getAttribute.md) | [!INCLUDE[formcontext-data-process/step/includes/getAttribute-description.md](formcontext-data-process/step/includes/getAttribute-description.md)] |
|      [<span data-ttu-id="85d42-173">getName</span><span class="sxs-lookup"><span data-stu-id="85d42-173">getName</span></span>](formcontext-data-process/step/getName.md)      |      [!INCLUDE[formcontext-data-process/step/includes/getName-description.md](formcontext-data-process/step/includes/getName-description.md)]      |
|  [<span data-ttu-id="85d42-174">getProgress</span><span class="sxs-lookup"><span data-stu-id="85d42-174">getProgress</span></span>](formcontext-data-process/step/getProgress.md)  |  [!INCLUDE[formcontext-data-process/step/includes/getProgress-description.md](formcontext-data-process/step/includes/getProgress-description.md)]  |
|   [<span data-ttu-id="85d42-175">isRequired</span><span class="sxs-lookup"><span data-stu-id="85d42-175">isRequired</span></span>](formcontext-data-process/step/isRequired.md)   |   [!INCLUDE[formcontext-data-process/step/includes/isRequired-description.md](formcontext-data-process/step/includes/isRequired-description.md)]   |
|  [<span data-ttu-id="85d42-176">setProgress</span><span class="sxs-lookup"><span data-stu-id="85d42-176">setProgress</span></span>](formcontext-data-process/step/setProgress.md)  |  [!INCLUDE[formcontext-data-process/step/includes/setProgress-description.md](formcontext-data-process/step/includes/setProgress-description.md)]  |

## <a name="navigation-methods"></a><span data-ttu-id="85d42-177">Navigation methods</span><span class="sxs-lookup"><span data-stu-id="85d42-177">Navigation methods</span></span>

<span data-ttu-id="85d42-178">Use these methods to move to next and previous stages.</span><span class="sxs-lookup"><span data-stu-id="85d42-178">Use these methods to move to next and previous stages.</span></span> <span data-ttu-id="85d42-179">Both these methods will cause the OnStageChange event to occur.</span><span class="sxs-lookup"><span data-stu-id="85d42-179">Both these methods will cause the OnStageChange event to occur.</span></span>


|                                <span data-ttu-id="85d42-180">Tên</span><span class="sxs-lookup"><span data-stu-id="85d42-180">Name</span></span>                                 |                                                                          <span data-ttu-id="85d42-181">Mô tả</span><span class="sxs-lookup"><span data-stu-id="85d42-181">Description</span></span>                                                                           |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     [<span data-ttu-id="85d42-182">moveNext</span><span class="sxs-lookup"><span data-stu-id="85d42-182">moveNext</span></span>](formContext-data-process/navigation/moveNext.md)     |     [!INCLUDE[formcontext-data-process/navigation/includes/moveNext-description.md](formcontext-data-process/navigation/includes/moveNext-description.md)]     |
| [<span data-ttu-id="85d42-183">movePrevious</span><span class="sxs-lookup"><span data-stu-id="85d42-183">movePrevious</span></span>](formContext-data-process/navigation/movePrevious.md) | [!INCLUDE[formcontext-data-process/navigation/includes/movePrevious-description.md](formcontext-data-process/navigation/includes/movePrevious-description.md)] |

## <a name="other-useful-methods"></a><span data-ttu-id="85d42-184">Other useful methods</span><span class="sxs-lookup"><span data-stu-id="85d42-184">Other useful methods</span></span>

<span data-ttu-id="85d42-185">Use these methods to find information about the stages in the active path, enabled processes, and selected stage.</span><span class="sxs-lookup"><span data-stu-id="85d42-185">Use these methods to find information about the stages in the active path, enabled processes, and selected stage.</span></span>


|                                  <span data-ttu-id="85d42-186">Tên</span><span class="sxs-lookup"><span data-stu-id="85d42-186">Name</span></span>                                  |                                                                           <span data-ttu-id="85d42-187">Mô tả</span><span class="sxs-lookup"><span data-stu-id="85d42-187">Description</span></span>                                                                            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85d42-188">getActivePath</span><span class="sxs-lookup"><span data-stu-id="85d42-188">getActivePath</span></span>](formContext-data-process/activepath/getActivePath.md)  | [!INCLUDE[formcontext-data-process/activepath/includes/getActivePath-description.md](formcontext-data-process/activepath/includes/getActivePath-description.md)] |
| [<span data-ttu-id="85d42-189">getEnabledProcesses</span><span class="sxs-lookup"><span data-stu-id="85d42-189">getEnabledProcesses</span></span>](formContext-data-process/getEnabledProcesses.md) |      [!INCLUDE[formcontext-data-process/includes/getEnabledProcesses-description.md](formcontext-data-process/includes/getEnabledProcesses-description.md)]      |
|    [<span data-ttu-id="85d42-190">getSelectedStage</span><span class="sxs-lookup"><span data-stu-id="85d42-190">getSelectedStage</span></span>](formContext-data-process/getSelectedStage.md)    |         [!INCLUDE[formcontext-data-process/includes/getSelectedStage-description.md](formcontext-data-process/includes/getSelectedStage-description.md)]         |

### <a name="related-topics"></a><span data-ttu-id="85d42-191">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="85d42-191">Related topics</span></span>

[<span data-ttu-id="85d42-192">formContext.ui.process (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="85d42-192">formContext.ui.process (Client API reference)</span></span>](formContext-ui-process.md)

[<span data-ttu-id="85d42-193">Understand Xrm object model</span><span class="sxs-lookup"><span data-stu-id="85d42-193">Understand Xrm object model</span></span>](../understand-clientapi-object-model.md)

[<span data-ttu-id="85d42-194">Controls (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="85d42-194">Controls (Client API reference)</span></span>](controls.md)




