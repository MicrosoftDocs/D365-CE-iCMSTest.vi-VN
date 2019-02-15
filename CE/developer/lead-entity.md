---
title: Lead entity (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about lead entity that represents an individual who is interested in receiving specific information about products or services offered by the company.
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
- lead entity, managing leads
- lead entity, associated information
- leads
- lead entity, converting leads to qualified leads
- lead entity, introduction
- lead entity
- managing leads, lead entity
- lead entity, definition
ms.assetid: a3e17cc7-a4ff-4a10-bc7a-ae03e055b30f
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2f0e9760bdf0023cd650e44eaae01e5bd86ac434
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385678"
---
# <a name="lead-entity"></a><span data-ttu-id="6b7df-103">Thực thể khách hàng tiềm năng</span><span class="sxs-lookup"><span data-stu-id="6b7df-103">Lead entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6b7df-104">A *lead* entity represents an individual that is identified as someone who is interested in receiving specific information about the products or services offered by the company.</span><span class="sxs-lookup"><span data-stu-id="6b7df-104">A *lead* entity represents an individual that is identified as someone who is interested in receiving specific information about the products or services offered by the company.</span></span> <span data-ttu-id="6b7df-105">The information is provided to a lead by a salesperson through email or other communication activities available in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="6b7df-105">The information is provided to a lead by a salesperson through email or other communication activities available in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span> <span data-ttu-id="6b7df-106">A lead is used to track contacts or accounts that are potential customers, but who have not yet been qualified.</span><span class="sxs-lookup"><span data-stu-id="6b7df-106">A lead is used to track contacts or accounts that are potential customers, but who have not yet been qualified.</span></span>  
  
 <span data-ttu-id="6b7df-107">Lead management is largely the same as opportunity management.</span><span class="sxs-lookup"><span data-stu-id="6b7df-107">Lead management is largely the same as opportunity management.</span></span> <span data-ttu-id="6b7df-108">However, a lead is kept separate from customer and opportunity data until the lead is qualified.</span><span class="sxs-lookup"><span data-stu-id="6b7df-108">However, a lead is kept separate from customer and opportunity data until the lead is qualified.</span></span> <span data-ttu-id="6b7df-109">The possible states for a lead are Open, Qualified, and Disqualified.</span><span class="sxs-lookup"><span data-stu-id="6b7df-109">The possible states for a lead are Open, Qualified, and Disqualified.</span></span> <span data-ttu-id="6b7df-110">A qualified lead may be converted to an account, contact or opportunity.</span><span class="sxs-lookup"><span data-stu-id="6b7df-110">A qualified lead may be converted to an account, contact or opportunity.</span></span> <span data-ttu-id="6b7df-111">To convert, use the <xref:Microsoft.Crm.Sdk.Messages.QualifyLeadRequest> message.</span><span class="sxs-lookup"><span data-stu-id="6b7df-111">To convert, use the <xref:Microsoft.Crm.Sdk.Messages.QualifyLeadRequest> message.</span></span>  
  
 <span data-ttu-id="6b7df-112">The following items can be associated with a lead:</span><span class="sxs-lookup"><span data-stu-id="6b7df-112">The following items can be associated with a lead:</span></span>  
  
- <span data-ttu-id="6b7df-113">Contact and account information</span><span class="sxs-lookup"><span data-stu-id="6b7df-113">Contact and account information</span></span>  
  
- <span data-ttu-id="6b7df-114">Customer requests</span><span class="sxs-lookup"><span data-stu-id="6b7df-114">Customer requests</span></span>  
  
- <span data-ttu-id="6b7df-115">Hoạt động</span><span class="sxs-lookup"><span data-stu-id="6b7df-115">Activities</span></span>  
  
- <span data-ttu-id="6b7df-116">Ghi chú</span><span class="sxs-lookup"><span data-stu-id="6b7df-116">Notes</span></span>  
  
- <span data-ttu-id="6b7df-117">Tệp đính kèm</span><span class="sxs-lookup"><span data-stu-id="6b7df-117">Attachments</span></span>  
  
  <span data-ttu-id="6b7df-118">A link is maintained between the lead and any accounts and contacts.</span><span class="sxs-lookup"><span data-stu-id="6b7df-118">A link is maintained between the lead and any accounts and contacts.</span></span> <span data-ttu-id="6b7df-119">You can create this link by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span><span class="sxs-lookup"><span data-stu-id="6b7df-119">You can create this link by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*></span></span> <span data-ttu-id="6b7df-120">method with the <xref:Microsoft.Xrm.Sdk.Messages.AssociateRequest> or the <xref:Microsoft.Xrm.Sdk.Messages.DisassociateRequest> messages.</span><span class="sxs-lookup"><span data-stu-id="6b7df-120">method with the <xref:Microsoft.Xrm.Sdk.Messages.AssociateRequest> or the <xref:Microsoft.Xrm.Sdk.Messages.DisassociateRequest> messages.</span></span> <span data-ttu-id="6b7df-121">This makes it possible to generate reports that indicate the value of different lead sources.</span><span class="sxs-lookup"><span data-stu-id="6b7df-121">This makes it possible to generate reports that indicate the value of different lead sources.</span></span>  
  
  <span data-ttu-id="6b7df-122">When you enter a lead into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], you can use the process (workflow) engine to automatically route it to a specific user or team based on rules that are defined by the business unit or channel partner.</span><span class="sxs-lookup"><span data-stu-id="6b7df-122">When you enter a lead into [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], you can use the process (workflow) engine to automatically route it to a specific user or team based on rules that are defined by the business unit or channel partner.</span></span> <span data-ttu-id="6b7df-123">Upon qualification, the lead is either converted to an opportunity or is inactivated, but retained to allow for accurate business reporting, for example, analysis of the effectiveness of different lead sources.</span><span class="sxs-lookup"><span data-stu-id="6b7df-123">Upon qualification, the lead is either converted to an opportunity or is inactivated, but retained to allow for accurate business reporting, for example, analysis of the effectiveness of different lead sources.</span></span> <span data-ttu-id="6b7df-124">For more information, see[Processes in Dynamics 365 for Customer Engagement 5](automate-business-processes-customer-engagement.md).</span><span class="sxs-lookup"><span data-stu-id="6b7df-124">For more information, see[Processes in Dynamics 365 for Customer Engagement 5](automate-business-processes-customer-engagement.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6b7df-125">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6b7df-125">See Also</span></span>  
 <span data-ttu-id="6b7df-126">[Lead Entity](entities/lead.md) </span><span class="sxs-lookup"><span data-stu-id="6b7df-126">[Lead Entity](entities/lead.md) </span></span>  
 <span data-ttu-id="6b7df-127">[Sample: Qualify a Lead](sample-qualify-lead.md) </span><span class="sxs-lookup"><span data-stu-id="6b7df-127">[Sample: Qualify a Lead](sample-qualify-lead.md) </span></span>  
 <span data-ttu-id="6b7df-128">[Thực thể bán hàng](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span><span class="sxs-lookup"><span data-stu-id="6b7df-128">[Sales Entities](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span></span>  
 [<span data-ttu-id="6b7df-129">Opportunity Entities</span><span class="sxs-lookup"><span data-stu-id="6b7df-129">Opportunity Entities</span></span>](opportunity-entities.md)
