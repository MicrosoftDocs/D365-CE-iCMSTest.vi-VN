---
title: Use IFRAME and web resource controls on a form | MicrosoftDocs
ms.custom: ''
ms.date: 04/18/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 1d1b53cb-bfee-4fba-9bea-ea9e6e31309d
author: JimDaly
ms.author: jdaly
manager: faisalmo
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 10c752e27312254691334b870523b96ca5b85e5e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387574"
---
# <a name="use-iframe-and-web-resource-controls-on-a-form"></a><span data-ttu-id="81e37-102">Use IFRAME and web resource controls on a form</span><span class="sxs-lookup"><span data-stu-id="81e37-102">Use IFRAME and web resource controls on a form</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="81e37-103">IFRAME and web resource controls embed content from another location in pages by using an HTML IFRAME element.</span><span class="sxs-lookup"><span data-stu-id="81e37-103">IFRAME and web resource controls embed content from another location in pages by using an HTML IFRAME element.</span></span>  

> [!NOTE]
>  <span data-ttu-id="81e37-104">The designs you choose for the form are also used for the [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)] reading pane and forms used by [!INCLUDE[pn_moca_full](../includes/pn-moca-full.md)].</span><span class="sxs-lookup"><span data-stu-id="81e37-104">The designs you choose for the form are also used for the [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)] reading pane and forms used by [!INCLUDE[pn_moca_full](../includes/pn-moca-full.md)].</span></span> <span data-ttu-id="81e37-105">Web resources and IFRAMEs aren’t displayed using the [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] reading pane, however, they are supported in [!INCLUDE[pn_moca_short](../includes/pn-moca-short.md)].</span><span class="sxs-lookup"><span data-stu-id="81e37-105">Web resources and IFRAMEs aren’t displayed using the [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] reading pane, however, they are supported in [!INCLUDE[pn_moca_short](../includes/pn-moca-short.md)].</span></span> <span data-ttu-id="81e37-106">If your IFRAME depends on access to the `Xrm` object of the page or any form event handlers, you should configure the IFRAME so that it's not visible by default.</span><span class="sxs-lookup"><span data-stu-id="81e37-106">If your IFRAME depends on access to the `Xrm` object of the page or any form event handlers, you should configure the IFRAME so that it's not visible by default.</span></span>  

 <span data-ttu-id="81e37-107">You can use an IFRAME to display the contents from another website in a form, for example, in an [!INCLUDE[pn_ASP.NET_short](../includes/pn-asp-net-short.md)] page.</span><span class="sxs-lookup"><span data-stu-id="81e37-107">You can use an IFRAME to display the contents from another website in a form, for example, in an [!INCLUDE[pn_ASP.NET_short](../includes/pn-asp-net-short.md)] page.</span></span> <span data-ttu-id="81e37-108">Displaying an entity form within an IFrame embedded in another entity form is not supported.</span><span class="sxs-lookup"><span data-stu-id="81e37-108">Displaying an entity form within an IFrame embedded in another entity form is not supported.</span></span>  

 <span data-ttu-id="81e37-109">You can use one of the following web resources to display the contents of web resources in a form:</span><span class="sxs-lookup"><span data-stu-id="81e37-109">You can use one of the following web resources to display the contents of web resources in a form:</span></span>  

-   [<span data-ttu-id="81e37-110">Web Page (HTML) Web Resources</span><span class="sxs-lookup"><span data-stu-id="81e37-110">Web Page (HTML) Web Resources</span></span>](webpage-html-web-resources.md)  

-   [<span data-ttu-id="81e37-111">Silverlight (XAP) Web Resources</span><span class="sxs-lookup"><span data-stu-id="81e37-111">Silverlight (XAP) Web Resources</span></span>](silverlight-xap-web-resources.md)  

-   [<span data-ttu-id="81e37-112">Image (JPG, PNG, GIF, ICO) Web Resources</span><span class="sxs-lookup"><span data-stu-id="81e37-112">Image (JPG, PNG, GIF, ICO) Web Resources</span></span>](image-web-resources.md)  

> [!NOTE]
> [!INCLUDE[pn_Silverlight_short](../includes/pn-silverlight-short.md)] <span data-ttu-id="81e37-113">is included for backward compatibility only and is not recommended.</span><span class="sxs-lookup"><span data-stu-id="81e37-113">is included for backward compatibility only and is not recommended.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)]<span data-ttu-id="81e37-114">[Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md)</span><span class="sxs-lookup"><span data-stu-id="81e37-114">[Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md)</span></span>  

 <span data-ttu-id="81e37-115">The following sections describe your options if you want these controls to show more than static content.</span><span class="sxs-lookup"><span data-stu-id="81e37-115">The following sections describe your options if you want these controls to show more than static content.</span></span>  

<a name="BKMK_IframeSecurity"></a>   
## <a name="select-whether-to-restrict-cross-frame-scripting"></a><span data-ttu-id="81e37-116"> Chọn xem có hạn chế gửi mã lệnh trên khung không</span><span class="sxs-lookup"><span data-stu-id="81e37-116">Select whether to restrict cross-frame scripting</span></span>  
 <span data-ttu-id="81e37-117">Use the **Restrict cross-frame scripting, where supported** option when you don’t fully trust the content displayed in an IFRAME.</span><span class="sxs-lookup"><span data-stu-id="81e37-117">Use the **Restrict cross-frame scripting, where supported** option when you don’t fully trust the content displayed in an IFRAME.</span></span> <span data-ttu-id="81e37-118">When this option is selected, the IFRAME has the attributes set that are listed in the following table.</span><span class="sxs-lookup"><span data-stu-id="81e37-118">When this option is selected, the IFRAME has the attributes set that are listed in the following table.</span></span>  


|        <span data-ttu-id="81e37-119">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="81e37-119">Attribute</span></span>        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        <span data-ttu-id="81e37-120">Mô tả</span><span class="sxs-lookup"><span data-stu-id="81e37-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `security="restricted"` |                                                                                                                                                                                                                                                                                                    <span data-ttu-id="81e37-121">This attribute is supported only by versions of [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] no earlier than version 6.</span><span class="sxs-lookup"><span data-stu-id="81e37-121">This attribute is supported only by versions of [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] no earlier than version 6.</span></span> <span data-ttu-id="81e37-122">The security attribute applies the user security setting Restricted Sites to the source file of the IFRAME.</span><span class="sxs-lookup"><span data-stu-id="81e37-122">The security attribute applies the user security setting Restricted Sites to the source file of the IFRAME.</span></span> <span data-ttu-id="81e37-123">(Zone settings are found on the **Security** tab of the **Internet Options** dialog box.) By default, scripting isn’t enabled in the Restricted Sites zone.</span><span class="sxs-lookup"><span data-stu-id="81e37-123">(Zone settings are found on the **Security** tab of the **Internet Options** dialog box.) By default, scripting isn’t enabled in the Restricted Sites zone.</span></span> <span data-ttu-id="81e37-124">By changing the security settings of the zone, various negative results can occur, including allowing scripts to run.</span><span class="sxs-lookup"><span data-stu-id="81e37-124">By changing the security settings of the zone, various negative results can occur, including allowing scripts to run.</span></span> <span data-ttu-id="81e37-125">For more information, see [security attribute](https://msdn.microsoft.com/library/ie/ms534622.aspx).</span><span class="sxs-lookup"><span data-stu-id="81e37-125">For more information, see [security attribute](https://msdn.microsoft.com/library/ie/ms534622.aspx).</span></span>                                                                                                                                                                                                                                                                                                     |
|      `sandbox=""`       | <span data-ttu-id="81e37-126">For browsers that support this attribute, the content in the IFRAME is essentially limited to only displaying information.</span><span class="sxs-lookup"><span data-stu-id="81e37-126">For browsers that support this attribute, the content in the IFRAME is essentially limited to only displaying information.</span></span> <span data-ttu-id="81e37-127">The following restrictions could be applied:</span><span class="sxs-lookup"><span data-stu-id="81e37-127">The following restrictions could be applied:</span></span><br /><br /> <span data-ttu-id="81e37-128">-   Browser plug-ins are disabled.</span><span class="sxs-lookup"><span data-stu-id="81e37-128">-   Browser plug-ins are disabled.</span></span><br /><span data-ttu-id="81e37-129">-   Forms and scripts are disabled.</span><span class="sxs-lookup"><span data-stu-id="81e37-129">-   Forms and scripts are disabled.</span></span><br /><span data-ttu-id="81e37-130">-   Links to other browsing contexts are disabled.</span><span class="sxs-lookup"><span data-stu-id="81e37-130">-   Links to other browsing contexts are disabled.</span></span><br /><span data-ttu-id="81e37-131">-   Content is treated as from a different domain even if the domain is the same.</span><span class="sxs-lookup"><span data-stu-id="81e37-131">-   Content is treated as from a different domain even if the domain is the same.</span></span><br /><br /> <span data-ttu-id="81e37-132">This attribute is defined by W3C and is supported by the following browsers:</span><span class="sxs-lookup"><span data-stu-id="81e37-132">This attribute is defined by W3C and is supported by the following browsers:</span></span><br /><br /> <span data-ttu-id="81e37-133">- [!INCLUDE[pn_IE_10](../includes/pn-ie-10.md)], [!INCLUDE[pn_ie_11](../includes/pn-ie-11.md)], và [!INCLUDE[pn_microsoft_edge](../includes/pn-microsoft-edge.md)]</span><span class="sxs-lookup"><span data-stu-id="81e37-133">- [!INCLUDE[pn_IE_10](../includes/pn-ie-10.md)], [!INCLUDE[pn_ie_11](../includes/pn-ie-11.md)], and [!INCLUDE[pn_microsoft_edge](../includes/pn-microsoft-edge.md)]</span></span><br />- [!INCLUDE[tn_Google_Chrome](../includes/tn-google-chrome.md)]<br />- [!INCLUDE[tn_Apple_Safari](../includes/tn-apple-safari.md)]<br />- [!INCLUDE[tn_Mozilla_Firefox](../includes/tn-mozilla-firefox.md)]<br /><br /> <span data-ttu-id="81e37-134">For more information about the sandbox attribute see:</span><span class="sxs-lookup"><span data-stu-id="81e37-134">For more information about the sandbox attribute see:</span></span><br /><br /> <span data-ttu-id="81e37-135">-   [How to Safeguard your Site with HTML5 Sandbox](https://msdn.microsoft.com/hh563496)</span><span class="sxs-lookup"><span data-stu-id="81e37-135">-   [How to Safeguard your Site with HTML5 Sandbox](https://msdn.microsoft.com/hh563496)</span></span><br /><span data-ttu-id="81e37-136">-   [WC3 Sandbox attribute](http://dev.w3.org/html5/spec-author-view/the-iframe-element.html)</span><span class="sxs-lookup"><span data-stu-id="81e37-136">-   [WC3 Sandbox attribute](http://dev.w3.org/html5/spec-author-view/the-iframe-element.html)</span></span><br /><span data-ttu-id="81e37-137">-   [Sandbox](https://msdn.microsoft.com/library/ie/hh673561.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e37-137">-   [Sandbox](https://msdn.microsoft.com/library/ie/hh673561.aspx)</span></span> |

<a name="BKMK_EnableIFrameCommunicationAccrossDomains"></a>   

### <a name="enabling-iframe-communication-across-domains"></a><span data-ttu-id="81e37-138">Enabling IFrame communication across domains</span><span class="sxs-lookup"><span data-stu-id="81e37-138">Enabling IFrame communication across domains</span></span>  
 <span data-ttu-id="81e37-139">There are times when you want to enable communication for an IFRAME that contains content on a different domain.</span><span class="sxs-lookup"><span data-stu-id="81e37-139">There are times when you want to enable communication for an IFRAME that contains content on a different domain.</span></span> <span data-ttu-id="81e37-140">`Window.postMessage` is a browser method that provides this capability for versions of [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] no earlier than [!INCLUDE[pn_IE_8](../includes/pn-ie-8.md)].</span><span class="sxs-lookup"><span data-stu-id="81e37-140">`Window.postMessage` is a browser method that provides this capability for versions of [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] no earlier than [!INCLUDE[pn_IE_8](../includes/pn-ie-8.md)].</span></span> [!INCLUDE[tn_Google_Chrome](../includes/tn-google-chrome.md)]<span data-ttu-id="81e37-141">, [!INCLUDE[tn_Mozilla_Firefox](../includes/tn-mozilla-firefox.md)], and [!INCLUDE[tn_Apple_Safari](../includes/tn-apple-safari.md)] also support it.</span><span class="sxs-lookup"><span data-stu-id="81e37-141">, [!INCLUDE[tn_Mozilla_Firefox](../includes/tn-mozilla-firefox.md)], and [!INCLUDE[tn_Apple_Safari](../includes/tn-apple-safari.md)] also support it.</span></span> <span data-ttu-id="81e37-142">For more information about using `postMessage`, see the following blog posts:</span><span class="sxs-lookup"><span data-stu-id="81e37-142">For more information about using `postMessage`, see the following blog posts:</span></span>  

-   [<span data-ttu-id="81e37-143">Cross domain calls to the parent CRM 2011 form</span><span class="sxs-lookup"><span data-stu-id="81e37-143">Cross domain calls to the parent CRM 2011 form</span></span>](http://blogs.msdn.com/b/devkeydet/archive/2012/02/14/cross-domain-calls-to-the-parent-crm-2011-form.aspx)  

-   [<span data-ttu-id="81e37-144">Cross-Document Messaging and RPC</span><span class="sxs-lookup"><span data-stu-id="81e37-144">Cross-Document Messaging and RPC</span></span>](https://msdn.microsoft.com/magazine/ff800814.aspx)  

<a name="BKMK_PassContextualInformation"></a>   

## <a name="pass-contextual-information-about-the-record"></a><span data-ttu-id="81e37-145">Pass contextual information about the record</span><span class="sxs-lookup"><span data-stu-id="81e37-145">Pass contextual information about the record</span></span>  
 <span data-ttu-id="81e37-146">You can provide contextual information by passing parameters to the URL defined in the control.</span><span class="sxs-lookup"><span data-stu-id="81e37-146">You can provide contextual information by passing parameters to the URL defined in the control.</span></span> <span data-ttu-id="81e37-147">The page that is displayed in the frame must be able to process parameters passed to it.</span><span class="sxs-lookup"><span data-stu-id="81e37-147">The page that is displayed in the frame must be able to process parameters passed to it.</span></span> <span data-ttu-id="81e37-148">All the parameters in the following table are passed if the IFRAME or web resource is configured by using the **Pass record object-type code and unique identifier as parameters** option.</span><span class="sxs-lookup"><span data-stu-id="81e37-148">All the parameters in the following table are passed if the IFRAME or web resource is configured by using the **Pass record object-type code and unique identifier as parameters** option.</span></span>  

 <span data-ttu-id="81e37-149">You can specify whether all the parameters in the following table will be passed.</span><span class="sxs-lookup"><span data-stu-id="81e37-149">You can specify whether all the parameters in the following table will be passed.</span></span>  


| <span data-ttu-id="81e37-150">Tham số</span><span class="sxs-lookup"><span data-stu-id="81e37-150">Parameter</span></span>  |        <span data-ttu-id="81e37-151">Tên</span><span class="sxs-lookup"><span data-stu-id="81e37-151">Name</span></span>        |                                 <span data-ttu-id="81e37-152">Mô tả</span><span class="sxs-lookup"><span data-stu-id="81e37-152">Description</span></span>                                 |
|------------|--------------------|-----------------------------------------------------------------------------|
| `typename` |    <span data-ttu-id="81e37-153">Tên Thực thể</span><span class="sxs-lookup"><span data-stu-id="81e37-153">Entity Name</span></span>     |                           <span data-ttu-id="81e37-154">Tên thực thể.</span><span class="sxs-lookup"><span data-stu-id="81e37-154">The name of the entity.</span></span>                           |
|   `type`   |  <span data-ttu-id="81e37-155">Entity Type Code</span><span class="sxs-lookup"><span data-stu-id="81e37-155">Entity Type Code</span></span>  | <span data-ttu-id="81e37-156">The integer that uniquely identifies the entity in a specific organization.</span><span class="sxs-lookup"><span data-stu-id="81e37-156">The integer that uniquely identifies the entity in a specific organization.</span></span> |
|    `id`    |    <span data-ttu-id="81e37-157">Object GUID</span><span class="sxs-lookup"><span data-stu-id="81e37-157">Object GUID</span></span>     |                      <span data-ttu-id="81e37-158">A GUID that represents a record.</span><span class="sxs-lookup"><span data-stu-id="81e37-158">A GUID that represents a record.</span></span>                       |
| `orgname`  | <span data-ttu-id="81e37-159">Tên tổ chức</span><span class="sxs-lookup"><span data-stu-id="81e37-159">Organization Name</span></span>  |                    <span data-ttu-id="81e37-160">The unique name of the organization.</span><span class="sxs-lookup"><span data-stu-id="81e37-160">The unique name of the organization.</span></span>                     |
| `userlcid` | <span data-ttu-id="81e37-161">User Language Code</span><span class="sxs-lookup"><span data-stu-id="81e37-161">User Language Code</span></span> |    <span data-ttu-id="81e37-162">The language code identifier that is being used by the current user.</span><span class="sxs-lookup"><span data-stu-id="81e37-162">The language code identifier that is being used by the current user.</span></span>     |

 [!INCLUDE[languagecode](../includes/languagecode.md)]  

> [!NOTE]
>  <span data-ttu-id="81e37-163">We suggest that you use the entity name instead of the type code because the entity type code for custom entities may be different between [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] organizations.</span><span class="sxs-lookup"><span data-stu-id="81e37-163">We suggest that you use the entity name instead of the type code because the entity type code for custom entities may be different between [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] organizations.</span></span>  

### <a name="example"></a><span data-ttu-id="81e37-164">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="81e37-164">Example</span></span>  
 <span data-ttu-id="81e37-165">The following sample shows the URL without parameters.</span><span class="sxs-lookup"><span data-stu-id="81e37-165">The following sample shows the URL without parameters.</span></span>  

```  
http://myserver/mypage.aspx  
```  

 <span data-ttu-id="81e37-166">The following sample shows the URL with parameters.</span><span class="sxs-lookup"><span data-stu-id="81e37-166">The following sample shows the URL with parameters.</span></span>  

```  
http://myserver/mypage.aspx?id=%7bB2232821-A775-DF11-8DD1-00155DBA3809%7d&orglcid=1033&orgname=adventureworkscycle&type=1&typename=account&userlcid=1033  
```  

### <a name="read-passed-parameters"></a><span data-ttu-id="81e37-167">Read passed parameters</span><span class="sxs-lookup"><span data-stu-id="81e37-167">Read passed parameters</span></span>  

 <span data-ttu-id="81e37-168">Passed parameters are typically read in the target .aspx page by using the **HttpRequest.QueryString** property.</span><span class="sxs-lookup"><span data-stu-id="81e37-168">Passed parameters are typically read in the target .aspx page by using the **HttpRequest.QueryString** property.</span></span> <span data-ttu-id="81e37-169">In an HTML page, the parameters can be accessed by using the **window.location.search** property in [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)].</span><span class="sxs-lookup"><span data-stu-id="81e37-169">In an HTML page, the parameters can be accessed by using the **window.location.search** property in [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)].</span></span> <span data-ttu-id="81e37-170">For more information, see [HttpRequest.QueryString Property](http://msdn2.microsoft.com/library/system.web.httprequest.querystring.aspx) and [search Property](http://msdn2.microsoft.com/library/ms534620.aspx).</span><span class="sxs-lookup"><span data-stu-id="81e37-170">For more information, see [HttpRequest.QueryString Property](http://msdn2.microsoft.com/library/system.web.httprequest.querystring.aspx) and [search Property](http://msdn2.microsoft.com/library/ms534620.aspx).</span></span>  

<a name="BKMK_PassFormData"></a>  

## <a name="pass-form-data"></a><span data-ttu-id="81e37-171">Pass form data</span><span class="sxs-lookup"><span data-stu-id="81e37-171">Pass form data</span></span>  

 <span data-ttu-id="81e37-172">Use the [getValue](clientapi/reference/controls/getValue.md) method on the attributes that contain the data that you want to pass to the other website, and compose a string of the query string arguments the other page will be able to use.</span><span class="sxs-lookup"><span data-stu-id="81e37-172">Use the [getValue](clientapi/reference/controls/getValue.md) method on the attributes that contain the data that you want to pass to the other website, and compose a string of the query string arguments the other page will be able to use.</span></span> <span data-ttu-id="81e37-173">Then use a [Field OnChange Event](clientapi/reference/events/attribute-onchange.md), [IFRAME OnReadyStateComplete Event](clientapi/reference/events/onreadystatecomplete.md), or [Tab TabStateChange Event](clientapi/reference/events/tabstatechange.md) and the [setSrc](clientapi/reference/controls/setSrc.md) method to append your parameters to the `src` property of the IFRAME or web resource.</span><span class="sxs-lookup"><span data-stu-id="81e37-173">Then use a [Field OnChange Event](clientapi/reference/events/attribute-onchange.md), [IFRAME OnReadyStateComplete Event](clientapi/reference/events/onreadystatecomplete.md), or [Tab TabStateChange Event](clientapi/reference/events/tabstatechange.md) and the [setSrc](clientapi/reference/controls/setSrc.md) method to append your parameters to the `src` property of the IFRAME or web resource.</span></span>  

 <span data-ttu-id="81e37-174">If you’re using the data parameter to pass data to a [!INCLUDE[pn_Silverlight_short](../includes/pn-silverlight-short.md)] web resource, you can use the [getData](clientapi/reference/controls/getData.md) and [setData](clientapi/reference/controls/setData.md) methods to manipulate the value passed via the data parameter.</span><span class="sxs-lookup"><span data-stu-id="81e37-174">If you’re using the data parameter to pass data to a [!INCLUDE[pn_Silverlight_short](../includes/pn-silverlight-short.md)] web resource, you can use the [getData](clientapi/reference/controls/getData.md) and [setData](clientapi/reference/controls/setData.md) methods to manipulate the value passed via the data parameter.</span></span> <span data-ttu-id="81e37-175">For webpage (HTML) web resources, use the [setSrc](clientapi/reference/controls/setSrc.md) method to manipulate the `querystring` parameter directly.</span><span class="sxs-lookup"><span data-stu-id="81e37-175">For webpage (HTML) web resources, use the [setSrc](clientapi/reference/controls/setSrc.md) method to manipulate the `querystring` parameter directly.</span></span>  

 <span data-ttu-id="81e37-176">Avoid using the [OnLoad Event](clientapi/reference/events/form-onload.md).</span><span class="sxs-lookup"><span data-stu-id="81e37-176">Avoid using the [OnLoad Event](clientapi/reference/events/form-onload.md).</span></span> <span data-ttu-id="81e37-177">IFRAMES and web resources load asynchronously and the frame may not have finished loading before the `Onload` event script finishes.</span><span class="sxs-lookup"><span data-stu-id="81e37-177">IFRAMES and web resources load asynchronously and the frame may not have finished loading before the `Onload` event script finishes.</span></span> <span data-ttu-id="81e37-178">This can cause the `src` property of the IFRAME or web resource you have changed to be overwritten by the default value of the IFRAME or web resource URL property.</span><span class="sxs-lookup"><span data-stu-id="81e37-178">This can cause the `src` property of the IFRAME or web resource you have changed to be overwritten by the default value of the IFRAME or web resource URL property.</span></span>  

<a name="BKMK_ChangeThePage"></a>   

## <a name="change-the-url"></a><span data-ttu-id="81e37-179">Change the URL</span><span class="sxs-lookup"><span data-stu-id="81e37-179">Change the URL</span></span>  

 <span data-ttu-id="81e37-180">You may want to change the target of the IFRAME based on such considerations as the data in the form or whether the user is working offline.</span><span class="sxs-lookup"><span data-stu-id="81e37-180">You may want to change the target of the IFRAME based on such considerations as the data in the form or whether the user is working offline.</span></span> <span data-ttu-id="81e37-181">You can set the target of the IFRAME dynamically.</span><span class="sxs-lookup"><span data-stu-id="81e37-181">You can set the target of the IFRAME dynamically.</span></span>  

> [!NOTE]
>  <span data-ttu-id="81e37-182">When you change the target page for the IFRAME, parameters aren’t passed to the new URL automatically.</span><span class="sxs-lookup"><span data-stu-id="81e37-182">When you change the target page for the IFRAME, parameters aren’t passed to the new URL automatically.</span></span> <span data-ttu-id="81e37-183">You must append the query string parameters to the URL before you use the `setSrc` method.</span><span class="sxs-lookup"><span data-stu-id="81e37-183">You must append the query string parameters to the URL before you use the `setSrc` method.</span></span>  

### <a name="example"></a><span data-ttu-id="81e37-184">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="81e37-184">Example</span></span>  

 <span data-ttu-id="81e37-185">The following sample shows you how to set the `src` property for the IFRAME and any parameters by using the `onChange` event of an option set field.</span><span class="sxs-lookup"><span data-stu-id="81e37-185">The following sample shows you how to set the `src` property for the IFRAME and any parameters by using the `onChange` event of an option set field.</span></span>  

```javascript  
//Get the value of an option set attribute  
var value = Xrm.Page.data.entity.attributes.get("new_pagechooser").getValue();  
var newTarget = "";  
//Set the target based on the value of the option set  
switch (value) {  
    case 100000001:  
        newTarget = "http://myServer/test/pageOne.aspx";  
        break;  
    default:  
        newTarget = "http://myServer/test/pageTwo.aspx";  
        break;  
}  
//Get the default URL for the IFRAME, which includes the   
// query string parameters  
var IFrame = Xrm.Page.ui.controls.get("IFRAME_test");  
var Url = IFrame.getSrc();  
// Capture the parameters  
var params = Url.substr(Url.indexOf("?"));  
//Append the parameters to the new page URL  
newTarget = newTarget + params;  
// Use the setSrc method so that the IFRAME uses the  
// new page with the existing parameters  
IFrame.setSrc(newTarget);  
```  

## <a name="see-also"></a><span data-ttu-id="81e37-186">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="81e37-186">See Also</span></span>  

 <span data-ttu-id="81e37-187">[Client scripting in Customer Engagement using JavaScript](clientapi/client-scripting.md) </span><span class="sxs-lookup"><span data-stu-id="81e37-187">[Client scripting in Customer Engagement using JavaScript](clientapi/client-scripting.md) </span></span>  
 [<span data-ttu-id="81e37-188">Use JavaScript with Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="81e37-188">Use JavaScript with Customer Engagement</span></span>](use-javascript.md)   
