---
title: 'Sample: Audit user access (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Sample demonstrating the auditing of user access to records.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: db508858-7386-44f3-9f91-29493e6fe2c4
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- auditing entity data changes in Microsoft Dynamics CRM, sample for auditing user access
- sample for auditing user access
- auditing user access sample
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f9590d073975dfc8a48ef3c17a332a3efdc0e267
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385736"
---
# <a name="sample-audit-user-access"></a><span data-ttu-id="93899-103">Sample: Audit user access</span><span class="sxs-lookup"><span data-stu-id="93899-103">Sample: Audit user access</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="93899-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="93899-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="93899-105">[Download the code samples of audit entity data changes and audit user access](https://code.msdn.microsoft.com/Audit-entity-data-changes-93eb8ae0).</span><span class="sxs-lookup"><span data-stu-id="93899-105">[Download the code samples of audit entity data changes and audit user access](https://code.msdn.microsoft.com/Audit-entity-data-changes-93eb8ae0).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="93899-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="93899-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="93899-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="93899-107">Requirements</span></span>  
 [!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)] <span data-ttu-id="93899-108">This sample requires the logged on user to have the System Administrator role for enabling auditing on an organization.</span><span class="sxs-lookup"><span data-stu-id="93899-108">This sample requires the logged on user to have the System Administrator role for enabling auditing on an organization.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="93899-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="93899-109">Demonstrates</span></span>  
 <span data-ttu-id="93899-110">This sample demonstrates how to audit user access to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="93899-110">This sample demonstrates how to audit user access to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span>  
  
## <a name="example"></a><span data-ttu-id="93899-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="93899-111">Example</span></span>  
 <span data-ttu-id="93899-112">The sample first enables user access auditing with the logged on user’s organization.</span><span class="sxs-lookup"><span data-stu-id="93899-112">The sample first enables user access auditing with the logged on user’s organization.</span></span> <span data-ttu-id="93899-113">Next, it creates and modifies an account entity so that audit records are generated.</span><span class="sxs-lookup"><span data-stu-id="93899-113">Next, it creates and modifies an account entity so that audit records are generated.</span></span> <span data-ttu-id="93899-114">Finally, the sample displays the audited information.</span><span class="sxs-lookup"><span data-stu-id="93899-114">Finally, the sample displays the audited information.</span></span>  
  
 [!code-csharp[auditing#useraccessauditing](../snippets/csharp/CRMV8/auditing/cs/useraccessauditing.cs#useraccessauditing)]  
  
### <a name="see-also"></a><span data-ttu-id="93899-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="93899-115">See also</span></span>  
 <span data-ttu-id="93899-116">[Audit Entity Data Changes in Dynamics 365 for Customer Engagement apps](audit-entity-data-changes.md) </span><span class="sxs-lookup"><span data-stu-id="93899-116">[Audit Entity Data Changes in Dynamics 365 for Customer Engagement apps](audit-entity-data-changes.md) </span></span>  
 <span data-ttu-id="93899-117">[Audit Entity](entities/audit.md)<!-- Bug 696490 --></span><span class="sxs-lookup"><span data-stu-id="93899-117">[Audit Entity](entities/audit.md)<!-- Bug 696490 --></span></span>
