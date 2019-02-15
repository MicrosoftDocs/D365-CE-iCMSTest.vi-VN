---
title: Use the Feedback entity to manage feedback and ratings for Dynamics 365 for Customer Engagement records (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the feedback eneity to obtain feedback and ratings for the records.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: c0d69f7b-5016-44e7-8b73-1f8c2de5b526
caps.latest.revision: 13
author: KumarVivek
ms.author: kvivek
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 560242cf4b518e8cc7199258aa3fdb86a137bd62
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386553"
---
# <a name="use-the-feedback-entity-to-manage-feedback-and-ratings-for-dynamics-365-for-customer-engagement-records"></a><span data-ttu-id="2f25f-103">Use the Feedback entity to manage feedback and ratings for Dynamics 365 for Customer Engagement records</span><span class="sxs-lookup"><span data-stu-id="2f25f-103">Use the Feedback entity to manage feedback and ratings for Dynamics 365 for Customer Engagement records</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2f25f-104">Improve your products and services by enabling users to provide feedback and ratings for entity records in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="2f25f-104">Improve your products and services by enabling users to provide feedback and ratings for entity records in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> <span data-ttu-id="2f25f-105">For example, you can enable feedbacks and ratings for the `Product` entity to know user's feedback on the products you sell, or on the `Incident` (case) entity to understand and improve the quality of your customer support team.</span><span class="sxs-lookup"><span data-stu-id="2f25f-105">For example, you can enable feedbacks and ratings for the `Product` entity to know user's feedback on the products you sell, or on the `Incident` (case) entity to understand and improve the quality of your customer support team.</span></span>  
  
 <span data-ttu-id="2f25f-106">You can enable feedback and rating for both system and custom entities in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="2f25f-106">You can enable feedback and rating for both system and custom entities in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="2f25f-107">By default, the `KnowledgeArticle` entity is enabled for feedback and ratings.</span><span class="sxs-lookup"><span data-stu-id="2f25f-107">By default, the `KnowledgeArticle` entity is enabled for feedback and ratings.</span></span> <span data-ttu-id="2f25f-108">Use the new `Feedback` entity to programmatically create and manage feedback for entity records.</span><span class="sxs-lookup"><span data-stu-id="2f25f-108">Use the new `Feedback` entity to programmatically create and manage feedback for entity records.</span></span>  
  
> [!NOTE]
> [!INCLUDE[cc_feature_included_with_update_8_1_0_admins](../includes/cc-feature-included-with-update-8-1-0-admins.md)]  
  
 <span data-ttu-id="2f25f-109">To programmatically enable feedback for a:</span><span class="sxs-lookup"><span data-stu-id="2f25f-109">To programmatically enable feedback for a:</span></span>  
  
- <span data-ttu-id="2f25f-110">System entity, use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> message to update the entity, and set the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest.HasFeedback> property to true.</span><span class="sxs-lookup"><span data-stu-id="2f25f-110">System entity, use the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> message to update the entity, and set the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest.HasFeedback> property to true.</span></span>  
  
- <span data-ttu-id="2f25f-111">Custom entity, set the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest>.<xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest.HasFeedback></span><span class="sxs-lookup"><span data-stu-id="2f25f-111">Custom entity, set the <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest>.<xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest.HasFeedback></span></span> <span data-ttu-id="2f25f-112">property to true  while creating the entity, or update existing custom entity to set the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest>.<xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest.HasFeedback></span><span class="sxs-lookup"><span data-stu-id="2f25f-112">property to true  while creating the entity, or update existing custom entity to set the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest>.<xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest.HasFeedback></span></span> <span data-ttu-id="2f25f-113">property to true.</span><span class="sxs-lookup"><span data-stu-id="2f25f-113">property to true.</span></span>  
  
  <span data-ttu-id="2f25f-114">Once you have enabled an entity for feedback and rating, you can't disable it.</span><span class="sxs-lookup"><span data-stu-id="2f25f-114">Once you have enabled an entity for feedback and rating, you can't disable it.</span></span> <span data-ttu-id="2f25f-115">After you enable an entity for feedback, a regarding relationship is created between the entity and the `Feedback` entity.</span><span class="sxs-lookup"><span data-stu-id="2f25f-115">After you enable an entity for feedback, a regarding relationship is created between the entity and the `Feedback` entity.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2f25f-116">You can also use the customization tools in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] to enable feedback and rating for system and custom entities.</span><span class="sxs-lookup"><span data-stu-id="2f25f-116">You can also use the customization tools in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] to enable feedback and rating for system and custom entities.</span></span> <span data-ttu-id="2f25f-117">More information: [Enable an entity for feedback](http://go.microsoft.com/fwlink/p/?LinkId=785436)</span><span class="sxs-lookup"><span data-stu-id="2f25f-117">More information: [Enable an entity for feedback](http://go.microsoft.com/fwlink/p/?LinkId=785436)</span></span>  
  
 <span data-ttu-id="2f25f-118">The `Feedback` entity stores the following information :</span><span class="sxs-lookup"><span data-stu-id="2f25f-118">The `Feedback` entity stores the following information :</span></span>  
  
- <span data-ttu-id="2f25f-119">Feedback title</span><span class="sxs-lookup"><span data-stu-id="2f25f-119">Feedback title</span></span>  
  
- <span data-ttu-id="2f25f-120">Feedback comments</span><span class="sxs-lookup"><span data-stu-id="2f25f-120">Feedback comments</span></span>  
  
- <span data-ttu-id="2f25f-121">Feedback rating.</span><span class="sxs-lookup"><span data-stu-id="2f25f-121">Feedback rating.</span></span> <span data-ttu-id="2f25f-122">You can also define a range for ratings by specifying a minimum and maximum (numerical) value for ratings.</span><span class="sxs-lookup"><span data-stu-id="2f25f-122">You can also define a range for ratings by specifying a minimum and maximum (numerical) value for ratings.</span></span> <span data-ttu-id="2f25f-123">For example, a rating of 4 on the scale of 1-5.</span><span class="sxs-lookup"><span data-stu-id="2f25f-123">For example, a rating of 4 on the scale of 1-5.</span></span>  
  
- <span data-ttu-id="2f25f-124">Normalized rating for feedback that is automatically calculated  to show the specified user rating scaled to a value between 0 and 1 based on the minimum and maximum rating values.</span><span class="sxs-lookup"><span data-stu-id="2f25f-124">Normalized rating for feedback that is automatically calculated  to show the specified user rating scaled to a value between 0 and 1 based on the minimum and maximum rating values.</span></span>  
  
  > [!NOTE]
  >  <span data-ttu-id="2f25f-125">The normalized rating helps to normalize or even out the specified rating value for different rating ranges (minimum and maximum rating values).</span><span class="sxs-lookup"><span data-stu-id="2f25f-125">The normalized rating helps to normalize or even out the specified rating value for different rating ranges (minimum and maximum rating values).</span></span> <span data-ttu-id="2f25f-126">The normalized  rating is calculated as follows: (Rating - Minimum Rating) / (Maximum Rating - Minimum Rating).</span><span class="sxs-lookup"><span data-stu-id="2f25f-126">The normalized  rating is calculated as follows: (Rating - Minimum Rating) / (Maximum Rating - Minimum Rating).</span></span>  
  >   
  >  <span data-ttu-id="2f25f-127">Also, rating for a record is calculated as an average of all the normalized ratings for the record.</span><span class="sxs-lookup"><span data-stu-id="2f25f-127">Also, rating for a record is calculated as an average of all the normalized ratings for the record.</span></span>  
  
- <span data-ttu-id="2f25f-128">Feedback status such as Open or Closed</span><span class="sxs-lookup"><span data-stu-id="2f25f-128">Feedback status such as Open or Closed</span></span>  
  
- <span data-ttu-id="2f25f-129">Feedback source to display the source from where the feedback was submitted.</span><span class="sxs-lookup"><span data-stu-id="2f25f-129">Feedback source to display the source from where the feedback was submitted.</span></span> <span data-ttu-id="2f25f-130">If the feedback was created from within [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)], the value is set to **Internal**.</span><span class="sxs-lookup"><span data-stu-id="2f25f-130">If the feedback was created from within [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)], the value is set to **Internal**.</span></span> <span data-ttu-id="2f25f-131">Developers can add a value of their choice depending on the application used to provide feedback.</span><span class="sxs-lookup"><span data-stu-id="2f25f-131">Developers can add a value of their choice depending on the application used to provide feedback.</span></span>  
  
- <span data-ttu-id="2f25f-132">User who created or last modified the feedback record</span><span class="sxs-lookup"><span data-stu-id="2f25f-132">User who created or last modified the feedback record</span></span>  
  
- <span data-ttu-id="2f25f-133">Entity record that the feedback is associated with</span><span class="sxs-lookup"><span data-stu-id="2f25f-133">Entity record that the feedback is associated with</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2f25f-134">In This Section</span><span class="sxs-lookup"><span data-stu-id="2f25f-134">In This Section</span></span>  
 [<span data-ttu-id="2f25f-135">Feedback Entity</span><span class="sxs-lookup"><span data-stu-id="2f25f-135">Feedback Entity</span></span>](entities/feedback.md)  
  
### <a name="see-also"></a><span data-ttu-id="2f25f-136">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2f25f-136">See also</span></span>  
 <span data-ttu-id="2f25f-137">[Work with knowledge articles in Dynamics 365 for Customer Engagement apps](work-knowledge-articles.md) </span><span class="sxs-lookup"><span data-stu-id="2f25f-137">[Work with knowledge articles in Dynamics 365 for Customer Engagement apps](work-knowledge-articles.md) </span></span>  
 [<span data-ttu-id="2f25f-138">Service entities in Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="2f25f-138">Service entities in Customer Engagement apps</span></span>](service-entities.md)
