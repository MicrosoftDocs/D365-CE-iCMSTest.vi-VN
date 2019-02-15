---
title: Use webhooks to create external handlers for server events(Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: You can send data about events that occur on the server to a web application using webhooks. Webhooks is a lightweight HTTP pattern for connecting Web APIs and services with a publish/subscribe model. webhook senders notify receivers about events by making requests to receiver endpoints with some information about the events.
ms.custom: ''
ms.date: 12/18/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8994bbac-951f-478a-972c-debe1afedaf9
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 87ebc53a6849b415e726fa631dbe2aa07cc146f6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387352"
---
# <a name="use-webhooks-to-create-external-handlers-for-server-events"></a><span data-ttu-id="89c00-105">Use webhooks to create external handlers for server events</span><span class="sxs-lookup"><span data-stu-id="89c00-105">Use webhooks to create external handlers for server events</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="89c00-106">Starting with [!INCLUDE [pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)] you can send data about events that occur on the server to a web application using webhooks.</span><span class="sxs-lookup"><span data-stu-id="89c00-106">Starting with [!INCLUDE [pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)] you can send data about events that occur on the server to a web application using webhooks.</span></span> <span data-ttu-id="89c00-107">Webhooks is a lightweight HTTP pattern for connecting Web APIs and services with a publish/subscribe model.</span><span class="sxs-lookup"><span data-stu-id="89c00-107">Webhooks is a lightweight HTTP pattern for connecting Web APIs and services with a publish/subscribe model.</span></span> <span data-ttu-id="89c00-108">Webhook senders notify receivers about events by making requests to receiver endpoints with some information about the events.</span><span class="sxs-lookup"><span data-stu-id="89c00-108">Webhook senders notify receivers about events by making requests to receiver endpoints with some information about the events.</span></span>

<span data-ttu-id="89c00-109">Webhooks enable developers and ISV’s to integrate Customer Engagement data with their own custom code hosted on external services.</span><span class="sxs-lookup"><span data-stu-id="89c00-109">Webhooks enable developers and ISV’s to integrate Customer Engagement data with their own custom code hosted on external services.</span></span> <span data-ttu-id="89c00-110">By using the webhook model, you can secure your endpoint by using authentication header or query string parameter keys.</span><span class="sxs-lookup"><span data-stu-id="89c00-110">By using the webhook model, you can secure your endpoint by using authentication header or query string parameter keys.</span></span> <span data-ttu-id="89c00-111">This is simpler than the SAS authentication model that you may currently use for [!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] integration.</span><span class="sxs-lookup"><span data-stu-id="89c00-111">This is simpler than the SAS authentication model that you may currently use for [!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] integration.</span></span>

<span data-ttu-id="89c00-112">When deciding between the webhook model and the [!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] integration, here are some items to keep in mind:</span><span class="sxs-lookup"><span data-stu-id="89c00-112">When deciding between the webhook model and the [!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] integration, here are some items to keep in mind:</span></span>

- <span data-ttu-id="89c00-113">[!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] works for high scale processing, and provides a full queueing mechanism if [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)] is pushing many events.</span><span class="sxs-lookup"><span data-stu-id="89c00-113">[!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] works for high scale processing, and provides a full queueing mechanism if [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)] is pushing many events.</span></span>
- <span data-ttu-id="89c00-114">Webhooks can only scale to the point at which your hosted web service can handle the messages.</span><span class="sxs-lookup"><span data-stu-id="89c00-114">Webhooks can only scale to the point at which your hosted web service can handle the messages.</span></span>
- <span data-ttu-id="89c00-115">Webhooks enables synchronous and asynchronous steps.</span><span class="sxs-lookup"><span data-stu-id="89c00-115">Webhooks enables synchronous and asynchronous steps.</span></span> <span data-ttu-id="89c00-116">[!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] only allows for asynchronous steps.</span><span class="sxs-lookup"><span data-stu-id="89c00-116">[!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] only allows for asynchronous steps.</span></span>
- <span data-ttu-id="89c00-117">Webhooks send POST requests with JSON payload and can be consumed by any programming language or web application hosted anywhere.</span><span class="sxs-lookup"><span data-stu-id="89c00-117">Webhooks send POST requests with JSON payload and can be consumed by any programming language or web application hosted anywhere.</span></span>
- <span data-ttu-id="89c00-118">Both webhooks and [!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] can be invoked from a plugin or custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="89c00-118">Both webhooks and [!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] can be invoked from a plugin or custom workflow activity.</span></span>


## <a name="get-started"></a><span data-ttu-id="89c00-119">Bắt đầu</span><span class="sxs-lookup"><span data-stu-id="89c00-119">Get Started</span></span>

<span data-ttu-id="89c00-120">There are three parts to using web hooks:</span><span class="sxs-lookup"><span data-stu-id="89c00-120">There are three parts to using web hooks:</span></span>

- <span data-ttu-id="89c00-121">Creating or configuring a service to consume webhook requests.</span><span class="sxs-lookup"><span data-stu-id="89c00-121">Creating or configuring a service to consume webhook requests.</span></span>
- <span data-ttu-id="89c00-122">Registering webhook step on the [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)] service, or</span><span class="sxs-lookup"><span data-stu-id="89c00-122">Registering webhook step on the [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)] service, or</span></span>
- <span data-ttu-id="89c00-123">Invoking a webhook from a plug-in or custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="89c00-123">Invoking a webhook from a plug-in or custom workflow activity.</span></span> 

<span data-ttu-id="89c00-124">This topic will start by explaining how to register a webhook and how to test the registration using a request logging site.</span><span class="sxs-lookup"><span data-stu-id="89c00-124">This topic will start by explaining how to register a webhook and how to test the registration using a request logging site.</span></span> <span data-ttu-id="89c00-125">This information will help inform you about the requirements in creating and configuring a service designed to consume webhook requests which is explained in [Create or Configure a service to consume webhook requests](#create-or-configure).</span><span class="sxs-lookup"><span data-stu-id="89c00-125">This information will help inform you about the requirements in creating and configuring a service designed to consume webhook requests which is explained in [Create or Configure a service to consume webhook requests](#create-or-configure).</span></span>

## <a name="register-a-webhook"></a><span data-ttu-id="89c00-126">Register a webhook</span><span class="sxs-lookup"><span data-stu-id="89c00-126">Register a webhook</span></span>

<span data-ttu-id="89c00-127">Use the Plug-in Registration tool to register a webhook.</span><span class="sxs-lookup"><span data-stu-id="89c00-127">Use the Plug-in Registration tool to register a webhook.</span></span> <span data-ttu-id="89c00-128">To get the Plug-in registration tool, see [Download tools from NuGet](download-tools-nuget.md).</span><span class="sxs-lookup"><span data-stu-id="89c00-128">To get the Plug-in registration tool, see [Download tools from NuGet](download-tools-nuget.md).</span></span> 

<span data-ttu-id="89c00-129">In the Plug-in Registration tool there is a new **Register New Web Hook** option to select.</span><span class="sxs-lookup"><span data-stu-id="89c00-129">In the Plug-in Registration tool there is a new **Register New Web Hook** option to select.</span></span>

![Shows the menu option to register a new web hook.](media/register-new-web-hook.PNG)

<span data-ttu-id="89c00-132">When you register a webhook you must provide three items of information:</span><span class="sxs-lookup"><span data-stu-id="89c00-132">When you register a webhook you must provide three items of information:</span></span>


|<span data-ttu-id="89c00-133">Mục</span><span class="sxs-lookup"><span data-stu-id="89c00-133">Item</span></span>  |<span data-ttu-id="89c00-134">Mô tả</span><span class="sxs-lookup"><span data-stu-id="89c00-134">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="89c00-135">**Tên**</span><span class="sxs-lookup"><span data-stu-id="89c00-135">**Name**</span></span>|<span data-ttu-id="89c00-136">A unique name describing the web hook.</span><span class="sxs-lookup"><span data-stu-id="89c00-136">A unique name describing the web hook.</span></span>|
|<span data-ttu-id="89c00-137">**Endpoint URL**</span><span class="sxs-lookup"><span data-stu-id="89c00-137">**Endpoint URL**</span></span>|<span data-ttu-id="89c00-138">The URL to post execution context information to.</span><span class="sxs-lookup"><span data-stu-id="89c00-138">The URL to post execution context information to.</span></span>|
|<span data-ttu-id="89c00-139">**Authentication**</span><span class="sxs-lookup"><span data-stu-id="89c00-139">**Authentication**</span></span>|<span data-ttu-id="89c00-140">One of three authentication options.</span><span class="sxs-lookup"><span data-stu-id="89c00-140">One of three authentication options.</span></span> <span data-ttu-id="89c00-141">For any type of authentication, you must provide the keys that will identify the request as legitimate.</span><span class="sxs-lookup"><span data-stu-id="89c00-141">For any type of authentication, you must provide the keys that will identify the request as legitimate.</span></span>|

### <a name="authentication-options"></a><span data-ttu-id="89c00-142">Authentication options</span><span class="sxs-lookup"><span data-stu-id="89c00-142">Authentication options</span></span>

<span data-ttu-id="89c00-143">The correct webhook registration authentication option and values to use depend on what the endpoint expects.</span><span class="sxs-lookup"><span data-stu-id="89c00-143">The correct webhook registration authentication option and values to use depend on what the endpoint expects.</span></span>  <span data-ttu-id="89c00-144">The owner of the endpoint must tell you what to use.</span><span class="sxs-lookup"><span data-stu-id="89c00-144">The owner of the endpoint must tell you what to use.</span></span> <span data-ttu-id="89c00-145">To use webhooks with [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)], the endpoint must allow one of the three authentication options described below:</span><span class="sxs-lookup"><span data-stu-id="89c00-145">To use webhooks with [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)], the endpoint must allow one of the three authentication options described below:</span></span>


|<span data-ttu-id="89c00-146">Loại</span><span class="sxs-lookup"><span data-stu-id="89c00-146">Type</span></span>  |<span data-ttu-id="89c00-147">Mô tả</span><span class="sxs-lookup"><span data-stu-id="89c00-147">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="89c00-148">**HttpHeader**</span><span class="sxs-lookup"><span data-stu-id="89c00-148">**HttpHeader**</span></span>|<span data-ttu-id="89c00-149">Includes one or more key values pairs in the header of the http request.</span><span class="sxs-lookup"><span data-stu-id="89c00-149">Includes one or more key values pairs in the header of the http request.</span></span><br /><span data-ttu-id="89c00-150">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="89c00-150">Example:</span></span> <br />`Key1: Value1`<br />`Key2: Value2`|
|<span data-ttu-id="89c00-151">**WebhookKey**</span><span class="sxs-lookup"><span data-stu-id="89c00-151">**WebhookKey**</span></span>|<span data-ttu-id="89c00-152">Includes a query string using `code` as the key and a value required by the endpoint.</span><span class="sxs-lookup"><span data-stu-id="89c00-152">Includes a query string using `code` as the key and a value required by the endpoint.</span></span> <span data-ttu-id="89c00-153">When registering the web hook using the Plug-in Registration tool, only enter the value.</span><span class="sxs-lookup"><span data-stu-id="89c00-153">When registering the web hook using the Plug-in Registration tool, only enter the value.</span></span><br /><span data-ttu-id="89c00-154">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="89c00-154">Example:</span></span> <br />`?code=00000000-0000-0000-0000-000000000001`|
|<span data-ttu-id="89c00-155">**HttpQueryString**</span><span class="sxs-lookup"><span data-stu-id="89c00-155">**HttpQueryString**</span></span>|<span data-ttu-id="89c00-156">Includes one or more key value pairs as query string parameters.</span><span class="sxs-lookup"><span data-stu-id="89c00-156">Includes one or more key value pairs as query string parameters.</span></span><br /><span data-ttu-id="89c00-157">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="89c00-157">Example:</span></span> <br />`?Key1=Value1&Key2=Value2`|

> [!NOTE]
> <span data-ttu-id="89c00-158">The **WebhookKey** option is useful with [Azure Functions](https://azure.microsoft.com/services/functions/) because the authentication query string is expected to have a key name of `code`.</span><span class="sxs-lookup"><span data-stu-id="89c00-158">The **WebhookKey** option is useful with [Azure Functions](https://azure.microsoft.com/services/functions/) because the authentication query string is expected to have a key name of `code`.</span></span>

<span data-ttu-id="89c00-159">Any request to the endpoint configured should fail when the authentication options passed in the request do not match.</span><span class="sxs-lookup"><span data-stu-id="89c00-159">Any request to the endpoint configured should fail when the authentication options passed in the request do not match.</span></span> <span data-ttu-id="89c00-160">This is the responsibility of the endpoint.</span><span class="sxs-lookup"><span data-stu-id="89c00-160">This is the responsibility of the endpoint.</span></span>

<a name="query-webhook-registrations"></a>

### <a name="query-webhook-registrations"></a><span data-ttu-id="89c00-161">Query webhook Registrations</span><span class="sxs-lookup"><span data-stu-id="89c00-161">Query webhook Registrations</span></span>

<span data-ttu-id="89c00-162">Webhook registrations are stored in the [ServiceEndpoint Entity](entities/serviceendpoint.md) and have a [Contract](entities/serviceendpoint.md#BKMK_Contract) value of `8`.</span><span class="sxs-lookup"><span data-stu-id="89c00-162">Webhook registrations are stored in the [ServiceEndpoint Entity](entities/serviceendpoint.md) and have a [Contract](entities/serviceendpoint.md#BKMK_Contract) value of `8`.</span></span>

<span data-ttu-id="89c00-163">You can find details about the registered webhooks by querying the **ServiceEndpoint** entity.</span><span class="sxs-lookup"><span data-stu-id="89c00-163">You can find details about the registered webhooks by querying the **ServiceEndpoint** entity.</span></span>

<span data-ttu-id="89c00-164">**Web API:**</span><span class="sxs-lookup"><span data-stu-id="89c00-164">**Web API:**</span></span>

`GET [organization URI]/api/data/v9.0/serviceendpoints?$filter=contract eq 8&$select= serviceendpointid,name,authtype,url`

<span data-ttu-id="89c00-165">**FetchXml:**</span><span class="sxs-lookup"><span data-stu-id="89c00-165">**FetchXml:**</span></span>

```xml
<fetch>
  <entity name="serviceendpoint" >
    <attribute name="serviceendpointid" />
    <attribute name="name" />
    <attribute name="authtype" />
    <attribute name="url" />
    <filter>
      <condition attribute="contract" operator="eq" value="8" />
    </filter>
  </entity>
</fetch> 
```
<span data-ttu-id="89c00-166">Details about the authentication values set are in the [AuthValue](entities/serviceendpoint.md#BKMK_AuthValue) property and cannot be retrieved.</span><span class="sxs-lookup"><span data-stu-id="89c00-166">Details about the authentication values set are in the [AuthValue](entities/serviceendpoint.md#BKMK_AuthValue) property and cannot be retrieved.</span></span>

## <a name="register-a-step-for-a-webhook"></a><span data-ttu-id="89c00-167">Register a step for a webhook</span><span class="sxs-lookup"><span data-stu-id="89c00-167">Register a step for a webhook</span></span>

<span data-ttu-id="89c00-168">Registering a step for a webhook is like registering a step for a plugin.</span><span class="sxs-lookup"><span data-stu-id="89c00-168">Registering a step for a webhook is like registering a step for a plugin.</span></span> <span data-ttu-id="89c00-169">The main difference is that you cannot specify any configuration information.</span><span class="sxs-lookup"><span data-stu-id="89c00-169">The main difference is that you cannot specify any configuration information.</span></span> 

<span data-ttu-id="89c00-170">Just like a plugin, you specify the message, and information about entities when appropriate.</span><span class="sxs-lookup"><span data-stu-id="89c00-170">Just like a plugin, you specify the message, and information about entities when appropriate.</span></span> <span data-ttu-id="89c00-171">You can also specify where in the event pipeline to execute the web hook, the execution mode and whether to delete any **AsyncOperation** when the operation succeeds.</span><span class="sxs-lookup"><span data-stu-id="89c00-171">You can also specify where in the event pipeline to execute the web hook, the execution mode and whether to delete any **AsyncOperation** when the operation succeeds.</span></span> 

![Plugin Registration dialog to register a new webhook step](media/Plugin-registration-register-webhook-step.PNG)

<span data-ttu-id="89c00-173">Information about the **Step Name**, and **Description** will be auto-populated based on the options you choose, but you can change them.</span><span class="sxs-lookup"><span data-stu-id="89c00-173">Information about the **Step Name**, and **Description** will be auto-populated based on the options you choose, but you can change them.</span></span> <span data-ttu-id="89c00-174">If you do not set some **Filtering Attributes** for a message that supports them, you will be prompted to do so as a performance best practices.</span><span class="sxs-lookup"><span data-stu-id="89c00-174">If you do not set some **Filtering Attributes** for a message that supports them, you will be prompted to do so as a performance best practices.</span></span>

### <a name="execution-mode-and-debugging-your-web-hook-registration"></a><span data-ttu-id="89c00-175">Execution mode and debugging your web hook registration</span><span class="sxs-lookup"><span data-stu-id="89c00-175">Execution mode and debugging your web hook registration</span></span>

<span data-ttu-id="89c00-176">Your choice in registering the webhook changes the experience you will have when debugging if things don’t work.</span><span class="sxs-lookup"><span data-stu-id="89c00-176">Your choice in registering the webhook changes the experience you will have when debugging if things don’t work.</span></span>

#### <a name="asynchronous-mode"></a><span data-ttu-id="89c00-177">Asynchronous mode</span><span class="sxs-lookup"><span data-stu-id="89c00-177">Asynchronous mode</span></span>
<span data-ttu-id="89c00-178">When you use asynchronous execution mode an asyncoperation job will be created to capture the success or failure of the operation.</span><span class="sxs-lookup"><span data-stu-id="89c00-178">When you use asynchronous execution mode an asyncoperation job will be created to capture the success or failure of the operation.</span></span> <span data-ttu-id="89c00-179">Choosing to delete the asyncoperation when it succeeds will save you database space.</span><span class="sxs-lookup"><span data-stu-id="89c00-179">Choosing to delete the asyncoperation when it succeeds will save you database space.</span></span> 

<span data-ttu-id="89c00-180">Any errors that occur will be recorded in System Jobs.</span><span class="sxs-lookup"><span data-stu-id="89c00-180">Any errors that occur will be recorded in System Jobs.</span></span> <span data-ttu-id="89c00-181">In the web application you can go to **Settings > System > System Jobs** to review the status of any web hooks.</span><span class="sxs-lookup"><span data-stu-id="89c00-181">In the web application you can go to **Settings > System > System Jobs** to review the status of any web hooks.</span></span> <span data-ttu-id="89c00-182">There will be a **Status Reason** value of **Failed**.</span><span class="sxs-lookup"><span data-stu-id="89c00-182">There will be a **Status Reason** value of **Failed**.</span></span> <span data-ttu-id="89c00-183">Open the failed system job entity to find details that describe why the job failed.</span><span class="sxs-lookup"><span data-stu-id="89c00-183">Open the failed system job entity to find details that describe why the job failed.</span></span>

#### <a name="synchronous-mode"></a><span data-ttu-id="89c00-184">Synchronous mode</span><span class="sxs-lookup"><span data-stu-id="89c00-184">Synchronous mode</span></span>

<span data-ttu-id="89c00-185">When you choose to use a synchronous execution mode any failure will be reported back to the user of the application with an **Endpoint unavailable** error dialog informing the user that the webhook service endpoint may be configured incorrectly or is not available.</span><span class="sxs-lookup"><span data-stu-id="89c00-185">When you choose to use a synchronous execution mode any failure will be reported back to the user of the application with an **Endpoint unavailable** error dialog informing the user that the webhook service endpoint may be configured incorrectly or is not available.</span></span> <span data-ttu-id="89c00-186">The dialog will allow you to download a log file to get details on any errors.</span><span class="sxs-lookup"><span data-stu-id="89c00-186">The dialog will allow you to download a log file to get details on any errors.</span></span>

> [!NOTE]
> <span data-ttu-id="89c00-187">You should use synchronous mode when it is important that the operation triggered by the webhook occur immediately or if you want the entire transaction to fail unless the webhook payload is recieved by the service.</span><span class="sxs-lookup"><span data-stu-id="89c00-187">You should use synchronous mode when it is important that the operation triggered by the webhook occur immediately or if you want the entire transaction to fail unless the webhook payload is recieved by the service.</span></span> <span data-ttu-id="89c00-188">A simple webhook step registration provides limited options to manage failure, but you can also invoke webhooks using plugins workflow activities if you require more control.</span><span class="sxs-lookup"><span data-stu-id="89c00-188">A simple webhook step registration provides limited options to manage failure, but you can also invoke webhooks using plugins workflow activities if you require more control.</span></span> <span data-ttu-id="89c00-189">More information: [Invoke a webhook from a plugin or workflow activity](#invoke-a-webhook-from-a-plugin-or-workflow-activity).</span><span class="sxs-lookup"><span data-stu-id="89c00-189">More information: [Invoke a webhook from a plugin or workflow activity](#invoke-a-webhook-from-a-plugin-or-workflow-activity).</span></span>


#### <a name="possible-causes-for-failure"></a><span data-ttu-id="89c00-190">Possible causes for failure</span><span class="sxs-lookup"><span data-stu-id="89c00-190">Possible causes for failure</span></span>

<span data-ttu-id="89c00-191">Webhooks are relatively simple.</span><span class="sxs-lookup"><span data-stu-id="89c00-191">Webhooks are relatively simple.</span></span> <span data-ttu-id="89c00-192">The service will send the request and evaluate the response.</span><span class="sxs-lookup"><span data-stu-id="89c00-192">The service will send the request and evaluate the response.</span></span> <span data-ttu-id="89c00-193">The system cannot parse any data returned with the body of the response, it will only look at the response `StatusCode` value.</span><span class="sxs-lookup"><span data-stu-id="89c00-193">The system cannot parse any data returned with the body of the response, it will only look at the response `StatusCode` value.</span></span>

<span data-ttu-id="89c00-194">The timeout is 60 seconds.</span><span class="sxs-lookup"><span data-stu-id="89c00-194">The timeout is 60 seconds.</span></span> <span data-ttu-id="89c00-195">Generally, if no response is returned before the timeout period or if the response `StatusCode` value is not within the `2xx` range to indicate success it will fail.</span><span class="sxs-lookup"><span data-stu-id="89c00-195">Generally, if no response is returned before the timeout period or if the response `StatusCode` value is not within the `2xx` range to indicate success it will fail.</span></span> <span data-ttu-id="89c00-196">The exception is when the error returned is in the following table:</span><span class="sxs-lookup"><span data-stu-id="89c00-196">The exception is when the error returned is in the following table:</span></span>

|`StatusCode`|<span data-ttu-id="89c00-197">Mô tả</span><span class="sxs-lookup"><span data-stu-id="89c00-197">Description</span></span>|
|-|-|
|`502`|<span data-ttu-id="89c00-198">Bad Gateway</span><span class="sxs-lookup"><span data-stu-id="89c00-198">Bad Gateway</span></span>|
|`503`|<span data-ttu-id="89c00-199">Service Unavailable</span><span class="sxs-lookup"><span data-stu-id="89c00-199">Service Unavailable</span></span>|
|`504`|<span data-ttu-id="89c00-200">Gateway Timeout</span><span class="sxs-lookup"><span data-stu-id="89c00-200">Gateway Timeout</span></span>|

<span data-ttu-id="89c00-201">These errors indicate a networking issue that might be resolved with another attempt.</span><span class="sxs-lookup"><span data-stu-id="89c00-201">These errors indicate a networking issue that might be resolved with another attempt.</span></span> <span data-ttu-id="89c00-202">The webhook service will make one more attempt only when these error codes are returned.</span><span class="sxs-lookup"><span data-stu-id="89c00-202">The webhook service will make one more attempt only when these error codes are returned.</span></span>

<span data-ttu-id="89c00-203">See [Query failed asynchronous jobs for a given step](#query-failed-asynchronous-jobs-for-a-given-step) for information about how to retrieve data about failed asynchronous jobs.</span><span class="sxs-lookup"><span data-stu-id="89c00-203">See [Query failed asynchronous jobs for a given step](#query-failed-asynchronous-jobs-for-a-given-step) for information about how to retrieve data about failed asynchronous jobs.</span></span>

### <a name="query-steps-registered-for-a-webhook"></a><span data-ttu-id="89c00-204">Query steps registered for a webhook</span><span class="sxs-lookup"><span data-stu-id="89c00-204">Query steps registered for a webhook</span></span>

<span data-ttu-id="89c00-205">Data for registered webhooks is in the [SdkMessageProcessingStep Entity](entities/sdkmessageprocessingstep.md).</span><span class="sxs-lookup"><span data-stu-id="89c00-205">Data for registered webhooks is in the [SdkMessageProcessingStep Entity](entities/sdkmessageprocessingstep.md).</span></span>

<span data-ttu-id="89c00-206">You can query the steps registered for a specific webhook when you know the serviceendpointid for the webhook.</span><span class="sxs-lookup"><span data-stu-id="89c00-206">You can query the steps registered for a specific webhook when you know the serviceendpointid for the webhook.</span></span> <span data-ttu-id="89c00-207">See [Query webhook registrations](#query-webhook-registrations) for a query to get the id for a registered web hook.</span><span class="sxs-lookup"><span data-stu-id="89c00-207">See [Query webhook registrations](#query-webhook-registrations) for a query to get the id for a registered web hook.</span></span>

<span data-ttu-id="89c00-208">**Web API:**</span><span class="sxs-lookup"><span data-stu-id="89c00-208">**Web API:**</span></span>

<span data-ttu-id="89c00-209">You can use this Web API Query where *&lt;id&gt;* is the [ServiceEndpointId](entities/serviceendpoint.md#BKMK_ServiceEndpointId) of the webhook:</span><span class="sxs-lookup"><span data-stu-id="89c00-209">You can use this Web API Query where *&lt;id&gt;* is the [ServiceEndpointId](entities/serviceendpoint.md#BKMK_ServiceEndpointId) of the webhook:</span></span>

```
GET [organization URI]/api/data/v9.0/serviceendpoints(@id)/serviceendpoint_sdkmessageprocessingstep?$select=sdkmessageprocessingstepid,name,description,asyncautodelete,filteringattributes,mode,stage?@id=<id>
```

<span data-ttu-id="89c00-210">For more information about the registered step, you can use this Web API query where *&lt;stepid&gt;* is the [SdkMessageProcessingStepId](entities/sdkmessageprocessingstep.md#BKMK_SdkMessageProcessingStepId) for the step:</span><span class="sxs-lookup"><span data-stu-id="89c00-210">For more information about the registered step, you can use this Web API query where *&lt;stepid&gt;* is the [SdkMessageProcessingStepId](entities/sdkmessageprocessingstep.md#BKMK_SdkMessageProcessingStepId) for the step:</span></span>

```
GET [organization URI]/api/data/v9.0/sdkmessageprocessingsteps(@id)?$select=name,description,filteringattributes,asyncautodelete,mode,stage&$expand=plugintypeid($select=friendlyname),eventhandler_serviceendpoint($select=name),sdkmessagefilterid($select=primaryobjecttypecode),sdkmessageid($select=name)?@id=<stepid>
```

<span data-ttu-id="89c00-211">**FetchXML:**</span><span class="sxs-lookup"><span data-stu-id="89c00-211">**FetchXML:**</span></span>

<span data-ttu-id="89c00-212">You can use this FetchXML to get the same information in one query where *&lt;serviceendpointid&gt;* is the id of the webhook:</span><span class="sxs-lookup"><span data-stu-id="89c00-212">You can use this FetchXML to get the same information in one query where *&lt;serviceendpointid&gt;* is the id of the webhook:</span></span>

```xml
<fetch>
  <entity name="sdkmessageprocessingstep" >
    <attribute name="name" />
    <attribute name="filteringattributes" />
    <attribute name="stage" />
    <attribute name="asyncautodeletename" />
    <attribute name="description" />
    <attribute name="mode" />
    <link-entity name="serviceendpoint" from="serviceendpointid" to="eventhandler" link-type="inner" alias="endpnt" >
      <attribute name="name" />
      <filter>
        <condition attribute="serviceendpointid" operator="eq" value="<serviceendpointid>" />
      </filter>
    </link-entity>
    <link-entity name="sdkmessagefilter" from="sdkmessagefilterid" to="sdkmessagefilterid" link-type="inner" alias="fltr" >
      <attribute name="primaryobjecttypecode" />
    </link-entity>
    <link-entity name="sdkmessage" from="sdkmessageid" to="sdkmessageid" link-type="inner" alias="msg" >
      <attribute name="name" />
    </link-entity>
  </entity>
</fetch>
```

<a name="query-failed-asynchronous-jobs-for-a-given-step"></a>

### <a name="query-failed-asynchronous-jobs-for-a-given-step"></a><span data-ttu-id="89c00-213">Query failed asynchronous jobs for a given step</span><span class="sxs-lookup"><span data-stu-id="89c00-213">Query failed asynchronous jobs for a given step</span></span>
<span data-ttu-id="89c00-214">When you know the **sdkmessageprocessingstepid** of a given step, you can query the [AsynchronousOperations Entity](entities/asyncoperation.md) for any errors.</span><span class="sxs-lookup"><span data-stu-id="89c00-214">When you know the **sdkmessageprocessingstepid** of a given step, you can query the [AsynchronousOperations Entity](entities/asyncoperation.md) for any errors.</span></span> <span data-ttu-id="89c00-215">You can use the [OwningExtensionId](entities/asyncoperation.md#BKMK_OwningExtensionId) value to filter the results to a specific registered step.</span><span class="sxs-lookup"><span data-stu-id="89c00-215">You can use the [OwningExtensionId](entities/asyncoperation.md#BKMK_OwningExtensionId) value to filter the results to a specific registered step.</span></span> <span data-ttu-id="89c00-216">The following examples use *&lt;stepid&gt;* for the **sdkmessageprocessingstepid** of the step.</span><span class="sxs-lookup"><span data-stu-id="89c00-216">The following examples use *&lt;stepid&gt;* for the **sdkmessageprocessingstepid** of the step.</span></span>

<span data-ttu-id="89c00-217">**Web API:**</span><span class="sxs-lookup"><span data-stu-id="89c00-217">**Web API:**</span></span>

`GET [organization URI]/api/data/v9.0/asyncoperations?$orderby=completedon desc&$filter=statuscode eq 31 and _owningextensionid_value eq @stepid&$select=name,friendlymessage,errorcode,message,completedon?@stepid=<stepid>`

<span data-ttu-id="89c00-218">**FetchXML:**</span><span class="sxs-lookup"><span data-stu-id="89c00-218">**FetchXML:**</span></span>

```xml
<fetch>
  <entity name="asyncoperation" >
    <attribute name="name" />
        <attribute name="friendlymessage" />
    <attribute name="errorcode" />
    <attribute name="message" />
    <attribute name="completedon" />     
    <filter>
      <condition attribute="owningextensionid" operator="eq" value="<stepid>" />
    </filter>
    <order attribute="completedon" descending="true" />
  </entity>
</fetch>
```

## <a name="test-your-registration-with-a-request-logging-site"></a><span data-ttu-id="89c00-219">Test your registration with a request logging site</span><span class="sxs-lookup"><span data-stu-id="89c00-219">Test your registration with a request logging site</span></span>

<span data-ttu-id="89c00-220">Before you move on to create or configure a service to consume web hooks, you should test what kind of data the service will receive so that you can know what kind of data you will need to process.</span><span class="sxs-lookup"><span data-stu-id="89c00-220">Before you move on to create or configure a service to consume web hooks, you should test what kind of data the service will receive so that you can know what kind of data you will need to process.</span></span> <span data-ttu-id="89c00-221">For this purpose, you can use one of several request logging sites.</span><span class="sxs-lookup"><span data-stu-id="89c00-221">For this purpose, you can use one of several request logging sites.</span></span> <span data-ttu-id="89c00-222">For the purpose of this example, we will use [RequestBin](https://requestb.in/) to configure a target for the webhook requests.</span><span class="sxs-lookup"><span data-stu-id="89c00-222">For the purpose of this example, we will use [RequestBin](https://requestb.in/) to configure a target for the webhook requests.</span></span> <span data-ttu-id="89c00-223">Use the following steps:</span><span class="sxs-lookup"><span data-stu-id="89c00-223">Use the following steps:</span></span>

1. <span data-ttu-id="89c00-224">Go to [https://requestb.in/](https://requestb.in/) and click **Create a RequestBin**.</span><span class="sxs-lookup"><span data-stu-id="89c00-224">Go to [https://requestb.in/](https://requestb.in/) and click **Create a RequestBin**.</span></span>
2. <span data-ttu-id="89c00-225">The next page will provide a Bin URL like : `https://requestb.in/<random string>`.</span><span class="sxs-lookup"><span data-stu-id="89c00-225">The next page will provide a Bin URL like : `https://requestb.in/<random string>`.</span></span> <span data-ttu-id="89c00-226">Copy this URL.</span><span class="sxs-lookup"><span data-stu-id="89c00-226">Copy this URL.</span></span>
3. <span data-ttu-id="89c00-227">Refresh the page and the page URL will change to `https://requestb.in/<random string>?inspect` and will show that no requests have been made to the URL.</span><span class="sxs-lookup"><span data-stu-id="89c00-227">Refresh the page and the page URL will change to `https://requestb.in/<random string>?inspect` and will show that no requests have been made to the URL.</span></span>
4. <span data-ttu-id="89c00-228">Use the plugin registration tool to register a new webhook as described under [Register a webhook](#register-a-webhook).</span><span class="sxs-lookup"><span data-stu-id="89c00-228">Use the plugin registration tool to register a new webhook as described under [Register a webhook](#register-a-webhook).</span></span> <span data-ttu-id="89c00-229">Use the URL you copied in step 2 as the **Endpoint URL**.</span><span class="sxs-lookup"><span data-stu-id="89c00-229">Use the URL you copied in step 2 as the **Endpoint URL**.</span></span> <span data-ttu-id="89c00-230">Set a name and any authentication properties you want.</span><span class="sxs-lookup"><span data-stu-id="89c00-230">Set a name and any authentication properties you want.</span></span> <span data-ttu-id="89c00-231">Request Bin will not evaluate these values in the way that an actual site that will process the data should, but you can see how they will be passed through.</span><span class="sxs-lookup"><span data-stu-id="89c00-231">Request Bin will not evaluate these values in the way that an actual site that will process the data should, but you can see how they will be passed through.</span></span>
5. <span data-ttu-id="89c00-232">Use the plugin registration tool to register a step using the webhook you created in step 4 as described in [Register a step for a webhook](#register-a-step-for-a-webhook).</span><span class="sxs-lookup"><span data-stu-id="89c00-232">Use the plugin registration tool to register a step using the webhook you created in step 4 as described in [Register a step for a webhook](#register-a-step-for-a-webhook).</span></span> <span data-ttu-id="89c00-233">Make sure to use an event that you can easily perform by editing data in the [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)] application, such as updating a contact entity.</span><span class="sxs-lookup"><span data-stu-id="89c00-233">Make sure to use an event that you can easily perform by editing data in the [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)] application, such as updating a contact entity.</span></span>
6. <span data-ttu-id="89c00-234">Use the [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)] app to perform the operation to trigger the event.</span><span class="sxs-lookup"><span data-stu-id="89c00-234">Use the [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)] app to perform the operation to trigger the event.</span></span>
7. <span data-ttu-id="89c00-235">After you trigger the event, return to the `https://requestb.in/<random string>?inspect` page from step 3 and refresh the page.</span><span class="sxs-lookup"><span data-stu-id="89c00-235">After you trigger the event, return to the `https://requestb.in/<random string>?inspect` page from step 3 and refresh the page.</span></span> <span data-ttu-id="89c00-236">You should discover a page similar to the following:</span><span class="sxs-lookup"><span data-stu-id="89c00-236">You should discover a page similar to the following:</span></span>

    ![An example of the request logged on the request bin web site](media/request-bin-example.png)

> [!NOTE]
> <span data-ttu-id="89c00-238">The results viewed on this site do not necessarily represent the capitalization of the values sent.</span><span class="sxs-lookup"><span data-stu-id="89c00-238">The results viewed on this site do not necessarily represent the capitalization of the values sent.</span></span> <span data-ttu-id="89c00-239">Http headers are case-insensitive and the RequestBin site appears to apply some formatting rules to make the values easier to read.</span><span class="sxs-lookup"><span data-stu-id="89c00-239">Http headers are case-insensitive and the RequestBin site appears to apply some formatting rules to make the values easier to read.</span></span> <span data-ttu-id="89c00-240">However, values sent by [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)] are all lower-case regardless of what is displayed here.</span><span class="sxs-lookup"><span data-stu-id="89c00-240">However, values sent by [!INCLUDE [Dynamics 365 for Customer Engagement](../includes/pn-dyn-365.md)] are all lower-case regardless of what is displayed here.</span></span> <span data-ttu-id="89c00-241">More information: [Header Data](#header-data)</span><span class="sxs-lookup"><span data-stu-id="89c00-241">More information: [Header Data](#header-data)</span></span>

<span data-ttu-id="89c00-242">This example shows the data that is passed in the webhook request for the update of a contact where the webhook is registered to pass **HttpHeader** authentication key value pairs:</span><span class="sxs-lookup"><span data-stu-id="89c00-242">This example shows the data that is passed in the webhook request for the update of a contact where the webhook is registered to pass **HttpHeader** authentication key value pairs:</span></span>


|<span data-ttu-id="89c00-243">Key</span><span class="sxs-lookup"><span data-stu-id="89c00-243">Key</span></span>|<span data-ttu-id="89c00-244">Value</span><span class="sxs-lookup"><span data-stu-id="89c00-244">Value</span></span>|
|---------|---------|
|`X-Test1`|`test1`|
|`X-Test2`|`test2`|


<span data-ttu-id="89c00-245">You will find execution context data as a JSON string in the **RAW BODY** section at the bottom of the entry.</span><span class="sxs-lookup"><span data-stu-id="89c00-245">You will find execution context data as a JSON string in the **RAW BODY** section at the bottom of the entry.</span></span> <span data-ttu-id="89c00-246">This is the data that the web service processing the webhook request will need to evaluate.</span><span class="sxs-lookup"><span data-stu-id="89c00-246">This is the data that the web service processing the webhook request will need to evaluate.</span></span> <span data-ttu-id="89c00-247">More information: [Request Body](#request-body)</span><span class="sxs-lookup"><span data-stu-id="89c00-247">More information: [Request Body](#request-body)</span></span>

<a name="create-or-configure"></a>

## <a name="create-or-configure-a-service-to-consume-webhook-requests"></a><span data-ttu-id="89c00-248">Create or Configure a service to consume webhook requests</span><span class="sxs-lookup"><span data-stu-id="89c00-248">Create or Configure a service to consume webhook requests</span></span>

<span data-ttu-id="89c00-249">Webhooks is simply a pattern that can be applied using a wide range of technologies.</span><span class="sxs-lookup"><span data-stu-id="89c00-249">Webhooks is simply a pattern that can be applied using a wide range of technologies.</span></span> <span data-ttu-id="89c00-250">There are no required frameworks, platforms, or programming languages you must use.</span><span class="sxs-lookup"><span data-stu-id="89c00-250">There are no required frameworks, platforms, or programming languages you must use.</span></span> <span data-ttu-id="89c00-251">Use the skills and knowledge you have to deliver the appropriate solution.</span><span class="sxs-lookup"><span data-stu-id="89c00-251">Use the skills and knowledge you have to deliver the appropriate solution.</span></span> <span data-ttu-id="89c00-252">[Azure Functions](https://azure.microsoft.com/services/functions/) provide an excellent way to deliver a solution using webhooks, but it is not a requirement.</span><span class="sxs-lookup"><span data-stu-id="89c00-252">[Azure Functions](https://azure.microsoft.com/services/functions/) provide an excellent way to deliver a solution using webhooks, but it is not a requirement.</span></span> <span data-ttu-id="89c00-253">This section will not provide guidance towards a specific solution but will instead describe the data that will be passed to your service that will enable your service to add value.</span><span class="sxs-lookup"><span data-stu-id="89c00-253">This section will not provide guidance towards a specific solution but will instead describe the data that will be passed to your service that will enable your service to add value.</span></span>

<span data-ttu-id="89c00-254">As demonstrated in [Test your registration with a request logging site](#test-your-registration-with-a-request-logging-site), you can register a test webhook step and use the request logging site to capture the specific kinds of data that your application can process.</span><span class="sxs-lookup"><span data-stu-id="89c00-254">As demonstrated in [Test your registration with a request logging site](#test-your-registration-with-a-request-logging-site), you can register a test webhook step and use the request logging site to capture the specific kinds of data that your application can process.</span></span> 

### <a name="data-passed-to-the-service"></a><span data-ttu-id="89c00-255">Data passed to the service</span><span class="sxs-lookup"><span data-stu-id="89c00-255">Data passed to the service</span></span>

<span data-ttu-id="89c00-256">There are three types of data in the request: Query String, Header Data, and Request Body.</span><span class="sxs-lookup"><span data-stu-id="89c00-256">There are three types of data in the request: Query String, Header Data, and Request Body.</span></span>

#### <a name="query-string"></a><span data-ttu-id="89c00-257">Chuỗi Truy vấn</span><span class="sxs-lookup"><span data-stu-id="89c00-257">Query String</span></span>

<span data-ttu-id="89c00-258">The only kind of data that will be passed as a query string may be the authentication values passed if the web hook is configured to use the **WebhookKey** or **HttpQueryString** options as described in [Authentication options](#authentication-options).</span><span class="sxs-lookup"><span data-stu-id="89c00-258">The only kind of data that will be passed as a query string may be the authentication values passed if the web hook is configured to use the **WebhookKey** or **HttpQueryString** options as described in [Authentication options](#authentication-options).</span></span> 

#### <a name="header-data"></a><span data-ttu-id="89c00-259">Header Data</span><span class="sxs-lookup"><span data-stu-id="89c00-259">Header Data</span></span>

<span data-ttu-id="89c00-260">If you choose the **HttpHeader** authentication option, you will need to use the key/value pairs that your service will require.</span><span class="sxs-lookup"><span data-stu-id="89c00-260">If you choose the **HttpHeader** authentication option, you will need to use the key/value pairs that your service will require.</span></span>

<span data-ttu-id="89c00-261">Other data you can expect to find passed to your service is in the table below:</span><span class="sxs-lookup"><span data-stu-id="89c00-261">Other data you can expect to find passed to your service is in the table below:</span></span>


|<span data-ttu-id="89c00-262">Key</span><span class="sxs-lookup"><span data-stu-id="89c00-262">Key</span></span>|<span data-ttu-id="89c00-263">Value Description</span><span class="sxs-lookup"><span data-stu-id="89c00-263">Value Description</span></span>|
|---------|---------|
|`x-request-id`|<span data-ttu-id="89c00-264">A unique identifier for the request</span><span class="sxs-lookup"><span data-stu-id="89c00-264">A unique identifier for the request</span></span>|
|`x-ms-dynamics-organization`|<span data-ttu-id="89c00-265">The name of the tenant sending the request</span><span class="sxs-lookup"><span data-stu-id="89c00-265">The name of the tenant sending the request</span></span>|
|`x-ms-dynamics-entity-name`|<span data-ttu-id="89c00-266">The logical name of the entity passed in the execution context data.</span><span class="sxs-lookup"><span data-stu-id="89c00-266">The logical name of the entity passed in the execution context data.</span></span>|
|`x-ms-dynamics-request-name`|<span data-ttu-id="89c00-267">The name of the Event that the webhook step was registered for.</span><span class="sxs-lookup"><span data-stu-id="89c00-267">The name of the Event that the webhook step was registered for.</span></span>|
|`x-ms-correlation-request-id`|<span data-ttu-id="89c00-268">Unique identifier for tracking any type of extension.</span><span class="sxs-lookup"><span data-stu-id="89c00-268">Unique identifier for tracking any type of extension.</span></span> <span data-ttu-id="89c00-269">This property is used by the platform for infinite loop prevention.</span><span class="sxs-lookup"><span data-stu-id="89c00-269">This property is used by the platform for infinite loop prevention.</span></span> <span data-ttu-id="89c00-270">In most cases, this property can be ignored.</span><span class="sxs-lookup"><span data-stu-id="89c00-270">In most cases, this property can be ignored.</span></span> <span data-ttu-id="89c00-271">This value may be used when working with technical support because it can be used to query telemetry to understand what occurred during the entire operation.</span><span class="sxs-lookup"><span data-stu-id="89c00-271">This value may be used when working with technical support because it can be used to query telemetry to understand what occurred during the entire operation.</span></span>
|`x-ms-dynamics-msg-size-exceeded`|<span data-ttu-id="89c00-272">Sent only when the HTTP payload size exceeds the 256KB.</span><span class="sxs-lookup"><span data-stu-id="89c00-272">Sent only when the HTTP payload size exceeds the 256KB.</span></span>|


#### <a name="request-body"></a><span data-ttu-id="89c00-273">Request Body</span><span class="sxs-lookup"><span data-stu-id="89c00-273">Request Body</span></span>

<span data-ttu-id="89c00-274">The body will contain string that represents the JSON value of an instance of the <xref:Microsoft.Xrm.Sdk.RemoteExecutionContext> class.</span><span class="sxs-lookup"><span data-stu-id="89c00-274">The body will contain string that represents the JSON value of an instance of the <xref:Microsoft.Xrm.Sdk.RemoteExecutionContext> class.</span></span> <span data-ttu-id="89c00-275">This is the same data that is passed to Azure service bus integrations.</span><span class="sxs-lookup"><span data-stu-id="89c00-275">This is the same data that is passed to Azure service bus integrations.</span></span> 

<span data-ttu-id="89c00-276">The service you create must parse this data to extract the relevant items of information for your service to provide its function.</span><span class="sxs-lookup"><span data-stu-id="89c00-276">The service you create must parse this data to extract the relevant items of information for your service to provide its function.</span></span> <span data-ttu-id="89c00-277">How you choose to parse this data depends on the technology you are using and your preferences.</span><span class="sxs-lookup"><span data-stu-id="89c00-277">How you choose to parse this data depends on the technology you are using and your preferences.</span></span>

<span data-ttu-id="89c00-278">The following is an example of the serialized JSON data passed for a step registered with the following properties:</span><span class="sxs-lookup"><span data-stu-id="89c00-278">The following is an example of the serialized JSON data passed for a step registered with the following properties:</span></span>


|<span data-ttu-id="89c00-279">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="89c00-279">Property</span></span>|<span data-ttu-id="89c00-280">Mô tả</span><span class="sxs-lookup"><span data-stu-id="89c00-280">Description</span></span>|
|---------|---------|
|<span data-ttu-id="89c00-281">**Thông báo**</span><span class="sxs-lookup"><span data-stu-id="89c00-281">**Message**</span></span>|<span data-ttu-id="89c00-282">Update</span><span class="sxs-lookup"><span data-stu-id="89c00-282">Update</span></span>|
|<span data-ttu-id="89c00-283">**Thực thể chính**</span><span class="sxs-lookup"><span data-stu-id="89c00-283">**Primary Entity**</span></span>|<span data-ttu-id="89c00-284">người liên hệ</span><span class="sxs-lookup"><span data-stu-id="89c00-284">contact</span></span>|
|<span data-ttu-id="89c00-285">**Secondary Entity**</span><span class="sxs-lookup"><span data-stu-id="89c00-285">**Secondary Entity**</span></span>|<span data-ttu-id="89c00-286">không</span><span class="sxs-lookup"><span data-stu-id="89c00-286">none</span></span>|
|<span data-ttu-id="89c00-287">**Filtering Attributes**</span><span class="sxs-lookup"><span data-stu-id="89c00-287">**Filtering Attributes**</span></span>|<span data-ttu-id="89c00-288">firstname,lastname</span><span class="sxs-lookup"><span data-stu-id="89c00-288">firstname,lastname</span></span>|
|<span data-ttu-id="89c00-289">**Run in User’s Context**</span><span class="sxs-lookup"><span data-stu-id="89c00-289">**Run in User’s Context**</span></span>|<span data-ttu-id="89c00-290">Calling User</span><span class="sxs-lookup"><span data-stu-id="89c00-290">Calling User</span></span>|
|<span data-ttu-id="89c00-291">**Execution Order**</span><span class="sxs-lookup"><span data-stu-id="89c00-291">**Execution Order**</span></span>|<span data-ttu-id="89c00-292">1</span><span class="sxs-lookup"><span data-stu-id="89c00-292">1</span></span>|
|<span data-ttu-id="89c00-293">**Event Pipeline Stage of Execution**</span><span class="sxs-lookup"><span data-stu-id="89c00-293">**Event Pipeline Stage of Execution**</span></span>|<span data-ttu-id="89c00-294">PostOperation</span><span class="sxs-lookup"><span data-stu-id="89c00-294">PostOperation</span></span>|
|<span data-ttu-id="89c00-295">**Execution Mode**</span><span class="sxs-lookup"><span data-stu-id="89c00-295">**Execution Mode**</span></span>|<span data-ttu-id="89c00-296">Asynchronous</span><span class="sxs-lookup"><span data-stu-id="89c00-296">Asynchronous</span></span>|

<span data-ttu-id="89c00-297">In this example, the contact's first name was changed from 'Jim' to 'James'.</span><span class="sxs-lookup"><span data-stu-id="89c00-297">In this example, the contact's first name was changed from 'Jim' to 'James'.</span></span>

```json
{
    "BusinessUnitId": "e2b9dd85-e89e-e711-8122-000d3aa2331c",
    "CorrelationId": "b374239d-4233-41a9-8b17-a86cb4f737b5",
    "Depth": 1,
    "InitiatingUserId": "75c2dd85-e89e-e711-8122-000d3aa2331c",
    "InputParameters": [{
        "key": "Target",
        "value": {
            "__type": "Entity:http:\/\/schemas.microsoft.com\/xrm\/2011\/Contracts",
            "Attributes": [{
                "key": "firstname",
                "value": "James"
            }, {
                "key": "contactid",
                "value": "6d81597f-0f9f-e711-8122-000d3aa2331c"
            }, {
                "key": "fullname",
                "value": "James Glynn (sample)"
            }, {
                "key": "yomifullname",
                "value": "James Glynn (sample)"
            }, {
                "key": "modifiedon",
                "value": "\/Date(1506384247000)\/"
            }, {
                "key": "modifiedby",
                "value": {
                    "__type": "EntityReference:http:\/\/schemas.microsoft.com\/xrm\/2011\/Contracts",
                    "Id": "75c2dd85-e89e-e711-8122-000d3aa2331c",
                    "KeyAttributes": [],
                    "LogicalName": "systemuser",
                    "Name": null,
                    "RowVersion": null
                }
            }, {
                "key": "modifiedonbehalfby",
                "value": null
            }],
            "EntityState": null,
            "FormattedValues": [],
            "Id": "6d81597f-0f9f-e711-8122-000d3aa2331c",
            "KeyAttributes": [],
            "LogicalName": "contact",
            "RelatedEntities": [],
            "RowVersion": null
        }
    }],
    "IsExecutingOffline": false,
    "IsInTransaction": false,
    "IsOfflinePlayback": false,
    "IsolationMode": 1,
    "MessageName": "Update",
    "Mode": 1,
    "OperationCreatedOn": "\/Date(1506409448000-0700)\/",
    "OperationId": "4af10637-4ea2-e711-8122-000d3aa2331c",
    "OrganizationId": "4ef5b371-e89e-e711-8122-000d3aa2331c",
    "OrganizationName": "OrgName",
    "OutputParameters": [],
    "OwningExtension": {
        "Id": "75417616-4ea2-e711-8122-000d3aa2331c",
        "KeyAttributes": [],
        "LogicalName": "sdkmessageprocessingstep",
        "Name": null,
        "RowVersion": null
    },
    "ParentContext": {
        "BusinessUnitId": "e2b9dd85-e89e-e711-8122-000d3aa2331c",
        "CorrelationId": "b374239d-4233-41a9-8b17-a86cb4f737b5",
        "Depth": 1,
        "InitiatingUserId": "75c2dd85-e89e-e711-8122-000d3aa2331c",
        "InputParameters": [{
            "key": "Target",
            "value": {
                "__type": "Entity:http:\/\/schemas.microsoft.com\/xrm\/2011\/Contracts",
                "Attributes": [{
                    "key": "firstname",
                    "value": "James"
                }, {
                    "key": "contactid",
                    "value": "6d81597f-0f9f-e711-8122-000d3aa2331c"
                }],
                "EntityState": null,
                "FormattedValues": [],
                "Id": "6d81597f-0f9f-e711-8122-000d3aa2331c",
                "KeyAttributes": [],
                "LogicalName": "contact",
                "RelatedEntities": [],
                "RowVersion": null
            }
        }, {
            "key": "SuppressDuplicateDetection",
            "value": false
        }],
        "IsExecutingOffline": false,
        "IsInTransaction": false,
        "IsOfflinePlayback": false,
        "IsolationMode": 1,
        "MessageName": "Update",
        "Mode": 1,
        "OperationCreatedOn": "\/Date(1506409448000-0700)\/",
        "OperationId": "4af10637-4ea2-e711-8122-000d3aa2331c",
        "OrganizationId": "4ef5b371-e89e-e711-8122-000d3aa2331c",
        "OrganizationName": "OneFarm",
        "OutputParameters": [],
        "OwningExtension": {
            "Id": "75417616-4ea2-e711-8122-000d3aa2331c",
            "KeyAttributes": [],
            "LogicalName": "sdkmessageprocessingstep",
            "Name": null,
            "RowVersion": null
        },
        "ParentContext": null,
        "PostEntityImages": [],
        "PreEntityImages": [],
        "PrimaryEntityId": "6d81597f-0f9f-e711-8122-000d3aa2331c",
        "PrimaryEntityName": "contact",
        "RequestId": null,
        "SecondaryEntityName": "none",
        "SharedVariables": [{
            "key": "ChangedEntityTypes",
            "value": [{
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "feedback",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "contract",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "salesorder",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "connection",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "socialactivity",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "postfollow",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "incident",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "invoice",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "entitlement",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "lead",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "opportunity",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "quote",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "socialprofile",
                "value": "Update"
            }, {
                "__type": "KeyValuePairOfstringstring:#System.Collections.Generic",
                "key": "contact",
                "value": "Update"
            }]
        }],
        "Stage": 30,
        "UserId": "75c2dd85-e89e-e711-8122-000d3aa2331c"
    },
    "PostEntityImages": [{
        "key": "AsynchronousStepPrimaryName",
        "value": {
            "Attributes": [{
                "key": "fullname",
                "value": "James Glynn (sample)"
            }, {
                "key": "contactid",
                "value": "6d81597f-0f9f-e711-8122-000d3aa2331c"
            }],
            "EntityState": null,
            "FormattedValues": [],
            "Id": "6d81597f-0f9f-e711-8122-000d3aa2331c",
            "KeyAttributes": [],
            "LogicalName": "contact",
            "RelatedEntities": [],
            "RowVersion": null
        }
    }],
    "PreEntityImages": [],
    "PrimaryEntityId": "6d81597f-0f9f-e711-8122-000d3aa2331c",
    "PrimaryEntityName": "contact",
    "RequestId": null,
    "SecondaryEntityName": "none",
    "SharedVariables": [],
    "Stage": 40,
    "UserId": "75c2dd85-e89e-e711-8122-000d3aa2331c"
}
```
> [!IMPORTANT]
> <span data-ttu-id="89c00-298">When the size of the entire HTTP payload exceeds 256KB, the `x-ms-dynamics-msg-size-exceeded` header will be included and the following <xref:Microsoft.Xrm.Sdk.RemoteExecutionContext> properties will be removed:</span><span class="sxs-lookup"><span data-stu-id="89c00-298">When the size of the entire HTTP payload exceeds 256KB, the `x-ms-dynamics-msg-size-exceeded` header will be included and the following <xref:Microsoft.Xrm.Sdk.RemoteExecutionContext> properties will be removed:</span></span>
> 
> - <xref:Microsoft.Xrm.Sdk.RemoteExecutionContext.ParentContext>
> - <xref:Microsoft.Xrm.Sdk.RemoteExecutionContext.InputParameters>
> - <xref:Microsoft.Xrm.Sdk.RemoteExecutionContext.PreEntityImages>
> - <xref:Microsoft.Xrm.Sdk.RemoteExecutionContext.PostEntityImages>
> 
><span data-ttu-id="89c00-299">Some operations do not include these properties.</span><span class="sxs-lookup"><span data-stu-id="89c00-299">Some operations do not include these properties.</span></span>

## <a name="invoke-a-webhook-from-a-plugin-or-workflow-activity"></a><span data-ttu-id="89c00-300">Invoke a webhook from a plugin or workflow activity</span><span class="sxs-lookup"><span data-stu-id="89c00-300">Invoke a webhook from a plugin or workflow activity</span></span>
<span data-ttu-id="89c00-301">Because a webhook is a kind of service endpoint you can also invoke it without registering a step with a plug-in or workflow activity in the same way you can for an [!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] endpoint.</span><span class="sxs-lookup"><span data-stu-id="89c00-301">Because a webhook is a kind of service endpoint you can also invoke it without registering a step with a plug-in or workflow activity in the same way you can for an [!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] endpoint.</span></span>  <span data-ttu-id="89c00-302">You need to provide the [ServiceEndpointId](entities/serviceendpoint.md#BKMK_ServiceEndpointId) to the <xref:Microsoft.Xrm.Sdk.IServiceEndpointNotificationService> interface.</span><span class="sxs-lookup"><span data-stu-id="89c00-302">You need to provide the [ServiceEndpointId](entities/serviceendpoint.md#BKMK_ServiceEndpointId) to the <xref:Microsoft.Xrm.Sdk.IServiceEndpointNotificationService> interface.</span></span> <span data-ttu-id="89c00-303">See the following [!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] samples for more information:</span><span class="sxs-lookup"><span data-stu-id="89c00-303">See the following [!INCLUDE [Azure Service Bus](../includes/pn-azure-service-bus.md)] samples for more information:</span></span> 
- [<span data-ttu-id="89c00-304">Sample: Azure aware custom plug-in</span><span class="sxs-lookup"><span data-stu-id="89c00-304">Sample: Azure aware custom plug-in</span></span>](sample-azure-aware-custom-plugin.md)
- [<span data-ttu-id="89c00-305">Sample: Azure aware custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="89c00-305">Sample: Azure aware custom workflow activity</span></span>](sample-azure-aware-custom-workflow-activity.md)

### <a name="see-also"></a><span data-ttu-id="89c00-306">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="89c00-306">See also</span></span>
[<span data-ttu-id="89c00-307">Extend Customer Engagement on the server</span><span class="sxs-lookup"><span data-stu-id="89c00-307">Extend Customer Engagement on the server</span></span>](extend-dynamics-365-server.md)<br />
[<span data-ttu-id="89c00-308">Write plug-ins to extend business processes</span><span class="sxs-lookup"><span data-stu-id="89c00-308">Write plug-ins to extend business processes</span></span>](write-plugin-extend-business-processes.md)<br />
[<span data-ttu-id="89c00-309">Automate your business processes in Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="89c00-309">Automate your business processes in Customer Engagement apps</span></span>](automate-business-processes-customer-engagement.md)<br />
[<span data-ttu-id="89c00-310">Asynchronous service in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="89c00-310">Asynchronous service in Dynamics 365 for Customer Engagement apps</span></span>](asynchronous-service.md)<br />
[<span data-ttu-id="89c00-311">Azure extensions for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="89c00-311">Azure extensions for Dynamics 365 for Customer Engagement apps</span></span>](azure-extensions.md)<br />
[<span data-ttu-id="89c00-312">Sample: Azure aware custom plug-in</span><span class="sxs-lookup"><span data-stu-id="89c00-312">Sample: Azure aware custom plug-in</span></span>](sample-azure-aware-custom-plugin.md)<br />
[<span data-ttu-id="89c00-313">Sample: Azure aware custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="89c00-313">Sample: Azure aware custom workflow activity</span></span>](sample-azure-aware-custom-workflow-activity.md)<br />
[<span data-ttu-id="89c00-314">Azure Functions</span><span class="sxs-lookup"><span data-stu-id="89c00-314">Azure Functions</span></span>](https://azure.microsoft.com/services/functions/)<br />
[<span data-ttu-id="89c00-315">ServiceEndpoint Entity</span><span class="sxs-lookup"><span data-stu-id="89c00-315">ServiceEndpoint Entity</span></span>](entities/serviceendpoint.md)<br />
[<span data-ttu-id="89c00-316">SdkMessageProcessingStep Entity</span><span class="sxs-lookup"><span data-stu-id="89c00-316">SdkMessageProcessingStep Entity</span></span>](entities/sdkmessageprocessingstep.md)<br />
[<span data-ttu-id="89c00-317">AsynchronousOperations Entity</span><span class="sxs-lookup"><span data-stu-id="89c00-317">AsynchronousOperations Entity</span></span>](entities/asyncoperation.md)<br />
<xref:Microsoft.Xrm.Sdk.RemoteExecutionContext><br />
<xref:Microsoft.Xrm.Sdk.IServiceEndpointNotificationService><br />
