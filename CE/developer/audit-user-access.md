---
title: Audit user access (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Support for the ability to audit user access, including user identification, access time, and client type.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 13c43edd-77ed-411e-a82e-3e60511c40e0
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 25c8cc78de9773c3f8a4c144d9cf595b94a998d3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386809"
---
# <a name="audit-user-access"></a><span data-ttu-id="6c172-103">Audit user access</span><span class="sxs-lookup"><span data-stu-id="6c172-103">Audit user access</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="6c172-104">apps support the ability to audit user access.</span><span class="sxs-lookup"><span data-stu-id="6c172-104">apps support the ability to audit user access.</span></span> <span data-ttu-id="6c172-105">The information that is recorded includes when the user started accessing [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps and if access originated from the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps web application, [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)], or SDK calls to the web services.</span><span class="sxs-lookup"><span data-stu-id="6c172-105">The information that is recorded includes when the user started accessing [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps and if access originated from the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps web application, [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)], or SDK calls to the web services.</span></span>  
  
## <a name="enable-user-access-auditing"></a><span data-ttu-id="6c172-106">Enable user access auditing</span><span class="sxs-lookup"><span data-stu-id="6c172-106">Enable user access auditing</span></span>  
 <span data-ttu-id="6c172-107">Auditing of user access is enabled at the organization level.</span><span class="sxs-lookup"><span data-stu-id="6c172-107">Auditing of user access is enabled at the organization level.</span></span> <span data-ttu-id="6c172-108">To enable or disable user access auditing, you must retrieve the target organization’s record, and update the `Organization.IsUserAccessAuditEnabled` attribute value for the organization.</span><span class="sxs-lookup"><span data-stu-id="6c172-108">To enable or disable user access auditing, you must retrieve the target organization’s record, and update the `Organization.IsUserAccessAuditEnabled` attribute value for the organization.</span></span> <span data-ttu-id="6c172-109">Global auditing on the organization must also be enabled by setting the `Organization.IsAuditEnabled` attribute to `true` in the organization record.</span><span class="sxs-lookup"><span data-stu-id="6c172-109">Global auditing on the organization must also be enabled by setting the `Organization.IsAuditEnabled` attribute to `true` in the organization record.</span></span> <span data-ttu-id="6c172-110">To audit the origin of user access, for example: web application, [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] or SDK, you must enable auditing on the entities being accessed.</span><span class="sxs-lookup"><span data-stu-id="6c172-110">To audit the origin of user access, for example: web application, [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] or SDK, you must enable auditing on the entities being accessed.</span></span>  
  
 <span data-ttu-id="6c172-111">The frequency of auditing user access can be read or set using the `Organization.UserAccessAuditingInterval` attribute.</span><span class="sxs-lookup"><span data-stu-id="6c172-111">The frequency of auditing user access can be read or set using the `Organization.UserAccessAuditingInterval` attribute.</span></span> <span data-ttu-id="6c172-112">The default attribute value of 4 indicates user access is audited once every 4 hours.</span><span class="sxs-lookup"><span data-stu-id="6c172-112">The default attribute value of 4 indicates user access is audited once every 4 hours.</span></span>  
  
 <span data-ttu-id="6c172-113">For more information about enabling auditing for an organization and entity, see [Configure Entities and Attributes for Auditing](configure-entities-attributes-auditing.md).</span><span class="sxs-lookup"><span data-stu-id="6c172-113">For more information about enabling auditing for an organization and entity, see [Configure Entities and Attributes for Auditing](configure-entities-attributes-auditing.md).</span></span>  
  
## <a name="filter-on-user-access-events"></a><span data-ttu-id="6c172-114">Filter on user access events</span><span class="sxs-lookup"><span data-stu-id="6c172-114">Filter on user access events</span></span>  
 <span data-ttu-id="6c172-115">To search for audit records that are related to user access, your code should retrieve `Audit` records of an organization and filter on the value in `Audit.Action`.</span><span class="sxs-lookup"><span data-stu-id="6c172-115">To search for audit records that are related to user access, your code should retrieve `Audit` records of an organization and filter on the value in `Audit.Action`.</span></span> <span data-ttu-id="6c172-116">An enumeration named `AuditAction` is provided to identify supported audit actions.</span><span class="sxs-lookup"><span data-stu-id="6c172-116">An enumeration named `AuditAction` is provided to identify supported audit actions.</span></span> <span data-ttu-id="6c172-117">The actions related to user access are shown in the following list.</span><span class="sxs-lookup"><span data-stu-id="6c172-117">The actions related to user access are shown in the following list.</span></span>  
  
- `AuditAction.UserAccessviaWeb`  
  
- `AuditAction.UserAccessviaWebServices`  
  
- `AuditAction.UserAccessAuditStarted`  
  
- `AuditAction.UserAccessAuditStopped`  
  
  <span data-ttu-id="6c172-118">`UserAccessviaWeb` indicates access from the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps web application or [!INCLUDE[pn_MS_Outlook_Short](../includes/pn-ms-outlook-short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c172-118">`UserAccessviaWeb` indicates access from the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps web application or [!INCLUDE[pn_MS_Outlook_Short](../includes/pn-ms-outlook-short.md)].</span></span> <span data-ttu-id="6c172-119">`UserAccessviaWebServices` indicates a web service request from the SDK.</span><span class="sxs-lookup"><span data-stu-id="6c172-119">`UserAccessviaWebServices` indicates a web service request from the SDK.</span></span> <span data-ttu-id="6c172-120">The `AuditAction` enumeration is available to your code when you include `SampleCode\CS\HelperCode\OptionSets.cs` or `SampleCode\VB\HelperCode\OptionSets.vb` in your application’s project.</span><span class="sxs-lookup"><span data-stu-id="6c172-120">The `AuditAction` enumeration is available to your code when you include `SampleCode\CS\HelperCode\OptionSets.cs` or `SampleCode\VB\HelperCode\OptionSets.vb` in your application’s project.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6c172-121">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6c172-121">See also</span></span>  
 <span data-ttu-id="6c172-122">[Audit Entity Data Changes in Dynamics 365 for Customer Engagement apps](audit-entity-data-changes.md) </span><span class="sxs-lookup"><span data-stu-id="6c172-122">[Audit Entity Data Changes in Dynamics 365 for Customer Engagement apps](audit-entity-data-changes.md) </span></span>  
 <span data-ttu-id="6c172-123">[Configure Entities and Attributes for Auditing](configure-entities-attributes-auditing.md)   </span><span class="sxs-lookup"><span data-stu-id="6c172-123">[Configure Entities and Attributes for Auditing](configure-entities-attributes-auditing.md)   </span></span>  
 <span data-ttu-id="6c172-124">[Sample: Audit Entity Data Changes](sample-audit-entity-data-changes.md) </span><span class="sxs-lookup"><span data-stu-id="6c172-124">[Sample: Audit Entity Data Changes](sample-audit-entity-data-changes.md) </span></span>  
 [<span data-ttu-id="6c172-125">Sample: Audit User Access</span><span class="sxs-lookup"><span data-stu-id="6c172-125">Sample: Audit User Access</span></span>](sample-audit-user-access.md)
