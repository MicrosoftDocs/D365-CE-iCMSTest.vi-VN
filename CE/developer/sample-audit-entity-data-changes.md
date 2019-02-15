---
title: 'Sample: Audit entity data changes (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Sample demonstrating how to audit entity data changes.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d30356c5-da29-4466-8356-ec3d1acad578
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- sample for audit entity data changes
- auditing entity data changes in Microsoft Dynamics CRM, sample for audit entity data changes
- sample for enabling and disabling auditing, on entities and their attributes
- enabling and disabling auditing sample, on entities and their attributes
- audit entity data changes sample
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7563ab45e2c6e1d9f4a4773d71b968b0264fa289
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388772"
---
# <a name="sample-audit-entity-data-changes"></a><span data-ttu-id="40635-103">Sample: Audit entity data changes</span><span class="sxs-lookup"><span data-stu-id="40635-103">Sample: Audit entity data changes</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="40635-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="40635-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="40635-105">[Download the code samples of audit entity data changes and audit user access](https://code.msdn.microsoft.com/Audit-entity-data-changes-93eb8ae0).</span><span class="sxs-lookup"><span data-stu-id="40635-105">[Download the code samples of audit entity data changes and audit user access](https://code.msdn.microsoft.com/Audit-entity-data-changes-93eb8ae0).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="40635-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="40635-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="40635-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="40635-107">Requirements</span></span>  
 [!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)] <span data-ttu-id="40635-108">This sample requires the logged on user to have the System Administrator role.</span><span class="sxs-lookup"><span data-stu-id="40635-108">This sample requires the logged on user to have the System Administrator role.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="40635-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="40635-109">Demonstrates</span></span>  
 <span data-ttu-id="40635-110">How to enable and disable auditing on an entity and its attributes, retrieve the data change history of the audited entity, and delete the audit records.</span><span class="sxs-lookup"><span data-stu-id="40635-110">How to enable and disable auditing on an entity and its attributes, retrieve the data change history of the audited entity, and delete the audit records.</span></span>  
  
## <a name="example"></a><span data-ttu-id="40635-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="40635-111">Example</span></span>  
 [!code-csharp[Auditing#Auditing](../snippets/csharp/CRMV8/auditing/cs/auditing.cs#auditing)]  
  
### <a name="see-also"></a><span data-ttu-id="40635-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="40635-112">See also</span></span>  
 <span data-ttu-id="40635-113">[Audit Entity Data Changes in Dynamics 365 for Customer Engagement apps](audit-entity-data-changes.md) </span><span class="sxs-lookup"><span data-stu-id="40635-113">[Audit Entity Data Changes in Dynamics 365 for Customer Engagement apps](audit-entity-data-changes.md) </span></span>  
 <span data-ttu-id="40635-114">[Sample: Audit User Access](sample-audit-user-access.md) </span><span class="sxs-lookup"><span data-stu-id="40635-114">[Sample: Audit User Access](sample-audit-user-access.md) </span></span>  
 <span data-ttu-id="40635-115">[Audit Entity](entities/audit.md)<!-- Bug 696490 --></span><span class="sxs-lookup"><span data-stu-id="40635-115">[Audit Entity](entities/audit.md)<!-- Bug 696490 --></span></span>  
 <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsAuditEnabled>   
 <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.IsAuditEnabled>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveRecordChangeHistoryRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.AttributeAuditDetail>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveAuditPartitionListRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.DeleteAuditDataRequest>
