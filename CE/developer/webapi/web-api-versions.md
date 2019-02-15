---
title: Dynamics 365 for Customer Engagement Web API Versions (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how versioning of Dynamics 365 for Customer Engagement Web API works. Dynamics 365 for Customer Engagement Web API versions support version specific differences in the same environment which is different from the behavior in the v8.x releases in which new capabilities were additive
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d9bb79a5-2bfa-4ffe-8cb4-60f192359489
caps.latest.revision: 34
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: cbb5403f2e630f6a86718399e046f1148d97e14f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388719"
---
# <a name="dynamics-365-for-customer-engagement-web-api-versions"></a><span data-ttu-id="b2296-104">Dynamics 365 for Customer Engagement Web API Versions</span><span class="sxs-lookup"><span data-stu-id="b2296-104">Dynamics 365 for Customer Engagement Web API Versions</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b2296-105">Beginning with the [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)] (v9.0) release, the [!INCLUDE[pn_ms_dyn_365](../../includes/pn-ms-dyn-365.md)] for Customer Engagement apps Web API supports version specific differences in the same environment.</span><span class="sxs-lookup"><span data-stu-id="b2296-105">Beginning with the [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)] (v9.0) release, the [!INCLUDE[pn_ms_dyn_365](../../includes/pn-ms-dyn-365.md)] for Customer Engagement apps Web API supports version specific differences in the same environment.</span></span>  
  
 <span data-ttu-id="b2296-106">This is different from the behavior for in the v8.*x* releases.</span><span class="sxs-lookup"><span data-stu-id="b2296-106">This is different from the behavior for in the v8.*x* releases.</span></span> <span data-ttu-id="b2296-107">In the previous releases new capabilities were available to any version of the service depending on the update applied to the environment.</span><span class="sxs-lookup"><span data-stu-id="b2296-107">In the previous releases new capabilities were available to any version of the service depending on the update applied to the environment.</span></span>  <span data-ttu-id="b2296-108">After an upgrade to v8.2, the v8.0, and v8.1 services were all identical.</span><span class="sxs-lookup"><span data-stu-id="b2296-108">After an upgrade to v8.2, the v8.0, and v8.1 services were all identical.</span></span> <span data-ttu-id="b2296-109">This was possible because all the changes were additive.</span><span class="sxs-lookup"><span data-stu-id="b2296-109">This was possible because all the changes were additive.</span></span> <span data-ttu-id="b2296-110">Nothing was removed or introduced breaking changes.</span><span class="sxs-lookup"><span data-stu-id="b2296-110">Nothing was removed or introduced breaking changes.</span></span> <span data-ttu-id="b2296-111">As a result, the specific version referenced in the service URL for the v8.*x* wasn't actually important.</span><span class="sxs-lookup"><span data-stu-id="b2296-111">As a result, the specific version referenced in the service URL for the v8.*x* wasn't actually important.</span></span>  
  
 <span data-ttu-id="b2296-112">Going forward the capabilities of the service can change, including potentially breaking changes such as removing specific operations.</span><span class="sxs-lookup"><span data-stu-id="b2296-112">Going forward the capabilities of the service can change, including potentially breaking changes such as removing specific operations.</span></span> <span data-ttu-id="b2296-113">This will allow for improvements to be applied on an on-going basis.</span><span class="sxs-lookup"><span data-stu-id="b2296-113">This will allow for improvements to be applied on an on-going basis.</span></span> <span data-ttu-id="b2296-114">This topic will record any version specific differences and any limitations where the Web API hasn't yet achieved parity with the organization service.</span><span class="sxs-lookup"><span data-stu-id="b2296-114">This topic will record any version specific differences and any limitations where the Web API hasn't yet achieved parity with the organization service.</span></span>  
  
## <a name="web-api-limitations"></a><span data-ttu-id="b2296-115">Web API Limitations</span><span class="sxs-lookup"><span data-stu-id="b2296-115">Web API Limitations</span></span>  

 <span data-ttu-id="b2296-116">The [!INCLUDE[pn_ms_dyn_365](../../includes/pn-ms-dyn-365.md)] for Customer Engagement apps Web API provides complete parity with the capabilities of the organization service.</span><span class="sxs-lookup"><span data-stu-id="b2296-116">The [!INCLUDE[pn_ms_dyn_365](../../includes/pn-ms-dyn-365.md)] for Customer Engagement apps Web API provides complete parity with the capabilities of the organization service.</span></span> <span data-ttu-id="b2296-117">For [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)], this topic describes the limitations carried forward from the [!INCLUDE[pn_crm_8_2_0_online](../../includes/pn-crm-8-2-0-online.md)] release.</span><span class="sxs-lookup"><span data-stu-id="b2296-117">For [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)], this topic describes the limitations carried forward from the [!INCLUDE[pn_crm_8_2_0_online](../../includes/pn-crm-8-2-0-online.md)] release.</span></span>          <span data-ttu-id="b2296-118">For earlier releases, see [Dynamics CRM 2016 Web API Limitations](https://msdn.microsoft.com/library/mt628816\(CRM.8\).aspx).</span><span class="sxs-lookup"><span data-stu-id="b2296-118">For earlier releases, see [Dynamics CRM 2016 Web API Limitations](https://msdn.microsoft.com/library/mt628816\(CRM.8\).aspx).</span></span>  
  
## <a name="limitations-addressed-in-includepncrm900onlineincludespn-crm-9-0-0-onlinemd"></a><span data-ttu-id="b2296-119">Limitations addressed in [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)]</span><span class="sxs-lookup"><span data-stu-id="b2296-119">Limitations addressed in [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)]</span></span>  
 <span data-ttu-id="b2296-120">In version 8.2, some custom actions were not available in Web API.</span><span class="sxs-lookup"><span data-stu-id="b2296-120">In version 8.2, some custom actions were not available in Web API.</span></span>
> [!NOTE]
>  <span data-ttu-id="b2296-121">This issue is addressed in [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)].</span><span class="sxs-lookup"><span data-stu-id="b2296-121">This issue is addressed in [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)].</span></span>  
  
 <span data-ttu-id="b2296-122">If you defined a custom action which includeed a complex return value and a simple return value, a corresponding Action was not available in the Web API but was available using the 2011 SOAP endpoint.</span><span class="sxs-lookup"><span data-stu-id="b2296-122">If you defined a custom action which includeed a complex return value and a simple return value, a corresponding Action was not available in the Web API but was available using the 2011 SOAP endpoint.</span></span> <span data-ttu-id="b2296-123">A complex return value is an `EntityReference`, `Entity`, or `EntityCollection`.</span><span class="sxs-lookup"><span data-stu-id="b2296-123">A complex return value is an `EntityReference`, `Entity`, or `EntityCollection`.</span></span> <span data-ttu-id="b2296-124">You can have any combination of simple return values or a single complex return value.</span><span class="sxs-lookup"><span data-stu-id="b2296-124">You can have any combination of simple return values or a single complex return value.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b2296-125">[Tạo hành động của riêng bạn](../create-own-actions.md)</span><span class="sxs-lookup"><span data-stu-id="b2296-125">[Create your own actions](../create-own-actions.md)</span></span>  
 
## <a name="new-operations-added"></a><span data-ttu-id="b2296-126">New operations added</span><span class="sxs-lookup"><span data-stu-id="b2296-126">New operations added</span></span>  
 <span data-ttu-id="b2296-127">The following operations have been added to the Web API for [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)].</span><span class="sxs-lookup"><span data-stu-id="b2296-127">The following operations have been added to the Web API for [!INCLUDE[pn_crm_9_0_0_online](../../includes/pn-crm-9-0-0-online.md)].</span></span>  
  
||||  
|-|-|-|  
|<xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>|<xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>|<xref:Microsoft.Crm.Sdk.Messages.RetrieveSharedPrincipalsAndAccessRequest>|  
  
### <a name="see-also"></a><span data-ttu-id="b2296-128">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b2296-128">See also</span></span>  
 <span data-ttu-id="b2296-129">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="b2296-129">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span></span>  
 <span data-ttu-id="b2296-130">[Authenticate to Dynamics 365 for Customer Engagement apps with the Web API](authenticate-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="b2296-130">[Authenticate to Dynamics 365 for Customer Engagement apps with the Web API](authenticate-web-api.md) </span></span>  
 <span data-ttu-id="b2296-131">[Web API types and operations](web-api-types-operations.md) </span><span class="sxs-lookup"><span data-stu-id="b2296-131">[Web API types and operations](web-api-types-operations.md) </span></span>  
 [<span data-ttu-id="b2296-132">Perform operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="b2296-132">Perform operations using the Web API</span></span>](perform-operations-web-api.md)
