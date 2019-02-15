---
title: Webpage (HTML) web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about using webpage (HTML) web resources to create user interface elements for client extensions.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: bba8645a-a725-4c4d-a393-bab8ca692482
caps.latest.revision: 38
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 751cbef47cb75dbea32fb5926b404eb9f1dc18ca
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387702"
---
# <a name="webpage-html-web-resources"></a><span data-ttu-id="75bff-103">Webpage (HTML) web resources</span><span class="sxs-lookup"><span data-stu-id="75bff-103">Webpage (HTML) web resources</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="75bff-104">Use webpage (HTML) web resources to create user interface elements for client extensions.</span><span class="sxs-lookup"><span data-stu-id="75bff-104">Use webpage (HTML) web resources to create user interface elements for client extensions.</span></span>

<a name="BKMK_Capabilities"></a>

## <a name="capabilities-of-html-web-resources"></a><span data-ttu-id="75bff-105">Capabilities of HTML web resources</span><span class="sxs-lookup"><span data-stu-id="75bff-105">Capabilities of HTML web resources</span></span>

<span data-ttu-id="75bff-106">Because an HTML web resource is just streamed to the user's browser, it can include any content that is rendered on the user's browser.</span><span class="sxs-lookup"><span data-stu-id="75bff-106">Because an HTML web resource is just streamed to the user's browser, it can include any content that is rendered on the user's browser.</span></span>  

<a name="BKMK_Limitations"></a>

## <a name="limitations-of-html-web-resources"></a><span data-ttu-id="75bff-107">Limitations of HTML web resources</span><span class="sxs-lookup"><span data-stu-id="75bff-107">Limitations of HTML web resources</span></span>  

- <span data-ttu-id="75bff-108">An HTML web resource can’t contain any code that must be executed on the server.</span><span class="sxs-lookup"><span data-stu-id="75bff-108">An HTML web resource can’t contain any code that must be executed on the server.</span></span> [!INCLUDE[pn_ASP.NET_short](../includes/pn-asp-net-short.md)] <span data-ttu-id="75bff-109">pages can’t be uploaded as HTML web resources.</span><span class="sxs-lookup"><span data-stu-id="75bff-109">pages can’t be uploaded as HTML web resources.</span></span>

- <span data-ttu-id="75bff-110">HTML web resources can only accept a limited number of query string parameters.</span><span class="sxs-lookup"><span data-stu-id="75bff-110">HTML web resources can only accept a limited number of query string parameters.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="75bff-111">[Pass parameters to HTML web resources](webpage-html-web-resources.md#BKMK_PassingParametersToWebResources)</span><span class="sxs-lookup"><span data-stu-id="75bff-111">[Pass parameters to HTML web resources](webpage-html-web-resources.md#BKMK_PassingParametersToWebResources)</span></span>  

<a name="BKMK_UsingTextEditor"></a>

## <a name="use-the-text-editor-for-html-web-resources"></a><span data-ttu-id="75bff-112">Use the text editor for HTML web resources</span><span class="sxs-lookup"><span data-stu-id="75bff-112">Use the text editor for HTML web resources</span></span>

 <span data-ttu-id="75bff-113">The text editor provided in the web resource form is intended for use with very simple HTML editing.</span><span class="sxs-lookup"><span data-stu-id="75bff-113">The text editor provided in the web resource form is intended for use with very simple HTML editing.</span></span> <span data-ttu-id="75bff-114">For more sophisticated HTML documents, you should edit the code in an external editor and use the **Browse** button to upload the contents of your file.</span><span class="sxs-lookup"><span data-stu-id="75bff-114">For more sophisticated HTML documents, you should edit the code in an external editor and use the **Browse** button to upload the contents of your file.</span></span>

 <span data-ttu-id="75bff-115">For example, a more complex HTML page that requires script to render the contents of the page will begin like the following sample.</span><span class="sxs-lookup"><span data-stu-id="75bff-115">For example, a more complex HTML page that requires script to render the contents of the page will begin like the following sample.</span></span>

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html>
<head>
 <title></title>
 <script src="Script/Script.js" type="text/javascript"></script>
 <link href="CSS/Styles.css" rel="stylesheet" type="text/css" />
</head>
<body onload="SDK.ImportWebResources.showData()">
 <div id="results" />
</body>
</html>
```

 <span data-ttu-id="75bff-116">After the document is opened in the text editor and saved, the HTML will be changed to this.</span><span class="sxs-lookup"><span data-stu-id="75bff-116">After the document is opened in the text editor and saved, the HTML will be changed to this.</span></span>  

```html
<HTML><HEAD><TITLE></TITLE>
<META charset=utf-8></HEAD>
<BODY contentEditable=true onload=SDK.ImportWebResources.showData()>
<SCRIPT type=text/javascript src="Script/Script.js"></SCRIPT>
 <LINK rel=stylesheet type=text/css href="CSS/Styles.css">
<DIV id=results></DIV></BODY></HTML>
```

<a name="BKMK_PreventEditing"></a>

## <a name="prevent-editing-of-web-resources-for-managed-solutions"></a><span data-ttu-id="75bff-117">Prevent editing of web resources for managed solutions</span><span class="sxs-lookup"><span data-stu-id="75bff-117">Prevent editing of web resources for managed solutions</span></span>

 <span data-ttu-id="75bff-118">Because of the capability for the HTML in web resources to be changed by using the text editor, it’s recommended that you use managed properties to set complex HTML web resources as not customizable for managed solutions.</span><span class="sxs-lookup"><span data-stu-id="75bff-118">Because of the capability for the HTML in web resources to be changed by using the text editor, it’s recommended that you use managed properties to set complex HTML web resources as not customizable for managed solutions.</span></span> <span data-ttu-id="75bff-119">When viewing web resources in the solutions window, open the **Managed Properties** dialog box to set the **Customizable** property to `false`.</span><span class="sxs-lookup"><span data-stu-id="75bff-119">When viewing web resources in the solutions window, open the **Managed Properties** dialog box to set the **Customizable** property to `false`.</span></span>  

<a name="BKMK_ReferencingOtherWebResources"></a>

## <a name="reference-other-web-resources-from-an-html-web-resource"></a><span data-ttu-id="75bff-120">Reference other web resources from an HTML web resource</span><span class="sxs-lookup"><span data-stu-id="75bff-120">Reference other web resources from an HTML web resource</span></span>

 <span data-ttu-id="75bff-121">You can create a set of related files outside of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] that use any of the web resource file types.</span><span class="sxs-lookup"><span data-stu-id="75bff-121">You can create a set of related files outside of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] that use any of the web resource file types.</span></span> <span data-ttu-id="75bff-122">If you’re careful to always use relative paths and import each web resource with a consistent naming convention that reflects the folder structure of your website, you’ll find that the HTML web resource will maintain links to related CSS, XML, JScript, image, and [!INCLUDE[pn_Silverlight_short](../includes/pn-silverlight-short.md)] files that have been imported as web resources.</span><span class="sxs-lookup"><span data-stu-id="75bff-122">If you’re careful to always use relative paths and import each web resource with a consistent naming convention that reflects the folder structure of your website, you’ll find that the HTML web resource will maintain links to related CSS, XML, JScript, image, and [!INCLUDE[pn_Silverlight_short](../includes/pn-silverlight-short.md)] files that have been imported as web resources.</span></span>  

 <span data-ttu-id="75bff-123">For example, if you create a web application project that uses the following [folder]/file structure:</span><span class="sxs-lookup"><span data-stu-id="75bff-123">For example, if you create a web application project that uses the following [folder]/file structure:</span></span>  

- <span data-ttu-id="75bff-124">page.htm</span><span class="sxs-lookup"><span data-stu-id="75bff-124">page.htm</span></span>

- <span data-ttu-id="75bff-125">[Styles]</span><span class="sxs-lookup"><span data-stu-id="75bff-125">[Styles]</span></span>

  -   <span data-ttu-id="75bff-126">style.css</span><span class="sxs-lookup"><span data-stu-id="75bff-126">style.css</span></span>

- <span data-ttu-id="75bff-127">[Scripts]</span><span class="sxs-lookup"><span data-stu-id="75bff-127">[Scripts]</span></span> 

  -   <span data-ttu-id="75bff-128">script.js</span><span class="sxs-lookup"><span data-stu-id="75bff-128">script.js</span></span>

  <span data-ttu-id="75bff-129">When you import these files as web resources, you can name where your solution publisher customization prefix is “new” in the following manner:</span><span class="sxs-lookup"><span data-stu-id="75bff-129">When you import these files as web resources, you can name where your solution publisher customization prefix is “new” in the following manner:</span></span>  

- `new_/page.htm`  

- `new_/Styles/style.css`  

- `new_/Scripts/script.js`  

  <span data-ttu-id="75bff-130">When you follow this pattern, your `new_/page.htm` HTML web resource can reference the other files the most common way using relative paths as shown in the following example.</span><span class="sxs-lookup"><span data-stu-id="75bff-130">When you follow this pattern, your `new_/page.htm` HTML web resource can reference the other files the most common way using relative paths as shown in the following example.</span></span>  

```html
<script src="Scripts/script.js" type="text/javascript"></script>
<link href="Styles/style.css" rel="stylesheet" type="text/css" />
```

 <span data-ttu-id="75bff-131">The solution publisher customization prefix becomes a virtual root folder for all the web resources in your solution.</span><span class="sxs-lookup"><span data-stu-id="75bff-131">The solution publisher customization prefix becomes a virtual root folder for all the web resources in your solution.</span></span> <span data-ttu-id="75bff-132">If you change your customization prefix, the relative paths within your HTML web resources won’t be changed.</span><span class="sxs-lookup"><span data-stu-id="75bff-132">If you change your customization prefix, the relative paths within your HTML web resources won’t be changed.</span></span>  

> [!NOTE]
> - <span data-ttu-id="75bff-133">An HTML web resource added to a form can’t use global objects defined by the [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] library loaded in the form.</span><span class="sxs-lookup"><span data-stu-id="75bff-133">An HTML web resource added to a form can’t use global objects defined by the [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] library loaded in the form.</span></span> <span data-ttu-id="75bff-134">An HTML web resource may interact with the `Xrm.Page` or `Xrm.Utility` objects within the form by using `parent.Xrm.Page` or `parent.Xrm.Utility`, but global objects defined by form scripts won’t be accessible using the parent.</span><span class="sxs-lookup"><span data-stu-id="75bff-134">An HTML web resource may interact with the `Xrm.Page` or `Xrm.Utility` objects within the form by using `parent.Xrm.Page` or `parent.Xrm.Utility`, but global objects defined by form scripts won’t be accessible using the parent.</span></span> <span data-ttu-id="75bff-135">You should load any libraries that an HTML web resource needs within the HTML web resource so they’re not dependent on scripts loaded in the form.</span><span class="sxs-lookup"><span data-stu-id="75bff-135">You should load any libraries that an HTML web resource needs within the HTML web resource so they’re not dependent on scripts loaded in the form.</span></span>  
>   - <span data-ttu-id="75bff-136">References included in code between web resources aren’t tracked as solution dependencies.</span><span class="sxs-lookup"><span data-stu-id="75bff-136">References included in code between web resources aren’t tracked as solution dependencies.</span></span>  

 <span data-ttu-id="75bff-137">Because web resources are also downloaded for users of [!INCLUDE[pn_crm_outlook_offline_access](../includes/pn-crm-outlook-offline-access.md)], users will have access to web resource content while they’re working offline.</span><span class="sxs-lookup"><span data-stu-id="75bff-137">Because web resources are also downloaded for users of [!INCLUDE[pn_crm_outlook_offline_access](../includes/pn-crm-outlook-offline-access.md)], users will have access to web resource content while they’re working offline.</span></span>  

<a name="BKMK_PassingParametersToWebResources"></a>

## <a name="pass-parameters-to-html-web-resources"></a><span data-ttu-id="75bff-138">Pass parameters to HTML web resources</span><span class="sxs-lookup"><span data-stu-id="75bff-138">Pass parameters to HTML web resources</span></span>

 <span data-ttu-id="75bff-139">An HTML web resource can accept only the parameters in the following table.</span><span class="sxs-lookup"><span data-stu-id="75bff-139">An HTML web resource can accept only the parameters in the following table.</span></span>


| <span data-ttu-id="75bff-140">Tham số</span><span class="sxs-lookup"><span data-stu-id="75bff-140">Parameter</span></span>  |            <span data-ttu-id="75bff-141">Tên</span><span class="sxs-lookup"><span data-stu-id="75bff-141">Name</span></span>            |                                                                                                               <span data-ttu-id="75bff-142">Mô tả</span><span class="sxs-lookup"><span data-stu-id="75bff-142">Description</span></span>                                                                                                               |
|------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="75bff-143">typename</span><span class="sxs-lookup"><span data-stu-id="75bff-143">typename</span></span>  |        <span data-ttu-id="75bff-144">Tên Thực thể</span><span class="sxs-lookup"><span data-stu-id="75bff-144">Entity Name</span></span>         |                                                                                                         <span data-ttu-id="75bff-145">The name of the entity.</span><span class="sxs-lookup"><span data-stu-id="75bff-145">The name of the entity.</span></span>                                                                                                         |
|    <span data-ttu-id="75bff-146">loại</span><span class="sxs-lookup"><span data-stu-id="75bff-146">type</span></span>    |      <span data-ttu-id="75bff-147">Entity Type Code</span><span class="sxs-lookup"><span data-stu-id="75bff-147">Entity Type Code</span></span>      |                                                                               <span data-ttu-id="75bff-148">An integer that uniquely identifies the entity in a specific organization.</span><span class="sxs-lookup"><span data-stu-id="75bff-148">An integer that uniquely identifies the entity in a specific organization.</span></span>                                                                                |
|     <span data-ttu-id="75bff-149">ID</span><span class="sxs-lookup"><span data-stu-id="75bff-149">id</span></span>     |        <span data-ttu-id="75bff-150">Object GUID</span><span class="sxs-lookup"><span data-stu-id="75bff-150">Object GUID</span></span>         |                                                                                                   <span data-ttu-id="75bff-151">The GUID that represents a record.</span><span class="sxs-lookup"><span data-stu-id="75bff-151">The GUID that represents a record.</span></span>                                                                                                    |
|  <span data-ttu-id="75bff-152">orgname</span><span class="sxs-lookup"><span data-stu-id="75bff-152">orgname</span></span>   |     <span data-ttu-id="75bff-153">Tên tổ chức</span><span class="sxs-lookup"><span data-stu-id="75bff-153">Organization Name</span></span>      |                                                                                                  <span data-ttu-id="75bff-154">The unique name of the organization.</span><span class="sxs-lookup"><span data-stu-id="75bff-154">The unique name of the organization.</span></span>                                                                                                   |
|  <span data-ttu-id="75bff-155">userlcid</span><span class="sxs-lookup"><span data-stu-id="75bff-155">userlcid</span></span>  |     <span data-ttu-id="75bff-156">User Language Code</span><span class="sxs-lookup"><span data-stu-id="75bff-156">User Language Code</span></span>     |                                                                                      <span data-ttu-id="75bff-157">The language code identifier being used by the current user.</span><span class="sxs-lookup"><span data-stu-id="75bff-157">The language code identifier being used by the current user.</span></span>                                                                                       |
|  <span data-ttu-id="75bff-158">orglcid</span><span class="sxs-lookup"><span data-stu-id="75bff-158">orglcid</span></span>   | <span data-ttu-id="75bff-159">Organization Language Code</span><span class="sxs-lookup"><span data-stu-id="75bff-159">Organization Language Code</span></span> |                                                                          <span data-ttu-id="75bff-160">The language code identifier that represents the base language for the organization.</span><span class="sxs-lookup"><span data-stu-id="75bff-160">The language code identifier that represents the base language for the organization.</span></span>                                                                           |
|    <span data-ttu-id="75bff-161">dữ liệu</span><span class="sxs-lookup"><span data-stu-id="75bff-161">data</span></span>    |  <span data-ttu-id="75bff-162">Optional Data Parameter</span><span class="sxs-lookup"><span data-stu-id="75bff-162">Optional Data Parameter</span></span>   |                                                                                                  <span data-ttu-id="75bff-163">An optional value that may be passed.</span><span class="sxs-lookup"><span data-stu-id="75bff-163">An optional value that may be passed.</span></span>                                                                                                  |
|   <span data-ttu-id="75bff-164">formid</span><span class="sxs-lookup"><span data-stu-id="75bff-164">formid</span></span>   |          <span data-ttu-id="75bff-165">Form Id</span><span class="sxs-lookup"><span data-stu-id="75bff-165">Form Id</span></span>           |                                                                                                   <span data-ttu-id="75bff-166">The GUID that represents a form ID.</span><span class="sxs-lookup"><span data-stu-id="75bff-166">The GUID that represents a form ID.</span></span>                                                                                                   |
| <span data-ttu-id="75bff-167">entrypoint</span><span class="sxs-lookup"><span data-stu-id="75bff-167">entrypoint</span></span> |        <span data-ttu-id="75bff-168">Entry Point</span><span class="sxs-lookup"><span data-stu-id="75bff-168">Entry Point</span></span>         | <span data-ttu-id="75bff-169">A string value.</span><span class="sxs-lookup"><span data-stu-id="75bff-169">A string value.</span></span> <span data-ttu-id="75bff-170">This parameter is intended to be passed as an optional value to web resources opened as custom help content for an entity.</span><span class="sxs-lookup"><span data-stu-id="75bff-170">This parameter is intended to be passed as an optional value to web resources opened as custom help content for an entity.</span></span> <span data-ttu-id="75bff-171">When enabled, the custom help URL will include a value of either “form” or “hierarchychart”.</span><span class="sxs-lookup"><span data-stu-id="75bff-171">When enabled, the custom help URL will include a value of either “form” or “hierarchychart”.</span></span> |
|  <span data-ttu-id="75bff-172">pagemode</span><span class="sxs-lookup"><span data-stu-id="75bff-172">pagemode</span></span>  |                            |                                                                                              [!INCLUDE[internal](../includes/internal.md)]                                                                                              |
|  <span data-ttu-id="75bff-173">bảo mật</span><span class="sxs-lookup"><span data-stu-id="75bff-173">security</span></span>  |                            |                                                                                              [!INCLUDE[internal](../includes/internal.md)]                                                                                              |
|   <span data-ttu-id="75bff-174">tabSet</span><span class="sxs-lookup"><span data-stu-id="75bff-174">tabSet</span></span>   |                            |                                                                                              [!INCLUDE[internal](../includes/internal.md)]                                                                                              |

 <span data-ttu-id="75bff-175">To pass more than one value in the data parameter, you must encode parameters in the value of the data parameter and then include logic to decode the multiple parameters using script in your HTML web resource.</span><span class="sxs-lookup"><span data-stu-id="75bff-175">To pass more than one value in the data parameter, you must encode parameters in the value of the data parameter and then include logic to decode the multiple parameters using script in your HTML web resource.</span></span> <span data-ttu-id="75bff-176">The [Sample: Passing Multiple Values to a Web Resource Through the Data Parameter](sample-pass-multiple-values-web-resource-through-data-parameter.md) topic demonstrates one approach to address passing multiple parameter values.</span><span class="sxs-lookup"><span data-stu-id="75bff-176">The [Sample: Passing Multiple Values to a Web Resource Through the Data Parameter](sample-pass-multiple-values-web-resource-through-data-parameter.md) topic demonstrates one approach to address passing multiple parameter values.</span></span>  

### <a name="see-also"></a><span data-ttu-id="75bff-177">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="75bff-177">See also</span></span>

 <span data-ttu-id="75bff-178">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="75bff-178">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span></span>  
 <span data-ttu-id="75bff-179">[Create Accessible Web Resources](create-accessible-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="75bff-179">[Create Accessible Web Resources](create-accessible-web-resources.md) </span></span>  
 <span data-ttu-id="75bff-180">[Using Style Sheet (CSS) Web Resources](css-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="75bff-180">[Using Style Sheet (CSS) Web Resources](css-web-resources.md) </span></span>  
 <span data-ttu-id="75bff-181">[Using Script (JScript) Web Resources](script-jscript-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="75bff-181">[Using Script (JScript) Web Resources](script-jscript-web-resources.md) </span></span>  
 <span data-ttu-id="75bff-182">[Using Data (XML) Web Resources](data-xml-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="75bff-182">[Using Data (XML) Web Resources](data-xml-web-resources.md) </span></span>  
 <span data-ttu-id="75bff-183">[Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="75bff-183">[Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md) </span></span>  
 [<span data-ttu-id="75bff-184">Using Stylesheet (XSL) Web Resources</span><span class="sxs-lookup"><span data-stu-id="75bff-184">Using Stylesheet (XSL) Web Resources</span></span>](stylesheet-xsl-web-resources.md)
