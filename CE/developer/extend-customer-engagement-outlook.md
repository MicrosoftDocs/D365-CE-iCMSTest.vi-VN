---
title: Extend Dynamics 365 for Outlook (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Dynamics 365 for Outlook lets users interact with data while they’re offline and not connected to a server. Dynamics 365 for Customer Engagement apps includes features that let you extend your solutions to offline scenarios by calling the web services offline from your custom code. In addition, the Sdk assembly provides programmatic support for basic Outlook actions such as synchronization, going offline or online, and Dynamics 365 for Outlook state verification. Offline programming uses the ASP.NET Development Server.
ms.custom: ''
ms.date: 01/29/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- Outlook
ms.assetid: a5f6fe12-cb80-4ea7-a986-eb9543636bd8
caps.latest.revision: 28
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b60eb85e2e3bc424e58cab6fe595930fd8890a11
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385899"
---
# <a name="extend-dynamics-365-for-outlook"></a><span data-ttu-id="eb0af-106">Extend Dynamics 365 for Outlook</span><span class="sxs-lookup"><span data-stu-id="eb0af-106">Extend Dynamics 365 for Outlook</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

> [!IMPORTANT]
> <span data-ttu-id="eb0af-107">Kể từ ngày 29/1/2018, dựa trên rất nhiều phản hồi từ khách hàng và tâm niệm liên tục hỗ trợ khách hàng của chúng tôi, chúng tôi đã **quyết định không bỏ[!INCLUDE[pn-crm-2016-outlook-shortest](../includes/pn-crm-2016-outlook-shortest.md)]** (trình bổ sung [!INCLUDE[pn-outlook](../includes/pn-outlook.md)]).</span><span class="sxs-lookup"><span data-stu-id="eb0af-107">As of 1/29/2018, based on overwhelming customer feedback and our desire to continue supporting our customers, we have **decided not to deprecate [!INCLUDE[pn-crm-2016-outlook-shortest](../includes/pn-crm-2016-outlook-shortest.md)]** ([!INCLUDE[pn-outlook](../includes/pn-outlook.md)] add-in).</span></span> <span data-ttu-id="eb0af-108">Xin hãy đọc [bài đăng blog này](https://blogs.msdn.microsoft.com/crm/2018/01/29/continued-support-for-outlook-add-in-dynamics-365-for-outlook/) để biết thêm thông tin.</span><span class="sxs-lookup"><span data-stu-id="eb0af-108">Please read [this blog post](https://blogs.msdn.microsoft.com/crm/2018/01/29/continued-support-for-outlook-add-in-dynamics-365-for-outlook/) for more details.</span></span>

[!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] <span data-ttu-id="eb0af-109">lets users interact with data while they’re offline and not connected to a server.</span><span class="sxs-lookup"><span data-stu-id="eb0af-109">lets users interact with data while they’re offline and not connected to a server.</span></span> [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="eb0af-110">apps includes features that let you extend your solutions to offline scenarios by calling the web services offline from your custom code.</span><span class="sxs-lookup"><span data-stu-id="eb0af-110">apps includes features that let you extend your solutions to offline scenarios by calling the web services offline from your custom code.</span></span> <span data-ttu-id="eb0af-111">In addition, the <xref:Microsoft.Crm.Outlook.Sdk> assembly provides programmatic support for basic [!INCLUDE[pn_MS_Outlook_Short](../includes/pn-ms-outlook-short.md)] actions such as synchronization, going offline or online, and [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] state verification.</span><span class="sxs-lookup"><span data-stu-id="eb0af-111">In addition, the <xref:Microsoft.Crm.Outlook.Sdk> assembly provides programmatic support for basic [!INCLUDE[pn_MS_Outlook_Short](../includes/pn-ms-outlook-short.md)] actions such as synchronization, going offline or online, and [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] state verification.</span></span> <span data-ttu-id="eb0af-112">Offline programming uses the [!INCLUDE[pn_ms_asp_net_development_server](../includes/pn-ms-asp-net-development-server.md)].</span><span class="sxs-lookup"><span data-stu-id="eb0af-112">Offline programming uses the [!INCLUDE[pn_ms_asp_net_development_server](../includes/pn-ms-asp-net-development-server.md)].</span></span>  
  
 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="eb0af-113">apps include features that allow administrators to customize and manage filters for their users.</span><span class="sxs-lookup"><span data-stu-id="eb0af-113">apps include features that allow administrators to customize and manage filters for their users.</span></span> <span data-ttu-id="eb0af-114">Filter templates provide the starting point for entity synchronization on [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)].</span><span class="sxs-lookup"><span data-stu-id="eb0af-114">Filter templates provide the starting point for entity synchronization on [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)].</span></span> <span data-ttu-id="eb0af-115">Filters determine which entity collections are synchronized to [!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] and to [!INCLUDE[pn_MS_SQL_Express](../includes/pn-ms-sql-express.md)] for offline-enabled [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps solution.</span><span class="sxs-lookup"><span data-stu-id="eb0af-115">Filters determine which entity collections are synchronized to [!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] and to [!INCLUDE[pn_MS_SQL_Express](../includes/pn-ms-sql-express.md)] for offline-enabled [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps solution.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="eb0af-116">In This Section</span><span class="sxs-lookup"><span data-stu-id="eb0af-116">In This Section</span></span>   
 [<span data-ttu-id="eb0af-117">Offline and Outlook Filters and Templates</span><span class="sxs-lookup"><span data-stu-id="eb0af-117">Offline and Outlook Filters and Templates</span></span>](outlook-client/offline-outlook-filters-templates.md)<br />  
 [<span data-ttu-id="eb0af-118">Sample: Retrieve Outlook Filters</span><span class="sxs-lookup"><span data-stu-id="eb0af-118">Sample: Retrieve Outlook Filters</span></span>](outlook-client/sample-create-retrieve-outlook-filters.md)<br />  
 [<span data-ttu-id="eb0af-119">Sample: Use Outlook Methods</span><span class="sxs-lookup"><span data-stu-id="eb0af-119">Sample: Use Outlook Methods</span></span>](outlook-client/sample-outlook-methods.md)<br />
  
## <a name="related-sections"></a><span data-ttu-id="eb0af-120">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="eb0af-120">Related Sections</span></span>  
 [<span data-ttu-id="eb0af-121">Extend Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="eb0af-121">Extend Dynamics 365 for Customer Engagement apps</span></span>](extend-dynamics-365-server.md)<br />
 [<span data-ttu-id="eb0af-122">Supported Extensions for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="eb0af-122">Supported Extensions for Dynamics 365 for Customer Engagement apps</span></span>](supported-extensions.md)<br />
 [<span data-ttu-id="eb0af-123">The Metadata and Data Models in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="eb0af-123">The Metadata and Data Models in Dynamics 365 for Customer Engagement apps</span></span>](metadata-data-models.md)<br />
 [<span data-ttu-id="eb0af-124">Extend Dynamics 365 for Customer Engagement apps on the server</span><span class="sxs-lookup"><span data-stu-id="eb0af-124">Extend Dynamics 365 for Customer Engagement apps on the server</span></span>](extend-dynamics-365-server.md)<br />
 [<span data-ttu-id="eb0af-125">Extend Dynamics 365 for Customer Engagement apps on the client</span><span class="sxs-lookup"><span data-stu-id="eb0af-125">Extend Dynamics 365 for Customer Engagement apps on the client</span></span>](extend-client.md)<br />
 [<span data-ttu-id="eb0af-126">Customize Dynamics 365 for Customer Engagement apps applications</span><span class="sxs-lookup"><span data-stu-id="eb0af-126">Customize Dynamics 365 for Customer Engagement apps applications</span></span>](customize-dev/customize-applications.md)<br />
 [<span data-ttu-id="eb0af-127">Package and distribute extensions using solutions</span><span class="sxs-lookup"><span data-stu-id="eb0af-127">Package and distribute extensions using solutions</span></span>](package-distribute-extensions-use-solutions.md)<br />
 [<span data-ttu-id="eb0af-128">Integrate Dynamics 365 for Customer Engagement apps with SharePoint</span><span class="sxs-lookup"><span data-stu-id="eb0af-128">Integrate Dynamics 365 for Customer Engagement apps with SharePoint</span></span>](integration-dev/integrate-sharepoint.md)<br />
 [<span data-ttu-id="eb0af-129">Integrate Dynamics 365 for Customer Engagement apps with OneNote</span><span class="sxs-lookup"><span data-stu-id="eb0af-129">Integrate Dynamics 365 for Customer Engagement apps with OneNote</span></span>](integration-dev/integrate-onenote.md)<br />
 <xref href="Microsoft.Dynamics.CRM.savedquery?text=savedquery EntityType" /><br />
 [<span data-ttu-id="eb0af-130">SavedQuery Entity</span><span class="sxs-lookup"><span data-stu-id="eb0af-130">SavedQuery Entity</span></span>](entities/savedquery.md)<br />
  

