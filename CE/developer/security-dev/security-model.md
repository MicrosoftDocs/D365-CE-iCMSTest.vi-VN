---
title: Security model (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Provides a security model that protects data integrity and privacy, and supports efficient data access and collaboration.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- record-based security, definition
- security model of Microsoft Dynamics CRM, types of security
- field-level security, definition
- goals for the security model in Microsoft Dynamics CRM, security model of Microsoft Dynamics CRM
- types of security in Microsoft Dynamics CRM, role-based security
- types of security in Microsoft Dynamics CRM, field-level security
- role-based security, definition
- learning about development in CRM, security model of Microsoft Dynamics CRM
- security model of Microsoft Dynamics CRM, goals for
- security model of Microsoft Dynamics CRM, overview of
- types of security in Microsoft Dynamics CRM, record-based security
ms.assetid: b5b10592-5e1f-4243-be90-2fedd718ad9c
caps.latest.revision: 38
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ace9670db418de23b33b3b94492d0dbe30d90758
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387722"
---
# <a name="security-model-of-customer-engagement"></a><span data-ttu-id="7e894-103">Security model of Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="7e894-103">Security model of Customer Engagement</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="7e894-104">apps provides a security model that protects data integrity and privacy, and supports efficient data access and collaboration.</span><span class="sxs-lookup"><span data-stu-id="7e894-104">apps provides a security model that protects data integrity and privacy, and supports efficient data access and collaboration.</span></span> <span data-ttu-id="7e894-105">Mục tiêu của mô hình như sau:</span><span class="sxs-lookup"><span data-stu-id="7e894-105">The goals of the model are as follows:</span></span>  
  
- <span data-ttu-id="7e894-106">Provide users with the access only to the appropriate levels of information that is required to do their jobs.</span><span class="sxs-lookup"><span data-stu-id="7e894-106">Provide users with the access only to the appropriate levels of information that is required to do their jobs.</span></span>  
  
- <span data-ttu-id="7e894-107">Categorize users by role and restrict access based on those roles.</span><span class="sxs-lookup"><span data-stu-id="7e894-107">Categorize users by role and restrict access based on those roles.</span></span>  
  
- <span data-ttu-id="7e894-108">Support data sharing so that users and teams can be granted access to records that they do not own for a specified collaborative effort.</span><span class="sxs-lookup"><span data-stu-id="7e894-108">Support data sharing so that users and teams can be granted access to records that they do not own for a specified collaborative effort.</span></span>  
  
- <span data-ttu-id="7e894-109">Prevent a user's access to records the user does not own or share.</span><span class="sxs-lookup"><span data-stu-id="7e894-109">Prevent a user's access to records the user does not own or share.</span></span>  
  
  <span data-ttu-id="7e894-110">**Role-based security** in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps focuses on grouping a set of privileges together that describe the responsibilities (or tasks that can be performed) for a user.</span><span class="sxs-lookup"><span data-stu-id="7e894-110">**Role-based security** in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps focuses on grouping a set of privileges together that describe the responsibilities (or tasks that can be performed) for a user.</span></span> [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] <span data-ttu-id="7e894-111">apps includes a set of predefined security roles.</span><span class="sxs-lookup"><span data-stu-id="7e894-111">apps includes a set of predefined security roles.</span></span> <span data-ttu-id="7e894-112">Each aggregates a set of user rights to make user security management easier.</span><span class="sxs-lookup"><span data-stu-id="7e894-112">Each aggregates a set of user rights to make user security management easier.</span></span> <span data-ttu-id="7e894-113">Also, each application deployment can define its own roles to meet the needs of different users.</span><span class="sxs-lookup"><span data-stu-id="7e894-113">Also, each application deployment can define its own roles to meet the needs of different users.</span></span>  
  
  <span data-ttu-id="7e894-114">**Record-based security** in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] focuses on access rights to specific records.</span><span class="sxs-lookup"><span data-stu-id="7e894-114">**Record-based security** in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] focuses on access rights to specific records.</span></span>  
  
  <span data-ttu-id="7e894-115">**Field-level security** in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps restricts access to specific high business impact fields in an entity only to specified users or teams.</span><span class="sxs-lookup"><span data-stu-id="7e894-115">**Field-level security** in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps restricts access to specific high business impact fields in an entity only to specified users or teams.</span></span>  
  
  <span data-ttu-id="7e894-116">Combine role-based security, record-level security, and field-level security to define the overall security rights that users have within your custom [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps application.</span><span class="sxs-lookup"><span data-stu-id="7e894-116">Combine role-based security, record-level security, and field-level security to define the overall security rights that users have within your custom [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps application.</span></span>  
  
  <span data-ttu-id="7e894-117">More overview information about security can be found on the [Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/CloudServices/Dynamics365), and in this white paper: [Microsoft Dynamics CRM Online security and compliance planning guide](http://download.microsoft.com/download/B/4/A/B4A6FDE3-A5ED-43A8-99CB-E218E51AE106/Microsoft%20Dynamics%20CRM%20Online%20security%20and%20compliance%20planning%20guide.pdf).</span><span class="sxs-lookup"><span data-stu-id="7e894-117">More overview information about security can be found on the [Microsoft Trust Center](https://www.microsoft.com/en-us/TrustCenter/CloudServices/Dynamics365), and in this white paper: [Microsoft Dynamics CRM Online security and compliance planning guide](http://download.microsoft.com/download/B/4/A/B4A6FDE3-A5ED-43A8-99CB-E218E51AE106/Microsoft%20Dynamics%20CRM%20Online%20security%20and%20compliance%20planning%20guide.pdf).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7e894-118">In This Section</span><span class="sxs-lookup"><span data-stu-id="7e894-118">In This Section</span></span>  
 [<span data-ttu-id="7e894-119">How Role-Based Security Can Be Used to Control Access to Entities In Microsoft Dynamics 365 for Customer Engagemen apps</span><span class="sxs-lookup"><span data-stu-id="7e894-119">How Role-Based Security Can Be Used to Control Access to Entities In Microsoft Dynamics 365 for Customer Engagemen apps</span></span>](how-role-based-security-control-access-entities.md)  
  
 [<span data-ttu-id="7e894-120">How Instance-Based Security Can Be Used to Control Access to Records In Microsoft Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="7e894-120">How Instance-Based Security Can Be Used to Control Access to Records In Microsoft Dynamics 365 for Customer Engagement apps</span></span>](use-record-based-security-control-access-records.md)  
  
 [<span data-ttu-id="7e894-121">How Field Security Can Be Used to Control Access to Field Values In Microsoft Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="7e894-121">How Field Security Can Be Used to Control Access to Field Values In Microsoft Dynamics 365 for Customer Engagement apps</span></span>](use-field-security-control-access-field-values.md)  
  
 [<span data-ttu-id="7e894-122">How hierarchical security can be used to control access to entities in Microsoft Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="7e894-122">How hierarchical security can be used to control access to entities in Microsoft Dynamics 365 for Customer Engagement apps</span></span>](hierarchical-security-control-access-entities.md)  
  
## <a name="related-sections"></a><span data-ttu-id="7e894-123">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="7e894-123">Related Sections</span></span>  
 <span data-ttu-id="7e894-124">[Security concepts for Microsoft Dynamics 365 for Customer Engagement apps](https://technet.microsoft.com/library/hh699698\(v=crm.8\).aspx)</span><span class="sxs-lookup"><span data-stu-id="7e894-124">[Security concepts for Microsoft Dynamics 365 for Customer Engagement apps](https://technet.microsoft.com/library/hh699698\(v=crm.8\).aspx)</span></span>  
  
   
