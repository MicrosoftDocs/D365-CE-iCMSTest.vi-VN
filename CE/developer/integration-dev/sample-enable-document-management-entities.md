---
title: 'Sample: Enable document management for entities | MicrosoftDocs'
description: ''
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 3272e732-908d-461f-be4d-81a94bfc9afb
author: KumarVivek
ms.author: kvivek
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 28
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a97c54b4c68425c26eba8a24ff4b16da167a4648
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387642"
---
# <a name="sample-enable-document-management-for-entities"></a><span data-ttu-id="cd979-102">Sample: Enable document management for entities</span><span class="sxs-lookup"><span data-stu-id="cd979-102">Sample: Enable document management for entities</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="cd979-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="cd979-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="cd979-104">Download the sample: [With SharePoint Integration](https://code.msdn.microsoft.com/Samples-of-Sharepoint-b4fb016f).</span><span class="sxs-lookup"><span data-stu-id="cd979-104">Download the sample: [With SharePoint Integration](https://code.msdn.microsoft.com/Samples-of-Sharepoint-b4fb016f).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cd979-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="cd979-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="cd979-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="cd979-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="cd979-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="cd979-107">Demonstrates</span></span>  
 <span data-ttu-id="cd979-108">The following sample shows how to enable document management for entities in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="cd979-108">The following sample shows how to enable document management for entities in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="cd979-109">In this sample code, document management is enabled for the `Contact` entity using the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> message.</span><span class="sxs-lookup"><span data-stu-id="cd979-109">In this sample code, document management is enabled for the `Contact` entity using the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> message.</span></span> <span data-ttu-id="cd979-110">By default, the setting for the `Contact` entity isn’t enabled in a new installation of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="cd979-110">By default, the setting for the `Contact` entity isn’t enabled in a new installation of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cd979-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="cd979-111">Example</span></span>  
 [!code-csharp[SharePointIntegration#EnableDocumentManagement](../../snippets/csharp/CRMV8/sharepointintegration/cs/enabledocumentmanagement.cs#enabledocumentmanagement)]  
  
### <a name="see-also"></a><span data-ttu-id="cd979-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cd979-112">See also</span></span>  
 <span data-ttu-id="cd979-113">[Integrate SharePoint with Microsoft Dynamics 365 for Customer Engagement apps](integrate-sharepoint.md) </span><span class="sxs-lookup"><span data-stu-id="cd979-113">[Integrate SharePoint with Microsoft Dynamics 365 for Customer Engagement apps](integrate-sharepoint.md) </span></span>  
 <span data-ttu-id="cd979-114">[Enable SharePoint Integration](enable-document-management-entities.md) </span><span class="sxs-lookup"><span data-stu-id="cd979-114">[Enable SharePoint Integration](enable-document-management-entities.md) </span></span>  
 <span data-ttu-id="cd979-115">[Sample: Create, Retrieve, Update, and Delete a SharePoint Location Record](sample-create-retrieve-update-delete-sharepoint-location-record.md) </span><span class="sxs-lookup"><span data-stu-id="cd979-115">[Sample: Create, Retrieve, Update, and Delete a SharePoint Location Record](sample-create-retrieve-update-delete-sharepoint-location-record.md) </span></span>  
 <span data-ttu-id="cd979-116">[Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="cd979-116">[Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md) </span></span>  
 [<span data-ttu-id="cd979-117">Sample: Create, Retrieve, Update, and Delete (CRUD) a SharePoint Location Record</span><span class="sxs-lookup"><span data-stu-id="cd979-117">Sample: Create, Retrieve, Update, and Delete (CRUD) a SharePoint Location Record</span></span>](sample-create-retrieve-update-delete-sharepoint-location-record.md)
