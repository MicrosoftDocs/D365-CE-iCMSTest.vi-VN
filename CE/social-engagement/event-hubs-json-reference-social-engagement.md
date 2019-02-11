---
title: JSON objects reference from Social Engagement | Microsoft Docs
description: Review the full list of properties and object in the Social Engagement payload for Event Hubs.
keywords: JSON, payload, metadata, event hubs, reference
ms.date: 08/22/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: 29a876d1-1915-3517-7ff0-cc357a156dec
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
ms.openlocfilehash: 9226f382ca154b72086a04d9370c3db28ea65d04
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375645"
---
# <a name="json-reference-for-events-from-includepnnetbreezeshortincludespn-social-engagement-shortmd"></a><span data-ttu-id="c6d59-104">JSON reference for events from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]</span><span class="sxs-lookup"><span data-stu-id="c6d59-104">JSON reference for events from [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]</span></span>
<span data-ttu-id="c6d59-105">This topic applies to version 2.1 of the JSON payload for social posts streamed to [!INCLUDE[pn_microsoft_azure_event_hubs](../includes/pn-microsoft-azure-event-hubs.md)] from [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-105">This topic applies to version 2.1 of the JSON payload for social posts streamed to [!INCLUDE[pn_microsoft_azure_event_hubs](../includes/pn-microsoft-azure-event-hubs.md)] from [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)].</span></span>  

<span data-ttu-id="c6d59-106">Latest version of the payload: Version 2.1</span><span class="sxs-lookup"><span data-stu-id="c6d59-106">Latest version of the payload: Version 2.1</span></span>  

> [!NOTE]
> <span data-ttu-id="c6d59-107">New objects and properties can get added to the payload without increasing the version number.</span><span class="sxs-lookup"><span data-stu-id="c6d59-107">New objects and properties can get added to the payload without increasing the version number.</span></span>

<span data-ttu-id="c6d59-108">For more information about getting a connection between [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] and [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)] up and running, see [Stream data from Social Engagement to Microsoft Azure Event Hubs](stream-data-to-event-hubs.md).</span><span class="sxs-lookup"><span data-stu-id="c6d59-108">For more information about getting a connection between [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] and [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)] up and running, see [Stream data from Social Engagement to Microsoft Azure Event Hubs](stream-data-to-event-hubs.md).</span></span>  

<a name="overview"></a>   
## <a name="overview"></a><span data-ttu-id="c6d59-109">Overview</span><span class="sxs-lookup"><span data-stu-id="c6d59-109">Overview</span></span>  
<span data-ttu-id="c6d59-110">When [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] streams events to [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)], a JSON payload is generated.</span><span class="sxs-lookup"><span data-stu-id="c6d59-110">When [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] streams events to [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)], a JSON payload is generated.</span></span> <span data-ttu-id="c6d59-111">A single social post in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] is a single event in the event hub.</span><span class="sxs-lookup"><span data-stu-id="c6d59-111">A single social post in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] is a single event in the event hub.</span></span> <span data-ttu-id="c6d59-112">The JSON payload contains information about a single social post that matches the defined filters and action on the automation rules that generated the payload.</span><span class="sxs-lookup"><span data-stu-id="c6d59-112">The JSON payload contains information about a single social post that matches the defined filters and action on the automation rules that generated the payload.</span></span> <span data-ttu-id="c6d59-113">Additional properties that you define in your automation rules are part of the [metadata object](#metadataProperties).</span><span class="sxs-lookup"><span data-stu-id="c6d59-113">Additional properties that you define in your automation rules are part of the [metadata object](#metadataProperties).</span></span> <span data-ttu-id="c6d59-114">The main content is part of the [post object](#documentProperties).</span><span class="sxs-lookup"><span data-stu-id="c6d59-114">The main content is part of the [post object](#documentProperties).</span></span>  

<a name="metadataProperties"></a>   
### <a name="metadata-object-elements"></a><span data-ttu-id="c6d59-115">metadata object elements</span><span class="sxs-lookup"><span data-stu-id="c6d59-115">metadata object elements</span></span>  
<span data-ttu-id="c6d59-116">Use this table to get a quick link to metadata object properties.</span><span class="sxs-lookup"><span data-stu-id="c6d59-116">Use this table to get a quick link to metadata object properties.</span></span>  


|                            <span data-ttu-id="c6d59-117">JSON element</span><span class="sxs-lookup"><span data-stu-id="c6d59-117">JSON element</span></span>                             |                                                           <span data-ttu-id="c6d59-118">Description</span><span class="sxs-lookup"><span data-stu-id="c6d59-118">Description</span></span>                                                            |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
|             [<span data-ttu-id="c6d59-119">Metadata JSON payload objects</span><span class="sxs-lookup"><span data-stu-id="c6d59-119">Metadata JSON payload objects</span></span>](#metadata)              | <span data-ttu-id="c6d59-120">JSON object describing the metadata for the payload sent to [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-120">JSON object describing the metadata for the payload sent to [!INCLUDE[pn_azure_event_hubs](../includes/pn-azure-event-hubs.md)].</span></span> |
|           [<span data-ttu-id="c6d59-121">metadata.matchedRules</span><span class="sxs-lookup"><span data-stu-id="c6d59-121">metadata.matchedRules</span></span>](#metadata.matchedrules)           |                                        <span data-ttu-id="c6d59-122">Array of automation rules that matched this post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-122">Array of automation rules that matched this post.</span></span>                                         |
|        [<span data-ttu-id="c6d59-123">metadata.matchedRules.id</span><span class="sxs-lookup"><span data-stu-id="c6d59-123">metadata.matchedRules.id</span></span>](#metadata.matchedrules.id)        |                           <span data-ttu-id="c6d59-124">ID of the automation rule that triggered the creation of this JSON payload.</span><span class="sxs-lookup"><span data-stu-id="c6d59-124">ID of the automation rule that triggered the creation of this JSON payload.</span></span>                            |
|      [<span data-ttu-id="c6d59-125">metadata.matchedRules.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-125">metadata.matchedRules.name</span></span>](#metadata.matchedrules.name)      |                          <span data-ttu-id="c6d59-126">Name of the automation rule that triggered the creation of this JSON payload.</span><span class="sxs-lookup"><span data-stu-id="c6d59-126">Name of the automation rule that triggered the creation of this JSON payload.</span></span>                           |
|             [<span data-ttu-id="c6d59-127">metadata.properties</span><span class="sxs-lookup"><span data-stu-id="c6d59-127">metadata.properties</span></span>](#metadata.properties)             |    <span data-ttu-id="c6d59-128">Array of key-value pairs defined in the additional properties of the "Stream to Event Hubs" action in an automation rule.</span><span class="sxs-lookup"><span data-stu-id="c6d59-128">Array of key-value pairs defined in the additional properties of the "Stream to Event Hubs" action in an automation rule.</span></span>     |
|         [<span data-ttu-id="c6d59-129">metadata.properties.key</span><span class="sxs-lookup"><span data-stu-id="c6d59-129">metadata.properties.key</span></span>](#metadata.properties.key)         |                         <span data-ttu-id="c6d59-130">Key of a key-value pair provided in additional properties of an automation rule.</span><span class="sxs-lookup"><span data-stu-id="c6d59-130">Key of a key-value pair provided in additional properties of an automation rule.</span></span>                         |
|       [<span data-ttu-id="c6d59-131">metadata.properties.value</span><span class="sxs-lookup"><span data-stu-id="c6d59-131">metadata.properties.value</span></span>](#metadata.properties.value)       |                        <span data-ttu-id="c6d59-132">Value of a key-value pair provided in additional properties of an automation rule.</span><span class="sxs-lookup"><span data-stu-id="c6d59-132">Value of a key-value pair provided in additional properties of an automation rule.</span></span>                        |
| [<span data-ttu-id="c6d59-133">metadata.properties.matchedrule</span><span class="sxs-lookup"><span data-stu-id="c6d59-133">metadata.properties.matchedrule</span></span>](#metadata.properties.matchedrule) |                                <span data-ttu-id="c6d59-134">ID of the automation rule that contains the additional properties</span><span class="sxs-lookup"><span data-stu-id="c6d59-134">ID of the automation rule that contains the additional properties</span></span>                                 |

<span data-ttu-id="c6d59-135">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-135">Back to [top](#overview)</span></span>  

<a name="metadata_sample_payload"></a>   
#### <a name="metadata-sample-payload"></a><span data-ttu-id="c6d59-136">metadata sample payload</span><span class="sxs-lookup"><span data-stu-id="c6d59-136">metadata sample payload</span></span>  

```json  
{  
  "metadata": {  
    "matchedRules": [  
      {  
        "id": 12345,  
        "name": "Support Requests"  
      },  
      {  
        "id": 54321,  
        "name": "Company News"  
      }  
    ],  
    "properties": [  
      {  
        "key": "customKey_1",  
        "value": "Some custom value.",  
        "matchedRule": 12345  
        },  

      {  
        "key": "customKey_2",  
        "value": "Some other custom value.",  
        "matchedRule": 54321  
      }  
    ]  
  }  

```  

<span data-ttu-id="c6d59-137">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-137">Back to [top](#overview)</span></span>  

<a name="documentProperties"></a>   
### <a name="post-object-elements"></a><span data-ttu-id="c6d59-138">post object elements</span><span class="sxs-lookup"><span data-stu-id="c6d59-138">post object elements</span></span>  
<span data-ttu-id="c6d59-139">Use this table to get a quick link to post object properties.</span><span class="sxs-lookup"><span data-stu-id="c6d59-139">Use this table to get a quick link to post object properties.</span></span>  


|                        <span data-ttu-id="c6d59-140">JSON element</span><span class="sxs-lookup"><span data-stu-id="c6d59-140">JSON element</span></span>                        |                                                                     <span data-ttu-id="c6d59-141">Description</span><span class="sxs-lookup"><span data-stu-id="c6d59-141">Description</span></span>                                                                      |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|                  [<span data-ttu-id="c6d59-142">post.id</span><span class="sxs-lookup"><span data-stu-id="c6d59-142">post.id</span></span>](#document.id)                   |                <span data-ttu-id="c6d59-143">The unique post ID in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.</span><span class="sxs-lookup"><span data-stu-id="c6d59-143">The unique post ID in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.</span></span>                |
|         [<span data-ttu-id="c6d59-144">post.contentType</span><span class="sxs-lookup"><span data-stu-id="c6d59-144">post.contentType</span></span>](#document.contentType)          |                                                            <span data-ttu-id="c6d59-145">The type of content in a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-145">The type of content in a post.</span></span>                                                            |
|            [<span data-ttu-id="c6d59-146">post.postType</span><span class="sxs-lookup"><span data-stu-id="c6d59-146">post.postType</span></span>](#document.postType)             |                                                 <span data-ttu-id="c6d59-147">The type of the post in its conversational context.</span><span class="sxs-lookup"><span data-stu-id="c6d59-147">The type of the post in its conversational context.</span></span>                                                  |
|                 [<span data-ttu-id="c6d59-148">post.uri</span><span class="sxs-lookup"><span data-stu-id="c6d59-148">post.uri</span></span>](#document.uri)                  |                                                <span data-ttu-id="c6d59-149">The post's URI—a  backlink to the post's original URI.</span><span class="sxs-lookup"><span data-stu-id="c6d59-149">The post's URI—a  backlink to the post's original URI.</span></span>                                                |
|               [<span data-ttu-id="c6d59-150">post.title</span><span class="sxs-lookup"><span data-stu-id="c6d59-150">post.title</span></span>](#document.title)                |                                                <span data-ttu-id="c6d59-151">The title as delivered from a post's meta information.</span><span class="sxs-lookup"><span data-stu-id="c6d59-151">The title as delivered from a post's meta information.</span></span>                                                |
|     [<span data-ttu-id="c6d59-152">post.acquisitionDate</span><span class="sxs-lookup"><span data-stu-id="c6d59-152">post.acquisitionDate</span></span>](#document.acquisitionDate)      |       <span data-ttu-id="c6d59-153">Timestamp when the post was acquired in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).</span><span class="sxs-lookup"><span data-stu-id="c6d59-153">Timestamp when the post was acquired in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).</span></span>        |
|    [<span data-ttu-id="c6d59-154">post.modificationDate</span><span class="sxs-lookup"><span data-stu-id="c6d59-154">post.modificationDate</span></span>](#document.modificationDate)     |     <span data-ttu-id="c6d59-155">Timestamp when  the post was last updated in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).</span><span class="sxs-lookup"><span data-stu-id="c6d59-155">Timestamp when  the post was last updated in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).</span></span>     |
|     [<span data-ttu-id="c6d59-156">post.publicationDate</span><span class="sxs-lookup"><span data-stu-id="c6d59-156">post.publicationDate</span></span>](#document.publicationDate)      |                                      <span data-ttu-id="c6d59-157">Timestamp when the post was published on the source (in ISO 8601 format).</span><span class="sxs-lookup"><span data-stu-id="c6d59-157">Timestamp when the post was published on the source (in ISO 8601 format).</span></span>                                       |
|             [<span data-ttu-id="c6d59-158">post.profile</span><span class="sxs-lookup"><span data-stu-id="c6d59-158">post.profile</span></span>](#document.profile)              |                                           <span data-ttu-id="c6d59-159">JSON object describing the social profile of the post's author.</span><span class="sxs-lookup"><span data-stu-id="c6d59-159">JSON object describing the social profile of the post's author.</span></span>                                            |
|              [<span data-ttu-id="c6d59-160">post.source</span><span class="sxs-lookup"><span data-stu-id="c6d59-160">post.source</span></span>](#document.source)               |                                               <span data-ttu-id="c6d59-161">JSON object describing on which source a post was found.</span><span class="sxs-lookup"><span data-stu-id="c6d59-161">JSON object describing on which source a post was found.</span></span>                                               |
|             [<span data-ttu-id="c6d59-162">post.content</span><span class="sxs-lookup"><span data-stu-id="c6d59-162">post.content</span></span>](#document.content)              |                                                    <span data-ttu-id="c6d59-163">JSON object describing the content of a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-163">JSON object describing the content of a post.</span></span>                                                     |
|            [<span data-ttu-id="c6d59-164">post.language</span><span class="sxs-lookup"><span data-stu-id="c6d59-164">post.language</span></span>](#document.language)             |                                                    <span data-ttu-id="c6d59-165">JSON object describing the language of a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-165">JSON object describing the language of a post.</span></span>                                                    |
|        [<span data-ttu-id="c6d59-166">post.abstractText</span><span class="sxs-lookup"><span data-stu-id="c6d59-166">post.abstractText</span></span>](#document.abstractText)         |                                                              <span data-ttu-id="c6d59-167">Short excerpt of the post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-167">Short excerpt of the post.</span></span>                                                              |
|               [<span data-ttu-id="c6d59-168">post.score</span><span class="sxs-lookup"><span data-stu-id="c6d59-168">post.score</span></span>](#document.score)                |               <span data-ttu-id="c6d59-169">JSON object describing the source specific score of the post or score of the author at the time the post was published.</span><span class="sxs-lookup"><span data-stu-id="c6d59-169">JSON object describing the source specific score of the post or score of the author at the time the post was published.</span></span>                |
|      [<span data-ttu-id="c6d59-170">post.referencedPost</span><span class="sxs-lookup"><span data-stu-id="c6d59-170">post.referencedPost</span></span>](#document.referencedPost)       |                                       <span data-ttu-id="c6d59-171">Information about the post that this post is a reply to, or a share of.</span><span class="sxs-lookup"><span data-stu-id="c6d59-171">Information about the post that this post is a reply to, or a share of.</span></span>                                        |
|           [<span data-ttu-id="c6d59-172">post.sentiment</span><span class="sxs-lookup"><span data-stu-id="c6d59-172">post.sentiment</span></span>](#document.sentiment)            |                                                   <span data-ttu-id="c6d59-173">JSON object describing the sentiment of a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-173">JSON object describing the sentiment of a post.</span></span>                                                    |
|                [<span data-ttu-id="c6d59-174">post.tags</span><span class="sxs-lookup"><span data-stu-id="c6d59-174">post.tags</span></span>](#document.tags)                 | <span data-ttu-id="c6d59-175">Array of JSON objects representing tags on a post that were added through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-175">Array of JSON objects representing tags on a post that were added through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> |
|          [<span data-ttu-id="c6d59-176">post.externalId</span><span class="sxs-lookup"><span data-stu-id="c6d59-176">post.externalId</span></span>](#document.externalId)           |                                                            <span data-ttu-id="c6d59-177">ID of the post on the source.</span><span class="sxs-lookup"><span data-stu-id="c6d59-177">ID of the post on the source.</span></span>                                                             |
|        [<span data-ttu-id="c6d59-178">post.postLocation</span><span class="sxs-lookup"><span data-stu-id="c6d59-178">post.postLocation</span></span>](#document.postLocation)         |                                          <span data-ttu-id="c6d59-179">JSON object describing the location on which a post was published.</span><span class="sxs-lookup"><span data-stu-id="c6d59-179">JSON object describing the location on which a post was published.</span></span>                                          |
|   [<span data-ttu-id="c6d59-180">post.fullContentLength</span><span class="sxs-lookup"><span data-stu-id="c6d59-180">post.fullContentLength</span></span>](#document.fullContentLenght)    |                                                    <span data-ttu-id="c6d59-181">Length in characters of a post's text content.</span><span class="sxs-lookup"><span data-stu-id="c6d59-181">Length in characters of a post's text content.</span></span>                                                    |
|              [<span data-ttu-id="c6d59-182">post.origin</span><span class="sxs-lookup"><span data-stu-id="c6d59-182">post.origin</span></span>](#document.origin)               |                     <span data-ttu-id="c6d59-183">JSON object describing the origin of a content.</span><span class="sxs-lookup"><span data-stu-id="c6d59-183">JSON object describing the origin of a content.</span></span> <span data-ttu-id="c6d59-184">For example: Facebook page on which the post was published.</span><span class="sxs-lookup"><span data-stu-id="c6d59-184">For example: Facebook page on which the post was published.</span></span>                      |
| [<span data-ttu-id="c6d59-185">post.matchingSearchTopics</span><span class="sxs-lookup"><span data-stu-id="c6d59-185">post.matchingSearchTopics</span></span>](#document.matchingSeachTopics) |                                      <span data-ttu-id="c6d59-186">Array of JSON objects describing the list of search topics a post matches.</span><span class="sxs-lookup"><span data-stu-id="c6d59-186">Array of JSON objects describing the list of search topics a post matches.</span></span>                                      |
|  [<span data-ttu-id="c6d59-187">post.externalCategories</span><span class="sxs-lookup"><span data-stu-id="c6d59-187">post.externalCategories</span></span>](#document.externalCategories)   |                                                <span data-ttu-id="c6d59-188">Array of categories as delivered by the data provider.</span><span class="sxs-lookup"><span data-stu-id="c6d59-188">Array of categories as delivered by the data provider.</span></span>                                                |
|        [<span data-ttu-id="c6d59-189">post.contributors</span><span class="sxs-lookup"><span data-stu-id="c6d59-189">post.contributors</span></span>](#document.contributors)         |                                <span data-ttu-id="c6d59-190">Array of names of those who contributed to the post as provided by the data provider.</span><span class="sxs-lookup"><span data-stu-id="c6d59-190">Array of names of those who contributed to the post as provided by the data provider.</span></span>                                 |
|               [<span data-ttu-id="c6d59-191">post.media</span><span class="sxs-lookup"><span data-stu-id="c6d59-191">post.media</span></span>](#document.media)                |                                                <span data-ttu-id="c6d59-192">Array of JSON objects describing the media in a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-192">Array of JSON objects describing the media in a post.</span></span>                                                 |
|      [<span data-ttu-id="c6d59-193">post.externalTopics</span><span class="sxs-lookup"><span data-stu-id="c6d59-193">post.externalTopics</span></span>](#document.externalTopics)       |                                            <span data-ttu-id="c6d59-194">Array of topics in this post as defined by the data provider.</span><span class="sxs-lookup"><span data-stu-id="c6d59-194">Array of topics in this post as defined by the data provider.</span></span>                                             |
|  [<span data-ttu-id="c6d59-195">post.contributorSummary</span><span class="sxs-lookup"><span data-stu-id="c6d59-195">post.contributorSummary</span></span>](#document.contributorSummary)   |                              <span data-ttu-id="c6d59-196">Short description about the contributor for this post as delivered by external providers.</span><span class="sxs-lookup"><span data-stu-id="c6d59-196">Short description about the contributor for this post as delivered by external providers.</span></span>                               |

<span data-ttu-id="c6d59-197">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-197">Back to [top](#overview)</span></span>  

<a name="document_sample_payload"></a>   
#### <a name="post-sample-payload"></a><span data-ttu-id="c6d59-198">post sample payload</span><span class="sxs-lookup"><span data-stu-id="c6d59-198">post sample payload</span></span>  

<a name="sampleTwitterReply"></a>   
##### <a name="sample-twitter-reply"></a><span data-ttu-id="c6d59-199">Sample Twitter reply</span><span class="sxs-lookup"><span data-stu-id="c6d59-199">Sample Twitter reply</span></span>  
<span data-ttu-id="c6d59-200">This is a sample post payload for a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] reply acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-200">This is a sample post payload for a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] reply acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> <span data-ttu-id="c6d59-201">We've made up some values to anonymize the sample.</span><span class="sxs-lookup"><span data-stu-id="c6d59-201">We've made up some values to anonymize the sample.</span></span>  

```json  
  "post": {  
    "id": "1234567",  
    "contentType": "POST",  
    "postType": "reply",  
    "uri": "http://twitter.com/externalHandle/status/1234567890",  
    "publicationDate": "2016-01-23T12:34:56.789+0000",  
    "acquisitionDate": "2016-01-23T12:34:56.789+0000",  
    "modificationDate": "2016-01-23T12:34:56.789+0000",  
    "profile": {  
      "name": "Display Name @chosenUserName",  
      "id": "mse-tw://#12345678",
      "uri": "mse-tw://#12345678",  
      "profileIcon": "https://path/to/the/profileIcon.png",  
      "externalHandle": "chosenUserName",  
      "displayName": "Display Name",  
      "externalId": "7654321"  
    },  
    "source": {  
      "name": "Microblogs",  
      "id": "18",  
      "param": "Twitter"  
    },  
    "content": {  
      "text": "Main text content of the tweet."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Main text content of the tweet.",  
    "score": {  
      "normalScore": 3,  
      "providerScore": 29.0,  
      "provider": "KLOUT"  
    },  
    "referencedPost": {  
      "profile": {  
        "displayName": "Referenced Display Name",  
        "id": "987654321"  
      },  
      "externalId": "123456789",  
    },  
    "sentiment": {  
      "polarity": "negative",  
      "value": -0.46005836  
    },  
        "tags": [  
          {  
            "probability": 0.8339088,  
            "type": "system",  
            "tag": {  
              "name": "Information request",  
              "id": "2473",  
              "parentId": "2470"  
            }  
          }  
        ],  
    "externalId": "12345ab54321",  
    "fullContentLength": 137,  
    "matchingSearchTopics": [  
      {  
        "id": "1234567",  
        "name": "Contoso search topic",  
        "parentId": "7654321"  
      }  
    ],  
  }  
}  

```  

<span data-ttu-id="c6d59-202">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-202">Back to [top](#overview)</span></span>  

<a name="sampleTwitterRetweet"></a>   
##### <a name="sample-twitter-retweet"></a><span data-ttu-id="c6d59-203">Sample Twitter retweet</span><span class="sxs-lookup"><span data-stu-id="c6d59-203">Sample Twitter retweet</span></span>  
<span data-ttu-id="c6d59-204">This is a sample post payload for a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] retweet acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-204">This is a sample post payload for a [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] retweet acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> <span data-ttu-id="c6d59-205">We've made up some values to anonymize the sample.</span><span class="sxs-lookup"><span data-stu-id="c6d59-205">We've made up some values to anonymize the sample.</span></span>  

```json  
  "post": {  
    "id": "5786261",  
    "contentType": "POST",  
    "postType": "share",  
    "uri": "http://twitter.com/externalHandle/statuses/1234567890",  
    "publicationDate": "2016-01-23T12:34:56-07:00",  
    "acquisitionDate": "2016-01-23T12:34:56-07:00",  
    "modificationDate": "2016-01-23T12:34:56-07:00",  
    "profile": {  
      "name": "Display Name @chosenUserName",  
      "id": "mse-tw://#12345678",
      "uri": "mse-tw://#12345678",  
      "profileIcon": "https://path/to/the/profileIcon.png",  
      "externalHandle": "chosenUserName",  
      "displayName": "Display Name",  
      "externalId": "7654321"  
    },  
    "source": {  
      "name": "Microblogs",  
      "id": "18",  
      "param": "Twitter"  
    },  
    "content": {  
      "text": "Main text of the tweet."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Main text of the tweet.",  
    "score": {  
      "normalScore": 4,  
      "providerScore": 46.0,  
      "provider": "KLOUT"  
    },  
    "referencedPost": {  
      "profile": {  
        "name": "Display Name of retweeted profile @anotherChosenUserName",  
        "profileIcon": "https://path/to/the/profileIcon.png",  
        "externalHandle": "anotherChosenUserName",  
        "displayName": "Display Name of retweeted profile"  
      },  
      "externalId": "123456789"  
    },  
    "sentiment": {  
      "polarity": "negative",  
      "value": -0.6864638  
    },  
    "tags": [  
      {  
        "probability": 0.8339088,  
        "type": "system",  
        "tag": {  
          "name": "Information request",  
          "id": "2473",  
          "parentId": "2470"  
        }  
      }  
    ],  
    "externalId": "12345ab54321",  
    "fullContentLength": 139,  
    "matchingSearchTopics": [  
      {  
        "name": "Contoso search topic",  
        "id": "12345",  
        "parentId": "54321"  
      }  
    ]  
  }  
}  

```  

<span data-ttu-id="c6d59-206">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-206">Back to [top](#overview)</span></span>  

<a name="sampleFacebookReply"></a>   
##### <a name="sample-facebook-reply"></a><span data-ttu-id="c6d59-207">Sample Facebook reply</span><span class="sxs-lookup"><span data-stu-id="c6d59-207">Sample Facebook reply</span></span>  
<span data-ttu-id="c6d59-208">This is a sample post payload for a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] reply acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-208">This is a sample post payload for a [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] reply acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> <span data-ttu-id="c6d59-209">We've made up some values to anonymize the sample.</span><span class="sxs-lookup"><span data-stu-id="c6d59-209">We've made up some values to anonymize the sample.</span></span>  

```json  
  "post": {  
    "id": "1234567",  
    "contentType": "POST",  
    "postType": "reply",  
    "uri": "http://www.facebook.com/123456789/posts/987654321?comment_id=123123123",  
    "publicationDate": "2016-01-23T12:34:56-07:00",  
    "acquisitionDate": "2016-01-23T12:34:56-07:00",  
    "modificationDate": "2016-01-23T12:34:56-07:00",  
    "profile": {  
      "name": "Name of the profile",  
      "id": "mse-fb://#109826384650057",
      "uri": "mse-fb://#109826384650057",  
      "profileIcon": "http://graph.facebook.com/123456789/picture?type=square",  
      "externalId": "123456789"  
    },  
    "source": {  
      "name": "Facebook Posts",  
      "id": "16",  
      "param": "Facebook"  
    },  
    "content": {  
      "text": "Text as provided for the reply. This is usually a text that contains several sentences. This example highlights the difference between post.content and post.abstractText."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Text as provided for the reply. This is usually a",  
    "referencedPost": {  
      "externalId": "987654321"  
    },  
    "sentiment": {  
      "polarity": "neutral",  
      "value": -0.0023945  
    },  
    "externalId": "321321321",  
    "fullContentLength": 227,  
    "origin": {  
      "id": "12345",  
      "externalId": "123456789"  
    },  
    "matchingSearchTopics": [  
      {  
        "name": "Contoso search topic",  
        "id": "12345",  
        "parentId": "54321"  
      }  
    ]  
  }  
}  

```  

<span data-ttu-id="c6d59-210">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-210">Back to [top](#overview)</span></span>  

<a name="sampleVideoPost"></a>   
##### <a name="sample-video-post"></a><span data-ttu-id="c6d59-211">Sample video post</span><span class="sxs-lookup"><span data-stu-id="c6d59-211">Sample video post</span></span>  
<span data-ttu-id="c6d59-212">This is a sample post payload for a video post acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-212">This is a sample post payload for a video post acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> <span data-ttu-id="c6d59-213">We've made up some values to anonymize the sample.</span><span class="sxs-lookup"><span data-stu-id="c6d59-213">We've made up some values to anonymize the sample.</span></span>  

```json  
  "post": {  
    "id": "1234567",  
    "contentType": "VIDEO",  
    "postType": "post",  
    "uri": "http://www.youtube.com/watch?v=videoId",  
    "title": "Title of the video",  
    "publicationDate": "2016-01-23T12:34:56-07:00",  
    "acquisitionDate": "2016-01-23T12:34:56-07:00",  
    "modificationDate": "2016-01-23T12:34:56-07:00",  
    "profile": {  
      "name": "Name of the profile",  
      "id": "mse-vd://#UUFSerfsZZt-sdER", 
      "uri": "mse-vd://#UUFSerfsZZt-sdER", 
      "externalId": "98765abc4321"  
    },  
    "source": {  
      "name": "Youtube Videos",  
      "id": "19",  
      "param": "YoutubeVideos"  
    },  
    "content": {  
      "text": "Text description as provided for the video. This is usually a text that contains several sentences. This example highlights the difference between post.content and post.abstractText."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Text description as provided for the video. This is usually a",  
    "embeddedMedia": "http://www.youtube.com/embed/videoId",  
    "media": [  
      {  
        "type": "VIDEO",  
        "embedUrl": "http://www.youtube.com/embed/videoId"  
      }  
    ],  
    "sentiment": {  
      "polarity": "neutral",  
      "value": -0.07142752  
    },  
    "fullContentLength": 358,  
    "matchingSearchTopics": [  
      {  
        "name": "Contoso search topic",  
        "id": "12345",  
        "parentId": "54321"  
      }  
    ]  
  }  
}  

```  

<span data-ttu-id="c6d59-214">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-214">Back to [top](#overview)</span></span>  

<a name="sampleBlogPost"></a>   
##### <a name="sample-blog-post"></a><span data-ttu-id="c6d59-215">Sample blog post</span><span class="sxs-lookup"><span data-stu-id="c6d59-215">Sample blog post</span></span>  
<span data-ttu-id="c6d59-216">This is a sample post payload for a blog post acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-216">This is a sample post payload for a blog post acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> <span data-ttu-id="c6d59-217">We've made up some values to anonymize the sample.</span><span class="sxs-lookup"><span data-stu-id="c6d59-217">We've made up some values to anonymize the sample.</span></span>  

```json  
  "post": {  
    "id": "1234567",  
    "contentType": "POST",  
    "postType": "post",  
    "uri": "http://someblog.tld/path/to/post",  
    "title": "Heading of this blog",  
    "acquisitionDate": "2016-01-23T12:34:56.789+0000",  
    "modificationDate": "2016-01-23T12:34:56.789+0000",  
    "publicationDate": "2016-01-23T12:34:56.789+0000",  
    "profile": {  
      "name": "Name of the profile",  
      "id": "mse-bl://contoso-blog.tumblr.com#1234567", 
      "uri": "mse-bl://contoso-blog.tumblr.com#1234567", 
      "externalId": "987654321"  
    },  
    "source": {  
      "name": "Blogs",  
      "id": "14",  
      "param": "Blogs"  
    },  
    "content": {  
      "text": "Main text content of the blog post. This is usually a text that contains several sentences. This example highlights the difference between post.content.text and post.abstractText."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Main text content of the blog post. This is usually a text that",  
    "sentiment": {  
      "polarity": "positive",  
      "value": 0.3150851  
    },  
    "externalId":"123456789abcd987654321",  
    "fullContentLength": 119,  
    "matchingSearchTopics": [  
      {  
        "id": "1234567",  
        "name": "Contoso search topic",  
        "parentId": "7654321"  
      }  
    ]  
  }  
}  

```  

<span data-ttu-id="c6d59-218">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-218">Back to [top](#overview)</span></span>  

<a name="sampleForumPost"></a>   
##### <a name="sample-forum-post"></a><span data-ttu-id="c6d59-219">Sample forum post</span><span class="sxs-lookup"><span data-stu-id="c6d59-219">Sample forum post</span></span>  
<span data-ttu-id="c6d59-220">This is a sample post payload for a forum post acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-220">This is a sample post payload for a forum post acquired through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> <span data-ttu-id="c6d59-221">We've made up some values to anonymize the sample.</span><span class="sxs-lookup"><span data-stu-id="c6d59-221">We've made up some values to anonymize the sample.</span></span>  

```json  
  "post": {  
    "id": "1234567",  
    "contentType": "POST",  
    "postType": "reply",  
    "uri": "http://forumdomain.tld/path/to/the/forum",  
    "publicationDate": "2016-01-23T12:34:56.789+0000",  
    "acquisitionDate": "2016-01-23T12:34:56.789+0000",  
    "modificationDate": "2016-01-23T12:34:56.789+0000",  
    "profile": {  
      "name": "Name of the profile",  
      "id": "mse-bd://forumdomain.tld#someuser", 
      "uri": "mse-bd://forumdomain.tld#someuser", 
      "displayName": "Name of the profile",  
      "externalHandle": "Name of the profile",  
      "externalId": "987654321"  
    },  
    "source": {  
      "name": "Board",  
      "id": "15",  
      "param": "Board"  
    },  
    "content": {  
      "text": "Main text content of the forum post."  
    },  
    "language": {  
      "name": "English",  
      "code": "en"  
    },  
    "abstractText": "Abstract text of the forum post.",  
    "referencedPost": {  
      "externalId":"123456789abcd987654321",  
    },  
    "sentiment": {  
      "polarity": "positive",  
      "value": 0.3773585  
    },  
    "externalId":"123456789abcd987654321",  
    "fullContentLength": 398,  
    "origin": {  
      "externalId":"123ab321",  
      "name":"Title of the forum",  
    },  
    "matchingSearchTopics": [  
      {  
        "id": "1234567",  
        "name": "Contoso search topic",  
        "parentId": "7654321"  
      }  
    ],  
  }  
}  

```  

<span data-ttu-id="c6d59-222">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-222">Back to [top](#overview)</span></span>  

<a name="metadata"></a>   
## <a name="metadata-json-payload-objects"></a><span data-ttu-id="c6d59-223">Metadata JSON payload objects</span><span class="sxs-lookup"><span data-stu-id="c6d59-223">Metadata JSON payload objects</span></span>  
<span data-ttu-id="c6d59-224">Read up on the fields currently supported in the metadata JSON payload.</span><span class="sxs-lookup"><span data-stu-id="c6d59-224">Read up on the fields currently supported in the metadata JSON payload.</span></span>  

<a name="metadata.matchedrules"></a>   
### <a name="metadatamatchedrules"></a><span data-ttu-id="c6d59-225">metadata.matchedRules</span><span class="sxs-lookup"><span data-stu-id="c6d59-225">metadata.matchedRules</span></span>  
<span data-ttu-id="c6d59-226">Array describing the automation rules that match this post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-226">Array describing the automation rules that match this post.</span></span>  

 <span data-ttu-id="c6d59-227">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-227">Property Value Type: object</span></span>  

 <span data-ttu-id="c6d59-228">Parent: *metadata*</span><span class="sxs-lookup"><span data-stu-id="c6d59-228">Parent: *metadata*</span></span>  

 <span data-ttu-id="c6d59-229">Sample: [metadata sample payload](#metadata_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-229">Sample: [metadata sample payload](#metadata_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-230">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-230">Back to [top](#overview)</span></span>  

<a name="metadata.matchedrules.id"></a>   
#### <a name="metadatamatchedrulesid"></a><span data-ttu-id="c6d59-231">metadata.matchedRules.id</span><span class="sxs-lookup"><span data-stu-id="c6d59-231">metadata.matchedRules.id</span></span>  
<span data-ttu-id="c6d59-232">ID of the automation rule that triggered the creation of this JSON payload.</span><span class="sxs-lookup"><span data-stu-id="c6d59-232">ID of the automation rule that triggered the creation of this JSON payload.</span></span>  

 <span data-ttu-id="c6d59-233">Property Value Type: number (integer)</span><span class="sxs-lookup"><span data-stu-id="c6d59-233">Property Value Type: number (integer)</span></span>  

 <span data-ttu-id="c6d59-234">Parent: *metadata.matchedRules*</span><span class="sxs-lookup"><span data-stu-id="c6d59-234">Parent: *metadata.matchedRules*</span></span>  

 <span data-ttu-id="c6d59-235">Sample: [metadata sample payload](#metadata_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-235">Sample: [metadata sample payload](#metadata_sample_payload)</span></span>  

<a name="metadata.matchedrules.name"></a>   
#### <a name="metadatamatchedrulesname"></a><span data-ttu-id="c6d59-236">metadata.matchedRules.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-236">metadata.matchedRules.name</span></span>  
<span data-ttu-id="c6d59-237">Name of the automation rule that triggered the creation of this JSON payload.</span><span class="sxs-lookup"><span data-stu-id="c6d59-237">Name of the automation rule that triggered the creation of this JSON payload.</span></span>  

 <span data-ttu-id="c6d59-238">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-238">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-239">Parent: *metadata.matchedRules*</span><span class="sxs-lookup"><span data-stu-id="c6d59-239">Parent: *metadata.matchedRules*</span></span>  

 <span data-ttu-id="c6d59-240">Sample: [metadata sample payload](#metadata_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-240">Sample: [metadata sample payload](#metadata_sample_payload)</span></span>  

<a name="metadata.properties"></a>   
### <a name="metadataproperties"></a><span data-ttu-id="c6d59-241">metadata.properties</span><span class="sxs-lookup"><span data-stu-id="c6d59-241">metadata.properties</span></span>  
<span data-ttu-id="c6d59-242">Array of key-value pairs defined in the additional properties of the "Stream to Event Hubs" action in an automation rule.</span><span class="sxs-lookup"><span data-stu-id="c6d59-242">Array of key-value pairs defined in the additional properties of the "Stream to Event Hubs" action in an automation rule.</span></span>  

 <span data-ttu-id="c6d59-243">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-243">Property Value Type: object</span></span>  

 <span data-ttu-id="c6d59-244">Parent: *metadata*</span><span class="sxs-lookup"><span data-stu-id="c6d59-244">Parent: *metadata*</span></span>  

 <span data-ttu-id="c6d59-245">Sample: [metadata sample payload](#metadata_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-245">Sample: [metadata sample payload](#metadata_sample_payload)</span></span>  

<span data-ttu-id="c6d59-246">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-246">Back to [top](#overview)</span></span>  

<a name="metadata.properties.key"></a>   
#### <a name="metadatapropertieskey"></a><span data-ttu-id="c6d59-247">metadata.properties.key</span><span class="sxs-lookup"><span data-stu-id="c6d59-247">metadata.properties.key</span></span>  
<span data-ttu-id="c6d59-248">Key of a key-value pair provided in additional properties of an automation rule.</span><span class="sxs-lookup"><span data-stu-id="c6d59-248">Key of a key-value pair provided in additional properties of an automation rule.</span></span>  

 <span data-ttu-id="c6d59-249">Property Value Type: number (integer)</span><span class="sxs-lookup"><span data-stu-id="c6d59-249">Property Value Type: number (integer)</span></span>  

 <span data-ttu-id="c6d59-250">Parent: *metadata.properties*</span><span class="sxs-lookup"><span data-stu-id="c6d59-250">Parent: *metadata.properties*</span></span>  

 <span data-ttu-id="c6d59-251">Sample: [metadata sample payload](#metadata_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-251">Sample: [metadata sample payload](#metadata_sample_payload)</span></span>  

<a name="metadata.properties.value"></a>   
#### <a name="metadatapropertiesvalue"></a><span data-ttu-id="c6d59-252">metadata.properties.value</span><span class="sxs-lookup"><span data-stu-id="c6d59-252">metadata.properties.value</span></span>  
<span data-ttu-id="c6d59-253">Value of a key-value pair provided in additional properties of an automation rule.</span><span class="sxs-lookup"><span data-stu-id="c6d59-253">Value of a key-value pair provided in additional properties of an automation rule.</span></span>  

 <span data-ttu-id="c6d59-254">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-254">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-255">Parent: *metadata.properties*</span><span class="sxs-lookup"><span data-stu-id="c6d59-255">Parent: *metadata.properties*</span></span>  

 <span data-ttu-id="c6d59-256">Sample: [metadata sample payload](#metadata_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-256">Sample: [metadata sample payload](#metadata_sample_payload)</span></span>  

<a name="metadata.properties.matchedrule"></a>   
#### <a name="metadatapropertiesmatchedrule"></a><span data-ttu-id="c6d59-257">metadata.properties.matchedrule</span><span class="sxs-lookup"><span data-stu-id="c6d59-257">metadata.properties.matchedrule</span></span>  
<span data-ttu-id="c6d59-258">ID of the automation rule that contains the additional properties.</span><span class="sxs-lookup"><span data-stu-id="c6d59-258">ID of the automation rule that contains the additional properties.</span></span>  

 <span data-ttu-id="c6d59-259">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-259">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-260">Parent: *metadata.properties*</span><span class="sxs-lookup"><span data-stu-id="c6d59-260">Parent: *metadata.properties*</span></span>  

 <span data-ttu-id="c6d59-261">Sample: [metadata sample payload](#metadata_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-261">Sample: [metadata sample payload](#metadata_sample_payload)</span></span>  

<a name="referenceTop"></a>   
## <a name="post-json-payload-objects"></a><span data-ttu-id="c6d59-262">Post JSON payload objects</span><span class="sxs-lookup"><span data-stu-id="c6d59-262">Post JSON payload objects</span></span>  
<span data-ttu-id="c6d59-263">Read up on the fields currently supported in the post JSON payload.</span><span class="sxs-lookup"><span data-stu-id="c6d59-263">Read up on the fields currently supported in the post JSON payload.</span></span>  

<a name="document.id"></a>   
### <a name="postid"></a><span data-ttu-id="c6d59-264">post.id</span><span class="sxs-lookup"><span data-stu-id="c6d59-264">post.id</span></span>  
<span data-ttu-id="c6d59-265">The unique post ID in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.</span><span class="sxs-lookup"><span data-stu-id="c6d59-265">The unique post ID in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.</span></span>  

 <span data-ttu-id="c6d59-266">Property Value Type: number (integer)</span><span class="sxs-lookup"><span data-stu-id="c6d59-266">Property Value Type: number (integer)</span></span>  

 <span data-ttu-id="c6d59-267">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-267">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-268">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-268">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-269">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-269">Back to [top](#overview)</span></span>  

<a name="document.contentType"></a>   
### <a name="postcontenttype"></a><span data-ttu-id="c6d59-270">post.contentType</span><span class="sxs-lookup"><span data-stu-id="c6d59-270">post.contentType</span></span>  
<span data-ttu-id="c6d59-271">The type of content in a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-271">The type of content in a post.</span></span>  

 <span data-ttu-id="c6d59-272">Property Value Type: enum</span><span class="sxs-lookup"><span data-stu-id="c6d59-272">Property Value Type: enum</span></span>  

 <span data-ttu-id="c6d59-273">Property Values:</span><span class="sxs-lookup"><span data-stu-id="c6d59-273">Property Values:</span></span>  

- <span data-ttu-id="c6d59-274">POST: The main content is text.</span><span class="sxs-lookup"><span data-stu-id="c6d59-274">POST: The main content is text.</span></span>  

- <span data-ttu-id="c6d59-275">IMAGE: The main content is a picture.</span><span class="sxs-lookup"><span data-stu-id="c6d59-275">IMAGE: The main content is a picture.</span></span>  

- <span data-ttu-id="c6d59-276">VIDEO: The main content is a video.</span><span class="sxs-lookup"><span data-stu-id="c6d59-276">VIDEO: The main content is a video.</span></span>  

- <span data-ttu-id="c6d59-277">LINK: The main content is a hyperlink.</span><span class="sxs-lookup"><span data-stu-id="c6d59-277">LINK: The main content is a hyperlink.</span></span>  

  <span data-ttu-id="c6d59-278">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-278">Parent: *post*</span></span>  

  <span data-ttu-id="c6d59-279">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-279">Sample: [post sample payload](#document_sample_payload)</span></span>  

  <span data-ttu-id="c6d59-280">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-280">Back to [top](#overview)</span></span>  

<a name="document.postType"></a>   
### <a name="postposttype"></a><span data-ttu-id="c6d59-281">post.postType</span><span class="sxs-lookup"><span data-stu-id="c6d59-281">post.postType</span></span>  
<span data-ttu-id="c6d59-282">The type of post in its conversational context.</span><span class="sxs-lookup"><span data-stu-id="c6d59-282">The type of post in its conversational context.</span></span>  

 <span data-ttu-id="c6d59-283">Property Value Type: enum</span><span class="sxs-lookup"><span data-stu-id="c6d59-283">Property Value Type: enum</span></span>  

 <span data-ttu-id="c6d59-284">Property Values:</span><span class="sxs-lookup"><span data-stu-id="c6d59-284">Property Values:</span></span>  

- <span data-ttu-id="c6d59-285">post: An original post, that other posts are related to.</span><span class="sxs-lookup"><span data-stu-id="c6d59-285">post: An original post, that other posts are related to.</span></span> <span data-ttu-id="c6d59-286">Think of the start of a conversation.</span><span class="sxs-lookup"><span data-stu-id="c6d59-286">Think of the start of a conversation.</span></span>  

- <span data-ttu-id="c6d59-287">reply: A reply or a comment to an original post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-287">reply: A reply or a comment to an original post.</span></span>  

- <span data-ttu-id="c6d59-288">share: A share or retweet of an original post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-288">share: A share or retweet of an original post.</span></span>  

- <span data-ttu-id="c6d59-289">privatemessage: A private conversation between two (or more) profiles.</span><span class="sxs-lookup"><span data-stu-id="c6d59-289">privatemessage: A private conversation between two (or more) profiles.</span></span>  

  <span data-ttu-id="c6d59-290">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-290">Parent: *post*</span></span>  

  <span data-ttu-id="c6d59-291">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-291">Sample: [post sample payload](#document_sample_payload)</span></span>  

  <span data-ttu-id="c6d59-292">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-292">Back to [top](#overview)</span></span>  

<a name="document.uri"></a>   
### <a name="posturi"></a><span data-ttu-id="c6d59-293">post.uri</span><span class="sxs-lookup"><span data-stu-id="c6d59-293">post.uri</span></span>  
<span data-ttu-id="c6d59-294">A backlink to the post's original URI.</span><span class="sxs-lookup"><span data-stu-id="c6d59-294">A backlink to the post's original URI.</span></span>  

> [!NOTE]
>  <span data-ttu-id="c6d59-295">The URI of news posts can't be used to link back to the original article.</span><span class="sxs-lookup"><span data-stu-id="c6d59-295">The URI of news posts can't be used to link back to the original article.</span></span>  

 <span data-ttu-id="c6d59-296">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-296">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-297">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-297">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-298">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-298">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-299">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-299">Back to [top](#overview)</span></span>  

<a name="document.title"></a>   
### <a name="posttitle"></a><span data-ttu-id="c6d59-300">post.title</span><span class="sxs-lookup"><span data-stu-id="c6d59-300">post.title</span></span>  
<span data-ttu-id="c6d59-301">The title as delivered from a post's meta information.</span><span class="sxs-lookup"><span data-stu-id="c6d59-301">The title as delivered from a post's meta information.</span></span>  

> [!NOTE]
>  <span data-ttu-id="c6d59-302">Not all posts have a title.</span><span class="sxs-lookup"><span data-stu-id="c6d59-302">Not all posts have a title.</span></span>  

 <span data-ttu-id="c6d59-303">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-303">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-304">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-304">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-305">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-305">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-306">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-306">Back to [top](#overview)</span></span>  

<a name="document.acquisitionDate"></a>   
### <a name="postacquisitiondate"></a><span data-ttu-id="c6d59-307">post.acquisitionDate</span><span class="sxs-lookup"><span data-stu-id="c6d59-307">post.acquisitionDate</span></span>  
<span data-ttu-id="c6d59-308">Timestamp when the post was acquired in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).</span><span class="sxs-lookup"><span data-stu-id="c6d59-308">Timestamp when the post was acquired in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).</span></span>  

 <span data-ttu-id="c6d59-309">Property Value Type: date-time</span><span class="sxs-lookup"><span data-stu-id="c6d59-309">Property Value Type: date-time</span></span>  

 <span data-ttu-id="c6d59-310">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-310">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-311">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-311">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-312">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-312">Back to [top](#overview)</span></span>  

<a name="document.modificationDate"></a>   
### <a name="postmodificationdate"></a><span data-ttu-id="c6d59-313">post.modificationDate</span><span class="sxs-lookup"><span data-stu-id="c6d59-313">post.modificationDate</span></span>  
<span data-ttu-id="c6d59-314">Timestamp when  the post was last updated in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).</span><span class="sxs-lookup"><span data-stu-id="c6d59-314">Timestamp when  the post was last updated in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] (in ISO 8601 format).</span></span>  

 <span data-ttu-id="c6d59-315">Property Value Type: date-time</span><span class="sxs-lookup"><span data-stu-id="c6d59-315">Property Value Type: date-time</span></span>  

 <span data-ttu-id="c6d59-316">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-316">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-317">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-317">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-318">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-318">Back to [top](#overview)</span></span>  

<a name="document.publicationDate"></a>   
### <a name="postpublicationdate"></a><span data-ttu-id="c6d59-319">post.publicationDate</span><span class="sxs-lookup"><span data-stu-id="c6d59-319">post.publicationDate</span></span>  
<span data-ttu-id="c6d59-320">Timestamp when the post was published on the source (in ISO 8601 format).</span><span class="sxs-lookup"><span data-stu-id="c6d59-320">Timestamp when the post was published on the source (in ISO 8601 format).</span></span>  

 <span data-ttu-id="c6d59-321">Property Value Type: date-time</span><span class="sxs-lookup"><span data-stu-id="c6d59-321">Property Value Type: date-time</span></span>  

 <span data-ttu-id="c6d59-322">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-322">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-323">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-323">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-324">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-324">Back to [top](#overview)</span></span>  

<a name="document.profile"></a>   
### <a name="postprofile"></a><span data-ttu-id="c6d59-325">post.profile</span><span class="sxs-lookup"><span data-stu-id="c6d59-325">post.profile</span></span>  
<span data-ttu-id="c6d59-326">JSON object describing the social profile of the post's author.</span><span class="sxs-lookup"><span data-stu-id="c6d59-326">JSON object describing the social profile of the post's author.</span></span>  

<span data-ttu-id="c6d59-327">In the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] user interface, this is referred to as an "author".</span><span class="sxs-lookup"><span data-stu-id="c6d59-327">In the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] user interface, this is referred to as an "author".</span></span> <span data-ttu-id="c6d59-328">More information: [Find out what people are talking about](analytics-conversations.md), [See author details](author-details.md)</span><span class="sxs-lookup"><span data-stu-id="c6d59-328">More information: [Find out what people are talking about](analytics-conversations.md), [See author details](author-details.md)</span></span>  

 <span data-ttu-id="c6d59-329">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-329">Property Value Type: object</span></span>  


|                           <span data-ttu-id="c6d59-330">JSON element</span><span class="sxs-lookup"><span data-stu-id="c6d59-330">JSON element</span></span>                            |                                                          <span data-ttu-id="c6d59-331">Description</span><span class="sxs-lookup"><span data-stu-id="c6d59-331">Description</span></span>                                                          |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
|             [<span data-ttu-id="c6d59-332">post.profile.uri</span><span class="sxs-lookup"><span data-stu-id="c6d59-332">post.profile.uri</span></span>](#document.profile.uri)             | <span data-ttu-id="c6d59-333">Unique URI of the profile in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.</span><span class="sxs-lookup"><span data-stu-id="c6d59-333">Unique URI of the profile in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.</span></span> |
|     [<span data-ttu-id="c6d59-334">post.profile.profileIcon</span><span class="sxs-lookup"><span data-stu-id="c6d59-334">post.profile.profileIcon</span></span>](#document.profile.profileIcon)     |                                                <span data-ttu-id="c6d59-335">URI to public profile picture.</span><span class="sxs-lookup"><span data-stu-id="c6d59-335">URI to public profile picture.</span></span>                                                 |
| [<span data-ttu-id="c6d59-336">post.profile.profileLocation</span><span class="sxs-lookup"><span data-stu-id="c6d59-336">post.profile.profileLocation</span></span>](#document.profile.profileLocation) |                     <span data-ttu-id="c6d59-337">JSON object describing the author's location information as specified by the author.</span><span class="sxs-lookup"><span data-stu-id="c6d59-337">JSON object describing the author's location information as specified by the author.</span></span>                      |
|  [<span data-ttu-id="c6d59-338">post.profile.externalHandle</span><span class="sxs-lookup"><span data-stu-id="c6d59-338">post.profile.externalHandle</span></span>](#document.profile.externalHandle)  |                                                 <span data-ttu-id="c6d59-339">Alias or handle of a profile.</span><span class="sxs-lookup"><span data-stu-id="c6d59-339">Alias or handle of a profile.</span></span>                                                 |
|     [<span data-ttu-id="c6d59-340">post.profile.displayName</span><span class="sxs-lookup"><span data-stu-id="c6d59-340">post.profile.displayName</span></span>](#document.profile.displayName)     |                                     <span data-ttu-id="c6d59-341">Display name of a profile as provided on the source.</span><span class="sxs-lookup"><span data-stu-id="c6d59-341">Display name of a profile as provided on the source.</span></span>                                      |
|      [<span data-ttu-id="c6d59-342">post.profile.externalId</span><span class="sxs-lookup"><span data-stu-id="c6d59-342">post.profile.externalId</span></span>](#document.profile.externalId)      |                                               <span data-ttu-id="c6d59-343">ID of the profile on the source.</span><span class="sxs-lookup"><span data-stu-id="c6d59-343">ID of the profile on the source.</span></span>                                                |
|            [<span data-ttu-id="c6d59-344">post.profile.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-344">post.profile.name</span></span>](#document.profile.name)            |     <span data-ttu-id="c6d59-345">Name for the profile in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] user interface.</span><span class="sxs-lookup"><span data-stu-id="c6d59-345">Name for the profile in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] user interface.</span></span>     |

 <span data-ttu-id="c6d59-346">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-346">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-347">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-347">Sample:</span></span>  

```json  
"profile": {  
  "name": "Display Name @externalHandle",  
  "uri": "mse-tw://#12345678",
  "profileIcon": "https://path/to/the/profileIcon.png" ,  
  "profileLocation": {  
    "locality": "Boston",  
    "adminDistrict": "Massachusetts",  
    "countryRegion": "United States",  
    "coordinates": {  
      "latitude": 42.156028747558594,  
      "longitude": -71.56590270996094  
    },  
    "quadKey": "030233212221101333012"  
  },  
  "displayName": "Display Name ",  
  "externalId": "1234567"  
  },  

```  

<span data-ttu-id="c6d59-348">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-348">Back to [top](#overview)</span></span>  

<a name="document.profile.uri"></a>   
#### <a name="postprofileuri"></a><span data-ttu-id="c6d59-349">post.profile.uri</span><span class="sxs-lookup"><span data-stu-id="c6d59-349">post.profile.uri</span></span>  
<span data-ttu-id="c6d59-350">Unique URI of the profile in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.</span><span class="sxs-lookup"><span data-stu-id="c6d59-350">Unique URI of the profile in the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution database.</span></span>

> [!NOTE]
> <span data-ttu-id="c6d59-351">**post.profile.uri** replaced **post.profile.id** in June 2018.</span><span class="sxs-lookup"><span data-stu-id="c6d59-351">**post.profile.uri** replaced **post.profile.id** in June 2018.</span></span> <span data-ttu-id="c6d59-352">You can find more details in [this blog post](https://blogs.msdn.microsoft.com/crm/2017/11/27/deprecation-of-post-profile-id-object-in-social-engagement-json-payload/).</span><span class="sxs-lookup"><span data-stu-id="c6d59-352">You can find more details in [this blog post](https://blogs.msdn.microsoft.com/crm/2017/11/27/deprecation-of-post-profile-id-object-in-social-engagement-json-payload/).</span></span> 

 <span data-ttu-id="c6d59-353">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-353">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-354">Parent: *post.profile*</span><span class="sxs-lookup"><span data-stu-id="c6d59-354">Parent: *post.profile*</span></span>  

 <span data-ttu-id="c6d59-355">Sample: [post.profile](#document.profile)</span><span class="sxs-lookup"><span data-stu-id="c6d59-355">Sample: [post.profile](#document.profile)</span></span>  

<a name="document.profile.profileIcon"></a>   
#### <a name="postprofileprofileicon"></a><span data-ttu-id="c6d59-356">post.profile.profileIcon</span><span class="sxs-lookup"><span data-stu-id="c6d59-356">post.profile.profileIcon</span></span>  
<span data-ttu-id="c6d59-357">URI to public profile picture.</span><span class="sxs-lookup"><span data-stu-id="c6d59-357">URI to public profile picture.</span></span>  

 <span data-ttu-id="c6d59-358">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-358">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-359">Parent: *post.profile*</span><span class="sxs-lookup"><span data-stu-id="c6d59-359">Parent: *post.profile*</span></span>  

 <span data-ttu-id="c6d59-360">Sample: [post.profile](#document.profile)</span><span class="sxs-lookup"><span data-stu-id="c6d59-360">Sample: [post.profile](#document.profile)</span></span>  

<a name="document.profile.profileLocation"></a>   
#### <a name="postprofileprofilelocation"></a><span data-ttu-id="c6d59-361">post.profile.profileLocation</span><span class="sxs-lookup"><span data-stu-id="c6d59-361">post.profile.profileLocation</span></span>  
<span data-ttu-id="c6d59-362">JSON object describing the author's location information as specified by the author.</span><span class="sxs-lookup"><span data-stu-id="c6d59-362">JSON object describing the author's location information as specified by the author.</span></span>  

<span data-ttu-id="c6d59-363">For some sources, profile owners can provide their location information.</span><span class="sxs-lookup"><span data-stu-id="c6d59-363">For some sources, profile owners can provide their location information.</span></span> <span data-ttu-id="c6d59-364">This is shown in the user interface as author location, as opposed to the post location, which specifies from where the post was published.</span><span class="sxs-lookup"><span data-stu-id="c6d59-364">This is shown in the user interface as author location, as opposed to the post location, which specifies from where the post was published.</span></span> <span data-ttu-id="c6d59-365">For the post location, see [post.postLocation](#document.postLocation)</span><span class="sxs-lookup"><span data-stu-id="c6d59-365">For the post location, see [post.postLocation](#document.postLocation)</span></span>  

 <span data-ttu-id="c6d59-366">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-366">Property Value Type: object</span></span>  

|<span data-ttu-id="c6d59-367">JSON element</span><span class="sxs-lookup"><span data-stu-id="c6d59-367">JSON element</span></span>|<span data-ttu-id="c6d59-368">Description</span><span class="sxs-lookup"><span data-stu-id="c6d59-368">Description</span></span>|  
|------------------|-----------------|  
|[<span data-ttu-id="c6d59-369">post.profile.profileLocation.locality</span><span class="sxs-lookup"><span data-stu-id="c6d59-369">post.profile.profileLocation.locality</span></span>](#document.profile.profileLocation.locality)|<span data-ttu-id="c6d59-370">Represents the name of a city.</span><span class="sxs-lookup"><span data-stu-id="c6d59-370">Represents the name of a city.</span></span>|  
|[<span data-ttu-id="c6d59-371">post.profile.profileLocation.adminDistrict</span><span class="sxs-lookup"><span data-stu-id="c6d59-371">post.profile.profileLocation.adminDistrict</span></span>](#document.profile.profileLocation.adminDistrict)|<span data-ttu-id="c6d59-372">Represents the name of an administrative division, for example a federal state or a province.</span><span class="sxs-lookup"><span data-stu-id="c6d59-372">Represents the name of an administrative division, for example a federal state or a province.</span></span>|  
|[<span data-ttu-id="c6d59-373">post.profile.profileLocation.countryRegion</span><span class="sxs-lookup"><span data-stu-id="c6d59-373">post.profile.profileLocation.countryRegion</span></span>](#document.profile.profileLocation.countryRegion)|<span data-ttu-id="c6d59-374">Represents the name of a country or region.</span><span class="sxs-lookup"><span data-stu-id="c6d59-374">Represents the name of a country or region.</span></span>|  
|[<span data-ttu-id="c6d59-375">post.profile.profileLocation.coordinates</span><span class="sxs-lookup"><span data-stu-id="c6d59-375">post.profile.profileLocation.coordinates</span></span>](#document.profile.profileLocation.coordinates)|<span data-ttu-id="c6d59-376">JSON object describing the coordinates of a social profile with latitude and longitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-376">JSON object describing the coordinates of a social profile with latitude and longitude.</span></span>|  
|[<span data-ttu-id="c6d59-377">post.profile.profileLocation.coordinates.latitude</span><span class="sxs-lookup"><span data-stu-id="c6d59-377">post.profile.profileLocation.coordinates.latitude</span></span>](#document.profile.profileLocation.coordinates.latitude)|<span data-ttu-id="c6d59-378">Geographic latitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-378">Geographic latitude.</span></span>|  
|[<span data-ttu-id="c6d59-379">post.profile.profileLocation.coordinates.longitude</span><span class="sxs-lookup"><span data-stu-id="c6d59-379">post.profile.profileLocation.coordinates.longitude</span></span>](#document.profile.profileLocation.coordinates.longitude)|<span data-ttu-id="c6d59-380">Geographic longitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-380">Geographic longitude.</span></span>|  
|[<span data-ttu-id="c6d59-381">post.profile.profileLocation.quadkey</span><span class="sxs-lookup"><span data-stu-id="c6d59-381">post.profile.profileLocation.quadkey</span></span>](#document.profile.profileLocation.quadkey)|<span data-ttu-id="c6d59-382">Quadtree key of a location, or “quadkey” for short.</span><span class="sxs-lookup"><span data-stu-id="c6d59-382">Quadtree key of a location, or “quadkey” for short.</span></span> <span data-ttu-id="c6d59-383">Identifies a single tile at a particular level of detail on a map.</span><span class="sxs-lookup"><span data-stu-id="c6d59-383">Identifies a single tile at a particular level of detail on a map.</span></span>|  

 <span data-ttu-id="c6d59-384">Parent: *post.profile*</span><span class="sxs-lookup"><span data-stu-id="c6d59-384">Parent: *post.profile*</span></span>  

 <span data-ttu-id="c6d59-385">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-385">Sample:</span></span>  

```json  
"profileLocation": {  
  "locality": "Boston",  
  "adminDistrict": "Massachusetts",  
  "countryRegion": "United States",  
  "coordinates": {  
    "latitude": 42.156028747558594,  
    "longitude": -71.56590270996094  
  },  
  "quadKey": "030233212221101333012"  
},  
```  

<a name="document.profile.profileLocation.locality"></a>   
##### <a name="postprofileprofilelocationlocality"></a><span data-ttu-id="c6d59-386">post.profile.profileLocation.locality</span><span class="sxs-lookup"><span data-stu-id="c6d59-386">post.profile.profileLocation.locality</span></span>  
<span data-ttu-id="c6d59-387">Represents the name of a city.</span><span class="sxs-lookup"><span data-stu-id="c6d59-387">Represents the name of a city.</span></span>  

 <span data-ttu-id="c6d59-388">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-388">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-389">Parent: *post.profile*</span><span class="sxs-lookup"><span data-stu-id="c6d59-389">Parent: *post.profile*</span></span>  

 <span data-ttu-id="c6d59-390">Sample: [post.profile.profileLocation](#document.profile.profileLocation)</span><span class="sxs-lookup"><span data-stu-id="c6d59-390">Sample: [post.profile.profileLocation](#document.profile.profileLocation)</span></span>  

<a name="document.profile.profileLocation.adminDistrict"></a>   
##### <a name="postprofileprofilelocationadmindistrict"></a><span data-ttu-id="c6d59-391">post.profile.profileLocation.adminDistrict</span><span class="sxs-lookup"><span data-stu-id="c6d59-391">post.profile.profileLocation.adminDistrict</span></span>  
<span data-ttu-id="c6d59-392">Represents the name of an administrative division, for example a federal state or a province.</span><span class="sxs-lookup"><span data-stu-id="c6d59-392">Represents the name of an administrative division, for example a federal state or a province.</span></span>  

 <span data-ttu-id="c6d59-393">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-393">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-394">Parent: *post.profile*</span><span class="sxs-lookup"><span data-stu-id="c6d59-394">Parent: *post.profile*</span></span>  

 <span data-ttu-id="c6d59-395">Sample: [post.profile.profileLocation](#document.profile.profileLocation)</span><span class="sxs-lookup"><span data-stu-id="c6d59-395">Sample: [post.profile.profileLocation](#document.profile.profileLocation)</span></span>  

<a name="document.profile.profileLocation.countryRegion"></a>   
##### <a name="postprofileprofilelocationcountryregion"></a><span data-ttu-id="c6d59-396">post.profile.profileLocation.countryRegion</span><span class="sxs-lookup"><span data-stu-id="c6d59-396">post.profile.profileLocation.countryRegion</span></span>  
<span data-ttu-id="c6d59-397">Represents the name of a country or region.</span><span class="sxs-lookup"><span data-stu-id="c6d59-397">Represents the name of a country or region.</span></span>  

 <span data-ttu-id="c6d59-398">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-398">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-399">Parent: *post.profile*</span><span class="sxs-lookup"><span data-stu-id="c6d59-399">Parent: *post.profile*</span></span>  

 <span data-ttu-id="c6d59-400">Sample: [post.profile.profileLocation](#document.profile.profileLocation)</span><span class="sxs-lookup"><span data-stu-id="c6d59-400">Sample: [post.profile.profileLocation](#document.profile.profileLocation)</span></span>  

<a name="document.profile.profileLocation.coordinates"></a>   
##### <a name="postprofileprofilelocationcoordinates"></a><span data-ttu-id="c6d59-401">post.profile.profileLocation.coordinates</span><span class="sxs-lookup"><span data-stu-id="c6d59-401">post.profile.profileLocation.coordinates</span></span>  
<span data-ttu-id="c6d59-402">JSON object describing the coordinates of a social profile with latitude and longitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-402">JSON object describing the coordinates of a social profile with latitude and longitude.</span></span>  

 <span data-ttu-id="c6d59-403">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-403">Sample:</span></span>  

```json  
"coordinates": {  
  "latitude": 42.156028747558594,  
  "longitude": -71.56590270996094  
},  
```  

<a name="document.profile.profileLocation.coordinates.latitude"></a>   
###### <a name="postprofileprofilelocationcoordinateslatitude"></a><span data-ttu-id="c6d59-404">post.profile.profileLocation.coordinates.latitude</span><span class="sxs-lookup"><span data-stu-id="c6d59-404">post.profile.profileLocation.coordinates.latitude</span></span>  
<span data-ttu-id="c6d59-405">Geographic latitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-405">Geographic latitude.</span></span>  

 <span data-ttu-id="c6d59-406">Property Value Type: number (floating point)</span><span class="sxs-lookup"><span data-stu-id="c6d59-406">Property Value Type: number (floating point)</span></span>  

 <span data-ttu-id="c6d59-407">Parent: *post.profile.profileLocation.coordinates*</span><span class="sxs-lookup"><span data-stu-id="c6d59-407">Parent: *post.profile.profileLocation.coordinates*</span></span>  

 <span data-ttu-id="c6d59-408">Sample: [post.profile.profileLocation.coordinates](#document.profile.profileLocation.coordinates)</span><span class="sxs-lookup"><span data-stu-id="c6d59-408">Sample: [post.profile.profileLocation.coordinates](#document.profile.profileLocation.coordinates)</span></span>  

<a name="document.profile.profileLocation.coordinates.longitude"></a>   
###### <a name="postprofileprofilelocationcoordinateslongitude"></a><span data-ttu-id="c6d59-409">post.profile.profileLocation.coordinates.longitude</span><span class="sxs-lookup"><span data-stu-id="c6d59-409">post.profile.profileLocation.coordinates.longitude</span></span>  
<span data-ttu-id="c6d59-410">Geographic longitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-410">Geographic longitude.</span></span>  

 <span data-ttu-id="c6d59-411">Property Value Type: number (floating point)</span><span class="sxs-lookup"><span data-stu-id="c6d59-411">Property Value Type: number (floating point)</span></span>  

 <span data-ttu-id="c6d59-412">Parent: *post.profile.profileLocation.coordinates*</span><span class="sxs-lookup"><span data-stu-id="c6d59-412">Parent: *post.profile.profileLocation.coordinates*</span></span>  

 <span data-ttu-id="c6d59-413">Sample: [post.profile.profileLocation.coordinates](#document.profile.profileLocation.coordinates)</span><span class="sxs-lookup"><span data-stu-id="c6d59-413">Sample: [post.profile.profileLocation.coordinates](#document.profile.profileLocation.coordinates)</span></span>  

<a name="document.profile.profileLocation.quadkey"></a>   
##### <a name="postprofileprofilelocationquadkey"></a><span data-ttu-id="c6d59-414">post.profile.profileLocation.quadkey</span><span class="sxs-lookup"><span data-stu-id="c6d59-414">post.profile.profileLocation.quadkey</span></span>  
<span data-ttu-id="c6d59-415">Quadtree key of a location, or “quadkey” for short.</span><span class="sxs-lookup"><span data-stu-id="c6d59-415">Quadtree key of a location, or “quadkey” for short.</span></span> <span data-ttu-id="c6d59-416">Identifies a single tile at a particular level of detail on a map.</span><span class="sxs-lookup"><span data-stu-id="c6d59-416">Identifies a single tile at a particular level of detail on a map.</span></span> <span data-ttu-id="c6d59-417">More information: [MSDN: Bing Maps Tile System](https://msdn.microsoft.com/library/bb259689.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6d59-417">More information: [MSDN: Bing Maps Tile System](https://msdn.microsoft.com/library/bb259689.aspx)</span></span>  

 <span data-ttu-id="c6d59-418">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-418">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-419">Parent: *post.profile.profileLocation*</span><span class="sxs-lookup"><span data-stu-id="c6d59-419">Parent: *post.profile.profileLocation*</span></span>  

 <span data-ttu-id="c6d59-420">Sample: [post.profile.profileLocation](#document.profile.profileLocation)</span><span class="sxs-lookup"><span data-stu-id="c6d59-420">Sample: [post.profile.profileLocation](#document.profile.profileLocation)</span></span>  

<a name="document.profile.externalHandle"></a>   
#### <a name="postprofileexternalhandle"></a><span data-ttu-id="c6d59-421">post.profile.externalHandle</span><span class="sxs-lookup"><span data-stu-id="c6d59-421">post.profile.externalHandle</span></span>  
<span data-ttu-id="c6d59-422">Alias or handle of a profile.</span><span class="sxs-lookup"><span data-stu-id="c6d59-422">Alias or handle of a profile.</span></span>  

 <span data-ttu-id="c6d59-423">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-423">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-424">Parent: *post.profile*</span><span class="sxs-lookup"><span data-stu-id="c6d59-424">Parent: *post.profile*</span></span>  

 <span data-ttu-id="c6d59-425">Sample: [post.profile](#document.profile)</span><span class="sxs-lookup"><span data-stu-id="c6d59-425">Sample: [post.profile](#document.profile)</span></span>  

<a name="document.profile.displayName"></a>   
#### <a name="postprofiledisplayname"></a><span data-ttu-id="c6d59-426">post.profile.displayName</span><span class="sxs-lookup"><span data-stu-id="c6d59-426">post.profile.displayName</span></span>  
<span data-ttu-id="c6d59-427">Display name of a profile as provided on the source.</span><span class="sxs-lookup"><span data-stu-id="c6d59-427">Display name of a profile as provided on the source.</span></span>  

 <span data-ttu-id="c6d59-428">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-428">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-429">Parent: *post.profile*</span><span class="sxs-lookup"><span data-stu-id="c6d59-429">Parent: *post.profile*</span></span>  

 <span data-ttu-id="c6d59-430">Sample: [post.profile](#document.profile)</span><span class="sxs-lookup"><span data-stu-id="c6d59-430">Sample: [post.profile](#document.profile)</span></span>  

<a name="document.profile.externalId"></a>   
#### <a name="postprofileexternalid"></a><span data-ttu-id="c6d59-431">post.profile.externalId</span><span class="sxs-lookup"><span data-stu-id="c6d59-431">post.profile.externalId</span></span>  
<span data-ttu-id="c6d59-432">ID of the profile on the source.</span><span class="sxs-lookup"><span data-stu-id="c6d59-432">ID of the profile on the source.</span></span>  

 <span data-ttu-id="c6d59-433">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-433">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-434">Parent: *post.profile*</span><span class="sxs-lookup"><span data-stu-id="c6d59-434">Parent: *post.profile*</span></span>  

 <span data-ttu-id="c6d59-435">Sample: [post.profile](#document.profile)</span><span class="sxs-lookup"><span data-stu-id="c6d59-435">Sample: [post.profile](#document.profile)</span></span>  

<a name="document.profile.name"></a>   
#### <a name="postprofilename"></a><span data-ttu-id="c6d59-436">post.profile.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-436">post.profile.name</span></span>  
<span data-ttu-id="c6d59-437">Representation in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] for the name for the profile.</span><span class="sxs-lookup"><span data-stu-id="c6d59-437">Representation in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] for the name for the profile.</span></span>  

 <span data-ttu-id="c6d59-438">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-438">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-439">Parent: *post.profile*</span><span class="sxs-lookup"><span data-stu-id="c6d59-439">Parent: *post.profile*</span></span>  

 <span data-ttu-id="c6d59-440">Sample: [post.profile](#document.profile)</span><span class="sxs-lookup"><span data-stu-id="c6d59-440">Sample: [post.profile](#document.profile)</span></span>  

<a name="document.source"></a>   
### <a name="postsource"></a><span data-ttu-id="c6d59-441">post.source</span><span class="sxs-lookup"><span data-stu-id="c6d59-441">post.source</span></span>  
<span data-ttu-id="c6d59-442">JSON object describing on which source a post was found.</span><span class="sxs-lookup"><span data-stu-id="c6d59-442">JSON object describing on which source a post was found.</span></span>  

 <span data-ttu-id="c6d59-443">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-443">Sample:</span></span>  

```json  
"source": {  
  "name": "Microblogs",  
  "id": "18",  
  "param": "Twitter"  
}  

```  

<span data-ttu-id="c6d59-444">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-444">Back to [top](#overview)</span></span>  

<a name="document.source.id"></a>   
#### <a name="postsourceid"></a><span data-ttu-id="c6d59-445">post.source.id</span><span class="sxs-lookup"><span data-stu-id="c6d59-445">post.source.id</span></span>  
<span data-ttu-id="c6d59-446">Represents the internal ID of the source that a post was found on.</span><span class="sxs-lookup"><span data-stu-id="c6d59-446">Represents the internal ID of the source that a post was found on.</span></span>  

 <span data-ttu-id="c6d59-447">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-447">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-448">Parent: *post.source*</span><span class="sxs-lookup"><span data-stu-id="c6d59-448">Parent: *post.source*</span></span>  

 <span data-ttu-id="c6d59-449">Sample: [post.source](#document.source)</span><span class="sxs-lookup"><span data-stu-id="c6d59-449">Sample: [post.source](#document.source)</span></span>  

 <span data-ttu-id="c6d59-450">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-450">Back to [top](#overview)</span></span>  

<a name="document.source.name"></a>   
#### <a name="postsourcename"></a><span data-ttu-id="c6d59-451">post.source.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-451">post.source.name</span></span>  
<span data-ttu-id="c6d59-452">Represents the name of the source that a post was found on.</span><span class="sxs-lookup"><span data-stu-id="c6d59-452">Represents the name of the source that a post was found on.</span></span>  

 <span data-ttu-id="c6d59-453">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-453">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-454">Parent: *post.source*</span><span class="sxs-lookup"><span data-stu-id="c6d59-454">Parent: *post.source*</span></span>  

 <span data-ttu-id="c6d59-455">Sample: [post.source](#document.source)</span><span class="sxs-lookup"><span data-stu-id="c6d59-455">Sample: [post.source](#document.source)</span></span>  

 <span data-ttu-id="c6d59-456">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-456">Back to [top](#overview)</span></span>  

<a name="document.source.param"></a>   
#### <a name="postsourceparam"></a><span data-ttu-id="c6d59-457">post.source.param</span><span class="sxs-lookup"><span data-stu-id="c6d59-457">post.source.param</span></span>  
<span data-ttu-id="c6d59-458">Describes on which source a post was found.</span><span class="sxs-lookup"><span data-stu-id="c6d59-458">Describes on which source a post was found.</span></span>  

 <span data-ttu-id="c6d59-459">Property Value Type: enum</span><span class="sxs-lookup"><span data-stu-id="c6d59-459">Property Value Type: enum</span></span>  

 <span data-ttu-id="c6d59-460">The sources availablility extends over time.</span><span class="sxs-lookup"><span data-stu-id="c6d59-460">The sources availablility extends over time.</span></span> <span data-ttu-id="c6d59-461">For an up-to-date list, check back often and follow the release announcements.</span><span class="sxs-lookup"><span data-stu-id="c6d59-461">For an up-to-date list, check back often and follow the release announcements.</span></span>  

 <span data-ttu-id="c6d59-462">Parent: *post.source*</span><span class="sxs-lookup"><span data-stu-id="c6d59-462">Parent: *post.source*</span></span>  

 <span data-ttu-id="c6d59-463">Sample: [post.source](#document.source)</span><span class="sxs-lookup"><span data-stu-id="c6d59-463">Sample: [post.source](#document.source)</span></span>  

 <span data-ttu-id="c6d59-464">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-464">Back to [top](#overview)</span></span>  

<a name="document.content"></a>   
### <a name="postcontent"></a><span data-ttu-id="c6d59-465">post.content</span><span class="sxs-lookup"><span data-stu-id="c6d59-465">post.content</span></span>  
<span data-ttu-id="c6d59-466">JSON object describing the text content of a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-466">JSON object describing the text content of a post.</span></span>  

 <span data-ttu-id="c6d59-467">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-467">Property Value Type: object</span></span>  

 <span data-ttu-id="c6d59-468">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-468">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-469">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-469">Sample:</span></span>  

```json  
{  
    “post” {  
        "content": {  
            "text": "Lorem ispum dolor sit amet...",  
            "metaText": "Lorem, dolor, amet",  
        }  
    }  
}  
```  

<span data-ttu-id="c6d59-470">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-470">Back to [top](#overview)</span></span>  

<a name="document.content.text"></a>   
#### <a name="postcontenttext"></a><span data-ttu-id="c6d59-471">post.content.text</span><span class="sxs-lookup"><span data-stu-id="c6d59-471">post.content.text</span></span>  
<span data-ttu-id="c6d59-472">Text content of the post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-472">Text content of the post.</span></span>  

 <span data-ttu-id="c6d59-473">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-473">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-474">Parent: *post.content*</span><span class="sxs-lookup"><span data-stu-id="c6d59-474">Parent: *post.content*</span></span>  

 <span data-ttu-id="c6d59-475">Sample: [post.content](#document.content)</span><span class="sxs-lookup"><span data-stu-id="c6d59-475">Sample: [post.content](#document.content)</span></span>  

<a name="document.content.metaText"></a>   
#### <a name="postcontentmetatext"></a><span data-ttu-id="c6d59-476">post.content.metaText</span><span class="sxs-lookup"><span data-stu-id="c6d59-476">post.content.metaText</span></span>  
<span data-ttu-id="c6d59-477">Meta text of the post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-477">Meta text of the post.</span></span>  

 <span data-ttu-id="c6d59-478">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-478">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-479">Parent: *post.content*</span><span class="sxs-lookup"><span data-stu-id="c6d59-479">Parent: *post.content*</span></span>  

 <span data-ttu-id="c6d59-480">Sample: [post.content](#document.content)</span><span class="sxs-lookup"><span data-stu-id="c6d59-480">Sample: [post.content](#document.content)</span></span>  

<a name="document.language"></a>   
### <a name="postlanguage"></a><span data-ttu-id="c6d59-481">post.language</span><span class="sxs-lookup"><span data-stu-id="c6d59-481">post.language</span></span>  
<span data-ttu-id="c6d59-482">JSON object describing the language of a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-482">JSON object describing the language of a post.</span></span>  

 <span data-ttu-id="c6d59-483">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-483">Property Value Type: object</span></span>  

|<span data-ttu-id="c6d59-484">JSON element</span><span class="sxs-lookup"><span data-stu-id="c6d59-484">JSON element</span></span>|<span data-ttu-id="c6d59-485">Description</span><span class="sxs-lookup"><span data-stu-id="c6d59-485">Description</span></span>|  
|------------------|-----------------|  
|[<span data-ttu-id="c6d59-486">post.language.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-486">post.language.name</span></span>](#document.language.name)|<span data-ttu-id="c6d59-487">The localized language name in the locale chosen in Global Settings.</span><span class="sxs-lookup"><span data-stu-id="c6d59-487">The localized language name in the locale chosen in Global Settings.</span></span>|  
|[<span data-ttu-id="c6d59-488">post.language.code</span><span class="sxs-lookup"><span data-stu-id="c6d59-488">post.language.code</span></span>](#document.language.code)|<span data-ttu-id="c6d59-489">Language code (in ISO 639-1 format) for the post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-489">Language code (in ISO 639-1 format) for the post.</span></span>|  

 <span data-ttu-id="c6d59-490">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-490">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-491">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-491">Sample:</span></span>  

```json  
{  
    “post” {  
        "language": {  
            "name": "Finnish",  
            "code": "fi",  
        }  
    }  
}  
```  

<span data-ttu-id="c6d59-492">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-492">Back to [top](#overview)</span></span>  

<a name="document.language.name"></a>   
#### <a name="postlanguagename"></a><span data-ttu-id="c6d59-493">post.language.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-493">post.language.name</span></span>  
<span data-ttu-id="c6d59-494">The localized language name in the locale chosen in Global Settings.</span><span class="sxs-lookup"><span data-stu-id="c6d59-494">The localized language name in the locale chosen in Global Settings.</span></span>  

 <span data-ttu-id="c6d59-495">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-495">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-496">Parent: *post.language*</span><span class="sxs-lookup"><span data-stu-id="c6d59-496">Parent: *post.language*</span></span>  

 <span data-ttu-id="c6d59-497">Sample: [post.language](#document.language)</span><span class="sxs-lookup"><span data-stu-id="c6d59-497">Sample: [post.language](#document.language)</span></span>  

<a name="document.language.code"></a>   
#### <a name="postlanguagecode"></a><span data-ttu-id="c6d59-498">post.language.code</span><span class="sxs-lookup"><span data-stu-id="c6d59-498">post.language.code</span></span>  
 <span data-ttu-id="c6d59-499">Language code (in ISO 639-1 format) for the post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-499">Language code (in ISO 639-1 format) for the post.</span></span>  

 <span data-ttu-id="c6d59-500">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-500">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-501">Parent: *post.language*</span><span class="sxs-lookup"><span data-stu-id="c6d59-501">Parent: *post.language*</span></span>  

 <span data-ttu-id="c6d59-502">Sample: [post.language](#document.language)</span><span class="sxs-lookup"><span data-stu-id="c6d59-502">Sample: [post.language](#document.language)</span></span>  

<a name="document.abstractText"></a>   
### <a name="postabstracttext"></a><span data-ttu-id="c6d59-503">post.abstractText</span><span class="sxs-lookup"><span data-stu-id="c6d59-503">post.abstractText</span></span>  
<span data-ttu-id="c6d59-504">Short excerpt of the post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-504">Short excerpt of the post.</span></span>  

 <span data-ttu-id="c6d59-505">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-505">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-506">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-506">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-507">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-507">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-508">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-508">Back to [top](#overview)</span></span>  

<a name="document.score"></a>   
### <a name="postscore"></a><span data-ttu-id="c6d59-509">post.score</span><span class="sxs-lookup"><span data-stu-id="c6d59-509">post.score</span></span>  
<span data-ttu-id="c6d59-510">JSON object describing the source-specific score of the post or score of the author at the time the post was published.</span><span class="sxs-lookup"><span data-stu-id="c6d59-510">JSON object describing the source-specific score of the post or score of the author at the time the post was published.</span></span>  

 <span data-ttu-id="c6d59-511">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-511">Property Value Type: object</span></span>  

 <span data-ttu-id="c6d59-512">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-512">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-513">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-513">Sample:</span></span>  

```json  
"score": {  
  "normalScore": 3,  
  "providerScore": 29.0,  
  "provider": "KLOUT"  
}  

```  

<span data-ttu-id="c6d59-514">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-514">Back to [top](#overview)</span></span>  

<a name="document.score.normalScore"></a>   
#### <a name="postscorenormalscore"></a><span data-ttu-id="c6d59-515">post.score.normalScore</span><span class="sxs-lookup"><span data-stu-id="c6d59-515">post.score.normalScore</span></span>  
<span data-ttu-id="c6d59-516">Normalized score, from 1 (lowest) to 5 (highest).</span><span class="sxs-lookup"><span data-stu-id="c6d59-516">Normalized score, from 1 (lowest) to 5 (highest).</span></span>  

 <span data-ttu-id="c6d59-517">Property Value Type: number (integer)</span><span class="sxs-lookup"><span data-stu-id="c6d59-517">Property Value Type: number (integer)</span></span>  

 <span data-ttu-id="c6d59-518">Parent: *post.score*</span><span class="sxs-lookup"><span data-stu-id="c6d59-518">Parent: *post.score*</span></span>  

 <span data-ttu-id="c6d59-519">Sample: [post.score](#document.score)</span><span class="sxs-lookup"><span data-stu-id="c6d59-519">Sample: [post.score](#document.score)</span></span>  

<a name="document.score.providerScore"></a>   
#### <a name="postscoreproviderscore"></a><span data-ttu-id="c6d59-520">post.score.providerScore</span><span class="sxs-lookup"><span data-stu-id="c6d59-520">post.score.providerScore</span></span>  
<span data-ttu-id="c6d59-521">Non-normalized score as given by the score provider.</span><span class="sxs-lookup"><span data-stu-id="c6d59-521">Non-normalized score as given by the score provider.</span></span>  

 <span data-ttu-id="c6d59-522">Property Value Type: number (floating point)</span><span class="sxs-lookup"><span data-stu-id="c6d59-522">Property Value Type: number (floating point)</span></span>  

 <span data-ttu-id="c6d59-523">Parent: *post.score*</span><span class="sxs-lookup"><span data-stu-id="c6d59-523">Parent: *post.score*</span></span>  

 <span data-ttu-id="c6d59-524">Sample: [post.score](#document.score)</span><span class="sxs-lookup"><span data-stu-id="c6d59-524">Sample: [post.score](#document.score)</span></span>  

<a name="document.score.provider"></a>   
#### <a name="postscoreprovider"></a><span data-ttu-id="c6d59-525">post.score.provider</span><span class="sxs-lookup"><span data-stu-id="c6d59-525">post.score.provider</span></span>  
<span data-ttu-id="c6d59-526">Scoring service the score is provided from.</span><span class="sxs-lookup"><span data-stu-id="c6d59-526">Scoring service the score is provided from.</span></span>  

 <span data-ttu-id="c6d59-527">Parent: *post.score*</span><span class="sxs-lookup"><span data-stu-id="c6d59-527">Parent: *post.score*</span></span>  

 <span data-ttu-id="c6d59-528">Sample: [post.score](#document.score)</span><span class="sxs-lookup"><span data-stu-id="c6d59-528">Sample: [post.score](#document.score)</span></span>  

<a name="document.referencedPost"></a>   
### <a name="postreferencedpost"></a><span data-ttu-id="c6d59-529">post.referencedPost</span><span class="sxs-lookup"><span data-stu-id="c6d59-529">post.referencedPost</span></span>  
<span data-ttu-id="c6d59-530">Information about the post that this post is a reply to, or a share of.</span><span class="sxs-lookup"><span data-stu-id="c6d59-530">Information about the post that this post is a reply to, or a share of.</span></span> <span data-ttu-id="c6d59-531">referencedPost has the same structure as the parent post, although only a subset of its fields contain data.</span><span class="sxs-lookup"><span data-stu-id="c6d59-531">referencedPost has the same structure as the parent post, although only a subset of its fields contain data.</span></span>  

 <span data-ttu-id="c6d59-532">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-532">Property Value Type: object</span></span>  

 <span data-ttu-id="c6d59-533">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-533">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-534">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-534">Sample:</span></span>  

```json  
{  
    “post” {  
        "referencedPost": {  
            "id": "123456789",  
            "externalId": "654321",  
            "profile": {  
                "id": "123456",  
                "name": "Microsoft"  
            }  
        }  
    }  
}  
```  

 <span data-ttu-id="c6d59-535">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-535">Back to [top](#overview)</span></span>  

<a name="document.sentiment"></a>   
### <a name="postsentiment"></a><span data-ttu-id="c6d59-536">post.sentiment</span><span class="sxs-lookup"><span data-stu-id="c6d59-536">post.sentiment</span></span>  
<span data-ttu-id="c6d59-537">JSON object describing the sentiment of a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-537">JSON object describing the sentiment of a post.</span></span>  

 <span data-ttu-id="c6d59-538">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-538">Property Value Type: object</span></span>  

 <span data-ttu-id="c6d59-539">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-539">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-540">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-540">Sample:</span></span>  

```json  
"sentiment": {  
  "polarity": "negative",  
  "value": -0.46005836  
}  
```  

<span data-ttu-id="c6d59-541">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-541">Back to [top](#overview)</span></span>  

<a name="document.sentiment.polarity"></a>   
#### <a name="postsentimentpolarity"></a><span data-ttu-id="c6d59-542">post.sentiment.polarity</span><span class="sxs-lookup"><span data-stu-id="c6d59-542">post.sentiment.polarity</span></span>  
<span data-ttu-id="c6d59-543">Sentiment value of a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-543">Sentiment value of a post.</span></span> <span data-ttu-id="c6d59-544">More information: [Adaptive learning based on changes to organization’s sentiment values](adaptive-learning.md), [Understand the public perception using sentiment analysis](analytics-sentiment.md)</span><span class="sxs-lookup"><span data-stu-id="c6d59-544">More information: [Adaptive learning based on changes to organization’s sentiment values](adaptive-learning.md), [Understand the public perception using sentiment analysis](analytics-sentiment.md)</span></span>  

 <span data-ttu-id="c6d59-545">Property Value Type: enum</span><span class="sxs-lookup"><span data-stu-id="c6d59-545">Property Value Type: enum</span></span>  

 <span data-ttu-id="c6d59-546">Property Values:</span><span class="sxs-lookup"><span data-stu-id="c6d59-546">Property Values:</span></span>  

- <span data-ttu-id="c6d59-547">Positive: Post has a positive sentiment value.</span><span class="sxs-lookup"><span data-stu-id="c6d59-547">Positive: Post has a positive sentiment value.</span></span>  

- <span data-ttu-id="c6d59-548">Negative: Post has a negative sentiment value.</span><span class="sxs-lookup"><span data-stu-id="c6d59-548">Negative: Post has a negative sentiment value.</span></span>  

- <span data-ttu-id="c6d59-549">Neutral: Post has neither a positive nor a negative sentiment value.</span><span class="sxs-lookup"><span data-stu-id="c6d59-549">Neutral: Post has neither a positive nor a negative sentiment value.</span></span>  

  <span data-ttu-id="c6d59-550">Parent: *post.sentiment*</span><span class="sxs-lookup"><span data-stu-id="c6d59-550">Parent: *post.sentiment*</span></span>  

  <span data-ttu-id="c6d59-551">Sample: [post.sentiment](#document.sentiment)</span><span class="sxs-lookup"><span data-stu-id="c6d59-551">Sample: [post.sentiment](#document.sentiment)</span></span>  

<a name="document.sentiment.value"></a>   
#### <a name="postsentimentvalue"></a><span data-ttu-id="c6d59-552">post.sentiment.value</span><span class="sxs-lookup"><span data-stu-id="c6d59-552">post.sentiment.value</span></span>  
<span data-ttu-id="c6d59-553">Sentiment value as a decimal value between -1 and 1.</span><span class="sxs-lookup"><span data-stu-id="c6d59-553">Sentiment value as a decimal value between -1 and 1.</span></span>  

 <span data-ttu-id="c6d59-554">Property Value Type: number</span><span class="sxs-lookup"><span data-stu-id="c6d59-554">Property Value Type: number</span></span>  

 <span data-ttu-id="c6d59-555">Parent: *post.sentiment*</span><span class="sxs-lookup"><span data-stu-id="c6d59-555">Parent: *post.sentiment*</span></span>  

 <span data-ttu-id="c6d59-556">Sample: [post.sentiment](#document.sentiment)</span><span class="sxs-lookup"><span data-stu-id="c6d59-556">Sample: [post.sentiment](#document.sentiment)</span></span>  

<a name="document.tags"></a>   
### <a name="posttags"></a><span data-ttu-id="c6d59-557">post.tags</span><span class="sxs-lookup"><span data-stu-id="c6d59-557">post.tags</span></span>  
<span data-ttu-id="c6d59-558">Array of JSON objects representing tags on a post that were added through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-558">Array of JSON objects representing tags on a post that were added through [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>  

 <span data-ttu-id="c6d59-559">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-559">Property Value Type: object</span></span>  

|<span data-ttu-id="c6d59-560">JSON element</span><span class="sxs-lookup"><span data-stu-id="c6d59-560">JSON element</span></span>|<span data-ttu-id="c6d59-561">Description</span><span class="sxs-lookup"><span data-stu-id="c6d59-561">Description</span></span>|  
|------------------|-----------------|  
|[<span data-ttu-id="c6d59-562">post.tags.probability</span><span class="sxs-lookup"><span data-stu-id="c6d59-562">post.tags.probability</span></span>](#document.tags.probability)|<span data-ttu-id="c6d59-563">Probability provided by the machine learning model with which a system tag applies to a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-563">Probability provided by the machine learning model with which a system tag applies to a post.</span></span>|  
|[<span data-ttu-id="c6d59-564">post.tags.type</span><span class="sxs-lookup"><span data-stu-id="c6d59-564">post.tags.type</span></span>](#document.tags.type)|<span data-ttu-id="c6d59-565">Describes how  the tag was assigned to a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-565">Describes how  the tag was assigned to a post.</span></span>|  
|[<span data-ttu-id="c6d59-566">post.tags.tag</span><span class="sxs-lookup"><span data-stu-id="c6d59-566">post.tags.tag</span></span>](#document.tags.tag)|<span data-ttu-id="c6d59-567">JSON object describing the tag.</span><span class="sxs-lookup"><span data-stu-id="c6d59-567">JSON object describing the tag.</span></span>|  
|[<span data-ttu-id="c6d59-568">post.tags.tag.id</span><span class="sxs-lookup"><span data-stu-id="c6d59-568">post.tags.tag.id</span></span>](#document.tags.tag.id)|<span data-ttu-id="c6d59-569">Internal ID of the tag.</span><span class="sxs-lookup"><span data-stu-id="c6d59-569">Internal ID of the tag.</span></span>|  
|[<span data-ttu-id="c6d59-570">post.tags.tag.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-570">post.tags.tag.name</span></span>](#document.tags.tag.name)|<span data-ttu-id="c6d59-571">Name of the tag.</span><span class="sxs-lookup"><span data-stu-id="c6d59-571">Name of the tag.</span></span> <span data-ttu-id="c6d59-572">Intentions are localized in the locale chosen in Global Settings.</span><span class="sxs-lookup"><span data-stu-id="c6d59-572">Intentions are localized in the locale chosen in Global Settings.</span></span>|  
|[<span data-ttu-id="c6d59-573">post.tags.tag.parentId</span><span class="sxs-lookup"><span data-stu-id="c6d59-573">post.tags.tag.parentId</span></span>](#document.tags.tag.parentId)|<span data-ttu-id="c6d59-574">ID of the group containing the tag.</span><span class="sxs-lookup"><span data-stu-id="c6d59-574">ID of the group containing the tag.</span></span>|  

 <span data-ttu-id="c6d59-575">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-575">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-576">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-576">Sample:</span></span>  

```json  
"tags": [ {  
  "probability": 0.7554345,  
  "type": "system",  
  "tag": {  
    "id": "12345",  
    "name": "Support request",  
    "parentId": "54321"  
  }, {...} ]  

```  

<span data-ttu-id="c6d59-577">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-577">Back to [top](#overview)</span></span>  

<a name="document.tags.probability"></a>   
#### <a name="posttagsprobability"></a><span data-ttu-id="c6d59-578">post.tags.probability</span><span class="sxs-lookup"><span data-stu-id="c6d59-578">post.tags.probability</span></span>  
 <span data-ttu-id="c6d59-579">Probability provided by the machine learning model with which a system tag applies to a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-579">Probability provided by the machine learning model with which a system tag applies to a post.</span></span>  

 <span data-ttu-id="c6d59-580">Property Value Type: number</span><span class="sxs-lookup"><span data-stu-id="c6d59-580">Property Value Type: number</span></span>  

 <span data-ttu-id="c6d59-581">Parent: *post.tags*</span><span class="sxs-lookup"><span data-stu-id="c6d59-581">Parent: *post.tags*</span></span>  

 <span data-ttu-id="c6d59-582">Sample: [post.tags](#document.tags)</span><span class="sxs-lookup"><span data-stu-id="c6d59-582">Sample: [post.tags](#document.tags)</span></span>  

<a name="document.tags.type"></a>   
#### <a name="posttagstype"></a><span data-ttu-id="c6d59-583">post.tags.type</span><span class="sxs-lookup"><span data-stu-id="c6d59-583">post.tags.type</span></span>  
<span data-ttu-id="c6d59-584">Describes how  the tag was assigned to a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-584">Describes how  the tag was assigned to a post.</span></span>  

> [!NOTE]
>  <span data-ttu-id="c6d59-585">Since automation rules pick up the posts before users can manually confirm or add tags to posts, this property usually has the value "system".</span><span class="sxs-lookup"><span data-stu-id="c6d59-585">Since automation rules pick up the posts before users can manually confirm or add tags to posts, this property usually has the value "system".</span></span>  

 <span data-ttu-id="c6d59-586">Property Value Type: enum</span><span class="sxs-lookup"><span data-stu-id="c6d59-586">Property Value Type: enum</span></span>  

 <span data-ttu-id="c6d59-587">Property Values:</span><span class="sxs-lookup"><span data-stu-id="c6d59-587">Property Values:</span></span>  

- <span data-ttu-id="c6d59-588">system: [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] added the tag to the post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-588">system: [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] added the tag to the post.</span></span>  

- <span data-ttu-id="c6d59-589">user: A user manually  added the tag to the post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-589">user: A user manually  added the tag to the post.</span></span>  

- <span data-ttu-id="c6d59-590">confirmed: A user confirmed a tag that was added by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-590">confirmed: A user confirmed a tag that was added by [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>  

  <span data-ttu-id="c6d59-591">Parent: *post.tags*</span><span class="sxs-lookup"><span data-stu-id="c6d59-591">Parent: *post.tags*</span></span>  

  <span data-ttu-id="c6d59-592">Sample: [post.tags](#document.tags)</span><span class="sxs-lookup"><span data-stu-id="c6d59-592">Sample: [post.tags](#document.tags)</span></span>  

<a name="document.tags.tag"></a>   
#### <a name="posttagstag"></a><span data-ttu-id="c6d59-593">post.tags.tag</span><span class="sxs-lookup"><span data-stu-id="c6d59-593">post.tags.tag</span></span>  
<span data-ttu-id="c6d59-594">JSON object describing the tag.</span><span class="sxs-lookup"><span data-stu-id="c6d59-594">JSON object describing the tag.</span></span>  

 <span data-ttu-id="c6d59-595">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-595">Property Value Type: object</span></span>  

 <span data-ttu-id="c6d59-596">Parent: *post.tags*</span><span class="sxs-lookup"><span data-stu-id="c6d59-596">Parent: *post.tags*</span></span>  

 <span data-ttu-id="c6d59-597">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-597">Sample:</span></span>  

```json  
"tag": {  
  "id": "12345",  
  "name": "Support request",  
  "parentId": "54321"  
},  
```  

<a name="document.tags.tag.id"></a>   
##### <a name="posttagstagid"></a><span data-ttu-id="c6d59-598">post.tags.tag.id</span><span class="sxs-lookup"><span data-stu-id="c6d59-598">post.tags.tag.id</span></span>  
<span data-ttu-id="c6d59-599">Internal ID of the tag.</span><span class="sxs-lookup"><span data-stu-id="c6d59-599">Internal ID of the tag.</span></span>  

 <span data-ttu-id="c6d59-600">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-600">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-601">Parent: *post.tags.tag*</span><span class="sxs-lookup"><span data-stu-id="c6d59-601">Parent: *post.tags.tag*</span></span>  

 <span data-ttu-id="c6d59-602">Sample: [post.tags.tag](#document.tags.tag)</span><span class="sxs-lookup"><span data-stu-id="c6d59-602">Sample: [post.tags.tag](#document.tags.tag)</span></span>  

<a name="document.tags.tag.name"></a>   
##### <a name="posttagstagname"></a><span data-ttu-id="c6d59-603">post.tags.tag.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-603">post.tags.tag.name</span></span>  
<span data-ttu-id="c6d59-604">Name of the tag.</span><span class="sxs-lookup"><span data-stu-id="c6d59-604">Name of the tag.</span></span> <span data-ttu-id="c6d59-605">Intentions are localized in the locale chosen in Global Settings.</span><span class="sxs-lookup"><span data-stu-id="c6d59-605">Intentions are localized in the locale chosen in Global Settings.</span></span> <span data-ttu-id="c6d59-606">More information: [Understand an author's intent using intention analysis](tags.md)</span><span class="sxs-lookup"><span data-stu-id="c6d59-606">More information: [Understand an author's intent using intention analysis](tags.md)</span></span>  

 <span data-ttu-id="c6d59-607">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-607">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-608">Parent: *post.tags.tag*</span><span class="sxs-lookup"><span data-stu-id="c6d59-608">Parent: *post.tags.tag*</span></span>  

 <span data-ttu-id="c6d59-609">Sample: [post.tags.tag](#document.tags.tag)</span><span class="sxs-lookup"><span data-stu-id="c6d59-609">Sample: [post.tags.tag](#document.tags.tag)</span></span>  

<a name="document.tags.tag.parentId"></a>   
##### <a name="posttagstagparentid"></a><span data-ttu-id="c6d59-610">post.tags.tag.parentId</span><span class="sxs-lookup"><span data-stu-id="c6d59-610">post.tags.tag.parentId</span></span>  
<span data-ttu-id="c6d59-611">ID of the group containing the tag.</span><span class="sxs-lookup"><span data-stu-id="c6d59-611">ID of the group containing the tag.</span></span>  

 <span data-ttu-id="c6d59-612">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-612">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-613">Parent: *post.tags.tag*</span><span class="sxs-lookup"><span data-stu-id="c6d59-613">Parent: *post.tags.tag*</span></span>  

 <span data-ttu-id="c6d59-614">Sample: [post.tags.tag](#document.tags.tag)</span><span class="sxs-lookup"><span data-stu-id="c6d59-614">Sample: [post.tags.tag](#document.tags.tag)</span></span>  

<a name="document.externalId"></a>   
### <a name="postexternalid"></a><span data-ttu-id="c6d59-615">post.externalId</span><span class="sxs-lookup"><span data-stu-id="c6d59-615">post.externalId</span></span>  
<span data-ttu-id="c6d59-616">ID of the post on the source.</span><span class="sxs-lookup"><span data-stu-id="c6d59-616">ID of the post on the source.</span></span>  

 <span data-ttu-id="c6d59-617">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-617">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-618">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-618">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-619">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-619">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-620">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-620">Back to [top](#overview)</span></span>  

<a name="document.postLocation"></a>   
### <a name="postpostlocation"></a><span data-ttu-id="c6d59-621">post.postLocation</span><span class="sxs-lookup"><span data-stu-id="c6d59-621">post.postLocation</span></span>  
<span data-ttu-id="c6d59-622">JSON object describing the location from which a post was published.</span><span class="sxs-lookup"><span data-stu-id="c6d59-622">JSON object describing the location from which a post was published.</span></span>  

 <span data-ttu-id="c6d59-623">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-623">Property Value Type: object</span></span>  

|<span data-ttu-id="c6d59-624">JSON element</span><span class="sxs-lookup"><span data-stu-id="c6d59-624">JSON element</span></span>|<span data-ttu-id="c6d59-625">Description</span><span class="sxs-lookup"><span data-stu-id="c6d59-625">Description</span></span>|  
|------------------|-----------------|  
|[<span data-ttu-id="c6d59-626">post.postLocation.locality</span><span class="sxs-lookup"><span data-stu-id="c6d59-626">post.postLocation.locality</span></span>](#document.postLocation.locality)|<span data-ttu-id="c6d59-627">Represents the name of a city.</span><span class="sxs-lookup"><span data-stu-id="c6d59-627">Represents the name of a city.</span></span>|  
|[<span data-ttu-id="c6d59-628">post.postLocation.adminDistrict</span><span class="sxs-lookup"><span data-stu-id="c6d59-628">post.postLocation.adminDistrict</span></span>](#document.postLocation.adminDistrict)|<span data-ttu-id="c6d59-629">Represents the name of an administrative division, for example a federal state or a province.</span><span class="sxs-lookup"><span data-stu-id="c6d59-629">Represents the name of an administrative division, for example a federal state or a province.</span></span>|  
|[<span data-ttu-id="c6d59-630">post.postLocation.countryRegion</span><span class="sxs-lookup"><span data-stu-id="c6d59-630">post.postLocation.countryRegion</span></span>](#document.postLocation.countryRegion)|<span data-ttu-id="c6d59-631">Represents the name of a country or region.</span><span class="sxs-lookup"><span data-stu-id="c6d59-631">Represents the name of a country or region.</span></span>|  
|[<span data-ttu-id="c6d59-632">post.postLocation.coordinates</span><span class="sxs-lookup"><span data-stu-id="c6d59-632">post.postLocation.coordinates</span></span>](#document.postLocation.coordinates)|<span data-ttu-id="c6d59-633">JSON object describing the coordinates of a post as defined by the author with latitude and longitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-633">JSON object describing the coordinates of a post as defined by the author with latitude and longitude.</span></span>|  
|[<span data-ttu-id="c6d59-634">post.postLocation.coordinates.latitude</span><span class="sxs-lookup"><span data-stu-id="c6d59-634">post.postLocation.coordinates.latitude</span></span>](#document.postLocation.coordinates.latitude)|<span data-ttu-id="c6d59-635">Geographic latitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-635">Geographic latitude.</span></span>|  
|[<span data-ttu-id="c6d59-636">post.postLocation.coordinates.longitude</span><span class="sxs-lookup"><span data-stu-id="c6d59-636">post.postLocation.coordinates.longitude</span></span>](#document.postLocation.coordinates.longitude)|<span data-ttu-id="c6d59-637">Geographic longitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-637">Geographic longitude.</span></span>|  
|[<span data-ttu-id="c6d59-638">post.postLocation.quadkey</span><span class="sxs-lookup"><span data-stu-id="c6d59-638">post.postLocation.quadkey</span></span>](#document.postLocation.quadkey)|<span data-ttu-id="c6d59-639">Quadtree key of a location, or “quadkey” for short.</span><span class="sxs-lookup"><span data-stu-id="c6d59-639">Quadtree key of a location, or “quadkey” for short.</span></span> <span data-ttu-id="c6d59-640">Identifies a single tile at a particular level of detail on a map.</span><span class="sxs-lookup"><span data-stu-id="c6d59-640">Identifies a single tile at a particular level of detail on a map.</span></span>|  

 <span data-ttu-id="c6d59-641">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-641">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-642">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-642">Sample:</span></span>  

```json  
"postLocation": {  
  "adminDistrict": "Massachusetts",  
  "countryRegion": "United States",  
  "coordinates": {  
    "latitude": 42.156028747558594,  
    "longitude": -71.56590270996094  
  },  
  "quadKey": "030233212221101333012"  
},  
```  

 <span data-ttu-id="c6d59-643">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-643">Back to [top](#overview)</span></span>  

<a name="document.postLocation.locality"></a>   
#### <a name="postpostlocationlocality"></a><span data-ttu-id="c6d59-644">post.postLocation.locality</span><span class="sxs-lookup"><span data-stu-id="c6d59-644">post.postLocation.locality</span></span>  
<span data-ttu-id="c6d59-645">Represents the name of a city.</span><span class="sxs-lookup"><span data-stu-id="c6d59-645">Represents the name of a city.</span></span>  

 <span data-ttu-id="c6d59-646">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-646">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-647">Parent: *post.postLocation*</span><span class="sxs-lookup"><span data-stu-id="c6d59-647">Parent: *post.postLocation*</span></span>  

 <span data-ttu-id="c6d59-648">Sample: [post.postLocation](#document.postLocation)</span><span class="sxs-lookup"><span data-stu-id="c6d59-648">Sample: [post.postLocation](#document.postLocation)</span></span>  

<a name="document.postLocation.adminDistrict"></a>   
#### <a name="postpostlocationadmindistrict"></a><span data-ttu-id="c6d59-649">post.postLocation.adminDistrict</span><span class="sxs-lookup"><span data-stu-id="c6d59-649">post.postLocation.adminDistrict</span></span>  
<span data-ttu-id="c6d59-650">Represents the name of an administrative division, for example a federal state or a province.</span><span class="sxs-lookup"><span data-stu-id="c6d59-650">Represents the name of an administrative division, for example a federal state or a province.</span></span>  

 <span data-ttu-id="c6d59-651">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-651">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-652">Parent: *post.postLocation*</span><span class="sxs-lookup"><span data-stu-id="c6d59-652">Parent: *post.postLocation*</span></span>  

 <span data-ttu-id="c6d59-653">Sample: [post.postLocation](#document.postLocation)</span><span class="sxs-lookup"><span data-stu-id="c6d59-653">Sample: [post.postLocation](#document.postLocation)</span></span>  

<a name="document.postLocation.countryRegion"></a>   
#### <a name="postpostlocationcountryregion"></a><span data-ttu-id="c6d59-654">post.postLocation.countryRegion</span><span class="sxs-lookup"><span data-stu-id="c6d59-654">post.postLocation.countryRegion</span></span>  
<span data-ttu-id="c6d59-655">Represents the name of a country or region.</span><span class="sxs-lookup"><span data-stu-id="c6d59-655">Represents the name of a country or region.</span></span>  

 <span data-ttu-id="c6d59-656">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-656">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-657">Parent: *post.postLocation*</span><span class="sxs-lookup"><span data-stu-id="c6d59-657">Parent: *post.postLocation*</span></span>  

 <span data-ttu-id="c6d59-658">Sample: [post.postLocation](#document.postLocation)</span><span class="sxs-lookup"><span data-stu-id="c6d59-658">Sample: [post.postLocation](#document.postLocation)</span></span>  

<a name="document.postLocation.coordinates"></a>   
#### <a name="postpostlocationcoordinates"></a><span data-ttu-id="c6d59-659">post.postLocation.coordinates</span><span class="sxs-lookup"><span data-stu-id="c6d59-659">post.postLocation.coordinates</span></span>  
<span data-ttu-id="c6d59-660">JSON object describing the coordinates of a post as defined by the author with latitude and longitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-660">JSON object describing the coordinates of a post as defined by the author with latitude and longitude.</span></span>  

 <span data-ttu-id="c6d59-661">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-661">Property Value Type: object</span></span>  

 <span data-ttu-id="c6d59-662">Parent: *post.postLocation*</span><span class="sxs-lookup"><span data-stu-id="c6d59-662">Parent: *post.postLocation*</span></span>  

 <span data-ttu-id="c6d59-663">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-663">Sample:</span></span>  

```json  
"coordinates": {  
  "latitude": 42.156028747558594,  
  "longitude": -71.56590270996094  
},  
```  

<a name="document.postLocation.coordinates.latitude"></a>   
##### <a name="postpostlocationcoordinateslatitude"></a><span data-ttu-id="c6d59-664">post.postLocation.coordinates.latitude</span><span class="sxs-lookup"><span data-stu-id="c6d59-664">post.postLocation.coordinates.latitude</span></span>  
<span data-ttu-id="c6d59-665">Geographic latitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-665">Geographic latitude.</span></span>  

 <span data-ttu-id="c6d59-666">Property Value Type: number (floating point)</span><span class="sxs-lookup"><span data-stu-id="c6d59-666">Property Value Type: number (floating point)</span></span>  

 <span data-ttu-id="c6d59-667">Parent: *post.profile.profileLocation.coordinates*</span><span class="sxs-lookup"><span data-stu-id="c6d59-667">Parent: *post.profile.profileLocation.coordinates*</span></span>  

 <span data-ttu-id="c6d59-668">Sample: [post.postLocation.coordinates](#document.postLocation.coordinates)</span><span class="sxs-lookup"><span data-stu-id="c6d59-668">Sample: [post.postLocation.coordinates](#document.postLocation.coordinates)</span></span>  

<a name="document.postLocation.coordinates.longitude"></a>   
##### <a name="postpostlocationcoordinateslongitude"></a><span data-ttu-id="c6d59-669">post.postLocation.coordinates.longitude</span><span class="sxs-lookup"><span data-stu-id="c6d59-669">post.postLocation.coordinates.longitude</span></span>  
<span data-ttu-id="c6d59-670">Geographic longitude.</span><span class="sxs-lookup"><span data-stu-id="c6d59-670">Geographic longitude.</span></span>  

 <span data-ttu-id="c6d59-671">Property Value Type: number (floating point)</span><span class="sxs-lookup"><span data-stu-id="c6d59-671">Property Value Type: number (floating point)</span></span>  

 <span data-ttu-id="c6d59-672">Parent: *post.postLocation.coordinates*</span><span class="sxs-lookup"><span data-stu-id="c6d59-672">Parent: *post.postLocation.coordinates*</span></span>  

 <span data-ttu-id="c6d59-673">Sample: [post.postLocation.coordinates](#document.postLocation.coordinates)</span><span class="sxs-lookup"><span data-stu-id="c6d59-673">Sample: [post.postLocation.coordinates](#document.postLocation.coordinates)</span></span>  

<a name="document.postLocation.quadkey"></a>   
#### <a name="postpostlocationquadkey"></a><span data-ttu-id="c6d59-674">post.postLocation.quadkey</span><span class="sxs-lookup"><span data-stu-id="c6d59-674">post.postLocation.quadkey</span></span>  
<span data-ttu-id="c6d59-675">Quadtree key of a location, or “quadkey” for short.</span><span class="sxs-lookup"><span data-stu-id="c6d59-675">Quadtree key of a location, or “quadkey” for short.</span></span> <span data-ttu-id="c6d59-676">Identifies a single tile at a particular level of detail on a map.</span><span class="sxs-lookup"><span data-stu-id="c6d59-676">Identifies a single tile at a particular level of detail on a map.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="c6d59-677">[MSDN: Bing Maps Tile System](https://msdn.microsoft.com/library/bb259689.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6d59-677">[MSDN: Bing Maps Tile System](https://msdn.microsoft.com/library/bb259689.aspx)</span></span>  

 <span data-ttu-id="c6d59-678">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-678">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-679">Parent: *post.postLocation*</span><span class="sxs-lookup"><span data-stu-id="c6d59-679">Parent: *post.postLocation*</span></span>  

 <span data-ttu-id="c6d59-680">Sample: [post.postLocation](#document.postLocation)</span><span class="sxs-lookup"><span data-stu-id="c6d59-680">Sample: [post.postLocation](#document.postLocation)</span></span>  

 <span data-ttu-id="c6d59-681">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-681">Back to [top](#overview)</span></span>  

<a name="document.fullContentLenght"></a>   
### <a name="postfullcontentlength"></a><span data-ttu-id="c6d59-682">post.fullContentLength</span><span class="sxs-lookup"><span data-stu-id="c6d59-682">post.fullContentLength</span></span>  
<span data-ttu-id="c6d59-683">Length in characters of the text-only content in a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-683">Length in characters of the text-only content in a post.</span></span>  

 <span data-ttu-id="c6d59-684">Property Value Type: number (integer)</span><span class="sxs-lookup"><span data-stu-id="c6d59-684">Property Value Type: number (integer)</span></span>  

 <span data-ttu-id="c6d59-685">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-685">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-686">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-686">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-687">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-687">Back to [top](#overview)</span></span>  

<a name="document.origin"></a>   
### <a name="postorigin"></a><span data-ttu-id="c6d59-688">post.origin</span><span class="sxs-lookup"><span data-stu-id="c6d59-688">post.origin</span></span>  
<span data-ttu-id="c6d59-689">JSON object describing the origin of the post on the source.</span><span class="sxs-lookup"><span data-stu-id="c6d59-689">JSON object describing the origin of the post on the source.</span></span> <span data-ttu-id="c6d59-690">This is different from the post.source object.</span><span class="sxs-lookup"><span data-stu-id="c6d59-690">This is different from the post.source object.</span></span>  <span data-ttu-id="c6d59-691">For example: A specific Facebook page on the Facebook source.</span><span class="sxs-lookup"><span data-stu-id="c6d59-691">For example: A specific Facebook page on the Facebook source.</span></span>  

 <span data-ttu-id="c6d59-692">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-692">Property Value Type: object</span></span>  

 <span data-ttu-id="c6d59-693">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-693">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-694">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-694">Sample:</span></span>  

```json  
"origin": {  
  "id": "12345",  
  "externalId": "54321",  
  "name": "Microsoft Facebook Page",  
},  
```  

<span data-ttu-id="c6d59-695">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-695">Back to [top](#overview)</span></span>  

<a name="document.origin.id"></a>   
#### <a name="postoriginid"></a><span data-ttu-id="c6d59-696">post.origin.id</span><span class="sxs-lookup"><span data-stu-id="c6d59-696">post.origin.id</span></span>  
<span data-ttu-id="c6d59-697">ID of the internal representation in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] for the origin of a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-697">ID of the internal representation in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] for the origin of a post.</span></span>  

 <span data-ttu-id="c6d59-698">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-698">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-699">Parent: *post.origin*</span><span class="sxs-lookup"><span data-stu-id="c6d59-699">Parent: *post.origin*</span></span>  

 <span data-ttu-id="c6d59-700">Sample: [post.origin](#document.origin)</span><span class="sxs-lookup"><span data-stu-id="c6d59-700">Sample: [post.origin](#document.origin)</span></span>  

<a name="document.origin.externalId"></a>   
#### <a name="postoriginexternalid"></a><span data-ttu-id="c6d59-701">post.origin.externalId</span><span class="sxs-lookup"><span data-stu-id="c6d59-701">post.origin.externalId</span></span>  
<span data-ttu-id="c6d59-702">ID of the origin for the original source of a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-702">ID of the origin for the original source of a post.</span></span>  

 <span data-ttu-id="c6d59-703">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-703">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-704">Parent: *post.origin*</span><span class="sxs-lookup"><span data-stu-id="c6d59-704">Parent: *post.origin*</span></span>  

 <span data-ttu-id="c6d59-705">Sample: [post.origin](#document.origin)</span><span class="sxs-lookup"><span data-stu-id="c6d59-705">Sample: [post.origin](#document.origin)</span></span>  

<a name="document.origin.forumName"></a>   
#### <a name="postoriginname"></a><span data-ttu-id="c6d59-706">post.origin.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-706">post.origin.name</span></span>  
<span data-ttu-id="c6d59-707">Name of the origin of the post on the source.</span><span class="sxs-lookup"><span data-stu-id="c6d59-707">Name of the origin of the post on the source.</span></span>  

 <span data-ttu-id="c6d59-708">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-708">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-709">Parent: *post.origin*</span><span class="sxs-lookup"><span data-stu-id="c6d59-709">Parent: *post.origin*</span></span>  

 <span data-ttu-id="c6d59-710">Sample: [post.origin](#document.origin)</span><span class="sxs-lookup"><span data-stu-id="c6d59-710">Sample: [post.origin](#document.origin)</span></span>  

<a name="document.matchingSeachTopics"></a>   
### <a name="postmatchingsearchtopics"></a><span data-ttu-id="c6d59-711">post.matchingSearchTopics</span><span class="sxs-lookup"><span data-stu-id="c6d59-711">post.matchingSearchTopics</span></span>  
<span data-ttu-id="c6d59-712">Array of JSON objects describing the list of search topics a post matches.</span><span class="sxs-lookup"><span data-stu-id="c6d59-712">Array of JSON objects describing the list of search topics a post matches.</span></span>  

 <span data-ttu-id="c6d59-713">Property Value Type: object</span><span class="sxs-lookup"><span data-stu-id="c6d59-713">Property Value Type: object</span></span>  

 <span data-ttu-id="c6d59-714">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-714">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-715">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-715">Sample:</span></span>  

```json  
        "matchingSearchTopics": [{  
          "name": "Contoso Brand Mentions",  
          "id": "12345",  
          "parentId": "54321",  
        },  
{...}]  
```  

<span data-ttu-id="c6d59-716">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-716">Back to [top](#overview)</span></span>  

<a name="document.matchingSeachTopics.name"></a>   
#### <a name="postmatchingsearchtopicsname"></a><span data-ttu-id="c6d59-717">post.matchingSearchTopics.name</span><span class="sxs-lookup"><span data-stu-id="c6d59-717">post.matchingSearchTopics.name</span></span>  
<span data-ttu-id="c6d59-718">Name of the search topic as defined in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d59-718">Name of the search topic as defined in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="c6d59-719">[Set up searches to listen to social media conversations](set-up-searches.md)</span><span class="sxs-lookup"><span data-stu-id="c6d59-719">[Set up searches to listen to social media conversations](set-up-searches.md)</span></span>  

 <span data-ttu-id="c6d59-720">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-720">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-721">Parent: *post.matchingSearchTopics*</span><span class="sxs-lookup"><span data-stu-id="c6d59-721">Parent: *post.matchingSearchTopics*</span></span>  

 <span data-ttu-id="c6d59-722">Sample: [post.matchingSearchTopics](#document.matchingSeachTopics)</span><span class="sxs-lookup"><span data-stu-id="c6d59-722">Sample: [post.matchingSearchTopics](#document.matchingSeachTopics)</span></span>  

<a name="document.matchingSeachTopics.id"></a>   
#### <a name="postmatchingsearchtopicsid"></a><span data-ttu-id="c6d59-723">post.matchingSearchTopics.id</span><span class="sxs-lookup"><span data-stu-id="c6d59-723">post.matchingSearchTopics.id</span></span>  
<span data-ttu-id="c6d59-724">ID of the search topic.</span><span class="sxs-lookup"><span data-stu-id="c6d59-724">ID of the search topic.</span></span>  

 <span data-ttu-id="c6d59-725">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-725">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-726">Parent: *post.matchingSearchTopics*</span><span class="sxs-lookup"><span data-stu-id="c6d59-726">Parent: *post.matchingSearchTopics*</span></span>  

 <span data-ttu-id="c6d59-727">Sample: [post.matchingSearchTopics](#document.matchingSeachTopics)</span><span class="sxs-lookup"><span data-stu-id="c6d59-727">Sample: [post.matchingSearchTopics](#document.matchingSeachTopics)</span></span>  

<a name="document.matchingSeachTopics.parentId"></a>   
#### <a name="postmatchingsearchtopicsparentid"></a><span data-ttu-id="c6d59-728">post.matchingSearchTopics.parentId</span><span class="sxs-lookup"><span data-stu-id="c6d59-728">post.matchingSearchTopics.parentId</span></span>  
<span data-ttu-id="c6d59-729">ID of the search topics's category.</span><span class="sxs-lookup"><span data-stu-id="c6d59-729">ID of the search topics's category.</span></span>  

 <span data-ttu-id="c6d59-730">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-730">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-731">Parent: *post.matchingSearchTopics*</span><span class="sxs-lookup"><span data-stu-id="c6d59-731">Parent: *post.matchingSearchTopics*</span></span>  

 <span data-ttu-id="c6d59-732">Sample: [post.matchingSearchTopics](#document.matchingSeachTopics)</span><span class="sxs-lookup"><span data-stu-id="c6d59-732">Sample: [post.matchingSearchTopics](#document.matchingSeachTopics)</span></span>  

<a name="document.externalCategories"></a>   
### <a name="postexternalcategories"></a><span data-ttu-id="c6d59-733">post.externalCategories</span><span class="sxs-lookup"><span data-stu-id="c6d59-733">post.externalCategories</span></span>  
<span data-ttu-id="c6d59-734">Array of categories as delivered by external providers.</span><span class="sxs-lookup"><span data-stu-id="c6d59-734">Array of categories as delivered by external providers.</span></span>  

> [!NOTE]
>  <span data-ttu-id="c6d59-735">This property is only available for News posts.</span><span class="sxs-lookup"><span data-stu-id="c6d59-735">This property is only available for News posts.</span></span>  

 <span data-ttu-id="c6d59-736">Property Value Type: array of strings</span><span class="sxs-lookup"><span data-stu-id="c6d59-736">Property Value Type: array of strings</span></span>  

 <span data-ttu-id="c6d59-737">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-737">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-738">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-738">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-739">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-739">Back to [top](#overview)</span></span>  

<a name="document.contributors"></a>   
### <a name="postcontributors"></a><span data-ttu-id="c6d59-740">post.contributors</span><span class="sxs-lookup"><span data-stu-id="c6d59-740">post.contributors</span></span>  
<span data-ttu-id="c6d59-741">Array of names of those who contributed to the post as provided by the data provider.</span><span class="sxs-lookup"><span data-stu-id="c6d59-741">Array of names of those who contributed to the post as provided by the data provider.</span></span>  

> [!NOTE]
>  <span data-ttu-id="c6d59-742">This property is only available for News posts.</span><span class="sxs-lookup"><span data-stu-id="c6d59-742">This property is only available for News posts.</span></span>  

 <span data-ttu-id="c6d59-743">Property Value Type: array of strings</span><span class="sxs-lookup"><span data-stu-id="c6d59-743">Property Value Type: array of strings</span></span>  

 <span data-ttu-id="c6d59-744">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-744">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-745">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-745">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-746">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-746">Back to [top](#overview)</span></span>  

<a name="document.media"></a>   
### <a name="postmedia"></a><span data-ttu-id="c6d59-747">post.media</span><span class="sxs-lookup"><span data-stu-id="c6d59-747">post.media</span></span>  
<span data-ttu-id="c6d59-748">Array of JSON objects describing the media in a post.</span><span class="sxs-lookup"><span data-stu-id="c6d59-748">Array of JSON objects describing the media in a post.</span></span>  

 <span data-ttu-id="c6d59-749">Property Value Type: objects</span><span class="sxs-lookup"><span data-stu-id="c6d59-749">Property Value Type: objects</span></span>  

|<span data-ttu-id="c6d59-750">JSON element</span><span class="sxs-lookup"><span data-stu-id="c6d59-750">JSON element</span></span>|<span data-ttu-id="c6d59-751">Description</span><span class="sxs-lookup"><span data-stu-id="c6d59-751">Description</span></span>|  
|------------------|-----------------|  
|[<span data-ttu-id="c6d59-752">post.media.type</span><span class="sxs-lookup"><span data-stu-id="c6d59-752">post.media.type</span></span>](#document.media.type)|<span data-ttu-id="c6d59-753">The type of media content.</span><span class="sxs-lookup"><span data-stu-id="c6d59-753">The type of media content.</span></span>|  
|[<span data-ttu-id="c6d59-754">post.media.embedUrl</span><span class="sxs-lookup"><span data-stu-id="c6d59-754">post.media.embedUrl</span></span>](#document.media.embedUrl)|<span data-ttu-id="c6d59-755">URL embedding the media file.</span><span class="sxs-lookup"><span data-stu-id="c6d59-755">URL embedding the media file.</span></span>|  

 <span data-ttu-id="c6d59-756">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-756">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-757">Sample:</span><span class="sxs-lookup"><span data-stu-id="c6d59-757">Sample:</span></span>  

```json  
"media": {  
  "type": "VIDEO",  
  "embedUrl": "http://www.youtube.com/embed/1dWKf8d8zfg"  
},  
```  

<span data-ttu-id="c6d59-758">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-758">Back to [top](#overview)</span></span>  

<a name="document.media.type"></a>   
#### <a name="postmediatype"></a><span data-ttu-id="c6d59-759">post.media.type</span><span class="sxs-lookup"><span data-stu-id="c6d59-759">post.media.type</span></span>  
<span data-ttu-id="c6d59-760">The type of media content.</span><span class="sxs-lookup"><span data-stu-id="c6d59-760">The type of media content.</span></span>  

 <span data-ttu-id="c6d59-761">Property Value Type: enum</span><span class="sxs-lookup"><span data-stu-id="c6d59-761">Property Value Type: enum</span></span>  

 <span data-ttu-id="c6d59-762">Property Values:</span><span class="sxs-lookup"><span data-stu-id="c6d59-762">Property Values:</span></span>  

- <span data-ttu-id="c6d59-763">POST: The main media content is text.</span><span class="sxs-lookup"><span data-stu-id="c6d59-763">POST: The main media content is text.</span></span>  

- <span data-ttu-id="c6d59-764">IMAGE: The main media content is a picture.</span><span class="sxs-lookup"><span data-stu-id="c6d59-764">IMAGE: The main media content is a picture.</span></span>  

- <span data-ttu-id="c6d59-765">VIDEO: The main media content is a video.</span><span class="sxs-lookup"><span data-stu-id="c6d59-765">VIDEO: The main media content is a video.</span></span>  

- <span data-ttu-id="c6d59-766">LINK: The main media content is a hyperlink.</span><span class="sxs-lookup"><span data-stu-id="c6d59-766">LINK: The main media content is a hyperlink.</span></span>  

  <span data-ttu-id="c6d59-767">Parent: *post.media*</span><span class="sxs-lookup"><span data-stu-id="c6d59-767">Parent: *post.media*</span></span>  

  <span data-ttu-id="c6d59-768">Sample: [post.media](#document.media)</span><span class="sxs-lookup"><span data-stu-id="c6d59-768">Sample: [post.media](#document.media)</span></span>  

<a name="document.media.embedUrl"></a>   
#### <a name="postmediaembedurl"></a><span data-ttu-id="c6d59-769">post.media.embedUrl</span><span class="sxs-lookup"><span data-stu-id="c6d59-769">post.media.embedUrl</span></span>  
<span data-ttu-id="c6d59-770">URL embedding the media file.</span><span class="sxs-lookup"><span data-stu-id="c6d59-770">URL embedding the media file.</span></span>  

 <span data-ttu-id="c6d59-771">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-771">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-772">Parent: *post.media*</span><span class="sxs-lookup"><span data-stu-id="c6d59-772">Parent: *post.media*</span></span>  

 <span data-ttu-id="c6d59-773">Sample: [post.media](#document.media)</span><span class="sxs-lookup"><span data-stu-id="c6d59-773">Sample: [post.media](#document.media)</span></span>  

<a name="document.externalTopics"></a>   
### <a name="postexternaltopics"></a><span data-ttu-id="c6d59-774">post.externalTopics</span><span class="sxs-lookup"><span data-stu-id="c6d59-774">post.externalTopics</span></span>  
<span data-ttu-id="c6d59-775">Array of topics in this post as delivered by external providers.</span><span class="sxs-lookup"><span data-stu-id="c6d59-775">Array of topics in this post as delivered by external providers.</span></span>  

 <span data-ttu-id="c6d59-776">Property Value Type: array of strings</span><span class="sxs-lookup"><span data-stu-id="c6d59-776">Property Value Type: array of strings</span></span>  

 <span data-ttu-id="c6d59-777">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-777">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-778">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-778">Sample: [post sample payload](#document_sample_payload)</span></span>  

 <span data-ttu-id="c6d59-779">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-779">Back to [top](#overview)</span></span>  

<a name="document.contributorSummary"></a>   
### <a name="postcontributorsummary"></a><span data-ttu-id="c6d59-780">post.contributorSummary</span><span class="sxs-lookup"><span data-stu-id="c6d59-780">post.contributorSummary</span></span>  
<span data-ttu-id="c6d59-781">Short description about the contributor for this post as delivered by external providers.</span><span class="sxs-lookup"><span data-stu-id="c6d59-781">Short description about the contributor for this post as delivered by external providers.</span></span>  

 <span data-ttu-id="c6d59-782">Property Value Type: string</span><span class="sxs-lookup"><span data-stu-id="c6d59-782">Property Value Type: string</span></span>  

 <span data-ttu-id="c6d59-783">Parent: *post*</span><span class="sxs-lookup"><span data-stu-id="c6d59-783">Parent: *post*</span></span>  

 <span data-ttu-id="c6d59-784">Sample: [post sample payload](#document_sample_payload)</span><span class="sxs-lookup"><span data-stu-id="c6d59-784">Sample: [post sample payload](#document_sample_payload)</span></span>  

<span data-ttu-id="c6d59-785">Back to [top](#overview)</span><span class="sxs-lookup"><span data-stu-id="c6d59-785">Back to [top](#overview)</span></span>

### <a name="see-also"></a><span data-ttu-id="c6d59-786">See Also</span><span class="sxs-lookup"><span data-stu-id="c6d59-786">See Also</span></span>  
<span data-ttu-id="c6d59-787">[Manage connections in Social Engagement](manage-connections.md) </span><span class="sxs-lookup"><span data-stu-id="c6d59-787">[Manage connections in Social Engagement](manage-connections.md) </span></span>  
<span data-ttu-id="c6d59-788">[Stream data from Social Engagement to Microsoft Azure Event Hubs](stream-data-to-event-hubs.md) </span><span class="sxs-lookup"><span data-stu-id="c6d59-788">[Stream data from Social Engagement to Microsoft Azure Event Hubs](stream-data-to-event-hubs.md) </span></span>  
[<span data-ttu-id="c6d59-789">Work with events from social posts in Azure Event Hubs</span><span class="sxs-lookup"><span data-stu-id="c6d59-789">Work with events from social posts in Azure Event Hubs</span></span>](work-with-event-hubs.md)
