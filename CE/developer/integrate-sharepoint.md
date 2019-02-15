---
title: Integrate Dynamics 365 for Customer Engagement with SharePoint (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The SharePoint integration feature enables you to store and manage documents on SharePoint in the context of a Dynamics 365 for Customer Engagement apps record, and use the SharePoint document management abilities in Dynamics 365 for Customer Engagement apps, such as checking the document in and out, viewing version history, and changing document properties.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: fc7f8994-a531-48d1-8495-3f8663f6c3e3
caps.latest.revision: 52
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f5a0faf2aa24d260310350b1fec5287d51e62935
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386422"
---
# <a name="integrate-dynamics-365-for-customer-engagement-apps-with-sharepoint"></a><span data-ttu-id="e3ff5-103">Integrate Dynamics 365 for Customer Engagement apps with SharePoint</span><span class="sxs-lookup"><span data-stu-id="e3ff5-103">Integrate Dynamics 365 for Customer Engagement apps with SharePoint</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_ms_sharepoint_server](../includes/pn-ms-sharepoint-server.md)] <span data-ttu-id="e3ff5-104">is a collaboration and content management application that simplifies how people store, find, and share information.</span><span class="sxs-lookup"><span data-stu-id="e3ff5-104">is a collaboration and content management application that simplifies how people store, find, and share information.</span></span> <span data-ttu-id="e3ff5-105">It helps people to collaborate effectively by having secure access to documents and information that they require to make business decisions.</span><span class="sxs-lookup"><span data-stu-id="e3ff5-105">It helps people to collaborate effectively by having secure access to documents and information that they require to make business decisions.</span></span>  
  
 <span data-ttu-id="e3ff5-106">The [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] integration feature enables you to store and manage documents on [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] in the context of a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps record, and use the [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] apps document management abilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, such as checking the document in and out, viewing version history, and changing document properties.</span><span class="sxs-lookup"><span data-stu-id="e3ff5-106">The [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] integration feature enables you to store and manage documents on [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] in the context of a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps record, and use the [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] apps document management abilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, such as checking the document in and out, viewing version history, and changing document properties.</span></span>  
  
 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="e3ff5-107">apps support two types of integration with [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] apps: client-to-server and server-to-server (server-based).</span><span class="sxs-lookup"><span data-stu-id="e3ff5-107">apps support two types of integration with [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] apps: client-to-server and server-to-server (server-based).</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="e3ff5-108">[Enable SharePoint integration](integration-dev/get-started-sharepoint-integration.md#SPIntegration)</span><span class="sxs-lookup"><span data-stu-id="e3ff5-108">[Enable SharePoint integration](integration-dev/get-started-sharepoint-integration.md#SPIntegration)</span></span>  
  
 <span data-ttu-id="e3ff5-109">Use the `SharePointSite` and `SharePointDocumentLocation` entities to store and manage the [!INCLUDE[pn_SharePoint_Server_short](../includes/pn-sharepoint-server-short.md)] location records in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps, and the `UserMapping` entity to define custom claim mappings to use a value other than the default value used by [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] apps to authenticate and authorize [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps user in [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)].</span><span class="sxs-lookup"><span data-stu-id="e3ff5-109">Use the `SharePointSite` and `SharePointDocumentLocation` entities to store and manage the [!INCLUDE[pn_SharePoint_Server_short](../includes/pn-sharepoint-server-short.md)] location records in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps, and the `UserMapping` entity to define custom claim mappings to use a value other than the default value used by [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] apps to authenticate and authorize [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps user in [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)].</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e3ff5-110">In This Section</span><span class="sxs-lookup"><span data-stu-id="e3ff5-110">In This Section</span></span>  
 [<span data-ttu-id="e3ff5-111">Understanding Dynamics 365 for Customer Engagement apps and SharePoint Integration</span><span class="sxs-lookup"><span data-stu-id="e3ff5-111">Understanding Dynamics 365 for Customer Engagement apps and SharePoint Integration</span></span>](integration-dev/get-started-sharepoint-integration.md)  
  
 [<span data-ttu-id="e3ff5-112">Enable SharePoint Integration</span><span class="sxs-lookup"><span data-stu-id="e3ff5-112">Enable SharePoint Integration</span></span>](integration-dev/enable-document-management-entities.md)  
  
 [<span data-ttu-id="e3ff5-113">Actions on SharePoint Location Records</span><span class="sxs-lookup"><span data-stu-id="e3ff5-113">Actions on SharePoint Location Records</span></span>](integration-dev/actions-on-sharepoint-location-records.md)  
  
 [<span data-ttu-id="e3ff5-114">Define custom claim mapping for SharePoint server-based integration</span><span class="sxs-lookup"><span data-stu-id="e3ff5-114">Define custom claim mapping for SharePoint server-based integration</span></span>](integration-dev/define-custom-claim-mapping-sharepoint-server-based-integration.md)  
  
 [<span data-ttu-id="e3ff5-115">Sample: Enable Document Management for Entities</span><span class="sxs-lookup"><span data-stu-id="e3ff5-115">Sample: Enable Document Management for Entities</span></span>](integration-dev/sample-enable-document-management-entities.md)  
  
 [<span data-ttu-id="e3ff5-116">Sample: Create, Retrieve, Update, and Delete a SharePoint Location Record</span><span class="sxs-lookup"><span data-stu-id="e3ff5-116">Sample: Create, Retrieve, Update, and Delete a SharePoint Location Record</span></span>](integration-dev/sample-create-retrieve-update-delete-sharepoint-location-record.md)  
  
 [<span data-ttu-id="e3ff5-117">Sample: Retrieve Absolute URL and Site Collection URL of a Location Record</span><span class="sxs-lookup"><span data-stu-id="e3ff5-117">Sample: Retrieve Absolute URL and Site Collection URL of a Location Record</span></span>](integration-dev/sample-retrieve-absolute-url-and-site-collection-url-of-a-location-record.md)  
  
## <a name="reference"></a><span data-ttu-id="e3ff5-118">Tham chiếu</span><span class="sxs-lookup"><span data-stu-id="e3ff5-118">Reference</span></span>  
 [<span data-ttu-id="e3ff5-119">Manage your documents using SharePoint</span><span class="sxs-lookup"><span data-stu-id="e3ff5-119">Manage your documents using SharePoint</span></span>](../admin/manage-documents-using-sharepoint.md)  
  
 [<span data-ttu-id="e3ff5-120">Office and SharePoint development</span><span class="sxs-lookup"><span data-stu-id="e3ff5-120">Office and SharePoint development</span></span>](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio)  
   
## <a name="related-sections"></a><span data-ttu-id="e3ff5-121">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="e3ff5-121">Related Sections</span></span>  
 [<span data-ttu-id="e3ff5-122">Extend Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="e3ff5-122">Extend Dynamics 365 for Customer Engagement apps</span></span>](extend-dynamics-365-server.md)  
  
 [<span data-ttu-id="e3ff5-123">Supported Extensions for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="e3ff5-123">Supported Extensions for Dynamics 365 for Customer Engagement apps</span></span>](supported-extensions.md)  
  
 [<span data-ttu-id="e3ff5-124">The Metadata and Data Models in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="e3ff5-124">The Metadata and Data Models in Dynamics 365 for Customer Engagement apps</span></span>](metadata-data-models.md)  
  
 [<span data-ttu-id="e3ff5-125">Extend Dynamics 365 for Customer Engagement on the server apps</span><span class="sxs-lookup"><span data-stu-id="e3ff5-125">Extend Dynamics 365 for Customer Engagement on the server apps</span></span>](extend-dynamics-365-server.md)  
  
 [<span data-ttu-id="e3ff5-126">Extend Dynamics 365 for Customer Engagement on the client apps</span><span class="sxs-lookup"><span data-stu-id="e3ff5-126">Extend Dynamics 365 for Customer Engagement on the client apps</span></span>](extend-client.md)  
  
 [<span data-ttu-id="e3ff5-127">Customize Dynamics 365 for Customer Engagement applications</span><span class="sxs-lookup"><span data-stu-id="e3ff5-127">Customize Dynamics 365 for Customer Engagement applications</span></span>](customize-dev/customize-applications.md)  
  
 [<span data-ttu-id="e3ff5-128">Package and distribute extensions using solutions</span><span class="sxs-lookup"><span data-stu-id="e3ff5-128">Package and distribute extensions using solutions</span></span>](package-distribute-extensions-use-solutions.md)  
  
 [<span data-ttu-id="e3ff5-129">Extend Dynamics 365 for Outlook</span><span class="sxs-lookup"><span data-stu-id="e3ff5-129">Extend Dynamics 365 for Outlook</span></span>](extend-customer-engagement-outlook.md)  
  
 [<span data-ttu-id="e3ff5-130">Integrate Dynamics 365 for Customer Engagement apps with OneNote</span><span class="sxs-lookup"><span data-stu-id="e3ff5-130">Integrate Dynamics 365 for Customer Engagement apps with OneNote</span></span>](integration-dev/integrate-onenote.md) 
  
 
