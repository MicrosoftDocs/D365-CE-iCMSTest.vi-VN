---
title: Web resources for Dynamics 365 for Customer Engagement (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Web resources are virtual files that are stored in the Dynamics 365 for Customer Engagement database and that you can retrieve by using a unique URL address.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8c947e83-6765-41d9-b4b7-c078a68257eb
author: JimDaly
ms.author: jdaly
manager: amyla
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 46
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b7acdfb0311d4d6e8fba155f9ff8811cc4511b8b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387387"
---
# <a name="web-resources-for-customer-engagement"></a><span data-ttu-id="da8c0-103">Web resources for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="da8c0-103">Web resources for Customer Engagement</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="da8c0-104">Web resources are *virtual files* that are stored in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] database and that you can retrieve by using a unique URL address.</span><span class="sxs-lookup"><span data-stu-id="da8c0-104">Web resources are *virtual files* that are stored in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] database and that you can retrieve by using a unique URL address.</span></span>  

<a name="BKMK_CapabilitiesOfWebResources"></a>   
## <a name="capabilities-of-web-resources"></a><span data-ttu-id="da8c0-105">Capabilities of web resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-105">Capabilities of web resources</span></span>  
 <span data-ttu-id="da8c0-106">Web resources represent files that can be used to extend the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application such as html files, [!INCLUDE[pn_JScript](../includes/pn-jscript.md)], and CSS, and several image formats.</span><span class="sxs-lookup"><span data-stu-id="da8c0-106">Web resources represent files that can be used to extend the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application such as html files, [!INCLUDE[pn_JScript](../includes/pn-jscript.md)], and CSS, and several image formats.</span></span> <span data-ttu-id="da8c0-107">You can use web resources in form customizations, the `SiteMap`, or the application ribbon because they can be referenced by using URL syntax.</span><span class="sxs-lookup"><span data-stu-id="da8c0-107">You can use web resources in form customizations, the `SiteMap`, or the application ribbon because they can be referenced by using URL syntax.</span></span>  

 <span data-ttu-id="da8c0-108">The URL syntax for web resources allows for relative path references.</span><span class="sxs-lookup"><span data-stu-id="da8c0-108">The URL syntax for web resources allows for relative path references.</span></span> <span data-ttu-id="da8c0-109">With your development tools, you can create a group of interdependent files on a development server by using file types compatible with web resources.</span><span class="sxs-lookup"><span data-stu-id="da8c0-109">With your development tools, you can create a group of interdependent files on a development server by using file types compatible with web resources.</span></span> <span data-ttu-id="da8c0-110">Then, if you use a consistent naming convention and relative path references, the website will function after you upload all the files into [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="da8c0-110">Then, if you use a consistent naming convention and relative path references, the website will function after you upload all the files into [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)].</span></span>  

 <span data-ttu-id="da8c0-111">Because web resources are stored in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] and are solution components, they can be easily exported and installed to on-premises deployments of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] or to [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="da8c0-111">Because web resources are stored in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] and are solution components, they can be easily exported and installed to on-premises deployments of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] or to [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span></span> <span data-ttu-id="da8c0-112">Web resources are also available to users of [!INCLUDE[pn_crm_outlook_offline_access](../includes/pn-crm-outlook-offline-access.md)] when offline because they are synchronized with the user's data.</span><span class="sxs-lookup"><span data-stu-id="da8c0-112">Web resources are also available to users of [!INCLUDE[pn_crm_outlook_offline_access](../includes/pn-crm-outlook-offline-access.md)] when offline because they are synchronized with the user's data.</span></span>  

 <span data-ttu-id="da8c0-113">You can use the form editor to add and configure form-enabled web resources into your entity forms.</span><span class="sxs-lookup"><span data-stu-id="da8c0-113">You can use the form editor to add and configure form-enabled web resources into your entity forms.</span></span>  

 <span data-ttu-id="da8c0-114">Because web resources are stored as records in the database, they can be managed programmatically by using the standard techniques to create, retrieve, and update records.</span><span class="sxs-lookup"><span data-stu-id="da8c0-114">Because web resources are stored as records in the database, they can be managed programmatically by using the standard techniques to create, retrieve, and update records.</span></span> <span data-ttu-id="da8c0-115">Text-based web resources (JScript, CSS, XML, XSL, RESX, and HTML) can be edited and saved in the application.</span><span class="sxs-lookup"><span data-stu-id="da8c0-115">Text-based web resources (JScript, CSS, XML, XSL, RESX, and HTML) can be edited and saved in the application.</span></span>  

<a name="BKMK_LimitationsOfWebResources"></a>   
### <a name="limitations-of-web-resources"></a><span data-ttu-id="da8c0-116">Limitations of web resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-116">Limitations of web resources</span></span>  
 <span data-ttu-id="da8c0-117">There is no type of web resource that supports the capabilities of an ASP.NET(.aspx) page to execute code on the server.</span><span class="sxs-lookup"><span data-stu-id="da8c0-117">There is no type of web resource that supports the capabilities of an ASP.NET(.aspx) page to execute code on the server.</span></span> <span data-ttu-id="da8c0-118">Web resources are limited to static files or files that are processed in the browser.</span><span class="sxs-lookup"><span data-stu-id="da8c0-118">Web resources are limited to static files or files that are processed in the browser.</span></span> <span data-ttu-id="da8c0-119">A web resource can contain code that is processed in the browser to execute web service calls to interact with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] data.</span><span class="sxs-lookup"><span data-stu-id="da8c0-119">A web resource can contain code that is processed in the browser to execute web service calls to interact with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] data.</span></span> <span data-ttu-id="da8c0-120">For more information, see [Work with Customer Engagement data using web resources](work-data-using-web-resources.md).</span><span class="sxs-lookup"><span data-stu-id="da8c0-120">For more information, see [Work with Customer Engagement data using web resources](work-data-using-web-resources.md).</span></span> 

 <span data-ttu-id="da8c0-121">Web resources are only available by using the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application security context.</span><span class="sxs-lookup"><span data-stu-id="da8c0-121">Web resources are only available by using the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application security context.</span></span> <span data-ttu-id="da8c0-122">Only licensed [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] users who have the necessary privileges can access them.</span><span class="sxs-lookup"><span data-stu-id="da8c0-122">Only licensed [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] users who have the necessary privileges can access them.</span></span>  

#### <a name="size-limitations"></a><span data-ttu-id="da8c0-123">Size limitations</span><span class="sxs-lookup"><span data-stu-id="da8c0-123">Size limitations</span></span>  
[!INCLUDE[sdk_MaxUploadFileSize](../includes/sdk-maxuploadfilesize.md)]

<a name="BKMK_WebResourceTypes"></a>   
## <a name="web-resource-types"></a><span data-ttu-id="da8c0-124">Web resource types</span><span class="sxs-lookup"><span data-stu-id="da8c0-124">Web resource types</span></span>  
 <span data-ttu-id="da8c0-125">You can use ten file formats to create web resources.</span><span class="sxs-lookup"><span data-stu-id="da8c0-125">You can use ten file formats to create web resources.</span></span> <span data-ttu-id="da8c0-126">The following table lists each file format, the allowed file extensions, and the type value that you use for each.</span><span class="sxs-lookup"><span data-stu-id="da8c0-126">The following table lists each file format, the allowed file extensions, and the type value that you use for each.</span></span>  


|                                    <span data-ttu-id="da8c0-127">File</span><span class="sxs-lookup"><span data-stu-id="da8c0-127">File</span></span>                                     | <span data-ttu-id="da8c0-128">File extensions</span><span class="sxs-lookup"><span data-stu-id="da8c0-128">File extensions</span></span> | <span data-ttu-id="da8c0-129">Loại</span><span class="sxs-lookup"><span data-stu-id="da8c0-129">Type</span></span> |
|-----------------------------------------------------------------------------|-----------------|------|
|                               <span data-ttu-id="da8c0-130">Trang web (HTML)</span><span class="sxs-lookup"><span data-stu-id="da8c0-130">Webpage (HTML)</span></span>                                |   <span data-ttu-id="da8c0-131">.htm, .html</span><span class="sxs-lookup"><span data-stu-id="da8c0-131">.htm, .html</span></span>   |  <span data-ttu-id="da8c0-132">1</span><span class="sxs-lookup"><span data-stu-id="da8c0-132">1</span></span>   |
|                              <span data-ttu-id="da8c0-133">Tờ mẫu (CSS)</span><span class="sxs-lookup"><span data-stu-id="da8c0-133">Style Sheet (CSS)</span></span>                              |      <span data-ttu-id="da8c0-134">.css</span><span class="sxs-lookup"><span data-stu-id="da8c0-134">.css</span></span>       |  <span data-ttu-id="da8c0-135">2</span><span class="sxs-lookup"><span data-stu-id="da8c0-135">2</span></span>   |
|                              <span data-ttu-id="da8c0-136">Mã lệnh (JScript)</span><span class="sxs-lookup"><span data-stu-id="da8c0-136">Script (JScript)</span></span>                               |       <span data-ttu-id="da8c0-137">.js</span><span class="sxs-lookup"><span data-stu-id="da8c0-137">.js</span></span>       |  <span data-ttu-id="da8c0-138">3</span><span class="sxs-lookup"><span data-stu-id="da8c0-138">3</span></span>   |
|                                 <span data-ttu-id="da8c0-139">Dữ liệu (XML)</span><span class="sxs-lookup"><span data-stu-id="da8c0-139">Data (XML)</span></span>                                  |      <span data-ttu-id="da8c0-140">.xml</span><span class="sxs-lookup"><span data-stu-id="da8c0-140">.xml</span></span>       |  <span data-ttu-id="da8c0-141">4</span><span class="sxs-lookup"><span data-stu-id="da8c0-141">4</span></span>   |
|                                 <span data-ttu-id="da8c0-142">Hình ảnh (PNG)</span><span class="sxs-lookup"><span data-stu-id="da8c0-142">Image (PNG)</span></span>                                 |      <span data-ttu-id="da8c0-143">.png</span><span class="sxs-lookup"><span data-stu-id="da8c0-143">.png</span></span>       |  <span data-ttu-id="da8c0-144">5</span><span class="sxs-lookup"><span data-stu-id="da8c0-144">5</span></span>   |
|                                 <span data-ttu-id="da8c0-145">Hình ảnh (JPG)</span><span class="sxs-lookup"><span data-stu-id="da8c0-145">Image (JPG)</span></span>                                 |      <span data-ttu-id="da8c0-146">.jpg</span><span class="sxs-lookup"><span data-stu-id="da8c0-146">.jpg</span></span>       |  <span data-ttu-id="da8c0-147">6</span><span class="sxs-lookup"><span data-stu-id="da8c0-147">6</span></span>   |
|                                 <span data-ttu-id="da8c0-148">Hình ảnh (GIF)</span><span class="sxs-lookup"><span data-stu-id="da8c0-148">Image (GIF)</span></span>                                 |      <span data-ttu-id="da8c0-149">.gif</span><span class="sxs-lookup"><span data-stu-id="da8c0-149">.gif</span></span>       |  <span data-ttu-id="da8c0-150">7</span><span class="sxs-lookup"><span data-stu-id="da8c0-150">7</span></span>   |
| [!INCLUDE[pn_Silverlight_short](../includes/pn-silverlight-short.md)] <span data-ttu-id="da8c0-151">(XAP)</span><span class="sxs-lookup"><span data-stu-id="da8c0-151">(XAP)</span></span> |      <span data-ttu-id="da8c0-152">.xap</span><span class="sxs-lookup"><span data-stu-id="da8c0-152">.xap</span></span>       |  <span data-ttu-id="da8c0-153">8</span><span class="sxs-lookup"><span data-stu-id="da8c0-153">8</span></span>   |
|                              <span data-ttu-id="da8c0-154">StyleSheet (XSL)</span><span class="sxs-lookup"><span data-stu-id="da8c0-154">StyleSheet (XSL)</span></span>                               |   <span data-ttu-id="da8c0-155">.xsl, .xslt</span><span class="sxs-lookup"><span data-stu-id="da8c0-155">.xsl, .xslt</span></span>   |  <span data-ttu-id="da8c0-156">9</span><span class="sxs-lookup"><span data-stu-id="da8c0-156">9</span></span>   |
|                                 <span data-ttu-id="da8c0-157">Hình ảnh (ICO)</span><span class="sxs-lookup"><span data-stu-id="da8c0-157">Image (ICO)</span></span>                                 |      <span data-ttu-id="da8c0-158">.ico</span><span class="sxs-lookup"><span data-stu-id="da8c0-158">.ico</span></span>       |  <span data-ttu-id="da8c0-159">10</span><span class="sxs-lookup"><span data-stu-id="da8c0-159">10</span></span>  |
|                             <span data-ttu-id="da8c0-160">Vector format (SVG)</span><span class="sxs-lookup"><span data-stu-id="da8c0-160">Vector format (SVG)</span></span>                             |      <span data-ttu-id="da8c0-161">.svg</span><span class="sxs-lookup"><span data-stu-id="da8c0-161">.svg</span></span>       |  <span data-ttu-id="da8c0-162">11</span><span class="sxs-lookup"><span data-stu-id="da8c0-162">11</span></span>  |
|                                <span data-ttu-id="da8c0-163">String (RESX)</span><span class="sxs-lookup"><span data-stu-id="da8c0-163">String (RESX)</span></span>                                |      <span data-ttu-id="da8c0-164">.resx</span><span class="sxs-lookup"><span data-stu-id="da8c0-164">.resx</span></span>      |  <span data-ttu-id="da8c0-165">12</span><span class="sxs-lookup"><span data-stu-id="da8c0-165">12</span></span>  |

<a name="BKMK_ReferencingWebResources"></a>   
## <a name="reference-web-resources"></a><span data-ttu-id="da8c0-166">Reference web resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-166">Reference web resources</span></span>  
 <span data-ttu-id="da8c0-167">There are several methods that you can use to reference web resources.</span><span class="sxs-lookup"><span data-stu-id="da8c0-167">There are several methods that you can use to reference web resources.</span></span>  

> [!NOTE]
> - <span data-ttu-id="da8c0-168">When possible, use the `$webresource` directive.</span><span class="sxs-lookup"><span data-stu-id="da8c0-168">When possible, use the `$webresource` directive.</span></span> <span data-ttu-id="da8c0-169">Only references that use the `$webresource` directive in the site map or ribbon commands will establish dependencies.</span><span class="sxs-lookup"><span data-stu-id="da8c0-169">Only references that use the `$webresource` directive in the site map or ribbon commands will establish dependencies.</span></span> <span data-ttu-id="da8c0-170">Dependencies are not created when web resources reference each other.</span><span class="sxs-lookup"><span data-stu-id="da8c0-170">Dependencies are not created when web resources reference each other.</span></span>  
>   - [!INCLUDE[sdk_silverlightwebresourcedirective](../includes/sdk-silverlightwebresourcedirective.md)]  

<a name="BKMK_WebResourceDirective"></a>   
### <a name="webresource-directive"></a><span data-ttu-id="da8c0-171">$webresource directive</span><span class="sxs-lookup"><span data-stu-id="da8c0-171">$webresource directive</span></span>  
 <span data-ttu-id="da8c0-172">You should always use the `$webresource` directive when referencing a web resource from a ribbon control or from a `SiteMap` sub area.</span><span class="sxs-lookup"><span data-stu-id="da8c0-172">You should always use the `$webresource` directive when referencing a web resource from a ribbon control or from a `SiteMap` sub area.</span></span> <span data-ttu-id="da8c0-173">Use the `$webresource` directive anywhere the XML allows a URL value.</span><span class="sxs-lookup"><span data-stu-id="da8c0-173">Use the `$webresource` directive anywhere the XML allows a URL value.</span></span> <span data-ttu-id="da8c0-174">The following sample shows how to use it.</span><span class="sxs-lookup"><span data-stu-id="da8c0-174">The following sample shows how to use it.</span></span>  

```xml  
$webresource:<name of Web Resource>  
```  

> [!NOTE]
>  <span data-ttu-id="da8c0-175">When using the `$webresource` directive, [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] will create or update solution dependencies.</span><span class="sxs-lookup"><span data-stu-id="da8c0-175">When using the `$webresource` directive, [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] will create or update solution dependencies.</span></span>  

### <a name="xrmnavigationopenwebresource"></a><span data-ttu-id="da8c0-176">Xrm.Navigation.openWebResource</span><span class="sxs-lookup"><span data-stu-id="da8c0-176">Xrm.Navigation.openWebResource</span></span>  
 <span data-ttu-id="da8c0-177">The Xrm.Navigation.[openWebResource](clientapi/reference/Xrm-Navigation/openWebResource.md) function will open an HTML web resource in a new window with parameters to pass the name of the web resource, any query string data to be passed in the data parameter, and information about height and width of the window.</span><span class="sxs-lookup"><span data-stu-id="da8c0-177">The Xrm.Navigation.[openWebResource](clientapi/reference/Xrm-Navigation/openWebResource.md) function will open an HTML web resource in a new window with parameters to pass the name of the web resource, any query string data to be passed in the data parameter, and information about height and width of the window.</span></span>  

 <span data-ttu-id="da8c0-178">The URL generated includes the unique GUID token so that the cached web resource will be loaded.</span><span class="sxs-lookup"><span data-stu-id="da8c0-178">The URL generated includes the unique GUID token so that the cached web resource will be loaded.</span></span>  

<a name="BKMK_RelativeUrl"></a>   
### <a name="relative-url"></a><span data-ttu-id="da8c0-179">Relative URL</span><span class="sxs-lookup"><span data-stu-id="da8c0-179">Relative URL</span></span>  
 <span data-ttu-id="da8c0-180">When referencing a web resource from areas that do not support using the `$webresource:` directive, a relative URL can be used.</span><span class="sxs-lookup"><span data-stu-id="da8c0-180">When referencing a web resource from areas that do not support using the `$webresource:` directive, a relative URL can be used.</span></span> <span data-ttu-id="da8c0-181">To enable this, we recommend that you use a consistent naming convention for the web resources that reflect a virtual file structure.</span><span class="sxs-lookup"><span data-stu-id="da8c0-181">To enable this, we recommend that you use a consistent naming convention for the web resources that reflect a virtual file structure.</span></span> <span data-ttu-id="da8c0-182">The solution publisher’s customization prefix will always be included as a prefix to the name of the web resource.</span><span class="sxs-lookup"><span data-stu-id="da8c0-182">The solution publisher’s customization prefix will always be included as a prefix to the name of the web resource.</span></span> <span data-ttu-id="da8c0-183">This can represent a virtual ”root” folder for all web resources added by that publisher.</span><span class="sxs-lookup"><span data-stu-id="da8c0-183">This can represent a virtual ”root” folder for all web resources added by that publisher.</span></span> <span data-ttu-id="da8c0-184">You can then use the forward slash character (/) to simulate a folder structure that will be honored by the web server.</span><span class="sxs-lookup"><span data-stu-id="da8c0-184">You can then use the forward slash character (/) to simulate a folder structure that will be honored by the web server.</span></span>  

 <span data-ttu-id="da8c0-185">From another web resource, you should always use relative URLs to reference each other.</span><span class="sxs-lookup"><span data-stu-id="da8c0-185">From another web resource, you should always use relative URLs to reference each other.</span></span> <span data-ttu-id="da8c0-186">For example, for the web page web resource `new_/content/contentpage.htm` to reference the CSS web resource `new_/Styles/styles.css`, create the link as follows:</span><span class="sxs-lookup"><span data-stu-id="da8c0-186">For example, for the web page web resource `new_/content/contentpage.htm` to reference the CSS web resource `new_/Styles/styles.css`, create the link as follows:</span></span>  

```html  
<link rel="stylesheet" type="text/css" href="../styles/styles.css" />  
```  

 <span data-ttu-id="da8c0-187">For the web page web resource `new_/content/contentpage.htm` to open the webpage web resource `isv_/foldername/dialogpage.htm`, create the link as follows:</span><span class="sxs-lookup"><span data-stu-id="da8c0-187">For the web page web resource `new_/content/contentpage.htm` to open the webpage web resource `isv_/foldername/dialogpage.htm`, create the link as follows:</span></span>  

```html  
<a href="../../isv_/foldername/dialogpage.htm">Dialog Page</a>  
```  

> [!NOTE]
>  <span data-ttu-id="da8c0-188">Do not use a relative URL using the WebResources folder as the root path for the URL.</span><span class="sxs-lookup"><span data-stu-id="da8c0-188">Do not use a relative URL using the WebResources folder as the root path for the URL.</span></span> <span data-ttu-id="da8c0-189">For example, do not use this: `/WebResources/<name of web resource>`.</span><span class="sxs-lookup"><span data-stu-id="da8c0-189">For example, do not use this: `/WebResources/<name of web resource>`.</span></span> <span data-ttu-id="da8c0-190">When a user belongs to more than one organization on a server, this path will always refer to the users default organization.</span><span class="sxs-lookup"><span data-stu-id="da8c0-190">When a user belongs to more than one organization on a server, this path will always refer to the users default organization.</span></span> <span data-ttu-id="da8c0-191">If the user is not using their default organization and the expected web resource is not included in the user’s default organization, a “File Not Found” error occurs even though the web resource does occur in the organization the user is currently working in.</span><span class="sxs-lookup"><span data-stu-id="da8c0-191">If the user is not using their default organization and the expected web resource is not included in the user’s default organization, a “File Not Found” error occurs even though the web resource does occur in the organization the user is currently working in.</span></span>  

<a name="BKMK_FullUrl"></a>   
### <a name="full-url"></a><span data-ttu-id="da8c0-192">Full URL</span><span class="sxs-lookup"><span data-stu-id="da8c0-192">Full URL</span></span>  
 <span data-ttu-id="da8c0-193">The following sample shows the style of URL you can use to view web resources.</span><span class="sxs-lookup"><span data-stu-id="da8c0-193">The following sample shows the style of URL you can use to view web resources.</span></span>  

```  
<Microsoft CRM URL>/WebResources/<name of web resource>  
```  

 <span data-ttu-id="da8c0-194">The application will process this URL and return the file that contains the latest version of the web resource.</span><span class="sxs-lookup"><span data-stu-id="da8c0-194">The application will process this URL and return the file that contains the latest version of the web resource.</span></span> <span data-ttu-id="da8c0-195">This URL will look like this:</span><span class="sxs-lookup"><span data-stu-id="da8c0-195">This URL will look like this:</span></span>  

```  
<Microsoft CRM URL>/%7B<version value>%7D/WebResources/<name of web resource>  
```  

 <span data-ttu-id="da8c0-196">The version value is updated when you publish customizations and ensures that the browser uses the latest cached version of the web resource.</span><span class="sxs-lookup"><span data-stu-id="da8c0-196">The version value is updated when you publish customizations and ensures that the browser uses the latest cached version of the web resource.</span></span> <span data-ttu-id="da8c0-197">Because of this, use a relative path to a web resource, the Xrm.Navigation.[openWebResource](clientapi/reference/Xrm-Navigation/openWebResource.md) function, or the [$webresource Directive](web-resources.md#BKMK_WebResourceDirective) (when possible) because the version value will automatically be included.</span><span class="sxs-lookup"><span data-stu-id="da8c0-197">Because of this, use a relative path to a web resource, the Xrm.Navigation.[openWebResource](clientapi/reference/Xrm-Navigation/openWebResource.md) function, or the [$webresource Directive](web-resources.md#BKMK_WebResourceDirective) (when possible) because the version value will automatically be included.</span></span> <span data-ttu-id="da8c0-198">For large web resources there can be significant performance implications if you don’t use the cached version of the file.</span><span class="sxs-lookup"><span data-stu-id="da8c0-198">For large web resources there can be significant performance implications if you don’t use the cached version of the file.</span></span>  

 <span data-ttu-id="da8c0-199">The following sample shows a URL for [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)], where `MyOrganization` is the name of your organization, and `new_/test/test.htm` is the name of the web resource:</span><span class="sxs-lookup"><span data-stu-id="da8c0-199">The following sample shows a URL for [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)], where `MyOrganization` is the name of your organization, and `new_/test/test.htm` is the name of the web resource:</span></span>  

```  
https://MyOrganization.crm.dynamics.com/WebResources/new_/test/test.htm  
```  

> [!NOTE]
>  <span data-ttu-id="da8c0-200">Including the ‘/’ character and a file name extension in the name of the web resource is an optional best practice.</span><span class="sxs-lookup"><span data-stu-id="da8c0-200">Including the ‘/’ character and a file name extension in the name of the web resource is an optional best practice.</span></span>  

 <span data-ttu-id="da8c0-201">The following sample shows a URL for on–premises [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], where `myServer` is the server name:</span><span class="sxs-lookup"><span data-stu-id="da8c0-201">The following sample shows a URL for on–premises [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], where `myServer` is the server name:</span></span>  

```  
http://myServer/MyOrganization/WebResources/new_/test/test.htm  
```  

 <span data-ttu-id="da8c0-202">When you write code to reference a web resource that will need to work for either [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] or on–premises [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], you should use the [getClientUrl](clientapi/reference/Xrm-Utility/getGlobalContext/getClientUrl.md) function.</span><span class="sxs-lookup"><span data-stu-id="da8c0-202">When you write code to reference a web resource that will need to work for either [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] or on–premises [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], you should use the [getClientUrl](clientapi/reference/Xrm-Utility/getGlobalContext/getClientUrl.md) function.</span></span>

## <a name="community-tools"></a><span data-ttu-id="da8c0-203">Các công cụ dành cho cộng đồng</span><span class="sxs-lookup"><span data-stu-id="da8c0-203">Community tools</span></span>

<span data-ttu-id="da8c0-204">**WebResources Manager** is a tool that XrmToolbox community developed for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="da8c0-204">**WebResources Manager** is a tool that XrmToolbox community developed for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement.</span></span> <span data-ttu-id="da8c0-205">Vui lòng xem chủ đề [Công cụ dành cho nhà phát triển](developer-tools.md) về các công cụ được cộng đồng phát triển.</span><span class="sxs-lookup"><span data-stu-id="da8c0-205">Please see the [Developer tools](developer-tools.md) topic for community developed tools.</span></span>

> [!NOTE]
> <span data-ttu-id="da8c0-206">Các công cụ dành cho cộng đồng không phải là sản phẩm của [!include[pn_microsoft_dynamics](../includes/pn-microsoft-dynamics.md)] và không mở rộng hỗ trợ đối với các công cụ dành cho cộng đồng.</span><span class="sxs-lookup"><span data-stu-id="da8c0-206">The community tools are not a product of [!include[pn_microsoft_dynamics](../includes/pn-microsoft-dynamics.md)] and does not extend support to the community tools.</span></span> <span data-ttu-id="da8c0-207">If you have questions pertaining to the tool, please contact the publisher.</span><span class="sxs-lookup"><span data-stu-id="da8c0-207">If you have questions pertaining to the tool, please contact the publisher.</span></span> <span data-ttu-id="da8c0-208">More Information: [XrmToolBox](https://www.xrmtoolbox.com).</span><span class="sxs-lookup"><span data-stu-id="da8c0-208">More Information: [XrmToolBox](https://www.xrmtoolbox.com).</span></span> 

### <a name="see-also"></a><span data-ttu-id="da8c0-209">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="da8c0-209">See also</span></span>  
 [<span data-ttu-id="da8c0-210">Write Client Application Extensions for Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="da8c0-210">Write Client Application Extensions for Dynamics 365 for Customer Engagement</span></span>](extend-client.md)<br />
 [<span data-ttu-id="da8c0-211">Create Accessible Web Resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-211">Create Accessible Web Resources</span></span>](create-accessible-web-resources.md)<br />
 [<span data-ttu-id="da8c0-212">Web Page (HTML) Web Resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-212">Web Page (HTML) Web Resources</span></span>](webpage-html-web-resources.md)<br />
 [<span data-ttu-id="da8c0-213">Silverlight (XAP) Web Resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-213">Silverlight (XAP) Web Resources</span></span>](silverlight-xap-web-resources.md)<br />
 [<span data-ttu-id="da8c0-214">Script (JScript) Web Resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-214">Script (JScript) Web Resources</span></span>](script-jscript-web-resources.md)<br />
 [<span data-ttu-id="da8c0-215">Image Web Resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-215">Image Web Resources</span></span>](image-web-resources.md)<br />
 [<span data-ttu-id="da8c0-216">Stylesheet (XSL) Web Resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-216">Stylesheet (XSL) Web Resources</span></span>](stylesheet-xsl-web-resources.md)<br />
 [<span data-ttu-id="da8c0-217">Data (XML) Web Resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-217">Data (XML) Web Resources</span></span>](data-xml-web-resources.md)<br />
 [<span data-ttu-id="da8c0-218">Style Sheet (CSS) Web Resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-218">Style Sheet (CSS) Web Resources</span></span>](css-web-resources.md)<br />
 [<span data-ttu-id="da8c0-219">Web Resource Messages and Methods</span><span class="sxs-lookup"><span data-stu-id="da8c0-219">Web Resource Messages and Methods</span></span>](webresource-entity-messages-methods.md)<br />
 [<span data-ttu-id="da8c0-220">Sample: Passing Multiple Values to a Web Resource Through the Data Parameter</span><span class="sxs-lookup"><span data-stu-id="da8c0-220">Sample: Passing Multiple Values to a Web Resource Through the Data Parameter</span></span>](sample-pass-multiple-values-web-resource-through-data-parameter.md)<br />
 [<span data-ttu-id="da8c0-221">Sample: Web Resource Utility</span><span class="sxs-lookup"><span data-stu-id="da8c0-221">Sample: Web Resource Utility</span></span>](sample-web-resource-utility.md)<br />
 [<span data-ttu-id="da8c0-222">Sample: Importing Files as Web Resources</span><span class="sxs-lookup"><span data-stu-id="da8c0-222">Sample: Importing Files as Web Resources</span></span>](sample-import-files-web-resources.md)<br />
 [<span data-ttu-id="da8c0-223">Use Web Service Data in Web Resources (REST and SOAP Endpoint)</span><span class="sxs-lookup"><span data-stu-id="da8c0-223">Use Web Service Data in Web Resources (REST and SOAP Endpoint)</span></span>](work-data-using-web-resources.md)<br />
 [<span data-ttu-id="da8c0-224">Streamline web resource development using Fiddler AutoResponder</span><span class="sxs-lookup"><span data-stu-id="da8c0-224">Streamline web resource development using Fiddler AutoResponder</span></span>](streamline-javascript-development-fiddler-autoresponder.md)
