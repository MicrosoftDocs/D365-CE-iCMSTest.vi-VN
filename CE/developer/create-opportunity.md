---
title: Create an opportunity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about creating a new opportunity or an opportunity from a qualified lead. An opportunity contains sales information like quotes, sales orders, and invoices.
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
- tax; freight; and totals, opportunity entities
- closing opportunities, opportunity entities
- opportunity entities, associating opportunities with accounts and contacts
- associating opportunities with accounts and contacts, opportunity entities
- opportunity entities, qualifying leads for opportunities
- overriding and discounting prices, opportunity entities
- prices, overriding and discounting
- adding products to opportunities, opportunity entities
- qualifying leads for opportunities, opportunity entities
- opportunity entities, overriding and discounting prices
- calculating tax; freight; and totals, opportunity entities
- opportunity entities, sales information contained in
- opportunity entities, adding products to opportunities
- opportunity entities, calculating tax; freight; and totals
- creating opportunities, introduction
- opportunity entities, creating and closing opportunities
ms.assetid: c607f3e9-58e2-4f5a-9ea3-30ba4f12f060
caps.latest.revision: 32
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 20f3191edfb3c330f36d57cbc01f412ca025a2c4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388395"
---
# <a name="create-an-opportunity"></a><span data-ttu-id="2abb2-104">Create an opportunity</span><span class="sxs-lookup"><span data-stu-id="2abb2-104">Create an opportunity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2abb2-105">You can create an opportunity from a qualified lead or you can create a new opportunity for one of your existing customers.</span><span class="sxs-lookup"><span data-stu-id="2abb2-105">You can create an opportunity from a qualified lead or you can create a new opportunity for one of your existing customers.</span></span> <span data-ttu-id="2abb2-106">You can track the information about each opportunity, such as state and status of the opportunity, the probability of the sale, and the estimated closing date.</span><span class="sxs-lookup"><span data-stu-id="2abb2-106">You can track the information about each opportunity, such as state and status of the opportunity, the probability of the sale, and the estimated closing date.</span></span> <span data-ttu-id="2abb2-107">An opportunity contains important sales information that can be used later in quotes, sales orders, and invoices.</span><span class="sxs-lookup"><span data-stu-id="2abb2-107">An opportunity contains important sales information that can be used later in quotes, sales orders, and invoices.</span></span> <span data-ttu-id="2abb2-108">The sales information includes:</span><span class="sxs-lookup"><span data-stu-id="2abb2-108">The sales information includes:</span></span>  
  
-   <span data-ttu-id="2abb2-109">Products and services from the product catalog and write-in products that you plan to sell</span><span class="sxs-lookup"><span data-stu-id="2abb2-109">Products and services from the product catalog and write-in products that you plan to sell</span></span>  
  
-   <span data-ttu-id="2abb2-110">Overridden prices of the products and services from the product catalog</span><span class="sxs-lookup"><span data-stu-id="2abb2-110">Overridden prices of the products and services from the product catalog</span></span>  
  
-   <span data-ttu-id="2abb2-111">Discounted prices of the products and services from the product catalog and the write-in products</span><span class="sxs-lookup"><span data-stu-id="2abb2-111">Discounted prices of the products and services from the product catalog and the write-in products</span></span>  
  
-   <span data-ttu-id="2abb2-112">Calculated or estimated revenues</span><span class="sxs-lookup"><span data-stu-id="2abb2-112">Calculated or estimated revenues</span></span>  
  
-   <span data-ttu-id="2abb2-113">Freight rates</span><span class="sxs-lookup"><span data-stu-id="2abb2-113">Freight rates</span></span>  
  
-   <span data-ttu-id="2abb2-114">Calculated tax and cost totals</span><span class="sxs-lookup"><span data-stu-id="2abb2-114">Calculated tax and cost totals</span></span>  
  
<a name="bkmk_PreparingDataforanOpportunity"></a>   
## <a name="prepare-data-for-an-opportunity"></a><span data-ttu-id="2abb2-115">Prepare Data for an Opportunity</span><span class="sxs-lookup"><span data-stu-id="2abb2-115">Prepare Data for an Opportunity</span></span>  
 <span data-ttu-id="2abb2-116">Before you create an opportunity, ensure that [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] contains necessary data:</span><span class="sxs-lookup"><span data-stu-id="2abb2-116">Before you create an opportunity, ensure that [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] contains necessary data:</span></span>  
  
- <span data-ttu-id="2abb2-117">Create accounts, contacts, and leads before you create an opportunity.</span><span class="sxs-lookup"><span data-stu-id="2abb2-117">Create accounts, contacts, and leads before you create an opportunity.</span></span> <span data-ttu-id="2abb2-118">You can create an opportunity for an existing account or contact, or convert a qualified lead into an opportunity.</span><span class="sxs-lookup"><span data-stu-id="2abb2-118">You can create an opportunity for an existing account or contact, or convert a qualified lead into an opportunity.</span></span>  
  
- <span data-ttu-id="2abb2-119">Each opportunity must be associated with one account or a contact.</span><span class="sxs-lookup"><span data-stu-id="2abb2-119">Each opportunity must be associated with one account or a contact.</span></span>  
  
- <span data-ttu-id="2abb2-120">Qualify a lead for an opportunity by using your company’s lead qualification criteria.</span><span class="sxs-lookup"><span data-stu-id="2abb2-120">Qualify a lead for an opportunity by using your company’s lead qualification criteria.</span></span> <span data-ttu-id="2abb2-121">The possible states for a lead are Open, Qualified, and Disqualified.</span><span class="sxs-lookup"><span data-stu-id="2abb2-121">The possible states for a lead are Open, Qualified, and Disqualified.</span></span>  
  
  <span data-ttu-id="2abb2-122">If you add products to an opportunity, the system must contain a product catalog, products, price lists, and units of measure.</span><span class="sxs-lookup"><span data-stu-id="2abb2-122">If you add products to an opportunity, the system must contain a product catalog, products, price lists, and units of measure.</span></span>  
  
<a name="bkmk_AddExistingProducts"></a>   
## <a name="add-existing-products-and-write-in-products"></a><span data-ttu-id="2abb2-123">Add Existing Products and Write-in Products</span><span class="sxs-lookup"><span data-stu-id="2abb2-123">Add Existing Products and Write-in Products</span></span>  
 <span data-ttu-id="2abb2-124">A single opportunity may be associated with multiple products that include existing products and write-in products.</span><span class="sxs-lookup"><span data-stu-id="2abb2-124">A single opportunity may be associated with multiple products that include existing products and write-in products.</span></span> <span data-ttu-id="2abb2-125">Existing products are a part of the product catalog and are associated with the price lists in the product catalog.</span><span class="sxs-lookup"><span data-stu-id="2abb2-125">Existing products are a part of the product catalog and are associated with the price lists in the product catalog.</span></span> <span data-ttu-id="2abb2-126">Write-in products are products that your company sells, but does not include in the product catalog.</span><span class="sxs-lookup"><span data-stu-id="2abb2-126">Write-in products are products that your company sells, but does not include in the product catalog.</span></span> <span data-ttu-id="2abb2-127">The prices of write-in products are not associated with the price lists in the product catalog.</span><span class="sxs-lookup"><span data-stu-id="2abb2-127">The prices of write-in products are not associated with the price lists in the product catalog.</span></span> <span data-ttu-id="2abb2-128">An existing product or a write-in product is a line item in the opportunity record.</span><span class="sxs-lookup"><span data-stu-id="2abb2-128">An existing product or a write-in product is a line item in the opportunity record.</span></span> <span data-ttu-id="2abb2-129">The existing products and the write-in products are represented by the opportunity product entity.</span><span class="sxs-lookup"><span data-stu-id="2abb2-129">The existing products and the write-in products are represented by the opportunity product entity.</span></span> <span data-ttu-id="2abb2-130">To associate the products with a specific opportunity, use the `OpportunityProduct.OpportunityId` attribute.</span><span class="sxs-lookup"><span data-stu-id="2abb2-130">To associate the products with a specific opportunity, use the `OpportunityProduct.OpportunityId` attribute.</span></span>  
  
 <span data-ttu-id="2abb2-131">To set up a product catalog, products, price lists, and discount lists you must have system administrator privileges.</span><span class="sxs-lookup"><span data-stu-id="2abb2-131">To set up a product catalog, products, price lists, and discount lists you must have system administrator privileges.</span></span>  
  
### <a name="add-existing-products-from-the-product-catalog"></a><span data-ttu-id="2abb2-132">Add Existing Products from the Product Catalog</span><span class="sxs-lookup"><span data-stu-id="2abb2-132">Add Existing Products from the Product Catalog</span></span>  
 <span data-ttu-id="2abb2-133">To specify an existing product from the catalog, set the `OpportunityProduct.IsProductOverridden` attribute to `false`.</span><span class="sxs-lookup"><span data-stu-id="2abb2-133">To specify an existing product from the catalog, set the `OpportunityProduct.IsProductOverridden` attribute to `false`.</span></span> <span data-ttu-id="2abb2-134">Specify the following information: product ID (`OpportunityProduct.ProductId`), price per unit (`OpportunityProduct.PricePerUnit`), quantity (`OpportunityProduct.Quantity`) and units of measure (`OpportunityProduct.UomId`).</span><span class="sxs-lookup"><span data-stu-id="2abb2-134">Specify the following information: product ID (`OpportunityProduct.ProductId`), price per unit (`OpportunityProduct.PricePerUnit`), quantity (`OpportunityProduct.Quantity`) and units of measure (`OpportunityProduct.UomId`).</span></span> <span data-ttu-id="2abb2-135">To associate a price list with the opportunity, use the `Opportunity.PriceLevelId` attribute.</span><span class="sxs-lookup"><span data-stu-id="2abb2-135">To associate a price list with the opportunity, use the `Opportunity.PriceLevelId` attribute.</span></span> <span data-ttu-id="2abb2-136">You can add other product-related data, such as tax amount (`OpportunityProduct.Tax`), volume discount (`OpportunityProduct.VolumeDiscountAmount`), or manual discount (`OpportunityProduct.ManualDiscountAmount`).</span><span class="sxs-lookup"><span data-stu-id="2abb2-136">You can add other product-related data, such as tax amount (`OpportunityProduct.Tax`), volume discount (`OpportunityProduct.VolumeDiscountAmount`), or manual discount (`OpportunityProduct.ManualDiscountAmount`).</span></span>  
  
### <a name="add-write-in-products"></a><span data-ttu-id="2abb2-137">Add Write-in Products</span><span class="sxs-lookup"><span data-stu-id="2abb2-137">Add Write-in Products</span></span>  
 <span data-ttu-id="2abb2-138">Although, a write-in product is not in the product catalog, you can add it to an opportunity.</span><span class="sxs-lookup"><span data-stu-id="2abb2-138">Although, a write-in product is not in the product catalog, you can add it to an opportunity.</span></span> <span data-ttu-id="2abb2-139">To specify a write-in product, set the `OpportunityProduct.IsProductOverridden` attribute to `true`.</span><span class="sxs-lookup"><span data-stu-id="2abb2-139">To specify a write-in product, set the `OpportunityProduct.IsProductOverridden` attribute to `true`.</span></span> <span data-ttu-id="2abb2-140">Specify the following information: product description (`OpportunityProduct.ProductDescription`), price per unit (`OpportunityProduct.PricePerUnit`), and quantity (`OpportunityProduct.Quantity`).</span><span class="sxs-lookup"><span data-stu-id="2abb2-140">Specify the following information: product description (`OpportunityProduct.ProductDescription`), price per unit (`OpportunityProduct.PricePerUnit`), and quantity (`OpportunityProduct.Quantity`).</span></span> <span data-ttu-id="2abb2-141">You can add other product-related data, such as tax amount (`OpportunityProduct.Tax`), volume discount (`OpportunityProduct.VolumeDiscountAmount`), or manual discount (`OpportunityProduct.ManualDiscountAmount`).</span><span class="sxs-lookup"><span data-stu-id="2abb2-141">You can add other product-related data, such as tax amount (`OpportunityProduct.Tax`), volume discount (`OpportunityProduct.VolumeDiscountAmount`), or manual discount (`OpportunityProduct.ManualDiscountAmount`).</span></span>  
  
<a name="bkmk_PriceOverride"></a>   
## <a name="price-overriding"></a><span data-ttu-id="2abb2-142">Price Overriding</span><span class="sxs-lookup"><span data-stu-id="2abb2-142">Price Overriding</span></span>  
 <span data-ttu-id="2abb2-143">For a write-in product, you can use any price that you want and the quantities that you plan to sell.</span><span class="sxs-lookup"><span data-stu-id="2abb2-143">For a write-in product, you can use any price that you want and the quantities that you plan to sell.</span></span> <span data-ttu-id="2abb2-144">However, if you add an existing product from the catalog, you have an option to override the list price.</span><span class="sxs-lookup"><span data-stu-id="2abb2-144">However, if you add an existing product from the catalog, you have an option to override the list price.</span></span> <span data-ttu-id="2abb2-145">To override the list price of the existing product, set the `OpportunityProduct.IsPriceOverridden` attribute to `true`.</span><span class="sxs-lookup"><span data-stu-id="2abb2-145">To override the list price of the existing product, set the `OpportunityProduct.IsPriceOverridden` attribute to `true`.</span></span> <span data-ttu-id="2abb2-146">Specify a desired price by using the `OpportunityProduct.PricePerUnit` attribute.</span><span class="sxs-lookup"><span data-stu-id="2abb2-146">Specify a desired price by using the `OpportunityProduct.PricePerUnit` attribute.</span></span>  
  
<a name="bkmk_ApplyDiscounts"></a>   
## <a name="apply-discounts"></a><span data-ttu-id="2abb2-147">Apply Discounts</span><span class="sxs-lookup"><span data-stu-id="2abb2-147">Apply Discounts</span></span>  
 <span data-ttu-id="2abb2-148">In addition to price overriding, you can apply volume discounts and manual discounts.</span><span class="sxs-lookup"><span data-stu-id="2abb2-148">In addition to price overriding, you can apply volume discounts and manual discounts.</span></span> <span data-ttu-id="2abb2-149">The discounts can be applied to line items and to a whole opportunity.</span><span class="sxs-lookup"><span data-stu-id="2abb2-149">The discounts can be applied to line items and to a whole opportunity.</span></span>  
  
 <span data-ttu-id="2abb2-150">For example, if the average order from your customers is for five units of your product, you could create an incentive for your customers to order more than five units by giving them a discount when they order six or more units.</span><span class="sxs-lookup"><span data-stu-id="2abb2-150">For example, if the average order from your customers is for five units of your product, you could create an incentive for your customers to order more than five units by giving them a discount when they order six or more units.</span></span> <span data-ttu-id="2abb2-151">A discount can be specified as a percentage or an amount.</span><span class="sxs-lookup"><span data-stu-id="2abb2-151">A discount can be specified as a percentage or an amount.</span></span> <span data-ttu-id="2abb2-152">To specify a volume discount for the opportunity product, use the `OpportunityProduct.VolumeDiscountAmount` attribute.</span><span class="sxs-lookup"><span data-stu-id="2abb2-152">To specify a volume discount for the opportunity product, use the `OpportunityProduct.VolumeDiscountAmount` attribute.</span></span> <span data-ttu-id="2abb2-153">To specify a manual discount for the opportunity product, use the `OpportunityProduct.ManualDiscountAmount` attribute.</span><span class="sxs-lookup"><span data-stu-id="2abb2-153">To specify a manual discount for the opportunity product, use the `OpportunityProduct.ManualDiscountAmount` attribute.</span></span> <span data-ttu-id="2abb2-154">To specify an overall discount for the opportunity, use the `Opportunity.DiscountAmount` attribute.</span><span class="sxs-lookup"><span data-stu-id="2abb2-154">To specify an overall discount for the opportunity, use the `Opportunity.DiscountAmount` attribute.</span></span>  
  
<a name="bkmk_CalculateTax"></a>   
## <a name="calculate-tax-and-totals"></a><span data-ttu-id="2abb2-155">Calculate Tax and Totals</span><span class="sxs-lookup"><span data-stu-id="2abb2-155">Calculate Tax and Totals</span></span>  
 <span data-ttu-id="2abb2-156">The estimated tax and the estimated total value of the opportunity are automatically calculated.</span><span class="sxs-lookup"><span data-stu-id="2abb2-156">The estimated tax and the estimated total value of the opportunity are automatically calculated.</span></span> <span data-ttu-id="2abb2-157">The estimated value is based on the combined cost of all products added to the opportunity and the associated price lists.</span><span class="sxs-lookup"><span data-stu-id="2abb2-157">The estimated value is based on the combined cost of all products added to the opportunity and the associated price lists.</span></span> <span data-ttu-id="2abb2-158">Instead of using the system calculated value, you can specify the estimated revenue for the opportunity.</span><span class="sxs-lookup"><span data-stu-id="2abb2-158">Instead of using the system calculated value, you can specify the estimated revenue for the opportunity.</span></span> <span data-ttu-id="2abb2-159">To do this, set the `Opportunity.IsRevenueSystemCalculated` attribute to `false` and specify the estimated value in the `Opportunity.EstimatedValue` attribute.</span><span class="sxs-lookup"><span data-stu-id="2abb2-159">To do this, set the `Opportunity.IsRevenueSystemCalculated` attribute to `false` and specify the estimated value in the `Opportunity.EstimatedValue` attribute.</span></span>  
  
 <span data-ttu-id="2abb2-160">The breakdown of the opportunity total costs is a follows:</span><span class="sxs-lookup"><span data-stu-id="2abb2-160">The breakdown of the opportunity total costs is a follows:</span></span>  
  
- <span data-ttu-id="2abb2-161">Total amount</span><span class="sxs-lookup"><span data-stu-id="2abb2-161">Total amount</span></span>  
  
- <span data-ttu-id="2abb2-162">Total amount less freight</span><span class="sxs-lookup"><span data-stu-id="2abb2-162">Total amount less freight</span></span>  
  
- <span data-ttu-id="2abb2-163">Total discount amount</span><span class="sxs-lookup"><span data-stu-id="2abb2-163">Total discount amount</span></span>  
  
- <span data-ttu-id="2abb2-164">Total line item amount</span><span class="sxs-lookup"><span data-stu-id="2abb2-164">Total line item amount</span></span>  
  
- <span data-ttu-id="2abb2-165">Total line item discount amount</span><span class="sxs-lookup"><span data-stu-id="2abb2-165">Total line item discount amount</span></span>  
  
- <span data-ttu-id="2abb2-166">Total discount</span><span class="sxs-lookup"><span data-stu-id="2abb2-166">Total discount</span></span>  
  
- <span data-ttu-id="2abb2-167">Total tax</span><span class="sxs-lookup"><span data-stu-id="2abb2-167">Total tax</span></span>  
  
  <span data-ttu-id="2abb2-168">Having information about individual costs helps you analyze your overall cost.</span><span class="sxs-lookup"><span data-stu-id="2abb2-168">Having information about individual costs helps you analyze your overall cost.</span></span> <span data-ttu-id="2abb2-169">You can make necessary adjustments to pricing, discounts, and freight cost to help with closing a deal.</span><span class="sxs-lookup"><span data-stu-id="2abb2-169">You can make necessary adjustments to pricing, discounts, and freight cost to help with closing a deal.</span></span>  
  
<a name="bkmk_CloseAnOpportunity"></a>   
## <a name="close-an-opportunity"></a><span data-ttu-id="2abb2-170">Close an Opportunity</span><span class="sxs-lookup"><span data-stu-id="2abb2-170">Close an Opportunity</span></span>  
 <span data-ttu-id="2abb2-171">If a customer decides to purchase products or services from your company, you can close an opportunity as a won opportunity.</span><span class="sxs-lookup"><span data-stu-id="2abb2-171">If a customer decides to purchase products or services from your company, you can close an opportunity as a won opportunity.</span></span> <span data-ttu-id="2abb2-172">The opportunity states are specified in the `Opportunity.StateCode` attribute.</span><span class="sxs-lookup"><span data-stu-id="2abb2-172">The opportunity states are specified in the `Opportunity.StateCode` attribute.</span></span> <span data-ttu-id="2abb2-173">If you are using early bound types, you can use the `OpportunityState` enumeration.</span><span class="sxs-lookup"><span data-stu-id="2abb2-173">If you are using early bound types, you can use the `OpportunityState` enumeration.</span></span> <span data-ttu-id="2abb2-174">For a list of the state values, see the picklist values for this entity.</span><span class="sxs-lookup"><span data-stu-id="2abb2-174">For a list of the state values, see the picklist values for this entity.</span></span> [!INCLUDE[metadata_browser](../includes/metadata-browser.md)]  
  
 <span data-ttu-id="2abb2-175">When you close an opportunity, an activity is created automatically by creating a record of the entity type opportunity close.</span><span class="sxs-lookup"><span data-stu-id="2abb2-175">When you close an opportunity, an activity is created automatically by creating a record of the entity type opportunity close.</span></span> <span data-ttu-id="2abb2-176">The states of the opportunity close activity are specified in the `OpportunityClose.StateCode` attribute.</span><span class="sxs-lookup"><span data-stu-id="2abb2-176">The states of the opportunity close activity are specified in the `OpportunityClose.StateCode` attribute.</span></span> <span data-ttu-id="2abb2-177">If you are using early bound types, you can use the `OpportunityCloseState` enumeration.</span><span class="sxs-lookup"><span data-stu-id="2abb2-177">If you are using early bound types, you can use the `OpportunityCloseState` enumeration.</span></span> <span data-ttu-id="2abb2-178">For a list of the state values, see the picklist values for this entity.</span><span class="sxs-lookup"><span data-stu-id="2abb2-178">For a list of the state values, see the picklist values for this entity.</span></span>  
  
 <span data-ttu-id="2abb2-179">The opportunity close activity contains information about the user that created the activity, and the date and time when it was created.</span><span class="sxs-lookup"><span data-stu-id="2abb2-179">The opportunity close activity contains information about the user that created the activity, and the date and time when it was created.</span></span> <span data-ttu-id="2abb2-180">It also contains the information about the estimated revenue, close date, and competitor.</span><span class="sxs-lookup"><span data-stu-id="2abb2-180">It also contains the information about the estimated revenue, close date, and competitor.</span></span> <span data-ttu-id="2abb2-181">You can add notes that explain the reasons why you closed the opportunity.</span><span class="sxs-lookup"><span data-stu-id="2abb2-181">You can add notes that explain the reasons why you closed the opportunity.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="2abb2-182">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2abb2-182">See also</span></span>  
 <span data-ttu-id="2abb2-183">[Opportunity Entities](opportunity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="2abb2-183">[Opportunity Entities](opportunity-entities.md) </span></span>  
 <span data-ttu-id="2abb2-184">[Converting an Opportunity to a Quote, Sales Order or Invoice](convert-opportunity-quote-sales-order-invoice.md) </span><span class="sxs-lookup"><span data-stu-id="2abb2-184">[Converting an Opportunity to a Quote, Sales Order or Invoice](convert-opportunity-quote-sales-order-invoice.md) </span></span>  
 <span data-ttu-id="2abb2-185">[Product Catalog Entities](product-catalog-entities.md) </span><span class="sxs-lookup"><span data-stu-id="2abb2-185">[Product Catalog Entities](product-catalog-entities.md) </span></span>  
 <span data-ttu-id="2abb2-186">[Thực thể bán hàng](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span><span class="sxs-lookup"><span data-stu-id="2abb2-186">[Sales Entities](sales-entities-lead-opportunity-competitor-quote-order-invoice.md) </span></span>  
 <span data-ttu-id="2abb2-187">[Customer Entities](customer-entities-account-contact.md) </span><span class="sxs-lookup"><span data-stu-id="2abb2-187">[Customer Entities](customer-entities-account-contact.md) </span></span>  
 [<span data-ttu-id="2abb2-188">Create Early-Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)</span><span class="sxs-lookup"><span data-stu-id="2abb2-188">Create Early-Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)</span></span>](org-service/create-early-bound-entity-classes-code-generation-tool.md)
