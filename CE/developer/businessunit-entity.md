---
title: BusinessUnit entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: A business unit is a unit of the top-level organization. Business units can be parents of other business units (child business units). The first business unit created for an organization is called the root business unit.
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
- businessunit entities
- business unit entities
- business unit, definition
ms.assetid: bf38e07e-37a2-419b-bd5e-d259d97a3c70
caps.latest.revision: 24
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9b747032510a3bc67413502eb7c27f8cd3764e33
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386489"
---
# <a name="businessunit-entity"></a><span data-ttu-id="c5a38-105">BusinessUnit entity</span><span class="sxs-lookup"><span data-stu-id="c5a38-105">BusinessUnit entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c5a38-106">An organization in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], such as a holding company or a corporation, is made up of business units.</span><span class="sxs-lookup"><span data-stu-id="c5a38-106">An organization in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], such as a holding company or a corporation, is made up of business units.</span></span> <span data-ttu-id="c5a38-107">A *business unit* is a unit of the top-level organization.</span><span class="sxs-lookup"><span data-stu-id="c5a38-107">A *business unit* is a unit of the top-level organization.</span></span> <span data-ttu-id="c5a38-108">Business units can be parents of other business units (child business units).</span><span class="sxs-lookup"><span data-stu-id="c5a38-108">Business units can be parents of other business units (child business units).</span></span> <span data-ttu-id="c5a38-109">The first business unit created for an organization is called the root business unit.</span><span class="sxs-lookup"><span data-stu-id="c5a38-109">The first business unit created for an organization is called the root business unit.</span></span> <span data-ttu-id="c5a38-110">Business units can be deleted, however, the root business unit can’t be deleted.</span><span class="sxs-lookup"><span data-stu-id="c5a38-110">Business units can be deleted, however, the root business unit can’t be deleted.</span></span>  
  
 <span data-ttu-id="c5a38-111">A *parent business unit* is any business unit with one or more business units that report to it in the hierarchy.</span><span class="sxs-lookup"><span data-stu-id="c5a38-111">A *parent business unit* is any business unit with one or more business units that report to it in the hierarchy.</span></span>  
  
 <span data-ttu-id="c5a38-112">A *child business unit* is a business unit that is immediately under another business unit in the business hierarchy of an organization.</span><span class="sxs-lookup"><span data-stu-id="c5a38-112">A *child business unit* is a business unit that is immediately under another business unit in the business hierarchy of an organization.</span></span>  
  
 <span data-ttu-id="c5a38-113">A business unit can own records as defined in the ownership type in the metadata definition for an entity.</span><span class="sxs-lookup"><span data-stu-id="c5a38-113">A business unit can own records as defined in the ownership type in the metadata definition for an entity.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="c5a38-114">[Entity Ownership](introduction-entities.md#EntityOwnership)</span><span class="sxs-lookup"><span data-stu-id="c5a38-114">[Entity Ownership](introduction-entities.md#EntityOwnership)</span></span>  
  
 <span data-ttu-id="c5a38-115">You can call the <xref:Microsoft.Crm.Sdk.Messages.WhoAmIRequest> message to find out the business unit for the currently logged on or impersonated user.</span><span class="sxs-lookup"><span data-stu-id="c5a38-115">You can call the <xref:Microsoft.Crm.Sdk.Messages.WhoAmIRequest> message to find out the business unit for the currently logged on or impersonated user.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c5a38-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c5a38-116">See also</span></span>  
 <span data-ttu-id="c5a38-117">[Administration and Security Entities](administration-security-entities.md) </span><span class="sxs-lookup"><span data-stu-id="c5a38-117">[Administration and Security Entities](administration-security-entities.md) </span></span>  
 <span data-ttu-id="c5a38-118">[BusinessUnit Entity](entities/businessunit.md) </span><span class="sxs-lookup"><span data-stu-id="c5a38-118">[BusinessUnit Entity](entities/businessunit.md) </span></span>  
 [<span data-ttu-id="c5a38-119">User and team entities</span><span class="sxs-lookup"><span data-stu-id="c5a38-119">User and team entities</span></span>](user-team-entities.md)   
