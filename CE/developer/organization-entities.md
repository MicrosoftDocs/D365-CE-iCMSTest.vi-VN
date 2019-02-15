---
title: Organization entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: An organization entity is internal to the customer relationship management process. The organization is the top level of the Dynamics 365 for Customer Engagement business hierarchy. The organization can be a specific business, a holding company, a corporation, and so on.
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
- organization, top level of business hierarchy
- organization records
- organization entities, introduction
- WhoAmIRequest message, determining organization
- announcement, definition
- deployment, definition
ms.assetid: 11ff225b-8173-419e-b16f-2d43faa4294d
caps.latest.revision: 30
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 409b6e0873ab519a61eba60d2cd968b416ffc108
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387855"
---
# <a name="organization-entities"></a><span data-ttu-id="ef045-105">Organization entities</span><span class="sxs-lookup"><span data-stu-id="ef045-105">Organization entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ef045-106">An *organization* entity is internal to the customer relationship management process.</span><span class="sxs-lookup"><span data-stu-id="ef045-106">An *organization* entity is internal to the customer relationship management process.</span></span> <span data-ttu-id="ef045-107">The organization is the top level of the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] business hierarchy.</span><span class="sxs-lookup"><span data-stu-id="ef045-107">The organization is the top level of the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] business hierarchy.</span></span> <span data-ttu-id="ef045-108">The organization can be a specific business, a holding company, a corporation, and so on.</span><span class="sxs-lookup"><span data-stu-id="ef045-108">The organization can be a specific business, a holding company, a corporation, and so on.</span></span> <span data-ttu-id="ef045-109">An organization is divided into business units.</span><span class="sxs-lookup"><span data-stu-id="ef045-109">An organization is divided into business units.</span></span> <span data-ttu-id="ef045-110">Schema customization is done at this level.</span><span class="sxs-lookup"><span data-stu-id="ef045-110">Schema customization is done at this level.</span></span>  

 <span data-ttu-id="ef045-111">A *deployment* is a single installation of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="ef045-111">A *deployment* is a single installation of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> 

 <span data-ttu-id="ef045-112">An *announcement* is a message that appears to all users on the home page of the web application.</span><span class="sxs-lookup"><span data-stu-id="ef045-112">An *announcement* is a message that appears to all users on the home page of the web application.</span></span> <span data-ttu-id="ef045-113">Announcements are owned by the organization and are represented by the `BusinessUnitNewsArticle` entity.</span><span class="sxs-lookup"><span data-stu-id="ef045-113">Announcements are owned by the organization and are represented by the `BusinessUnitNewsArticle` entity.</span></span>  

 <span data-ttu-id="ef045-114">You can call the <xref:Microsoft.Crm.Sdk.Messages.WhoAmIRequest> message to find out the organization for the currently logged on or impersonated user.</span><span class="sxs-lookup"><span data-stu-id="ef045-114">You can call the <xref:Microsoft.Crm.Sdk.Messages.WhoAmIRequest> message to find out the organization for the currently logged on or impersonated user.</span></span>  

## <a name="actions-on-the-organization-entity"></a><span data-ttu-id="ef045-115">Actions on the organization entity</span><span class="sxs-lookup"><span data-stu-id="ef045-115">Actions on the organization entity</span></span>

 <span data-ttu-id="ef045-116">An organization record is created when an organization is created in a deployment of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="ef045-116">An organization record is created when an organization is created in a deployment of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> <span data-ttu-id="ef045-117">To create, import, or delete an organization programmatically, you must use the deployment web service.</span><span class="sxs-lookup"><span data-stu-id="ef045-117">To create, import, or delete an organization programmatically, you must use the deployment web service.</span></span> <span data-ttu-id="ef045-118">After an organization is created, you can use the organization web service to retrieve or update the organization.</span><span class="sxs-lookup"><span data-stu-id="ef045-118">After an organization is created, you can use the organization web service to retrieve or update the organization.</span></span> 

 <span data-ttu-id="ef045-119">An organization can own records as defined in the ownership type in the metadata definition for an entity.</span><span class="sxs-lookup"><span data-stu-id="ef045-119">An organization can own records as defined in the ownership type in the metadata definition for an entity.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="ef045-120">[Entity Ownership](introduction-entities.md#EntityOwnership)</span><span class="sxs-lookup"><span data-stu-id="ef045-120">[Entity Ownership](introduction-entities.md#EntityOwnership)</span></span>
  
### <a name="see-also"></a><span data-ttu-id="ef045-121">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ef045-121">See also</span></span>

 <span data-ttu-id="ef045-122">[Administration and Security Entities](administration-security-entities.md) </span><span class="sxs-lookup"><span data-stu-id="ef045-122">[Administration and Security Entities](administration-security-entities.md) </span></span>  
 <span data-ttu-id="ef045-123">[Organization Entity](entities/organization.md) </span><span class="sxs-lookup"><span data-stu-id="ef045-123">[Organization Entity](entities/organization.md) </span></span>  
 [<span data-ttu-id="ef045-124">BusinessUnitNewsArticle Entity</span><span class="sxs-lookup"><span data-stu-id="ef045-124">BusinessUnitNewsArticle Entity</span></span>](entities/businessunitnewsarticle.md)   
