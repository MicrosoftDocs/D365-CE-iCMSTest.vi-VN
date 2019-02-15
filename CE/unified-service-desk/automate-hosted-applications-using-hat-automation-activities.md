---
title: Automate hosted applications using HAT automation activities | MicrosoftDocs
description: Learn about the Hosted Application Toolkit (HAT) Software Factory that provides a set of workflow activities to drive automations that help you to automate hosted applications.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: d6d724ee-b55b-4b2d-afe5-991a32ff1a3c
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: aa01e18c50749dbd64315275718ee684bedae551
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388215"
---
# <a name="automate-hosted-applications-using-hat-automation-activities"></a><span data-ttu-id="1e102-103">Automate hosted applications using HAT automation activities</span><span class="sxs-lookup"><span data-stu-id="1e102-103">Automate hosted applications using HAT automation activities</span></span>
[!INCLUDE[pn_Windows_Workflow_Foundation](../includes/pn-windows-workflow-foundation.md)] <span data-ttu-id="1e102-104">(WF) allows you to implement business rules and procedures through a unique process of designing a workflow or automation model composed of multiple elements (called *activities*) that describe the business process.</span><span class="sxs-lookup"><span data-stu-id="1e102-104">(WF) allows you to implement business rules and procedures through a unique process of designing a workflow or automation model composed of multiple elements (called *activities*) that describe the business process.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="1e102-105">[Windows Workflow Foundation](http://msdn.microsoft.com/library/dd489441\(v=vs.100\).aspx)</span><span class="sxs-lookup"><span data-stu-id="1e102-105">[Windows Workflow Foundation](http://msdn.microsoft.com/library/dd489441\(v=vs.100\).aspx)</span></span>  
  
 <span data-ttu-id="1e102-106">In [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)], you can use the WF workflows or automations to describe the business logic that drives the hosted applications.</span><span class="sxs-lookup"><span data-stu-id="1e102-106">In [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)], you can use the WF workflows or automations to describe the business logic that drives the hosted applications.</span></span> <span data-ttu-id="1e102-107">Automations in [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] are WF assemblies or XAML that are executed by the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Automation Manager.</span><span class="sxs-lookup"><span data-stu-id="1e102-107">Automations in [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] are WF assemblies or XAML that are executed by the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Automation Manager.</span></span> <span data-ttu-id="1e102-108">Automations drive hosted applications independent of their type.</span><span class="sxs-lookup"><span data-stu-id="1e102-108">Automations drive hosted applications independent of their type.</span></span>  
  
 <span data-ttu-id="1e102-109">The [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] Software Factory provides a set of workflow activities to drive automations that help you to automate hosted applications.</span><span class="sxs-lookup"><span data-stu-id="1e102-109">The [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] Software Factory provides a set of workflow activities to drive automations that help you to automate hosted applications.</span></span> <span data-ttu-id="1e102-110">The activities cover [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] action, such as `DoAction` and `SetContext`, as well as the original WF activities to drive applications hosted via data-driven adapters (DDAs).</span><span class="sxs-lookup"><span data-stu-id="1e102-110">The activities cover [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] action, such as `DoAction` and `SetContext`, as well as the original WF activities to drive applications hosted via data-driven adapters (DDAs).</span></span> <span data-ttu-id="1e102-111">If the automation activities provided by [!INCLUDE[pn_hat](../includes/pn-hat.md)] don’t meet your development needs, you can extend them to fit your requirements.</span><span class="sxs-lookup"><span data-stu-id="1e102-111">If the automation activities provided by [!INCLUDE[pn_hat](../includes/pn-hat.md)] don’t meet your development needs, you can extend them to fit your requirements.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="1e102-112">In This Section</span><span class="sxs-lookup"><span data-stu-id="1e102-112">In This Section</span></span>  
 [<span data-ttu-id="1e102-113">Sử dụng hoạt động tự động hóa HAT</span><span class="sxs-lookup"><span data-stu-id="1e102-113">Use HAT automation activities</span></span>](../unified-service-desk/use-hat-automation-activities.md)  
  
 [<span data-ttu-id="1e102-114">Types of HAT automation activities</span><span class="sxs-lookup"><span data-stu-id="1e102-114">Types of HAT automation activities</span></span>](../unified-service-desk/types-of-hat-automation-activities.md)  
  
 [<span data-ttu-id="1e102-115">Create a HAT automation</span><span class="sxs-lookup"><span data-stu-id="1e102-115">Create a HAT automation</span></span>](../unified-service-desk/create-hat-automation.md)  
  
## <a name="related-sections"></a><span data-ttu-id="1e102-116">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="1e102-116">Related Sections</span></span>  
 [<span data-ttu-id="1e102-117">Work with HAT Software Factory</span><span class="sxs-lookup"><span data-stu-id="1e102-117">Work with HAT Software Factory</span></span>](../unified-service-desk/work-with-hat-software-factory.md)
