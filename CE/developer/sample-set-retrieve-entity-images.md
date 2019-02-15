---
title: 'Sample: Set and retrieve entity images (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
descriptions: The sample demonstrates how to set and retrieve data for entity images.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: fa9352f2-ef46-401f-b376-d0192c9f45a7
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b2394beb6731358a2a63498b00bc6b97f73f0d8d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386880"
---
# <a name="sample-set-and-retrieve-entity-images"></a><span data-ttu-id="9aa48-102">Sample: Set and retrieve entity images</span><span class="sxs-lookup"><span data-stu-id="9aa48-102">Sample: Set and retrieve entity images</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9aa48-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="9aa48-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="9aa48-104">Download the complete sample from [Work with late bound entities](https://code.msdn.microsoft.com/Work-with-late-bound-e3208935).</span><span class="sxs-lookup"><span data-stu-id="9aa48-104">Download the complete sample from [Work with late bound entities](https://code.msdn.microsoft.com/Work-with-late-bound-e3208935).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="9aa48-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="9aa48-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="9aa48-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="9aa48-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="9aa48-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="9aa48-107">Demonstrates</span></span>  
 <span data-ttu-id="9aa48-108">This sample shows how to set and retrieve data for entity images.</span><span class="sxs-lookup"><span data-stu-id="9aa48-108">This sample shows how to set and retrieve data for entity images.</span></span>  
  
 <span data-ttu-id="9aa48-109">The sample does the following tasks:</span><span class="sxs-lookup"><span data-stu-id="9aa48-109">The sample does the following tasks:</span></span>  
  
1. <span data-ttu-id="9aa48-110">Uses the `CreateImageAttributeDemoEntity` method to:</span><span class="sxs-lookup"><span data-stu-id="9aa48-110">Uses the `CreateImageAttributeDemoEntity` method to:</span></span>  
  
   1.  <span data-ttu-id="9aa48-111">Create a custom entity with the schema name `sample_ImageAttributeDemo` and a primary attribute with the schema name `sample_Name`.</span><span class="sxs-lookup"><span data-stu-id="9aa48-111">Create a custom entity with the schema name `sample_ImageAttributeDemo` and a primary attribute with the schema name `sample_Name`.</span></span>  
  
   2.  <span data-ttu-id="9aa48-112">Create an image attribute with the schema name `EntityImage`.</span><span class="sxs-lookup"><span data-stu-id="9aa48-112">Create an image attribute with the schema name `EntityImage`.</span></span> <span data-ttu-id="9aa48-113">All image attributes use this name.</span><span class="sxs-lookup"><span data-stu-id="9aa48-113">All image attributes use this name.</span></span>  
  
   3.  <span data-ttu-id="9aa48-114">Retrieve and update the main form for the `sample_ImageAttributeDemo` entity to set the `<form>` `showImage` attribute to `true` so that the image is displayed in the form.</span><span class="sxs-lookup"><span data-stu-id="9aa48-114">Retrieve and update the main form for the `sample_ImageAttributeDemo` entity to set the `<form>` `showImage` attribute to `true` so that the image is displayed in the form.</span></span>  
  
   4.  <span data-ttu-id="9aa48-115">Publish the `sample_ImageAttributeDemo` entity.</span><span class="sxs-lookup"><span data-stu-id="9aa48-115">Publish the `sample_ImageAttributeDemo` entity.</span></span>  
  
2. <span data-ttu-id="9aa48-116">Creates five new records for the `sample_ImageAttributeDemo` entity using five different sized images located in the `Images` folder as shown here.</span><span class="sxs-lookup"><span data-stu-id="9aa48-116">Creates five new records for the `sample_ImageAttributeDemo` entity using five different sized images located in the `Images` folder as shown here.</span></span>  
  
   <span data-ttu-id="9aa48-117">![The relative size of source images](media/image-attribute-sample-before.png "The relative size of source images")</span><span class="sxs-lookup"><span data-stu-id="9aa48-117">![The relative size of source images](media/image-attribute-sample-before.png "The relative size of source images")</span></span>  
  
    <span data-ttu-id="9aa48-118">The `sample_Name` primary attribute field value is the name of the file.</span><span class="sxs-lookup"><span data-stu-id="9aa48-118">The `sample_Name` primary attribute field value is the name of the file.</span></span>  
  
    <span data-ttu-id="9aa48-119">After each record is created you have the opportunity to view the record in the web browser application using the `ShowEntityFormInBrowser` method so that you can see how the source images are resized to fit the space available in the form.</span><span class="sxs-lookup"><span data-stu-id="9aa48-119">After each record is created you have the opportunity to view the record in the web browser application using the `ShowEntityFormInBrowser` method so that you can see how the source images are resized to fit the space available in the form.</span></span>  
  
   [!code-csharp[DynamicEntity#EntityImages2](../snippets/csharp/CRMV8/dynamicentity/cs/entityimages2.cs#entityimages2)]  
  
   > [!NOTE]
   >  <span data-ttu-id="9aa48-120">This code uses late bound entities because the entity is created in the sample and is not available as a strongly typed class.</span><span class="sxs-lookup"><span data-stu-id="9aa48-120">This code uses late bound entities because the entity is created in the sample and is not available as a strongly typed class.</span></span> <span data-ttu-id="9aa48-121">However, after early bound classes are generated, the strongly typed classes could be used.</span><span class="sxs-lookup"><span data-stu-id="9aa48-121">However, after early bound classes are generated, the strongly typed classes could be used.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="9aa48-122">[Create Early Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)](org-service/create-early-bound-entity-classes-code-generation-tool.md)</span><span class="sxs-lookup"><span data-stu-id="9aa48-122">[Create Early Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)](org-service/create-early-bound-entity-classes-code-generation-tool.md)</span></span>
  
3. <span data-ttu-id="9aa48-123">Retrieves the records with the `entityimage` attribute and saves the resized files.</span><span class="sxs-lookup"><span data-stu-id="9aa48-123">Retrieves the records with the `entityimage` attribute and saves the resized files.</span></span> <span data-ttu-id="9aa48-124">After you run the sample you can find the files saved in the `\bin\Debug` folder.</span><span class="sxs-lookup"><span data-stu-id="9aa48-124">After you run the sample you can find the files saved in the `\bin\Debug` folder.</span></span>  
  
   [!code-csharp[DynamicEntity#EntityImages3](../snippets/csharp/CRMV8/dynamicentity/cs/entityimages3.cs#entityimages3)]  
  
    <span data-ttu-id="9aa48-125">The image files are resized as shown here.</span><span class="sxs-lookup"><span data-stu-id="9aa48-125">The image files are resized as shown here.</span></span>  
  
   <span data-ttu-id="9aa48-126">![The relative size of downloaded images](media/image-attribute-sample-after.png "The relative size of downloaded images")</span><span class="sxs-lookup"><span data-stu-id="9aa48-126">![The relative size of downloaded images](media/image-attribute-sample-after.png "The relative size of downloaded images")</span></span>  
  
4. <span data-ttu-id="9aa48-127">Retrieves the records with the `entityimage_url` attribute and displays the relative URL values you can include in your application to access the images.</span><span class="sxs-lookup"><span data-stu-id="9aa48-127">Retrieves the records with the `entityimage_url` attribute and displays the relative URL values you can include in your application to access the images.</span></span> <span data-ttu-id="9aa48-128">This query should be more responsive because the amount of data transferred is smaller.</span><span class="sxs-lookup"><span data-stu-id="9aa48-128">This query should be more responsive because the amount of data transferred is smaller.</span></span>  
  
   [!code-csharp[DynamicEntity#EntityImages4](../snippets/csharp/CRMV8/dynamicentity/cs/entityimages4.cs#entityimages4)]  
  
    <span data-ttu-id="9aa48-129">The relative URLs will look something like the following examples:</span><span class="sxs-lookup"><span data-stu-id="9aa48-129">The relative URLs will look something like the following examples:</span></span>  
  
   -   <span data-ttu-id="9aa48-130">/Image/download.aspx?Entity=sample_imageattributedemo&Attribute=entityimage&Id=2ed5a666-7b51-e311-9088-00155d9c5607&Timestamp=635205044273046819</span><span class="sxs-lookup"><span data-stu-id="9aa48-130">/Image/download.aspx?Entity=sample_imageattributedemo&Attribute=entityimage&Id=2ed5a666-7b51-e311-9088-00155d9c5607&Timestamp=635205044273046819</span></span>  
  
   -   <span data-ttu-id="9aa48-131">/Image/download.aspx?Entity=sample_imageattributedemo&Attribute=entityimage&Id=22f17c6d-7b51-e311-9088-00155d9c5607&Timestamp=635205044320978850</span><span class="sxs-lookup"><span data-stu-id="9aa48-131">/Image/download.aspx?Entity=sample_imageattributedemo&Attribute=entityimage&Id=22f17c6d-7b51-e311-9088-00155d9c5607&Timestamp=635205044320978850</span></span>  
  
   -   <span data-ttu-id="9aa48-132">/Image/download.aspx?Entity=sample_imageattributedemo&Attribute=entityimage&Id=24f17c6d-7b51-e311-9088-00155d9c5607&Timestamp=635205044333049824</span><span class="sxs-lookup"><span data-stu-id="9aa48-132">/Image/download.aspx?Entity=sample_imageattributedemo&Attribute=entityimage&Id=24f17c6d-7b51-e311-9088-00155d9c5607&Timestamp=635205044333049824</span></span>  
  
   -   <span data-ttu-id="9aa48-133">/Image/download.aspx?Entity=sample_imageattributedemo&Attribute=entityimage&Id=26f17c6d-7b51-e311-9088-00155d9c5607&Timestamp=635205044343080227</span><span class="sxs-lookup"><span data-stu-id="9aa48-133">/Image/download.aspx?Entity=sample_imageattributedemo&Attribute=entityimage&Id=26f17c6d-7b51-e311-9088-00155d9c5607&Timestamp=635205044343080227</span></span>  
  
   -   <span data-ttu-id="9aa48-134">/Image/download.aspx?Entity=sample_imageattributedemo&Attribute=entityimage&Id=28f17c6d-7b51-e311-9088-00155d9c5607&Timestamp=635205044353421800</span><span class="sxs-lookup"><span data-stu-id="9aa48-134">/Image/download.aspx?Entity=sample_imageattributedemo&Attribute=entityimage&Id=28f17c6d-7b51-e311-9088-00155d9c5607&Timestamp=635205044353421800</span></span>  
  
   <span data-ttu-id="9aa48-135">The `DeleteImageAttributeDemoEntity` method gives you the option to delete the `sample_ImageAttributeDemo` entity and return your organization to state it was before running the sample.</span><span class="sxs-lookup"><span data-stu-id="9aa48-135">The `DeleteImageAttributeDemoEntity` method gives you the option to delete the `sample_ImageAttributeDemo` entity and return your organization to state it was before running the sample.</span></span> <span data-ttu-id="9aa48-136">You can’t run the sample again until you delete this entity.</span><span class="sxs-lookup"><span data-stu-id="9aa48-136">You can’t run the sample again until you delete this entity.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9aa48-137">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="9aa48-137">Example</span></span>  
 <span data-ttu-id="9aa48-138">The following is the full code for the sample.</span><span class="sxs-lookup"><span data-stu-id="9aa48-138">The following is the full code for the sample.</span></span>  
  
 [!code-csharp[DynamicEntity#EntityImages](../snippets/csharp/CRMV8/dynamicentity/cs/entityimages.cs#entityimages)]  
  
### <a name="see-also"></a><span data-ttu-id="9aa48-139">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9aa48-139">See also</span></span>  
 <span data-ttu-id="9aa48-140">[Image Attributes](image-attributes.md) </span><span class="sxs-lookup"><span data-stu-id="9aa48-140">[Image Attributes](image-attributes.md) </span></span>  
 <span data-ttu-id="9aa48-141">[Introduction to entity attributes in Dynamics 365 for Customer Engagement apps](introduction-entity-attributes.md) </span><span class="sxs-lookup"><span data-stu-id="9aa48-141">[Introduction to entity attributes in Dynamics 365 for Customer Engagement apps](introduction-entity-attributes.md) </span></span>  
 [<span data-ttu-id="9aa48-142">Introduction to Entities in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="9aa48-142">Introduction to Entities in Dynamics 365 for Customer Engagement apps</span></span>](introduction-entities.md)
