---
title: Use dialogs for guided processes (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Dialogs are the synchronous or interactive processes in Dynamics 365 for Customer Engagement (online) Customer Engagement that collect and process information by using step-by-step scripts to direct users through a process
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- workflow, dialog
ms.assetid: d17f8ae2-854b-4f67-a115-5a03d4f0b8ce
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9133eae4263f2721022cb1050714867faea91091
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385616"
---
# <a name="use-dialogs-for-guided-processes"></a><span data-ttu-id="4c928-103">Use dialogs for guided processes</span><span class="sxs-lookup"><span data-stu-id="4c928-103">Use dialogs for guided processes</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4c928-104">Dialogs are the synchronous or interactive processes in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement that collect and process information by using step-by-step scripts to direct users through a process.</span><span class="sxs-lookup"><span data-stu-id="4c928-104">Dialogs are the synchronous or interactive processes in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement that collect and process information by using step-by-step scripts to direct users through a process.</span></span> <span data-ttu-id="4c928-105">For example, you can create dialogs to act as a guide for your service representatives for case resolution and case escalation.</span><span class="sxs-lookup"><span data-stu-id="4c928-105">For example, you can create dialogs to act as a guide for your service representatives for case resolution and case escalation.</span></span> <span data-ttu-id="4c928-106">Similarly, you can create dialogs for standardizing sales processes such as opportunity qualification and lead scoring.</span><span class="sxs-lookup"><span data-stu-id="4c928-106">Similarly, you can create dialogs for standardizing sales processes such as opportunity qualification and lead scoring.</span></span>  
  
 <span data-ttu-id="4c928-107">Every time that you run a dialog in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)], a `ProcessSession` record is created.</span><span class="sxs-lookup"><span data-stu-id="4c928-107">Every time that you run a dialog in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)], a `ProcessSession` record is created.</span></span> <span data-ttu-id="4c928-108">The process session stores the session log about the dialog process that was run.</span><span class="sxs-lookup"><span data-stu-id="4c928-108">The process session stores the session log about the dialog process that was run.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4c928-109">Due to the interactive nature of the dialog process, you can’t run a dialog using the [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)].</span><span class="sxs-lookup"><span data-stu-id="4c928-109">Due to the interactive nature of the dialog process, you can’t run a dialog using the [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)].</span></span> <span data-ttu-id="4c928-110">A dialog can only be run through the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web application.</span><span class="sxs-lookup"><span data-stu-id="4c928-110">A dialog can only be run through the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web application.</span></span> <span data-ttu-id="4c928-111">Dialogs aren’t supported in [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)].</span><span class="sxs-lookup"><span data-stu-id="4c928-111">Dialogs aren’t supported in [!INCLUDE[pn_crm_for_outlook_short](../includes/pn-crm-for-outlook-short.md)].</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4c928-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4c928-112">See also</span></span>  
 <span data-ttu-id="4c928-113">[Processes, Workflows, and Dialogs](process-categories.md) </span><span class="sxs-lookup"><span data-stu-id="4c928-113">[Processes, Workflows, and Dialogs](process-categories.md) </span></span>  
 [<span data-ttu-id="4c928-114">Processes in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="4c928-114">Processes in Dynamics 365 for Customer Engagement apps</span></span>](automate-business-processes-customer-engagement.md)
