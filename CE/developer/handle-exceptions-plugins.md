---
title: Handle exceptions in plug-ins (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about handling exceptions for synchronous plug-ins, that are passed back from a plug-in by displaying an error message in a dialog of the web application user interface. The exception message for asynchronous registered plug-ins is written to a System Job (AsyncOperation) record which can be viewed in the System Jobs area of the web application.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f4f28db1-d744-462a-9eae-544106f95cb8
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0b187fb61602dcd28e64a5d8f5f52386dd41f5d4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388062"
---
# <a name="handle-exceptions-in-plug-ins"></a><span data-ttu-id="78ec5-104">Handle exceptions in plug-ins</span><span class="sxs-lookup"><span data-stu-id="78ec5-104">Handle exceptions in plug-ins</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="78ec5-105">For synchronous plug-ins, whether registered in the sandbox or not, the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps platform handles exceptions passed back from a plug-in by displaying an error message in a dialog of the web application user interface.</span><span class="sxs-lookup"><span data-stu-id="78ec5-105">For synchronous plug-ins, whether registered in the sandbox or not, the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps platform handles exceptions passed back from a plug-in by displaying an error message in a dialog of the web application user interface.</span></span> <span data-ttu-id="78ec5-106">The exception message for asynchronous registered plug-ins is written to a System Job (`AsyncOperation`) record which can be viewed in the System Jobs area of the web application.</span><span class="sxs-lookup"><span data-stu-id="78ec5-106">The exception message for asynchronous registered plug-ins is written to a System Job (`AsyncOperation`) record which can be viewed in the System Jobs area of the web application.</span></span>  
  
 <span data-ttu-id="78ec5-107">For synchronous plug-ins, you can optionally display a custom error message in the error dialog of the web application by having your plug-in throw an <xref:Microsoft.Xrm.Sdk.InvalidPluginExecutionException> exception with the custom message string as the exception **Message** property value.</span><span class="sxs-lookup"><span data-stu-id="78ec5-107">For synchronous plug-ins, you can optionally display a custom error message in the error dialog of the web application by having your plug-in throw an <xref:Microsoft.Xrm.Sdk.InvalidPluginExecutionException> exception with the custom message string as the exception **Message** property value.</span></span> <span data-ttu-id="78ec5-108">If you throw <xref:Microsoft.Xrm.Sdk.InvalidPluginExecutionException> and do not provide a custom message, a generic default message is displayed in the error dialog.</span><span class="sxs-lookup"><span data-stu-id="78ec5-108">If you throw <xref:Microsoft.Xrm.Sdk.InvalidPluginExecutionException> and do not provide a custom message, a generic default message is displayed in the error dialog.</span></span> <span data-ttu-id="78ec5-109">It is recommended that plug-ins only pass an <xref:Microsoft.Xrm.Sdk.InvalidPluginExecutionException> back to the platform.</span><span class="sxs-lookup"><span data-stu-id="78ec5-109">It is recommended that plug-ins only pass an <xref:Microsoft.Xrm.Sdk.InvalidPluginExecutionException> back to the platform.</span></span>  
  
 <span data-ttu-id="78ec5-110">If a synchronous plug-in returns an exception other than <xref:Microsoft.Xrm.Sdk.InvalidPluginExecutionException> back to the platform, the error dialog is displayed to the user and the exception message ([System.Exception.Message](https://msdn.microsoft.com/library/system.exception.message.aspx)) with stack trace is also written to one of two places.</span><span class="sxs-lookup"><span data-stu-id="78ec5-110">If a synchronous plug-in returns an exception other than <xref:Microsoft.Xrm.Sdk.InvalidPluginExecutionException> back to the platform, the error dialog is displayed to the user and the exception message ([System.Exception.Message](https://msdn.microsoft.com/library/system.exception.message.aspx)) with stack trace is also written to one of two places.</span></span> <span data-ttu-id="78ec5-111">For plug-ins not registered in the sandbox, the information is written to the Application event log on the server that runs the plug-in.</span><span class="sxs-lookup"><span data-stu-id="78ec5-111">For plug-ins not registered in the sandbox, the information is written to the Application event log on the server that runs the plug-in.</span></span> <span data-ttu-id="78ec5-112">The event log can be viewed by using the Event Viewer administrative tool.</span><span class="sxs-lookup"><span data-stu-id="78ec5-112">The event log can be viewed by using the Event Viewer administrative tool.</span></span> <span data-ttu-id="78ec5-113">For plug-ins registered in the sandbox, the exception message and stack trace is written to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps platform trace.</span><span class="sxs-lookup"><span data-stu-id="78ec5-113">For plug-ins registered in the sandbox, the exception message and stack trace is written to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps platform trace.</span></span> <span data-ttu-id="78ec5-114">For more information about tracing, see the Logging and Tracing section of the [Debug a Plug-in](debug-plugin.md) topic.</span><span class="sxs-lookup"><span data-stu-id="78ec5-114">For more information about tracing, see the Logging and Tracing section of the [Debug a Plug-in](debug-plugin.md) topic.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="78ec5-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="78ec5-115">See also</span></span>  
 <span data-ttu-id="78ec5-116">[Plug-in Development](plugin-development.md) </span><span class="sxs-lookup"><span data-stu-id="78ec5-116">[Plug-in Development](plugin-development.md) </span></span>  
 <span data-ttu-id="78ec5-117">[Pass Data Between Plug-ins](pass-data-between-plug-ins.md) </span><span class="sxs-lookup"><span data-stu-id="78ec5-117">[Pass Data Between Plug-ins](pass-data-between-plug-ins.md) </span></span>  
 <span data-ttu-id="78ec5-118">[Write a Plug-in](write-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="78ec5-118">[Write a Plug-in](write-plugin.md) </span></span>  
 <span data-ttu-id="78ec5-119">[Debug a Plug-in](debug-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="78ec5-119">[Debug a Plug-in](debug-plugin.md) </span></span>  
 [<span data-ttu-id="78ec5-120">Handle Exceptions in Your Code</span><span class="sxs-lookup"><span data-stu-id="78ec5-120">Handle Exceptions in Your Code</span></span>](org-service/handle-exceptions-code.md)
