---
title: Plug-in registration entities (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Learn about plug-in registration entities that define a Dynamics 365 for Customer Engagement web services (SDK) message, the entities that support a particular message, and the entities used during plug-in registration. These entities do not apply to custom workflow activities. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: bd82dfec-a852-4bb1-8f46-7d574ac50782
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f4d84685eeeafd12ba260285055289710d065889
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386198"
---
# <a name="plug-in-registration-entities"></a><span data-ttu-id="a9ca5-104">Plug-in registration entities</span><span class="sxs-lookup"><span data-stu-id="a9ca5-104">Plug-in registration entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a9ca5-105">The plug-in registration entities define a [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)] message, the entities that support a particular SDK message, and the entities used during plug-in registration.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-105">The plug-in registration entities define a [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)] message, the entities that support a particular SDK message, and the entities used during plug-in registration.</span></span> <span data-ttu-id="a9ca5-106">These entities do not apply to custom workflow activities.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-106">These entities do not apply to custom workflow activities.</span></span>  
  
 <span data-ttu-id="a9ca5-107">An *SDK Message* defines a message to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps platform.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-107">An *SDK Message* defines a message to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps platform.</span></span> <span data-ttu-id="a9ca5-108">The message represents the operation that the platform is to perform.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-108">The message represents the operation that the platform is to perform.</span></span> <span data-ttu-id="a9ca5-109">You should not create or update a record of this entity.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-109">You should not create or update a record of this entity.</span></span>  
  
 <span data-ttu-id="a9ca5-110">An *SDK Message Filter* defines what entity type, for example, account or contact, supports a particular SDK message.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-110">An *SDK Message Filter* defines what entity type, for example, account or contact, supports a particular SDK message.</span></span> <span data-ttu-id="a9ca5-111">It also identifies whether a custom plug-in can be registered for the message and executed when the message is processed by the event execution pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-111">It also identifies whether a custom plug-in can be registered for the message and executed when the message is processed by the event execution pipeline.</span></span>  
  
 <span data-ttu-id="a9ca5-112">The SDK message processing entities are used when registering a plug-in in the event execution pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-112">The SDK message processing entities are used when registering a plug-in in the event execution pipeline.</span></span> <span data-ttu-id="a9ca5-113">An *SDK Message Processing Step* entity identifies the event in the pipeline for which a plug-in should be executed.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-113">An *SDK Message Processing Step* entity identifies the event in the pipeline for which a plug-in should be executed.</span></span> <span data-ttu-id="a9ca5-114">An *SDK Message Processing Step Image* entity stores a snapshot of an entity, including its attributes, during an event that occurs before or after the core platform operation.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-114">An *SDK Message Processing Step Image* entity stores a snapshot of an entity, including its attributes, during an event that occurs before or after the core platform operation.</span></span> <span data-ttu-id="a9ca5-115">An *SDK Message Processing Step Secure Configuration* entity stores secure custom information that is passed to a plug-in’s constructor at run-time.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-115">An *SDK Message Processing Step Secure Configuration* entity stores secure custom information that is passed to a plug-in’s constructor at run-time.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a9ca5-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a9ca5-116">See also</span></span>  
 <span data-ttu-id="a9ca5-117">[Write Plug-Ins to Extend Business Processes](write-plugin-extend-business-processes.md) </span><span class="sxs-lookup"><span data-stu-id="a9ca5-117">[Write Plug-Ins to Extend Business Processes](write-plugin-extend-business-processes.md) </span></span>  
 <span data-ttu-id="a9ca5-118">[SdkMessage Entity](entities/sdkmessage.md) </span><span class="sxs-lookup"><span data-stu-id="a9ca5-118">[SdkMessage Entity](entities/sdkmessage.md) </span></span>  
 <span data-ttu-id="a9ca5-119">[SdkMessageFilter Entity](entities/sdkmessagefilter.md) </span><span class="sxs-lookup"><span data-stu-id="a9ca5-119">[SdkMessageFilter Entity](entities/sdkmessagefilter.md) </span></span>  
 <span data-ttu-id="a9ca5-120">[SdkMessageProcessingStep Entity](entities/sdkmessageprocessingstep.md) </span><span class="sxs-lookup"><span data-stu-id="a9ca5-120">[SdkMessageProcessingStep Entity](entities/sdkmessageprocessingstep.md) </span></span>  
 <span data-ttu-id="a9ca5-121">[SdkMessageProcessingStepImage Entity](entities/sdkmessageprocessingstepimage.md) </span><span class="sxs-lookup"><span data-stu-id="a9ca5-121">[SdkMessageProcessingStepImage Entity](entities/sdkmessageprocessingstepimage.md) </span></span>  
 <span data-ttu-id="a9ca5-122">[SdkMessageProcessingStepSecureConfig Entity](entities/sdkmessageprocessingstepsecureconfig.md) </span><span class="sxs-lookup"><span data-stu-id="a9ca5-122">[SdkMessageProcessingStepSecureConfig Entity](entities/sdkmessageprocessingstepsecureconfig.md) </span></span>  
 [<span data-ttu-id="a9ca5-123">Plug-in Entities</span><span class="sxs-lookup"><span data-stu-id="a9ca5-123">Plug-in Entities</span></span>](plug-in-entities.md)
