---
title: Pass parameters to a URL using the SiteMap  (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn about passing parameters to a URL using the SiteMap
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 979da39a-2d15-4564-84d8-86dd0bcf3c38
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e1559737a20aadbf86df4c95e0019a60e3f7b205
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386042"
---
# <a name="pass-parameters-to-a-url-using-the-sitemap"></a><span data-ttu-id="1cc88-103">Pass parameters to a URL using the SiteMap</span><span class="sxs-lookup"><span data-stu-id="1cc88-103">Pass parameters to a URL using the SiteMap</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1cc88-104">To give the target application information about the organization and the language context of the user and organization, pass parameters to the target URL for a `<SubArea>` element in the site map.</span><span class="sxs-lookup"><span data-stu-id="1cc88-104">To give the target application information about the organization and the language context of the user and organization, pass parameters to the target URL for a `<SubArea>` element in the site map.</span></span> <span data-ttu-id="1cc88-105">All the parameters are passed if the `<SubArea>` element is configured by setting the `PassParams` attribute to `true`.</span><span class="sxs-lookup"><span data-stu-id="1cc88-105">All the parameters are passed if the `<SubArea>` element is configured by setting the `PassParams` attribute to `true`.</span></span>  
  
 <span data-ttu-id="1cc88-106">The following table shows the parameters that are passed.</span><span class="sxs-lookup"><span data-stu-id="1cc88-106">The following table shows the parameters that are passed.</span></span>  
  
|<span data-ttu-id="1cc88-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="1cc88-107">Parameter</span></span>|<span data-ttu-id="1cc88-108">Tên</span><span class="sxs-lookup"><span data-stu-id="1cc88-108">Name</span></span>|<span data-ttu-id="1cc88-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="1cc88-109">Description</span></span>|  
|---------------|----------|-----------------|  
|<span data-ttu-id="1cc88-110">orgname</span><span class="sxs-lookup"><span data-stu-id="1cc88-110">orgname</span></span>|<span data-ttu-id="1cc88-111">Tên tổ chức</span><span class="sxs-lookup"><span data-stu-id="1cc88-111">Organization Name</span></span>|<span data-ttu-id="1cc88-112">Unique name of the organization.</span><span class="sxs-lookup"><span data-stu-id="1cc88-112">Unique name of the organization.</span></span>|  
|<span data-ttu-id="1cc88-113">userlcid</span><span class="sxs-lookup"><span data-stu-id="1cc88-113">userlcid</span></span>|<span data-ttu-id="1cc88-114">User Language Code</span><span class="sxs-lookup"><span data-stu-id="1cc88-114">User Language Code</span></span>|<span data-ttu-id="1cc88-115">Language code ID that is used by the current user.</span><span class="sxs-lookup"><span data-stu-id="1cc88-115">Language code ID that is used by the current user.</span></span>|  
|<span data-ttu-id="1cc88-116">orglcid</span><span class="sxs-lookup"><span data-stu-id="1cc88-116">orglcid</span></span>|<span data-ttu-id="1cc88-117">Organization Language Code</span><span class="sxs-lookup"><span data-stu-id="1cc88-117">Organization Language Code</span></span>|<span data-ttu-id="1cc88-118">Language code identifier that represents the base language for the organization.</span><span class="sxs-lookup"><span data-stu-id="1cc88-118">Language code identifier that represents the base language for the organization.</span></span>|  
  
[!INCLUDE[languagecode](../../includes/languagecode.md)]
  
 <span data-ttu-id="1cc88-119">**Ví dụ**</span><span class="sxs-lookup"><span data-stu-id="1cc88-119">**Example**</span></span>  
  
 <span data-ttu-id="1cc88-120">The following sample shows the URL without parameters.</span><span class="sxs-lookup"><span data-stu-id="1cc88-120">The following sample shows the URL without parameters.</span></span>  
  
```  
http://myserver/mypage.aspx  
```  
  
 <span data-ttu-id="1cc88-121">The following sample shows the URL with parameters.</span><span class="sxs-lookup"><span data-stu-id="1cc88-121">The following sample shows the URL with parameters.</span></span>  
  
```  
http://myserver/mypage.aspx?orgname=AdventureWorksCycle&userlcid=1033&orglcid=1033  
```  
  
### <a name="reading-passed-parameters"></a><span data-ttu-id="1cc88-122">Reading passed parameters</span><span class="sxs-lookup"><span data-stu-id="1cc88-122">Reading passed parameters</span></span>  
 <span data-ttu-id="1cc88-123">Webpage (HTML) web resources will accept these parameters.</span><span class="sxs-lookup"><span data-stu-id="1cc88-123">Webpage (HTML) web resources will accept these parameters.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="1cc88-124">[Passing parameters to HTML web resources](../webpage-html-web-resources.md#BKMK_PassingParametersToWebResources)</span><span class="sxs-lookup"><span data-stu-id="1cc88-124">[Passing parameters to HTML web resources](../webpage-html-web-resources.md#BKMK_PassingParametersToWebResources)</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1cc88-125">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1cc88-125">See also</span></span>  
 <span data-ttu-id="1cc88-126">[Change Application Navigation using the SiteMap](/developer/customize-dev/change-application-navigation-using-sitemap.md)  </span><span class="sxs-lookup"><span data-stu-id="1cc88-126">[Change Application Navigation using the SiteMap](/developer/customize-dev/change-application-navigation-using-sitemap.md)  </span></span>  
 [<span data-ttu-id="1cc88-127">SiteMap schema</span><span class="sxs-lookup"><span data-stu-id="1cc88-127">SiteMap schema</span></span>](sitemap-schema.md)  
