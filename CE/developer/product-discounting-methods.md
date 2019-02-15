---
title: Product discounting methods (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'The Organization.DiscountCalculationMethod attribute specifies the discount method: either line item or unit level.'
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 06c76a25-3bba-4d03-a37b-0f213a7576ca
caps.latest.revision: 11
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6c6d2bb353fcaf95ab969649765d88c28832bf57
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386204"
---
# <a name="product-discounting-methods"></a><span data-ttu-id="1892b-103">Product discounting methods</span><span class="sxs-lookup"><span data-stu-id="1892b-103">Product discounting methods</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1892b-104">Discounts can be applied either at the line item level or at per unit level.</span><span class="sxs-lookup"><span data-stu-id="1892b-104">Discounts can be applied either at the line item level or at per unit level.</span></span> <span data-ttu-id="1892b-105">Use the `Organization.DiscountCalculationMethod` attribute to specify the discount method.</span><span class="sxs-lookup"><span data-stu-id="1892b-105">Use the `Organization.DiscountCalculationMethod` attribute to specify the discount method.</span></span> <span data-ttu-id="1892b-106">Set the value of the attribute to:</span><span class="sxs-lookup"><span data-stu-id="1892b-106">Set the value of the attribute to:</span></span>  
  
- <span data-ttu-id="1892b-107">**0** for discounting at line item level</span><span class="sxs-lookup"><span data-stu-id="1892b-107">**0** for discounting at line item level</span></span>  
  
- <span data-ttu-id="1892b-108">**1** for discounting at per unit level</span><span class="sxs-lookup"><span data-stu-id="1892b-108">**1** for discounting at per unit level</span></span>  
  
  <span data-ttu-id="1892b-109">You can also use the **Sales** tab in the system settings area in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify the discount calculation method.</span><span class="sxs-lookup"><span data-stu-id="1892b-109">You can also use the **Sales** tab in the system settings area in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify the discount calculation method.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="1892b-110">[Manage product catalog configuration](https://technet.microsoft.com/library/dn832125.aspx)</span><span class="sxs-lookup"><span data-stu-id="1892b-110">[Manage product catalog configuration](https://technet.microsoft.com/library/dn832125.aspx)</span></span>  
  
  <span data-ttu-id="1892b-111">To illustrate the discounting model with an example, consider the following product line item entry in an opportunity:</span><span class="sxs-lookup"><span data-stu-id="1892b-111">To illustrate the discounting model with an example, consider the following product line item entry in an opportunity:</span></span>  
  
|<span data-ttu-id="1892b-112">Product Name</span><span class="sxs-lookup"><span data-stu-id="1892b-112">Product Name</span></span>|<span data-ttu-id="1892b-113">Price Per Unit</span><span class="sxs-lookup"><span data-stu-id="1892b-113">Price Per Unit</span></span>|<span data-ttu-id="1892b-114">Số lượng</span><span class="sxs-lookup"><span data-stu-id="1892b-114">Quantity</span></span>|<span data-ttu-id="1892b-115">Giảm giá</span><span class="sxs-lookup"><span data-stu-id="1892b-115">Discount</span></span>|<span data-ttu-id="1892b-116">Extended Amount</span><span class="sxs-lookup"><span data-stu-id="1892b-116">Extended Amount</span></span>|  
|------------------|--------------------|--------------|--------------|---------------------|  
|<span data-ttu-id="1892b-117">Example Product</span><span class="sxs-lookup"><span data-stu-id="1892b-117">Example Product</span></span>|<span data-ttu-id="1892b-118">100</span><span class="sxs-lookup"><span data-stu-id="1892b-118">100</span></span>|<span data-ttu-id="1892b-119">200</span><span class="sxs-lookup"><span data-stu-id="1892b-119">200</span></span>|<span data-ttu-id="1892b-120">10</span><span class="sxs-lookup"><span data-stu-id="1892b-120">10</span></span>|<span data-ttu-id="1892b-121">?</span><span class="sxs-lookup"><span data-stu-id="1892b-121">?</span></span>|  
  
 <span data-ttu-id="1892b-122">**Extended Amount** for the product line item entry is calculated depending on your selected discounting model:</span><span class="sxs-lookup"><span data-stu-id="1892b-122">**Extended Amount** for the product line item entry is calculated depending on your selected discounting model:</span></span>  
  
- <span data-ttu-id="1892b-123">**Line item**: The discount applied is 10, and the **Extended Amount** is 19990 ((Price Per Unit \* Quantity) – discount applied).</span><span class="sxs-lookup"><span data-stu-id="1892b-123">**Line item**: The discount applied is 10, and the **Extended Amount** is 19990 ((Price Per Unit \* Quantity) – discount applied).</span></span>  
  
- <span data-ttu-id="1892b-124">**Per unit**: The discount applied is 2000 (Quantity \* Discount), and the **Extended Amount** is 18000 ((Price Per Unit \* Quantity) – discount applied).</span><span class="sxs-lookup"><span data-stu-id="1892b-124">**Per unit**: The discount applied is 2000 (Quantity \* Discount), and the **Extended Amount** is 18000 ((Price Per Unit \* Quantity) – discount applied).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1892b-125">If you upgrade from a previous version of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] to the current version, by default the value of the `Organization.DiscountCalculationMethod` attribute is set to **0** (line item) to support the old discounting behavior where discounts could only be applied at the line level.</span><span class="sxs-lookup"><span data-stu-id="1892b-125">If you upgrade from a previous version of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] to the current version, by default the value of the `Organization.DiscountCalculationMethod` attribute is set to **0** (line item) to support the old discounting behavior where discounts could only be applied at the line level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1892b-126">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1892b-126">See also</span></span>

 <span data-ttu-id="1892b-127">[Discount Entity](entities/discount.md) </span><span class="sxs-lookup"><span data-stu-id="1892b-127">[Discount Entity](entities/discount.md) </span></span>  
 <span data-ttu-id="1892b-128">[DiscountType Entity](entities/discounttype.md) </span><span class="sxs-lookup"><span data-stu-id="1892b-128">[DiscountType Entity](entities/discounttype.md) </span></span>  
 [<span data-ttu-id="1892b-129">Product catalog entities</span><span class="sxs-lookup"><span data-stu-id="1892b-129">Product catalog entities</span></span>](product-catalog-entities.md)
