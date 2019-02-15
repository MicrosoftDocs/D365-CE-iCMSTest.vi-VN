---
title: Queue entities (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Queues help in organizing, prioritizing, and monitoring the progress of your work while you are using Dynamics 365 for Customer Engagement. Customizable entites can be enabled for queues, and queues are categorized into public or private queues.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- queues and queue items, inheritance
- security, queue
- queues, about and benefits of
- queues and queue items, definitions
- managing work, queue entities
- queue-enabled entities, list of default entities
- queues, security
- enabling entities for queues
- queues and queue items, actions on
- limiting access to queues
- queues, using to managing work
ms.assetid: a60160f0-6de8-4aed-af92-cb180e883c82
caps.latest.revision: 55
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3a74d8ee615b614bd1ffc5ff9dd2f93ebab36cb8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386814"
---
# <a name="queue-entities"></a><span data-ttu-id="56ed7-104">Queue entities</span><span class="sxs-lookup"><span data-stu-id="56ed7-104">Queue entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="56ed7-105">*Queues* are instrumental in organizing, prioritizing, and monitoring the progress of your work while you are using [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="56ed7-105">*Queues* are instrumental in organizing, prioritizing, and monitoring the progress of your work while you are using [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> <span data-ttu-id="56ed7-106">As a central location for work management, queues assist you in processing cases, responding to service calls, or sending out product information to prospective customers.</span><span class="sxs-lookup"><span data-stu-id="56ed7-106">As a central location for work management, queues assist you in processing cases, responding to service calls, or sending out product information to prospective customers.</span></span> <span data-ttu-id="56ed7-107">Programmatically, a queue is a collection of queue items.</span><span class="sxs-lookup"><span data-stu-id="56ed7-107">Programmatically, a queue is a collection of queue items.</span></span> <span data-ttu-id="56ed7-108">A queue item serves as a container for an entity record, such as a task, an email, or a case that needs processing.</span><span class="sxs-lookup"><span data-stu-id="56ed7-108">A queue item serves as a container for an entity record, such as a task, an email, or a case that needs processing.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="56ed7-109">The capabilities of queues was enhanced in [!INCLUDE[pn_crm_2013_sp](../includes/pn-crm-2013-sp.md)] (on-premises) and [!INCLUDE[pn_v6_online_ur1_shortest](../includes/pn-v6-online-ur1-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="56ed7-109">The capabilities of queues was enhanced in [!INCLUDE[pn_crm_2013_sp](../includes/pn-crm-2013-sp.md)] (on-premises) and [!INCLUDE[pn_v6_online_ur1_shortest](../includes/pn-v6-online-ur1-shortest.md)].</span></span> <span data-ttu-id="56ed7-110">For details about what was added from earlier versions, see the [Dynamics CRM 2013 version of this topic](https://msdn.microsoft.com/library/gg328459\(v=crm.7\).aspx).</span><span class="sxs-lookup"><span data-stu-id="56ed7-110">For details about what was added from earlier versions, see the [Dynamics CRM 2013 version of this topic](https://msdn.microsoft.com/library/gg328459\(v=crm.7\).aspx).</span></span>  
  
 <span data-ttu-id="56ed7-111">The following information pertains to queues:</span><span class="sxs-lookup"><span data-stu-id="56ed7-111">The following information pertains to queues:</span></span>  
  
-   <span data-ttu-id="56ed7-112">All customizable entities can be enabled for queues.</span><span class="sxs-lookup"><span data-stu-id="56ed7-112">All customizable entities can be enabled for queues.</span></span>  
  
-   <span data-ttu-id="56ed7-113">Queues may be public or private.</span><span class="sxs-lookup"><span data-stu-id="56ed7-113">Queues may be public or private.</span></span> <span data-ttu-id="56ed7-114">Private queue items are only visible to the members of the queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-114">Private queue items are only visible to the members of the queue.</span></span>  
  
-   <span data-ttu-id="56ed7-115">A private queue is automatically created for each new user or team.</span><span class="sxs-lookup"><span data-stu-id="56ed7-115">A private queue is automatically created for each new user or team.</span></span>  
  
-   <span data-ttu-id="56ed7-116">A queue can contain multiple entity types, such as tasks, emails, or cases.</span><span class="sxs-lookup"><span data-stu-id="56ed7-116">A queue can contain multiple entity types, such as tasks, emails, or cases.</span></span>  
  
-   <span data-ttu-id="56ed7-117">A queue contains information about the user who is working on a particular queue item.</span><span class="sxs-lookup"><span data-stu-id="56ed7-117">A queue contains information about the user who is working on a particular queue item.</span></span> <span data-ttu-id="56ed7-118">This helps you manage your resources more efficiently and helps to prevent duplication of work.</span><span class="sxs-lookup"><span data-stu-id="56ed7-118">This helps you manage your resources more efficiently and helps to prevent duplication of work.</span></span>  
  
-   <span data-ttu-id="56ed7-119">Queues can be enabled for workflows and audit.</span><span class="sxs-lookup"><span data-stu-id="56ed7-119">Queues can be enabled for workflows and audit.</span></span> <span data-ttu-id="56ed7-120">This helps improve productivity and track the entity and attribute data changes for future analysis and reporting.</span><span class="sxs-lookup"><span data-stu-id="56ed7-120">This helps improve productivity and track the entity and attribute data changes for future analysis and reporting.</span></span>  
  
<a name="BKMK_MemberCapabilities"></a>   
## <a name="members-capabilities"></a><span data-ttu-id="56ed7-121">Members capabilities</span><span class="sxs-lookup"><span data-stu-id="56ed7-121">Members capabilities</span></span>  
 <span data-ttu-id="56ed7-122">Queues are categorized into public or private queues.</span><span class="sxs-lookup"><span data-stu-id="56ed7-122">Queues are categorized into public or private queues.</span></span> <span data-ttu-id="56ed7-123">Private queues have individual users as members to make controlling access to queues easier.</span><span class="sxs-lookup"><span data-stu-id="56ed7-123">Private queues have individual users as members to make controlling access to queues easier.</span></span> <span data-ttu-id="56ed7-124">If you add a team to a private queue, all the members of that team become members of the private queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-124">If you add a team to a private queue, all the members of that team become members of the private queue.</span></span>  
  
<a name="BKMK_publicAndPrivateQueues"></a>   
## <a name="public-and-private-queues"></a><span data-ttu-id="56ed7-125">Public and private queues</span><span class="sxs-lookup"><span data-stu-id="56ed7-125">Public and private queues</span></span>  
 <span data-ttu-id="56ed7-126">The `QueueViewType` attribute is a picklist that defines whether a queue is public or private.</span><span class="sxs-lookup"><span data-stu-id="56ed7-126">The `QueueViewType` attribute is a picklist that defines whether a queue is public or private.</span></span>  
  
-   <span data-ttu-id="56ed7-127">All user queues are private queues for the user: Only the user will be able to see queue items in their private queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-127">All user queues are private queues for the user: Only the user will be able to see queue items in their private queue.</span></span>  
  
-   <span data-ttu-id="56ed7-128">Team queues are marked as private with members: the team owner and all team members will be able to see the queue in the application.</span><span class="sxs-lookup"><span data-stu-id="56ed7-128">Team queues are marked as private with members: the team owner and all team members will be able to see the queue in the application.</span></span>  
  
-   <span data-ttu-id="56ed7-129">All other queues are public.</span><span class="sxs-lookup"><span data-stu-id="56ed7-129">All other queues are public.</span></span> <span data-ttu-id="56ed7-130">Everyone with read privileges for the queue entity will be able to see these queues.</span><span class="sxs-lookup"><span data-stu-id="56ed7-130">Everyone with read privileges for the queue entity will be able to see these queues.</span></span>  
  
<a name="BKMK_QueueAttributes"></a>   
## <a name="attributes-used-to-manage-queues"></a><span data-ttu-id="56ed7-131">Attributes used to manage queues</span><span class="sxs-lookup"><span data-stu-id="56ed7-131">Attributes used to manage queues</span></span>  
 <span data-ttu-id="56ed7-132">Use the following attributes to manage queues.</span><span class="sxs-lookup"><span data-stu-id="56ed7-132">Use the following attributes to manage queues.</span></span>  
  
|<span data-ttu-id="56ed7-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="56ed7-133">SchemaName</span></span>|<span data-ttu-id="56ed7-134">DisplayName</span><span class="sxs-lookup"><span data-stu-id="56ed7-134">DisplayName</span></span>|<span data-ttu-id="56ed7-135">Loại</span><span class="sxs-lookup"><span data-stu-id="56ed7-135">Type</span></span>|<span data-ttu-id="56ed7-136">Mô tả</span><span class="sxs-lookup"><span data-stu-id="56ed7-136">Description</span></span>|  
|----------------|-----------------|----------|-----------------|  
|<span data-ttu-id="56ed7-137">NumberOfItems</span><span class="sxs-lookup"><span data-stu-id="56ed7-137">NumberOfItems</span></span>|<span data-ttu-id="56ed7-138">Queue Items</span><span class="sxs-lookup"><span data-stu-id="56ed7-138">Queue Items</span></span>|<span data-ttu-id="56ed7-139">Số nguyên</span><span class="sxs-lookup"><span data-stu-id="56ed7-139">Integer</span></span>|<span data-ttu-id="56ed7-140">Number of Queue items associated with the queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-140">Number of Queue items associated with the queue.</span></span>|  
|<span data-ttu-id="56ed7-141">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="56ed7-141">NumberOfMembers</span></span>|<span data-ttu-id="56ed7-142">Không.</span><span class="sxs-lookup"><span data-stu-id="56ed7-142">No.</span></span> <span data-ttu-id="56ed7-143">of Members</span><span class="sxs-lookup"><span data-stu-id="56ed7-143">of Members</span></span>|<span data-ttu-id="56ed7-144">Số nguyên</span><span class="sxs-lookup"><span data-stu-id="56ed7-144">Integer</span></span>|<span data-ttu-id="56ed7-145">Number of Members associated with the queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-145">Number of Members associated with the queue.</span></span>|  
|<span data-ttu-id="56ed7-146">QueueViewType</span><span class="sxs-lookup"><span data-stu-id="56ed7-146">QueueViewType</span></span>|<span data-ttu-id="56ed7-147">Loại</span><span class="sxs-lookup"><span data-stu-id="56ed7-147">Type</span></span>|<span data-ttu-id="56ed7-148">Danh sách chọn</span><span class="sxs-lookup"><span data-stu-id="56ed7-148">Picklist</span></span>|<span data-ttu-id="56ed7-149">Select whether the queue is public or private.</span><span class="sxs-lookup"><span data-stu-id="56ed7-149">Select whether the queue is public or private.</span></span> <span data-ttu-id="56ed7-150">A public queue can be viewed by all.</span><span class="sxs-lookup"><span data-stu-id="56ed7-150">A public queue can be viewed by all.</span></span> <span data-ttu-id="56ed7-151">A private queue can be viewed only by the members added to the queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-151">A private queue can be viewed only by the members added to the queue.</span></span>|  
  
<a name="BKMK_deletingQueues"></a>   
## <a name="restrictions-on-deleting-queues"></a><span data-ttu-id="56ed7-152">Restrictions on deleting queues</span><span class="sxs-lookup"><span data-stu-id="56ed7-152">Restrictions on deleting queues</span></span>  
 <span data-ttu-id="56ed7-153">A queue cannot be deleted if the following are true:</span><span class="sxs-lookup"><span data-stu-id="56ed7-153">A queue cannot be deleted if the following are true:</span></span>  
  
-   <span data-ttu-id="56ed7-154">When the queue has queue items.</span><span class="sxs-lookup"><span data-stu-id="56ed7-154">When the queue has queue items.</span></span>  
  
-   <span data-ttu-id="56ed7-155">When any routing rule uses the queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-155">When any routing rule uses the queue.</span></span>  
  
<a name="BKMK_Enabling"></a>   
## <a name="enable-entities-for-queues"></a><span data-ttu-id="56ed7-156">Enable entities for queues</span><span class="sxs-lookup"><span data-stu-id="56ed7-156">Enable entities for queues</span></span>  
 <span data-ttu-id="56ed7-157">To enable a customizable entity, business or custom, for queues, use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> message to set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsValidForQueue> attribute to `true`.</span><span class="sxs-lookup"><span data-stu-id="56ed7-157">To enable a customizable entity, business or custom, for queues, use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> message to set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsValidForQueue> attribute to `true`.</span></span> <span data-ttu-id="56ed7-158">For a list of customizable entities, see [Which Entities are Customizable?](which-entities-are-customizable.md).</span><span class="sxs-lookup"><span data-stu-id="56ed7-158">For a list of customizable entities, see [Which Entities are Customizable?](which-entities-are-customizable.md).</span></span> <span data-ttu-id="56ed7-159">The queue entity and the queue item entity are customizable entities, but they cannot be enabled for queues.</span><span class="sxs-lookup"><span data-stu-id="56ed7-159">The queue entity and the queue item entity are customizable entities, but they cannot be enabled for queues.</span></span>  
  
 <span data-ttu-id="56ed7-160">The following list contains default queue-enabled entities in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]:</span><span class="sxs-lookup"><span data-stu-id="56ed7-160">The following list contains default queue-enabled entities in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]:</span></span>  
  
-   <span data-ttu-id="56ed7-161">Cuộc hẹn</span><span class="sxs-lookup"><span data-stu-id="56ed7-161">Appointment</span></span>  
  
-   <span data-ttu-id="56ed7-162">Campaignactivity</span><span class="sxs-lookup"><span data-stu-id="56ed7-162">Campaignactivity</span></span>  
  
-   <span data-ttu-id="56ed7-163">CampaignResponse</span><span class="sxs-lookup"><span data-stu-id="56ed7-163">CampaignResponse</span></span>  
  
-   <span data-ttu-id="56ed7-164">Email</span><span class="sxs-lookup"><span data-stu-id="56ed7-164">Email</span></span>  
  
-   <span data-ttu-id="56ed7-165">Fax</span><span class="sxs-lookup"><span data-stu-id="56ed7-165">Fax</span></span>  
  
-   <span data-ttu-id="56ed7-166">Sự cố</span><span class="sxs-lookup"><span data-stu-id="56ed7-166">Incident</span></span>  
  
-   <span data-ttu-id="56ed7-167">Thư tín</span><span class="sxs-lookup"><span data-stu-id="56ed7-167">Letter</span></span>  
  
-   <span data-ttu-id="56ed7-168">Cuộc gọi Điện thoại </span><span class="sxs-lookup"><span data-stu-id="56ed7-168">PhoneCall</span></span>  
  
-   <span data-ttu-id="56ed7-169">RecurringAppointmentMaster</span><span class="sxs-lookup"><span data-stu-id="56ed7-169">RecurringAppointmentMaster</span></span>  
  
-   <span data-ttu-id="56ed7-170">ServiceAppointment</span><span class="sxs-lookup"><span data-stu-id="56ed7-170">ServiceAppointment</span></span>  
  
-   <span data-ttu-id="56ed7-171">SocialActivity</span><span class="sxs-lookup"><span data-stu-id="56ed7-171">SocialActivity</span></span>  
  
-   <span data-ttu-id="56ed7-172">Nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="56ed7-172">Task</span></span>  
  
<a name="BKMK_Inheriting"></a>   
## <a name="inherit-privileges-and-provide-limited-access-to-a-queue"></a><span data-ttu-id="56ed7-173">Inherit privileges and provide limited access to a queue</span><span class="sxs-lookup"><span data-stu-id="56ed7-173">Inherit privileges and provide limited access to a queue</span></span>  
 <span data-ttu-id="56ed7-174">A queue and a queue item have a parental relationship in which operations on the parent queue record are propagated to the child queue item records.</span><span class="sxs-lookup"><span data-stu-id="56ed7-174">A queue and a queue item have a parental relationship in which operations on the parent queue record are propagated to the child queue item records.</span></span> <span data-ttu-id="56ed7-175">For more information about parental relationships and cascading rules, see [Entity Relationship Behavior](entity-relationship-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="56ed7-175">For more information about parental relationships and cascading rules, see [Entity Relationship Behavior](entity-relationship-behavior.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="56ed7-176">In this particular parental relationship, only the Delete action is cascaded from the parent queue entity to the child queue item entity.</span><span class="sxs-lookup"><span data-stu-id="56ed7-176">In this particular parental relationship, only the Delete action is cascaded from the parent queue entity to the child queue item entity.</span></span> <span data-ttu-id="56ed7-177">Other actions, such as Assign, Merge or Share are not cascaded.</span><span class="sxs-lookup"><span data-stu-id="56ed7-177">Other actions, such as Assign, Merge or Share are not cascaded.</span></span>  
  
 <span data-ttu-id="56ed7-178">The privileges on a queue item are inherited from the privileges on a queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-178">The privileges on a queue item are inherited from the privileges on a queue.</span></span>  
  
- <span data-ttu-id="56ed7-179">If you have `prvReadQueue` privilege, you also have read privilege on a queue item entity.</span><span class="sxs-lookup"><span data-stu-id="56ed7-179">If you have `prvReadQueue` privilege, you also have read privilege on a queue item entity.</span></span>  
  
- <span data-ttu-id="56ed7-180">If you have `prvAppendToQueue` privilege, you also have create, update, and delete privileges on a queue item entity.</span><span class="sxs-lookup"><span data-stu-id="56ed7-180">If you have `prvAppendToQueue` privilege, you also have create, update, and delete privileges on a queue item entity.</span></span>  
  
  <span data-ttu-id="56ed7-181">Often, you must limit access to the queue when permitting access to the queue items.</span><span class="sxs-lookup"><span data-stu-id="56ed7-181">Often, you must limit access to the queue when permitting access to the queue items.</span></span> <span data-ttu-id="56ed7-182">As a queue owner with full access to the queue, you might want to share a queue with a team that will have only limited access to the queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-182">As a queue owner with full access to the queue, you might want to share a queue with a team that will have only limited access to the queue.</span></span> <span data-ttu-id="56ed7-183">For example, if the support team is given read and append to privileges on a queue, team members cannot make any changes to the queue, such as changing queue name or queue owner.</span><span class="sxs-lookup"><span data-stu-id="56ed7-183">For example, if the support team is given read and append to privileges on a queue, team members cannot make any changes to the queue, such as changing queue name or queue owner.</span></span> <span data-ttu-id="56ed7-184">However, they can create, retrieve, update, and delete queue items.</span><span class="sxs-lookup"><span data-stu-id="56ed7-184">However, they can create, retrieve, update, and delete queue items.</span></span>  
  
<a name="BKMK_Actions"></a>   
## <a name="actions-on-queues-and-queue-items"></a><span data-ttu-id="56ed7-185">Actions on queues and queue items</span><span class="sxs-lookup"><span data-stu-id="56ed7-185">Actions on queues and queue items</span></span>  
 <span data-ttu-id="56ed7-186">You can perform a variety of actions on queues and queue items, if you have appropriate privileges on the queue entity and the queue item entity.</span><span class="sxs-lookup"><span data-stu-id="56ed7-186">You can perform a variety of actions on queues and queue items, if you have appropriate privileges on the queue entity and the queue item entity.</span></span>  
  
### <a name="actions-on-queues"></a><span data-ttu-id="56ed7-187">Actions on queues</span><span class="sxs-lookup"><span data-stu-id="56ed7-187">Actions on queues</span></span>  
 <span data-ttu-id="56ed7-188">Perform the following actions on the queues:</span><span class="sxs-lookup"><span data-stu-id="56ed7-188">Perform the following actions on the queues:</span></span>  
  
-   <span data-ttu-id="56ed7-189">Customize queues and queue items by adding custom attributes.</span><span class="sxs-lookup"><span data-stu-id="56ed7-189">Customize queues and queue items by adding custom attributes.</span></span>  
  
-   <span data-ttu-id="56ed7-190">Add an entity record to a queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-190">Add an entity record to a queue.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="56ed7-191">An entity record cannot be added in multiple queues.</span><span class="sxs-lookup"><span data-stu-id="56ed7-191">An entity record cannot be added in multiple queues.</span></span> <span data-ttu-id="56ed7-192">An exception is an email entity record with the status “Received”.</span><span class="sxs-lookup"><span data-stu-id="56ed7-192">An exception is an email entity record with the status “Received”.</span></span>  
  
-   <span data-ttu-id="56ed7-193">Add entity records of different entity types in the same queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-193">Add entity records of different entity types in the same queue.</span></span>  
  
-   <span data-ttu-id="56ed7-194">Change an ownership of a queue by assigning it to another user or team.</span><span class="sxs-lookup"><span data-stu-id="56ed7-194">Change an ownership of a queue by assigning it to another user or team.</span></span>  
  
-   <span data-ttu-id="56ed7-195">Add principals to a private queue using the <xref:Microsoft.Crm.Sdk.Messages.AddPrincipalToQueueRequest>.</span><span class="sxs-lookup"><span data-stu-id="56ed7-195">Add principals to a private queue using the <xref:Microsoft.Crm.Sdk.Messages.AddPrincipalToQueueRequest>.</span></span>  
  
-   <span data-ttu-id="56ed7-196">Clean up the history for a queue by deleting inactive queue items in the queue, such as completed or canceled phone calls.</span><span class="sxs-lookup"><span data-stu-id="56ed7-196">Clean up the history for a queue by deleting inactive queue items in the queue, such as completed or canceled phone calls.</span></span>  
  
-   <span data-ttu-id="56ed7-197">Retrieve all the queues that a user has access to using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveUserQueuesRequest></span><span class="sxs-lookup"><span data-stu-id="56ed7-197">Retrieve all the queues that a user has access to using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveUserQueuesRequest></span></span>  
  
-   <span data-ttu-id="56ed7-198">Make a queue the default queue for a user by setting the `SystemUser.QueueId` attribute to the ID of the queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-198">Make a queue the default queue for a user by setting the `SystemUser.QueueId` attribute to the ID of the queue.</span></span> <span data-ttu-id="56ed7-199">The same queue can be specified as a default queue for different users.</span><span class="sxs-lookup"><span data-stu-id="56ed7-199">The same queue can be specified as a default queue for different users.</span></span>  
  
-   <span data-ttu-id="56ed7-200">Create a workflow that operates on all private queues.</span><span class="sxs-lookup"><span data-stu-id="56ed7-200">Create a workflow that operates on all private queues.</span></span> <span data-ttu-id="56ed7-201">For example, whenever a user creates a task, the workflow adds the task to the default queue of the user.</span><span class="sxs-lookup"><span data-stu-id="56ed7-201">For example, whenever a user creates a task, the workflow adds the task to the default queue of the user.</span></span> <span data-ttu-id="56ed7-202">You can also create a workflow that operates only on a particular queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-202">You can also create a workflow that operates only on a particular queue.</span></span>  
  
-   <span data-ttu-id="56ed7-203">Configure an email for incoming messages, if you want incoming email messages to be delivered to a queue.</span><span class="sxs-lookup"><span data-stu-id="56ed7-203">Configure an email for incoming messages, if you want incoming email messages to be delivered to a queue.</span></span>  
  
### <a name="actions-on-queue-items"></a><span data-ttu-id="56ed7-204">Actions on queue items</span><span class="sxs-lookup"><span data-stu-id="56ed7-204">Actions on queue items</span></span>  
 <span data-ttu-id="56ed7-205">Perform the following actions on the queue items:</span><span class="sxs-lookup"><span data-stu-id="56ed7-205">Perform the following actions on the queue items:</span></span>  
  
- <span data-ttu-id="56ed7-206">Assign a queue item to a user using the <xref:Microsoft.Crm.Sdk.Messages.PickFromQueueRequest>.</span><span class="sxs-lookup"><span data-stu-id="56ed7-206">Assign a queue item to a user using the <xref:Microsoft.Crm.Sdk.Messages.PickFromQueueRequest>.</span></span>  
  
- <span data-ttu-id="56ed7-207">Move a queue item from a source queue to a destination queue by using the <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest> message.</span><span class="sxs-lookup"><span data-stu-id="56ed7-207">Move a queue item from a source queue to a destination queue by using the <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest> message.</span></span> <span data-ttu-id="56ed7-208">A queue item can be moved from one queue to another until it is deactivated by using the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="56ed7-208">A queue item can be moved from one queue to another until it is deactivated by using the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message.</span></span>  
  
  > [!NOTE]
  >  <span data-ttu-id="56ed7-209">A queue item is automatically deactivated if the state of the record in the queue item changed from Active to Inactive.</span><span class="sxs-lookup"><span data-stu-id="56ed7-209">A queue item is automatically deactivated if the state of the record in the queue item changed from Active to Inactive.</span></span> <span data-ttu-id="56ed7-210">This applies to queue-enabled entities that have Active and Inactive states.</span><span class="sxs-lookup"><span data-stu-id="56ed7-210">This applies to queue-enabled entities that have Active and Inactive states.</span></span> <span data-ttu-id="56ed7-211">To determine if an entity is queue-enabled and if an entity record can be in an Active or Inactive state, see entity metadata information.</span><span class="sxs-lookup"><span data-stu-id="56ed7-211">To determine if an entity is queue-enabled and if an entity record can be in an Active or Inactive state, see entity metadata information.</span></span> [!INCLUDE[metadata_browser](../includes/metadata-browser.md)]  
  
- <span data-ttu-id="56ed7-212">Release a queue item back to the queue using the <xref:Microsoft.Crm.Sdk.Messages.ReleaseToQueueRequest>.</span><span class="sxs-lookup"><span data-stu-id="56ed7-212">Release a queue item back to the queue using the <xref:Microsoft.Crm.Sdk.Messages.ReleaseToQueueRequest>.</span></span>  
  
- <span data-ttu-id="56ed7-213">Delete a queue item from a queue by using the <xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> message.</span><span class="sxs-lookup"><span data-stu-id="56ed7-213">Delete a queue item from a queue by using the <xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> message.</span></span> <span data-ttu-id="56ed7-214">When you delete a queue item, a referenced entity record is not deleted.</span><span class="sxs-lookup"><span data-stu-id="56ed7-214">When you delete a queue item, a referenced entity record is not deleted.</span></span> <span data-ttu-id="56ed7-215">However, when you delete an entity record, all queue items that reference this entity record are deleted.</span><span class="sxs-lookup"><span data-stu-id="56ed7-215">However, when you delete an entity record, all queue items that reference this entity record are deleted.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="56ed7-216">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="56ed7-216">See also</span></span>  
 <span data-ttu-id="56ed7-217">[Configure EMail for Incoming Messages](configure-email-incoming-messages.md) </span><span class="sxs-lookup"><span data-stu-id="56ed7-217">[Configure EMail for Incoming Messages](configure-email-incoming-messages.md) </span></span>  
 <span data-ttu-id="56ed7-218">[Queue Entity](entities/queue.md) </span><span class="sxs-lookup"><span data-stu-id="56ed7-218">[Queue Entity](entities/queue.md) </span></span>  
 <span data-ttu-id="56ed7-219">[QueueItem Entity](entities/queueitem.md) </span><span class="sxs-lookup"><span data-stu-id="56ed7-219">[QueueItem Entity](entities/queueitem.md) </span></span>  
 <span data-ttu-id="56ed7-220">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span><span class="sxs-lookup"><span data-stu-id="56ed7-220">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest>   
 [<span data-ttu-id="56ed7-221">Business Management Entities</span><span class="sxs-lookup"><span data-stu-id="56ed7-221">Business Management Entities</span></span>](business-management-entities.md)
