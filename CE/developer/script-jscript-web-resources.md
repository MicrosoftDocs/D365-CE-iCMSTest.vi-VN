---
title: Script(JScript) web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Learn about using JavaScript web resources to create a library of JavaScript functions that can be accessed from anywhere. '
ms.custom: ''
ms.date: 03/02/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- web resource, Jscript
ms.assetid: 882565b5-aa86-475e-971a-b5123bbadcf9
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 432b07d6eba58f408ee5af0e1cc9aa9b9345d9c1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387207"
---
# <a name="scriptjscript-web-resources"></a><span data-ttu-id="3ad44-103">Script(JScript) web resources</span><span class="sxs-lookup"><span data-stu-id="3ad44-103">Script(JScript) web resources</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3ad44-104">Use Script(JScript) web resources to create a library of [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] functions that can be accessed from anywhere.</span><span class="sxs-lookup"><span data-stu-id="3ad44-104">Use Script(JScript) web resources to create a library of [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] functions that can be accessed from anywhere.</span></span>  
  
<a name="BKMK_capabilities"></a>   
## <a name="capabilities-of-script-web-resources"></a><span data-ttu-id="3ad44-105">Capabilities of script web resources</span><span class="sxs-lookup"><span data-stu-id="3ad44-105">Capabilities of script web resources</span></span>  
 <span data-ttu-id="3ad44-106">With [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources, you can more efficiently manage code used in form scripts, webpage (HTML) web resources, or ribbon commands by linking them to shared library of [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] functions.</span><span class="sxs-lookup"><span data-stu-id="3ad44-106">With [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources, you can more efficiently manage code used in form scripts, webpage (HTML) web resources, or ribbon commands by linking them to shared library of [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] functions.</span></span>  
  
<a name="BKMK_limitations"></a>   
## <a name="limitations-of-script-web-resources"></a><span data-ttu-id="3ad44-107">Limitations of script web resources</span><span class="sxs-lookup"><span data-stu-id="3ad44-107">Limitations of script web resources</span></span>  
 <span data-ttu-id="3ad44-108">Like all web resources, [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources use the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] web application security context.</span><span class="sxs-lookup"><span data-stu-id="3ad44-108">Like all web resources, [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resources use the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] web application security context.</span></span> <span data-ttu-id="3ad44-109">Only licensed [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] users who have the necessary privileges can access them.</span><span class="sxs-lookup"><span data-stu-id="3ad44-109">Only licensed [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] users who have the necessary privileges can access them.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3ad44-110">References included in code between web resources aren’t tracked as solution dependencies.</span><span class="sxs-lookup"><span data-stu-id="3ad44-110">References included in code between web resources aren’t tracked as solution dependencies.</span></span>  
  
<a name="BKMK_Using"></a>   
## <a name="using-javascript-libraries"></a><span data-ttu-id="3ad44-111">Using JavaScript libraries</span><span class="sxs-lookup"><span data-stu-id="3ad44-111">Using JavaScript libraries</span></span>  
 <span data-ttu-id="3ad44-112">For information about developing and testing [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] libraries as well as how to associate them with ribbon commands and form events, see [Client scripting in Customer Engagement using JavaScript](clientapi/client-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="3ad44-112">For information about developing and testing [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] libraries as well as how to associate them with ribbon commands and form events, see [Client scripting in Customer Engagement using JavaScript](clientapi/client-scripting.md).</span></span>  
  
<a name="BKMK_Referencing"></a>   
## <a name="referencing-a-script-web-resource-from-a-webpage-web-resource"></a><span data-ttu-id="3ad44-113">Referencing a script web resource from a webpage web resource</span><span class="sxs-lookup"><span data-stu-id="3ad44-113">Referencing a script web resource from a webpage web resource</span></span>  
 <span data-ttu-id="3ad44-114">All web resources can use relative URLs to reference each other.</span><span class="sxs-lookup"><span data-stu-id="3ad44-114">All web resources can use relative URLs to reference each other.</span></span> <span data-ttu-id="3ad44-115">In the following example, for the webpage web resource `new_/content/contentpage.htm` to reference the [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resource `new_/scripts/myScript.js`, add the following HTML code to the head element of `new_/content/contentpage.htm`.</span><span class="sxs-lookup"><span data-stu-id="3ad44-115">In the following example, for the webpage web resource `new_/content/contentpage.htm` to reference the [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] web resource `new_/scripts/myScript.js`, add the following HTML code to the head element of `new_/content/contentpage.htm`.</span></span>  
  
```html  
<script type="text/jscript" src="../scripts/myScript.js"></script>  
```  
  
 <span data-ttu-id="3ad44-116">To reference a [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] from a different publisher, the path must include the customization prefix for that publisher.</span><span class="sxs-lookup"><span data-stu-id="3ad44-116">To reference a [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] from a different publisher, the path must include the customization prefix for that publisher.</span></span> <span data-ttu-id="3ad44-117">For example, for the `new_/content/contentpage.htm` page to reference the `MyIsv_/scripts/customscripts.js` page, the `src` attribute value should be `../../MyIsv_/scripts/customscripts.js`.</span><span class="sxs-lookup"><span data-stu-id="3ad44-117">For example, for the `new_/content/contentpage.htm` page to reference the `MyIsv_/scripts/customscripts.js` page, the `src` attribute value should be `../../MyIsv_/scripts/customscripts.js`.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3ad44-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3ad44-118">See also</span></span>  
 <span data-ttu-id="3ad44-119">[Use JavaScript with Customer Engagement apps](use-javascript.md) </span><span class="sxs-lookup"><span data-stu-id="3ad44-119">[Use JavaScript with Customer Engagement apps](use-javascript.md) </span></span>  
 <span data-ttu-id="3ad44-120">[Client scripting in Customer Engagement apps using JavaScript](clientapi/client-scripting.md) </span><span class="sxs-lookup"><span data-stu-id="3ad44-120">[Client scripting in Customer Engagement apps using JavaScript](clientapi/client-scripting.md) </span></span>  
 <span data-ttu-id="3ad44-121">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="3ad44-121">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span></span>  
 <span data-ttu-id="3ad44-122">[Using Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="3ad44-122">[Using Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span></span>  
 <span data-ttu-id="3ad44-123">[Using Style Sheet (CSS) Web Resources](css-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="3ad44-123">[Using Style Sheet (CSS) Web Resources](css-web-resources.md) </span></span>  
 <span data-ttu-id="3ad44-124">[Using Data (XML) Web Resources](data-xml-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="3ad44-124">[Using Data (XML) Web Resources](data-xml-web-resources.md) </span></span>  
 <span data-ttu-id="3ad44-125">[Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="3ad44-125">[Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md) </span></span>  
 <span data-ttu-id="3ad44-126">[Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="3ad44-126">[Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md) </span></span>  
 <span data-ttu-id="3ad44-127">[Using Stylesheet (XSL) Web Resources](stylesheet-xsl-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="3ad44-127">[Using Stylesheet (XSL) Web Resources](stylesheet-xsl-web-resources.md) </span></span>  
 [<span data-ttu-id="3ad44-128">Streamline web resource development using Fiddler AutoResponder</span><span class="sxs-lookup"><span data-stu-id="3ad44-128">Streamline web resource development using Fiddler AutoResponder</span></span>](streamline-javascript-development-fiddler-autoresponder.md)    
