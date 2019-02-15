---
title: Incident (case) entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'Learn about incident (case) entities that performs the incident management by creating an incident and specifying an active SLA record. An incident can be in one of three states: Active, Resolved, or Canceled.'
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
- incident (case) entities, tracking actions and communications
- routing and queuing, definition
- tracking actions and communications, incident (case) entities
- incident (case) entities, tracking incidents and activities
- incident (case) entities, tracking customer requests; questions; or problems
- tracking customer requests; questions; or problems
- knowledge base, definition
- managing incidents, incident (case) entities
- incident (case) entities, introduction
- incident management, definition
- incident (case) entities, managing
- managing cases, incident (case) entities
- incident, definition
- tracking incidents and activities, incident (case) entities
- incident states, types of
- case entities, see 'incident (case) entities'
ms.assetid: 441cd857-456f-4319-a0e3-69555277eee5
caps.latest.revision: 29
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 36b9fb7cc27c32b003aa55402d8febb863cd0c9a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386090"
---
# <a name="incident-case-entities"></a><span data-ttu-id="e1033-104">Incident (case) entities</span><span class="sxs-lookup"><span data-stu-id="e1033-104">Incident (case) entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e1033-105">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], *incident management* is the primary aspect of the customer service part of the [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)].</span><span class="sxs-lookup"><span data-stu-id="e1033-105">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], *incident management* is the primary aspect of the customer service part of the [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)].</span></span> <span data-ttu-id="e1033-106">The other features, such as the *knowledge base*, are used to help manage cases.</span><span class="sxs-lookup"><span data-stu-id="e1033-106">The other features, such as the *knowledge base*, are used to help manage cases.</span></span> <span data-ttu-id="e1033-107">In [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], an incident is referred to as a case.</span><span class="sxs-lookup"><span data-stu-id="e1033-107">In [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], an incident is referred to as a case.</span></span>  
  
 <span data-ttu-id="e1033-108">A customer service representative creates an incident (case) to track a customer request, question, or a problem.</span><span class="sxs-lookup"><span data-stu-id="e1033-108">A customer service representative creates an incident (case) to track a customer request, question, or a problem.</span></span> <span data-ttu-id="e1033-109">All actions and communications can be tracked in the `incident` entity.</span><span class="sxs-lookup"><span data-stu-id="e1033-109">All actions and communications can be tracked in the `incident` entity.</span></span> <span data-ttu-id="e1033-110">You can manually apply a service level agreement (SLA) to an incident by updating the incident record, and specifying an active SLA record in the `SLAId` attribute of the incident record.</span><span class="sxs-lookup"><span data-stu-id="e1033-110">You can manually apply a service level agreement (SLA) to an incident by updating the incident record, and specifying an active SLA record in the `SLAId` attribute of the incident record.</span></span> <span data-ttu-id="e1033-111">An incident can be in one of three states: *Active*, *Resolved*, or *Canceled*.</span><span class="sxs-lookup"><span data-stu-id="e1033-111">An incident can be in one of three states: *Active*, *Resolved*, or *Canceled*.</span></span>  
  
 <span data-ttu-id="e1033-112">By using the incident management APIs, you can create reports to measure statistics, such as individual customer service representative statistics (call lengths, resolutions, and so on) and the average length of time that incidents remain active.</span><span class="sxs-lookup"><span data-stu-id="e1033-112">By using the incident management APIs, you can create reports to measure statistics, such as individual customer service representative statistics (call lengths, resolutions, and so on) and the average length of time that incidents remain active.</span></span>  
  
 [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="e1033-113">supports the ability to track many incidents and activities.</span><span class="sxs-lookup"><span data-stu-id="e1033-113">supports the ability to track many incidents and activities.</span></span> <span data-ttu-id="e1033-114">Many of these tasks overlap with activities in sales force automation.</span><span class="sxs-lookup"><span data-stu-id="e1033-114">Many of these tasks overlap with activities in sales force automation.</span></span> <span data-ttu-id="e1033-115">Routing and queuing is the process of moving activities and cases from the customer to the correct customer service representative for service request completion.</span><span class="sxs-lookup"><span data-stu-id="e1033-115">Routing and queuing is the process of moving activities and cases from the customer to the correct customer service representative for service request completion.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e1033-116">In This Section</span><span class="sxs-lookup"><span data-stu-id="e1033-116">In This Section</span></span>  
 [<span data-ttu-id="e1033-117">Incident Entity</span><span class="sxs-lookup"><span data-stu-id="e1033-117">Incident Entity</span></span>](entities/incident.md)  
  
 [<span data-ttu-id="e1033-118">Incident (case) hierarchies</span><span class="sxs-lookup"><span data-stu-id="e1033-118">Incident (case) hierarchies</span></span>](incident-case-hierarchies.md)  
  
 [<span data-ttu-id="e1033-119">IncidentResolution Entity</span><span class="sxs-lookup"><span data-stu-id="e1033-119">IncidentResolution Entity</span></span>](entities/incidentresolution.md)  
  
 [<span data-ttu-id="e1033-120">Sample: Close an Incident</span><span class="sxs-lookup"><span data-stu-id="e1033-120">Sample: Close an Incident</span></span>](sample-close-incident.md)  
  
## <a name="related-sections"></a><span data-ttu-id="e1033-121">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="e1033-121">Related Sections</span></span>  
 [<span data-ttu-id="e1033-122">Contract Entities</span><span class="sxs-lookup"><span data-stu-id="e1033-122">Contract Entities</span></span>](contract-entities.md)  
  
 [<span data-ttu-id="e1033-123">Knowledge Base Entities</span><span class="sxs-lookup"><span data-stu-id="e1033-123">Knowledge Base Entities</span></span>](knowledge-management-entities.md)
