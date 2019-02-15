---
title: Pass data between plug-ins (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about SharedVariables that is used for passing information between plug-ins. This is a collection of keyalue pairs. At run time, plug-ins can add, read, or modify properties in the SharedVariables collection. This provides a method of information communication among plug-ins.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
f1_keywords:
- plugins
- plugin
ms.assetid: b3f4fbd0-cede-4e68-8908-39a1f3419ca9
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c5bbd5199bcd8e678f7409eab141ee6f5b9dae6f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386981"
---
# <a name="pass-data-between-plug-ins"></a><span data-ttu-id="c0ac1-105">Pass data between plug-ins</span><span class="sxs-lookup"><span data-stu-id="c0ac1-105">Pass data between plug-ins</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c0ac1-106">The message pipeline model for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps defines a parameter collection of custom data values in the execution context that is passed through the pipeline and shared among registered plug-ins, even from different 3rd party developers.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-106">The message pipeline model for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps defines a parameter collection of custom data values in the execution context that is passed through the pipeline and shared among registered plug-ins, even from different 3rd party developers.</span></span> <span data-ttu-id="c0ac1-107">This collection of data can be used by different plug-ins to communicate information between plug-ins and enable chain processing where data processed by one plug-in can be processed by the next plug-in in the sequence and so on.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-107">This collection of data can be used by different plug-ins to communicate information between plug-ins and enable chain processing where data processed by one plug-in can be processed by the next plug-in in the sequence and so on.</span></span> <span data-ttu-id="c0ac1-108">This feature is especially useful in pricing engine scenarios where multiple pricing plug-ins pass data between one another to calculate the total price for a sales order or invoice.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-108">This feature is especially useful in pricing engine scenarios where multiple pricing plug-ins pass data between one another to calculate the total price for a sales order or invoice.</span></span> <span data-ttu-id="c0ac1-109">Another potential use for this feature is to communicate information between a plug-in registered for a pre-event and a plug-in registered for a post-event.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-109">Another potential use for this feature is to communicate information between a plug-in registered for a pre-event and a plug-in registered for a post-event.</span></span>  
  
 <span data-ttu-id="c0ac1-110">The name of the parameter that is used for passing information between plug-ins is <xref:Microsoft.Xrm.Sdk.IExecutionContext.SharedVariables>.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-110">The name of the parameter that is used for passing information between plug-ins is <xref:Microsoft.Xrm.Sdk.IExecutionContext.SharedVariables>.</span></span> <span data-ttu-id="c0ac1-111">This is a collection of key\value pairs.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-111">This is a collection of key\value pairs.</span></span> <span data-ttu-id="c0ac1-112">At run time, plug-ins can add, read, or modify properties in the **SharedVariables** collection.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-112">At run time, plug-ins can add, read, or modify properties in the **SharedVariables** collection.</span></span> <span data-ttu-id="c0ac1-113">This provides a method of information communication among plug-ins.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-113">This provides a method of information communication among plug-ins.</span></span>  

 <span data-ttu-id="c0ac1-114">Download the sample: [Work with plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade).</span><span class="sxs-lookup"><span data-stu-id="c0ac1-114">Download the sample: [Work with plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade).</span></span>
  
 <span data-ttu-id="c0ac1-115">This sample shows how to use **SharedVariables** to pass data from a pre-event registered plug-in to a post-event registered plug-in.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-115">This sample shows how to use **SharedVariables** to pass data from a pre-event registered plug-in to a post-event registered plug-in.</span></span>  
  
 [!code-csharp[Plug-ins#SharedVariablesPlugin](../snippets/csharp/CRMV8/plug-ins/cs/sharedvariablesplugin.cs#sharedvariablesplugin)]  
  
 <span data-ttu-id="c0ac1-116">It is important that any type of data added to the shared variables collection be serializable otherwise the server will not know how to serialize the data and plug-in execution will fail.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-116">It is important that any type of data added to the shared variables collection be serializable otherwise the server will not know how to serialize the data and plug-in execution will fail.</span></span>  
  
 <span data-ttu-id="c0ac1-117">For a plug-in registered in stage 20 or 40, to access the shared variables from a stage 10 registered plug-in that executes on create, update, delete, or by a <xref:Microsoft.Crm.Sdk.Messages.RetrieveExchangeRateRequest>, you must access the <xref:Microsoft.Xrm.Sdk.IPluginExecutionContext.ParentContext>.**SharedVariables** collection.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-117">For a plug-in registered in stage 20 or 40, to access the shared variables from a stage 10 registered plug-in that executes on create, update, delete, or by a <xref:Microsoft.Crm.Sdk.Messages.RetrieveExchangeRateRequest>, you must access the <xref:Microsoft.Xrm.Sdk.IPluginExecutionContext.ParentContext>.**SharedVariables** collection.</span></span> <span data-ttu-id="c0ac1-118">For all other cases, <xref:Microsoft.Xrm.Sdk.IPluginExecutionContext>.**SharedVariables** contains the collection.</span><span class="sxs-lookup"><span data-stu-id="c0ac1-118">For all other cases, <xref:Microsoft.Xrm.Sdk.IPluginExecutionContext>.**SharedVariables** contains the collection.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c0ac1-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c0ac1-119">See also</span></span>  
 <span data-ttu-id="c0ac1-120">[Plug-in Development](plugin-development.md) </span><span class="sxs-lookup"><span data-stu-id="c0ac1-120">[Plug-in Development](plugin-development.md) </span></span>  
 <span data-ttu-id="c0ac1-121">[Impersonation in Plug-ins](impersonation-plugins.md) </span><span class="sxs-lookup"><span data-stu-id="c0ac1-121">[Impersonation in Plug-ins](impersonation-plugins.md) </span></span>  
 <span data-ttu-id="c0ac1-122">[Event Execution Pipeline](event-execution-pipeline.md) </span><span class="sxs-lookup"><span data-stu-id="c0ac1-122">[Event Execution Pipeline](event-execution-pipeline.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.IPluginExecutionContext>
