---
title: Contract entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about contract entity that is used to track customer service agreements. You can create contracts for existing customers that specify the type of service and terms that apply to each customer.
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
- contract status options, contract entities
- status options, contract entities
- contract entities, contract templates
- contract entities, rules for using
- contract entity, definition
- contract templates, contract entities
- contract entities, tracking customer services agreements
- contract entities, status options
- contract entities, introduction
- tracking customer services agreements, contract entities
ms.assetid: 631e9570-86e5-490e-98dd-ee27925ea8e8
caps.latest.revision: 30
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bf3f919b1cce089df630b4492bf7fad3a3add224
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385534"
---
# <a name="contract-entities"></a><span data-ttu-id="c5d42-104">Contract entities</span><span class="sxs-lookup"><span data-stu-id="c5d42-104">Contract entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c5d42-105">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], a *contract* is an agreement to provide support during specified coverage dates or for a specified number of cases or length of time.</span><span class="sxs-lookup"><span data-stu-id="c5d42-105">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], a *contract* is an agreement to provide support during specified coverage dates or for a specified number of cases or length of time.</span></span> <span data-ttu-id="c5d42-106">When customers contact customer service, the level of support they receive is determined by their contract.</span><span class="sxs-lookup"><span data-stu-id="c5d42-106">When customers contact customer service, the level of support they receive is determined by their contract.</span></span>  
  
 <span data-ttu-id="c5d42-107">The contract entity is used to track customer service agreements.</span><span class="sxs-lookup"><span data-stu-id="c5d42-107">The contract entity is used to track customer service agreements.</span></span> <span data-ttu-id="c5d42-108">You can create contracts for existing customers that specify the type of service and terms that apply to each customer.</span><span class="sxs-lookup"><span data-stu-id="c5d42-108">You can create contracts for existing customers that specify the type of service and terms that apply to each customer.</span></span> <span data-ttu-id="c5d42-109">New contracts are created based on the contract template.</span><span class="sxs-lookup"><span data-stu-id="c5d42-109">New contracts are created based on the contract template.</span></span> <span data-ttu-id="c5d42-110">Bạn có thể tạo ra những hợp đồng chỉ dành cho các khách hàng và người liên hệ hiện có.</span><span class="sxs-lookup"><span data-stu-id="c5d42-110">You can create contracts only for existing accounts and contacts.</span></span>  
  
 <span data-ttu-id="c5d42-111">A contract has the status of “Draft” until it is invoiced.</span><span class="sxs-lookup"><span data-stu-id="c5d42-111">A contract has the status of “Draft” until it is invoiced.</span></span> <span data-ttu-id="c5d42-112">You can change the contract template until the contract status changes.</span><span class="sxs-lookup"><span data-stu-id="c5d42-112">You can change the contract template until the contract status changes.</span></span> <span data-ttu-id="c5d42-113">Each new contract is assigned a unique ID that can’t be used for another contract unless it is being renewed.</span><span class="sxs-lookup"><span data-stu-id="c5d42-113">Each new contract is assigned a unique ID that can’t be used for another contract unless it is being renewed.</span></span> <span data-ttu-id="c5d42-114">When you renew a contract, it is saved as a draft with an ID that corresponds to the original contract.</span><span class="sxs-lookup"><span data-stu-id="c5d42-114">When you renew a contract, it is saved as a draft with an ID that corresponds to the original contract.</span></span> <span data-ttu-id="c5d42-115">If a contract with a status of “Invoiced” or “Active” is modified, the amended contract remains associated with the original account.</span><span class="sxs-lookup"><span data-stu-id="c5d42-115">If a contract with a status of “Invoiced” or “Active” is modified, the amended contract remains associated with the original account.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c5d42-116">In This Section</span><span class="sxs-lookup"><span data-stu-id="c5d42-116">In This Section</span></span>  
 [<span data-ttu-id="c5d42-117">Contract Entity</span><span class="sxs-lookup"><span data-stu-id="c5d42-117">Contract Entity</span></span>](entities/contract.md)  
  
 [<span data-ttu-id="c5d42-118">ContractDetail Entity</span><span class="sxs-lookup"><span data-stu-id="c5d42-118">ContractDetail Entity</span></span>](entities/contractdetail.md)  
  
 [<span data-ttu-id="c5d42-119">Sample: Manage Contracts</span><span class="sxs-lookup"><span data-stu-id="c5d42-119">Sample: Manage Contracts</span></span>](sample-manage-contracts.md)  
  
## <a name="related-sections"></a><span data-ttu-id="c5d42-120">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="c5d42-120">Related Sections</span></span>  
 [<span data-ttu-id="c5d42-121">Service entities (contract, incident, knowledge base)</span><span class="sxs-lookup"><span data-stu-id="c5d42-121">Service entities (contract, incident, knowledge base)</span></span>](service-entities.md)  
  
 [<span data-ttu-id="c5d42-122">Incident (case) entities</span><span class="sxs-lookup"><span data-stu-id="c5d42-122">Incident (case) entities</span></span>](incident-case-entities.md)  
  
 [<span data-ttu-id="c5d42-123">Knowledge base entities</span><span class="sxs-lookup"><span data-stu-id="c5d42-123">Knowledge base entities</span></span>](knowledge-management-entities.md)
