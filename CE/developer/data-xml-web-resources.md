---
title: Data (XML) Web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about using data (XML) Web resources to save and access data.
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
- web resource, xml
ms.assetid: beb9d687-1a93-4a93-a96f-86b28e5683a5
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4fff9b6ef7d0fe2deea3b5d4d92e58f32f6c6201
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388696"
---
# <a name="data-xml-web-resources"></a><span data-ttu-id="88758-103">Data (XML) Web resources</span><span class="sxs-lookup"><span data-stu-id="88758-103">Data (XML) Web resources</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="88758-104">Use Data (XML) Web resources to save and access data.</span><span class="sxs-lookup"><span data-stu-id="88758-104">Use Data (XML) Web resources to save and access data.</span></span>  
  
## <a name="capabilities-of-xml-web-resources"></a><span data-ttu-id="88758-105">Capabilities of XML Web resources</span><span class="sxs-lookup"><span data-stu-id="88758-105">Capabilities of XML Web resources</span></span>  
 <span data-ttu-id="88758-106">Use XML Web resources to cache data that you want to use in your solution.</span><span class="sxs-lookup"><span data-stu-id="88758-106">Use XML Web resources to cache data that you want to use in your solution.</span></span>  
  
### <a name="limitations-of-xml-web-resources"></a><span data-ttu-id="88758-107">Limitations of XML Web resources</span><span class="sxs-lookup"><span data-stu-id="88758-107">Limitations of XML Web resources</span></span>  
 <span data-ttu-id="88758-108">Use XML Web resources to cache configuration settings or metadata for your solutions.</span><span class="sxs-lookup"><span data-stu-id="88758-108">Use XML Web resources to cache configuration settings or metadata for your solutions.</span></span>  
  
 <span data-ttu-id="88758-109">An XML Web resource does not represent a robust solution for data that is frequently updated by multiple users.</span><span class="sxs-lookup"><span data-stu-id="88758-109">An XML Web resource does not represent a robust solution for data that is frequently updated by multiple users.</span></span> <span data-ttu-id="88758-110">While one user is updating an XML Web resource, another user (or automated process) could update the Web resource and that data would be lost when the first user saves their changes.</span><span class="sxs-lookup"><span data-stu-id="88758-110">While one user is updating an XML Web resource, another user (or automated process) could update the Web resource and that data would be lost when the first user saves their changes.</span></span>  
  
 <span data-ttu-id="88758-111">All XML files must use the .xml file name extension.</span><span class="sxs-lookup"><span data-stu-id="88758-111">All XML files must use the .xml file name extension.</span></span> <span data-ttu-id="88758-112">Files that use XML data but do not use the .xml file name extension cannot be uploaded as Web resources unless the file name extension is changed.</span><span class="sxs-lookup"><span data-stu-id="88758-112">Files that use XML data but do not use the .xml file name extension cannot be uploaded as Web resources unless the file name extension is changed.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="88758-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="88758-113">See also</span></span>  
 <span data-ttu-id="88758-114">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="88758-114">[Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md) </span></span>  
 <span data-ttu-id="88758-115">[Using Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="88758-115">[Using Web Page (HTML) Web Resources](webpage-html-web-resources.md) </span></span>  
 <span data-ttu-id="88758-116">[Using Style Sheet (CSS) Web Resources](css-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="88758-116">[Using Style Sheet (CSS) Web Resources](css-web-resources.md) </span></span>  
 <span data-ttu-id="88758-117">[Using Script (JScript) Web Resources](script-jscript-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="88758-117">[Using Script (JScript) Web Resources](script-jscript-web-resources.md) </span></span>  
 <span data-ttu-id="88758-118">[Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="88758-118">[Using Image (JPG, PNG, GIF) Web Resources](image-web-resources.md) </span></span>  
 <span data-ttu-id="88758-119">[Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md) </span><span class="sxs-lookup"><span data-stu-id="88758-119">[Using Silverlight (XAP) Web Resources](silverlight-xap-web-resources.md) </span></span>  
 [<span data-ttu-id="88758-120">Using Stylesheet (XSL) Web Resources</span><span class="sxs-lookup"><span data-stu-id="88758-120">Using Stylesheet (XSL) Web Resources</span></span>](stylesheet-xsl-web-resources.md)
