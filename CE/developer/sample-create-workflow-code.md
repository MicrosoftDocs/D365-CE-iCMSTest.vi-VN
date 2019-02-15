---
title: 'Sample: Create a workflow in code (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
descrption: The sample shows how to programmatically create an asynchronous workflow in code instead of using a workflow editor or designer. This sample works only with an on-premises deployment of Dynamics 365 for Customer Engagement (online) because custom XAML workflows are not supported in Dynamics 365 for Customer Engagement (online).
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 7105761b-9710-4ad1-a3ee-b7dd58287c81
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 92bb2669a7a8d2b465dd0f68d2ebbaeb319703c4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386917"
---
# <a name="sample-create-a-workflow-in-code"></a><span data-ttu-id="ce2eb-102">Sample: Create a workflow in code</span><span class="sxs-lookup"><span data-stu-id="ce2eb-102">Sample: Create a workflow in code</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ce2eb-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="ce2eb-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] for Customer Engagement apps.</span></span> <span data-ttu-id="ce2eb-104">Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).</span><span class="sxs-lookup"><span data-stu-id="ce2eb-104">Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ce2eb-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="ce2eb-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="ce2eb-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="ce2eb-106">Requirements</span></span>  
 <span data-ttu-id="ce2eb-107">You must enable support for custom XAML workflows on your on-premises server.</span><span class="sxs-lookup"><span data-stu-id="ce2eb-107">You must enable support for custom XAML workflows on your on-premises server.</span></span> [!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]  
  
## <a name="demonstrates"></a><span data-ttu-id="ce2eb-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="ce2eb-108">Demonstrates</span></span>  
 <span data-ttu-id="ce2eb-109">The following sample shows how to programmatically create an asynchronous workflow in code instead of using a workflow editor or designer.</span><span class="sxs-lookup"><span data-stu-id="ce2eb-109">The following sample shows how to programmatically create an asynchronous workflow in code instead of using a workflow editor or designer.</span></span> <span data-ttu-id="ce2eb-110">This sample works only with an on-premises deployment of [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] because custom XAML workflows are not supported in [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="ce2eb-110">This sample works only with an on-premises deployment of [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] because custom XAML workflows are not supported in [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]
## <a name="example"></a><span data-ttu-id="ce2eb-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="ce2eb-111">Example</span></span>  
 [!code-csharp[Workflows#CreateAWorkflow](../snippets/csharp/CRMV8/workflows/cs/createaworkflow.cs#createaworkflow)]  
  
### <a name="see-also"></a><span data-ttu-id="ce2eb-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ce2eb-112">See also</span></span>  
 <span data-ttu-id="ce2eb-113">[Sample code for workflows](sample-code-processes.md) </span><span class="sxs-lookup"><span data-stu-id="ce2eb-113">[Sample code for workflows](sample-code-processes.md) </span></span>  
 <span data-ttu-id="ce2eb-114">[Sample: Create a real-time workflow in code](sample-create-real-time-workflow-code.md) </span><span class="sxs-lookup"><span data-stu-id="ce2eb-114">[Sample: Create a real-time workflow in code](sample-create-real-time-workflow-code.md) </span></span>  
 <span data-ttu-id="ce2eb-115">[Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md) </span><span class="sxs-lookup"><span data-stu-id="ce2eb-115">[Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md) </span></span>  
 [<span data-ttu-id="ce2eb-116">Workflow and Process Entities</span><span class="sxs-lookup"><span data-stu-id="ce2eb-116">Workflow and Process Entities</span></span>](workflow-process-entities.md)
