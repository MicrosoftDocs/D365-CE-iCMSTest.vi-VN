---
title: Create and manage product families, products, bundles, and product properties (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Supports hierarchical organization of the product catalog through the creation and management products and bundles under a product family, defining related products, and adding properties (attributes) to the parent product family.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0f6c4255-094e-455e-bf7b-b832b981f58b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6c49ad129433f23be07046bd7bce4b7a28693ef9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387112"
---
# <a name="create-and-manage-product-families-products-bundles-and-product-properties"></a><span data-ttu-id="dda36-103">Create and manage product families, products, bundles, and product properties</span><span class="sxs-lookup"><span data-stu-id="dda36-103">Create and manage product families, products, bundles, and product properties</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="dda36-104">Define your product catalog by organizing your products in a hierarchical structure by creating products and bundles under a product family, defining related products, and adding properties (attributes) to the parent product family so that all the child products and bundles under a product family automatically inherit the properties.</span><span class="sxs-lookup"><span data-stu-id="dda36-104">Define your product catalog by organizing your products in a hierarchical structure by creating products and bundles under a product family, defining related products, and adding properties (attributes) to the parent product family so that all the child products and bundles under a product family automatically inherit the properties.</span></span>  
  
 <span data-ttu-id="dda36-105">By default, when you create a product family, product, or bundle record, they are in the **Draft** state.</span><span class="sxs-lookup"><span data-stu-id="dda36-105">By default, when you create a product family, product, or bundle record, they are in the **Draft** state.</span></span> <span data-ttu-id="dda36-106">After you have created a product, defined related products, and configured attributes for the parent product family record, you must publish the product family, product, or bundle record for them to become available in the system to your sales agents for selling.</span><span class="sxs-lookup"><span data-stu-id="dda36-106">After you have created a product, defined related products, and configured attributes for the parent product family record, you must publish the product family, product, or bundle record for them to become available in the system to your sales agents for selling.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="dda36-107">[Publish a product family, product, or bundle](publish-revise-revert-retire-activate-products.md#Publish)</span><span class="sxs-lookup"><span data-stu-id="dda36-107">[Publish a product family, product, or bundle](publish-revise-revert-retire-activate-products.md#Publish)</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="dda36-108">For products not associated with a product family, that is, products that don’t have a parent product family record assigned to them, you can create them directly in an **Active** state by setting the **Organization.CreateProductsWithoutParentInActiveState** attribute to `1` (true).</span><span class="sxs-lookup"><span data-stu-id="dda36-108">For products not associated with a product family, that is, products that don’t have a parent product family record assigned to them, you can create them directly in an **Active** state by setting the **Organization.CreateProductsWithoutParentInActiveState** attribute to `1` (true).</span></span> <span data-ttu-id="dda36-109">By default, this attribute is set to `0` (false) for a fresh installation of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps and to `1` (true) if you’re upgrading from a previous version of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to ensure compatibility for your applications working with the previous version of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps where the product records were created in an **Active** state.</span><span class="sxs-lookup"><span data-stu-id="dda36-109">By default, this attribute is set to `0` (false) for a fresh installation of [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps and to `1` (true) if you’re upgrading from a previous version of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to ensure compatibility for your applications working with the previous version of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps where the product records were created in an **Active** state.</span></span>  
> 
>  <span data-ttu-id="dda36-110">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify whether products are created in an **Active** state.</span><span class="sxs-lookup"><span data-stu-id="dda36-110">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)] to specify whether products are created in an **Active** state.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="dda36-111">[Manage product catalog configuration](https://technet.microsoft.com/library/dn832125.aspx)</span><span class="sxs-lookup"><span data-stu-id="dda36-111">[Manage product catalog configuration](https://technet.microsoft.com/library/dn832125.aspx)</span></span>  
  
<a name="Define"></a>   
## <a name="define-products-product-families-and-bundles"></a><span data-ttu-id="dda36-112">Define products, product families, and bundles</span><span class="sxs-lookup"><span data-stu-id="dda36-112">Define products, product families, and bundles</span></span>  
 <span data-ttu-id="dda36-113">Use the `Product.ProductStructure` attribute to define whether an item is a product family, product, or bundle.</span><span class="sxs-lookup"><span data-stu-id="dda36-113">Use the `Product.ProductStructure` attribute to define whether an item is a product family, product, or bundle.</span></span> <span data-ttu-id="dda36-114">Set the value of this attribute to:</span><span class="sxs-lookup"><span data-stu-id="dda36-114">Set the value of this attribute to:</span></span>  
  
- <span data-ttu-id="dda36-115">**1** to create a product</span><span class="sxs-lookup"><span data-stu-id="dda36-115">**1** to create a product</span></span>  
  
- <span data-ttu-id="dda36-116">**2** to create a product family</span><span class="sxs-lookup"><span data-stu-id="dda36-116">**2** to create a product family</span></span>  
  
- <span data-ttu-id="dda36-117">**3** to create a bundle</span><span class="sxs-lookup"><span data-stu-id="dda36-117">**3** to create a bundle</span></span>  
  
  <span data-ttu-id="dda36-118">Here are some important points to consider while defining product families, products, and bundles:</span><span class="sxs-lookup"><span data-stu-id="dda36-118">Here are some important points to consider while defining product families, products, and bundles:</span></span>  
  
- <span data-ttu-id="dda36-119">A product family record can contain multiple child product family, product, and bundle instances in a hierarchical structure.</span><span class="sxs-lookup"><span data-stu-id="dda36-119">A product family record can contain multiple child product family, product, and bundle instances in a hierarchical structure.</span></span> <span data-ttu-id="dda36-120">For a child product family, child product, or child bundle instance, you define the parent product family instance using the `Product.ParentProductId` attribute.</span><span class="sxs-lookup"><span data-stu-id="dda36-120">For a child product family, child product, or child bundle instance, you define the parent product family instance using the `Product.ParentProductId` attribute.</span></span> <span data-ttu-id="dda36-121">You can’t change the parent record once you’ve set it.</span><span class="sxs-lookup"><span data-stu-id="dda36-121">You can’t change the parent record once you’ve set it.</span></span>  
  
- <span data-ttu-id="dda36-122">A product or bundle can’t be set as a parent, which implies that a product or bundle record can’t have child records.</span><span class="sxs-lookup"><span data-stu-id="dda36-122">A product or bundle can’t be set as a parent, which implies that a product or bundle record can’t have child records.</span></span>  
  
- <span data-ttu-id="dda36-123">A product family, product, or bundle instance can be part of only one product family instance.</span><span class="sxs-lookup"><span data-stu-id="dda36-123">A product family, product, or bundle instance can be part of only one product family instance.</span></span>  
  
- <span data-ttu-id="dda36-124">There is no limit on the nesting level for a product family.</span><span class="sxs-lookup"><span data-stu-id="dda36-124">There is no limit on the nesting level for a product family.</span></span>  
  
- <span data-ttu-id="dda36-125">The `Product.ValidFromDate` and `Product.ValidToDate` attributes don’t have any out-of-box business logic associated with them, except that there is a check to ensure that the date in `Product.ValidToDate` should be later than or equal to the date in `Product.ValidFromDate`.</span><span class="sxs-lookup"><span data-stu-id="dda36-125">The `Product.ValidFromDate` and `Product.ValidToDate` attributes don’t have any out-of-box business logic associated with them, except that there is a check to ensure that the date in `Product.ValidToDate` should be later than or equal to the date in `Product.ValidFromDate`.</span></span> <span data-ttu-id="dda36-126">If required, you can implement your own business logic based on these attributes.</span><span class="sxs-lookup"><span data-stu-id="dda36-126">If required, you can implement your own business logic based on these attributes.</span></span> <span data-ttu-id="dda36-127">For example, you could run a scheduled job to automatically retire last season’s products by using the date value in the `Product.ValidToDate` attribute.</span><span class="sxs-lookup"><span data-stu-id="dda36-127">For example, you could run a scheduled job to automatically retire last season’s products by using the date value in the `Product.ValidToDate` attribute.</span></span>  
  
  <span data-ttu-id="dda36-128">The following code sample demonstrates how you can create a product family and a child product record.</span><span class="sxs-lookup"><span data-stu-id="dda36-128">The following code sample demonstrates how you can create a product family and a child product record.</span></span>  
  
```csharp  
// Create a product family  
Product newProductFamily = new Product  
{  
   Name = "Example Product Family",  
   ProductNumber = "PF001",  
   ProductStructure = new OptionSetValue(2)  
};  
_productFamilyId = _serviceProxy.Create(newProductFamily);  
Console.WriteLine("\nCreated {0}", newProductFamily.Name);  
  
// Create a product record under the product family  
Product newProduct1 = new Product  
{  
   Name = "Example Product 1",  
   ProductNumber = "P001",  
   ProductStructure = new OptionSetValue(1),  
   ParentProductId = new EntityReference(Product.EntityLogicalName, _productFamilyId),  
   QuantityDecimal = 2,  
   DefaultUoMScheduleId = new EntityReference(UoMSchedule.EntityLogicalName, _unitGroupId),  
   DefaultUoMId = new EntityReference(UoM.EntityLogicalName, _unit.Id)  
};  
_product1Id = _serviceProxy.Create(newProduct1);  
Console.WriteLine("Created {0} under the product family", newProduct1.Name);  
```  
  
<a name="Properties"></a>   
## <a name="define-product-properties"></a><span data-ttu-id="dda36-129">Define product properties</span><span class="sxs-lookup"><span data-stu-id="dda36-129">Define product properties</span></span>  
 <span data-ttu-id="dda36-130">Product properties help you define the characteristics of  product such as its size, color, or component.</span><span class="sxs-lookup"><span data-stu-id="dda36-130">Product properties help you define the characteristics of  product such as its size, color, or component.</span></span> <span data-ttu-id="dda36-131">A product property is defined using the `DynamicProperty` entity.</span><span class="sxs-lookup"><span data-stu-id="dda36-131">A product property is defined using the `DynamicProperty` entity.</span></span> <span data-ttu-id="dda36-132">While defining a product property, you can only associate it to a product family record in a `Draft` state, and not to a product or bundle record.</span><span class="sxs-lookup"><span data-stu-id="dda36-132">While defining a product property, you can only associate it to a product family record in a `Draft` state, and not to a product or bundle record.</span></span> <span data-ttu-id="dda36-133">The maximum number of product properties that can be associated to a draft product family record is determined by the following organization setting: **Organization.MaximumDynamicPropertiesAllowed**.</span><span class="sxs-lookup"><span data-stu-id="dda36-133">The maximum number of product properties that can be associated to a draft product family record is determined by the following organization setting: **Organization.MaximumDynamicPropertiesAllowed**.</span></span> <span data-ttu-id="dda36-134">The number comes into effect when you publish a child product record or bundle under a product family that the properties are attached to, and not at the time when you attach the properties to a *draft* product family record.</span><span class="sxs-lookup"><span data-stu-id="dda36-134">The number comes into effect when you publish a child product record or bundle under a product family that the properties are attached to, and not at the time when you attach the properties to a *draft* product family record.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="dda36-135">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps or [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] to configure the maximum number of product properties.</span><span class="sxs-lookup"><span data-stu-id="dda36-135">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps or [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] to configure the maximum number of product properties.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="dda36-136">[Manage product catalog configuration](https://technet.microsoft.com/library/dn832125.aspx).</span><span class="sxs-lookup"><span data-stu-id="dda36-136">[Manage product catalog configuration](https://technet.microsoft.com/library/dn832125.aspx).</span></span>  
  
 <span data-ttu-id="dda36-137">While creating a product property, you specify its name, the product family record in `Draft` state with which it is associated, attributes of the property such as whether its hidden, required, or read-only, and the data type of the property.</span><span class="sxs-lookup"><span data-stu-id="dda36-137">While creating a product property, you specify its name, the product family record in `Draft` state with which it is associated, attributes of the property such as whether its hidden, required, or read-only, and the data type of the property.</span></span> <span data-ttu-id="dda36-138">A product property can be of one of the following data types:</span><span class="sxs-lookup"><span data-stu-id="dda36-138">A product property can be of one of the following data types:</span></span>  
  
|<span data-ttu-id="dda36-139">Value</span><span class="sxs-lookup"><span data-stu-id="dda36-139">Value</span></span>|<span data-ttu-id="dda36-140">Loại Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="dda36-140">Data Type</span></span>|  
|-----------|---------------|  
|<span data-ttu-id="dda36-141">0</span><span class="sxs-lookup"><span data-stu-id="dda36-141">0</span></span>|<span data-ttu-id="dda36-142">Bộ Tùy chọn</span><span class="sxs-lookup"><span data-stu-id="dda36-142">Option Set</span></span>|  
|<span data-ttu-id="dda36-143">1</span><span class="sxs-lookup"><span data-stu-id="dda36-143">1</span></span>|<span data-ttu-id="dda36-144">Thập phân</span><span class="sxs-lookup"><span data-stu-id="dda36-144">Decimal</span></span>|  
|<span data-ttu-id="dda36-145">2</span><span class="sxs-lookup"><span data-stu-id="dda36-145">2</span></span>|<span data-ttu-id="dda36-146">Số thực Dấu phẩy Động</span><span class="sxs-lookup"><span data-stu-id="dda36-146">Floating Point Number</span></span>|  
|<span data-ttu-id="dda36-147">3</span><span class="sxs-lookup"><span data-stu-id="dda36-147">3</span></span>|<span data-ttu-id="dda36-148">Một dòng Văn bản</span><span class="sxs-lookup"><span data-stu-id="dda36-148">Single Line of Text</span></span>|  
|<span data-ttu-id="dda36-149">4</span><span class="sxs-lookup"><span data-stu-id="dda36-149">4</span></span>|<span data-ttu-id="dda36-150">Số Nguyên</span><span class="sxs-lookup"><span data-stu-id="dda36-150">Whole Number</span></span>|  
  
 <span data-ttu-id="dda36-151">You cannot change the data type of a product property after its created.</span><span class="sxs-lookup"><span data-stu-id="dda36-151">You cannot change the data type of a product property after its created.</span></span> <span data-ttu-id="dda36-152">When you create a product property, its created in the `Draft` state.</span><span class="sxs-lookup"><span data-stu-id="dda36-152">When you create a product property, its created in the `Draft` state.</span></span>  
  
 <span data-ttu-id="dda36-153">The following sample code demonstrates how you  can create a product property:</span><span class="sxs-lookup"><span data-stu-id="dda36-153">The following sample code demonstrates how you  can create a product property:</span></span>  
  
```csharp  
DynamicProperty newProperty = new DynamicProperty  
{  
    Name = "Example Property",  
    RegardingObjectId = new EntityReference(Product.EntityLogicalName,  
                                            _productFamilyId),  
    IsReadOnly = true,  
    IsRequired = true,  
    IsHidden = false,  
    DataType = new OptionSetValue(3), //Single line of text  
    DefaultValueString = "Default Value"  
};  
_productPropertyId = _serviceProxy.Create(newProperty);  
```  
  
 <span data-ttu-id="dda36-154">For the complete sample, see [Sample: Create and publish products](sample-create-publish-products.md)</span><span class="sxs-lookup"><span data-stu-id="dda36-154">For the complete sample, see [Sample: Create and publish products](sample-create-publish-products.md)</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="dda36-155">When you create a product property of `Option Set` data type, you must define individual options for the product property by creating  `DynamicPropertyOptionSetItem` entity records.</span><span class="sxs-lookup"><span data-stu-id="dda36-155">When you create a product property of `Option Set` data type, you must define individual options for the product property by creating  `DynamicPropertyOptionSetItem` entity records.</span></span> <span data-ttu-id="dda36-156">Each entity record stores information about the individual option where the  `DynamicPropertyOptionSetItem.DynamicPropertyOptionName` and `DynamicPropertyOptionSetItem.DynamicPropertyOptionValue` attributes define the option name and value respectively, and you can associate individual option records to the parent product property instance using the `DynamicPropertyOptionSetItem.DynamicPropertyId` attribute.</span><span class="sxs-lookup"><span data-stu-id="dda36-156">Each entity record stores information about the individual option where the  `DynamicPropertyOptionSetItem.DynamicPropertyOptionName` and `DynamicPropertyOptionSetItem.DynamicPropertyOptionValue` attributes define the option name and value respectively, and you can associate individual option records to the parent product property instance using the `DynamicPropertyOptionSetItem.DynamicPropertyId` attribute.</span></span>  
  
 <span data-ttu-id="dda36-157">For information about creating and managing product properties using the web client, see [Use properties to describe a product](http://go.microsoft.com/fwlink/p/?LinkId=512709)</span><span class="sxs-lookup"><span data-stu-id="dda36-157">For information about creating and managing product properties using the web client, see [Use properties to describe a product](http://go.microsoft.com/fwlink/p/?LinkId=512709)</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="dda36-158">The way you define a product property determines how it can be used by the sales agent at run time, that is, while adding an associated product to an opportunity, quote, order, or invoice.</span><span class="sxs-lookup"><span data-stu-id="dda36-158">The way you define a product property determines how it can be used by the sales agent at run time, that is, while adding an associated product to an opportunity, quote, order, or invoice.</span></span> <span data-ttu-id="dda36-159">An *updatable* product property’s value can be changed at run time, whereas the value of a *read-only* product property can’t be.</span><span class="sxs-lookup"><span data-stu-id="dda36-159">An *updatable* product property’s value can be changed at run time, whereas the value of a *read-only* product property can’t be.</span></span> <span data-ttu-id="dda36-160">For a product property set as *required*, a value for the property must be specified at the run time.</span><span class="sxs-lookup"><span data-stu-id="dda36-160">For a product property set as *required*, a value for the property must be specified at the run time.</span></span> <span data-ttu-id="dda36-161">Otherwise, the property is displayed as unresolved.</span><span class="sxs-lookup"><span data-stu-id="dda36-161">Otherwise, the property is displayed as unresolved.</span></span> <span data-ttu-id="dda36-162">A *hidden* property won’t be displayed to sales agents at the run time.</span><span class="sxs-lookup"><span data-stu-id="dda36-162">A *hidden* property won’t be displayed to sales agents at the run time.</span></span>  
> 
>  <span data-ttu-id="dda36-163">Also, product properties don’t affect the pricing of a product.</span><span class="sxs-lookup"><span data-stu-id="dda36-163">Also, product properties don’t affect the pricing of a product.</span></span> <span data-ttu-id="dda36-164">This implies that the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps pricing engine doesn’t support changing the price of a product based on a change in the product property values.</span><span class="sxs-lookup"><span data-stu-id="dda36-164">This implies that the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps pricing engine doesn’t support changing the price of a product based on a change in the product property values.</span></span>  
  
<a name="ChangeProductProperties"></a>   
### <a name="change-product-properties"></a><span data-ttu-id="dda36-165">Change product properties</span><span class="sxs-lookup"><span data-stu-id="dda36-165">Change product properties</span></span>  
 <span data-ttu-id="dda36-166">It's important to know the various states  of the product property in order to understand how and when it can be changed.</span><span class="sxs-lookup"><span data-stu-id="dda36-166">It's important to know the various states  of the product property in order to understand how and when it can be changed.</span></span> <span data-ttu-id="dda36-167">A product property can be in **Draft**, **Active**, or **Retired** state.</span><span class="sxs-lookup"><span data-stu-id="dda36-167">A product property can be in **Draft**, **Active**, or **Retired** state.</span></span> <span data-ttu-id="dda36-168">When a product is created, its in the **Draft** state, and changes to the **Active** state once the product family record with which it is associated is published.</span><span class="sxs-lookup"><span data-stu-id="dda36-168">When a product is created, its in the **Draft** state, and changes to the **Active** state once the product family record with which it is associated is published.</span></span> <span data-ttu-id="dda36-169">When the associated product family record is retired, the state of the product property also changes to `Retired`.</span><span class="sxs-lookup"><span data-stu-id="dda36-169">When the associated product family record is retired, the state of the product property also changes to `Retired`.</span></span>  
  
 <span data-ttu-id="dda36-170">A product property can be changes at two levels: *first* at the product family level to which the product property is associated with; *second* at the child product family, product, or bundle level where the product property is inherited.</span><span class="sxs-lookup"><span data-stu-id="dda36-170">A product property can be changes at two levels: *first* at the product family level to which the product property is associated with; *second* at the child product family, product, or bundle level where the product property is inherited.</span></span>  
  
 <span data-ttu-id="dda36-171">**Changing product property for the product family that its associate with**</span><span class="sxs-lookup"><span data-stu-id="dda36-171">**Changing product property for the product family that its associate with**</span></span>  
  
 <span data-ttu-id="dda36-172">For a `Draft`  product family record, you can change a product property associated to it.</span><span class="sxs-lookup"><span data-stu-id="dda36-172">For a `Draft`  product family record, you can change a product property associated to it.</span></span> <span data-ttu-id="dda36-173">Once you publish the product family record (changes to `Active` state), you cannot change the product property until you revise the product family record.</span><span class="sxs-lookup"><span data-stu-id="dda36-173">Once you publish the product family record (changes to `Active` state), you cannot change the product property until you revise the product family record.</span></span> <span data-ttu-id="dda36-174">After revising the product family record (changes to `Under Revision` state), and then *overwrite* the published (active) version of the property to make changes.</span><span class="sxs-lookup"><span data-stu-id="dda36-174">After revising the product family record (changes to `Under Revision` state), and then *overwrite* the published (active) version of the property to make changes.</span></span> <span data-ttu-id="dda36-175">For information about product life cycle, see [Publish, revise, revert, retire, and activate products (product lifecycle)](publish-revise-revert-retire-activate-products.md)</span><span class="sxs-lookup"><span data-stu-id="dda36-175">For information about product life cycle, see [Publish, revise, revert, retire, and activate products (product lifecycle)](publish-revise-revert-retire-activate-products.md)</span></span>  
  
 <span data-ttu-id="dda36-176">**Changing inherited product property for the child product family, product, or bundle**</span><span class="sxs-lookup"><span data-stu-id="dda36-176">**Changing inherited product property for the child product family, product, or bundle**</span></span>  
  
 <span data-ttu-id="dda36-177">For a product property in the `Draft` state, the child product family, product, and bundle records can *override* the inherited property to define their own version of the property.</span><span class="sxs-lookup"><span data-stu-id="dda36-177">For a product property in the `Draft` state, the child product family, product, and bundle records can *override* the inherited property to define their own version of the property.</span></span> <span data-ttu-id="dda36-178">For example, override the inherited property to change its name or change attributes from hidden to visible, required to optional, or read-only to updatable.</span><span class="sxs-lookup"><span data-stu-id="dda36-178">For example, override the inherited property to change its name or change attributes from hidden to visible, required to optional, or read-only to updatable.</span></span> <span data-ttu-id="dda36-179">You cannot override or change the data type of the inherited property.</span><span class="sxs-lookup"><span data-stu-id="dda36-179">You cannot override or change the data type of the inherited property.</span></span>  
  
 <span data-ttu-id="dda36-180">**To override a product property**, you create an instance of the product property  and set the `BaseDynamicPropertyId` property to the GUID of the property you are overriding.</span><span class="sxs-lookup"><span data-stu-id="dda36-180">**To override a product property**, you create an instance of the product property  and set the `BaseDynamicPropertyId` property to the GUID of the property you are overriding.</span></span> <span data-ttu-id="dda36-181">Additionally, you also associate the new property instance to the child product family, product, or bundle record where its being overridden.</span><span class="sxs-lookup"><span data-stu-id="dda36-181">Additionally, you also associate the new property instance to the child product family, product, or bundle record where its being overridden.</span></span>  
  
 <span data-ttu-id="dda36-182">The following sample code demonstrates how you can override an existing product property record, say with GUID `_productPropertyId`, and associate the overridden property to the product record, say with GUID `_product1Id`.</span><span class="sxs-lookup"><span data-stu-id="dda36-182">The following sample code demonstrates how you can override an existing product property record, say with GUID `_productPropertyId`, and associate the overridden property to the product record, say with GUID `_product1Id`.</span></span> <span data-ttu-id="dda36-183">After this, you can update the attributes of the new property to specify your own values to complete the override.</span><span class="sxs-lookup"><span data-stu-id="dda36-183">After this, you can update the attributes of the new property to specify your own values to complete the override.</span></span>  
  
```csharp  
// Override a product property  
DynamicProperty newOverrideProperty = new DynamicProperty();  
newOverrideProperty.BaseDynamicPropertyId = new EntityReference(DynamicProperty.EntityLogicalName,  
                           _productPropertyId);  
newOverrideProperty.RegardingObjectId = new EntityReference(Product.EntityLogicalName, _product1Id);  
_productOverridenPropertyId = _serviceProxy.Create(newOverrideProperty);  
  
// Retrieve the attributes of the cloned property you want to update                      
ColumnSet columns = new ColumnSet();  
columns.AddColumns("name", "isreadonly", "isrequired");  
DynamicProperty retrievedOverridenProperty = (DynamicProperty)_serviceProxy.Retrieve(  
                                               DynamicProperty.EntityLogicalName, _productOverridenPropertyId,  
                                               columns);  
  
// Update the attributes  
retrievedOverridenProperty.Name = "Overridden Example Property";  
retrievedOverridenProperty.IsReadOnly = true;  
retrievedOverridenProperty.IsRequired = false;  
_serviceProxy.Update(retrievedOverridenProperty);  
```  
  
 <span data-ttu-id="dda36-184">For the complete sample, see [Sample: Create and publish products](sample-create-publish-products.md)</span><span class="sxs-lookup"><span data-stu-id="dda36-184">For the complete sample, see [Sample: Create and publish products](sample-create-publish-products.md)</span></span>  
  
 <span data-ttu-id="dda36-185">For a product property in the `Active` state, you can *overwrite* the inherited property for the child product family, product, or bundle record provided both the following clauses are true:</span><span class="sxs-lookup"><span data-stu-id="dda36-185">For a product property in the `Active` state, you can *overwrite* the inherited property for the child product family, product, or bundle record provided both the following clauses are true:</span></span>  
  
- <span data-ttu-id="dda36-186">The child product family, product, or bundle record is in the **Under Revision** state.</span><span class="sxs-lookup"><span data-stu-id="dda36-186">The child product family, product, or bundle record is in the **Under Revision** state.</span></span>  
  
- <span data-ttu-id="dda36-187">The inherited active product property is already overridden.</span><span class="sxs-lookup"><span data-stu-id="dda36-187">The inherited active product property is already overridden.</span></span>  
  
  <span data-ttu-id="dda36-188">**To overwrite a product property**, you create an instance of the product property  and set the `BaseDynamicPropertyId` property to the GUID of the already overridden property.</span><span class="sxs-lookup"><span data-stu-id="dda36-188">**To overwrite a product property**, you create an instance of the product property  and set the `BaseDynamicPropertyId` property to the GUID of the already overridden property.</span></span> <span data-ttu-id="dda36-189">Additionally, you also associate the new property instance with the product family, product, or bundle record that is in the `Under Revision` stage.</span><span class="sxs-lookup"><span data-stu-id="dda36-189">Additionally, you also associate the new property instance with the product family, product, or bundle record that is in the `Under Revision` stage.</span></span>  
  
  <span data-ttu-id="dda36-190">The following sample code demonstrates how you can overwrite a product property record in the active state that is already overridden, say with GUID `_productOverridenPropertyId`, and associate the new property to the product record in the `Under Revision` state, say with GUID `_product1Id`.</span><span class="sxs-lookup"><span data-stu-id="dda36-190">The following sample code demonstrates how you can overwrite a product property record in the active state that is already overridden, say with GUID `_productOverridenPropertyId`, and associate the new property to the product record in the `Under Revision` state, say with GUID `_product1Id`.</span></span> <span data-ttu-id="dda36-191">After this, you can update the attributes of the new property to specify your own values, and complete the overwrite.</span><span class="sxs-lookup"><span data-stu-id="dda36-191">After this, you can update the attributes of the new property to specify your own values, and complete the overwrite.</span></span>  
  
```csharp  
// Overwrite a product property  
DynamicProperty newOverwriteProperty = new DynamicProperty();  
newOverwriteProperty.BaseDynamicPropertyId = new EntityReference(DynamicProperty.EntityLogicalName,  
                           _productOverridenPropertyId);  
newOverwriteProperty.RegardingObjectId = new EntityReference(Product.EntityLogicalName,  
    _product1Id);  
_productOverwrittenPropertyId = _serviceProxy.Create(newOverwriteProperty);  
  
// Retrieve the attributes of the cloned property you want to update  
ColumnSet myCols = new ColumnSet();  
myCols.AddColumns("name", "isreadonly", "isrequired");  
DynamicProperty retrievedOverwrittenProperty = (DynamicProperty)_serviceProxy.Retrieve(  
                                                   DynamicProperty.EntityLogicalName, _productOverwrittenPropertyId,  
                                                   myCols);  
  
// Update the attributes of the cloned property to complete the overwrite   
retrievedOverwrittenProperty.Name = "Overwritten Example Property";  
retrievedOverwrittenProperty.IsReadOnly = true;  
retrievedOverridenProperty.IsRequired = false;  
_serviceProxy.Update(retrievedOverwrittenProperty);  
```  
  
 <span data-ttu-id="dda36-192">For the complete sample, see [Sample: Create and publish products](sample-create-publish-products.md)</span><span class="sxs-lookup"><span data-stu-id="dda36-192">For the complete sample, see [Sample: Create and publish products](sample-create-publish-products.md)</span></span>  
  
<a name="BundlesKits"></a>   
## <a name="bundles-and-kits"></a><span data-ttu-id="dda36-193">Bundles and kits</span><span class="sxs-lookup"><span data-stu-id="dda36-193">Bundles and kits</span></span>  
 <span data-ttu-id="dda36-194">A *bundle* is a feature introduced in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] to replace the older kit functionality.</span><span class="sxs-lookup"><span data-stu-id="dda36-194">A *bundle* is a feature introduced in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] to replace the older kit functionality.</span></span> <span data-ttu-id="dda36-195">Tương tự như một bộ công cụ, một gói là một tập hợp các sản phẩm được bán như là đơn vị duy nhất.</span><span class="sxs-lookup"><span data-stu-id="dda36-195">Similar to a kit, a bundle is a collection of products that is sold as single unit.</span></span> <span data-ttu-id="dda36-196">Product bundling is useful in grouping products in a way that customers get more benefit from the full line of products or to offer discounts on bundled products that enables you to group products and sell as a single unit.</span><span class="sxs-lookup"><span data-stu-id="dda36-196">Product bundling is useful in grouping products in a way that customers get more benefit from the full line of products or to offer discounts on bundled products that enables you to group products and sell as a single unit.</span></span>  
  
 <span data-ttu-id="dda36-197">Only products can be added to a bundle; you can’t add a product family, a bundle, or a kit record to a bundle.</span><span class="sxs-lookup"><span data-stu-id="dda36-197">Only products can be added to a bundle; you can’t add a product family, a bundle, or a kit record to a bundle.</span></span> <span data-ttu-id="dda36-198">You can add products to a bundle or a kit by creating a product association record using the `ProductAssociation` entity.</span><span class="sxs-lookup"><span data-stu-id="dda36-198">You can add products to a bundle or a kit by creating a product association record using the `ProductAssociation` entity.</span></span> <span data-ttu-id="dda36-199">The `ProductAssociation.ProductId` record specifies the bundle or kit that you want to add a product to and the `ProductAssociation.AssociatedProduct` specifies the product to be added.</span><span class="sxs-lookup"><span data-stu-id="dda36-199">The `ProductAssociation.ProductId` record specifies the bundle or kit that you want to add a product to and the `ProductAssociation.AssociatedProduct` specifies the product to be added.</span></span> <span data-ttu-id="dda36-200">The maximum number of products that can be added to a bundle is determined by the following organization setting:  `Organization.MaxProductsinBundle`.</span><span class="sxs-lookup"><span data-stu-id="dda36-200">The maximum number of products that can be added to a bundle is determined by the following organization setting:  `Organization.MaxProductsinBundle`.</span></span>  
  
 <span data-ttu-id="dda36-201">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps or [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] to specify the maximum number of products that can be added to a bundle.</span><span class="sxs-lookup"><span data-stu-id="dda36-201">You can also use the **Sales** tab in the system settings area in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps or [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)] to specify the maximum number of products that can be added to a bundle.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="dda36-202">[Manage product catalog configuration](https://technet.microsoft.com/library/dn832125.aspx)</span><span class="sxs-lookup"><span data-stu-id="dda36-202">[Manage product catalog configuration](https://technet.microsoft.com/library/dn832125.aspx)</span></span>  
  
 <span data-ttu-id="dda36-203">The following code sample demonstrates how you can add products to a bundle.</span><span class="sxs-lookup"><span data-stu-id="dda36-203">The following code sample demonstrates how you can add products to a bundle.</span></span>  
  
```csharp
// Add a product to a bundle  
ProductAssociation newAssociation1 = new ProductAssociation  
{  
   AssociatedProduct = new EntityReference(Product.EntityLogicalName, _product1Id),  
   ProductId = new EntityReference(Product.EntityLogicalName, _bundleId),  
   Quantity = new decimal(15),  
   ProductIsRequired = new OptionSetValue(0),  
   UoMId = new EntityReference(UoM.EntityLogicalName, unit.Id)  
};  
_product1AssociationId = _serviceProxy.Create(newAssociation1);                      
  
// Add another product to the bundle                      
ProductAssociation newAssociation2 = new ProductAssociation  
{  
   AssociatedProduct = new EntityReference(Product.EntityLogicalName, _product2Id),  
   ProductId = new EntityReference(Product.EntityLogicalName, _bundleId),  
   Quantity = new decimal(20),  
   ProductIsRequired = new OptionSetValue(1),  
   UoMId = new EntityReference(UoM.EntityLogicalName, unit.Id),                          
};  
_product2AssociationId = _serviceProxy.Create(newAssociation2);  
  
if ((_product1AssociationId != null) && (_product1AssociationId != null))  
Console.WriteLine("\nAdded both the products to the bundle");  
```  
  
 <span data-ttu-id="dda36-204">For the complete sample, see [Sample: Add products to a bundle](sample-add-products-bundle.md).</span><span class="sxs-lookup"><span data-stu-id="dda36-204">For the complete sample, see [Sample: Add products to a bundle](sample-add-products-bundle.md).</span></span>  
  
### <a name="differences-between-kits-and-bundles"></a><span data-ttu-id="dda36-205">Differences between kits and bundles</span><span class="sxs-lookup"><span data-stu-id="dda36-205">Differences between kits and bundles</span></span>  
 <span data-ttu-id="dda36-206">Both kits and bundles enable you to group products into a single unit, but here are some differences between the two.</span><span class="sxs-lookup"><span data-stu-id="dda36-206">Both kits and bundles enable you to group products into a single unit, but here are some differences between the two.</span></span>  
  
|<span data-ttu-id="dda36-207">Kits</span><span class="sxs-lookup"><span data-stu-id="dda36-207">Kits</span></span>|<span data-ttu-id="dda36-208">Bundles</span><span class="sxs-lookup"><span data-stu-id="dda36-208">Bundles</span></span>|  
|----------|-------------|  
|<span data-ttu-id="dda36-209">All the products in a kit are mandatory.</span><span class="sxs-lookup"><span data-stu-id="dda36-209">All the products in a kit are mandatory.</span></span>|<span data-ttu-id="dda36-210">Some products in a bundle can be optional.</span><span class="sxs-lookup"><span data-stu-id="dda36-210">Some products in a bundle can be optional.</span></span>|  
|<span data-ttu-id="dda36-211">Kits support nesting; you can add a kit to another kit.</span><span class="sxs-lookup"><span data-stu-id="dda36-211">Kits support nesting; you can add a kit to another kit.</span></span>|<span data-ttu-id="dda36-212">You can’t add a bundle to another bundle.</span><span class="sxs-lookup"><span data-stu-id="dda36-212">You can’t add a bundle to another bundle.</span></span> <span data-ttu-id="dda36-213">You can only add products to a bundle.</span><span class="sxs-lookup"><span data-stu-id="dda36-213">You can only add products to a bundle.</span></span>|  
|<span data-ttu-id="dda36-214">While adding a kit to an opportunity, quote, order, or invoice, you can only see the kit level details; you can’t see individual products in the kit.</span><span class="sxs-lookup"><span data-stu-id="dda36-214">While adding a kit to an opportunity, quote, order, or invoice, you can only see the kit level details; you can’t see individual products in the kit.</span></span>|<span data-ttu-id="dda36-215">While adding a bundle to opportunity, quote, order, or invoice, you can see the bundle level details as well as individual products in the bundle.</span><span class="sxs-lookup"><span data-stu-id="dda36-215">While adding a bundle to opportunity, quote, order, or invoice, you can see the bundle level details as well as individual products in the bundle.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="dda36-216">Kits are deprecated in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps; you should use bundles instead.</span><span class="sxs-lookup"><span data-stu-id="dda36-216">Kits are deprecated in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps; you should use bundles instead.</span></span>  
  
<a name="ProductRelationships"></a>   
## <a name="define-product-relationships-for-enhanced-suggestions-during-product-sale"></a><span data-ttu-id="dda36-217">Define product relationships for enhanced suggestions during product sale</span><span class="sxs-lookup"><span data-stu-id="dda36-217">Define product relationships for enhanced suggestions during product sale</span></span>  
 <span data-ttu-id="dda36-218">You can define related products for a product that are displayed as suggestions to your sales agents during opportunity or order management.</span><span class="sxs-lookup"><span data-stu-id="dda36-218">You can define related products for a product that are displayed as suggestions to your sales agents during opportunity or order management.</span></span> <span data-ttu-id="dda36-219">The product suggestions for a product enables your sales agents to recommend related products and bundles/kits to the customers, and increase product sales.</span><span class="sxs-lookup"><span data-stu-id="dda36-219">The product suggestions for a product enables your sales agents to recommend related products and bundles/kits to the customers, and increase product sales.</span></span> <span data-ttu-id="dda36-220">You can define the following relationships for a product: **accessory**, **cross-sell**, **substitute**, and **up-sell**.</span><span class="sxs-lookup"><span data-stu-id="dda36-220">You can define the following relationships for a product: **accessory**, **cross-sell**, **substitute**, and **up-sell**.</span></span> <span data-ttu-id="dda36-221">For example, Surface Pro can be added as an up-sell product for Surface RT so that when your sales agent is adding Surface RT to any opportunity, quote, order, or invoice, Surface Pro will be suggested as the up-sell option.</span><span class="sxs-lookup"><span data-stu-id="dda36-221">For example, Surface Pro can be added as an up-sell product for Surface RT so that when your sales agent is adding Surface RT to any opportunity, quote, order, or invoice, Surface Pro will be suggested as the up-sell option.</span></span>  
  
 <span data-ttu-id="dda36-222">Use the **ProductSubstitute.SalesRelationshipType** attribute to define product relationships.</span><span class="sxs-lookup"><span data-stu-id="dda36-222">Use the **ProductSubstitute.SalesRelationshipType** attribute to define product relationships.</span></span> <span data-ttu-id="dda36-223">Set the value of this attribute to:</span><span class="sxs-lookup"><span data-stu-id="dda36-223">Set the value of this attribute to:</span></span>  
  
- <span data-ttu-id="dda36-224">**0** for up-sell</span><span class="sxs-lookup"><span data-stu-id="dda36-224">**0** for up-sell</span></span>  
  
- <span data-ttu-id="dda36-225">**1** for cross-sell</span><span class="sxs-lookup"><span data-stu-id="dda36-225">**1** for cross-sell</span></span>  
  
- <span data-ttu-id="dda36-226">**2** for accessory</span><span class="sxs-lookup"><span data-stu-id="dda36-226">**2** for accessory</span></span>  
  
- <span data-ttu-id="dda36-227">**3** for substitute</span><span class="sxs-lookup"><span data-stu-id="dda36-227">**3** for substitute</span></span>  
  
  <span data-ttu-id="dda36-228">While defining product relationships, it’s important to define the direction of the relationship to prevent duplication of data.</span><span class="sxs-lookup"><span data-stu-id="dda36-228">While defining product relationships, it’s important to define the direction of the relationship to prevent duplication of data.</span></span> <span data-ttu-id="dda36-229">The supported directions the product relationships are:</span><span class="sxs-lookup"><span data-stu-id="dda36-229">The supported directions the product relationships are:</span></span>  
  
|<span data-ttu-id="dda36-230">Product relationship</span><span class="sxs-lookup"><span data-stu-id="dda36-230">Product relationship</span></span>|<span data-ttu-id="dda36-231">Hướng</span><span class="sxs-lookup"><span data-stu-id="dda36-231">Direction</span></span>|  
|--------------------------|---------------|  
|<span data-ttu-id="dda36-232">Accessory</span><span class="sxs-lookup"><span data-stu-id="dda36-232">Accessory</span></span>|<span data-ttu-id="dda36-233">Uni-directional</span><span class="sxs-lookup"><span data-stu-id="dda36-233">Uni-directional</span></span>|  
|<span data-ttu-id="dda36-234">Cross-sell</span><span class="sxs-lookup"><span data-stu-id="dda36-234">Cross-sell</span></span>|<span data-ttu-id="dda36-235">Uni-directional or Bi-directional</span><span class="sxs-lookup"><span data-stu-id="dda36-235">Uni-directional or Bi-directional</span></span>|  
|<span data-ttu-id="dda36-236">Substitute</span><span class="sxs-lookup"><span data-stu-id="dda36-236">Substitute</span></span>|<span data-ttu-id="dda36-237">Uni-directional or Bi-directional</span><span class="sxs-lookup"><span data-stu-id="dda36-237">Uni-directional or Bi-directional</span></span>|  
|<span data-ttu-id="dda36-238">Up-Sell</span><span class="sxs-lookup"><span data-stu-id="dda36-238">Up-Sell</span></span>|<span data-ttu-id="dda36-239">Uni-directional</span><span class="sxs-lookup"><span data-stu-id="dda36-239">Uni-directional</span></span>|  
  
 <span data-ttu-id="dda36-240">Use the **ProductSubstitute.Direction** attribute to specify direction for a product relationship.</span><span class="sxs-lookup"><span data-stu-id="dda36-240">Use the **ProductSubstitute.Direction** attribute to specify direction for a product relationship.</span></span> <span data-ttu-id="dda36-241">Set the value of this attribute to:</span><span class="sxs-lookup"><span data-stu-id="dda36-241">Set the value of this attribute to:</span></span>  
  
- <span data-ttu-id="dda36-242">**0** for uni-directional</span><span class="sxs-lookup"><span data-stu-id="dda36-242">**0** for uni-directional</span></span>  
  
- <span data-ttu-id="dda36-243">**1** for bi-directional</span><span class="sxs-lookup"><span data-stu-id="dda36-243">**1** for bi-directional</span></span>  
  
  <span data-ttu-id="dda36-244">The following code sample demonstrates how you can define relationships for products.</span><span class="sxs-lookup"><span data-stu-id="dda36-244">The following code sample demonstrates how you can define relationships for products.</span></span>  
  
```csharp
// Set product relationship  
// Set product1 and product2 as substitute of each other (bi-directional)  
ProductSubstitute newProductRelation = new ProductSubstitute  
{  
   SalesRelationshipType = new OptionSetValue(3),  
   Direction = new OptionSetValue(1),  
   ProductId = new EntityReference(Product.EntityLogicalName, _product1Id),  
   SubstitutedProductId = new EntityReference(Product.EntityLogicalName, _product2Id)  
};  
_productRelationId = _serviceProxy.Create(newProductRelation);  
```  
  
<a name="Clone"></a>   
## <a name="clone-a-product-family-product-or-bundle"></a><span data-ttu-id="dda36-245">Clone a product family, product, or bundle</span><span class="sxs-lookup"><span data-stu-id="dda36-245">Clone a product family, product, or bundle</span></span>  
 <span data-ttu-id="dda36-246">Use the <xref:Microsoft.Crm.Sdk.Messages.CloneProductRequest> message to clone a product family, product, or bundle record, and create a copy of the record under the same parent node.</span><span class="sxs-lookup"><span data-stu-id="dda36-246">Use the <xref:Microsoft.Crm.Sdk.Messages.CloneProductRequest> message to clone a product family, product, or bundle record, and create a copy of the record under the same parent node.</span></span> <span data-ttu-id="dda36-247">You must provide the ID of the record to clone.</span><span class="sxs-lookup"><span data-stu-id="dda36-247">You must provide the ID of the record to clone.</span></span> <span data-ttu-id="dda36-248">Cloning a product record also copies the properties of the product.</span><span class="sxs-lookup"><span data-stu-id="dda36-248">Cloning a product record also copies the properties of the product.</span></span> <span data-ttu-id="dda36-249">The cloned record is created with the date and time stamp appended to the original values in the **Product.Name** and **Product.ProductNumber** attributes; the date time stamp denotes the time when the record was cloned.</span><span class="sxs-lookup"><span data-stu-id="dda36-249">The cloned record is created with the date and time stamp appended to the original values in the **Product.Name** and **Product.ProductNumber** attributes; the date time stamp denotes the time when the record was cloned.</span></span> <span data-ttu-id="dda36-250">The following code sample demonstrates how to clone a product.</span><span class="sxs-lookup"><span data-stu-id="dda36-250">The following code sample demonstrates how to clone a product.</span></span>  
  
```csharp  
CloneProductRequest cloneReq = new CloneProductRequest  
{  
   Source = new EntityReference(Product.EntityLogicalName, _productId)  
};  
  
CloneProductResponse cloned = (CloneProductResponse)_serviceProxy.Execute(cloneReq);                                       
_productCloneId = cloned.ClonedProduct.Id;  
  
// Retrieve the cloned product record  
Product retrievedProduct = (Product)_serviceProxy.Retrieve(Product.EntityLogicalName, _productCloneId, new ColumnSet(true));  
Console.WriteLine("\nCreated clone product: {0}", retrievedProduct.Name);  
```  
  
## <a name="next-step"></a><span data-ttu-id="dda36-251">Bước tiếp theo</span><span class="sxs-lookup"><span data-stu-id="dda36-251">Next step</span></span>  
 <span data-ttu-id="dda36-252">Publish your product records to make products available for selling by your sales agents.</span><span class="sxs-lookup"><span data-stu-id="dda36-252">Publish your product records to make products available for selling by your sales agents.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="dda36-253">[Publish a product family, product, or bundle](publish-revise-revert-retire-activate-products.md#Publish)</span><span class="sxs-lookup"><span data-stu-id="dda36-253">[Publish a product family, product, or bundle](publish-revise-revert-retire-activate-products.md#Publish)</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="dda36-254">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="dda36-254">See also</span></span>  
 <span data-ttu-id="dda36-255">[Publish, revise, revert, retire, and activate products (product lifecycle)](publish-revise-revert-retire-activate-products.md) </span><span class="sxs-lookup"><span data-stu-id="dda36-255">[Publish, revise, revert, retire, and activate products (product lifecycle)](publish-revise-revert-retire-activate-products.md) </span></span>  
 <span data-ttu-id="dda36-256">[Sample: Create and publish products](sample-create-publish-products.md) </span><span class="sxs-lookup"><span data-stu-id="dda36-256">[Sample: Create and publish products](sample-create-publish-products.md) </span></span>  
 <span data-ttu-id="dda36-257">[Sample: Clone product records](sample-clone-product-records.md) </span><span class="sxs-lookup"><span data-stu-id="dda36-257">[Sample: Clone product records](sample-clone-product-records.md) </span></span>  
 <span data-ttu-id="dda36-258">[Sample: Add products to a bundle](sample-add-products-bundle.md) </span><span class="sxs-lookup"><span data-stu-id="dda36-258">[Sample: Add products to a bundle](sample-add-products-bundle.md) </span></span>  
 [<span data-ttu-id="dda36-259">Product catalog entities</span><span class="sxs-lookup"><span data-stu-id="dda36-259">Product catalog entities</span></span>](product-catalog-entities.md)
