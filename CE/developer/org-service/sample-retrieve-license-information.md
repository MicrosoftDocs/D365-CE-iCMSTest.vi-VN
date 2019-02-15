---
title: 'Sample: Retrieve license information (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to use the IDeploymentService.RetrieveDeploymentLicenseTypeRequest message and the IOrganizationService.RetrieveLicenseInfoRequest message to retrieve information about licenses
keywords: ''
ms.date: 12/15/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 7c8bd1ce-59e0-4884-b7bf-e809d7fd0b75
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0ff0b135805ccaa70a39af3dfbb3f203a7cea22b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386520"
---
# <a name="sample-retrieve-license-information"></a><span data-ttu-id="b0b80-103">Sample: Retrieve license information</span><span class="sxs-lookup"><span data-stu-id="b0b80-103">Sample: Retrieve license information</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b0b80-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="b0b80-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="b0b80-105">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span><span class="sxs-lookup"><span data-stu-id="b0b80-105">Download the Sample: [Work with early bound entity classes in code](https://code.msdn.microsoft.com/Work-with-early-bound-6914f6e7).</span></span>   

## <a name="prerequisites"></a><span data-ttu-id="b0b80-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="b0b80-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="b0b80-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="b0b80-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
 [<span data-ttu-id="b0b80-108">Full Sample – C#</span><span class="sxs-lookup"><span data-stu-id="b0b80-108">Full Sample – C#</span></span>](sample-initialize-record-existing-record.md#full_C)  
  
## <a name="demonstrates"></a><span data-ttu-id="b0b80-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="b0b80-109">Demonstrates</span></span>  
 <span data-ttu-id="b0b80-110">This sample shows how to use the <xref:Microsoft.Xrm.Sdk.Deployment.IDeploymentService>.<xref:Microsoft.Crm.Sdk.Messages.RetrieveDeploymentLicenseTypeRequest></span><span class="sxs-lookup"><span data-stu-id="b0b80-110">This sample shows how to use the <xref:Microsoft.Xrm.Sdk.Deployment.IDeploymentService>.<xref:Microsoft.Crm.Sdk.Messages.RetrieveDeploymentLicenseTypeRequest></span></span> <span data-ttu-id="b0b80-111">message and the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Crm.Sdk.Messages.RetrieveLicenseInfoRequest></span><span class="sxs-lookup"><span data-stu-id="b0b80-111">message and the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Crm.Sdk.Messages.RetrieveLicenseInfoRequest></span></span> <span data-ttu-id="b0b80-112">message to retrieve information about licenses.</span><span class="sxs-lookup"><span data-stu-id="b0b80-112">message to retrieve information about licenses.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b0b80-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="b0b80-113">Example</span></span>  
 [!code-csharp[StrongTypes#License1](../../snippets/csharp/CRMV8/strongtypes/cs/license1.cs#license1)]  
  
<a name="full_C"></a>   
## <a name="full-sample--c"></a><span data-ttu-id="b0b80-114">Full Sample – C#</span><span class="sxs-lookup"><span data-stu-id="b0b80-114">Full Sample – C#</span></span>  
 [!code-csharp[StrongTypes#License](../../snippets/csharp/CRMV8/strongtypes/cs/license.cs#license)]  
  
### <a name="see-also"></a><span data-ttu-id="b0b80-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b0b80-115">See also</span></span>  
 <span data-ttu-id="b0b80-116">[Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md) </span><span class="sxs-lookup"><span data-stu-id="b0b80-116">[Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Deployment.IDeploymentService>   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveDeploymentLicenseTypeRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveLicenseInfoRequest>
