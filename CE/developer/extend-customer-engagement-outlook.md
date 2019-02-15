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
# <a name="extend-dynamics-365-for-outlook"></a>Extend Dynamics 365 for Outlook

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

> [!IMPORTANT]
> Kể từ ngày 29/1/2018, dựa trên rất nhiều phản hồi từ khách hàng và tâm niệm liên tục hỗ trợ khách hàng của chúng tôi, chúng tôi đã **quyết định không bỏ[!INCLUDE[pn-crm-2016-outlook-shortest](../includes/pn-crm-2016-outlook-shortest.md)]** (trình bổ sung [!INCLUDE[pn-outlook](../includes/pn-outlook.md)]). Xin hãy đọc [bài đăng blog này](https://blogs.msdn.microsoft.com/crm/2018/01/29/continued-support-for-outlook-add-in-dynamics-365-for-outlook/) để biết thêm thông tin.

[!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] lets users interact with data while they’re offline and not connected to a server. [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps includes features that let you extend your solutions to offline scenarios by calling the web services offline from your custom code. In addition, the <xref:Microsoft.Crm.Outlook.Sdk> assembly provides programmatic support for basic [!INCLUDE[pn_MS_Outlook_Short](../includes/pn-ms-outlook-short.md)] actions such as synchronization, going offline or online, and [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] state verification. Offline programming uses the [!INCLUDE[pn_ms_asp_net_development_server](../includes/pn-ms-asp-net-development-server.md)].  
  
 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps include features that allow administrators to customize and manage filters for their users. Filter templates provide the starting point for entity synchronization on [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)]. Filters determine which entity collections are synchronized to [!INCLUDE[pn_Outlook_short](../includes/pn-outlook-short.md)] and to [!INCLUDE[pn_MS_SQL_Express](../includes/pn-ms-sql-express.md)] for offline-enabled [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps solution.  
  
## <a name="in-this-section"></a>In This Section   
 [Offline and Outlook Filters and Templates](outlook-client/offline-outlook-filters-templates.md)<br />  
 [Sample: Retrieve Outlook Filters](outlook-client/sample-create-retrieve-outlook-filters.md)<br />  
 [Sample: Use Outlook Methods](outlook-client/sample-outlook-methods.md)<br />
  
## <a name="related-sections"></a>Các phần liên quan  
 [Extend Dynamics 365 for Customer Engagement apps](extend-dynamics-365-server.md)<br />
 [Supported Extensions for Dynamics 365 for Customer Engagement apps](supported-extensions.md)<br />
 [The Metadata and Data Models in Dynamics 365 for Customer Engagement apps](metadata-data-models.md)<br />
 [Extend Dynamics 365 for Customer Engagement apps on the server](extend-dynamics-365-server.md)<br />
 [Extend Dynamics 365 for Customer Engagement apps on the client](extend-client.md)<br />
 [Customize Dynamics 365 for Customer Engagement apps applications](customize-dev/customize-applications.md)<br />
 [Package and distribute extensions using solutions](package-distribute-extensions-use-solutions.md)<br />
 [Integrate Dynamics 365 for Customer Engagement apps with SharePoint](integration-dev/integrate-sharepoint.md)<br />
 [Integrate Dynamics 365 for Customer Engagement apps with OneNote](integration-dev/integrate-onenote.md)<br />
 <xref href="Microsoft.Dynamics.CRM.savedquery?text=savedquery EntityType" /><br />
 [SavedQuery Entity](entities/savedquery.md)<br />
  

