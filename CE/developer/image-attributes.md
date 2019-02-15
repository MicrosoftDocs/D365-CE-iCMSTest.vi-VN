---
title: Image attributes (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about image attributes that include image data witht in the application, and supporting attributes, Retrieving image data, and Uploading image data.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: accdb615-e378-403f-8fb9-abb882f72d81
caps.latest.revision: 8
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0135f1ae0b7846269434eae6b2c85d2450d2ab0d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388022"
---
# <a name="image-attributes"></a><span data-ttu-id="4fd01-103">Image attributes</span><span class="sxs-lookup"><span data-stu-id="4fd01-103">Image attributes</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4fd01-104">Entity records that include image data provide a unique experience within the application.</span><span class="sxs-lookup"><span data-stu-id="4fd01-104">Entity records that include image data provide a unique experience within the application.</span></span> <span data-ttu-id="4fd01-105">As a developer you need to understand how you work with image data.</span><span class="sxs-lookup"><span data-stu-id="4fd01-105">As a developer you need to understand how you work with image data.</span></span>  
  
 <span data-ttu-id="4fd01-106">Only certain system entities and custom entities support images.</span><span class="sxs-lookup"><span data-stu-id="4fd01-106">Only certain system entities and custom entities support images.</span></span> <span data-ttu-id="4fd01-107">For information about which system entities support images, see [Entity images](introduction-entities.md#BKMK_EntityImages).</span><span class="sxs-lookup"><span data-stu-id="4fd01-107">For information about which system entities support images, see [Entity images](introduction-entities.md#BKMK_EntityImages).</span></span>  
  
<a name="BKMK_SupportingAttributes"></a>   
## <a name="supporting-attributes"></a><span data-ttu-id="4fd01-108">Supporting attributes</span><span class="sxs-lookup"><span data-stu-id="4fd01-108">Supporting attributes</span></span>  
 <span data-ttu-id="4fd01-109">For those entities which support image attributes, the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.SchemaName> of the entity image attribute is always `EntityImage`.</span><span class="sxs-lookup"><span data-stu-id="4fd01-109">For those entities which support image attributes, the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.SchemaName> of the entity image attribute is always `EntityImage`.</span></span> <span data-ttu-id="4fd01-110">When an image attribute is added to an entity some additional attributes are created to support it.</span><span class="sxs-lookup"><span data-stu-id="4fd01-110">When an image attribute is added to an entity some additional attributes are created to support it.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4fd01-111">Clients that do not use the current .NET assemblies need to include <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.SdkClientVersion> with a value of ‘6.0.0.0’ or higher in order to receive <xref:Microsoft.Xrm.Sdk.Metadata.ImageAttributeMetadata> attributes.</span><span class="sxs-lookup"><span data-stu-id="4fd01-111">Clients that do not use the current .NET assemblies need to include <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.SdkClientVersion> with a value of ‘6.0.0.0’ or higher in order to receive <xref:Microsoft.Xrm.Sdk.Metadata.ImageAttributeMetadata> attributes.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="4fd01-112"><xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.SdkClientVersion>.</span><span class="sxs-lookup"><span data-stu-id="4fd01-112"><xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.SdkClientVersion>.</span></span>  
  
### <a name="entityimagetimestamp-attribute"></a><span data-ttu-id="4fd01-113">EntityImage_Timestamp attribute</span><span class="sxs-lookup"><span data-stu-id="4fd01-113">EntityImage_Timestamp attribute</span></span>  
 <span data-ttu-id="4fd01-114">Attribute Type Name:  `BigIntType`</span><span class="sxs-lookup"><span data-stu-id="4fd01-114">Attribute Type Name:  `BigIntType`</span></span>  
  
 <span data-ttu-id="4fd01-115">The value represents when the image was last updated and is used to help make sure that the latest version of the image is downloaded and cached on the client.</span><span class="sxs-lookup"><span data-stu-id="4fd01-115">The value represents when the image was last updated and is used to help make sure that the latest version of the image is downloaded and cached on the client.</span></span>  
  
### <a name="entityimageurl-attribute"></a><span data-ttu-id="4fd01-116">EntityImage_URL attribute</span><span class="sxs-lookup"><span data-stu-id="4fd01-116">EntityImage_URL attribute</span></span>  
 <span data-ttu-id="4fd01-117">Attribute Type Name: `StringType`</span><span class="sxs-lookup"><span data-stu-id="4fd01-117">Attribute Type Name: `StringType`</span></span>  
  
 <span data-ttu-id="4fd01-118">An absolute URL to display the entity image in a client.</span><span class="sxs-lookup"><span data-stu-id="4fd01-118">An absolute URL to display the entity image in a client.</span></span>  
  
 <span data-ttu-id="4fd01-119">The URL is composed this way:</span><span class="sxs-lookup"><span data-stu-id="4fd01-119">The URL is composed this way:</span></span>  
  
```  
{0}/image/download.aspx?entity={1}&attribute={2}&id={3}&timestamp={4}
```  
  
- <span data-ttu-id="4fd01-120">0 : The organization URL</span><span class="sxs-lookup"><span data-stu-id="4fd01-120">0 : The organization URL</span></span>  
  
- <span data-ttu-id="4fd01-121">1 : The entity logical name</span><span class="sxs-lookup"><span data-stu-id="4fd01-121">1 : The entity logical name</span></span>  
  
- <span data-ttu-id="4fd01-122">2 : The attribute logical name</span><span class="sxs-lookup"><span data-stu-id="4fd01-122">2 : The attribute logical name</span></span>  
  
- <span data-ttu-id="4fd01-123">3 : The EntityImageId value.</span><span class="sxs-lookup"><span data-stu-id="4fd01-123">3 : The EntityImageId value.</span></span>  
  
- <span data-ttu-id="4fd01-124">4 : The EntityImage_Timestamp value</span><span class="sxs-lookup"><span data-stu-id="4fd01-124">4 : The EntityImage_Timestamp value</span></span>  
  
  <span data-ttu-id="4fd01-125">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="4fd01-125">For example:</span></span>   
  `https://myorg.crm.dynamics.com/image/download.aspx?attribute=entityimage&entity=contact&id={ECB6D3DF-4A04-E311-AFE0-00155D9C3020}&timestamp=635120312218444444`  
  
### <a name="entityimageid"></a><span data-ttu-id="4fd01-126">EntityImageId</span><span class="sxs-lookup"><span data-stu-id="4fd01-126">EntityImageId</span></span>  
 <span data-ttu-id="4fd01-127">Attribute Type Name: `UniqueIdentifierType`</span><span class="sxs-lookup"><span data-stu-id="4fd01-127">Attribute Type Name: `UniqueIdentifierType`</span></span>  
  
 <span data-ttu-id="4fd01-128">The unique identifier of the image</span><span class="sxs-lookup"><span data-stu-id="4fd01-128">The unique identifier of the image</span></span>  
  
<a name="BKMK_RetrievingImages"></a>   
## <a name="retrieving-image-data"></a><span data-ttu-id="4fd01-129">Retrieving image data</span><span class="sxs-lookup"><span data-stu-id="4fd01-129">Retrieving image data</span></span>  
 <span data-ttu-id="4fd01-130">When you use <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> or <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*> the `EntityImage` is not included when the <xref:Microsoft.Xrm.Sdk.Query.ColumnSet>.`AllColumns`</span><span class="sxs-lookup"><span data-stu-id="4fd01-130">When you use <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> or <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*> the `EntityImage` is not included when the <xref:Microsoft.Xrm.Sdk.Query.ColumnSet>.`AllColumns`</span></span> <span data-ttu-id="4fd01-131">property is set to true.</span><span class="sxs-lookup"><span data-stu-id="4fd01-131">property is set to true.</span></span> <span data-ttu-id="4fd01-132">Because of the potential size of data in this attribute, to return this attribute you must explicitly request it.</span><span class="sxs-lookup"><span data-stu-id="4fd01-132">Because of the potential size of data in this attribute, to return this attribute you must explicitly request it.</span></span>  
  
 <span data-ttu-id="4fd01-133">The binary data representing the image isn’t returned using the deprecated <xref:Microsoft.Crm.Sdk.Messages.ExecuteFetchRequest> class.</span><span class="sxs-lookup"><span data-stu-id="4fd01-133">The binary data representing the image isn’t returned using the deprecated <xref:Microsoft.Crm.Sdk.Messages.ExecuteFetchRequest> class.</span></span> <span data-ttu-id="4fd01-134">You should use <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> instead.</span><span class="sxs-lookup"><span data-stu-id="4fd01-134">You should use <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> instead.</span></span>  
  
 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="4fd01-135">[Sample: Set and retrieve entity images](sample-set-retrieve-entity-images.md).</span><span class="sxs-lookup"><span data-stu-id="4fd01-135">[Sample: Set and retrieve entity images](sample-set-retrieve-entity-images.md).</span></span>  
  
<a name="BKMK_UploadingImages"></a>   
## <a name="uploading-image-data"></a><span data-ttu-id="4fd01-136">Uploading image data</span><span class="sxs-lookup"><span data-stu-id="4fd01-136">Uploading image data</span></span>  
 <span data-ttu-id="4fd01-137">To update images set the value of the `EntityImage` to a `byte[]` that contains the content of the file.</span><span class="sxs-lookup"><span data-stu-id="4fd01-137">To update images set the value of the `EntityImage` to a `byte[]` that contains the content of the file.</span></span> <span data-ttu-id="4fd01-138">All images are displayed in a 144x144 pixel square.</span><span class="sxs-lookup"><span data-stu-id="4fd01-138">All images are displayed in a 144x144 pixel square.</span></span> <span data-ttu-id="4fd01-139">Images will be cropped and resized to reduce the size of the data before being saved.</span><span class="sxs-lookup"><span data-stu-id="4fd01-139">Images will be cropped and resized to reduce the size of the data before being saved.</span></span>  
  
- <span data-ttu-id="4fd01-140">Images with at least one side larger than 144 pixels are cropped on center to 144x144.</span><span class="sxs-lookup"><span data-stu-id="4fd01-140">Images with at least one side larger than 144 pixels are cropped on center to 144x144.</span></span>  
  
- <span data-ttu-id="4fd01-141">Images with both sides smaller than 144 are cropped square to their smallest side.</span><span class="sxs-lookup"><span data-stu-id="4fd01-141">Images with both sides smaller than 144 are cropped square to their smallest side.</span></span>  
  
  <span data-ttu-id="4fd01-142">The following table shows two examples.</span><span class="sxs-lookup"><span data-stu-id="4fd01-142">The following table shows two examples.</span></span>  
  
|<span data-ttu-id="4fd01-143">Before</span><span class="sxs-lookup"><span data-stu-id="4fd01-143">Before</span></span>|<span data-ttu-id="4fd01-144">After</span><span class="sxs-lookup"><span data-stu-id="4fd01-144">After</span></span>|  
|------------|-----------|  
|<span data-ttu-id="4fd01-145">![Image before resize](media/crm-itpro-cust-imagebeforeresize.png "Image before resize")</span><span class="sxs-lookup"><span data-stu-id="4fd01-145">![Image before resize](media/crm-itpro-cust-imagebeforeresize.png "Image before resize")</span></span><br /><br /> <span data-ttu-id="4fd01-146">300x428</span><span class="sxs-lookup"><span data-stu-id="4fd01-146">300x428</span></span>|<span data-ttu-id="4fd01-147">![image after resize](media/crm-itpro-cust-imageafterresize.jpg "image after resize")</span><span class="sxs-lookup"><span data-stu-id="4fd01-147">![image after resize](media/crm-itpro-cust-imageafterresize.jpg "image after resize")</span></span><br /><br /> <span data-ttu-id="4fd01-148">144x144</span><span class="sxs-lookup"><span data-stu-id="4fd01-148">144x144</span></span>|  
|<span data-ttu-id="4fd01-149">![Second image resize example](media/crm-itpro-cust-imagebeforeresizeexample2.png "Second image resize example")</span><span class="sxs-lookup"><span data-stu-id="4fd01-149">![Second image resize example](media/crm-itpro-cust-imagebeforeresizeexample2.png "Second image resize example")</span></span><br /><br /> <span data-ttu-id="4fd01-150">91x130</span><span class="sxs-lookup"><span data-stu-id="4fd01-150">91x130</span></span>|<span data-ttu-id="4fd01-151">![second resize example](media/crm-itpro-cust-imageafterresizeexample2.jpg "second resize example")</span><span class="sxs-lookup"><span data-stu-id="4fd01-151">![second resize example](media/crm-itpro-cust-imageafterresizeexample2.jpg "second resize example")</span></span><br /><br /> <span data-ttu-id="4fd01-152">91x91</span><span class="sxs-lookup"><span data-stu-id="4fd01-152">91x91</span></span>|  
  
 [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="4fd01-153">[Sample: Set and retrieve entity images](sample-set-retrieve-entity-images.md).</span><span class="sxs-lookup"><span data-stu-id="4fd01-153">[Sample: Set and retrieve entity images](sample-set-retrieve-entity-images.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4fd01-154">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4fd01-154">See also</span></span>  
 <span data-ttu-id="4fd01-155">[Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md) </span><span class="sxs-lookup"><span data-stu-id="4fd01-155">[Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md) </span></span>  
 <span data-ttu-id="4fd01-156">[Introduction to entity attributes in Dynamics 365 for Customer Engagement apps](introduction-entity-attributes.md) </span><span class="sxs-lookup"><span data-stu-id="4fd01-156">[Introduction to entity attributes in Dynamics 365 for Customer Engagement apps](introduction-entity-attributes.md) </span></span>  
 [<span data-ttu-id="4fd01-157">Sample: Set and retrieve entity images</span><span class="sxs-lookup"><span data-stu-id="4fd01-157">Sample: Set and retrieve entity images</span></span>](sample-set-retrieve-entity-images.md)
