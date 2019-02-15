---
title: Write a listener application for a Microsoft Azure solution (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The topic describes how to write an Azure solution listener application that can read and process Dynamics 365 for Customer Engagement (online) Customer Engagement messages that are posted to the Azure Service Bus.
ms.custom: ''
ms.date: 12/17/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: bf0b34fa-b49b-41f6-a2ca-9029a1ba64a1
caps.latest.revision: 60
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9271150f0fae099c90034af13e319eb11bd5726f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388351"
---
# <a name="write-a-listener-application-for-a-azure-solution"></a><span data-ttu-id="63ba3-103">Write a listener application for a Azure solution</span><span class="sxs-lookup"><span data-stu-id="63ba3-103">Write a listener application for a Azure solution</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="63ba3-104">This topic describes how to write an [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] solution  listener application that can read and process [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement messages that are posted to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span><span class="sxs-lookup"><span data-stu-id="63ba3-104">This topic describes how to write an [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] solution  listener application that can read and process [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement messages that are posted to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span></span> <span data-ttu-id="63ba3-105">As a prerequisite, you should familiarize yourself with how to write a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] listener before trying to learn the specifics of a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] listener.</span><span class="sxs-lookup"><span data-stu-id="63ba3-105">As a prerequisite, you should familiarize yourself with how to write a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] listener before trying to learn the specifics of a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] listener.</span></span> <span data-ttu-id="63ba3-106">For more information, see the [Azure Service Bus documentation](https://azure.microsoft.com/en-us/documentation/services/service-bus/).</span><span class="sxs-lookup"><span data-stu-id="63ba3-106">For more information, see the [Azure Service Bus documentation](https://azure.microsoft.com/en-us/documentation/services/service-bus/).</span></span>  
  
<a name="bkmk_writequeued"></a>

## <a name="write-a-queue-listener"></a><span data-ttu-id="63ba3-107">Write a queue listener</span><span class="sxs-lookup"><span data-stu-id="63ba3-107">Write a queue listener</span></span>

<span data-ttu-id="63ba3-108">A message *queue* is a repository of messages received at a service bus endpoint.</span><span class="sxs-lookup"><span data-stu-id="63ba3-108">A message *queue* is a repository of messages received at a service bus endpoint.</span></span> <span data-ttu-id="63ba3-109">A *queue listener* is an application that reads and processes these queued messages.</span><span class="sxs-lookup"><span data-stu-id="63ba3-109">A *queue listener* is an application that reads and processes these queued messages.</span></span> <span data-ttu-id="63ba3-110">Because the service bus messages are stored in a queue, a listener doesn’t have to be actively listening for messages to be received in the queue.</span><span class="sxs-lookup"><span data-stu-id="63ba3-110">Because the service bus messages are stored in a queue, a listener doesn’t have to be actively listening for messages to be received in the queue.</span></span> <span data-ttu-id="63ba3-111">A queue listener can be started after messages have arrived in the queue and still process those messages.</span><span class="sxs-lookup"><span data-stu-id="63ba3-111">A queue listener can be started after messages have arrived in the queue and still process those messages.</span></span> <span data-ttu-id="63ba3-112">Other types of listeners discussed in the next section must be actively listening or they will miss the opportunity to read a message.</span><span class="sxs-lookup"><span data-stu-id="63ba3-112">Other types of listeners discussed in the next section must be actively listening or they will miss the opportunity to read a message.</span></span> <span data-ttu-id="63ba3-113">These messages can originate from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] or from some other source.</span><span class="sxs-lookup"><span data-stu-id="63ba3-113">These messages can originate from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] or from some other source.</span></span> 
  
> [!IMPORTANT]
>  <span data-ttu-id="63ba3-114">When writing a queue listener, check each message header action to determine if the message originated from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="63ba3-114">When writing a queue listener, check each message header action to determine if the message originated from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)].</span></span> <span data-ttu-id="63ba3-115">For information on how to do this see [Filter messages](write-listener-application-azure-solution.md#filter).</span><span class="sxs-lookup"><span data-stu-id="63ba3-115">For information on how to do this see [Filter messages](write-listener-application-azure-solution.md#filter).</span></span>  
  
<span data-ttu-id="63ba3-116">You can do a destructive message read using [Receive](https://msdn.microsoft.com/library/microsoft.servicebus.messaging.queueclient.receive.aspx) in [ReceiveAndDelete](https://msdn.microsoft.com/library/microsoft.servicebus.messaging.receivemode.aspx) mode, where the message is read and removed from the queue, or a non-destructive read using [PeekLock](https://msdn.microsoft.com/library/microsoft.servicebus.messaging.receivemode.aspx) mode, where the message is read but still available in the queue.</span><span class="sxs-lookup"><span data-stu-id="63ba3-116">You can do a destructive message read using [Receive](https://msdn.microsoft.com/library/microsoft.servicebus.messaging.queueclient.receive.aspx) in [ReceiveAndDelete](https://msdn.microsoft.com/library/microsoft.servicebus.messaging.receivemode.aspx) mode, where the message is read and removed from the queue, or a non-destructive read using [PeekLock](https://msdn.microsoft.com/library/microsoft.servicebus.messaging.receivemode.aspx) mode, where the message is read but still available in the queue.</span></span> <span data-ttu-id="63ba3-117">The persistent queue listener sample code provided in this SDK does a destructive read.</span><span class="sxs-lookup"><span data-stu-id="63ba3-117">The persistent queue listener sample code provided in this SDK does a destructive read.</span></span> <span data-ttu-id="63ba3-118">For more information about reading messages from a queue, see [How to Receive Messages from a Queue](http://azure.microsoft.com/documentation/articles/service-bus-dotnet-how-to-use-queues/#how-to-receive-messages-from-a-queue).</span><span class="sxs-lookup"><span data-stu-id="63ba3-118">For more information about reading messages from a queue, see [How to Receive Messages from a Queue](http://azure.microsoft.com/documentation/articles/service-bus-dotnet-how-to-use-queues/#how-to-receive-messages-from-a-queue).</span></span>  
  
<span data-ttu-id="63ba3-119">A *topic* is similar to a queue but implements a publish/subscribe model.</span><span class="sxs-lookup"><span data-stu-id="63ba3-119">A *topic* is similar to a queue but implements a publish/subscribe model.</span></span> <span data-ttu-id="63ba3-120">One or more listeners can subscribe to the topic and receive messages from its queue.</span><span class="sxs-lookup"><span data-stu-id="63ba3-120">One or more listeners can subscribe to the topic and receive messages from its queue.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="63ba3-121">[Queues, Topics, and Subscriptions](https://msdn.microsoft.com/library/windowsazure/hh367516.aspx)</span><span class="sxs-lookup"><span data-stu-id="63ba3-121">[Queues, Topics, and Subscriptions](https://msdn.microsoft.com/library/windowsazure/hh367516.aspx)</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="63ba3-122">To use these queue or topic contracts, you must write your listener applications using the [Azure SDK](http://azure.microsoft.com/downloads/archive-net-downloads/) version 1.7 or higher.</span><span class="sxs-lookup"><span data-stu-id="63ba3-122">To use these queue or topic contracts, you must write your listener applications using the [Azure SDK](http://azure.microsoft.com/downloads/archive-net-downloads/) version 1.7 or higher.</span></span>  
  
<span data-ttu-id="63ba3-123">Use of queues and topics in your multisystem software design can result in the decoupling of systems.</span><span class="sxs-lookup"><span data-stu-id="63ba3-123">Use of queues and topics in your multisystem software design can result in the decoupling of systems.</span></span> <span data-ttu-id="63ba3-124">If the listener application ever becomes unavailable, the message delivery from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] will still succeed and the listener application can continue processing the queue message when it is back online.</span><span class="sxs-lookup"><span data-stu-id="63ba3-124">If the listener application ever becomes unavailable, the message delivery from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] will still succeed and the listener application can continue processing the queue message when it is back online.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="63ba3-125">[Queues, Topics, and Subscriptions](https://msdn.microsoft.com/library/windowsazure/hh367516.aspx)</span><span class="sxs-lookup"><span data-stu-id="63ba3-125">[Queues, Topics, and Subscriptions](https://msdn.microsoft.com/library/windowsazure/hh367516.aspx)</span></span>  
  
<a name="bkmk_writeoneway"></a>

## <a name="write-a-one-way-two-way-or-rest-listener"></a><span data-ttu-id="63ba3-126">Write a one-way, two-way, or REST listener</span><span class="sxs-lookup"><span data-stu-id="63ba3-126">Write a one-way, two-way, or REST listener</span></span>

<span data-ttu-id="63ba3-127">In addition to the queue listener described previously, you can write a listener for three other service bus contracts that are supported by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]: one-way, two-way, and REST.</span><span class="sxs-lookup"><span data-stu-id="63ba3-127">In addition to the queue listener described previously, you can write a listener for three other service bus contracts that are supported by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]: one-way, two-way, and REST.</span></span> <span data-ttu-id="63ba3-128">A one-way listener can read and process a message posted to the service bus.</span><span class="sxs-lookup"><span data-stu-id="63ba3-128">A one-way listener can read and process a message posted to the service bus.</span></span> <span data-ttu-id="63ba3-129">A two-way listener can do the same but can also return a string of some information back to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="63ba3-129">A two-way listener can do the same but can also return a string of some information back to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="63ba3-130">A REST listener is the same as the two-way listener except that it works with a REST endpoint.</span><span class="sxs-lookup"><span data-stu-id="63ba3-130">A REST listener is the same as the two-way listener except that it works with a REST endpoint.</span></span> <span data-ttu-id="63ba3-131">Notice that these listeners must be actively listening at a service endpoint to read a message sent over the service bus.</span><span class="sxs-lookup"><span data-stu-id="63ba3-131">Notice that these listeners must be actively listening at a service endpoint to read a message sent over the service bus.</span></span> <span data-ttu-id="63ba3-132">If the listener isn’t listening when [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] attempts to post a message to the service bus, the message doesn’t get sent.</span><span class="sxs-lookup"><span data-stu-id="63ba3-132">If the listener isn’t listening when [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] attempts to post a message to the service bus, the message doesn’t get sent.</span></span>  
  
<span data-ttu-id="63ba3-133">Writing a listener is structured around what is known as ABC: address, binding, and contract.</span><span class="sxs-lookup"><span data-stu-id="63ba3-133">Writing a listener is structured around what is known as ABC: address, binding, and contract.</span></span> 

### <a name="one-way-listener"></a><span data-ttu-id="63ba3-134">One-way listener</span><span class="sxs-lookup"><span data-stu-id="63ba3-134">One-way listener</span></span>
  
- <span data-ttu-id="63ba3-135">Address: service URI</span><span class="sxs-lookup"><span data-stu-id="63ba3-135">Address: service URI</span></span>  
  
- <span data-ttu-id="63ba3-136">Binding: [WS2007HttpRelayBinding](https://msdn.microsoft.com/library/microsoft.servicebus.ws2007httprelaybinding.aspx)</span><span class="sxs-lookup"><span data-stu-id="63ba3-136">Binding: [WS2007HttpRelayBinding](https://msdn.microsoft.com/library/microsoft.servicebus.ws2007httprelaybinding.aspx)</span></span>  
  
- <span data-ttu-id="63ba3-137">Contract: <xref:Microsoft.Xrm.Sdk.IServiceEndpointPlugin></span><span class="sxs-lookup"><span data-stu-id="63ba3-137">Contract: <xref:Microsoft.Xrm.Sdk.IServiceEndpointPlugin></span></span>  
  
<span data-ttu-id="63ba3-138">After your listener is registered with an endpoint, the listener’s <xref:Microsoft.Xrm.Sdk.IServiceEndpointPlugin.Execute*> method is invoked whenever a message is posted to the service bus by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="63ba3-138">After your listener is registered with an endpoint, the listener’s <xref:Microsoft.Xrm.Sdk.IServiceEndpointPlugin.Execute*> method is invoked whenever a message is posted to the service bus by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)].</span></span> <span data-ttu-id="63ba3-139">The `Execute` method doesn’t return any data from the method call.</span><span class="sxs-lookup"><span data-stu-id="63ba3-139">The `Execute` method doesn’t return any data from the method call.</span></span> <span data-ttu-id="63ba3-140">For more information, see the one-way listener sample, [Sample: One-way Listener](sample-one-way-listener.md).</span><span class="sxs-lookup"><span data-stu-id="63ba3-140">For more information, see the one-way listener sample, [Sample: One-way Listener](sample-one-way-listener.md).</span></span>  
  
### <a name="two-way-listener"></a><span data-ttu-id="63ba3-141">Two-way listener</span><span class="sxs-lookup"><span data-stu-id="63ba3-141">Two-way listener</span></span>
  
- <span data-ttu-id="63ba3-142">Address: service URI</span><span class="sxs-lookup"><span data-stu-id="63ba3-142">Address: service URI</span></span>  
  
- <span data-ttu-id="63ba3-143">Binding: [WS2007HttpRelayBinding](https://msdn.microsoft.com/library/microsoft.servicebus.ws2007httprelaybinding.aspx)</span><span class="sxs-lookup"><span data-stu-id="63ba3-143">Binding: [WS2007HttpRelayBinding](https://msdn.microsoft.com/library/microsoft.servicebus.ws2007httprelaybinding.aspx)</span></span>  
  
- <span data-ttu-id="63ba3-144">Contract: <xref:Microsoft.Xrm.Sdk.ITwoWayServiceEndpointPlugin></span><span class="sxs-lookup"><span data-stu-id="63ba3-144">Contract: <xref:Microsoft.Xrm.Sdk.ITwoWayServiceEndpointPlugin></span></span>  
  
<span data-ttu-id="63ba3-145">For this two-way contract, the <xref:Microsoft.Xrm.Sdk.ITwoWayServiceEndpointPlugin.Execute*> method returns a string from the method call.</span><span class="sxs-lookup"><span data-stu-id="63ba3-145">For this two-way contract, the <xref:Microsoft.Xrm.Sdk.ITwoWayServiceEndpointPlugin.Execute*> method returns a string from the method call.</span></span> <span data-ttu-id="63ba3-146">For more information, see the two-way listener sample, [Sample: Two-way Listener](sample-two-way-listener.md).</span><span class="sxs-lookup"><span data-stu-id="63ba3-146">For more information, see the two-way listener sample, [Sample: Two-way Listener](sample-two-way-listener.md).</span></span>  
  
### <a name="rest-listener"></a><span data-ttu-id="63ba3-147">REST listener</span><span class="sxs-lookup"><span data-stu-id="63ba3-147">REST listener</span></span>
  
- <span data-ttu-id="63ba3-148">Address: service URI</span><span class="sxs-lookup"><span data-stu-id="63ba3-148">Address: service URI</span></span>  
  
- <span data-ttu-id="63ba3-149">Binding: [WebHttpRelayBinding](https://msdn.microsoft.com/library/microsoft.servicebus.webhttprelaybinding.aspx)</span><span class="sxs-lookup"><span data-stu-id="63ba3-149">Binding: [WebHttpRelayBinding](https://msdn.microsoft.com/library/microsoft.servicebus.webhttprelaybinding.aspx)</span></span>  
  
- <span data-ttu-id="63ba3-150">Contract: <xref:Microsoft.Xrm.Sdk.IWebHttpServiceEndpointPlugin></span><span class="sxs-lookup"><span data-stu-id="63ba3-150">Contract: <xref:Microsoft.Xrm.Sdk.IWebHttpServiceEndpointPlugin></span></span>  
  
<span data-ttu-id="63ba3-151">For the REST contract, the <xref:Microsoft.Xrm.Sdk.IWebHttpServiceEndpointPlugin.Execute*>  method returns a string from the method call.</span><span class="sxs-lookup"><span data-stu-id="63ba3-151">For the REST contract, the <xref:Microsoft.Xrm.Sdk.IWebHttpServiceEndpointPlugin.Execute*>  method returns a string from the method call.</span></span> <span data-ttu-id="63ba3-152">Refer to the REST listener sample, [Sample: REST Listener](sample-rest-listener.md), for more information.</span><span class="sxs-lookup"><span data-stu-id="63ba3-152">Refer to the REST listener sample, [Sample: REST Listener](sample-rest-listener.md), for more information.</span></span> <span data-ttu-id="63ba3-153">Notice that in the REST listener sample, a [WebServiceHost](https://msdn.microsoft.com/library/system.servicemodel.web.webservicehost.aspx) is instantiated and not a [ServiceHost](https://msdn.microsoft.com/library/system.servicemodel.servicehost.aspx) as was done in the two-way sample.</span><span class="sxs-lookup"><span data-stu-id="63ba3-153">Notice that in the REST listener sample, a [WebServiceHost](https://msdn.microsoft.com/library/system.servicemodel.web.webservicehost.aspx) is instantiated and not a [ServiceHost](https://msdn.microsoft.com/library/system.servicemodel.servicehost.aspx) as was done in the two-way sample.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="63ba3-154">When using the out-of-box (ServiceBusPlugin) plug-in with a two-way or REST listener, the plug-in doesn’t use any string data returned from the listener.</span><span class="sxs-lookup"><span data-stu-id="63ba3-154">When using the out-of-box (ServiceBusPlugin) plug-in with a two-way or REST listener, the plug-in doesn’t use any string data returned from the listener.</span></span> <span data-ttu-id="63ba3-155">However, a custom [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)]-aware plug-in could make use of this information.</span><span class="sxs-lookup"><span data-stu-id="63ba3-155">However, a custom [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)]-aware plug-in could make use of this information.</span></span>  
> 
>  <span data-ttu-id="63ba3-156">When you run the listener samples, the issuer secret you’re prompted for is the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] management key.</span><span class="sxs-lookup"><span data-stu-id="63ba3-156">When you run the listener samples, the issuer secret you’re prompted for is the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] management key.</span></span> <span data-ttu-id="63ba3-157">The WS2007 Federation HTTP binding uses `token` mode and the WS-Trust 1.3 protocol.</span><span class="sxs-lookup"><span data-stu-id="63ba3-157">The WS2007 Federation HTTP binding uses `token` mode and the WS-Trust 1.3 protocol.</span></span>  
  
<a name="filter"></a>

## <a name="filter-messages"></a><span data-ttu-id="63ba3-158">Filter messages</span><span class="sxs-lookup"><span data-stu-id="63ba3-158">Filter messages</span></span>

<span data-ttu-id="63ba3-159">There is a property bag of extra information added to each brokered message [Properties](https://msdn.microsoft.com/library/windowsazure/microsoft.servicebus.messaging.brokeredmessage.properties.aspx) property sent from [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] and [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="63ba3-159">There is a property bag of extra information added to each brokered message [Properties](https://msdn.microsoft.com/library/windowsazure/microsoft.servicebus.messaging.brokeredmessage.properties.aspx) property sent from [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] and [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)].</span></span> <span data-ttu-id="63ba3-160">The property bag, available with queue, relay, and topic contract endpoints, contains the following information:</span><span class="sxs-lookup"><span data-stu-id="63ba3-160">The property bag, available with queue, relay, and topic contract endpoints, contains the following information:</span></span>  
  
- <span data-ttu-id="63ba3-161">Organization URI</span><span class="sxs-lookup"><span data-stu-id="63ba3-161">Organization URI</span></span>  
  
- <span data-ttu-id="63ba3-162">Calling user ID</span><span class="sxs-lookup"><span data-stu-id="63ba3-162">Calling user ID</span></span>  
  
- <span data-ttu-id="63ba3-163">Initiating user ID</span><span class="sxs-lookup"><span data-stu-id="63ba3-163">Initiating user ID</span></span>  
  
- <span data-ttu-id="63ba3-164">Entity logical name</span><span class="sxs-lookup"><span data-stu-id="63ba3-164">Entity logical name</span></span>  
  
- <span data-ttu-id="63ba3-165">Request name</span><span class="sxs-lookup"><span data-stu-id="63ba3-165">Request name</span></span>  
  
<span data-ttu-id="63ba3-166">This information identifies the organization, user, entity, and message request being processed by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] that resulted in the service bus message being posted.</span><span class="sxs-lookup"><span data-stu-id="63ba3-166">This information identifies the organization, user, entity, and message request being processed by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] that resulted in the service bus message being posted.</span></span> <span data-ttu-id="63ba3-167">The availability of these properties indicates that the message was sent from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="63ba3-167">The availability of these properties indicates that the message was sent from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)].</span></span> <span data-ttu-id="63ba3-168">Your listener code can decide how to process the message based on these values.</span><span class="sxs-lookup"><span data-stu-id="63ba3-168">Your listener code can decide how to process the message based on these values.</span></span>  
  
<a name="bkmk_multiple-formats"></a>
 
## <a name="read-the-data-context-in-multiple-data-formats"></a><span data-ttu-id="63ba3-169">Read the data context in multiple data formats</span><span class="sxs-lookup"><span data-stu-id="63ba3-169">Read the data context in multiple data formats</span></span>

<span data-ttu-id="63ba3-170">The data context from the current [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] operation is passed to your [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] solution listener application in the body of a service bus message.</span><span class="sxs-lookup"><span data-stu-id="63ba3-170">The data context from the current [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] operation is passed to your [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] solution listener application in the body of a service bus message.</span></span> <span data-ttu-id="63ba3-171">In previous releases, only a .NET binary format was supported.</span><span class="sxs-lookup"><span data-stu-id="63ba3-171">In previous releases, only a .NET binary format was supported.</span></span>  <span data-ttu-id="63ba3-172">For cross-platform (non-.NET) interoperability, you can now specify one of three data formats for the message body: .NET Binary, JSON, or XML.</span><span class="sxs-lookup"><span data-stu-id="63ba3-172">For cross-platform (non-.NET) interoperability, you can now specify one of three data formats for the message body: .NET Binary, JSON, or XML.</span></span>  <span data-ttu-id="63ba3-173">This format is specified in the [MessageFormat](entities/serviceendpoint.md#BKMK_MessageFormat) attribute of the [ServiceEndpoint Entity](entities/serviceendpoint.md).</span><span class="sxs-lookup"><span data-stu-id="63ba3-173">This format is specified in the [MessageFormat](entities/serviceendpoint.md#BKMK_MessageFormat) attribute of the [ServiceEndpoint Entity](entities/serviceendpoint.md).</span></span>  
  
> [!NOTE]
> [!INCLUDE[cc_feature_included_with_update_8_1_0_admins](../includes/cc-feature-included-with-update-8-1-0-admins.md)]  
  
<span data-ttu-id="63ba3-174">When receiving messages, your listener application can read the data context in the message body based on the contenttype of the message.</span><span class="sxs-lookup"><span data-stu-id="63ba3-174">When receiving messages, your listener application can read the data context in the message body based on the contenttype of the message.</span></span> <span data-ttu-id="63ba3-175">Sample code to do so is shown below.</span><span class="sxs-lookup"><span data-stu-id="63ba3-175">Sample code to do so is shown below.</span></span>  
  
```csharp
var receivedMessage = inboundQueueClient.Receive(TimeSpan.MaxValue);  
  
if (receivedMessage.ContentType = "application/msbin1")  
{  
    RemoteExecutionContext context = receivedMessage.GetBody<RemoteExecutionContext>();  
}  
else if (receivedMessage.ContentType = "application/json")  
{  
    //string jsonBody = new StreamReader(receivedMessage.GetBody<Stream>(), Encoding.UTF8).ReadToEnd();  
    RemoteExecutionContext contextFromJSON = receivedMessage.GetBody<RemoteExecutionContext>(  
        new DataContractJsonSerializer(typeof(RemoteExecutionContext)));  
}  
else if (receivedMessage.ContentType = "application/xml")  
{  
    //string xmlBody = new StreamReader(receivedMessage.GetBody<Stream>(), Encoding.UTF8).ReadToEnd();  
    RemoteExecutionContext contextFromXML = receivedMessage.GetBody<RemoteExecutionContext>(  
        new DataContractSerializer(typeof(RemoteExecutionContext)));  
}  
```  
  
### <a name="see-also"></a><span data-ttu-id="63ba3-176">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="63ba3-176">See also</span></span>

 <span data-ttu-id="63ba3-177">[Azure Extensions](azure-extensions.md) </span><span class="sxs-lookup"><span data-stu-id="63ba3-177">[Azure Extensions](azure-extensions.md) </span></span>  
 <span data-ttu-id="63ba3-178">[Write a Custom Azure-aware Plug-in](write-custom-azure-aware-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="63ba3-178">[Write a Custom Azure-aware Plug-in](write-custom-azure-aware-plugin.md) </span></span>  
 <span data-ttu-id="63ba3-179">[Sample: Persistent Queue Listener](sample-persistent-queue-listener.md) </span><span class="sxs-lookup"><span data-stu-id="63ba3-179">[Sample: Persistent Queue Listener](sample-persistent-queue-listener.md) </span></span>  
 <span data-ttu-id="63ba3-180">[Sample: One-way Listener](sample-one-way-listener.md) </span><span class="sxs-lookup"><span data-stu-id="63ba3-180">[Sample: One-way Listener](sample-one-way-listener.md) </span></span>  
 <span data-ttu-id="63ba3-181">[Sample: Two-way Listener](sample-two-way-listener.md) </span><span class="sxs-lookup"><span data-stu-id="63ba3-181">[Sample: Two-way Listener](sample-two-way-listener.md) </span></span>  
 <span data-ttu-id="63ba3-182">[Sample: REST Listener](sample-rest-listener.md) </span><span class="sxs-lookup"><span data-stu-id="63ba3-182">[Sample: REST Listener](sample-rest-listener.md) </span></span>  
 <span data-ttu-id="63ba3-183">[Send Dynamics 365 for Customer Engagement Data over the Azure Service Bus](work-data-azure-solution.md) </span><span class="sxs-lookup"><span data-stu-id="63ba3-183">[Send Dynamics 365 for Customer Engagement Data over the Azure Service Bus](work-data-azure-solution.md) </span></span>  
 [<span data-ttu-id="63ba3-184">Work with Dynamics 365 for Customer Engagement event data in your Azure Event Hub solution</span><span class="sxs-lookup"><span data-stu-id="63ba3-184">Work with Dynamics 365 for Customer Engagement event data in your Azure Event Hub solution</span></span>](work-event-data-azure-event-hub-solution.md)
