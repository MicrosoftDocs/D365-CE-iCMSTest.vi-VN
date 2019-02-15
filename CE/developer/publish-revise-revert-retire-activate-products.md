---
title: Publish, revise, revert, retire, and activate products--product lifecycle (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Programmatically control the product lifecycle through the draft, active, under revision, and retired states.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ada37ff8-0f03-47b4-bfd7-25a4b0aacb5b
caps.latest.revision: 27
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0147afc8adec2572d42a3f18841415c6562aa6e7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386449"
---
# <a name="publish-revise-revert-retire-and-activate-products-product-lifecycle"></a><span data-ttu-id="3f15a-103">Publish, revise, revert, retire, and activate products (product lifecycle)</span><span class="sxs-lookup"><span data-stu-id="3f15a-103">Publish, revise, revert, retire, and activate products (product lifecycle)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3f15a-104">By default, a product record is in the **Draft** state when you create it, and isn’t available for your sales agents.</span><span class="sxs-lookup"><span data-stu-id="3f15a-104">By default, a product record is in the **Draft** state when you create it, and isn’t available for your sales agents.</span></span> <span data-ttu-id="3f15a-105">The record becomes available to your sales agents only when you publish it, which changes the state of the record to **Active**.</span><span class="sxs-lookup"><span data-stu-id="3f15a-105">The record becomes available to your sales agents only when you publish it, which changes the state of the record to **Active**.</span></span> <span data-ttu-id="3f15a-106">For products that aren’t associated with a product family, that is, products that don’t have a parent product family record, you can create them directly in an **Active** state by setting the **Organization.CreateProductsWithoutParentInActiveState** attribute to `1` (true).</span><span class="sxs-lookup"><span data-stu-id="3f15a-106">For products that aren’t associated with a product family, that is, products that don’t have a parent product family record, you can create them directly in an **Active** state by setting the **Organization.CreateProductsWithoutParentInActiveState** attribute to `1` (true).</span></span> <span data-ttu-id="3f15a-107">By default, this attribute is set to `0` (false) for a fresh installation of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] and to `1` (true) if you’re upgrading from a previous version of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] to ensure compatibility for your applications working with the previous version of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] where the product records were created in an **Active** state.</span><span class="sxs-lookup"><span data-stu-id="3f15a-107">By default, this attribute is set to `0` (false) for a fresh installation of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] and to `1` (true) if you’re upgrading from a previous version of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] to ensure compatibility for your applications working with the previous version of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] where the product records were created in an **Active** state.</span></span>  
  
 <span data-ttu-id="3f15a-108">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify whether products are created in an active state.</span><span class="sxs-lookup"><span data-stu-id="3f15a-108">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify whether products are created in an active state.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="3f15a-109">[Manage product catalog configuration](https://technet.microsoft.com/library/dn832125.aspx)</span><span class="sxs-lookup"><span data-stu-id="3f15a-109">[Manage product catalog configuration](https://technet.microsoft.com/library/dn832125.aspx)</span></span>  
  
 <span data-ttu-id="3f15a-110">Furthermore, you can revise, revert, retire, and activate your product records to maintain your product catalog as per your business requirements.</span><span class="sxs-lookup"><span data-stu-id="3f15a-110">Furthermore, you can revise, revert, retire, and activate your product records to maintain your product catalog as per your business requirements.</span></span> <span data-ttu-id="3f15a-111">The following illustration shows the state transitions of a product when you perform various operations on a product record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="3f15a-111">The following illustration shows the state transitions of a product when you perform various operations on a product record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span>  
  
 <span data-ttu-id="3f15a-112">![Product lifecycle and state transitions](media/crm-sdk-product-life-cycle.png "Product lifecycle and state transitions")</span><span class="sxs-lookup"><span data-stu-id="3f15a-112">![Product lifecycle and state transitions](media/crm-sdk-product-life-cycle.png "Product lifecycle and state transitions")</span></span>  
  
 <span data-ttu-id="3f15a-113">\*\*\*Activate\\*\*\*\* : The activate operation is applicable for certain type of product records only.</span><span class="sxs-lookup"><span data-stu-id="3f15a-113">\*\*\*Activate\\*\*\*\* : The activate operation is applicable for certain type of product records only.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="3f15a-114">[Activate a product or kit record](publish-revise-revert-retire-activate-products.md#Activate)</span><span class="sxs-lookup"><span data-stu-id="3f15a-114">[Activate a product or kit record](publish-revise-revert-retire-activate-products.md#Activate)</span></span>  
  
<a name="Publish"></a>   
## <a name="publish-a-product-family-product-or-bundle"></a><span data-ttu-id="3f15a-115">Publish a product family, product, or bundle</span><span class="sxs-lookup"><span data-stu-id="3f15a-115">Publish a product family, product, or bundle</span></span>  
 <span data-ttu-id="3f15a-116">Use the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message to publish an individual product family, product, or bundle record.</span><span class="sxs-lookup"><span data-stu-id="3f15a-116">Use the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message to publish an individual product family, product, or bundle record.</span></span> <span data-ttu-id="3f15a-117">In this case, the state of the target record changes from **Draft** to **Active**.</span><span class="sxs-lookup"><span data-stu-id="3f15a-117">In this case, the state of the target record changes from **Draft** to **Active**.</span></span> <span data-ttu-id="3f15a-118">A child product or bundle record under a product family record can be published only if the parent product family record is published (in the **Active** state).</span><span class="sxs-lookup"><span data-stu-id="3f15a-118">A child product or bundle record under a product family record can be published only if the parent product family record is published (in the **Active** state).</span></span> <span data-ttu-id="3f15a-119">You cannot publish multiple product family, product, or bundle records at once.</span><span class="sxs-lookup"><span data-stu-id="3f15a-119">You cannot publish multiple product family, product, or bundle records at once.</span></span>  
  
 <span data-ttu-id="3f15a-120">Use the <xref:Microsoft.Crm.Sdk.Messages.PublishProductHierarchyRequest> message to publish a product family hierarchy including the child products and bundles.</span><span class="sxs-lookup"><span data-stu-id="3f15a-120">Use the <xref:Microsoft.Crm.Sdk.Messages.PublishProductHierarchyRequest> message to publish a product family hierarchy including the child products and bundles.</span></span> <span data-ttu-id="3f15a-121">You can use this message only with a product family record.</span><span class="sxs-lookup"><span data-stu-id="3f15a-121">You can use this message only with a product family record.</span></span> <span data-ttu-id="3f15a-122">The state of the target product family record and all the child product or bundle records changes from **Draft** to **Active**.</span><span class="sxs-lookup"><span data-stu-id="3f15a-122">The state of the target product family record and all the child product or bundle records changes from **Draft** to **Active**.</span></span>  
  
 <span data-ttu-id="3f15a-123">The following code sample demonstrates how you can publish an individual product family, product, or bundle record.</span><span class="sxs-lookup"><span data-stu-id="3f15a-123">The following code sample demonstrates how you can publish an individual product family, product, or bundle record.</span></span>  
  
```csharp  
SetStateRequest publishRequest = new SetStateRequest  
{  
   EntityMoniker = new EntityReference(Product.EntityLogicalName, _productId),  
   State = new OptionSetValue((int)ProductState.Active),  
   Status = new OptionSetValue(1)  
};              
_serviceProxy.Execute(publishRequest);  
```  
  
 <span data-ttu-id="3f15a-124">The following code sample demonstrates how you can publish a product family, including its child records.</span><span class="sxs-lookup"><span data-stu-id="3f15a-124">The following code sample demonstrates how you can publish a product family, including its child records.</span></span>  
  
```csharp  
PublishProductHierarchyRequest publishRequest = new PublishProductHierarchyRequest  
{  
   Target = new EntityReference(Product.EntityLogicalName, _productFamilyId)  
};  
_serviceProxy.Execute(publishRequest);  
  
```  
  
 <span data-ttu-id="3f15a-125">For the complete sample code, see [Sample: Create and publish products](sample-create-publish-products.md).</span><span class="sxs-lookup"><span data-stu-id="3f15a-125">For the complete sample code, see [Sample: Create and publish products](sample-create-publish-products.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="3f15a-126">For the product or bundle records that aren’t associated with a product family, you must publish them individually after creating or editing them to make them available to your sales agents.</span><span class="sxs-lookup"><span data-stu-id="3f15a-126">For the product or bundle records that aren’t associated with a product family, you must publish them individually after creating or editing them to make them available to your sales agents.</span></span> <span data-ttu-id="3f15a-127">For product or bundle records associated with a product family, use the <xref:Microsoft.Crm.Sdk.Messages.PublishProductHierarchyRequest> message on the parent product family record to publish multiple child product or bundle records, along with the parent product family record, at once.</span><span class="sxs-lookup"><span data-stu-id="3f15a-127">For product or bundle records associated with a product family, use the <xref:Microsoft.Crm.Sdk.Messages.PublishProductHierarchyRequest> message on the parent product family record to publish multiple child product or bundle records, along with the parent product family record, at once.</span></span>  
> 
>  <span data-ttu-id="3f15a-128">Also, for products that aren’t associated with a product family, you can create them directly in an **Active** state by setting the **Organization.CreateProductsWithoutParentInActiveState** attribute to `1` (true).</span><span class="sxs-lookup"><span data-stu-id="3f15a-128">Also, for products that aren’t associated with a product family, you can create them directly in an **Active** state by setting the **Organization.CreateProductsWithoutParentInActiveState** attribute to `1` (true).</span></span> <span data-ttu-id="3f15a-129">Alternately, use the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify whether products not associated with product families are created in an active state.</span><span class="sxs-lookup"><span data-stu-id="3f15a-129">Alternately, use the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify whether products not associated with product families are created in an active state.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="3f15a-130">[Configure product catalog information](http://go.microsoft.com/fwlink/p/?LinkId=512492)</span><span class="sxs-lookup"><span data-stu-id="3f15a-130">[Configure product catalog information](http://go.microsoft.com/fwlink/p/?LinkId=512492)</span></span>  
  
<a name="Revise"></a>   
## <a name="revise-a-product-family-product-or-bundle"></a><span data-ttu-id="3f15a-131">Revise a product family, product, or bundle</span><span class="sxs-lookup"><span data-stu-id="3f15a-131">Revise a product family, product, or bundle</span></span>  
 <span data-ttu-id="3f15a-132">Use the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message to revise a product family, product, or bundle record.</span><span class="sxs-lookup"><span data-stu-id="3f15a-132">Use the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message to revise a product family, product, or bundle record.</span></span>  
  
- <span data-ttu-id="3f15a-133">When invoked for a product family record, it revises the product family and its child records.</span><span class="sxs-lookup"><span data-stu-id="3f15a-133">When invoked for a product family record, it revises the product family and its child records.</span></span>  
  
- <span data-ttu-id="3f15a-134">When invoked for a product or a bundle record, it revises the individual record only.</span><span class="sxs-lookup"><span data-stu-id="3f15a-134">When invoked for a product or a bundle record, it revises the individual record only.</span></span>  
  
  <span data-ttu-id="3f15a-135">The state of the target record changes from **Active** to **Under Revision**.</span><span class="sxs-lookup"><span data-stu-id="3f15a-135">The state of the target record changes from **Active** to **Under Revision**.</span></span>  
  
  <span data-ttu-id="3f15a-136">After the product properties (attributes) are updated, the target record must to be published for the changes to reflect.</span><span class="sxs-lookup"><span data-stu-id="3f15a-136">After the product properties (attributes) are updated, the target record must to be published for the changes to reflect.</span></span> <span data-ttu-id="3f15a-137">On publishing, the state of the target record changes from **Under Revision** to **Active**.</span><span class="sxs-lookup"><span data-stu-id="3f15a-137">On publishing, the state of the target record changes from **Under Revision** to **Active**.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3f15a-138">When you revise a product and change the properties, [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] internally creates a new version of the product and copies the product details from the existing product to the newer version.</span><span class="sxs-lookup"><span data-stu-id="3f15a-138">When you revise a product and change the properties, [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] internally creates a new version of the product and copies the product details from the existing product to the newer version.</span></span> <span data-ttu-id="3f15a-139">Phiên bản sản phẩm mới có tất cả các chi tiết bao gồm các danh sách giá cả, sản phẩm mối quan hệ, và tài sản.</span><span class="sxs-lookup"><span data-stu-id="3f15a-139">The new product version has all the details including price lists, product relationships, and properties.</span></span> <span data-ttu-id="3f15a-140">The opportunities created with the older version of the product can continue to refer to the older version of the product.</span><span class="sxs-lookup"><span data-stu-id="3f15a-140">The opportunities created with the older version of the product can continue to refer to the older version of the product.</span></span> <span data-ttu-id="3f15a-141">The opportunities that are created after the product is revised or retired will refer to the current (newer) product version.</span><span class="sxs-lookup"><span data-stu-id="3f15a-141">The opportunities that are created after the product is revised or retired will refer to the current (newer) product version.</span></span>  
  
<a name="Revert"></a>   
## <a name="revert-a-product-family-product-or-bundle"></a><span data-ttu-id="3f15a-142">Revert a product family, product, or bundle</span><span class="sxs-lookup"><span data-stu-id="3f15a-142">Revert a product family, product, or bundle</span></span>  
 <span data-ttu-id="3f15a-143">Use the <xref:Microsoft.Crm.Sdk.Messages.RevertProductRequest> message to revert a product family, product, or bundle record to its last **Active** state.</span><span class="sxs-lookup"><span data-stu-id="3f15a-143">Use the <xref:Microsoft.Crm.Sdk.Messages.RevertProductRequest> message to revert a product family, product, or bundle record to its last **Active** state.</span></span> <span data-ttu-id="3f15a-144">All the product property (attribute) changes done to the record since it was last published (**Active** state) will be lost.</span><span class="sxs-lookup"><span data-stu-id="3f15a-144">All the product property (attribute) changes done to the record since it was last published (**Active** state) will be lost.</span></span>  
  
- <span data-ttu-id="3f15a-145">When invoked for a product family record, it reverts the product family and its child records to their last **Active** state, and all the changes done to the product properties of the records since they were last published will be lost.</span><span class="sxs-lookup"><span data-stu-id="3f15a-145">When invoked for a product family record, it reverts the product family and its child records to their last **Active** state, and all the changes done to the product properties of the records since they were last published will be lost.</span></span>  
  
- <span data-ttu-id="3f15a-146">When invoked for a product or a bundle record, it reverts the individual product or bundle record to its last **Active** state, and all the changes done to the product properties of the record since it was last published will be lost.</span><span class="sxs-lookup"><span data-stu-id="3f15a-146">When invoked for a product or a bundle record, it reverts the individual product or bundle record to its last **Active** state, and all the changes done to the product properties of the record since it was last published will be lost.</span></span>  
  
  <span data-ttu-id="3f15a-147">The state of the target record changes from **Under Revision** to **Active**.</span><span class="sxs-lookup"><span data-stu-id="3f15a-147">The state of the target record changes from **Under Revision** to **Active**.</span></span>  
  
  <span data-ttu-id="3f15a-148">The following code sample demonstrates how to revert a product record.</span><span class="sxs-lookup"><span data-stu-id="3f15a-148">The following code sample demonstrates how to revert a product record.</span></span>  
  
```csharp  
RevertProductRequest revertReq = new RevertProductRequest  
{  
   Target = new EntityReference(Product.EntityLogicalName, _productId)  
};  
RevertProductResponse reverted = (RevertProductResponse)_serviceProxy.Execute(revertReq);  
```  
  
<a name="Retire"></a>   
## <a name="retire-a-product-family-product-or-bundle"></a><span data-ttu-id="3f15a-149">Retire a product family, product, or bundle</span><span class="sxs-lookup"><span data-stu-id="3f15a-149">Retire a product family, product, or bundle</span></span>  
 <span data-ttu-id="3f15a-150">Use the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message to retire a product family, product, or bundle record.</span><span class="sxs-lookup"><span data-stu-id="3f15a-150">Use the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message to retire a product family, product, or bundle record.</span></span>  
  
- <span data-ttu-id="3f15a-151">When invoked for a product family record, it retires the entire product family hierarchy.</span><span class="sxs-lookup"><span data-stu-id="3f15a-151">When invoked for a product family record, it retires the entire product family hierarchy.</span></span>  
  
- <span data-ttu-id="3f15a-152">When invoked for a product or a bundle record, it retires the individual record only.</span><span class="sxs-lookup"><span data-stu-id="3f15a-152">When invoked for a product or a bundle record, it retires the individual record only.</span></span>  
  
  <span data-ttu-id="3f15a-153">The state of the target record changes to **Retired**.</span><span class="sxs-lookup"><span data-stu-id="3f15a-153">The state of the target record changes to **Retired**.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3f15a-154">You can’t retire a product that is part of a published (**Active**) bundle.</span><span class="sxs-lookup"><span data-stu-id="3f15a-154">You can’t retire a product that is part of a published (**Active**) bundle.</span></span> <span data-ttu-id="3f15a-155">Also, you can’t add a retired product to a bundle or can’t add a product to a retired bundle.</span><span class="sxs-lookup"><span data-stu-id="3f15a-155">Also, you can’t add a retired product to a bundle or can’t add a product to a retired bundle.</span></span>  
  
<a name="Activate"></a>   
## <a name="activate-a-product-or-kit-record"></a><span data-ttu-id="3f15a-156">Activate a product or kit record</span><span class="sxs-lookup"><span data-stu-id="3f15a-156">Activate a product or kit record</span></span>  
 <span data-ttu-id="3f15a-157">Use the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message to activate only the following types of record:</span><span class="sxs-lookup"><span data-stu-id="3f15a-157">Use the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message to activate only the following types of record:</span></span>  
  
- <span data-ttu-id="3f15a-158">A retired product record that does not have a parent record.</span><span class="sxs-lookup"><span data-stu-id="3f15a-158">A retired product record that does not have a parent record.</span></span>  
  
- <span data-ttu-id="3f15a-159">A retired kit record.</span><span class="sxs-lookup"><span data-stu-id="3f15a-159">A retired kit record.</span></span>  
  
  <span data-ttu-id="3f15a-160">The state of the target record changes from **Retired** to **Active**.</span><span class="sxs-lookup"><span data-stu-id="3f15a-160">The state of the target record changes from **Retired** to **Active**.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3f15a-161">You can’t activate a retired product family or a retired bundle record.</span><span class="sxs-lookup"><span data-stu-id="3f15a-161">You can’t activate a retired product family or a retired bundle record.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3f15a-162">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3f15a-162">See also</span></span>  
 <span data-ttu-id="3f15a-163">[Manage Product Pricing](product-pricing-methods.md) </span><span class="sxs-lookup"><span data-stu-id="3f15a-163">[Manage Product Pricing](product-pricing-methods.md) </span></span>  
 <span data-ttu-id="3f15a-164">[Create and manage product families, products and bundles](create-manage-product-families-products-bundles-product-properties.md) </span><span class="sxs-lookup"><span data-stu-id="3f15a-164">[Create and manage product families, products and bundles](create-manage-product-families-products-bundles-product-properties.md) </span></span>  
 [<span data-ttu-id="3f15a-165">Product catalog entities</span><span class="sxs-lookup"><span data-stu-id="3f15a-165">Product catalog entities</span></span>](product-catalog-entities.md)
