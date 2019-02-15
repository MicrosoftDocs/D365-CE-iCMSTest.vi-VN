---
title: Insert, update, delete, and order global option set options (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2016
- Dynamics CRM Online
ms.assetid: dfcafa54-d368-46c8-8760-19bcbc4c6797
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5556d55cc343fc2f86bc4c1226767d1155b51b10
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387462"
---
# <a name="insert-update-delete-and-order-global-option-set-options"></a><span data-ttu-id="28b00-102">Insert, update, delete, and order global option set options</span><span class="sxs-lookup"><span data-stu-id="28b00-102">Insert, update, delete, and order global option set options</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="28b00-103">These code samples show you how to insert, update, delete, and order options in a global option set.</span><span class="sxs-lookup"><span data-stu-id="28b00-103">These code samples show you how to insert, update, delete, and order options in a global option set.</span></span>  
  
<a name="BKMK_InsertNewOption"></a>   
## <a name="insert-a-new-option"></a><span data-ttu-id="28b00-104">Insert a new option</span><span class="sxs-lookup"><span data-stu-id="28b00-104">Insert a new option</span></span>  
 <span data-ttu-id="28b00-105">The following sample shows how to add a new option to a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.InsertOptionValueRequest>:</span><span class="sxs-lookup"><span data-stu-id="28b00-105">The following sample shows how to add a new option to a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.InsertOptionValueRequest>:</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets5](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets5.cs#workwithglobaloptionsets5)]  

  
<a name="BKMK_UpdateAnOption"></a>   
## <a name="update-an-option"></a><span data-ttu-id="28b00-106">Update an option</span><span class="sxs-lookup"><span data-stu-id="28b00-106">Update an option</span></span>  
 <span data-ttu-id="28b00-107">The following sample shows how to update an option in a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionValueRequest>:</span><span class="sxs-lookup"><span data-stu-id="28b00-107">The following sample shows how to update an option in a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.UpdateOptionValueRequest>:</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets7](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets7.cs#workwithglobaloptionsets7)]  
  
<a name="BKMK_DeleteAnOption"></a>   
## <a name="delete-an-option"></a><span data-ttu-id="28b00-108">Xóa một tùy chọn</span><span class="sxs-lookup"><span data-stu-id="28b00-108">Delete an option</span></span>  
 <span data-ttu-id="28b00-109">The following sample shows how to deletes an option in a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionValueRequest>:</span><span class="sxs-lookup"><span data-stu-id="28b00-109">The following sample shows how to deletes an option in a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.DeleteOptionValueRequest>:</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets11](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets11.cs#workwithglobaloptionsets11)]  
  
<a name="BKMK_OrderOptions"></a>   
## <a name="order-options"></a><span data-ttu-id="28b00-110">Order options</span><span class="sxs-lookup"><span data-stu-id="28b00-110">Order options</span></span>  
 <span data-ttu-id="28b00-111">The following sample shows how to set the order of options in a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest>:</span><span class="sxs-lookup"><span data-stu-id="28b00-111">The following sample shows how to set the order of options in a global option set by using <xref:Microsoft.Xrm.Sdk.Messages.OrderOptionRequest>:</span></span>  
  
 [!code-csharp[OptionSets#WorkwithGlobalOptionSets8](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets8.cs#workwithglobaloptionsets8)] 
  
### <a name="see-also"></a><span data-ttu-id="28b00-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="28b00-112">See also</span></span>  
 [<span data-ttu-id="28b00-113">Customize Global Options Sets</span><span class="sxs-lookup"><span data-stu-id="28b00-113">Customize Global Options Sets</span></span>](../org-service/customize-global-option-sets.md)   
