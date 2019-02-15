---
title: Work with knowledge articles in Dynamics 365 for Customer Engagement (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The section provides information about working with the new native Dynamics 365 for Customer Engagement knowledge management capabilities.
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
- knowledge base entities, creating and searching for knowledge base articles
- creating a subject tree hierarchy (best practice), knowledge base entities
- creating and searching for knowledge base articles, knowledge base entities
- knowledge base entities, templates for
- publishing and unpublishing knowledge base articles, knowledge base entities
- knowledge base entities, creating a subject tree hierarchy (best practice)
- knowledge base entities, specifying search keywords
- states, knowledge base entities
- knowledge base entities, publishing and unpublishing knowledge base articles
- knowledge base entities, KB articles states
- KB articles, see 'knowledge base entities'
- search keywords, knowledge base entities
ms.assetid: 7d0f1da8-1d6b-4795-a4c1-b0ed898e59f0
caps.latest.revision: 39
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c0be1564842758abdcea72c3b091465bff8c8735
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386439"
---
# <a name="work-with-knowledge-articles-in-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="01e55-103">Work with knowledge articles in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="01e55-103">Work with knowledge articles in Dynamics 365 for Customer Engagement apps</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="01e55-104">The new knowledge articles in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] enable you to create rich knowledge articles along with versioning and translation support.</span><span class="sxs-lookup"><span data-stu-id="01e55-104">The new knowledge articles in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] enable you to create rich knowledge articles along with versioning and translation support.</span></span> <span data-ttu-id="01e55-105">When you create and publish a knowledge article, it become available to users in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance so that they can use information in the articles to effectively service the customers.</span><span class="sxs-lookup"><span data-stu-id="01e55-105">When you create and publish a knowledge article, it become available to users in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance so that they can use information in the articles to effectively service the customers.</span></span> <span data-ttu-id="01e55-106">Use the `KnowledgeArticle` entity to store and manage knowledge natively in Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="01e55-106">Use the `KnowledgeArticle` entity to store and manage knowledge natively in Dynamics 365 for Customer Engagement.</span></span>  
  
 <span data-ttu-id="01e55-107">This topic provides information about working with the new native Dynamics 365 for Customer Engagement knowledge management capabilities.</span><span class="sxs-lookup"><span data-stu-id="01e55-107">This topic provides information about working with the new native Dynamics 365 for Customer Engagement knowledge management capabilities.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="01e55-108">If you’re using the earlier knowledge base article (`KBArticle`) entity model, see [Work with earlier Dynamics 365 for Customer Engagement knowledge base articles](work-knowledge-articles.md#EarlierKBArticle) later in this topic.</span><span class="sxs-lookup"><span data-stu-id="01e55-108">If you’re using the earlier knowledge base article (`KBArticle`) entity model, see [Work with earlier Dynamics 365 for Customer Engagement knowledge base articles](work-knowledge-articles.md#EarlierKBArticle) later in this topic.</span></span>  
  
 <span data-ttu-id="01e55-109">You can’t programmatically enable the knowledge base management feature for entities in your Dynamics 365 for Customer Engagement instance; it can only be done using the Dynamics 365 for Customer Engagement web client.</span><span class="sxs-lookup"><span data-stu-id="01e55-109">You can’t programmatically enable the knowledge base management feature for entities in your Dynamics 365 for Customer Engagement instance; it can only be done using the Dynamics 365 for Customer Engagement web client.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="01e55-110">[Set up knowledge management in CRM](http://go.microsoft.com/fwlink/p/?LinkId=691083)</span><span class="sxs-lookup"><span data-stu-id="01e55-110">[Set up knowledge management in CRM](http://go.microsoft.com/fwlink/p/?LinkId=691083)</span></span>  
  
<a name="Create"></a>   
## <a name="create-a-knowledge-article"></a><span data-ttu-id="01e55-111">Tạo bài viết trong cơ sở kiến thức</span><span class="sxs-lookup"><span data-stu-id="01e55-111">Create a knowledge article</span></span>  
 <span data-ttu-id="01e55-112">When you create a knowledge article record, Dynamics 365 for Customer Engagement internally creates a root article for the record.</span><span class="sxs-lookup"><span data-stu-id="01e55-112">When you create a knowledge article record, Dynamics 365 for Customer Engagement internally creates a root article for the record.</span></span> <span data-ttu-id="01e55-113">The root article acts as a container for the primary knowledge article created by you along with all the article versions and translations that you might create in future.</span><span class="sxs-lookup"><span data-stu-id="01e55-113">The root article acts as a container for the primary knowledge article created by you along with all the article versions and translations that you might create in future.</span></span> <span data-ttu-id="01e55-114">The following diagram depicts the entity model for the `KnowledgeArticle` entity.</span><span class="sxs-lookup"><span data-stu-id="01e55-114">The following diagram depicts the entity model for the `KnowledgeArticle` entity.</span></span>  
  
 <span data-ttu-id="01e55-115">![KnowledgeArticle entity model](media/crm-knowledgearticleentitymodel.png "KnowledgeArticle entity model")</span><span class="sxs-lookup"><span data-stu-id="01e55-115">![KnowledgeArticle entity model](media/crm-knowledgearticleentitymodel.png "KnowledgeArticle entity model")</span></span>  
  
 <span data-ttu-id="01e55-116">When you create a knowledge article record, it’s created in the `Draft` state.</span><span class="sxs-lookup"><span data-stu-id="01e55-116">When you create a knowledge article record, it’s created in the `Draft` state.</span></span> <span data-ttu-id="01e55-117">Using the new `KnowledgeArticle` entity, you can create an article by specifying its contents and formatting in the HTML format as compared to using the old `KbArticle` entity where you had to associate it with a template that described the sections and formatting for the article.</span><span class="sxs-lookup"><span data-stu-id="01e55-117">Using the new `KnowledgeArticle` entity, you can create an article by specifying its contents and formatting in the HTML format as compared to using the old `KbArticle` entity where you had to associate it with a template that described the sections and formatting for the article.</span></span> <span data-ttu-id="01e55-118">You can specify your own value for the `KnowledgeArticle`.`ArticlePublicNumber`</span><span class="sxs-lookup"><span data-stu-id="01e55-118">You can specify your own value for the `KnowledgeArticle`.`ArticlePublicNumber`</span></span> <span data-ttu-id="01e55-119">attribute while creating a knowledge article record programmatically; otherwise, the value is automatically generated based on the format you specified in the Dynamics 365 for Customer Engagement settings area in the web client.</span><span class="sxs-lookup"><span data-stu-id="01e55-119">attribute while creating a knowledge article record programmatically; otherwise, the value is automatically generated based on the format you specified in the Dynamics 365 for Customer Engagement settings area in the web client.</span></span> <span data-ttu-id="01e55-120">The `KnowledgeArticle`.`ArticlePublicNumber`</span><span class="sxs-lookup"><span data-stu-id="01e55-120">The `KnowledgeArticle`.`ArticlePublicNumber`</span></span> <span data-ttu-id="01e55-121">attribute stores the ID exposed to customers, partners, and other external users to reference and look up knowledge articles, and remains the same across knowledge article versions and translations.</span><span class="sxs-lookup"><span data-stu-id="01e55-121">attribute stores the ID exposed to customers, partners, and other external users to reference and look up knowledge articles, and remains the same across knowledge article versions and translations.</span></span>  
  
 <span data-ttu-id="01e55-122">The following sample code shows how you can create a knowledge article record:</span><span class="sxs-lookup"><span data-stu-id="01e55-122">The following sample code shows how you can create a knowledge article record:</span></span>  
  
```csharp  
KnowledgeArticle newKnowledgeArticle = new KnowledgeArticle  
{  
   Title = "Sample Knowledge Article",  
   Content = "<p>This is the article content.</p>"  
};  
knowledgeArticleId = _serviceProxy.Create(newKnowledgeArticle);  
Console.WriteLine("Created {0}", newKnowledgeArticle.Title);  
```  
  
<a name="Version"></a>   
## <a name="create-major-and-minor-versions-of-a-knowledge-article"></a><span data-ttu-id="01e55-123">Create major and minor versions of a knowledge article</span><span class="sxs-lookup"><span data-stu-id="01e55-123">Create major and minor versions of a knowledge article</span></span>  
 <span data-ttu-id="01e55-124">When you create a knowledge article record, the major version is automatically set to 1 and minor version to 0.</span><span class="sxs-lookup"><span data-stu-id="01e55-124">When you create a knowledge article record, the major version is automatically set to 1 and minor version to 0.</span></span> <span data-ttu-id="01e55-125">Use the `CreateKnowledgeArticleVersion` message (<xref href="Microsoft.Dynamics.CRM.CreateKnowledgeArticleVersion ?text=CreateKnowledgeArticleVersion Action" /> or <xref:Microsoft.Crm.Sdk.Messages.CreateKnowledgeArticleVersionRequest>) to create a major or minor version of a knowledge article.</span><span class="sxs-lookup"><span data-stu-id="01e55-125">Use the `CreateKnowledgeArticleVersion` message (<xref href="Microsoft.Dynamics.CRM.CreateKnowledgeArticleVersion ?text=CreateKnowledgeArticleVersion Action" /> or <xref:Microsoft.Crm.Sdk.Messages.CreateKnowledgeArticleVersionRequest>) to create a major or minor version of a knowledge article.</span></span> <span data-ttu-id="01e55-126">In the request message, set `IsMajor` to `true` to create a major version; set it to `false` to create a minor version.</span><span class="sxs-lookup"><span data-stu-id="01e55-126">In the request message, set `IsMajor` to `true` to create a major version; set it to `false` to create a minor version.</span></span> <span data-ttu-id="01e55-127">The new version record that is created uses the:</span><span class="sxs-lookup"><span data-stu-id="01e55-127">The new version record that is created uses the:</span></span>  
  
- <span data-ttu-id="01e55-128">`KnowledgeArticle`.`RootArticleId`</span><span class="sxs-lookup"><span data-stu-id="01e55-128">`KnowledgeArticle`.`RootArticleId`</span></span> <span data-ttu-id="01e55-129">attribute to maintain the association with the root knowledge article record.</span><span class="sxs-lookup"><span data-stu-id="01e55-129">attribute to maintain the association with the root knowledge article record.</span></span>  
  
- <span data-ttu-id="01e55-130">`KnowledgeArticle`.`PreviousArticleContentId`</span><span class="sxs-lookup"><span data-stu-id="01e55-130">`KnowledgeArticle`.`PreviousArticleContentId`</span></span> <span data-ttu-id="01e55-131">attribute to point to the previous version of the record.</span><span class="sxs-lookup"><span data-stu-id="01e55-131">attribute to point to the previous version of the record.</span></span>  
  
  <span data-ttu-id="01e55-132">The following sample code shows how to create a major version of a knowledge article record using <xref:Microsoft.Crm.Sdk.Messages.CreateKnowledgeArticleVersionRequest>.</span><span class="sxs-lookup"><span data-stu-id="01e55-132">The following sample code shows how to create a major version of a knowledge article record using <xref:Microsoft.Crm.Sdk.Messages.CreateKnowledgeArticleVersionRequest>.</span></span>  
  
```csharp  
CreateKnowledgeArticleVersionRequest versionRequest = new CreateKnowledgeArticleVersionRequest  
{  
   Source = new EntityReference(KnowledgeArticle.EntityLogicalName, knowledgeArticleId),  
   IsMajor = true  
};  
CreateKnowledgeArticleVersionResponse versionResponse = (CreateKnowledgeArticleVersionResponse)_serviceProxy.Execute(versionRequest);  
```  
  
<a name="Translation"></a>   
## <a name="create-a-knowledge-article-translation"></a><span data-ttu-id="01e55-133">Create a knowledge article translation</span><span class="sxs-lookup"><span data-stu-id="01e55-133">Create a knowledge article translation</span></span>  
 <span data-ttu-id="01e55-134">Use <xref href="Microsoft.Dynamics.CRM.CreateKnowledgeArticleTranslation?text=CreateKnowledgeArticleTranslation Action" /> (Web API) or <xref:Microsoft.Crm.Sdk.Messages.CreateKnowledgeArticleTranslationRequest> (organization service) to create a translation for a knowledge article record.</span><span class="sxs-lookup"><span data-stu-id="01e55-134">Use <xref href="Microsoft.Dynamics.CRM.CreateKnowledgeArticleTranslation?text=CreateKnowledgeArticleTranslation Action" /> (Web API) or <xref:Microsoft.Crm.Sdk.Messages.CreateKnowledgeArticleTranslationRequest> (organization service) to create a translation for a knowledge article record.</span></span> <span data-ttu-id="01e55-135">You can translate your knowledge article in more than 150 languages, and information about these supported languages is available in the new `LanguageLocale` entity.</span><span class="sxs-lookup"><span data-stu-id="01e55-135">You can translate your knowledge article in more than 150 languages, and information about these supported languages is available in the new `LanguageLocale` entity.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="01e55-136">[LanguageLocale Entity](entities/languagelocale.md)</span><span class="sxs-lookup"><span data-stu-id="01e55-136">[LanguageLocale Entity](entities/languagelocale.md)</span></span>  
  
 <span data-ttu-id="01e55-137">Using <xref href="Microsoft.Dynamics.CRM.CreateKnowledgeArticleTranslation?text=CreateKnowledgeArticleTranslation Action" /> (Web API) or <xref:Microsoft.Crm.Sdk.Messages.CreateKnowledgeArticleTranslationRequest> (organization service) creates a new knowledge article record with the title, content, description and keywords copied from the source record to the new record, and the language of the new record set to the one you specified in the request.</span><span class="sxs-lookup"><span data-stu-id="01e55-137">Using <xref href="Microsoft.Dynamics.CRM.CreateKnowledgeArticleTranslation?text=CreateKnowledgeArticleTranslation Action" /> (Web API) or <xref:Microsoft.Crm.Sdk.Messages.CreateKnowledgeArticleTranslationRequest> (organization service) creates a new knowledge article record with the title, content, description and keywords copied from the source record to the new record, and the language of the new record set to the one you specified in the request.</span></span> <span data-ttu-id="01e55-138">You also need to specify whether the new record will be a major or minor version.</span><span class="sxs-lookup"><span data-stu-id="01e55-138">You also need to specify whether the new record will be a major or minor version.</span></span> <span data-ttu-id="01e55-139">The new record uses the `KnowledgeArticle`.`ParentArticleContentId`</span><span class="sxs-lookup"><span data-stu-id="01e55-139">The new record uses the `KnowledgeArticle`.`ParentArticleContentId`</span></span> <span data-ttu-id="01e55-140">attribute to maintain the association with the primary knowledge article record.</span><span class="sxs-lookup"><span data-stu-id="01e55-140">attribute to maintain the association with the primary knowledge article record.</span></span>  
  
 <span data-ttu-id="01e55-141">After you execute this message and get a response, retrieve the knowledge article record from the response object, and then update the title, content, description, and keywords to add the translated content.</span><span class="sxs-lookup"><span data-stu-id="01e55-141">After you execute this message and get a response, retrieve the knowledge article record from the response object, and then update the title, content, description, and keywords to add the translated content.</span></span>  
  
 <span data-ttu-id="01e55-142">The following sample code shows how to create a knowledge article translation using <xref:Microsoft.Crm.Sdk.Messages.CreateKnowledgeArticleTranslationRequest>:</span><span class="sxs-lookup"><span data-stu-id="01e55-142">The following sample code shows how to create a knowledge article translation using <xref:Microsoft.Crm.Sdk.Messages.CreateKnowledgeArticleTranslationRequest>:</span></span>  
  
```csharp  
CreateKnowledgeArticleTranslationRequest translationRequest = new CreateKnowledgeArticleTranslationRequest  
{  
   Source = new EntityReference(KnowledgeArticle.EntityLogicalName, knowledgeArticleId),  
   Language = new EntityReference(LanguageLocale.EntityLogicalName, languageLocaleId), //languageLocaleId = GUID of the Primary Key of LanguageLocale record  
   IsMajor = true    // Creating a major version   
};  
CreateKnowledgeArticleTranslationResponse translationResponse = (CreateKnowledgeArticleTranslationResponse)_serviceProxy.Execute(translationRequest);  
  
// Retrieve the new knowledge article record  
KnowledgeArticle respObject = (KnowledgeArticle)_serviceProxy.Retrieve(KnowledgeArticle.EntityLogicalName,   
      translationResponse.CreateKnowledgeArticleTranslation.Id, new ColumnSet(true));  
```  
  
> [!NOTE]
>  <span data-ttu-id="01e55-143">The GUID value of the primary key (`LanguageLocaleId`) for each language record in the `LanguageLocale` entity is the same across all [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organizations.</span><span class="sxs-lookup"><span data-stu-id="01e55-143">The GUID value of the primary key (`LanguageLocaleId`) for each language record in the `LanguageLocale` entity is the same across all [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organizations.</span></span>  
  
<a name="KnowledgeLifecycle"></a>   
## <a name="knowledge-article-lifecycle-change-the-state-of-a-knowledge-article"></a><span data-ttu-id="01e55-144">Knowledge article lifecycle: Change the state of a knowledge article</span><span class="sxs-lookup"><span data-stu-id="01e55-144">Knowledge article lifecycle: Change the state of a knowledge article</span></span>  
 <span data-ttu-id="01e55-145">During its lifecycle, a knowledge article can be in the following states:</span><span class="sxs-lookup"><span data-stu-id="01e55-145">During its lifecycle, a knowledge article can be in the following states:</span></span>  
  
- <span data-ttu-id="01e55-146">0: Draft (after a knowledge article is created)</span><span class="sxs-lookup"><span data-stu-id="01e55-146">0: Draft (after a knowledge article is created)</span></span>  
  
- <span data-ttu-id="01e55-147">1: Approved (after a knowledge article is approved)</span><span class="sxs-lookup"><span data-stu-id="01e55-147">1: Approved (after a knowledge article is approved)</span></span>  
  
- <span data-ttu-id="01e55-148">2: Scheduled (after a knowledge article is scheduled to be published)</span><span class="sxs-lookup"><span data-stu-id="01e55-148">2: Scheduled (after a knowledge article is scheduled to be published)</span></span>  
  
- <span data-ttu-id="01e55-149">3: Published (after a knowledge article is published)</span><span class="sxs-lookup"><span data-stu-id="01e55-149">3: Published (after a knowledge article is published)</span></span>  
  
- <span data-ttu-id="01e55-150">4: Expired (after a knowledge article is expired as per the expiration date specified while publishing)</span><span class="sxs-lookup"><span data-stu-id="01e55-150">4: Expired (after a knowledge article is expired as per the expiration date specified while publishing)</span></span>  
  
- <span data-ttu-id="01e55-151">5: Archived (after a knowledge article is archived)</span><span class="sxs-lookup"><span data-stu-id="01e55-151">5: Archived (after a knowledge article is archived)</span></span>  
  
- <span data-ttu-id="01e55-152">6: Discarded (after a knowledge article is discarded)</span><span class="sxs-lookup"><span data-stu-id="01e55-152">6: Discarded (after a knowledge article is discarded)</span></span>  
  
  <span data-ttu-id="01e55-153">To change the state of the article, use the `Update` message on the knowledge article record to update the `KnowledgeArticle.StateCode` attribute.</span><span class="sxs-lookup"><span data-stu-id="01e55-153">To change the state of the article, use the `Update` message on the knowledge article record to update the `KnowledgeArticle.StateCode` attribute.</span></span> <span data-ttu-id="01e55-154">For early bound types, use the `KnowledgeArticleState` enumeration to set the possible states.</span><span class="sxs-lookup"><span data-stu-id="01e55-154">For early bound types, use the `KnowledgeArticleState` enumeration to set the possible states.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="01e55-155">[Perform specialized operations using Update](org-service/perform-specialized-operations-using-update.md).</span><span class="sxs-lookup"><span data-stu-id="01e55-155">[Perform specialized operations using Update](org-service/perform-specialized-operations-using-update.md).</span></span>  
  
  <span data-ttu-id="01e55-156">The following sample code shows how to publish a knowledge article record.</span><span class="sxs-lookup"><span data-stu-id="01e55-156">The following sample code shows how to publish a knowledge article record.</span></span>  
  
```csharp  
// Retrieve the knowledge article record  
KnowledgeArticle myKnowledgeArticle = (KnowledgeArticle)_serviceProxy.Retrieve(  
        KnowledgeArticle.EntityLogicalName, knowledgeArticleId, new ColumnSet("statecode"));  
  
// Update the knowledge article record  
myKnowledgeArticle.StateCode = KnowledgeArticleState.Published;  
UpdateRequest updateKnowledgeArticle = new UpdateRequest  
{  
    Target = myKnowledgeArticle  
};  
_serviceProxy.Execute(updateKnowledgeArticle);  
  
```  
  
<a name="Associate"></a>   
## <a name="associate-a-knowledge-article-record-with-a-dynamics-365-for-customer-engagement-apps-entity-instance"></a><span data-ttu-id="01e55-157">Associate a knowledge article record with a Dynamics 365 for Customer Engagement apps entity instance</span><span class="sxs-lookup"><span data-stu-id="01e55-157">Associate a knowledge article record with a Dynamics 365 for Customer Engagement apps entity instance</span></span>  
 <span data-ttu-id="01e55-158">When you enable embedded knowledge search for an entity in Dynamics 365 for Customer Engagement using the web client, a many-to-many relationship, `msdyn_`***<Entity_Name>***`_knowledgearticle`, is automatically created.</span><span class="sxs-lookup"><span data-stu-id="01e55-158">When you enable embedded knowledge search for an entity in Dynamics 365 for Customer Engagement using the web client, a many-to-many relationship, `msdyn_`***<Entity_Name>***`_knowledgearticle`, is automatically created.</span></span> <span data-ttu-id="01e55-159">You can use this relationship to programmatically associate or link a `KnowledgeArticle` instance with a Dynamics 365 for Customer Engagement entity instance.</span><span class="sxs-lookup"><span data-stu-id="01e55-159">You can use this relationship to programmatically associate or link a `KnowledgeArticle` instance with a Dynamics 365 for Customer Engagement entity instance.</span></span> <span data-ttu-id="01e55-160">When you associate a `KnowledgeArticle` instance with an entity instance, a record for the relationship is created in an intersect entity called `msdyn_`***<Entity_Name>***`_knowledgearticle`.</span><span class="sxs-lookup"><span data-stu-id="01e55-160">When you associate a `KnowledgeArticle` instance with an entity instance, a record for the relationship is created in an intersect entity called `msdyn_`***<Entity_Name>***`_knowledgearticle`.</span></span> <span data-ttu-id="01e55-161">For example, when you associate a `KnowledgeArticle` instance with an `Account` instance for the first time, an intersect entity called `msdyn_account_knowledgearticle` is created, and a record with the association mapping is created in this intersect entity.</span><span class="sxs-lookup"><span data-stu-id="01e55-161">For example, when you associate a `KnowledgeArticle` instance with an `Account` instance for the first time, an intersect entity called `msdyn_account_knowledgearticle` is created, and a record with the association mapping is created in this intersect entity.</span></span> <span data-ttu-id="01e55-162">By default, the `Incident` (Case) entity is enabled for the embedded knowledge search, and when you link a `KnowledgeArticle` record to an `Incident` record, an association record is created in the `KnowledgeArticleIncident` intersect entity.</span><span class="sxs-lookup"><span data-stu-id="01e55-162">By default, the `Incident` (Case) entity is enabled for the embedded knowledge search, and when you link a `KnowledgeArticle` record to an `Incident` record, an association record is created in the `KnowledgeArticleIncident` intersect entity.</span></span>  
  
 <span data-ttu-id="01e55-163">The following sample code demonstrates how to associate a `KnowledgeArticle` instance with an `Account` instance:</span><span class="sxs-lookup"><span data-stu-id="01e55-163">The following sample code demonstrates how to associate a `KnowledgeArticle` instance with an `Account` instance:</span></span>  
  
```csharp  
// Associate the knowledge article record with an account record  
  
// Step 1: Create a collection of knowledge article records that will be   
// associated to the account. In this case, we have only a single  
// knowledge article record to be associated.  
EntityReferenceCollection relatedEntities = new EntityReferenceCollection();  
relatedEntities.Add(new EntityReference(KnowledgeArticle.EntityLogicalName, knowledgeArticleId));  
  
// Step 2: Create an object that defines the relationship between knowledge article record and account record.  
// Use the many-to-many relationship name (msdyn_account_knowledgearticle) between knowledge article  
// record and account record.  
Relationship newRelationship = new Relationship("msdyn_account_knowledgearticle");  
  
// Step 3: Associate the knowledge article record with the account record.  
_serviceProxy.Associate(Account.EntityLogicalName, accountId, newRelationship, relatedEntities);  
  
```  
  
<a name="IncrementViewCount"></a>   
## <a name="increment-knowledge-article-view-count"></a><span data-ttu-id="01e55-164">Increment knowledge article view count</span><span class="sxs-lookup"><span data-stu-id="01e55-164">Increment knowledge article view count</span></span>  
 <span data-ttu-id="01e55-165">Use the <xref:Microsoft.Crm.Sdk.Messages.IncrementKnowledgeArticleViewCountRequest> message to increment the view count of a knowledge article record for a given day in the `KnowledgeArticleViews` entity.</span><span class="sxs-lookup"><span data-stu-id="01e55-165">Use the <xref:Microsoft.Crm.Sdk.Messages.IncrementKnowledgeArticleViewCountRequest> message to increment the view count of a knowledge article record for a given day in the `KnowledgeArticleViews` entity.</span></span> <span data-ttu-id="01e55-166">If a record doesn’t exist for a knowledge article for a specified day, it will create a record and then set the specified view count value in the `KnowledgeArticleViews`.`KnowledgeArticleView`</span><span class="sxs-lookup"><span data-stu-id="01e55-166">If a record doesn’t exist for a knowledge article for a specified day, it will create a record and then set the specified view count value in the `KnowledgeArticleViews`.`KnowledgeArticleView`</span></span> <span data-ttu-id="01e55-167">attribute.</span><span class="sxs-lookup"><span data-stu-id="01e55-167">attribute.</span></span> <span data-ttu-id="01e55-168">If a record already exists for a knowledge article for the specified day, it will just increment the view count in the `KnowledgeArticleViews`.`KnowledgeArticleView`</span><span class="sxs-lookup"><span data-stu-id="01e55-168">If a record already exists for a knowledge article for the specified day, it will just increment the view count in the `KnowledgeArticleViews`.`KnowledgeArticleView`</span></span> <span data-ttu-id="01e55-169">attribute of the existing record.</span><span class="sxs-lookup"><span data-stu-id="01e55-169">attribute of the existing record.</span></span>  
  
<a name="Search"></a>   
## <a name="search-knowledge-articles-using-full-text-search"></a><span data-ttu-id="01e55-170">Search knowledge articles using full-text search</span><span class="sxs-lookup"><span data-stu-id="01e55-170">Search knowledge articles using full-text search</span></span>  
 <span data-ttu-id="01e55-171">Knowledge articles in Dynamics 365 for Customer Engagement, including their versions and translations, are full-text indexed and support SQL Server full-text search.</span><span class="sxs-lookup"><span data-stu-id="01e55-171">Knowledge articles in Dynamics 365 for Customer Engagement, including their versions and translations, are full-text indexed and support SQL Server full-text search.</span></span> <span data-ttu-id="01e55-172">For more information about full-text search, see [SQL Server: Full-text Search](https://docs.microsoft.com/sql/relational-databases/search/full-text-search).</span><span class="sxs-lookup"><span data-stu-id="01e55-172">For more information about full-text search, see [SQL Server: Full-text Search](https://docs.microsoft.com/sql/relational-databases/search/full-text-search).</span></span>  
  
 <span data-ttu-id="01e55-173">Use the <xref:Microsoft.Crm.Sdk.Messages.FullTextSearchKnowledgeArticleRequest> message to search knowledge article from your applications to find the information you are looking for.</span><span class="sxs-lookup"><span data-stu-id="01e55-173">Use the <xref:Microsoft.Crm.Sdk.Messages.FullTextSearchKnowledgeArticleRequest> message to search knowledge article from your applications to find the information you are looking for.</span></span> <span data-ttu-id="01e55-174">The <xref:Microsoft.Crm.Sdk.Messages.FullTextSearchKnowledgeArticleRequest> message lets you use inflectional stem matching (allows for a different tense or inflection to be substituted for the search text) and specify query criteria (using FetchXML or QueryExpression to specify filtering, ordering, sorting, and paging) to find knowledge articles with specified text.</span><span class="sxs-lookup"><span data-stu-id="01e55-174">The <xref:Microsoft.Crm.Sdk.Messages.FullTextSearchKnowledgeArticleRequest> message lets you use inflectional stem matching (allows for a different tense or inflection to be substituted for the search text) and specify query criteria (using FetchXML or QueryExpression to specify filtering, ordering, sorting, and paging) to find knowledge articles with specified text.</span></span> <span data-ttu-id="01e55-175">You can also choose to remove multiple versions of the same articles in the search results and filter on the knowledge article state while searching for a text.</span><span class="sxs-lookup"><span data-stu-id="01e55-175">You can also choose to remove multiple versions of the same articles in the search results and filter on the knowledge article state while searching for a text.</span></span>  
  
<a name="EarlierKBArticle"></a>   
## <a name="work-with-earlier-dynamics-365-for-customer-engagement-apps-knowledge-base-articles"></a><span data-ttu-id="01e55-176">Work with earlier Dynamics 365 for Customer Engagement apps knowledge base articles</span><span class="sxs-lookup"><span data-stu-id="01e55-176">Work with earlier Dynamics 365 for Customer Engagement apps knowledge base articles</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="01e55-177">This section provides you with information about working with the earlier knowledge base article entity model for knowledge management in Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="01e55-177">This section provides you with information about working with the earlier knowledge base article entity model for knowledge management in Dynamics 365 for Customer Engagement.</span></span> <span data-ttu-id="01e55-178">While the entities mentioned in this section are still available in the current version, you should use the knowledge management entities mentioned earlier to take advantage of the enhanced knowledge management experience.</span><span class="sxs-lookup"><span data-stu-id="01e55-178">While the entities mentioned in this section are still available in the current version, you should use the knowledge management entities mentioned earlier to take advantage of the enhanced knowledge management experience.</span></span>  
  
 <span data-ttu-id="01e55-179">During its lifecycle, a knowledge base article can be in the following states:</span><span class="sxs-lookup"><span data-stu-id="01e55-179">During its lifecycle, a knowledge base article can be in the following states:</span></span>  
  
- <span data-ttu-id="01e55-180">1: Draft (after an article is created)</span><span class="sxs-lookup"><span data-stu-id="01e55-180">1: Draft (after an article is created)</span></span>  
  
- <span data-ttu-id="01e55-181">2: Unapproved (during editing)</span><span class="sxs-lookup"><span data-stu-id="01e55-181">2: Unapproved (during editing)</span></span>  
  
- <span data-ttu-id="01e55-182">3: Published (after an article is published)</span><span class="sxs-lookup"><span data-stu-id="01e55-182">3: Published (after an article is published)</span></span>  
  
  <span data-ttu-id="01e55-183">To change the state of the article, use the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="01e55-183">To change the state of the article, use the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message.</span></span> <span data-ttu-id="01e55-184">For early bound types, use the `KbArticleState` enumeration to set the possible states.</span><span class="sxs-lookup"><span data-stu-id="01e55-184">For early bound types, use the `KbArticleState` enumeration to set the possible states.</span></span>  
  
  <span data-ttu-id="01e55-185">When you create an article, you have to associate it with a template and a subject.</span><span class="sxs-lookup"><span data-stu-id="01e55-185">When you create an article, you have to associate it with a template and a subject.</span></span> <span data-ttu-id="01e55-186">An article template describes the sections and formatting for the article.</span><span class="sxs-lookup"><span data-stu-id="01e55-186">An article template describes the sections and formatting for the article.</span></span> <span data-ttu-id="01e55-187">Subjects are used to organize the articles by business categories that are also used to group cases (incidents), sales literature, and products.</span><span class="sxs-lookup"><span data-stu-id="01e55-187">Subjects are used to organize the articles by business categories that are also used to group cases (incidents), sales literature, and products.</span></span> <span data-ttu-id="01e55-188">A best practice is to create a subject tree hierarchy and all necessary article templates before you create an article.</span><span class="sxs-lookup"><span data-stu-id="01e55-188">A best practice is to create a subject tree hierarchy and all necessary article templates before you create an article.</span></span>  
  
> [!NOTE]
> [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="01e55-189">provides several article templates.</span><span class="sxs-lookup"><span data-stu-id="01e55-189">provides several article templates.</span></span> <span data-ttu-id="01e55-190">They include a standard article, a solution to a problem, a procedure, and other templates.</span><span class="sxs-lookup"><span data-stu-id="01e55-190">They include a standard article, a solution to a problem, a procedure, and other templates.</span></span> <span data-ttu-id="01e55-191">The recommended method of creating article templates is by using the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] web application.</span><span class="sxs-lookup"><span data-stu-id="01e55-191">The recommended method of creating article templates is by using the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] web application.</span></span> <span data-ttu-id="01e55-192">If you want to create an article template programmatically, use existing article templates as examples of what information to include and how to format the data.</span><span class="sxs-lookup"><span data-stu-id="01e55-192">If you want to create an article template programmatically, use existing article templates as examples of what information to include and how to format the data.</span></span>  
  
 <span data-ttu-id="01e55-193">To associate an article with a template, use the `KbArticle.KbArticleTemplateId` attribute.</span><span class="sxs-lookup"><span data-stu-id="01e55-193">To associate an article with a template, use the `KbArticle.KbArticleTemplateId` attribute.</span></span> <span data-ttu-id="01e55-194">To place an article in a specific category by specifying a subject, use the `KbArticle.SubjectId` attribute.</span><span class="sxs-lookup"><span data-stu-id="01e55-194">To place an article in a specific category by specifying a subject, use the `KbArticle.SubjectId` attribute.</span></span>  
  
 <span data-ttu-id="01e55-195">Specify the title of the article and the keywords that you want to use in the search.</span><span class="sxs-lookup"><span data-stu-id="01e55-195">Specify the title of the article and the keywords that you want to use in the search.</span></span> <span data-ttu-id="01e55-196">To describe an article you can use the `KbArticle.Description` attribute.</span><span class="sxs-lookup"><span data-stu-id="01e55-196">To describe an article you can use the `KbArticle.Description` attribute.</span></span> <span data-ttu-id="01e55-197">To add the content for the article, use the `KbArticle.Content` attribute.</span><span class="sxs-lookup"><span data-stu-id="01e55-197">To add the content for the article, use the `KbArticle.Content` attribute.</span></span> <span data-ttu-id="01e55-198">Use the `Kbarticle.ArticleXml` attribute to add the XML data for article.</span><span class="sxs-lookup"><span data-stu-id="01e55-198">Use the `Kbarticle.ArticleXml` attribute to add the XML data for article.</span></span> <span data-ttu-id="01e55-199">The `KbArticle.LanguageCode` value is obtained from the template to help you write the queries that sort the articles by the language.</span><span class="sxs-lookup"><span data-stu-id="01e55-199">The `KbArticle.LanguageCode` value is obtained from the template to help you write the queries that sort the articles by the language.</span></span>  
  
 <span data-ttu-id="01e55-200">When an article is created it is saved as a draft.</span><span class="sxs-lookup"><span data-stu-id="01e55-200">When an article is created it is saved as a draft.</span></span> <span data-ttu-id="01e55-201">After that, you can change the state of the article from “Draft” to “Unapproved.”</span><span class="sxs-lookup"><span data-stu-id="01e55-201">After that, you can change the state of the article from “Draft” to “Unapproved.”</span></span> <span data-ttu-id="01e55-202">You can modify the content of an unapproved article and make it ready for publishing.</span><span class="sxs-lookup"><span data-stu-id="01e55-202">You can modify the content of an unapproved article and make it ready for publishing.</span></span> <span data-ttu-id="01e55-203">When the article is ready to be published, change the state from “Unapproved” to “Published.”</span><span class="sxs-lookup"><span data-stu-id="01e55-203">When the article is ready to be published, change the state from “Unapproved” to “Published.”</span></span>  
  
 <span data-ttu-id="01e55-204">An unpublished article obtains the format settings from a template.</span><span class="sxs-lookup"><span data-stu-id="01e55-204">An unpublished article obtains the format settings from a template.</span></span> <span data-ttu-id="01e55-205">If you change a template format, the changes are automatically propagated to articles in the “Draft” and “Unapproved” states.</span><span class="sxs-lookup"><span data-stu-id="01e55-205">If you change a template format, the changes are automatically propagated to articles in the “Draft” and “Unapproved” states.</span></span>  
  
 <span data-ttu-id="01e55-206">After you publish an article, you can add comments (`KbArticleComment`), but you can’t edit it, regardless of your privileges.</span><span class="sxs-lookup"><span data-stu-id="01e55-206">After you publish an article, you can add comments (`KbArticleComment`), but you can’t edit it, regardless of your privileges.</span></span> <span data-ttu-id="01e55-207">The comments can be added to the article that is in any of the states.</span><span class="sxs-lookup"><span data-stu-id="01e55-207">The comments can be added to the article that is in any of the states.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="01e55-208">The comments can be added to the article in any state: Draft, Unapproved or Published.</span><span class="sxs-lookup"><span data-stu-id="01e55-208">The comments can be added to the article in any state: Draft, Unapproved or Published.</span></span>  
  
 <span data-ttu-id="01e55-209">To revise or update the article, you have to unpublish it.</span><span class="sxs-lookup"><span data-stu-id="01e55-209">To revise or update the article, you have to unpublish it.</span></span> <span data-ttu-id="01e55-210">To unpublish an article, change the state of the article from Published to Unapproved.</span><span class="sxs-lookup"><span data-stu-id="01e55-210">To unpublish an article, change the state of the article from Published to Unapproved.</span></span> <span data-ttu-id="01e55-211">To delete an article from the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] database, change the state of the article from Published to Unapproved or Draft.</span><span class="sxs-lookup"><span data-stu-id="01e55-211">To delete an article from the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] database, change the state of the article from Published to Unapproved or Draft.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="01e55-212">A knowledge base article cannot be deleted, if it is in the Published state.</span><span class="sxs-lookup"><span data-stu-id="01e55-212">A knowledge base article cannot be deleted, if it is in the Published state.</span></span>  
  
 <span data-ttu-id="01e55-213">For more information on creating, updating, editing, and locating an article in the knowledge base, see [Use articles in the knowledge base](http://go.microsoft.com/fwlink/p/?LinkId=526812).</span><span class="sxs-lookup"><span data-stu-id="01e55-213">For more information on creating, updating, editing, and locating an article in the knowledge base, see [Use articles in the knowledge base](http://go.microsoft.com/fwlink/p/?LinkId=526812).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="01e55-214">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="01e55-214">See also</span></span>  
 <span data-ttu-id="01e55-215">[Knowledge Base Entities](knowledge-management-entities.md)  </span><span class="sxs-lookup"><span data-stu-id="01e55-215">[Knowledge Base Entities](knowledge-management-entities.md)  </span></span>  
 <span data-ttu-id="01e55-216">[KnowledgeArticle Entity](entities/knowledgearticle.md) </span><span class="sxs-lookup"><span data-stu-id="01e55-216">[KnowledgeArticle Entity](entities/knowledgearticle.md) </span></span>  
 <span data-ttu-id="01e55-217">[KnowledgeArticleViews Entity](entities/knowledgearticleviews.md) </span><span class="sxs-lookup"><span data-stu-id="01e55-217">[KnowledgeArticleViews Entity](entities/knowledgearticleviews.md) </span></span>  
 <span data-ttu-id="01e55-218">[KnowledgeBaseRecord Entity](entities/knowledgebaserecord.md) </span><span class="sxs-lookup"><span data-stu-id="01e55-218">[KnowledgeBaseRecord Entity](entities/knowledgebaserecord.md) </span></span>  
 <span data-ttu-id="01e55-219">[LanguageLocale Entity](entities/languagelocale.md) </span><span class="sxs-lookup"><span data-stu-id="01e55-219">[LanguageLocale Entity](entities/languagelocale.md) </span></span>  
 [<span data-ttu-id="01e55-220">KbArticle Entity</span><span class="sxs-lookup"><span data-stu-id="01e55-220">KbArticle Entity</span></span>](entities/kbarticle.md)
