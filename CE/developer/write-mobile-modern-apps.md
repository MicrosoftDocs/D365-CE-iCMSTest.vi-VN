---
title: Write mobile and modern apps (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Dynamics 365 for Customer Engagement apps provide separate clients for phones and tablets which adapt to system customizations and configurations
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
- mobile, modern,app
ms.assetid: 16d118f7-b8fa-4a23-8e56-6148669d3bc0
caps.latest.revision: 24
author: SushantSikka
ms.author: susikka
manager: sakudes
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4a33a36667122eb1da4df1570ed2e2a800bc91e9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387099"
---
# <a name="write-mobile-and-modern-apps"></a><span data-ttu-id="622c1-103">Write mobile and modern apps</span><span class="sxs-lookup"><span data-stu-id="622c1-103">Write mobile and modern apps</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<!-- TODO: Do you really mean to refer to only crm online in this intro? -->

[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="622c1-104">apps provide separate clients for phones and tablets which adapt to the customizations and configurations you apply to the system.</span><span class="sxs-lookup"><span data-stu-id="622c1-104">apps provide separate clients for phones and tablets which adapt to the customizations and configurations you apply to the system.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="622c1-105">[Dynamics 365 for phones and Tablets User's Guide](../mobile-app/dynamics-365-phones-tablets-users-guide.md).</span><span class="sxs-lookup"><span data-stu-id="622c1-105">[Dynamics 365 for phones and Tablets User's Guide](../mobile-app/dynamics-365-phones-tablets-users-guide.md).</span></span>

<span data-ttu-id="622c1-106">Organizations can use the mobile development tools and libraries to easily create and deploy mobile apps that offer additional functionality to what is available on Dynamics 365 for Customer Engagement for Phones and Tablets.</span><span class="sxs-lookup"><span data-stu-id="622c1-106">Organizations can use the mobile development tools and libraries to easily create and deploy mobile apps that offer additional functionality to what is available on Dynamics 365 for Customer Engagement for Phones and Tablets.</span></span>

<span data-ttu-id="622c1-107">Here are four scenarios where you can create mobile apps that leverage the Microsoft Dynamics CRM platform to provide additional value to the organization:</span><span class="sxs-lookup"><span data-stu-id="622c1-107">Here are four scenarios where you can create mobile apps that leverage the Microsoft Dynamics CRM platform to provide additional value to the organization:</span></span>

|<span data-ttu-id="622c1-108">Cơ hội</span><span class="sxs-lookup"><span data-stu-id="622c1-108">Opportunity</span></span>|<span data-ttu-id="622c1-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="622c1-109">Description</span></span>|
|-----|-----|
|<span data-ttu-id="622c1-110">Task specific apps</span><span class="sxs-lookup"><span data-stu-id="622c1-110">Task specific apps</span></span>|<span data-ttu-id="622c1-111">Create rich mobile apps that merge Dynamics 365 for Customer Engagement apps data with data from multiple systems, such as ERP, Billing or Help Desk for a very concise mobile experience.</span><span class="sxs-lookup"><span data-stu-id="622c1-111">Create rich mobile apps that merge Dynamics 365 for Customer Engagement apps data with data from multiple systems, such as ERP, Billing or Help Desk for a very concise mobile experience.</span></span>|
|<span data-ttu-id="622c1-112">Aggregate multiple systems</span><span class="sxs-lookup"><span data-stu-id="622c1-112">Aggregate multiple systems</span></span>|<span data-ttu-id="622c1-113">Create mobile apps with a streamlined user experience which target activities people frequently perform using Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="622c1-113">Create mobile apps with a streamlined user experience which target activities people frequently perform using Dynamics 365 for Customer Engagement apps.</span></span>|
|<span data-ttu-id="622c1-114">Self-service enablement</span><span class="sxs-lookup"><span data-stu-id="622c1-114">Self-service enablement</span></span>|<span data-ttu-id="622c1-115">Create mobile apps that can be used by your customers and that can feed data back directly to Dynamics 365 for Customer Engagement apps to enable scenarios such as event registration or loyalty program apps.</span><span class="sxs-lookup"><span data-stu-id="622c1-115">Create mobile apps that can be used by your customers and that can feed data back directly to Dynamics 365 for Customer Engagement apps to enable scenarios such as event registration or loyalty program apps.</span></span>|
|<span data-ttu-id="622c1-116">Device specific experiences</span><span class="sxs-lookup"><span data-stu-id="622c1-116">Device specific experiences</span></span>|<span data-ttu-id="622c1-117">Create rich mobile apps for Dynamics 365 for Customer Engagement apps that leverage the capabilities of modern mobile devices, such as GPS, camera, biometric security, and mobile payments.</span><span class="sxs-lookup"><span data-stu-id="622c1-117">Create rich mobile apps for Dynamics 365 for Customer Engagement apps that leverage the capabilities of modern mobile devices, such as GPS, camera, biometric security, and mobile payments.</span></span>|
   
## <a name="getting-started"></a><span data-ttu-id="622c1-118">Bắt đầu</span><span class="sxs-lookup"><span data-stu-id="622c1-118">Getting started</span></span> 
  
[<span data-ttu-id="622c1-119">Walkthrough: Register an app with Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="622c1-119">Walkthrough: Register an app with Azure Active Directory</span></span>](walkthrough-register-dynamics-365-app-azure-active-directory.md)  

<span data-ttu-id="622c1-120">Resources for getting started with mobile app development:</span><span class="sxs-lookup"><span data-stu-id="622c1-120">Resources for getting started with mobile app development:</span></span>

* [<span data-ttu-id="622c1-121">Resources for Android mobile application development</span><span class="sxs-lookup"><span data-stu-id="622c1-121">Resources for Android mobile application development</span></span>](android-mobile-app-development.md)
* [<span data-ttu-id="622c1-122">Resources for iOS mobile application development</span><span class="sxs-lookup"><span data-stu-id="622c1-122">Resources for iOS mobile application development</span></span>](ios-mobile-app-development.md)
* [<span data-ttu-id="622c1-123">Hỏi cộng đồng</span><span class="sxs-lookup"><span data-stu-id="622c1-123">Ask the community</span></span>](https://community.dynamics.com/search#q=section%3A117+%26%26+tag%3A%22Mobile+App+Development%22&group=57)
 
## <a name="see-also"></a><span data-ttu-id="622c1-124">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="622c1-124">See Also</span></span>  

[<span data-ttu-id="622c1-125">Azure Mobile Connector SDK for Dynamics 365 for Customer Engagement Online</span><span class="sxs-lookup"><span data-stu-id="622c1-125">Azure Mobile Connector SDK for Dynamics 365 for Customer Engagement Online</span></span>](https://github.com/Azure/mobile-services-dynamics-connector)<br /><span data-ttu-id="622c1-126"> 
[CRM Service Utility for Mobile development](https://github.com/DynamicsCRM/crm-mobilesdk-tool-svcutil)</span><span class="sxs-lookup"><span data-stu-id="622c1-126"> 
[CRM Service Utility for Mobile development](https://github.com/DynamicsCRM/crm-mobilesdk-tool-svcutil)</span></span>
 
## <a name="related-sections"></a><span data-ttu-id="622c1-127">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="622c1-127">Related Sections</span></span>
  
[<span data-ttu-id="622c1-128">Developer Guide for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="622c1-128">Developer Guide for Dynamics 365 for Customer Engagement apps</span></span>](developer-guide.md)<br /><span data-ttu-id="622c1-129"> 
[Mobile Development Helper Code for Dynamics CRM](http://code.msdn.microsoft.com/Mobile-Development-Helper-3213e2e6)</span><span class="sxs-lookup"><span data-stu-id="622c1-129"> 
[Mobile Development Helper Code for Dynamics CRM](http://code.msdn.microsoft.com/Mobile-Development-Helper-3213e2e6)</span></span><br /><span data-ttu-id="622c1-130"> 
[odata.org](http://www.odata.org)</span><span class="sxs-lookup"><span data-stu-id="622c1-130"> 
[odata.org](http://www.odata.org)</span></span><br /> 
