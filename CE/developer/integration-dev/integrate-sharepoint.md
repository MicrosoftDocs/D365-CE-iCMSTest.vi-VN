---
title: Integrate Dynamics 365 for Customer Engagement with SharePoint (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
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
ms.openlocfilehash: b95413dfcfc1c3b8368d059abd606409aeabca25
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387210"
---
# <a name="integrate-dynamics-365-for-customer-engagement-with-sharepoint"></a><span data-ttu-id="b8136-102">Integrate Dynamics 365 for Customer Engagement with SharePoint</span><span class="sxs-lookup"><span data-stu-id="b8136-102">Integrate Dynamics 365 for Customer Engagement with SharePoint</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_ms_sharepoint_server](../../includes/pn-ms-sharepoint-server.md)] <span data-ttu-id="b8136-103">is a collaboration and content management application that simplifies how people store, find, and share information.</span><span class="sxs-lookup"><span data-stu-id="b8136-103">is a collaboration and content management application that simplifies how people store, find, and share information.</span></span> <span data-ttu-id="b8136-104">It helps people to collaborate effectively by having secure access to documents and information that they require to make business decisions.</span><span class="sxs-lookup"><span data-stu-id="b8136-104">It helps people to collaborate effectively by having secure access to documents and information that they require to make business decisions.</span></span>  
  
 <span data-ttu-id="b8136-105">The [!INCLUDE[pn_SharePoint_short](../../includes/pn-sharepoint-short.md)] integration feature enables you to store and manage documents on [!INCLUDE[pn_SharePoint_short](../../includes/pn-sharepoint-short.md)] in the context of a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps record, and use the [!INCLUDE[pn_SharePoint_short](../../includes/pn-sharepoint-short.md)] document management abilities in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps, such as checking the document in and out, viewing version history, and changing document properties.</span><span class="sxs-lookup"><span data-stu-id="b8136-105">The [!INCLUDE[pn_SharePoint_short](../../includes/pn-sharepoint-short.md)] integration feature enables you to store and manage documents on [!INCLUDE[pn_SharePoint_short](../../includes/pn-sharepoint-short.md)] in the context of a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps record, and use the [!INCLUDE[pn_SharePoint_short](../../includes/pn-sharepoint-short.md)] document management abilities in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps, such as checking the document in and out, viewing version history, and changing document properties.</span></span>  
  
 [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] <span data-ttu-id="b8136-106">apps supports two types of integration with [!INCLUDE[pn_SharePoint_short](../../includes/pn-sharepoint-short.md)]: client-to-server and server-to-server (server-based).</span><span class="sxs-lookup"><span data-stu-id="b8136-106">apps supports two types of integration with [!INCLUDE[pn_SharePoint_short](../../includes/pn-sharepoint-short.md)]: client-to-server and server-to-server (server-based).</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b8136-107">[Enable SharePoint integration](get-started-sharepoint-integration.md#SPIntegration)</span><span class="sxs-lookup"><span data-stu-id="b8136-107">[Enable SharePoint integration](get-started-sharepoint-integration.md#SPIntegration)</span></span>  
  
 <span data-ttu-id="b8136-108">Use the `SharePointSite` and `SharePointDocumentLocation` entities to store and manage the [!INCLUDE[pn_SharePoint_Server_short](../../includes/pn-sharepoint-server-short.md)] location records in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], and the `UserMapping` entity to define custom claim mappings to use a value other than the default value used by [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] to authenticate and authorize [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] users in [!INCLUDE[pn_SharePoint_short](../../includes/pn-sharepoint-short.md)].</span><span class="sxs-lookup"><span data-stu-id="b8136-108">Use the `SharePointSite` and `SharePointDocumentLocation` entities to store and manage the [!INCLUDE[pn_SharePoint_Server_short](../../includes/pn-sharepoint-server-short.md)] location records in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], and the `UserMapping` entity to define custom claim mappings to use a value other than the default value used by [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] to authenticate and authorize [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] users in [!INCLUDE[pn_SharePoint_short](../../includes/pn-sharepoint-short.md)].</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b8136-109">In This Section</span><span class="sxs-lookup"><span data-stu-id="b8136-109">In This Section</span></span>  

[<span data-ttu-id="b8136-110">Understanding Microsoft Dynamics 365 for Customer Engagement apps and SharePoint Integration</span><span class="sxs-lookup"><span data-stu-id="b8136-110">Understanding Microsoft Dynamics 365 for Customer Engagement apps and SharePoint Integration</span></span>](get-started-sharepoint-integration.md)  
[<span data-ttu-id="b8136-111">Enable SharePoint Integration</span><span class="sxs-lookup"><span data-stu-id="b8136-111">Enable SharePoint Integration</span></span>](enable-document-management-entities.md)  
[<span data-ttu-id="b8136-112">Actions on SharePoint Location Records</span><span class="sxs-lookup"><span data-stu-id="b8136-112">Actions on SharePoint Location Records</span></span>](actions-on-sharepoint-location-records.md)  
[<span data-ttu-id="b8136-113">Define custom claim mapping for SharePoint server-based integration</span><span class="sxs-lookup"><span data-stu-id="b8136-113">Define custom claim mapping for SharePoint server-based integration</span></span>](define-custom-claim-mapping-sharepoint-server-based-integration.md)  
[<span data-ttu-id="b8136-114">Sample: Enable Document Management for Entities</span><span class="sxs-lookup"><span data-stu-id="b8136-114">Sample: Enable Document Management for Entities</span></span>](sample-enable-document-management-entities.md)  
[<span data-ttu-id="b8136-115">Sample: Create, Retrieve, Update, and Delete a SharePoint Location Record</span><span class="sxs-lookup"><span data-stu-id="b8136-115">Sample: Create, Retrieve, Update, and Delete a SharePoint Location Record</span></span>](sample-create-retrieve-update-delete-sharepoint-location-record.md)  
[<span data-ttu-id="b8136-116">Sample: Retrieve Absolute URL and Site Collection URL of a Location Record</span><span class="sxs-lookup"><span data-stu-id="b8136-116">Sample: Retrieve Absolute URL and Site Collection URL of a Location Record</span></span>](sample-retrieve-absolute-url-and-site-collection-url-of-a-location-record.md)  
  
## <a name="reference"></a><span data-ttu-id="b8136-117">Tham chiếu</span><span class="sxs-lookup"><span data-stu-id="b8136-117">Reference</span></span>  

[<span data-ttu-id="b8136-118">Manage your documents using SharePoint</span><span class="sxs-lookup"><span data-stu-id="b8136-118">Manage your documents using SharePoint</span></span>](https://technet.microsoft.com/library/dn531062.aspx)  
[<span data-ttu-id="b8136-119">SharePoint general development</span><span class="sxs-lookup"><span data-stu-id="b8136-119">SharePoint general development</span></span>](https://msdn.microsoft.com/sharepoint/default.aspx)  
<span data-ttu-id="b8136-120">[Overview of document management in SharePoint 2013](https://technet.microsoft.com/library/cc261933\(v=office.15\).aspx)</span><span class="sxs-lookup"><span data-stu-id="b8136-120">[Overview of document management in SharePoint 2013](https://technet.microsoft.com/library/cc261933\(v=office.15\).aspx)</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="b8136-121">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="b8136-121">Related Sections</span></span>  

<span data-ttu-id="b8136-122">[Extend Microsoft Dynamics 365 for Customer Engagement apps](../extend-dynamics-365-server.md) </span><span class="sxs-lookup"><span data-stu-id="b8136-122">[Extend Microsoft Dynamics 365 for Customer Engagement apps](../extend-dynamics-365-server.md) </span></span>  
[<span data-ttu-id="b8136-123">Integrate Microsoft Dynamics 365 for Customer Engagement apps with OneNote</span><span class="sxs-lookup"><span data-stu-id="b8136-123">Integrate Microsoft Dynamics 365 for Customer Engagement apps with OneNote</span></span>](integrate-onenote.md)
