---
title: 'Sample: Create a real-time workflow in code (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: 'The sample shows you how to create a real-time workflow in code instead of using the interactive workflow designer in the web application. This sample works only with an on-premises or an Internet-facing deployment (IFD) of Dynamics 365 for Customer Engagement because custom XAML workflows aren’t supported in Dynamics 365 for Customer Engagement (online). '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 78a964e8-0f5a-4075-8d22-32b984e3c0c3
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d19f5e9100b26fb3225cd7a88ab9797b7bcccba8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387130"
---
# <a name="sample-create-a-real-time-workflow-in-code"></a><span data-ttu-id="0138f-104">Sample: Create a real-time workflow in code</span><span class="sxs-lookup"><span data-stu-id="0138f-104">Sample: Create a real-time workflow in code</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0138f-105">This sample code applies to on–premises [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0138f-105">This sample code applies to on–premises [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="0138f-106">Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).</span><span class="sxs-lookup"><span data-stu-id="0138f-106">Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0138f-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="0138f-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="0138f-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="0138f-108">Requirements</span></span>  
 <span data-ttu-id="0138f-109">You must enable support for custom XAML workflows on your on-premises server.</span><span class="sxs-lookup"><span data-stu-id="0138f-109">You must enable support for custom XAML workflows on your on-premises server.</span></span> [!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]  
  
## <a name="demonstrates"></a><span data-ttu-id="0138f-110">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="0138f-110">Demonstrates</span></span>  
 <span data-ttu-id="0138f-111">The following sample shows you how to create a real-time workflow in code instead of using the interactive workflow designer in the web application.</span><span class="sxs-lookup"><span data-stu-id="0138f-111">The following sample shows you how to create a real-time workflow in code instead of using the interactive workflow designer in the web application.</span></span> <span data-ttu-id="0138f-112">This sample works only with an on-premises or an Internet-facing deployment (IFD) of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] for Customer Engagement because custom XAML workflows aren’t supported in Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0138f-112">This sample works only with an on-premises or an Internet-facing deployment (IFD) of [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] for Customer Engagement because custom XAML workflows aren’t supported in Dynamics 365 for Customer Engagement.</span></span>  
  
 [!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]

## <a name="example"></a><span data-ttu-id="0138f-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="0138f-113">Example</span></span>  
 [!code-csharp[Workflows#CreateRealtimeWorkflow](../snippets/csharp/CRMV8/workflows/cs/createrealtimeworkflow.cs#createrealtimeworkflow)]  
  
### <a name="see-also"></a><span data-ttu-id="0138f-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0138f-114">See also</span></span>  
 <span data-ttu-id="0138f-115">[Create real-time workflows](create-real-time-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0138f-115">[Create real-time workflows](create-real-time-workflows.md) </span></span>  
 <span data-ttu-id="0138f-116">[Sample: Set the State of a Workflow](sample-set-state-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="0138f-116">[Sample: Set the State of a Workflow](sample-set-state-workflow.md) </span></span>  
 <span data-ttu-id="0138f-117">[Workflow and Process Entities](workflow-process-entities.md) </span><span class="sxs-lookup"><span data-stu-id="0138f-117">[Workflow and Process Entities](workflow-process-entities.md) </span></span>  
 [<span data-ttu-id="0138f-118">Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)</span><span class="sxs-lookup"><span data-stu-id="0138f-118">Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)</span></span>](automate-business-processes-customer-engagement.md)
