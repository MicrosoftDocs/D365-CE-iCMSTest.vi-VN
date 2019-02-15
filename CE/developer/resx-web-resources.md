---
title: String (RESX) web resources (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: 'Learn about using string web resources to make localized strings available for use in Dynamics 365 for Customer Engagement. '
ms.custom: ''
ms.date: 12/28/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 2abb6e22-c64c-4f87-8b55-9f4405103cec
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b398099b56274d17f3083080750e173302fcf468
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388420"
---
# <a name="string-resx-web-resources"></a><span data-ttu-id="6616b-103">String (RESX) web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-103">String (RESX) web resources</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6616b-104">Use these web resources to manage localized strings in any user interface you define or with error messages you will display.</span><span class="sxs-lookup"><span data-stu-id="6616b-104">Use these web resources to manage localized strings in any user interface you define or with error messages you will display.</span></span> 

> [!NOTE]
> <span data-ttu-id="6616b-105">String (RESX) web resources were added with the [!INCLUDE[../includes/pn-crm-9-0-0-online.md](../includes/pn-crm-9-0-0-online.md)].</span><span class="sxs-lookup"><span data-stu-id="6616b-105">String (RESX) web resources were added with the [!INCLUDE[../includes/pn-crm-9-0-0-online.md](../includes/pn-crm-9-0-0-online.md)].</span></span>

# <a name="using-resx-web-resources"></a><span data-ttu-id="6616b-106">Using RESX web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-106">Using RESX web resources</span></span>

<!-- 
Much of this content also found in developer/clientapi/reference/Xrm-Utility/getResourceString.md
If you change this, make sure that topic is in sync.
-->

<span data-ttu-id="6616b-107">RESX web resources contain the keys and localized string values for a single language defined using the RESX XML format.</span><span class="sxs-lookup"><span data-stu-id="6616b-107">RESX web resources contain the keys and localized string values for a single language defined using the RESX XML format.</span></span> <span data-ttu-id="6616b-108">RESX is a common format for defining localized resources for windows applications, so there is common tooling available to work with this type of file and localization vendors will be familiar with working with them.</span><span class="sxs-lookup"><span data-stu-id="6616b-108">RESX is a common format for defining localized resources for windows applications, so there is common tooling available to work with this type of file and localization vendors will be familiar with working with them.</span></span> <span data-ttu-id="6616b-109">When the file is published as a web resource in CRM it will be converted to a JSON format which will be downloaded to the application when needed.</span><span class="sxs-lookup"><span data-stu-id="6616b-109">When the file is published as a web resource in CRM it will be converted to a JSON format which will be downloaded to the application when needed.</span></span>

<span data-ttu-id="6616b-110">When you create RESX web resources you must explicitly set the language value and include the locale identifier (LCID) for the appropriate language in the name of the web resource.</span><span class="sxs-lookup"><span data-stu-id="6616b-110">When you create RESX web resources you must explicitly set the language value and include the locale identifier (LCID) for the appropriate language in the name of the web resource.</span></span> <span data-ttu-id="6616b-111">For example, `new_/strings/MyAppResources.1033.resx` would contain resources for English language.</span><span class="sxs-lookup"><span data-stu-id="6616b-111">For example, `new_/strings/MyAppResources.1033.resx` would contain resources for English language.</span></span> <span data-ttu-id="6616b-112">See [Microsoft Locale ID Values](https://msdn.microsoft.com/library/ms912047(WinEmbedded.10).aspx) for a list of LCID values.</span><span class="sxs-lookup"><span data-stu-id="6616b-112">See [Microsoft Locale ID Values](https://msdn.microsoft.com/library/ms912047(WinEmbedded.10).aspx) for a list of LCID values.</span></span>

<span data-ttu-id="6616b-113">To extract the localized value use the [Xrm.Utility.getResourceString](clientapi/reference/Xrm-Utility/getResourceString.md) function.</span><span class="sxs-lookup"><span data-stu-id="6616b-113">To extract the localized value use the [Xrm.Utility.getResourceString](clientapi/reference/Xrm-Utility/getResourceString.md) function.</span></span> <span data-ttu-id="6616b-114">This function accepts two parameters: `WebResourceName` and `keyValue`.</span><span class="sxs-lookup"><span data-stu-id="6616b-114">This function accepts two parameters: `WebResourceName` and `keyValue`.</span></span> 

<span data-ttu-id="6616b-115">For example `Xrm.Utility.getResourceString("new_/strings/MyAppResources","hello")` will return the localized string value for the resource key hello within the `new_/strings/MyAppResources.1033.resx` web resource if the user’s preferred language is English.</span><span class="sxs-lookup"><span data-stu-id="6616b-115">For example `Xrm.Utility.getResourceString("new_/strings/MyAppResources","hello")` will return the localized string value for the resource key hello within the `new_/strings/MyAppResources.1033.resx` web resource if the user’s preferred language is English.</span></span> <span data-ttu-id="6616b-116">Notice that the function doesn’t refer to any specific language or full name of any RESX web resource.</span><span class="sxs-lookup"><span data-stu-id="6616b-116">Notice that the function doesn’t refer to any specific language or full name of any RESX web resource.</span></span> <span data-ttu-id="6616b-117">This functionality depends on the RESX web resource being associated to the calling JavaScript web resource as a dependency.</span><span class="sxs-lookup"><span data-stu-id="6616b-117">This functionality depends on the RESX web resource being associated to the calling JavaScript web resource as a dependency.</span></span> <span data-ttu-id="6616b-118">More information: [Web Resource dependencies](web-resource-dependencies.md).</span><span class="sxs-lookup"><span data-stu-id="6616b-118">More information: [Web Resource dependencies](web-resource-dependencies.md).</span></span>

<span data-ttu-id="6616b-119">The appropriate string value will be determined by the individual user’s language preference and the languages available in the organization.</span><span class="sxs-lookup"><span data-stu-id="6616b-119">The appropriate string value will be determined by the individual user’s language preference and the languages available in the organization.</span></span> <span data-ttu-id="6616b-120">If a localized string is not found that matches the user’s language preference, the localized string will automatically fallback to the base language for the organization.</span><span class="sxs-lookup"><span data-stu-id="6616b-120">If a localized string is not found that matches the user’s language preference, the localized string will automatically fallback to the base language for the organization.</span></span> <span data-ttu-id="6616b-121">If no matching localized string is found for the organizations base language, a null value will be returned.</span><span class="sxs-lookup"><span data-stu-id="6616b-121">If no matching localized string is found for the organizations base language, a null value will be returned.</span></span>

### <a name="see-also"></a><span data-ttu-id="6616b-122">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6616b-122">See also</span></span>
[<span data-ttu-id="6616b-123">Web resources for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="6616b-123">Web resources for Dynamics 365 for Customer Engagement apps</span></span>](web-resources.md)<br />
[<span data-ttu-id="6616b-124">Create accessible web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-124">Create accessible web resources</span></span>](create-accessible-web-resources.md)<br />
[<span data-ttu-id="6616b-125">Create web resources and IFrame content for use with the Dynamics 365 for Customer Engagement apps for mobile clients</span><span class="sxs-lookup"><span data-stu-id="6616b-125">Create web resources and IFrame content for use with the Dynamics 365 for Customer Engagement apps for mobile clients</span></span>](create-web-resources-iframe-mobile.md)<br />
[<span data-ttu-id="6616b-126">Web resource dependencies</span><span class="sxs-lookup"><span data-stu-id="6616b-126">Web resource dependencies</span></span>](web-resource-dependencies.md)<br />
[<span data-ttu-id="6616b-127">Webpage (HTML) web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-127">Webpage (HTML) web resources</span></span>](webpage-html-web-resources.md)<br />
[<span data-ttu-id="6616b-128">Silverlight (XAP) web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-128">Silverlight (XAP) web resources</span></span>](silverlight-xap-web-resources.md)<br />
[<span data-ttu-id="6616b-129">Script (JScript) web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-129">Script (JScript) web resources</span></span>](script-jscript-web-resources.md)<br />
[<span data-ttu-id="6616b-130">Image (JPG, PNG, GIF, ICO) web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-130">Image (JPG, PNG, GIF, ICO) web resources</span></span>](image-web-resources.md)<br />
[<span data-ttu-id="6616b-131">Stylesheet (XSL) web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-131">Stylesheet (XSL) web resources</span></span>](stylesheet-xsl-web-resources.md)<br />
[<span data-ttu-id="6616b-132">Data (XML) Web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-132">Data (XML) Web resources</span></span>](data-xml-web-resources.md)<br />
[<span data-ttu-id="6616b-133">CSS web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-133">CSS web resources</span></span>](css-web-resources.md)<br />
[<span data-ttu-id="6616b-134">WebResource entity messages and methods</span><span class="sxs-lookup"><span data-stu-id="6616b-134">WebResource entity messages and methods</span></span>](webresource-entity-messages-methods.md)<br />
[<span data-ttu-id="6616b-135">Sample: Pass multiple values to a  web resource through the data parameter</span><span class="sxs-lookup"><span data-stu-id="6616b-135">Sample: Pass multiple values to a  web resource through the data parameter</span></span>](sample-pass-multiple-values-web-resource-through-data-parameter.md)<br />
[<span data-ttu-id="6616b-136">Sample: Import files as web resources</span><span class="sxs-lookup"><span data-stu-id="6616b-136">Sample: Import files as web resources</span></span>](sample-import-files-web-resources.md)<br />
[<span data-ttu-id="6616b-137">Sample: Web resource utility</span><span class="sxs-lookup"><span data-stu-id="6616b-137">Sample: Web resource utility</span></span>](sample-web-resource-utility.md)<br />
