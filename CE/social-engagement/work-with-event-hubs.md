---
title: Work with events from Social Engagement in Azure Event Hubs | Microsoft Docs
description: Learn how to work with events in Event Hubs.
keywords: event hubs, stream analytics, authomation rule
ms.date: 02/20/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 80d207d4-f2df-4a04-8e39-5d09d3f44005
author: m-hartmann
ms.author: mhart
manager: sakudes
topic-status: Drafting
ms.custom:
- dyn365-socialengagement
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365SE
ms.openlocfilehash: 686f7cf3282976dfef2a137188d4d6070b339fbf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375674"
---
# <a name="work-with-events-from-includepnnetbreezeshortincludespn-social-engagement-shortmd-in-azure-event-hubs"></a><span data-ttu-id="0251f-104">Work with events from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] in Azure Event Hubs</span><span class="sxs-lookup"><span data-stu-id="0251f-104">Work with events from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] in Azure Event Hubs</span></span>
[!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] <span data-ttu-id="0251f-105">lets you stream posts to [!INCLUDE[pn_microsoft_azure_event_hubs](../includes/pn-microsoft-azure-event-hubs.md)] and empowers you with data, so unleash your creativity!</span><span class="sxs-lookup"><span data-stu-id="0251f-105">lets you stream posts to [!INCLUDE[pn_microsoft_azure_event_hubs](../includes/pn-microsoft-azure-event-hubs.md)] and empowers you with data, so unleash your creativity!</span></span> <span data-ttu-id="0251f-106">The options that [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)] offer are huge.</span><span class="sxs-lookup"><span data-stu-id="0251f-106">The options that [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)] offer are huge.</span></span> <span data-ttu-id="0251f-107">Benefit from a simple data format and highly performant cloud services to work with your data with endless possibilities.</span><span class="sxs-lookup"><span data-stu-id="0251f-107">Benefit from a simple data format and highly performant cloud services to work with your data with endless possibilities.</span></span> <span data-ttu-id="0251f-108">Build your own apps, connect your data with other data sources, and step into big data analysis.</span><span class="sxs-lookup"><span data-stu-id="0251f-108">Build your own apps, connect your data with other data sources, and step into big data analysis.</span></span>  

 <span data-ttu-id="0251f-109">To get you started, we’ve provided some inspiration to build a real-time [!INCLUDE[pn_microsoft_power_bi](../includes/pn-microsoft-power-bi.md)] Dashboard where we’ll stream posts from [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] to [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-109">To get you started, we’ve provided some inspiration to build a real-time [!INCLUDE[pn_microsoft_power_bi](../includes/pn-microsoft-power-bi.md)] Dashboard where we’ll stream posts from [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] to [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)].</span></span> <span data-ttu-id="0251f-110">By using the power of [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)] we can consolidate the information and push it to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] to analyze our data in real time.</span><span class="sxs-lookup"><span data-stu-id="0251f-110">By using the power of [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)] we can consolidate the information and push it to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] to analyze our data in real time.</span></span> [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)] <span data-ttu-id="0251f-111">provides the capabilities to combine the data from a variety of sources, where [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)] is one of them.</span><span class="sxs-lookup"><span data-stu-id="0251f-111">provides the capabilities to combine the data from a variety of sources, where [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)] is one of them.</span></span> <span data-ttu-id="0251f-112">It can send the data to another event hub, a SQL database, or to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-112">It can send the data to another event hub, a SQL database, or to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)].</span></span> [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] <span data-ttu-id="0251f-113">lets you build your own business intelligence based on the data sources you are connected to.</span><span class="sxs-lookup"><span data-stu-id="0251f-113">lets you build your own business intelligence based on the data sources you are connected to.</span></span> <span data-ttu-id="0251f-114">All connections listed in the scenario below are supported by default with the services.</span><span class="sxs-lookup"><span data-stu-id="0251f-114">All connections listed in the scenario below are supported by default with the services.</span></span> <span data-ttu-id="0251f-115">No need to customize—get started right away!</span><span class="sxs-lookup"><span data-stu-id="0251f-115">No need to customize—get started right away!</span></span>  

 <span data-ttu-id="0251f-116">For the following scenario, we assume that you have access to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] and an Azure subscription (including [!INCLUDE[pn_azure_service_bus](../includes/pn-azure-service-bus.md)], [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)], and [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)]), and have admin permissions to work through the steps.</span><span class="sxs-lookup"><span data-stu-id="0251f-116">For the following scenario, we assume that you have access to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] and an Azure subscription (including [!INCLUDE[pn_azure_service_bus](../includes/pn-azure-service-bus.md)], [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)], and [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)]), and have admin permissions to work through the steps.</span></span> <span data-ttu-id="0251f-117">If you want to know more about the functionality of these services, please refer to the following links:</span><span class="sxs-lookup"><span data-stu-id="0251f-117">If you want to know more about the functionality of these services, please refer to the following links:</span></span>  

-   [<span data-ttu-id="0251f-118">Service Bus documentation</span><span class="sxs-lookup"><span data-stu-id="0251f-118">Service Bus documentation</span></span>](https://azure.microsoft.com/documentation/services/service-bus/)  

-   [<span data-ttu-id="0251f-119">Event Hubs documentation</span><span class="sxs-lookup"><span data-stu-id="0251f-119">Event Hubs documentation</span></span>](https://azure.microsoft.com/documentation/services/event-hubs/)  

-   [<span data-ttu-id="0251f-120">Stream Analytics documentation</span><span class="sxs-lookup"><span data-stu-id="0251f-120">Stream Analytics documentation</span></span>](https://azure.microsoft.com/documentation/services/stream-analytics/)  

-   [<span data-ttu-id="0251f-121">Get started with Power BI</span><span class="sxs-lookup"><span data-stu-id="0251f-121">Get started with Power BI</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=786439)  

<a name="Analyze_in_Power_BI"></a>   
## <a name="analyze-social-posts-in-real-time-with-power-bi"></a><span data-ttu-id="0251f-122">Analyze social posts in real time with Power BI</span><span class="sxs-lookup"><span data-stu-id="0251f-122">Analyze social posts in real time with Power BI</span></span>  
 <span data-ttu-id="0251f-123">Learn more about the power and flexibility of the integration with [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)], connecting [!INCLUDE[cc_Microsoft](../includes/cc-microsoft.md)] services across the board.</span><span class="sxs-lookup"><span data-stu-id="0251f-123">Learn more about the power and flexibility of the integration with [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)], connecting [!INCLUDE[cc_Microsoft](../includes/cc-microsoft.md)] services across the board.</span></span> <span data-ttu-id="0251f-124">In this lightweight example, we’ll connect a data set of social posts to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] to perform real-time analysis.</span><span class="sxs-lookup"><span data-stu-id="0251f-124">In this lightweight example, we’ll connect a data set of social posts to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] to perform real-time analysis.</span></span> <span data-ttu-id="0251f-125">Make sure that you have access to the required services with the right privileges (usually admin permissions).</span><span class="sxs-lookup"><span data-stu-id="0251f-125">Make sure that you have access to the required services with the right privileges (usually admin permissions).</span></span>  


|                           <span data-ttu-id="0251f-126">Step</span><span class="sxs-lookup"><span data-stu-id="0251f-126">Step</span></span>                           |                                                                                    <span data-ttu-id="0251f-127">Description</span><span class="sxs-lookup"><span data-stu-id="0251f-127">Description</span></span>                                                                                    |                                                           <span data-ttu-id="0251f-128">Step</span><span class="sxs-lookup"><span data-stu-id="0251f-128">Step</span></span>                                                            |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0251f-129">![Step 1](media/crm-ua-walkthrough-green-1.png "Step 1")</span><span class="sxs-lookup"><span data-stu-id="0251f-129">![Step 1](media/crm-ua-walkthrough-green-1.png "Step 1")</span></span> |                         <span data-ttu-id="0251f-130">Create the event hub you will  stream data to.</span><span class="sxs-lookup"><span data-stu-id="0251f-130">Create the event hub you will  stream data to.</span></span><br /><br /> <span data-ttu-id="0251f-131">You can skip this step if you already have an event hub to work with.</span><span class="sxs-lookup"><span data-stu-id="0251f-131">You can skip this step if you already have an event hub to work with.</span></span>                          |                                  [<span data-ttu-id="0251f-132">Step 1: Create an event hub</span><span class="sxs-lookup"><span data-stu-id="0251f-132">Step 1: Create an event hub</span></span>](#step1_create_event_hub)                                   |
| <span data-ttu-id="0251f-133">![Step 2](media/crm-ua-walkthrough-green-2.png "Step 2")</span><span class="sxs-lookup"><span data-stu-id="0251f-133">![Step 2](media/crm-ua-walkthrough-green-2.png "Step 2")</span></span> | <span data-ttu-id="0251f-134">Establish the connection between [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] and [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-134">Establish the connection between [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] and [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)].</span></span> |                     [<span data-ttu-id="0251f-135">Step 2: Connect Social Engagement to the event hub</span><span class="sxs-lookup"><span data-stu-id="0251f-135">Step 2: Connect Social Engagement to the event hub</span></span>](#step3_connect_to_event_hub)                     |
| <span data-ttu-id="0251f-136">![Step 3](media/crm-ua-walkthrough-green-3.png "Step 3")</span><span class="sxs-lookup"><span data-stu-id="0251f-136">![Step 3](media/crm-ua-walkthrough-green-3.png "Step 3")</span></span> |                             <span data-ttu-id="0251f-137">Define the data set that gets streamed as events to [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-137">Define the data set that gets streamed as events to [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)].</span></span>                              | [<span data-ttu-id="0251f-138">Step 3: Create an automation rule to select the posts that get streamed to the event hub</span><span class="sxs-lookup"><span data-stu-id="0251f-138">Step 3: Create an automation rule to select the posts that get streamed to the event hub</span></span>](#step3_create_automation_rule) |
| <span data-ttu-id="0251f-139">![Step 4](media/crm-ua-walkthrough-green-4.png "Step 4")</span><span class="sxs-lookup"><span data-stu-id="0251f-139">![Step 4](media/crm-ua-walkthrough-green-4.png "Step 4")</span></span> |                  <span data-ttu-id="0251f-140">Create an [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)] job and write the query to further process your data.</span><span class="sxs-lookup"><span data-stu-id="0251f-140">Create an [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)] job and write the query to further process your data.</span></span>                  |                    [<span data-ttu-id="0251f-141">Step 4: Create an Azure Stream Analytics job</span><span class="sxs-lookup"><span data-stu-id="0251f-141">Step 4: Create an Azure Stream Analytics job</span></span>](#step4_create_stream_analytics_job)                     |
| <span data-ttu-id="0251f-142">![Step 5](media/crm-ua-walkthrough-green-5.png "Step 5")</span><span class="sxs-lookup"><span data-stu-id="0251f-142">![Step 5](media/crm-ua-walkthrough-green-5.png "Step 5")</span></span> |                                                 <span data-ttu-id="0251f-143">Send the data to a [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] dashboard.</span><span class="sxs-lookup"><span data-stu-id="0251f-143">Send the data to a [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] dashboard.</span></span>                                                 |                         [<span data-ttu-id="0251f-144">Step 5: Create a dashboard in Power BI</span><span class="sxs-lookup"><span data-stu-id="0251f-144">Step 5: Create a dashboard in Power BI</span></span>](#step5_create_powerBI_dashboard)                         |

<a name="step1_create_event_hub"></a>   
### <a name="step-1-create-an-event-hub"></a><span data-ttu-id="0251f-145">Step 1: Create an event hub</span><span class="sxs-lookup"><span data-stu-id="0251f-145">Step 1: Create an event hub</span></span>  

1. <span data-ttu-id="0251f-146">Create a new namespace in Service Bus.</span><span class="sxs-lookup"><span data-stu-id="0251f-146">Create a new namespace in Service Bus.</span></span> <span data-ttu-id="0251f-147">Select **Type: Messaging**, and then choose the other values to your preference.</span><span class="sxs-lookup"><span data-stu-id="0251f-147">Select **Type: Messaging**, and then choose the other values to your preference.</span></span> <span data-ttu-id="0251f-148">You can also use an existing Service Bus namespace.</span><span class="sxs-lookup"><span data-stu-id="0251f-148">You can also use an existing Service Bus namespace.</span></span>  

2. <span data-ttu-id="0251f-149">[Create a new event hub](https://azure.microsoft.com/documentation/articles/event-hubs-csharp-ephcs-getstarted/) in the namespace.</span><span class="sxs-lookup"><span data-stu-id="0251f-149">[Create a new event hub](https://azure.microsoft.com/documentation/articles/event-hubs-csharp-ephcs-getstarted/) in the namespace.</span></span>  

3. <span data-ttu-id="0251f-150">To get the connection string, click **Connection Information** in the Event Hub view in [Azure Portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="0251f-150">To get the connection string, click **Connection Information** in the Event Hub view in [Azure Portal](https://portal.azure.com/).</span></span> <span data-ttu-id="0251f-151">If it’s a new setup, you need to configure the Shared Access Signature (SAS) Policies first.</span><span class="sxs-lookup"><span data-stu-id="0251f-151">If it’s a new setup, you need to configure the Shared Access Signature (SAS) Policies first.</span></span>  

   1.  <span data-ttu-id="0251f-152">Create a new SAS policy under **shared access policies**.</span><span class="sxs-lookup"><span data-stu-id="0251f-152">Create a new SAS policy under **shared access policies**.</span></span> <span data-ttu-id="0251f-153">Give it a name, add a rule named *SendRule* with *Send* rights,  and then click **Save**.</span><span class="sxs-lookup"><span data-stu-id="0251f-153">Give it a name, add a rule named *SendRule* with *Send* rights,  and then click **Save**.</span></span>  

   2.  <span data-ttu-id="0251f-154">Copy the **Connection String** for *SendRule*; we’ll need it again in the next step.</span><span class="sxs-lookup"><span data-stu-id="0251f-154">Copy the **Connection String** for *SendRule*; we’ll need it again in the next step.</span></span>  

   <span data-ttu-id="0251f-155">![Access Azure event hub connections in Social Engagement](media/event-hubs-connection-information.png "Access Azure event hub connections in Social Engagement")</span><span class="sxs-lookup"><span data-stu-id="0251f-155">![Access Azure event hub connections in Social Engagement](media/event-hubs-connection-information.png "Access Azure event hub connections in Social Engagement")</span></span>  

<a name="step3_connect_to_event_hub"></a>   
### <a name="step-2-connect-includepnnetbreezeshortincludespn-social-engagement-shortmd-to-the-event-hub"></a><span data-ttu-id="0251f-156">Step 2: Connect [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to the event hub</span><span class="sxs-lookup"><span data-stu-id="0251f-156">Step 2: Connect [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to the event hub</span></span>  
 <span data-ttu-id="0251f-157">Now that the event hub is ready to receive data, you need to connect [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to your event hub using the Connection String provided for your event hub in the [Azure Portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="0251f-157">Now that the event hub is ready to receive data, you need to connect [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to your event hub using the Connection String provided for your event hub in the [Azure Portal](https://portal.azure.com/).</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0251f-158">[Stream data from Social Engagement to Microsoft Azure Event Hubs](stream-data-to-event-hubs.md)</span><span class="sxs-lookup"><span data-stu-id="0251f-158">[Stream data from Social Engagement to Microsoft Azure Event Hubs](stream-data-to-event-hubs.md)</span></span>  

 <span data-ttu-id="0251f-159">![Connect Social Engagement to Azure Event Hubs](media/event-hub-connection-settings.png "Connect Social Engagement to Azure Event Hubs")</span><span class="sxs-lookup"><span data-stu-id="0251f-159">![Connect Social Engagement to Azure Event Hubs](media/event-hub-connection-settings.png "Connect Social Engagement to Azure Event Hubs")</span></span>  

<a name="step3_create_automation_rule"></a>   
### <a name="step-3-create-an-automation-rule-to-select-the-posts-that-get-streamed-to-the-event-hub"></a><span data-ttu-id="0251f-160">Step 3: Create an automation rule to select the posts that get streamed to the event hub</span><span class="sxs-lookup"><span data-stu-id="0251f-160">Step 3: Create an automation rule to select the posts that get streamed to the event hub</span></span>  
 <span data-ttu-id="0251f-161">In [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], create an automation rule that streams events to your event hub.</span><span class="sxs-lookup"><span data-stu-id="0251f-161">In [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], create an automation rule that streams events to your event hub.</span></span> <span data-ttu-id="0251f-162">Make sure the filters are defined according to your requirements so you get the posts that you are looking for.</span><span class="sxs-lookup"><span data-stu-id="0251f-162">Make sure the filters are defined according to your requirements so you get the posts that you are looking for.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0251f-163">[Route posts using automation rules](automation-rules.md), [Get relevant data using filters](use-filters.md)</span><span class="sxs-lookup"><span data-stu-id="0251f-163">[Route posts using automation rules](automation-rules.md), [Get relevant data using filters](use-filters.md)</span></span>  

1. <span data-ttu-id="0251f-164">In [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], go to **Settings > Automation Rules**, and then create an automation rule that streams events to your event hub.</span><span class="sxs-lookup"><span data-stu-id="0251f-164">In [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], go to **Settings > Automation Rules**, and then create an automation rule that streams events to your event hub.</span></span>  

2. <span data-ttu-id="0251f-165">In [Azure Portal](https://portal.azure.com/), check the dashboard of the event hub and verify that the events from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] appear.</span><span class="sxs-lookup"><span data-stu-id="0251f-165">In [Azure Portal](https://portal.azure.com/), check the dashboard of the event hub and verify that the events from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] appear.</span></span> <span data-ttu-id="0251f-166">Depending on the selected data set, it may take a while for new posts to get published on social media and pushed to the event hub.</span><span class="sxs-lookup"><span data-stu-id="0251f-166">Depending on the selected data set, it may take a while for new posts to get published on social media and pushed to the event hub.</span></span>  

   <span data-ttu-id="0251f-167">![Events from Social Engagement shown in a connected event hub](media/verify-data-in-event-hubs.png "Events from Social Engagement shown in a connected event hub")</span><span class="sxs-lookup"><span data-stu-id="0251f-167">![Events from Social Engagement shown in a connected event hub](media/verify-data-in-event-hubs.png "Events from Social Engagement shown in a connected event hub")</span></span>  

<a name="step4_create_stream_analytics_job"></a>   
### <a name="step-4-create-an-azure-stream-analytics-job"></a><span data-ttu-id="0251f-168">Step 4: Create an Azure Stream Analytics job</span><span class="sxs-lookup"><span data-stu-id="0251f-168">Step 4: Create an Azure Stream Analytics job</span></span>  
 <span data-ttu-id="0251f-169">Let's go ahead and connect the event hub and [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-169">Let's go ahead and connect the event hub and [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)].</span></span>  

1. <span data-ttu-id="0251f-170">In the [Azure Portal](https://portal.azure.com/), create a new [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)] job.</span><span class="sxs-lookup"><span data-stu-id="0251f-170">In the [Azure Portal](https://portal.azure.com/), create a new [!INCLUDE[pn_azure_stream_analytics](../includes/pn-azure-stream-analytics.md)] job.</span></span>  

2. <span data-ttu-id="0251f-171">Name the job, and then choose the Region and the [Regional Monitoring Storage Account](https://azure.microsoft.com/documentation/articles/storage-monitor-storage-account/).</span><span class="sxs-lookup"><span data-stu-id="0251f-171">Name the job, and then choose the Region and the [Regional Monitoring Storage Account](https://azure.microsoft.com/documentation/articles/storage-monitor-storage-account/).</span></span>  

3. <span data-ttu-id="0251f-172">Go to **Stream Analytics Job details** and define the **input** source as **Data Stream > Event Hub**.</span><span class="sxs-lookup"><span data-stu-id="0251f-172">Go to **Stream Analytics Job details** and define the **input** source as **Data Stream > Event Hub**.</span></span> <span data-ttu-id="0251f-173">Provide an alias for your input and choose the namespace created in Step 1.</span><span class="sxs-lookup"><span data-stu-id="0251f-173">Provide an alias for your input and choose the namespace created in Step 1.</span></span>  

    <span data-ttu-id="0251f-174">For Event Hub Policy name, select **RootManagedSharedAccessKey**.</span><span class="sxs-lookup"><span data-stu-id="0251f-174">For Event Hub Policy name, select **RootManagedSharedAccessKey**.</span></span> <span data-ttu-id="0251f-175">Make a note of your input alias; you’ll need it later.</span><span class="sxs-lookup"><span data-stu-id="0251f-175">Make a note of your input alias; you’ll need it later.</span></span>  

4. <span data-ttu-id="0251f-176">Keep the Serialization settings to **JSON** and **UTF8**.</span><span class="sxs-lookup"><span data-stu-id="0251f-176">Keep the Serialization settings to **JSON** and **UTF8**.</span></span>  

5. <span data-ttu-id="0251f-177">Add an **output sink** for [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-177">Add an **output sink** for [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)].</span></span> <span data-ttu-id="0251f-178">For our scenario, select [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-178">For our scenario, select [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)].</span></span> <span data-ttu-id="0251f-179">Provide an alias for your output and make a note of it; we’ll need it later.</span><span class="sxs-lookup"><span data-stu-id="0251f-179">Provide an alias for your output and make a note of it; we’ll need it later.</span></span>  <span data-ttu-id="0251f-180">When you select [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)], you need to authorize your account, or create a new subscription.</span><span class="sxs-lookup"><span data-stu-id="0251f-180">When you select [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)], you need to authorize your account, or create a new subscription.</span></span>  

   > [!TIP]
   >  <span data-ttu-id="0251f-181">Sign in to the [Office 365 portal](https://portal.office.com) and open [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] first to establish a fresh session with [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] before you choose it as the output sink.</span><span class="sxs-lookup"><span data-stu-id="0251f-181">Sign in to the [Office 365 portal](https://portal.office.com) and open [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] first to establish a fresh session with [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] before you choose it as the output sink.</span></span>  

6. <span data-ttu-id="0251f-182">Now for the tricky part: We need to tell the [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)] job what data it should look for and what it should pass on to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-182">Now for the tricky part: We need to tell the [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)] job what data it should look for and what it should pass on to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)].</span></span> <span data-ttu-id="0251f-183">This is done with a SQL statement, which selects the events that match certain conditions (the selectors).</span><span class="sxs-lookup"><span data-stu-id="0251f-183">This is done with a SQL statement, which selects the events that match certain conditions (the selectors).</span></span> <span data-ttu-id="0251f-184">The resulting data gets pushed to the connected service (in this case [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)]), to store the events generated by [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-184">The resulting data gets pushed to the connected service (in this case [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)]), to store the events generated by [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)].</span></span> <span data-ttu-id="0251f-185">Refer to our examples below or develop your own [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)] SQL statement to query the data on the event hub and aggregate the data set you want to push to the output sink.</span><span class="sxs-lookup"><span data-stu-id="0251f-185">Refer to our examples below or develop your own [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)] SQL statement to query the data on the event hub and aggregate the data set you want to push to the output sink.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0251f-186">[MSDN: Stream Analytics Query Language Reference](https://msdn.microsoft.com/library/dn834998.aspx)</span><span class="sxs-lookup"><span data-stu-id="0251f-186">[MSDN: Stream Analytics Query Language Reference](https://msdn.microsoft.com/library/dn834998.aspx)</span></span>  

   > [!TIP]
   >  <span data-ttu-id="0251f-187">Windows Dev Center hosts the Service Bus Explorer—a tool to manage [!INCLUDE[pn_azure_service_bus](../includes/pn-azure-service-bus.md)] components.</span><span class="sxs-lookup"><span data-stu-id="0251f-187">Windows Dev Center hosts the Service Bus Explorer—a tool to manage [!INCLUDE[pn_azure_service_bus](../includes/pn-azure-service-bus.md)] components.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0251f-188">[Service Bus Explorer Download](https://code.msdn.microsoft.com/windowsapps/Service-Bus-Explorer-f2abca5a)</span><span class="sxs-lookup"><span data-stu-id="0251f-188">[Service Bus Explorer Download](https://code.msdn.microsoft.com/windowsapps/Service-Bus-Explorer-f2abca5a)</span></span>  
   > 
   >  <span data-ttu-id="0251f-189">Connect with Service Bus Explorer to your [!INCLUDE[pn_azure_service_bus](../includes/pn-azure-service-bus.md)] namespace.</span><span class="sxs-lookup"><span data-stu-id="0251f-189">Connect with Service Bus Explorer to your [!INCLUDE[pn_azure_service_bus](../includes/pn-azure-service-bus.md)] namespace.</span></span>  
   > 
   >  <span data-ttu-id="0251f-190">In the [Azure Portal](https://portal.azure.com/), go to **Service Bus > [namespace] > Connection Information**.</span><span class="sxs-lookup"><span data-stu-id="0251f-190">In the [Azure Portal](https://portal.azure.com/), go to **Service Bus > [namespace] > Connection Information**.</span></span> <span data-ttu-id="0251f-191">Copy the connection string from your SAS key for RootManagedSharedAccessKey to connect to your namespace.</span><span class="sxs-lookup"><span data-stu-id="0251f-191">Copy the connection string from your SAS key for RootManagedSharedAccessKey to connect to your namespace.</span></span>  
   > 
   >  <span data-ttu-id="0251f-192">In Service Bus Explorer, expand the event hub you connected to [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-192">In Service Bus Explorer, expand the event hub you connected to [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> <span data-ttu-id="0251f-193">Right-click the $Default consumer group, and then click Create Consumer Group Listener.</span><span class="sxs-lookup"><span data-stu-id="0251f-193">Right-click the $Default consumer group, and then click Create Consumer Group Listener.</span></span> <span data-ttu-id="0251f-194">Start the listener, and then review the JSON payload in the Event Text field of the Events tab.</span><span class="sxs-lookup"><span data-stu-id="0251f-194">Start the listener, and then review the JSON payload in the Event Text field of the Events tab.</span></span>  
   > 
   > [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0251f-195">[JSON reference for events from Social Engagement](event-hubs-json-reference-social-engagement.md)</span><span class="sxs-lookup"><span data-stu-id="0251f-195">[JSON reference for events from Social Engagement](event-hubs-json-reference-social-engagement.md)</span></span>  

   1.  <span data-ttu-id="0251f-196">Example 1: In this simple “Hello World” example, we count all new posts over time and push them every 30 seconds to the output sink.</span><span class="sxs-lookup"><span data-stu-id="0251f-196">Example 1: In this simple “Hello World” example, we count all new posts over time and push them every 30 seconds to the output sink.</span></span>  

       ```  
       SELECT  
           count (*) AS count,  
           System.TimeStamp AS Time  
       INTO  
           [your-output-sink-alias]  
       FROM  
           [your-stream-input-alias]  
       GROUP BY  
       TumblingWindow(second,30)  

       ```  

   2.  <span data-ttu-id="0251f-197">Example 2: In this example, we select unique publishers and their country/region information.</span><span class="sxs-lookup"><span data-stu-id="0251f-197">Example 2: In this example, we select unique publishers and their country/region information.</span></span> <span data-ttu-id="0251f-198">The results will get pushed to the output sink every 30 seconds.</span><span class="sxs-lookup"><span data-stu-id="0251f-198">The results will get pushed to the output sink every 30 seconds.</span></span>  

       ```  
       WITH current_window AS  
       (  
           SELECT  
               post.profile.profileLocation.adminDistrict,  
               post.profile.profileLocation.countryRegion,  
               count (*) AS count  
           FROM  
               [your-stream-input-alias]  
           GROUP BY  
               post.profile.profileLocation.adminDistrict,  
               post.profile.profileLocation.countryRegion,  
               TumblingWindow (second,30)  
       )  
       SELECT  
           *,  
           System.Timestamp AS Time  
       INTO  
           [your-output-sink-alias]  
       FROM   
           current_window  

       ``` 

   3.  <span data-ttu-id="0251f-199">Example 3: In this example, we select the name of a matching search topic in addition to the id, title, acquisition date and time, source name, and the content excerpt of posts.</span><span class="sxs-lookup"><span data-stu-id="0251f-199">Example 3: In this example, we select the name of a matching search topic in addition to the id, title, acquisition date and time, source name, and the content excerpt of posts.</span></span> <span data-ttu-id="0251f-200">We're using the [GetArrayElement function](https://msdn.microsoft.com/azure/stream-analytics/reference/getarrayelement-azure-stream-analytics) to select the first object of the [post.matchingSearchTopic](event-hubs-json-reference-social-engagement.md#document.matchingSeachTopics) array.</span><span class="sxs-lookup"><span data-stu-id="0251f-200">We're using the [GetArrayElement function](https://msdn.microsoft.com/azure/stream-analytics/reference/getarrayelement-azure-stream-analytics) to select the first object of the [post.matchingSearchTopic](event-hubs-json-reference-social-engagement.md#document.matchingSeachTopics) array.</span></span> <span data-ttu-id="0251f-201">To select all objects of the array, you can use the [GetArrayElements function](https://msdn.microsoft.com/azure/stream-analytics/reference/getarrayelements-azure-stream-analytics).</span><span class="sxs-lookup"><span data-stu-id="0251f-201">To select all objects of the array, you can use the [GetArrayElements function](https://msdn.microsoft.com/azure/stream-analytics/reference/getarrayelements-azure-stream-analytics).</span></span>

       ```
       WITH sub_query AS
       (
           SELECT
               post.id,
               post.title,
               post.acquisitionDate,
               post.source.param,
               post.sentiment.polarity,
               System.TimeStamp AS time,
               GetArrayElement(post.matchingSearchTopics, 0) AS SearchTopic,
               post.content.text
           FROM
               [your-stream-input-alias]
       )
       SELECT
           id,
           title,
           acquisitionDate,
           param AS source,
           polarity,
           time,
           SearchTopic.name AS topic,
           text
       INTO
           [your-output-sink-alias]
       FROM
           sub_query
       ```


<a name="step5_create_powerBI_dashboard"></a>   
### <a name="step-5-create-a-dashboard-in-power-bi"></a><span data-ttu-id="0251f-202">Step 5: Create a dashboard in Power BI</span><span class="sxs-lookup"><span data-stu-id="0251f-202">Step 5: Create a dashboard in Power BI</span></span>  
 <span data-ttu-id="0251f-203">Let’s close the loop.</span><span class="sxs-lookup"><span data-stu-id="0251f-203">Let’s close the loop.</span></span> <span data-ttu-id="0251f-204">Since our goal is to create a real-time dashboard in [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)], we need to make sure it receives data from [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)].</span><span class="sxs-lookup"><span data-stu-id="0251f-204">Since our goal is to create a real-time dashboard in [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)], we need to make sure it receives data from [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)].</span></span> <span data-ttu-id="0251f-205">When we defined the output sink, we authorized [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] with the [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)] job.</span><span class="sxs-lookup"><span data-stu-id="0251f-205">When we defined the output sink, we authorized [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] with the [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)] job.</span></span> <span data-ttu-id="0251f-206">A data set in [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] was already created.</span><span class="sxs-lookup"><span data-stu-id="0251f-206">A data set in [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] was already created.</span></span> <span data-ttu-id="0251f-207">Go to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] and select the data set you defined in step 4.5.</span><span class="sxs-lookup"><span data-stu-id="0251f-207">Go to [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] and select the data set you defined in step 4.5.</span></span> <span data-ttu-id="0251f-208">The name of the data set matches the name of your [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)] output sink.</span><span class="sxs-lookup"><span data-stu-id="0251f-208">The name of the data set matches the name of your [!INCLUDE[pn_stream_analytics](../includes/pn-stream-analytics.md)] output sink.</span></span>  

 <span data-ttu-id="0251f-209">In [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)], create a new visualization.</span><span class="sxs-lookup"><span data-stu-id="0251f-209">In [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)], create a new visualization.</span></span>  

1. <span data-ttu-id="0251f-210">For the example 1, in step 4, it’s a **line chart**.</span><span class="sxs-lookup"><span data-stu-id="0251f-210">For the example 1, in step 4, it’s a **line chart**.</span></span>  

   <span data-ttu-id="0251f-211">**Values:** *count*</span><span class="sxs-lookup"><span data-stu-id="0251f-211">**Values:** *count*</span></span>  

   <span data-ttu-id="0251f-212">**Axis:** *time*</span><span class="sxs-lookup"><span data-stu-id="0251f-212">**Axis:** *time*</span></span>  

   <span data-ttu-id="0251f-213">![Line chart in Microsoft Power BI](media/power-bi-simple-chart.png "Line chart in Microsoft Power BI")</span><span class="sxs-lookup"><span data-stu-id="0251f-213">![Line chart in Microsoft Power BI](media/power-bi-simple-chart.png "Line chart in Microsoft Power BI")</span></span>  

2. <span data-ttu-id="0251f-214">For the example 2, in step 4, we can select a map to visualize the data.</span><span class="sxs-lookup"><span data-stu-id="0251f-214">For the example 2, in step 4, we can select a map to visualize the data.</span></span>  

   <span data-ttu-id="0251f-215">**Location:** *countryregion* or *admindisctrict*</span><span class="sxs-lookup"><span data-stu-id="0251f-215">**Location:** *countryregion* or *admindisctrict*</span></span>  

   <span data-ttu-id="0251f-216">**Values:** *count*</span><span class="sxs-lookup"><span data-stu-id="0251f-216">**Values:** *count*</span></span>  

   <span data-ttu-id="0251f-217">There are almost unlimited options to combine data from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] with data from other applications or the Internet.</span><span class="sxs-lookup"><span data-stu-id="0251f-217">There are almost unlimited options to combine data from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] with data from other applications or the Internet.</span></span> <span data-ttu-id="0251f-218">The following picture shows you a [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] dashboard that correlates weather data with the different types of intentions from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]'s machine-learning based intention analysis.</span><span class="sxs-lookup"><span data-stu-id="0251f-218">The following picture shows you a [!INCLUDE[pn_power_bi](../includes/pn-power-bi.md)] dashboard that correlates weather data with the different types of intentions from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]'s machine-learning based intention analysis.</span></span>  

   <span data-ttu-id="0251f-219">![Power BI dashboard with Social Engagement intentions](media/power-bi-dashboard-event-hub.png "Power BI dashboard with Social Engagement intentions")</span><span class="sxs-lookup"><span data-stu-id="0251f-219">![Power BI dashboard with Social Engagement intentions](media/power-bi-dashboard-event-hub.png "Power BI dashboard with Social Engagement intentions")</span></span>  

<a name="privacy"></a>   
### <a name="privacy-notice"></a><span data-ttu-id="0251f-220">Privacy notice</span><span class="sxs-lookup"><span data-stu-id="0251f-220">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_mse_azure_event_hubs](../includes/cc-privacy-mse-azure-event-hubs.md)]  

### <a name="see-also"></a><span data-ttu-id="0251f-221">See Also</span><span class="sxs-lookup"><span data-stu-id="0251f-221">See Also</span></span>  
 <span data-ttu-id="0251f-222">[Stream data from Social Engagement to Microsoft Azure Event Hubs](stream-data-to-event-hubs.md) </span><span class="sxs-lookup"><span data-stu-id="0251f-222">[Stream data from Social Engagement to Microsoft Azure Event Hubs](stream-data-to-event-hubs.md) </span></span>  
 <span data-ttu-id="0251f-223">[JSON reference for events from Social Engagement](event-hubs-json-reference-social-engagement.md) </span><span class="sxs-lookup"><span data-stu-id="0251f-223">[JSON reference for events from Social Engagement](event-hubs-json-reference-social-engagement.md) </span></span>  
 <span data-ttu-id="0251f-224">[Manage connections in Social Engagement](manage-connections.md) </span><span class="sxs-lookup"><span data-stu-id="0251f-224">[Manage connections in Social Engagement](manage-connections.md) </span></span>  
 [<span data-ttu-id="0251f-225">Administer Microsoft Social Engagement</span><span class="sxs-lookup"><span data-stu-id="0251f-225">Administer Microsoft Social Engagement</span></span>](administer-microsoft-social-engagement.md)
