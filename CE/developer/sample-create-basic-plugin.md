---
title: 'Sample: Create a basic plug-in (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample shows how to write a basic plug-in that can access the Dynamics 365 for Customer Engagement organization Web service. '
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 40a9c015-696f-43e4-9b4d-209fe7b8ace6
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 16
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 341bbc52c312c6d97c31249a4eff34da367e8048
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387589"
---
# <a name="sample-create-a-basic-plug-in"></a><span data-ttu-id="4f752-103">Sample: Create a basic plug-in</span><span class="sxs-lookup"><span data-stu-id="4f752-103">Sample: Create a basic plug-in</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4f752-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="4f752-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement apps.</span></span> <span data-ttu-id="4f752-105">Download the sample: [Work with plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade).</span><span class="sxs-lookup"><span data-stu-id="4f752-105">Download the sample: [Work with plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4f752-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="4f752-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="4f752-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="4f752-107">Requirements</span></span>  
 <span data-ttu-id="4f752-108">Register this plug-in for an account entity, on the Create message, and in asynchronous mode.</span><span class="sxs-lookup"><span data-stu-id="4f752-108">Register this plug-in for an account entity, on the Create message, and in asynchronous mode.</span></span> <span data-ttu-id="4f752-109">Alternately, you can register the plug-in on a post-event in the sandbox.</span><span class="sxs-lookup"><span data-stu-id="4f752-109">Alternately, you can register the plug-in on a post-event in the sandbox.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="4f752-110">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="4f752-110">Demonstrates</span></span>  
 <span data-ttu-id="4f752-111">This sample shows how to write a basic plug-in that can access the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] for Customer Engagement apps Organization Web service.</span><span class="sxs-lookup"><span data-stu-id="4f752-111">This sample shows how to write a basic plug-in that can access the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] for Customer Engagement apps Organization Web service.</span></span>  
  
 <span data-ttu-id="4f752-112">The plug-in creates a task activity after a new account is created.</span><span class="sxs-lookup"><span data-stu-id="4f752-112">The plug-in creates a task activity after a new account is created.</span></span> <span data-ttu-id="4f752-113">The activity reminds the user to follow-up with the new account customer one week after the account was created.</span><span class="sxs-lookup"><span data-stu-id="4f752-113">The activity reminds the user to follow-up with the new account customer one week after the account was created.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4f752-114">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="4f752-114">Example</span></span>  
 [!code-csharp[Plug-ins#FollowupPlugin](../snippets/csharp/CRMV8/plug-ins/cs/followupplugin.cs#followupplugin)]  
  
### <a name="see-also"></a><span data-ttu-id="4f752-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4f752-115">See also</span></span>  
 <span data-ttu-id="4f752-116">[Plug-in Development](plugin-development.md) </span><span class="sxs-lookup"><span data-stu-id="4f752-116">[Plug-in Development](plugin-development.md) </span></span>  
 <span data-ttu-id="4f752-117">[Sample: Web Access from a Sandboxed Plug-in](sample-web-access-sandboxed-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="4f752-117">[Sample: Web Access from a Sandboxed Plug-in](sample-web-access-sandboxed-plugin.md) </span></span>  
 <span data-ttu-id="4f752-118">[Write a Plug-in](write-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="4f752-118">[Write a Plug-in](write-plugin.md) </span></span>  
 <span data-ttu-id="4f752-119">[Register and Deploy Plug-ins](register-deploy-plugins.md) </span><span class="sxs-lookup"><span data-stu-id="4f752-119">[Register and Deploy Plug-ins](register-deploy-plugins.md) </span></span>  
 <span data-ttu-id="4f752-120">[Event Execution Pipeline](event-execution-pipeline.md) </span><span class="sxs-lookup"><span data-stu-id="4f752-120">[Event Execution Pipeline](event-execution-pipeline.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.IPlugin>   
 <xref:Microsoft.Xrm.Sdk.IPluginExecutionContext>   
 <xref:Microsoft.Xrm.Sdk.ITracingService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationServiceFactory>
