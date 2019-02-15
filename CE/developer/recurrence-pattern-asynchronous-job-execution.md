---
title: Recurrence pattern in asynchronous job execution (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about executing asynchronous system operations one time or on a recurring basis by using a recurrence rule. Use the AsyncOperation.RecurrencePattern attribute to specify the recurrence rule.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: abfb5df5-138b-4c7e-8730-4903aa2be3d3
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 47b769338f43bc3b2640e751b76fb8afbdbdd465
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385835"
---
# <a name="recurrence-pattern-in-asynchronous-job-execution"></a><span data-ttu-id="a30f4-104">Recurrence pattern in asynchronous job execution</span><span class="sxs-lookup"><span data-stu-id="a30f4-104">Recurrence pattern in asynchronous job execution</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a30f4-105">You can execute asynchronous system operations one time or on a recurring basis by using a recurrence rule.</span><span class="sxs-lookup"><span data-stu-id="a30f4-105">You can execute asynchronous system operations one time or on a recurring basis by using a recurrence rule.</span></span> <span data-ttu-id="a30f4-106">Use the `AsyncOperation.RecurrencePattern` attribute to specify the recurrence rule.</span><span class="sxs-lookup"><span data-stu-id="a30f4-106">Use the `AsyncOperation.RecurrencePattern` attribute to specify the recurrence rule.</span></span> <span data-ttu-id="a30f4-107">This property is included in the request classes of the<xref:Microsoft.Xrm.Sdk.IOrganizationService> messages that submit asynchronous jobs, such as bulk delete, or bulk detect duplicates.</span><span class="sxs-lookup"><span data-stu-id="a30f4-107">This property is included in the request classes of the<xref:Microsoft.Xrm.Sdk.IOrganizationService> messages that submit asynchronous jobs, such as bulk delete, or bulk detect duplicates.</span></span> <span data-ttu-id="a30f4-108">It is also included in the entities that represent asynchronous operations, such as the `AsyncOperation` (system job) entity.</span><span class="sxs-lookup"><span data-stu-id="a30f4-108">It is also included in the entities that represent asynchronous operations, such as the `AsyncOperation` (system job) entity.</span></span>  
  
 <span data-ttu-id="a30f4-109">Use the following format to set the `AsyncOperation.RecurrencePattern` attribute.</span><span class="sxs-lookup"><span data-stu-id="a30f4-109">Use the following format to set the `AsyncOperation.RecurrencePattern` attribute.</span></span>  
  
|<span data-ttu-id="a30f4-110">Recurrence pattern</span><span class="sxs-lookup"><span data-stu-id="a30f4-110">Recurrence pattern</span></span>|<span data-ttu-id="a30f4-111">Frequency of job execution</span><span class="sxs-lookup"><span data-stu-id="a30f4-111">Frequency of job execution</span></span>|  
|------------------------|--------------------------------|  
|<span data-ttu-id="a30f4-112">"FREQ=MONTHLY;"</span><span class="sxs-lookup"><span data-stu-id="a30f4-112">"FREQ=MONTHLY;"</span></span>|<span data-ttu-id="a30f4-113">Once a month</span><span class="sxs-lookup"><span data-stu-id="a30f4-113">Once a month</span></span>|  
|<span data-ttu-id="a30f4-114">"FREQ=WEEKLY;"</span><span class="sxs-lookup"><span data-stu-id="a30f4-114">"FREQ=WEEKLY;"</span></span>|<span data-ttu-id="a30f4-115">Once a week</span><span class="sxs-lookup"><span data-stu-id="a30f4-115">Once a week</span></span>|  
|<span data-ttu-id="a30f4-116">FREQ=DAILY;"</span><span class="sxs-lookup"><span data-stu-id="a30f4-116">FREQ=DAILY;"</span></span>|<span data-ttu-id="a30f4-117">Once a day</span><span class="sxs-lookup"><span data-stu-id="a30f4-117">Once a day</span></span>|  
|<span data-ttu-id="a30f4-118">"FREQ=HOURLY;"</span><span class="sxs-lookup"><span data-stu-id="a30f4-118">"FREQ=HOURLY;"</span></span>|<span data-ttu-id="a30f4-119">Once an hour</span><span class="sxs-lookup"><span data-stu-id="a30f4-119">Once an hour</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="a30f4-120">A complete format for a recurrence rule is described in the [RFC2445](http://go.microsoft.com/fwlink/p/?LinkId=262221) Internet standard (Internet Calendaring and Scheduling Core Object Specification).</span><span class="sxs-lookup"><span data-stu-id="a30f4-120">A complete format for a recurrence rule is described in the [RFC2445](http://go.microsoft.com/fwlink/p/?LinkId=262221) Internet standard (Internet Calendaring and Scheduling Core Object Specification).</span></span>  
  
 <span data-ttu-id="a30f4-121">You can specify how frequently you want to repeat the recurrence rule by using an INTERVAL part of the rule.</span><span class="sxs-lookup"><span data-stu-id="a30f4-121">You can specify how frequently you want to repeat the recurrence rule by using an INTERVAL part of the rule.</span></span> <span data-ttu-id="a30f4-122">For example, to execute a job every three days, use the following format: "FREQ=DAILY;INTERVAL=3;".</span><span class="sxs-lookup"><span data-stu-id="a30f4-122">For example, to execute a job every three days, use the following format: "FREQ=DAILY;INTERVAL=3;".</span></span> <span data-ttu-id="a30f4-123">The INTERVAL is an optional part of the recurrence rule.</span><span class="sxs-lookup"><span data-stu-id="a30f4-123">The INTERVAL is an optional part of the recurrence rule.</span></span> <span data-ttu-id="a30f4-124">If you do not specify INTERVAL, it is set to 1.</span><span class="sxs-lookup"><span data-stu-id="a30f4-124">If you do not specify INTERVAL, it is set to 1.</span></span>  
  
 <span data-ttu-id="a30f4-125">To run an asynchronous job without recurrence, set this property to a value that is specified in the `AsyncOperation.RecurrencePattern` property programming reference topic for a particular message request class or an entity.</span><span class="sxs-lookup"><span data-stu-id="a30f4-125">To run an asynchronous job without recurrence, set this property to a value that is specified in the `AsyncOperation.RecurrencePattern` property programming reference topic for a particular message request class or an entity.</span></span>  
  
 <span data-ttu-id="a30f4-126">To specify the start time of the job execution, use the `AsyncOperation.RecurrenceStartTime` property or the <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest.StartDateTime> property in the message request classes or in the records that represent asynchronous operations.</span><span class="sxs-lookup"><span data-stu-id="a30f4-126">To specify the start time of the job execution, use the `AsyncOperation.RecurrenceStartTime` property or the <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest.StartDateTime> property in the message request classes or in the records that represent asynchronous operations.</span></span> <span data-ttu-id="a30f4-127">If the property is not set, the start time is set to the value that is contained in the `DateTime.Now` property.</span><span class="sxs-lookup"><span data-stu-id="a30f4-127">If the property is not set, the start time is set to the value that is contained in the `DateTime.Now` property.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a30f4-128">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a30f4-128">See also</span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest.RecurrencePattern>   
 <xref:Microsoft.Crm.Sdk.Messages.BulkDeleteRequest.StartDateTime>   
 <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest.RecurrencePattern>   
 <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest.RecurrenceStartTime>   
 <span data-ttu-id="a30f4-129">[Delete Data in Bulk in Dynamics 365 for Customer Engagement apps](delete-data-bulk.md) </span><span class="sxs-lookup"><span data-stu-id="a30f4-129">[Delete Data in Bulk in Dynamics 365 for Customer Engagement apps](delete-data-bulk.md) </span></span>  
 <span data-ttu-id="a30f4-130">[Asynchronous Operation (system job) Entity](asyncoperation-system-job-entity.md) </span><span class="sxs-lookup"><span data-stu-id="a30f4-130">[Asynchronous Operation (system job) Entity](asyncoperation-system-job-entity.md) </span></span>  
 <span data-ttu-id="a30f4-131">[Asynchronous Service in Dynamics 365 for Customer Engagement apps](asynchronous-service.md) </span><span class="sxs-lookup"><span data-stu-id="a30f4-131">[Asynchronous Service in Dynamics 365 for Customer Engagement apps](asynchronous-service.md) </span></span>  
 [<span data-ttu-id="a30f4-132">Supported entities for asynchronous operations</span><span class="sxs-lookup"><span data-stu-id="a30f4-132">Supported entities for asynchronous operations</span></span>](supported-entities-asynchronous-operations.md)
