---
title: 'Sample: Work with global option sets (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2016
- Dynamics CRM Online
ms.assetid: 348e0bc9-ddde-4bbe-a0aa-968d0d6b0ac2
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a0b911448eda17d4a8ccefa75496cd4d7e80d098
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385625"
---
# <a name="sample-work-with-global-option-sets"></a><span data-ttu-id="99f8e-102">Sample: Work with global option sets</span><span class="sxs-lookup"><span data-stu-id="99f8e-102">Sample: Work with global option sets</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="99f8e-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="99f8e-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="99f8e-104">Download the sample: [Work with global option sets](https://code.msdn.microsoft.com/Samples-of-option-set-37c4b418).</span><span class="sxs-lookup"><span data-stu-id="99f8e-104">Download the sample: [Work with global option sets](https://code.msdn.microsoft.com/Samples-of-option-set-37c4b418).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="99f8e-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="99f8e-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="99f8e-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="99f8e-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="99f8e-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="99f8e-107">Demonstrates</span></span>  
 <span data-ttu-id="99f8e-108">This sample shows how to perform the following actions with global option sets:</span><span class="sxs-lookup"><span data-stu-id="99f8e-108">This sample shows how to perform the following actions with global option sets:</span></span>  
  
-   <span data-ttu-id="99f8e-109">Create, retrieve, or update a global option set.</span><span class="sxs-lookup"><span data-stu-id="99f8e-109">Create, retrieve, or update a global option set.</span></span>  
  
-   <span data-ttu-id="99f8e-110">Create a <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute using a global option set.</span><span class="sxs-lookup"><span data-stu-id="99f8e-110">Create a <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> attribute using a global option set.</span></span>  
  
-   <span data-ttu-id="99f8e-111">Insert or update an option item.</span><span class="sxs-lookup"><span data-stu-id="99f8e-111">Insert or update an option item.</span></span>  
  
-   <span data-ttu-id="99f8e-112">Re-order option items.</span><span class="sxs-lookup"><span data-stu-id="99f8e-112">Re-order option items.</span></span>  
  
-   <span data-ttu-id="99f8e-113">Retrieve all global option sets.</span><span class="sxs-lookup"><span data-stu-id="99f8e-113">Retrieve all global option sets.</span></span>  
  
## <a name="example"></a><span data-ttu-id="99f8e-114">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="99f8e-114">Example</span></span>  
 [!code-csharp[optionsets#WorkwithGlobalOptionSets](../../snippets/csharp/CRMV8/optionsets/cs/workwithglobaloptionsets.cs#workwithglobaloptionsets)]  
  
### <a name="see-also"></a><span data-ttu-id="99f8e-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="99f8e-115">See also</span></span>  
 <span data-ttu-id="99f8e-116">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="99f8e-116">[Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](use-organization-service-metadata.md) </span></span>  
 <span data-ttu-id="99f8e-117">[Customize Global Option Sets in Dynamics 365 for Customer Engagement apps](customize-global-option-sets.md) </span><span class="sxs-lookup"><span data-stu-id="99f8e-117">[Customize Global Option Sets in Dynamics 365 for Customer Engagement apps](customize-global-option-sets.md) </span></span>  
 <span data-ttu-id="99f8e-118">[Sample: Dump global option set information to a file](sample-dump-global-option-set-information-file.md) </span><span class="sxs-lookup"><span data-stu-id="99f8e-118">[Sample: Dump global option set information to a file](sample-dump-global-option-set-information-file.md) </span></span>  
 [<span data-ttu-id="99f8e-119">Global Option Set Messages</span><span class="sxs-lookup"><span data-stu-id="99f8e-119">Global Option Set Messages</span></span>](customize-global-option-sets.md#messages)
