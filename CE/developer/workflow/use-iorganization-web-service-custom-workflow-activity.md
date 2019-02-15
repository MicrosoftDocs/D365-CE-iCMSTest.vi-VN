---
title: Use the IOrganization web service in a custom workflow activity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn on how to get the IOrganizationService from within the Execute method of your custom workflow activity.
ms.custom: ''
ms.date: 11/20/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 639d3a2d-9979-40aa-8947-1f5bbb489d79
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f126faa39821c55358f9bbd53e16701bbdafd9ba
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388230"
---
# <a name="use-the-iorganization-web-service-in-a-custom-workflow-activity"></a><span data-ttu-id="b8058-103">Use the IOrganization web service in a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="b8058-103">Use the IOrganization web service in a custom workflow activity</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b8058-104">To call [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement organization web service methods from within a custom workflow activity, you must first obtain a reference to the web service.</span><span class="sxs-lookup"><span data-stu-id="b8058-104">To call [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement organization web service methods from within a custom workflow activity, you must first obtain a reference to the web service.</span></span> <span data-ttu-id="b8058-105">This is described in the following procedure and sample code.</span><span class="sxs-lookup"><span data-stu-id="b8058-105">This is described in the following procedure and sample code.</span></span>  
  
1.  <span data-ttu-id="b8058-106">Get a reference to <xref:Microsoft.Xrm.Sdk.IOrganizationServiceFactory>.</span><span class="sxs-lookup"><span data-stu-id="b8058-106">Get a reference to <xref:Microsoft.Xrm.Sdk.IOrganizationServiceFactory>.</span></span>  
  
2.  <span data-ttu-id="b8058-107">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationServiceFactory>.<xref:Microsoft.Xrm.Sdk.IOrganizationServiceFactory.CreateOrganizationService(System.Nullable{System.Guid})></span><span class="sxs-lookup"><span data-stu-id="b8058-107">Use the <xref:Microsoft.Xrm.Sdk.IOrganizationServiceFactory>.<xref:Microsoft.Xrm.Sdk.IOrganizationServiceFactory.CreateOrganizationService(System.Nullable{System.Guid})></span></span> <span data-ttu-id="b8058-108">method to create an instance of<xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span><span class="sxs-lookup"><span data-stu-id="b8058-108">method to create an instance of<xref:Microsoft.Xrm.Sdk.IOrganizationService>.</span></span>  
  
3.  <span data-ttu-id="b8058-109">Use the<xref:Microsoft.Xrm.Sdk.IOrganizationService> instance to call the supported methods.</span><span class="sxs-lookup"><span data-stu-id="b8058-109">Use the<xref:Microsoft.Xrm.Sdk.IOrganizationService> instance to call the supported methods.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b8058-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="b8058-110">Example</span></span>  

 <span data-ttu-id="b8058-111">The following sample shows how to get the<xref:Microsoft.Xrm.Sdk.IOrganizationService> from within the `Execute` method of your custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="b8058-111">The following sample shows how to get the<xref:Microsoft.Xrm.Sdk.IOrganizationService> from within the `Execute` method of your custom workflow activity.</span></span>  
  
```csharp  
  
protected override void Execute(CodeActivityContext executionContext)  
{  
   // Get the context service.  
   IWorkflowContext context = executionContext.GetExtension<IWorkflowContext>();  
   IOrganizationServiceFactory serviceFactory = executionContext.GetExtension<IOrganizationServiceFactory>();  
  
   // Use the context service to create an instance of IOrganizationService.  
   IOrganizationService _orgService = serviceFactory.CreateOrganizationService(context.InitiatingUserId);  
  
   // Use the service reference to call web methods.  
   _orgService.Execute(…);  
}  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="b8058-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b8058-112">See also</span></span>  

 <span data-ttu-id="b8058-113">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="b8058-113">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span></span>  
 <span data-ttu-id="b8058-114">[Register and use a custom workflow activity assembly](register-use-custom-workflow-activity-assembly.md) </span><span class="sxs-lookup"><span data-stu-id="b8058-114">[Register and use a custom workflow activity assembly](register-use-custom-workflow-activity-assembly.md) </span></span>  
 <span data-ttu-id="b8058-115">[Sample: Create a Custom Workflow Activity](sample-create-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="b8058-115">[Sample: Create a Custom Workflow Activity](sample-create-custom-workflow-activity.md) </span></span>  
 <span data-ttu-id="b8058-116">[IOrganizationService Web Service](../org-service/use-organization-service-read-write-data-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="b8058-116">[IOrganizationService Web Service](../org-service/use-organization-service-read-write-data-metadata.md) </span></span>  
 <span data-ttu-id="b8058-117">[Organization service methods](../org-service/organization-service-methods.md) </span><span class="sxs-lookup"><span data-stu-id="b8058-117">[Organization service methods](../org-service/organization-service-methods.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Workflow.IWorkflowContext>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationServiceFactory>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService>
