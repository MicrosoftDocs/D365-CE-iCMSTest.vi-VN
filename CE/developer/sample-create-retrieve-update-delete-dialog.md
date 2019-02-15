---
title: 'Sample: Create, retrieve, update, and delete a dialog (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample shows how to create, retrieve, update, and delete a dialog process using the methods IOrganizationService.Entity, IOrganizationService.ColumnSet, and IOrganizationService. Guid.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6bebfba9-833f-4e46-88e4-d1b5fa6b5962
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c68880016f2e8221fde04aa4eaddf1d52913ba8e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386044"
---
# <a name="sample-create-retrieve-update-and-delete-a-dialog"></a><span data-ttu-id="da820-104">Sample: Create, retrieve, update, and delete a dialog</span><span class="sxs-lookup"><span data-stu-id="da820-104">Sample: Create, retrieve, update, and delete a dialog</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="da820-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="da820-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] for Customer Engagement apps.</span></span> <span data-ttu-id="da820-106">See the complete sample here [Sample: Create, retrieve, update, and delete a dialog](https://msdn.microsoft.com/en-us/library/gg334435.aspx)</span><span class="sxs-lookup"><span data-stu-id="da820-106">See the complete sample here [Sample: Create, retrieve, update, and delete a dialog](https://msdn.microsoft.com/en-us/library/gg334435.aspx)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="da820-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="da820-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="da820-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="da820-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="da820-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="da820-109">Demonstrates</span></span>  
 <span data-ttu-id="da820-110">This sample shows how to create, retrieve, update, and delete a dialog process using these methods:</span><span class="sxs-lookup"><span data-stu-id="da820-110">This sample shows how to create, retrieve, update, and delete a dialog process using these methods:</span></span>  
  
-   <span data-ttu-id="da820-111"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="da820-111"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span>  
  
-   <span data-ttu-id="da820-112"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span><span class="sxs-lookup"><span data-stu-id="da820-112"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span></span>  
  
-  <span data-ttu-id="da820-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span><span class="sxs-lookup"><span data-stu-id="da820-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span></span> <xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>  
  
## <a name="example"></a><span data-ttu-id="da820-114">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="da820-114">Example</span></span>  
 [!code-csharp[Dialogs#CRUDDialog](../snippets/csharp/CRMV8/dialogs/cs/cruddialog.cs#cruddialog)]  
  
### <a name="see-also"></a><span data-ttu-id="da820-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="da820-115">See also</span></span>  
 <span data-ttu-id="da820-116">[Use Dialogs in Dynamics 365 for Customer Engagement apps](use-dialogs-guided-processes.md) </span><span class="sxs-lookup"><span data-stu-id="da820-116">[Use Dialogs in Dynamics 365 for Customer Engagement apps](use-dialogs-guided-processes.md) </span></span>  
 <span data-ttu-id="da820-117">[Sample: Create a Workflow in Code](sample-create-workflow-code.md) </span><span class="sxs-lookup"><span data-stu-id="da820-117">[Sample: Create a Workflow in Code](sample-create-workflow-code.md) </span></span>  
 <span data-ttu-id="da820-118">[Sample Code for Processes](sample-code-processes.md) </span><span class="sxs-lookup"><span data-stu-id="da820-118">[Sample Code for Processes](sample-code-processes.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>
