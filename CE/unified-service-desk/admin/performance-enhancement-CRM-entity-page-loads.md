---
title: Performance enhancement for CRM entity page loads | MicrosoftDocs
description: Learn about Internet Explorer pooling feature, which creates a dynamic pool of Internet Explorer process instances. The hosted control that you open uses an Internet Explorer instance from the pool to perform faster inline navigation.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 02/06/2018
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: FA8D5702-C698-42B0-89BF-CD444BF3FB73
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: a404efc15e65edb081012163a383280d441539bb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382367"
---
# <a name="performance-enhancement-for-crm-entity-page-loads"></a><span data-ttu-id="d1c8c-104">Performance enhancement for CRM entity page loads</span><span class="sxs-lookup"><span data-stu-id="d1c8c-104">Performance enhancement for CRM entity page loads</span></span>
<span data-ttu-id="d1c8c-105">With this release of [!INCLUDE[pn-unified-service-desk-3-2](../../includes/pn-unified-service-desk-3-2.md)], you can experience enhanced performance of CRM entity page loading in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] with the Internet Explorer Pooling feature.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-105">With this release of [!INCLUDE[pn-unified-service-desk-3-2](../../includes/pn-unified-service-desk-3-2.md)], you can experience enhanced performance of CRM entity page loading in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] with the Internet Explorer Pooling feature.</span></span> 
  
[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="d1c8c-106">always maintains a pool of Internet Explorer instances for hosted controls to use.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-106">always maintains a pool of Internet Explorer instances for hosted controls to use.</span></span> <span data-ttu-id="d1c8c-107">Opening a hosted control using a pooled Internet Explorer instance enhances the performance of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="d1c8c-107">Opening a hosted control using a pooled Internet Explorer instance enhances the performance of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span>

> [!Note]
> - <span data-ttu-id="d1c8c-108">The Internet Explorer pooling feature supports only CRM entity pages hosted in CRM page hosted control.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-108">The Internet Explorer pooling feature supports only CRM entity pages hosted in CRM page hosted control.</span></span>
> - <span data-ttu-id="d1c8c-109">When you enable the pooling feature and open a CRM page hosted control, you can see in Task Manager that [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] creates a number of Internet Explorer process instances for hosted controls to use.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-109">When you enable the pooling feature and open a CRM page hosted control, you can see in Task Manager that [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] creates a number of Internet Explorer process instances for hosted controls to use.</span></span> 
> - <span data-ttu-id="d1c8c-110">The performance of the Internet Explorer pooling feature is dependent on the resources available on the client computer.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-110">The performance of the Internet Explorer pooling feature is dependent on the resources available on the client computer.</span></span>

## <a name="enable-internet-explorer-pooling"></a><span data-ttu-id="d1c8c-111">Enable Internet Explorer pooling</span><span class="sxs-lookup"><span data-stu-id="d1c8c-111">Enable Internet Explorer pooling</span></span>

<span data-ttu-id="d1c8c-112">By default, Internet Explorer pooling is disabled.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-112">By default, Internet Explorer pooling is disabled.</span></span> <span data-ttu-id="d1c8c-113">To enable pooling, a System Administrator must configure the option on the **Active UII Options** page and set it to **true**.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-113">To enable pooling, a System Administrator must configure the option on the **Active UII Options** page and set it to **true**.</span></span>

<span data-ttu-id="d1c8c-114">To enable Internet Explorer pooling:</span><span class="sxs-lookup"><span data-stu-id="d1c8c-114">To enable Internet Explorer pooling:</span></span>

1. <span data-ttu-id="d1c8c-115">Đăng nhập vào ứng dụng [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="d1c8c-115">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. <span data-ttu-id="d1c8c-116">Chọn **Tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-116">Choose **Options**.</span></span>  

4. <span data-ttu-id="d1c8c-117">click **New** on the **Active UII Options** page.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-117">click **New** on the **Active UII Options** page.</span></span>

5. <span data-ttu-id="d1c8c-118">Choose **Others** for the **Global Option** field.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-118">Choose **Others** for the **Global Option** field.</span></span>

6. <span data-ttu-id="d1c8c-119">Type **InternetExplorerPooling** for the **Name** field.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-119">Type **InternetExplorerPooling** for the **Name** field.</span></span>

7. <span data-ttu-id="d1c8c-120">Set **true** for the **Value** field.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-120">Set **true** for the **Value** field.</span></span>

8. <span data-ttu-id="d1c8c-121">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="d1c8c-121">Click **Save**.</span></span>

   <span data-ttu-id="d1c8c-122">![Enable InternetExplorerPooling option](../../unified-service-desk/media/crm-itpro-usd-options-internetexplorerpooling.PNG "Enable InternetExplorerPooling option")</span><span class="sxs-lookup"><span data-stu-id="d1c8c-122">![Enable InternetExplorerPooling option](../../unified-service-desk/media/crm-itpro-usd-options-internetexplorerpooling.PNG "Enable InternetExplorerPooling option")</span></span>

## <a name="see-also"></a><span data-ttu-id="d1c8c-123">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d1c8c-123">See also</span></span>

[<span data-ttu-id="d1c8c-124">Quản lý tùy chọn cho Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d1c8c-124">Manage Options for Unified Service Desk</span></span>](../../unified-service-desk/admin/manage-options-unified-service-desk.md)
 
