---
title: How hierarchical security can be used to control access to entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Provides an additional, more granular security model for accessing records in a hierarchical organizational structure.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 61ec481c-c128-498b-a784-16fe11af424b
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 97352c1f0e86762f26d3de31f2f83f38cc65d992
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387874"
---
# <a name="how-hierarchical-security-can-be-used-to-control-access-to-entities"></a><span data-ttu-id="c2767-103">How hierarchical security can be used to control access to entities</span><span class="sxs-lookup"><span data-stu-id="c2767-103">How hierarchical security can be used to control access to entities</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c2767-104">Hierarchy security offers a more granular access to records for an organization and helps to bring the maintenance costs down.</span><span class="sxs-lookup"><span data-stu-id="c2767-104">Hierarchy security offers a more granular access to records for an organization and helps to bring the maintenance costs down.</span></span> <span data-ttu-id="c2767-105">Ví dụ, trong các tình huống phức tạp, bạn có thể bắt đầu với việc tạo ra một số đơn vị kinh doanh và sau đó thêm an ninh hệ thống phân cấp.</span><span class="sxs-lookup"><span data-stu-id="c2767-105">For example, in complex scenarios, you can start with creating several business units and then add the hierarchy security.</span></span> <span data-ttu-id="c2767-106">Điều này sẽ đạt được một truy cập vào dữ liệu chi tiết hơn với ít chi phí bảo trì thấp hơn nhiều chi phí số lớn các đơn vị kinh doanh có thể yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="c2767-106">This will achieve a more granular access to data with far less maintenance costs that a large number of business units may require.</span></span> <span data-ttu-id="c2767-107">The hierarchy security model is an extension to the earlier security models that use business units, security roles, sharing, and teams.</span><span class="sxs-lookup"><span data-stu-id="c2767-107">The hierarchy security model is an extension to the earlier security models that use business units, security roles, sharing, and teams.</span></span> <span data-ttu-id="c2767-108">Nó có thể được sử dụng kết hợp với tất cả các mô hình bảo mật hiện tại.</span><span class="sxs-lookup"><span data-stu-id="c2767-108">It can be used in conjunction with all other existing security models.</span></span>  
  
 <span data-ttu-id="c2767-109">Previously, implementing this kind of security often required developers to mimic this behavior using custom plug-ins. Now, with the hierarchy security model, that type of security is built into the  product.</span><span class="sxs-lookup"><span data-stu-id="c2767-109">Previously, implementing this kind of security often required developers to mimic this behavior using custom plug-ins. Now, with the hierarchy security model, that type of security is built into the  product.</span></span> <span data-ttu-id="c2767-110">This removes the need to create and update custom plug-ins.</span><span class="sxs-lookup"><span data-stu-id="c2767-110">This removes the need to create and update custom plug-ins.</span></span>  
  
 <span data-ttu-id="c2767-111">For a detailed description of the hierarchy security model, see [Security concepts for Microsoft Dynamics 365 for Customer Engagment apps](https://technet.microsoft.com/library/hh699698.aspx) in the [!INCLUDE[pn_crm_2015_ig](../../includes/pn-crm-2015-ig.md)] for Customer Engagement apps documentation.</span><span class="sxs-lookup"><span data-stu-id="c2767-111">For a detailed description of the hierarchy security model, see [Security concepts for Microsoft Dynamics 365 for Customer Engagment apps](https://technet.microsoft.com/library/hh699698.aspx) in the [!INCLUDE[pn_crm_2015_ig](../../includes/pn-crm-2015-ig.md)] for Customer Engagement apps documentation.</span></span>  
  
 [<span data-ttu-id="c2767-112">Video: Hierarchical Security Modelling in Microsoft Dynamics CRM 2015</span><span class="sxs-lookup"><span data-stu-id="c2767-112">Video: Hierarchical Security Modelling in Microsoft Dynamics CRM 2015</span></span>](http://youtu.be/kx5So32DrCo)  
  
## <a name="position-hierarchy"></a><span data-ttu-id="c2767-113">hệ thống cấp bậc vị trí</span><span class="sxs-lookup"><span data-stu-id="c2767-113">Position hierarchy</span></span>  
 <span data-ttu-id="c2767-114">Administrators can define various job positions in the organization and arrange them in the position hierarchy.</span><span class="sxs-lookup"><span data-stu-id="c2767-114">Administrators can define various job positions in the organization and arrange them in the position hierarchy.</span></span> <span data-ttu-id="c2767-115">You can add users to any given position or “tag” a user with a particular position.</span><span class="sxs-lookup"><span data-stu-id="c2767-115">You can add users to any given position or “tag” a user with a particular position.</span></span> <span data-ttu-id="c2767-116">A user can be tagged only with one position in a given hierarchy; however, a position can be used for multiple users.</span><span class="sxs-lookup"><span data-stu-id="c2767-116">A user can be tagged only with one position in a given hierarchy; however, a position can be used for multiple users.</span></span> <span data-ttu-id="c2767-117">Người dùng tại các vị trí cao hơn trong hệ thống có quyền truy cập vào dữ liệu của những người sử dụng tại các vị trí thấp hơn, trong đường dẫn tổ tiên trực tiếp.</span><span class="sxs-lookup"><span data-stu-id="c2767-117">Users at the higher positions in the hierarchy have access to the data of the users at the lower positions, in the direct ancestor path.</span></span> <span data-ttu-id="c2767-118">The direct higher positions have Read, Write, Update, Append, and AppendTo access to the lower positions’ data in the direct ancestor path.</span><span class="sxs-lookup"><span data-stu-id="c2767-118">The direct higher positions have Read, Write, Update, Append, and AppendTo access to the lower positions’ data in the direct ancestor path.</span></span> <span data-ttu-id="c2767-119">The non-direct higher positions have read-only access to the lower positions’ data in the direct ancestor path.</span><span class="sxs-lookup"><span data-stu-id="c2767-119">The non-direct higher positions have read-only access to the lower positions’ data in the direct ancestor path.</span></span>  
  
 <span data-ttu-id="c2767-120">With the position hierarchy security, a user at a higher position has access to the records owned by a lower position user or by the team that a user is a member of, and to the records that are directly shared to the user or the team that a user is a member of.</span><span class="sxs-lookup"><span data-stu-id="c2767-120">With the position hierarchy security, a user at a higher position has access to the records owned by a lower position user or by the team that a user is a member of, and to the records that are directly shared to the user or the team that a user is a member of.</span></span> <span data-ttu-id="c2767-121">In addition to the position hierarchy security model, the users at a higher level must have at least the user level Read privilege on an entity to see the records that the users at the lower positions have access to.</span><span class="sxs-lookup"><span data-stu-id="c2767-121">In addition to the position hierarchy security model, the users at a higher level must have at least the user level Read privilege on an entity to see the records that the users at the lower positions have access to.</span></span> <span data-ttu-id="c2767-122">For example, if a user at a higher level doesn’t have the Read access to the `Case` entity, that user won’t be able to see the cases that the users at a lower positions have access to.</span><span class="sxs-lookup"><span data-stu-id="c2767-122">For example, if a user at a higher level doesn’t have the Read access to the `Case` entity, that user won’t be able to see the cases that the users at a lower positions have access to.</span></span>  
  
 <span data-ttu-id="c2767-123">As a developer, you can implement a position hierarchy by using the **Position** entity.</span><span class="sxs-lookup"><span data-stu-id="c2767-123">As a developer, you can implement a position hierarchy by using the **Position** entity.</span></span>  
  
 <span data-ttu-id="c2767-124">Two new privileges have been added that are related to the position hierarchy feature as shown in the table below.</span><span class="sxs-lookup"><span data-stu-id="c2767-124">Two new privileges have been added that are related to the position hierarchy feature as shown in the table below.</span></span>  
  
|<span data-ttu-id="c2767-125">Đặc quyền</span><span class="sxs-lookup"><span data-stu-id="c2767-125">Privilege</span></span>|<span data-ttu-id="c2767-126">Mô tả</span><span class="sxs-lookup"><span data-stu-id="c2767-126">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c2767-127">prvAssignPosition</span><span class="sxs-lookup"><span data-stu-id="c2767-127">prvAssignPosition</span></span>|<span data-ttu-id="c2767-128">Assign a position to a system user.</span><span class="sxs-lookup"><span data-stu-id="c2767-128">Assign a position to a system user.</span></span>|  
|<span data-ttu-id="c2767-129">prvWriteHierarchicalSecurityConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2767-129">prvWriteHierarchicalSecurityConfiguration</span></span>|<span data-ttu-id="c2767-130">Change hierarchy security settings.</span><span class="sxs-lookup"><span data-stu-id="c2767-130">Change hierarchy security settings.</span></span>|  
  
 <span data-ttu-id="c2767-131">For more information about the `Position` entity and its messages, see [Position Entity](../entities/position.md).</span><span class="sxs-lookup"><span data-stu-id="c2767-131">For more information about the `Position` entity and its messages, see [Position Entity](../entities/position.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c2767-132">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c2767-132">See also</span></span>  
 <span data-ttu-id="c2767-133">[Video: Hierarchical Security Modelling in Microsoft Dynamics CRM 2015](http://youtu.be/kx5So32DrCo) </span><span class="sxs-lookup"><span data-stu-id="c2767-133">[Video: Hierarchical Security Modelling in Microsoft Dynamics CRM 2015](http://youtu.be/kx5So32DrCo) </span></span>  
 <span data-ttu-id="c2767-134">[The Security Model of Microsoft Dynamics 365 for Customer Engagement apps](security-model.md) </span><span class="sxs-lookup"><span data-stu-id="c2767-134">[The Security Model of Microsoft Dynamics 365 for Customer Engagement apps](security-model.md) </span></span>  
 <span data-ttu-id="c2767-135">[Security concepts for Microsoft Dynamics 365 for Customer Engagement apps](https://technet.microsoft.com/library/hh699698.aspx) [Position Entity](../entities/position.md)</span><span class="sxs-lookup"><span data-stu-id="c2767-135">[Security concepts for Microsoft Dynamics 365 for Customer Engagement apps](https://technet.microsoft.com/library/hh699698.aspx) [Position Entity](../entities/position.md)</span></span>
