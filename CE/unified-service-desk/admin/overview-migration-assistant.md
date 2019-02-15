---
title: Migrate Dynamics 365 for Customer Engagement Web Client configurations to Dynamics 365 for Customer Engagement apps (Unified Interface apps) | MicrosoftDocs
description: Learn how to migrate your Unified Service Desk configurations from Dynamics 365 for Customer Engagement Web Client to Unified Interface apps
keywords: ''
ms.date: 07/30/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD, dyn365-admin
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 785880FF-00C7-489F-BC2D-2C45ECBFF3C9
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 64cad1bfd7c0da41292ad05812cfcf61270d9c45
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382540"
---
# <a name="migration-of-unified-service-desk-configurations-from-dynamics-365-for-customer-engagementa-web-client-to-dynamics-365-for-customer-engagement-unified-interface-apps"></a><span data-ttu-id="bb6f5-103">Migration of Unified Service Desk configurations from Dynamics 365 for Customer Engagementa Web Client to Dynamics 365 for Customer Engagement Unified Interface apps</span><span class="sxs-lookup"><span data-stu-id="bb6f5-103">Migration of Unified Service Desk configurations from Dynamics 365 for Customer Engagementa Web Client to Dynamics 365 for Customer Engagement Unified Interface apps</span></span>

## <a name="overview"></a><span data-ttu-id="bb6f5-104">Tổng quan</span><span class="sxs-lookup"><span data-stu-id="bb6f5-104">Overview</span></span>
  
[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="bb6f5-105">supports Unified Interface apps.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-105">supports Unified Interface apps.</span></span> <span data-ttu-id="bb6f5-106">This lets you to upgrade to the latest version of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to deliver intelligent and personalized experience to the rising expectations of your customers.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-106">This lets you to upgrade to the latest version of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to deliver intelligent and personalized experience to the rising expectations of your customers.</span></span>

<span data-ttu-id="bb6f5-107">If you are using [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web Client with all the configurations needed for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], you will want to know how to use all the configurations in the Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-107">If you are using [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web Client with all the configurations needed for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], you will want to know how to use all the configurations in the Unified Interface App.</span></span> <span data-ttu-id="bb6f5-108">To tackle the issue of configuring in the Unified Interface App, we have introduced a tool, **[!INCLUDE[pn-web-client-unified-interface-configuration-migration-assistant](../../includes/pn-web-client-unified-interface-configuration-migration-assistant.md)]**, for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="bb6f5-108">To tackle the issue of configuring in the Unified Interface App, we have introduced a tool, **[!INCLUDE[pn-web-client-unified-interface-configuration-migration-assistant](../../includes/pn-web-client-unified-interface-configuration-migration-assistant.md)]**, for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span>

<span data-ttu-id="bb6f5-109">**[!INCLUDE[pn-web-client-unified-interface-configuration-migration-assistant](../../includes/pn-web-client-unified-interface-configuration-migration-assistant.md)]** for Unified Service Desk, a tool that helps you to seamlessly migrate your existing [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations from [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web Client to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-109">**[!INCLUDE[pn-web-client-unified-interface-configuration-migration-assistant](../../includes/pn-web-client-unified-interface-configuration-migration-assistant.md)]** for Unified Service Desk, a tool that helps you to seamlessly migrate your existing [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations from [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web Client to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Unified Interface App.</span></span>

## <a name="how-web-client---unified-interface-migration-assistant-helps"></a><span data-ttu-id="bb6f5-110">How Web Client - Unified Interface Migration Assistant helps</span><span class="sxs-lookup"><span data-stu-id="bb6f5-110">How Web Client - Unified Interface Migration Assistant helps</span></span>

<span data-ttu-id="bb6f5-111">The migration assistant helps with the migration of:</span><span class="sxs-lookup"><span data-stu-id="bb6f5-111">The migration assistant helps with the migration of:</span></span>

- <span data-ttu-id="bb6f5-112">**CRM Page** hosted controls to **Unified Interface Page** hosted controls.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-112">**CRM Page** hosted controls to **Unified Interface Page** hosted controls.</span></span>
- <span data-ttu-id="bb6f5-113">**RunXRM** commands as web resources that you can import as a solution and deploy on Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-113">**RunXRM** commands as web resources that you can import as a solution and deploy on Unified Interface App.</span></span>
- <span data-ttu-id="bb6f5-114">Events and actions that are only supported in Web Client to the corresponding events and actions in Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-114">Events and actions that are only supported in Web Client to the corresponding events and actions in Unified Interface App.</span></span>
- <span data-ttu-id="bb6f5-115">Actions, action calls, events, and window navigation rules associated with the hosted control to Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-115">Actions, action calls, events, and window navigation rules associated with the hosted control to Unified Interface App.</span></span>
- <span data-ttu-id="bb6f5-116">Dashboards and Search hosted controls.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-116">Dashboards and Search hosted controls.</span></span>
- <span data-ttu-id="bb6f5-117">**KM Control** to **Unified Interface KM Control**.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-117">**KM Control** to **Unified Interface KM Control**.</span></span>
- <span data-ttu-id="bb6f5-118">Configurations from Web Client to Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="bb6f5-118">Configurations from Web Client to Unified Interface App.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="bb6f5-119">Download the migration assistant</span><span class="sxs-lookup"><span data-stu-id="bb6f5-119">Download the migration assistant</span></span>](download-migration-assistant.md)

## <a name="see-also"></a><span data-ttu-id="bb6f5-120">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="bb6f5-120">See also</span></span>

[<span data-ttu-id="bb6f5-121">Download the Web Client - Unified Interface Migration Assistant</span><span class="sxs-lookup"><span data-stu-id="bb6f5-121">Download the Web Client - Unified Interface Migration Assistant</span></span>](download-migration-assistant.md)

[<span data-ttu-id="bb6f5-122">Migration steps of the configurations from Dynamics 365 for Customer Engagement Web Client to Unified Interface apps</span><span class="sxs-lookup"><span data-stu-id="bb6f5-122">Migration steps of the configurations from Dynamics 365 for Customer Engagement Web Client to Unified Interface apps</span></span>](migration-steps-web-client-unified-interface-configuration.md)

[<span data-ttu-id="bb6f5-123">Download the tools from NuGet</span><span class="sxs-lookup"><span data-stu-id="bb6f5-123">Download the tools from NuGet</span></span>](/dynamics365/customer-engagement/developer/download-tools-nuget)

[<span data-ttu-id="bb6f5-124">Nhập dữ liệu cấu hình</span><span class="sxs-lookup"><span data-stu-id="bb6f5-124">Import configuration data</span></span>](/dynamics365/customer-engagement/admin/import-configuration-data)
