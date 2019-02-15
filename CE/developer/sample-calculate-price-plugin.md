---
title: 'Sample: Calculate Price plug-in (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrates how to write a plug-in that calculates the pricing of the opportunities, quotes, orders, and invoices based on your custom code.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 683204f7-570a-43ab-bf7e-a12d26cec214
author: KumarVivek
ms.author: kvivek
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 12
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2fbe138bd192686a135e98c635d5e28371f7b56c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385653"
---
# <a name="sample-calculate-price-plug-in"></a><span data-ttu-id="9b0e8-103">Sample: Calculate Price plug-in</span><span class="sxs-lookup"><span data-stu-id="9b0e8-103">Sample: Calculate Price plug-in</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9b0e8-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="9b0e8-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="9b0e8-105">Download the sample: [Work with custom price plug-in](https://msdn.microsoft.com/en-us/library/dn817877.aspx).</span><span class="sxs-lookup"><span data-stu-id="9b0e8-105">Download the sample: [Work with custom price plug-in](https://msdn.microsoft.com/en-us/library/dn817877.aspx).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9b0e8-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="9b0e8-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]

## <a name="requirements"></a><span data-ttu-id="9b0e8-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="9b0e8-107">Requirements</span></span>  
 <span data-ttu-id="9b0e8-108">Ensure the following:</span><span class="sxs-lookup"><span data-stu-id="9b0e8-108">Ensure the following:</span></span>  
  
-   <span data-ttu-id="9b0e8-109">Set the value of the `Organization.OOBPriceCalculationEnabled` attribute to `0` (false).</span><span class="sxs-lookup"><span data-stu-id="9b0e8-109">Set the value of the `Organization.OOBPriceCalculationEnabled` attribute to `0` (false).</span></span>  
  
-   <span data-ttu-id="9b0e8-110">Register the plug-in on the **CalculatePrice** message, **Post-operation** event stage, and **Synchronous** execution mode.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-110">Register the plug-in on the **CalculatePrice** message, **Post-operation** event stage, and **Synchronous** execution mode.</span></span> <span data-ttu-id="9b0e8-111">For more information, see [Register and Deploy Plug-ins](register-deploy-plugins.md).</span><span class="sxs-lookup"><span data-stu-id="9b0e8-111">For more information, see [Register and Deploy Plug-ins](register-deploy-plugins.md).</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="9b0e8-112">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="9b0e8-112">Demonstrates</span></span>  
 <span data-ttu-id="9b0e8-113">This sample shows how to write a plug-in that calculates the pricing of the opportunities, quotes, orders, and invoices based on your custom code.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-113">This sample shows how to write a plug-in that calculates the pricing of the opportunities, quotes, orders, and invoices based on your custom code.</span></span> <span data-ttu-id="9b0e8-114">The discounts and taxes are calculated based on the total amount of all the product line items in an opportunity, quote, order, or invoice:</span><span class="sxs-lookup"><span data-stu-id="9b0e8-114">The discounts and taxes are calculated based on the total amount of all the product line items in an opportunity, quote, order, or invoice:</span></span>  
  
- <span data-ttu-id="9b0e8-115">**Discount**: If the total amount is greater than 1000 and less than 5000, discount is 5%; if the total amount is 5000 or greater, discount is 10%.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-115">**Discount**: If the total amount is greater than 1000 and less than 5000, discount is 5%; if the total amount is 5000 or greater, discount is 10%.</span></span>  
  
- <span data-ttu-id="9b0e8-116">**Tax**: Tax is applied on the amount that is effective after the discount is applied (total amount minus discount).</span><span class="sxs-lookup"><span data-stu-id="9b0e8-116">**Tax**: Tax is applied on the amount that is effective after the discount is applied (total amount minus discount).</span></span> <span data-ttu-id="9b0e8-117">If the effective amount is less than 5000, tax is 10%; otherwise, tax is 8%.</span><span class="sxs-lookup"><span data-stu-id="9b0e8-117">If the effective amount is less than 5000, tax is 10%; otherwise, tax is 8%.</span></span>  
  
  <span data-ttu-id="9b0e8-118">Để biết thêm chi tiết, xem [sử dụng định giá tùy chỉnh cho sản phẩm](use-custom-pricing-products.md).</span><span class="sxs-lookup"><span data-stu-id="9b0e8-118">For more information, see [Use custom pricing for products](use-custom-pricing-products.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="9b0e8-119">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="9b0e8-119">Example</span></span>  
 [!code-csharp[Plug-Ins#CalculatePricePlugin](../snippets/csharp/CRMV8/plug-ins/cs/calculatepriceplugin.cs#calculatepriceplugin)]  
  
### <a name="see-also"></a><span data-ttu-id="9b0e8-120">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9b0e8-120">See also</span></span>  
 <span data-ttu-id="9b0e8-121">[Use custom pricing for products](use-custom-pricing-products.md) </span><span class="sxs-lookup"><span data-stu-id="9b0e8-121">[Use custom pricing for products](use-custom-pricing-products.md) </span></span>  
 <span data-ttu-id="9b0e8-122">[Create and manage product families, products and bundles](create-manage-product-families-products-bundles-product-properties.md) </span><span class="sxs-lookup"><span data-stu-id="9b0e8-122">[Create and manage product families, products and bundles](create-manage-product-families-products-bundles-product-properties.md) </span></span>  
 [<span data-ttu-id="9b0e8-123">Thực thể Danh mục Sản phẩm</span><span class="sxs-lookup"><span data-stu-id="9b0e8-123">Product catalog entities</span></span>](product-catalog-entities.md)
