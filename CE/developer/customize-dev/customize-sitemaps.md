---
title: Customize SiteMaps (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The SiteMap provides the structure for navigation in Dynamics 365 for Customer Engagement. The SiteMap entity stores information about the site map, and the SiteMap.SiteMapXml attribute stores the XML that defines the site map.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 54f00cc7-0653-423d-abe0-5344ad3711c3
caps.latest.revision: 14
author: KumarVivek
ms.author: kvivek
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e6a88c62a2f157c684d8faeaefd7e0ee3c463676
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386262"
---
# <a name="customize-sitemaps"></a><span data-ttu-id="4aef7-104">Customize SiteMaps</span><span class="sxs-lookup"><span data-stu-id="4aef7-104">Customize SiteMaps</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4aef7-105">The SiteMap provides the structure for navigation in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="4aef7-105">The SiteMap provides the structure for navigation in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement.</span></span> <span data-ttu-id="4aef7-106">The `SiteMap` entity stores information about the site map, and the `SiteMap.SiteMapXml` attribute stores the XML that defines the site map.</span><span class="sxs-lookup"><span data-stu-id="4aef7-106">The `SiteMap` entity stores information about the site map, and the `SiteMap.SiteMapXml` attribute stores the XML that defines the site map.</span></span> <span data-ttu-id="4aef7-107">The site map XML is exposed as the `SiteMap` node in the              customizations.xml file of an exported unmanaged solution.</span><span class="sxs-lookup"><span data-stu-id="4aef7-107">The site map XML is exposed as the `SiteMap` node in the              customizations.xml file of an exported unmanaged solution.</span></span>  
  
 <span data-ttu-id="4aef7-108">The structure of navigation defined in the site map XML is  evaluated together with your security privileges to display navigation options in the application.</span><span class="sxs-lookup"><span data-stu-id="4aef7-108">The structure of navigation defined in the site map XML is  evaluated together with your security privileges to display navigation options in the application.</span></span> <span data-ttu-id="4aef7-109">If your security privileges do not provide read access to an entity specified in the site map XML, the navigation option will not be displayed to you.</span><span class="sxs-lookup"><span data-stu-id="4aef7-109">If your security privileges do not provide read access to an entity specified in the site map XML, the navigation option will not be displayed to you.</span></span>  
  
 <span data-ttu-id="4aef7-110">With the introduction of modular business apps in the [!INCLUDE[pn_crm_8_2_0_online](../../includes/pn-crm-8-2-0-online.md)], where each app has its own custom navigation and elements defined, there are two types of site maps now available in [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)]:</span><span class="sxs-lookup"><span data-stu-id="4aef7-110">With the introduction of modular business apps in the [!INCLUDE[pn_crm_8_2_0_online](../../includes/pn-crm-8-2-0-online.md)], where each app has its own custom navigation and elements defined, there are two types of site maps now available in [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)]:</span></span>  
  
- <span data-ttu-id="4aef7-111">Default site map that contains the navigation information for the default app (**[!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] - custom**).</span><span class="sxs-lookup"><span data-stu-id="4aef7-111">Default site map that contains the navigation information for the default app (**[!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] - custom**).</span></span> <span data-ttu-id="4aef7-112">This site map controls the navigation for your default [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="4aef7-112">This site map controls the navigation for your default [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] instance.</span></span>  
  
- <span data-ttu-id="4aef7-113">App-specific site maps that contain navigation information for a modular business app.</span><span class="sxs-lookup"><span data-stu-id="4aef7-113">App-specific site maps that contain navigation information for a modular business app.</span></span>  
  
  <span data-ttu-id="4aef7-114">You can use the `SiteMap.IsAppAware` attribute to distinguish between the two types of site maps: 0 indicates the default site map; 1 indicates the app-specific site map.</span><span class="sxs-lookup"><span data-stu-id="4aef7-114">You can use the `SiteMap.IsAppAware` attribute to distinguish between the two types of site maps: 0 indicates the default site map; 1 indicates the app-specific site map.</span></span>  
  
  <span data-ttu-id="4aef7-115">You can edit the default and app-specific site maps to change the application navigation, edit labels, add or change icons, or add or remove elements.</span><span class="sxs-lookup"><span data-stu-id="4aef7-115">You can edit the default and app-specific site maps to change the application navigation, edit labels, add or change icons, or add or remove elements.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="4aef7-116">[Change application navigation using the SiteMap](change-application-navigation-using-sitemap.md)</span><span class="sxs-lookup"><span data-stu-id="4aef7-116">[Change application navigation using the SiteMap](change-application-navigation-using-sitemap.md)</span></span>
  
  <span data-ttu-id="4aef7-117">You can use a site map editor or programmatically update site map.</span><span class="sxs-lookup"><span data-stu-id="4aef7-117">You can use a site map editor or programmatically update site map.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="4aef7-118">In This Section</span><span class="sxs-lookup"><span data-stu-id="4aef7-118">In This Section</span></span>  
 [<span data-ttu-id="4aef7-119">Change application navigation using the SiteMap</span><span class="sxs-lookup"><span data-stu-id="4aef7-119">Change application navigation using the SiteMap</span></span>](change-application-navigation-using-sitemap.md)  
  
 [<span data-ttu-id="4aef7-120">Pass parameters to a URL using the SiteMap</span><span class="sxs-lookup"><span data-stu-id="4aef7-120">Pass parameters to a URL using the SiteMap</span></span>](pass-parameters-url-using-sitemap.md)   
  
 [<span data-ttu-id="4aef7-121">SiteMap schema</span><span class="sxs-lookup"><span data-stu-id="4aef7-121">SiteMap schema</span></span>](sitemap-schema.md)  
  
### <a name="see-also"></a><span data-ttu-id="4aef7-122">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4aef7-122">See also</span></span>  
 <span data-ttu-id="4aef7-123">[Customize Microsoft Dynamics 365 for Customer Engagement applications](customize-applications.md) </span><span class="sxs-lookup"><span data-stu-id="4aef7-123">[Customize Microsoft Dynamics 365 for Customer Engagement applications](customize-applications.md) </span></span>  
 <!--[Define access permission for modular business apps in Dynamics 365 for Customer Engagement](../create-manage-business-apps.md) -->
