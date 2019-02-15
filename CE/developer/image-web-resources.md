---
title: Image web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Learn about using image web resources to make images available for use in Dynamics 365 for Customer Engagement apps. '
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
- images
- web resource, image
ms.assetid: dfa3f3e2-471e-4295-be47-ab6936189340
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a2d4a93a266ae2702904846d0b9c35e88ea1d8c4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388063"
---
# <a name="image-web-resources"></a><span data-ttu-id="dd54c-103">Image web resources</span><span class="sxs-lookup"><span data-stu-id="dd54c-103">Image web resources</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="dd54c-104">Use image web resources to make images available for use in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="dd54c-104">Use image web resources to make images available for use in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

<span data-ttu-id="dd54c-105">There are 5 types of image web resources:</span><span class="sxs-lookup"><span data-stu-id="dd54c-105">There are 5 types of image web resources:</span></span> 
* <span data-ttu-id="dd54c-106">PNG Format</span><span class="sxs-lookup"><span data-stu-id="dd54c-106">PNG Format</span></span>
* <span data-ttu-id="dd54c-107">JPG Format</span><span class="sxs-lookup"><span data-stu-id="dd54c-107">JPG Format</span></span>
* <span data-ttu-id="dd54c-108">GIF Format</span><span class="sxs-lookup"><span data-stu-id="dd54c-108">GIF Format</span></span>
* <span data-ttu-id="dd54c-109">ICO Format</span><span class="sxs-lookup"><span data-stu-id="dd54c-109">ICO Format</span></span>
* <span data-ttu-id="dd54c-110">Vector Format (SVG)</span><span class="sxs-lookup"><span data-stu-id="dd54c-110">Vector Format (SVG)</span></span>

> [!NOTE]
> <span data-ttu-id="dd54c-111">Vector Format (SVG) web resources were added with the [!INCLUDE[../includes/pn-crm-9-0-0-online.md](../includes/pn-crm-9-0-0-online.md)].</span><span class="sxs-lookup"><span data-stu-id="dd54c-111">Vector Format (SVG) web resources were added with the [!INCLUDE[../includes/pn-crm-9-0-0-online.md](../includes/pn-crm-9-0-0-online.md)].</span></span>

  
<a name="BKMK_Capabilities"></a>   
## <a name="capabilities-of-image-web-resources"></a><span data-ttu-id="dd54c-112">Capabilities of image web resources</span><span class="sxs-lookup"><span data-stu-id="dd54c-112">Capabilities of image web resources</span></span>  
 <span data-ttu-id="dd54c-113">With image web resources you can add images where you need them.</span><span class="sxs-lookup"><span data-stu-id="dd54c-113">With image web resources you can add images where you need them.</span></span> <span data-ttu-id="dd54c-114">Common uses include the following:</span><span class="sxs-lookup"><span data-stu-id="dd54c-114">Common uses include the following:</span></span>  
  
- <span data-ttu-id="dd54c-115">Biểu tượng thực thể tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="dd54c-115">Custom entity icons</span></span>  
- <span data-ttu-id="dd54c-116">Icons for custom Ribbon controls and `SiteMap` subareas</span><span class="sxs-lookup"><span data-stu-id="dd54c-116">Icons for custom Ribbon controls and `SiteMap` subareas</span></span>  
- <span data-ttu-id="dd54c-117">Decorative graphics for entity forms and webpage web resources.</span><span class="sxs-lookup"><span data-stu-id="dd54c-117">Decorative graphics for entity forms and webpage web resources.</span></span>  
- <span data-ttu-id="dd54c-118">Background images that are used by CSS web resources.</span><span class="sxs-lookup"><span data-stu-id="dd54c-118">Background images that are used by CSS web resources.</span></span>  

<span data-ttu-id="dd54c-119">Use Vector Format (SVG) web resources for any icon presented in the application.</span><span class="sxs-lookup"><span data-stu-id="dd54c-119">Use Vector Format (SVG) web resources for any icon presented in the application.</span></span> <span data-ttu-id="dd54c-120">Hình ảnh véc-tơ được định nghĩa là Đồ họa Véc tơ Có thể thay đổi quy mô (SVG), một định dạng hình ảnh véc-tơ dựa trên XML.</span><span class="sxs-lookup"><span data-stu-id="dd54c-120">Vector images are defined as Scalable Vector Graphics (SVG) an XML-based vector image format.</span></span> <span data-ttu-id="dd54c-121">So với các tài nguyên web hình ảnh khác, hình ảnh véc-tơ có lợi thế đó là khả năng mở rộng.</span><span class="sxs-lookup"><span data-stu-id="dd54c-121">The advantage of vector images over other image web resources is that they scale.</span></span> <span data-ttu-id="dd54c-122">Bạn có thể xác định một hình ảnh véc-tơ và tái sử dụng nó, chứ không phải cung cấp nhiều kích cỡ hình ảnh.</span><span class="sxs-lookup"><span data-stu-id="dd54c-122">You can define one vector image and re-use it rather than provide multiple sizes of images.</span></span> <span data-ttu-id="dd54c-123">You will use these in with a new <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IconVectorName></span><span class="sxs-lookup"><span data-stu-id="dd54c-123">You will use these in with a new <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IconVectorName></span></span> <span data-ttu-id="dd54c-124">property to define the icon for a custom entity instead of the `IconLargeName`, `IconMediumName`, or `IconSmallName` properties.</span><span class="sxs-lookup"><span data-stu-id="dd54c-124">property to define the icon for a custom entity instead of the `IconLargeName`, `IconMediumName`, or `IconSmallName` properties.</span></span>
  
<a name="BKMK_Limitations"></a>   
## <a name="limitations-of-image-web-resources"></a><span data-ttu-id="dd54c-125">Limitations of image web resources</span><span class="sxs-lookup"><span data-stu-id="dd54c-125">Limitations of image web resources</span></span>  
 <span data-ttu-id="dd54c-126">Like all web resources, image web resources use the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] security context.</span><span class="sxs-lookup"><span data-stu-id="dd54c-126">Like all web resources, image web resources use the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] security context.</span></span> <span data-ttu-id="dd54c-127">Only licensed [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] users who have the necessary privileges can access them.</span><span class="sxs-lookup"><span data-stu-id="dd54c-127">Only licensed [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] users who have the necessary privileges can access them.</span></span>  
 
  
<a name="BKMK_ReferenceFromWebPageWebResource"></a>   
## <a name="reference-an-image-web-resource-from-a-webpage-web-resource"></a><span data-ttu-id="dd54c-128">Reference an image web resource from a webpage web resource</span><span class="sxs-lookup"><span data-stu-id="dd54c-128">Reference an image web resource from a webpage web resource</span></span>  
 <span data-ttu-id="dd54c-129">All web resources can use relative URLs to reference each other.</span><span class="sxs-lookup"><span data-stu-id="dd54c-129">All web resources can use relative URLs to reference each other.</span></span> <span data-ttu-id="dd54c-130">In the following example, for the webpage (HTML) web resource new_/content/contentpage.htm to reference the image web resource new_/Images/image1.png, add the following HTML code to new_/content/contentpage.htm:</span><span class="sxs-lookup"><span data-stu-id="dd54c-130">In the following example, for the webpage (HTML) web resource new_/content/contentpage.htm to reference the image web resource new_/Images/image1.png, add the following HTML code to new_/content/contentpage.htm:</span></span>  
  
```html  
<img src="../Images/image1.png" />  
```  
  
<a name="BKMK_ReferenceFromForm"></a>   
## <a name="reference-an-image-web-resource-from-a-dynamics-365-for-customer-engagement-apps-form"></a><span data-ttu-id="dd54c-131">Reference an image web resource from a Dynamics 365 for Customer Engagement apps form</span><span class="sxs-lookup"><span data-stu-id="dd54c-131">Reference an image web resource from a Dynamics 365 for Customer Engagement apps form</span></span>  
  
#### <a name="add-an-image-to-an-entity-form"></a><span data-ttu-id="dd54c-132">Add an image to an entity form</span><span class="sxs-lookup"><span data-stu-id="dd54c-132">Add an image to an entity form</span></span>  
  
1.  <span data-ttu-id="dd54c-133">Navigate to the form editor for an entity.</span><span class="sxs-lookup"><span data-stu-id="dd54c-133">Navigate to the form editor for an entity.</span></span>  
  
2.  <span data-ttu-id="dd54c-134">Select where you want to add the image in the form.</span><span class="sxs-lookup"><span data-stu-id="dd54c-134">Select where you want to add the image in the form.</span></span>  
  
3.  <span data-ttu-id="dd54c-135">On the **Insert tab**, click **Web Resource**.</span><span class="sxs-lookup"><span data-stu-id="dd54c-135">On the **Insert tab**, click **Web Resource**.</span></span>  
  
4.  <span data-ttu-id="dd54c-136">On the **General** tab, select the web resource image that you want to add.</span><span class="sxs-lookup"><span data-stu-id="dd54c-136">On the **General** tab, select the web resource image that you want to add.</span></span>  
  
5.  <span data-ttu-id="dd54c-137">Specify a name for the web resource.</span><span class="sxs-lookup"><span data-stu-id="dd54c-137">Specify a name for the web resource.</span></span> <span data-ttu-id="dd54c-138">You can also specify a label and alternative text.</span><span class="sxs-lookup"><span data-stu-id="dd54c-138">You can also specify a label and alternative text.</span></span>  
  
6.  <span data-ttu-id="dd54c-139">On the **Formatting** tab, you can define:</span><span class="sxs-lookup"><span data-stu-id="dd54c-139">On the **Formatting** tab, you can define:</span></span>  
  
    -   <span data-ttu-id="dd54c-140">The number of columns the images should use.</span><span class="sxs-lookup"><span data-stu-id="dd54c-140">The number of columns the images should use.</span></span>  
  
    -   <span data-ttu-id="dd54c-141">The number of rows the images should use, or if it should automatically expand to use available space.</span><span class="sxs-lookup"><span data-stu-id="dd54c-141">The number of rows the images should use, or if it should automatically expand to use available space.</span></span>  
  
    -   <span data-ttu-id="dd54c-142">The size of the image using the following options:</span><span class="sxs-lookup"><span data-stu-id="dd54c-142">The size of the image using the following options:</span></span>  
  
        - <span data-ttu-id="dd54c-143">**Stretch to fit**</span><span class="sxs-lookup"><span data-stu-id="dd54c-143">**Stretch to fit**</span></span>  
  
        - <span data-ttu-id="dd54c-144">**Stretch to fit (maintain aspect ratio)**</span><span class="sxs-lookup"><span data-stu-id="dd54c-144">**Stretch to fit (maintain aspect ratio)**</span></span>  
  
        - <span data-ttu-id="dd54c-145">**Original**</span><span class="sxs-lookup"><span data-stu-id="dd54c-145">**Original**</span></span>  
  
        - <span data-ttu-id="dd54c-146">**Specific**</span><span class="sxs-lookup"><span data-stu-id="dd54c-146">**Specific**</span></span>  
  
    -   <span data-ttu-id="dd54c-147">If you select “Specific,” you can enter the desired height and width in pixels.</span><span class="sxs-lookup"><span data-stu-id="dd54c-147">If you select “Specific,” you can enter the desired height and width in pixels.</span></span>  
  
7.  <span data-ttu-id="dd54c-148">Bấm **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd54c-148">Click **OK**.</span></span>  
  
8.  <span data-ttu-id="dd54c-149">You must save your changes and publish the form before users can see the image in the form.</span><span class="sxs-lookup"><span data-stu-id="dd54c-149">You must save your changes and publish the form before users can see the image in the form.</span></span>  
  
<a name="BKMK_ReferenceWithWebResourcedirective"></a>   
## <a name="reference-an-image-web-resource-from-a-ribbon-element-or-from-the-site-map-subarea"></a><span data-ttu-id="dd54c-150">Reference an image web resource from a ribbon element or from the Site Map subarea</span><span class="sxs-lookup"><span data-stu-id="dd54c-150">Reference an image web resource from a ribbon element or from the Site Map subarea</span></span>  
 <span data-ttu-id="dd54c-151">Use the `$webresource:` directive to specify a web resource image to use as an icon in the ribbon or in the application navigation using Site Map.</span><span class="sxs-lookup"><span data-stu-id="dd54c-151">Use the `$webresource:` directive to specify a web resource image to use as an icon in the ribbon or in the application navigation using Site Map.</span></span> <span data-ttu-id="dd54c-152">The following sample shows how to specify icons for a button in the ribbon.</span><span class="sxs-lookup"><span data-stu-id="dd54c-152">The following sample shows how to specify icons for a button in the ribbon.</span></span>  
  
```xml  
<Button Id="MyISV.opportunity.form.actions.FlyoutAnchor.Button.1" Image16by16="$webresource:new_/icons/oneIcon16.png" Image32by32="$webresource:new_/icons/oneIcon32.png"/>  
```  
  
> [!NOTE]
>  <span data-ttu-id="dd54c-153">Using the `$webresource:` directive adds a solution dependency that prevents the referenced image web resources from being deleted as long as they are used by another solution component.</span><span class="sxs-lookup"><span data-stu-id="dd54c-153">Using the `$webresource:` directive adds a solution dependency that prevents the referenced image web resources from being deleted as long as they are used by another solution component.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="dd54c-154">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="dd54c-154">See also</span></span>  
 <span data-ttu-id="dd54c-155">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="dd54c-155">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span></span>  
 <span data-ttu-id="dd54c-156">[Using Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="dd54c-156">[Using Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span></span>  
 <span data-ttu-id="dd54c-157">[Using Style Sheet (CSS) Web Resources](css-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="dd54c-157">[Using Style Sheet (CSS) Web Resources](css-web-resources.md) </span></span>  
 <span data-ttu-id="dd54c-158">[Using Script (JScript) Web Resources](script-jscript-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="dd54c-158">[Using Script (JScript) Web Resources](script-jscript-web-resources.md) </span></span>  
 <span data-ttu-id="dd54c-159">[Using Data (XML) Web Resources](data-xml-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="dd54c-159">[Using Data (XML) Web Resources](data-xml-web-resources.md) </span></span>  
 <span data-ttu-id="dd54c-160">[Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="dd54c-160">[Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md) </span></span>  
 [<span data-ttu-id="dd54c-161">Using Stylesheet (XSL) Web Resources</span><span class="sxs-lookup"><span data-stu-id="dd54c-161">Using Stylesheet (XSL) Web Resources</span></span>](stylesheet-xsl-web-resources.md)
