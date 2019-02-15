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
# <a name="sample-calculate-price-plug-in"></a>Sample: Calculate Price plug-in

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the sample: [Work with custom price plug-in](https://msdn.microsoft.com/en-us/library/dn817877.aspx).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]

## <a name="requirements"></a>Yêu cầu  
 Ensure the following:  
  
-   Set the value of the `Organization.OOBPriceCalculationEnabled` attribute to `0` (false).  
  
-   Register the plug-in on the **CalculatePrice** message, **Post-operation** event stage, and **Synchronous** execution mode. For more information, see [Register and Deploy Plug-ins](register-deploy-plugins.md).  
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to write a plug-in that calculates the pricing of the opportunities, quotes, orders, and invoices based on your custom code. The discounts and taxes are calculated based on the total amount of all the product line items in an opportunity, quote, order, or invoice:  
  
- **Discount**: If the total amount is greater than 1000 and less than 5000, discount is 5%; if the total amount is 5000 or greater, discount is 10%.  
  
- **Tax**: Tax is applied on the amount that is effective after the discount is applied (total amount minus discount). If the effective amount is less than 5000, tax is 10%; otherwise, tax is 8%.  
  
  Để biết thêm chi tiết, xem [sử dụng định giá tùy chỉnh cho sản phẩm](use-custom-pricing-products.md).  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Plug-Ins#CalculatePricePlugin](../snippets/csharp/CRMV8/plug-ins/cs/calculatepriceplugin.cs#calculatepriceplugin)]  
  
### <a name="see-also"></a>Xem thêm  
 [Use custom pricing for products](use-custom-pricing-products.md)   
 [Create and manage product families, products and bundles](create-manage-product-families-products-bundles-product-properties.md)   
 [Thực thể Danh mục Sản phẩm](product-catalog-entities.md)
