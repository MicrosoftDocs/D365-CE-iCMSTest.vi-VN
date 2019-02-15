---
title: CSS web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Learn about using cascading style sheet (CSS) web resources to create style sheets for use in webpage web resources. '
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
- web resource, css
ms.assetid: 7794a5f1-2055-426b-985b-c9ad23fcd1ad
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 19017663ac3982ab6e10a4df744c5c216466d16f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385908"
---
# <a name="css-web-resources"></a><span data-ttu-id="72a99-103">CSS web resources</span><span class="sxs-lookup"><span data-stu-id="72a99-103">CSS web resources</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="72a99-104">Use cascading style sheet (CSS) web resources to create style sheets for use in webpage web resources.</span><span class="sxs-lookup"><span data-stu-id="72a99-104">Use cascading style sheet (CSS) web resources to create style sheets for use in webpage web resources.</span></span>  
  
## <a name="capabilities-of-css-web-resources"></a><span data-ttu-id="72a99-105">Capabilities of CSS web resources</span><span class="sxs-lookup"><span data-stu-id="72a99-105">Capabilities of CSS web resources</span></span>  
 <span data-ttu-id="72a99-106">With CSS web resources, you can manage the appearance of webpage web resources by linking them to a shared library of CSS styles.</span><span class="sxs-lookup"><span data-stu-id="72a99-106">With CSS web resources, you can manage the appearance of webpage web resources by linking them to a shared library of CSS styles.</span></span>  
  
### <a name="limitations-of-css-web-resources"></a><span data-ttu-id="72a99-107">Limitations of CSS web resources</span><span class="sxs-lookup"><span data-stu-id="72a99-107">Limitations of CSS web resources</span></span>  
 <span data-ttu-id="72a99-108">Like all web resources, CSS web resources are only available in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps security context.</span><span class="sxs-lookup"><span data-stu-id="72a99-108">Like all web resources, CSS web resources are only available in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps security context.</span></span> <span data-ttu-id="72a99-109">Only licensed [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps users who have the necessary privileges can access them.</span><span class="sxs-lookup"><span data-stu-id="72a99-109">Only licensed [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps users who have the necessary privileges can access them.</span></span>  
  
## <a name="referencing-a-style-sheet-web-resource-from-a-webpage-web-resource"></a><span data-ttu-id="72a99-110">Referencing a style sheet web resource from a webpage web resource</span><span class="sxs-lookup"><span data-stu-id="72a99-110">Referencing a style sheet web resource from a webpage web resource</span></span>  
 <span data-ttu-id="72a99-111">All web resources can use relative URLs to reference each other.</span><span class="sxs-lookup"><span data-stu-id="72a99-111">All web resources can use relative URLs to reference each other.</span></span> <span data-ttu-id="72a99-112">In the following example, for the webpage web resource `sample_/content/contentpage.htm` to reference the style sheet web resource `sample_/styles/styles.css`, add the following example to the head element of sample_/content/contentpage.htm:</span><span class="sxs-lookup"><span data-stu-id="72a99-112">In the following example, for the webpage web resource `sample_/content/contentpage.htm` to reference the style sheet web resource `sample_/styles/styles.css`, add the following example to the head element of sample_/content/contentpage.htm:</span></span>  
  
```html  
<link rel="stylesheet" type="text/css" href="../styles/styles.css" />  
```  
  
 <span data-ttu-id="72a99-113">To reference a style sheet from a different publisher, the path must include that solution publisher customization prefix.</span><span class="sxs-lookup"><span data-stu-id="72a99-113">To reference a style sheet from a different publisher, the path must include that solution publisher customization prefix.</span></span> <span data-ttu-id="72a99-114">For example, for the `sample_/content/contentpage.htm` page to reference the `MyIsv_/styles/styles.css` page, the href parameter value should be `../../MyIsv_/styles/styles.css`.</span><span class="sxs-lookup"><span data-stu-id="72a99-114">For example, for the `sample_/content/contentpage.htm` page to reference the `MyIsv_/styles/styles.css` page, the href parameter value should be `../../MyIsv_/styles/styles.css`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="72a99-115">References included in code between web resources aren’t tracked as solution dependencies.</span><span class="sxs-lookup"><span data-stu-id="72a99-115">References included in code between web resources aren’t tracked as solution dependencies.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="72a99-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="72a99-116">See also</span></span>  
 <span data-ttu-id="72a99-117">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="72a99-117">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span></span>  
 <span data-ttu-id="72a99-118">[Using Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="72a99-118">[Using Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span></span>  
 <span data-ttu-id="72a99-119">[Using Script (JScript) Web Resources](script-jscript-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="72a99-119">[Using Script (JScript) Web Resources](script-jscript-web-resources.md) </span></span>  
 <span data-ttu-id="72a99-120">[Using Data (XML) Web Resources](data-xml-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="72a99-120">[Using Data (XML) Web Resources](data-xml-web-resources.md) </span></span>  
 <span data-ttu-id="72a99-121">[Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="72a99-121">[Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md) </span></span>  
 <span data-ttu-id="72a99-122">[Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="72a99-122">[Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md) </span></span>  
 <span data-ttu-id="72a99-123">[Using Stylesheet (XSL) Web Resources](stylesheet-xsl-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="72a99-123">[Using Stylesheet (XSL) Web Resources](stylesheet-xsl-web-resources.md) </span></span>  
 [<span data-ttu-id="72a99-124">WebResource Entity</span><span class="sxs-lookup"><span data-stu-id="72a99-124">WebResource Entity</span></span>](entities/webresource.md)
