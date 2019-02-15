---
title: Extend Dynamics 365 for Customer Engagement apps on the client (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn how developers can extend and customize Dynamics 365 for Customer Engagement apps in clients such as web applications, Dynamics 365 for phones, and Dynamics 365 for tablets by using JavaScript and web resources
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
- extending Microsoft Dynamics CRM and Dynamics CRM Online, building solutions and modeling your business data
- building solutions by extending Microsoft Dynamics CRM and Dynamics CRM Online
- modeling your business data by extending Microsoft Dynamics CRM and Dynamics CRM Online
- extending Microsoft Dynamics CRM and Dynamics CRM Online, introduction
- extending Microsoft Dynamics CRM and Dynamics CRM Online, with solutions; customizations; reports; plug-ins; processes; workflows; dashboards; SharePoint; and Outlook
ms.assetid: c6562c62-34fa-40c8-9f48-fae3e7d8b551
caps.latest.revision: 46
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4bfff5f692c5bd535f606ddee9dbf581a60c84fc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387374"
---
# <a name="extend-dynamics-365-for-customer-engagement-on-the-client"></a><span data-ttu-id="e45a9-103">Extend Dynamics 365 for Customer Engagement on the client</span><span class="sxs-lookup"><span data-stu-id="e45a9-103">Extend Dynamics 365 for Customer Engagement on the client</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e45a9-104">This section contains information about changes developers and customizers can make to extend [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps in the clients provided for [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps -- the web application, [!INCLUDE[pn_Microsoft_Dynamics_CRM_Mobile](../includes/pn-dyn-365-phones.md)], and [!INCLUDE[pn_moca_full](../includes/pn-moca-full.md)] -- by using [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] and web resources.</span><span class="sxs-lookup"><span data-stu-id="e45a9-104">This section contains information about changes developers and customizers can make to extend [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] apps in the clients provided for [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps -- the web application, [!INCLUDE[pn_Microsoft_Dynamics_CRM_Mobile](../includes/pn-dyn-365-phones.md)], and [!INCLUDE[pn_moca_full](../includes/pn-moca-full.md)] -- by using [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] and web resources.</span></span> <span data-ttu-id="e45a9-105">These clients are designed to allow you to add extensions that can be applied for all clients rather than each one separately.</span><span class="sxs-lookup"><span data-stu-id="e45a9-105">These clients are designed to allow you to add extensions that can be applied for all clients rather than each one separately.</span></span>  
  
 <span data-ttu-id="e45a9-106">Client extensions can provide a very rich and responsive experience for users because the code runs on their device.</span><span class="sxs-lookup"><span data-stu-id="e45a9-106">Client extensions can provide a very rich and responsive experience for users because the code runs on their device.</span></span> <span data-ttu-id="e45a9-107">However, critical business logic should not be applied only by client-side scripts.</span><span class="sxs-lookup"><span data-stu-id="e45a9-107">However, critical business logic should not be applied only by client-side scripts.</span></span> <span data-ttu-id="e45a9-108">Unlike extensions that are applied on the server, client extensions can’t apply business logic for data entering the system by other means, such as integrations with other systems, custom clients, or data import.</span><span class="sxs-lookup"><span data-stu-id="e45a9-108">Unlike extensions that are applied on the server, client extensions can’t apply business logic for data entering the system by other means, such as integrations with other systems, custom clients, or data import.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e45a9-109">In This Section</span><span class="sxs-lookup"><span data-stu-id="e45a9-109">In This Section</span></span>  
 [<span data-ttu-id="e45a9-110">Use JavaScript with Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="e45a9-110">Use JavaScript with Customer Engagement</span></span>](use-javascript.md)  
  
 [<span data-ttu-id="e45a9-111">Work with data using web resources</span><span class="sxs-lookup"><span data-stu-id="e45a9-111">Work with data using web resources</span></span>](work-data-using-web-resources.md) 
 
 [<span data-ttu-id="e45a9-112">Open Forms, Views, and Dialogs with a URL</span><span class="sxs-lookup"><span data-stu-id="e45a9-112">Open Forms, Views, and Dialogs with a URL</span></span>](open-forms-views-dialogs-reports-url.md)  
  
 [<span data-ttu-id="e45a9-113">Open forms, views, and dashboards in Dynamics 365 for Customer Engagement mobile client with a URL</span><span class="sxs-lookup"><span data-stu-id="e45a9-113">Open forms, views, and dashboards in Dynamics 365 for Customer Engagement mobile client with a URL</span></span>](open-forms-views-dashboards-mobile-client-url.md)  
  
 [<span data-ttu-id="e45a9-114">Web Resources for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="e45a9-114">Web Resources for Customer Engagement apps</span></span>](web-resources.md)  
  
## <a name="related-sections"></a><span data-ttu-id="e45a9-115">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="e45a9-115">Related Sections</span></span>  

[<span data-ttu-id="e45a9-116">Client scripting in Customer Engagement apps using JavaScript</span><span class="sxs-lookup"><span data-stu-id="e45a9-116">Client scripting in Customer Engagement apps using JavaScript</span></span>](clientapi/client-scripting.md)

[<span data-ttu-id="e45a9-117">Tùy chỉnh lệnh và ru băng</span><span class="sxs-lookup"><span data-stu-id="e45a9-117">Customize commands and the ribbon</span></span>](customize-dev/customize-commands-ribbon.md)
  
  
