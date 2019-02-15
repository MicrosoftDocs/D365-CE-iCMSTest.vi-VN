---
title: Use Single-Tenant Server-to-server authentication | MicrosoftDocs
description: An enterprise can create a web application or service to connect to all the Dynamics 365 for Customer Engagement (online) organizations for the single tenant
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: e238f839-3592-44c4-9f82-dc287551c581
caps.latest.revision: 7
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8bfb89bdc4c6ff29c4f02d9e1181dc99d9fdf18b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386830"
---
# <a name="use-single-tenant-server-to-server-authentication"></a><span data-ttu-id="37acc-103">Use Single-Tenant Server-to-server authentication</span><span class="sxs-lookup"><span data-stu-id="37acc-103">Use Single-Tenant Server-to-server authentication</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="37acc-104">The single-tenant server-to-server scenario typically applies for enterprise organizations who have multiple [!INCLUDE[pn_crm_8_2_0_online](../includes/pn-crm-8-2-0-online.md)] organizations using [!INCLUDE[pn_Active_Dir_Fed_Svcs_AD_FS](../includes/pn-active-dir-fed-svcs-ad-fs.md)] for authentication.</span><span class="sxs-lookup"><span data-stu-id="37acc-104">The single-tenant server-to-server scenario typically applies for enterprise organizations who have multiple [!INCLUDE[pn_crm_8_2_0_online](../includes/pn-crm-8-2-0-online.md)] organizations using [!INCLUDE[pn_Active_Dir_Fed_Svcs_AD_FS](../includes/pn-active-dir-fed-svcs-ad-fs.md)] for authentication.</span></span> <span data-ttu-id="37acc-105">However, it can also be applied by organizations using [!INCLUDE[pn_crm_8_2_0_online_subsequent](../includes/pn-crm-8-2-0-online-subsequent.md)] when the application will not be distributed to other [!INCLUDE[pn_dyn_365_online](../includes/pn-crm-online.md)] organizations.</span><span class="sxs-lookup"><span data-stu-id="37acc-105">However, it can also be applied by organizations using [!INCLUDE[pn_crm_8_2_0_online_subsequent](../includes/pn-crm-8-2-0-online-subsequent.md)] when the application will not be distributed to other [!INCLUDE[pn_dyn_365_online](../includes/pn-crm-online.md)] organizations.</span></span>  
  
 <span data-ttu-id="37acc-106">An enterprise can create a web application or service to connect to all the [!INCLUDE[pn_dyn_365_online](../includes/pn-crm-online.md)] organizations for the single tenant.</span><span class="sxs-lookup"><span data-stu-id="37acc-106">An enterprise can create a web application or service to connect to all the [!INCLUDE[pn_dyn_365_online](../includes/pn-crm-online.md)] organizations for the single tenant.</span></span>  
  
## <a name="differences-from-multi-tenant-scenario"></a><span data-ttu-id="37acc-107">Differences from multi-tenant scenario</span><span class="sxs-lookup"><span data-stu-id="37acc-107">Differences from multi-tenant scenario</span></span>  
 <span data-ttu-id="37acc-108">Creating a web application or service for a single-tenant server-to-server authentication is similar to that used for a multi-tenant organization but there are some important differences.</span><span class="sxs-lookup"><span data-stu-id="37acc-108">Creating a web application or service for a single-tenant server-to-server authentication is similar to that used for a multi-tenant organization but there are some important differences.</span></span>  
  
-   <span data-ttu-id="37acc-109">Because all the organizations are in the same tenant, there is no need for a tenant admin to grant consent.</span><span class="sxs-lookup"><span data-stu-id="37acc-109">Because all the organizations are in the same tenant, there is no need for a tenant admin to grant consent.</span></span> <span data-ttu-id="37acc-110">The application is already registered on the tenant.</span><span class="sxs-lookup"><span data-stu-id="37acc-110">The application is already registered on the tenant.</span></span>  
  
-   <span data-ttu-id="37acc-111">You have the opportunity to use certificates rather than keys if you prefer.</span><span class="sxs-lookup"><span data-stu-id="37acc-111">You have the opportunity to use certificates rather than keys if you prefer.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="37acc-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="37acc-112">See also</span></span>  
 <span data-ttu-id="37acc-113">[Use Multi-Tenant Server-to-server authentication](use-multi-tenant-server-server-authentication.md) </span><span class="sxs-lookup"><span data-stu-id="37acc-113">[Use Multi-Tenant Server-to-server authentication](use-multi-tenant-server-server-authentication.md) </span></span>  
 <span data-ttu-id="37acc-114">[Build web applications using Server-to-Server (S2S) authentication](build-web-applications-server-server-s2s-authentication.md) </span><span class="sxs-lookup"><span data-stu-id="37acc-114">[Build web applications using Server-to-Server (S2S) authentication](build-web-applications-server-server-s2s-authentication.md) </span></span>  
 [<span data-ttu-id="37acc-115">Connect to Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="37acc-115">Connect to Dynamics 365 for Customer Engagement</span></span>](connect-customer-engagement.md)
