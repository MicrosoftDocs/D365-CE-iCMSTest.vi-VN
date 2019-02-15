---
title: 'Sample: Upload, retrieve, and download an attachment | MicrosoftDocs'
description: 'The sample demonstrates how to upload, retrieve, and download an attachment for an annotation using the IOrganizationService.Entity) and IOrganizationService.ColumnSet) methods. '
ms.custom: ''
ms.date: 11/24/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- uploading; retrieving; and downloading attachments sample, sample for the annotation (note) entity
- sample for uploading; retrieving; and downloading attachments, annotation (note) entity sample
ms.assetid: a231c619-7130-43f0-b3da-fd1a87545672
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7385b434350bf9a1b95057821311576b11a08dda
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387528"
---
# <a name="sample-upload-retrieve-and-download-an-attachment"></a><span data-ttu-id="3d62e-103">Sample: Upload, retrieve, and download an attachment</span><span class="sxs-lookup"><span data-stu-id="3d62e-103">Sample: Upload, retrieve, and download an attachment</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3d62e-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="3d62e-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="3d62e-105">Download the complete sample from [Work with Annotations](https://code.msdn.microsoft.com/Annotation-Sample-9d797e21).</span><span class="sxs-lookup"><span data-stu-id="3d62e-105">Download the complete sample from [Work with Annotations](https://code.msdn.microsoft.com/Annotation-Sample-9d797e21).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="3d62e-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="3d62e-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="3d62e-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="3d62e-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="3d62e-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="3d62e-108">Demonstrates</span></span>  
 <span data-ttu-id="3d62e-109">This sample shows how to upload, retrieve, and download an attachment for an annotation using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="3d62e-109">This sample shows how to upload, retrieve, and download an attachment for an annotation using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span> <span data-ttu-id="3d62e-110">and <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span><span class="sxs-lookup"><span data-stu-id="3d62e-110">and <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span></span> <span data-ttu-id="3d62e-111">methods.</span><span class="sxs-lookup"><span data-stu-id="3d62e-111">methods.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3d62e-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="3d62e-112">Example</span></span>  
 [!code-csharp[Annotation#UploadAndDownloadAttachment](../snippets/csharp/CRMV8/annotation/cs/uploadanddownloadattachment.cs#uploadanddownloadattachment)]  
  
### <a name="see-also"></a><span data-ttu-id="3d62e-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3d62e-113">See also</span></span>  
 <span data-ttu-id="3d62e-114">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="3d62e-114">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="3d62e-115">[Annotation (Note) Entity](annotation-note-entity.md) </span><span class="sxs-lookup"><span data-stu-id="3d62e-115">[Annotation (Note) Entity](annotation-note-entity.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>
