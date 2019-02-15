---
title: Implement single sign-on from an ASPX webpage or IFRAME (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: This topic describes how to develop a custom webpage that can make SDK calls to Dynamics 365 for Customer Engagement apps on behalf of the Dynamics 365 for Customer Engagement apps user who is signed in
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
- single sign-on from an ASPX webpage or IFRAME, implementing
- ASPX webpage with (optionally) IFRAME display, implementing single sign-on from an ASPX webpage or IFRAME
- Windows Azure-hosted webpage, implementing single sign-on from an ASPX webpage or IFRAME
- implementing single sign-on from an ASPX webpage or IFRAME, ASPX webpage with (optionally) IFRAME display
- custom website makes SDK calls to CRM on behalf of logged-on user, separate website for
ms.assetid: c2b38554-eab9-4793-a2f5-62b7a11d99f7
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 307673ec53269feb46b2963ccec57041df166453
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385881"
---
# <a name="implement-single-sign-on-from-an-aspx-webpage-or-iframe"></a><span data-ttu-id="72443-103">Implement single sign-on from an ASPX webpage or IFRAME</span><span class="sxs-lookup"><span data-stu-id="72443-103">Implement single sign-on from an ASPX webpage or IFRAME</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="72443-104">This topic describes how to develop a custom webpage that can make SDK calls to [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps on behalf of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps user who is signed in.</span><span class="sxs-lookup"><span data-stu-id="72443-104">This topic describes how to develop a custom webpage that can make SDK calls to [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps on behalf of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps user who is signed in.</span></span> <span data-ttu-id="72443-105">The typical use of this capability is to write a webpage that is displayed in an inline frame in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application user interface.</span><span class="sxs-lookup"><span data-stu-id="72443-105">The typical use of this capability is to write a webpage that is displayed in an inline frame in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application user interface.</span></span> <span data-ttu-id="72443-106">That webpage performs its intended operation, for example, providing a store front, while being hosted on a website independent of the site that’s hosting [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="72443-106">That webpage performs its intended operation, for example, providing a store front, while being hosted on a website independent of the site that’s hosting [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span> <span data-ttu-id="72443-107">However, the webpage can perform its operations on behalf of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps user who is signed in.</span><span class="sxs-lookup"><span data-stu-id="72443-107">However, the webpage can perform its operations on behalf of the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps user who is signed in.</span></span> <span data-ttu-id="72443-108">The result is seamless integration between a webpage and [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="72443-108">The result is seamless integration between a webpage and [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span>  
  
## <a name="includepndynamicscrmincludespn-dynamics-crmmd-apps-with-a-separate-website"></a>[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="72443-109">apps with a separate website</span><span class="sxs-lookup"><span data-stu-id="72443-109">apps with a separate website</span></span>  
 <span data-ttu-id="72443-110">This scenario is for a [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps Internet-facing deployment (IFD) where a separate website hosts a custom ASPX webpage that is optionally displayed in an inline frame of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application.</span><span class="sxs-lookup"><span data-stu-id="72443-110">This scenario is for a [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps Internet-facing deployment (IFD) where a separate website hosts a custom ASPX webpage that is optionally displayed in an inline frame of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application.</span></span> <span data-ttu-id="72443-111">This scenario uses federated claims.</span><span class="sxs-lookup"><span data-stu-id="72443-111">This scenario uses federated claims.</span></span> <span data-ttu-id="72443-112">Therefore, you’ll have to set up a security token service (STS) server for identity management.</span><span class="sxs-lookup"><span data-stu-id="72443-112">Therefore, you’ll have to set up a security token service (STS) server for identity management.</span></span> <span data-ttu-id="72443-113">You’ll also need a certificate to be used when making [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps and the website relying parties, which established cross-domain trust between these parties.</span><span class="sxs-lookup"><span data-stu-id="72443-113">You’ll also need a certificate to be used when making [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps and the website relying parties, which established cross-domain trust between these parties.</span></span>  
  
### <a name="background-information"></a><span data-ttu-id="72443-114">Background information</span><span class="sxs-lookup"><span data-stu-id="72443-114">Background information</span></span>  
 <span data-ttu-id="72443-115">For more information about how to configure claims and a relying party, see the following topics in [Deploying and administering Microsoft Dynamics 365 for Customer Engagement apps](https://technet.microsoft.com/library/hh699811.aspx):</span><span class="sxs-lookup"><span data-stu-id="72443-115">For more information about how to configure claims and a relying party, see the following topics in [Deploying and administering Microsoft Dynamics 365 for Customer Engagement apps](https://technet.microsoft.com/library/hh699811.aspx):</span></span>  
  
- <span data-ttu-id="72443-116">[Post-Installation and Configuration Guidelines](https://technet.microsoft.com/library/hh699726.aspx) - Configure a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Internet-facing deployment (IFD)</span><span class="sxs-lookup"><span data-stu-id="72443-116">[Post-Installation and Configuration Guidelines](https://technet.microsoft.com/library/hh699726.aspx) - Configure a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Internet-facing deployment (IFD)</span></span>  
  
- <span data-ttu-id="72443-117">[System requirements and required technologies](https://technet.microsoft.com/library/hh699831.aspx) - Accessing [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps from the Internet - Claims-based authentication and [!INCLUDE[pn_ifd_short](../includes/pn-ifd-short.md)] requirements</span><span class="sxs-lookup"><span data-stu-id="72443-117">[System requirements and required technologies](https://technet.microsoft.com/library/hh699831.aspx) - Accessing [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps from the Internet - Claims-based authentication and [!INCLUDE[pn_ifd_short](../includes/pn-ifd-short.md)] requirements</span></span>  
  
  <span data-ttu-id="72443-118">For more information about identity management, see [the identity training course](http://channel9.msdn.com/Learn/Courses/IdentityTrainingCourse).</span><span class="sxs-lookup"><span data-stu-id="72443-118">For more information about identity management, see [the identity training course](http://channel9.msdn.com/Learn/Courses/IdentityTrainingCourse).</span></span>  
  
  [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="72443-119">[Walkthrough: Single Sign-on from a Custom Web Page](https://msdn.microsoft.com/library/gg509057\(v=crm.5\).aspx) in the [!INCLUDE[pn_CRM_2011](../includes/pn-crm-2011.md)] SDK.</span><span class="sxs-lookup"><span data-stu-id="72443-119">[Walkthrough: Single Sign-on from a Custom Web Page](https://msdn.microsoft.com/library/gg509057\(v=crm.5\).aspx) in the [!INCLUDE[pn_CRM_2011](../includes/pn-crm-2011.md)] SDK.</span></span>  
  
<a name="crmonline-azure"></a>   
## <a name="includepndynamicscrmonlineincludespn-dynamics-crm-onlinemd-apps-with-an-azure-hosted-webpage"></a>[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="72443-120">apps with an Azure-hosted webpage</span><span class="sxs-lookup"><span data-stu-id="72443-120">apps with an Azure-hosted webpage</span></span>  
 <span data-ttu-id="72443-121">This scenario is for use with [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps where [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] hosts a custom webpage that’s optionally displayed in an inline frame of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application.</span><span class="sxs-lookup"><span data-stu-id="72443-121">This scenario is for use with [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps where [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] hosts a custom webpage that’s optionally displayed in an inline frame of the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application.</span></span> <span data-ttu-id="72443-122">This scenario uses federated claims, provided by the [!INCLUDE[pn_Windows_Live](../includes/pn-windows-live.md)] security token service (STS) server for identity management.</span><span class="sxs-lookup"><span data-stu-id="72443-122">This scenario uses federated claims, provided by the [!INCLUDE[pn_Windows_Live](../includes/pn-windows-live.md)] security token service (STS) server for identity management.</span></span> <span data-ttu-id="72443-123">You must provide a certificate to be used when making [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps and the [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] website relying parties, which established cross-domain trust between these parties.</span><span class="sxs-lookup"><span data-stu-id="72443-123">You must provide a certificate to be used when making [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps and the [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] website relying parties, which established cross-domain trust between these parties.</span></span>  
  
### <a name="background-information"></a><span data-ttu-id="72443-124">Background information</span><span class="sxs-lookup"><span data-stu-id="72443-124">Background information</span></span>  
 <span data-ttu-id="72443-125">For more information about how to configure a relying party, see the following topic: [Secure Azure Web Role ASP.NET Web Application Using Access Control Service v2.0](http://social.technet.microsoft.com/wiki/contents/articles/2590.aspx)</span><span class="sxs-lookup"><span data-stu-id="72443-125">For more information about how to configure a relying party, see the following topic: [Secure Azure Web Role ASP.NET Web Application Using Access Control Service v2.0](http://social.technet.microsoft.com/wiki/contents/articles/2590.aspx)</span></span>  
  
 <span data-ttu-id="72443-126">For more information about identity management, see [http://channel9.msdn.com/Learn/Courses/IdentityTrainingCourse](http://channel9.msdn.com/Learn/Courses/IdentityTrainingCourse)</span><span class="sxs-lookup"><span data-stu-id="72443-126">For more information about identity management, see [http://channel9.msdn.com/Learn/Courses/IdentityTrainingCourse](http://channel9.msdn.com/Learn/Courses/IdentityTrainingCourse)</span></span>  
  
 <span data-ttu-id="72443-127">For more information about implementing this scenario including problems you may run into and the workarounds, see these blogs: [Dynamics 365 for Customer Engagement apps & Azure: Improving the SSO experience](http://blogs.msdn.com/b/devkeydet/archive/2013/01/14/crm-online-amp-windows-azure-improving-the-sso-experience.aspx), and [Dynamics 365 for Customer Engagement apps & Azure Series](http://blogs.msdn.com/b/devkeydet/archive/2013/01/27/crm-online-amp-windows-azure-series.aspx).</span><span class="sxs-lookup"><span data-stu-id="72443-127">For more information about implementing this scenario including problems you may run into and the workarounds, see these blogs: [Dynamics 365 for Customer Engagement apps & Azure: Improving the SSO experience](http://blogs.msdn.com/b/devkeydet/archive/2013/01/14/crm-online-amp-windows-azure-improving-the-sso-experience.aspx), and [Dynamics 365 for Customer Engagement apps & Azure Series](http://blogs.msdn.com/b/devkeydet/archive/2013/01/27/crm-online-amp-windows-azure-series.aspx).</span></span>  
  
<a name="BKMK_EnableIFrameCommunicationAccrossDomains"></a>   
## <a name="enable-inline-frame-communication-across-domains"></a><span data-ttu-id="72443-128">Enable inline frame communication across domains</span><span class="sxs-lookup"><span data-stu-id="72443-128">Enable inline frame communication across domains</span></span>  
 <span data-ttu-id="72443-129">If you want to enable communication for an inline frame (iframe) that contains content from a different domain, you can use the `Window.postMessage` method.</span><span class="sxs-lookup"><span data-stu-id="72443-129">If you want to enable communication for an inline frame (iframe) that contains content from a different domain, you can use the `Window.postMessage` method.</span></span> <span data-ttu-id="72443-130">This browser method can be used for [!INCLUDE[pn_IE_8](../includes/pn-ie-8.md)].</span><span class="sxs-lookup"><span data-stu-id="72443-130">This browser method can be used for [!INCLUDE[pn_IE_8](../includes/pn-ie-8.md)].</span></span> [!INCLUDE[tn_Google_Chrome](../includes/tn-google-chrome.md)]<span data-ttu-id="72443-131">, [!INCLUDE[tn_Mozilla_Firefox](../includes/tn-mozilla-firefox.md)], and [!INCLUDE[tn_Apple_Safari](../includes/tn-apple-safari.md)] also support this method.</span><span class="sxs-lookup"><span data-stu-id="72443-131">, [!INCLUDE[tn_Mozilla_Firefox](../includes/tn-mozilla-firefox.md)], and [!INCLUDE[tn_Apple_Safari](../includes/tn-apple-safari.md)] also support this method.</span></span> <span data-ttu-id="72443-132">For more information about using `postMessage`, see the following blog posts:</span><span class="sxs-lookup"><span data-stu-id="72443-132">For more information about using `postMessage`, see the following blog posts:</span></span>  
  
-   [<span data-ttu-id="72443-133">Cross domain calls to the parent CRM 2011 form</span><span class="sxs-lookup"><span data-stu-id="72443-133">Cross domain calls to the parent CRM 2011 form</span></span>](http://blogs.msdn.com/b/devkeydet/archive/2012/02/14/cross-domain-calls-to-the-parent-crm-2011-form.aspx)  
  
-   [<span data-ttu-id="72443-134">Cross-Document Messaging and RPC</span><span class="sxs-lookup"><span data-stu-id="72443-134">Cross-Document Messaging and RPC</span></span>](https://msdn.microsoft.com/magazine/ff800814.aspx)  
  
### <a name="see-also"></a><span data-ttu-id="72443-135">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="72443-135">See also</span></span>  
 <span data-ttu-id="72443-136">[Access the Web Services (Authentication) in Dynamics 365 for Customer Engagement apps](authenticate-users.md) </span><span class="sxs-lookup"><span data-stu-id="72443-136">[Access the Web Services (Authentication) in Dynamics 365 for Customer Engagement apps](authenticate-users.md) </span></span>  
 <span data-ttu-id="72443-137">[Sample: Impersonate Using the ActOnBehalfOf Privilege](org-service/sample-impersonate-actonbehalfof-privilege.md) </span><span class="sxs-lookup"><span data-stu-id="72443-137">[Sample: Impersonate Using the ActOnBehalfOf Privilege](org-service/sample-impersonate-actonbehalfof-privilege.md) </span></span>  
 <span data-ttu-id="72443-138">[Impersonate Another User](org-service/impersonate-another-user.md) </span><span class="sxs-lookup"><span data-stu-id="72443-138">[Impersonate Another User](org-service/impersonate-another-user.md) </span></span>  
 [<span data-ttu-id="72443-139">Web Resources for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="72443-139">Web Resources for Dynamics 365 for Customer Engagement apps</span></span>](web-resources.md)