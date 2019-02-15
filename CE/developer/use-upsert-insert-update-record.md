---
title: Use Upsert to insert or update a record (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: UpsertRequest(Update or Insert) message helps you simplify various data integration scenarios where you do not know if a record already exists in Dynamics 365 for Customer Engagement apps. In such cases you won’t know if you should call an UpdateRequest or a CreateRequest operation. This results in your querying for the record first to determine if it exists before performing the appropriate operation. UpsertRequest message helps you solve that issue
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: bfa82c05-13d3-488b-a094-4097d2aafa2f
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c5b854d605be07129634c67335da80f5b5aec78b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385666"
---
# <a name="use-upsert-to-insert-or-update-a-record"></a><span data-ttu-id="384c9-106">Use Upsert to insert or update a record</span><span class="sxs-lookup"><span data-stu-id="384c9-106">Use Upsert to insert or update a record</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="384c9-107">You can reduce the complexity involved with data integration scenarios by using the <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> message.</span><span class="sxs-lookup"><span data-stu-id="384c9-107">You can reduce the complexity involved with data integration scenarios by using the <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> message.</span></span> <span data-ttu-id="384c9-108">When loading data into [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement from an external system, for example in a bulk data integration scenario, you may not know if a record already exists in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="384c9-108">When loading data into [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement from an external system, for example in a bulk data integration scenario, you may not know if a record already exists in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="384c9-109">In such cases you won’t know if you should call an <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> or a <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> operation.</span><span class="sxs-lookup"><span data-stu-id="384c9-109">In such cases you won’t know if you should call an <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> or a <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> operation.</span></span> <span data-ttu-id="384c9-110">This results in your querying for the record first to determine if it exists before performing the appropriate operation.</span><span class="sxs-lookup"><span data-stu-id="384c9-110">This results in your querying for the record first to determine if it exists before performing the appropriate operation.</span></span> <span data-ttu-id="384c9-111">You can now reduce this complexity and load data into [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] more efficiently by using the new <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> (Update or Insert) message.</span><span class="sxs-lookup"><span data-stu-id="384c9-111">You can now reduce this complexity and load data into [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] more efficiently by using the new <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> (Update or Insert) message.</span></span>  
  
<a name="BKMK_UsingUpsert"></a>   
## <a name="using-upsert"></a><span data-ttu-id="384c9-112">Using Upsert</span><span class="sxs-lookup"><span data-stu-id="384c9-112">Using Upsert</span></span>  
 <span data-ttu-id="384c9-113">It is best to use <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> only when you aren’t sure if the record exists.</span><span class="sxs-lookup"><span data-stu-id="384c9-113">It is best to use <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> only when you aren’t sure if the record exists.</span></span> <span data-ttu-id="384c9-114">That is, when you aren’t sure if you should call a <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> or an <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> operation.</span><span class="sxs-lookup"><span data-stu-id="384c9-114">That is, when you aren’t sure if you should call a <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> or an <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> operation.</span></span> <span data-ttu-id="384c9-115">There is a performance decrease in using <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> versus using <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest>.</span><span class="sxs-lookup"><span data-stu-id="384c9-115">There is a performance decrease in using <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> versus using <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest>.</span></span> <span data-ttu-id="384c9-116">If you are sure the record doesn’t exist, use <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest>.</span><span class="sxs-lookup"><span data-stu-id="384c9-116">If you are sure the record doesn’t exist, use <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest>.</span></span>  
  
 <span data-ttu-id="384c9-117">The <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> includes a property named <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest.Target>.</span><span class="sxs-lookup"><span data-stu-id="384c9-117">The <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> includes a property named <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest.Target>.</span></span> <span data-ttu-id="384c9-118">This property contains the entity definition that will be used in an <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> or a <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> operation.</span><span class="sxs-lookup"><span data-stu-id="384c9-118">This property contains the entity definition that will be used in an <xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> or a <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> operation.</span></span> <span data-ttu-id="384c9-119">It also includes all the attributes required by the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> for the target entity type so that the record can be created if it doesn’t exist.</span><span class="sxs-lookup"><span data-stu-id="384c9-119">It also includes all the attributes required by the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> for the target entity type so that the record can be created if it doesn’t exist.</span></span>  
  
 <span data-ttu-id="384c9-120">You can inspect <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.RecordCreated> to determine if the record was created.</span><span class="sxs-lookup"><span data-stu-id="384c9-120">You can inspect <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.RecordCreated> to determine if the record was created.</span></span> <span data-ttu-id="384c9-121"><xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.RecordCreated> will be true if the record didn’t exist and was created.</span><span class="sxs-lookup"><span data-stu-id="384c9-121"><xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.RecordCreated> will be true if the record didn’t exist and was created.</span></span> <span data-ttu-id="384c9-122">It will be false if the record already existed and was updated.</span><span class="sxs-lookup"><span data-stu-id="384c9-122">It will be false if the record already existed and was updated.</span></span> <span data-ttu-id="384c9-123"><xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.Target> will be an `EntityReference` to the record that was found to exist or to the record that was created.</span><span class="sxs-lookup"><span data-stu-id="384c9-123"><xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.Target> will be an `EntityReference` to the record that was found to exist or to the record that was created.</span></span>  
  
 <span data-ttu-id="384c9-124">To understand how <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> works, see the following section.</span><span class="sxs-lookup"><span data-stu-id="384c9-124">To understand how <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> works, see the following section.</span></span>  
  
<a name="BKMK_upsert"></a>   
## <a name="understanding-the-upsert-process"></a><span data-ttu-id="384c9-125">Understanding the Upsert process</span><span class="sxs-lookup"><span data-stu-id="384c9-125">Understanding the Upsert process</span></span>  
 <span data-ttu-id="384c9-126">The following steps describe the processing logic when an <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> is received:</span><span class="sxs-lookup"><span data-stu-id="384c9-126">The following steps describe the processing logic when an <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> is received:</span></span>  
  
1. <span data-ttu-id="384c9-127">Send <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> with enough data for a create or insert operation.</span><span class="sxs-lookup"><span data-stu-id="384c9-127">Send <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> with enough data for a create or insert operation.</span></span>  
  
2. [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="384c9-128">will look up the record targeted by the target entity.</span><span class="sxs-lookup"><span data-stu-id="384c9-128">will look up the record targeted by the target entity.</span></span>  
  
3. <span data-ttu-id="384c9-129">If the record exists:</span><span class="sxs-lookup"><span data-stu-id="384c9-129">If the record exists:</span></span>  
  
   1.  <span data-ttu-id="384c9-130">Set the ID property of the target entity with the ID of the found record.</span><span class="sxs-lookup"><span data-stu-id="384c9-130">Set the ID property of the target entity with the ID of the found record.</span></span>  
  
   2.  <span data-ttu-id="384c9-131">Call Update.</span><span class="sxs-lookup"><span data-stu-id="384c9-131">Call Update.</span></span>  
  
   3.  <span data-ttu-id="384c9-132">Set the <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.RecordCreated> to `false`.</span><span class="sxs-lookup"><span data-stu-id="384c9-132">Set the <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.RecordCreated> to `false`.</span></span>  
  
   4.  <span data-ttu-id="384c9-133">Create an <xref:Microsoft.Xrm.Sdk.EntityReference> from the target entity of the update as the value for <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.Target>.</span><span class="sxs-lookup"><span data-stu-id="384c9-133">Create an <xref:Microsoft.Xrm.Sdk.EntityReference> from the target entity of the update as the value for <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.Target>.</span></span>  
  
   5.  <span data-ttu-id="384c9-134">Return the <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse>.</span><span class="sxs-lookup"><span data-stu-id="384c9-134">Return the <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse>.</span></span>  
  
4. <span data-ttu-id="384c9-135">If the record doesn’t exist:</span><span class="sxs-lookup"><span data-stu-id="384c9-135">If the record doesn’t exist:</span></span>  
  
   1.  <span data-ttu-id="384c9-136">Copy any alternate key values into the target entity attributes.</span><span class="sxs-lookup"><span data-stu-id="384c9-136">Copy any alternate key values into the target entity attributes.</span></span>  
  
   2.  <span data-ttu-id="384c9-137">Call `Create`.</span><span class="sxs-lookup"><span data-stu-id="384c9-137">Call `Create`.</span></span>  
  
   3.  <span data-ttu-id="384c9-138">Set the <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.RecordCreated> to `true`.</span><span class="sxs-lookup"><span data-stu-id="384c9-138">Set the <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.RecordCreated> to `true`.</span></span>  
  
   4.  <span data-ttu-id="384c9-139">Create an <xref:Microsoft.Xrm.Sdk.EntityReference> from the target entity type and the ID result of the `Create` request as the value for <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.Target>.</span><span class="sxs-lookup"><span data-stu-id="384c9-139">Create an <xref:Microsoft.Xrm.Sdk.EntityReference> from the target entity type and the ID result of the `Create` request as the value for <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse.Target>.</span></span>  
  
   5.  <span data-ttu-id="384c9-140">Return the <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse>.</span><span class="sxs-lookup"><span data-stu-id="384c9-140">Return the <xref:Microsoft.Xrm.Sdk.Messages.UpsertResponse>.</span></span>  
  
   <span data-ttu-id="384c9-141">The following illustration shows the process that unfolds when an <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> is received.</span><span class="sxs-lookup"><span data-stu-id="384c9-141">The following illustration shows the process that unfolds when an <xref:Microsoft.Xrm.Sdk.Messages.UpsertRequest> is received.</span></span>  
  
   <span data-ttu-id="384c9-142">![upsert process flow](media/upsert-flowchart-dynamics-crm-2015.png "upsert process flow")</span><span class="sxs-lookup"><span data-stu-id="384c9-142">![upsert process flow](media/upsert-flowchart-dynamics-crm-2015.png "upsert process flow")</span></span>  
  
<a name="BKMK_SampleCode"></a>   
## <a name="sample-code"></a><span data-ttu-id="384c9-143">Mã mẫu</span><span class="sxs-lookup"><span data-stu-id="384c9-143">Sample code</span></span>  
 <span data-ttu-id="384c9-144">The [Insert or update a record using Upsert](http://go.microsoft.com/fwlink/p/?LinkId=532924) sample [ProductUpsertSample.cs](https://code.msdn.microsoft.com/Insert-or-update-a-record-aa160870/sourcecode?fileId=136218&pathId=1243320355) file contains the following `ProcessUpsert` method to apply the `UpsertRequest` message on the contents of an XML file to create new records or update existing ones.</span><span class="sxs-lookup"><span data-stu-id="384c9-144">The [Insert or update a record using Upsert](http://go.microsoft.com/fwlink/p/?LinkId=532924) sample [ProductUpsertSample.cs](https://code.msdn.microsoft.com/Insert-or-update-a-record-aa160870/sourcecode?fileId=136218&pathId=1243320355) file contains the following `ProcessUpsert` method to apply the `UpsertRequest` message on the contents of an XML file to create new records or update existing ones.</span></span>  
  
 [!code-csharp[UpsertSample#ProductUpsertSample1](../snippets/csharp/CRMV8/upsertsample/cs/productupsertsample1.cs#productupsertsample1)]  
  
### <a name="see-also"></a><span data-ttu-id="384c9-145">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="384c9-145">See also</span></span>  
 <span data-ttu-id="384c9-146">[Use change tracking to synchronize data with external systems](use-change-tracking-synchronize-data-external-systems.md) </span><span class="sxs-lookup"><span data-stu-id="384c9-146">[Use change tracking to synchronize data with external systems](use-change-tracking-synchronize-data-external-systems.md) </span></span>  
 <span data-ttu-id="384c9-147">[Define alternate keys for an entity](define-alternate-keys-entity.md) </span><span class="sxs-lookup"><span data-stu-id="384c9-147">[Define alternate keys for an entity](define-alternate-keys-entity.md) </span></span>  
 [<span data-ttu-id="384c9-148">Using alternate keys</span><span class="sxs-lookup"><span data-stu-id="384c9-148">Using alternate keys</span></span>](use-alternate-key-create-record.md)
