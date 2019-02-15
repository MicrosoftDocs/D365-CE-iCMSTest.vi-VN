---
title: Configure Azure integration with Dynamics 365 for Customer Engagement apps (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The topic describes configuring Azure integration with Dynamics 365 for Customer Engagement apps.
ms.custom: ''
ms.date: 05/16/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 79e49782-edd1-41ef-b110-2c2ed0771058
caps.latest.revision: 62
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 74e203fc9a40aa5723f0491b186ea5b5990cd349
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388205"
---
# <a name="configure-azure-integration-with-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="0a917-103">Configure Azure integration with Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="0a917-103">Configure Azure integration with Dynamics 365 for Customer Engagement apps</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0a917-104">You can post the message request data for the current core operation to cloud hosted applications listening on the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span><span class="sxs-lookup"><span data-stu-id="0a917-104">You can post the message request data for the current core operation to cloud hosted applications listening on the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span></span> <span data-ttu-id="0a917-105">To enable this capability in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, perform the tasks detailed in this topic.</span><span class="sxs-lookup"><span data-stu-id="0a917-105">To enable this capability in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, perform the tasks detailed in this topic.</span></span>  

> [!NOTE]
> <span data-ttu-id="0a917-106">These instructions apply to Online deployments only.</span><span class="sxs-lookup"><span data-stu-id="0a917-106">These instructions apply to Online deployments only.</span></span> <span data-ttu-id="0a917-107">For on-premises deployments, see documentation for the most recent on-premises release at [Dynamics CRM 2016 SDK: Configure Azure integration with Microsoft Dynamics 365 for Customer Engagement aps](https://msdn.microsoft.com/library/gg309340.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a917-107">For on-premises deployments, see documentation for the most recent on-premises release at [Dynamics CRM 2016 SDK: Configure Azure integration with Microsoft Dynamics 365 for Customer Engagement aps](https://msdn.microsoft.com/library/gg309340.aspx)</span></span>
  

<a name="bkmk_configureappfabric"></a>
   
## <a name="configure-azure-for-includepndynamicscrmincludespn-dynamics-crmmd-integration"></a><span data-ttu-id="0a917-108">Configure Azure For [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] integration</span><span class="sxs-lookup"><span data-stu-id="0a917-108">Configure Azure For [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] integration</span></span>

<span data-ttu-id="0a917-109">When you use SAS for authorization, you need to configure the rules and issuers of your [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] solution to allow a listener application to read the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps message posted to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span><span class="sxs-lookup"><span data-stu-id="0a917-109">When you use SAS for authorization, you need to configure the rules and issuers of your [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] solution to allow a listener application to read the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps message posted to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span></span> <span data-ttu-id="0a917-110">In addition, you must configure the service bus rules to accept the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps issuer claim.</span><span class="sxs-lookup"><span data-stu-id="0a917-110">In addition, you must configure the service bus rules to accept the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps issuer claim.</span></span> <span data-ttu-id="0a917-111">The recommended method to configure [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] is to use the Plug-in Registration Tool.</span><span class="sxs-lookup"><span data-stu-id="0a917-111">The recommended method to configure [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] is to use the Plug-in Registration Tool.</span></span>  
  
<span data-ttu-id="0a917-112">For instructions on configuring authorization see [Walkthrough: Configure Microsoft Azure (SAS) for integration with Dynamics 365 for Customer Engagement apps](walkthrough-configure-azure-sas-integration.md).</span><span class="sxs-lookup"><span data-stu-id="0a917-112">For instructions on configuring authorization see [Walkthrough: Configure Microsoft Azure (SAS) for integration with Dynamics 365 for Customer Engagement apps](walkthrough-configure-azure-sas-integration.md).</span></span>  

## <a name="test-configuration"></a><span data-ttu-id="0a917-113">Test Configuration</span><span class="sxs-lookup"><span data-stu-id="0a917-113">Test Configuration</span></span>

<span data-ttu-id="0a917-114">After configuring [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] integration, you will need to perform these additional tasks.</span><span class="sxs-lookup"><span data-stu-id="0a917-114">After configuring [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] integration, you will need to perform these additional tasks.</span></span>  
  
1. <span data-ttu-id="0a917-115">Write and register a listener application with a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] solution endpoint.</span><span class="sxs-lookup"><span data-stu-id="0a917-115">Write and register a listener application with a [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] solution endpoint.</span></span> <span data-ttu-id="0a917-116">For more information, see the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] [documentation](https://azure.microsoft.com/en-us/documentation/articles/service-bus-fundamentals-hybrid-solutions/).</span><span class="sxs-lookup"><span data-stu-id="0a917-116">For more information, see the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] [documentation](https://azure.microsoft.com/en-us/documentation/articles/service-bus-fundamentals-hybrid-solutions/).</span></span>  
  
2. <span data-ttu-id="0a917-117">Register a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] aware plug-in or a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] aware custom workflow activity with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="0a917-117">Register a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] aware plug-in or a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] aware custom workflow activity with [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0a917-118">[Walkthrough: Register an Azure-aware Plug-in with Plug-in Registration Tool](walkthrough-register-azure-aware-plug-in-using-plug-in-registration-tool.md)</span><span class="sxs-lookup"><span data-stu-id="0a917-118">[Walkthrough: Register an Azure-aware Plug-in with Plug-in Registration Tool](walkthrough-register-azure-aware-plug-in-using-plug-in-registration-tool.md)</span></span>  
  
3. <span data-ttu-id="0a917-119">Perform the necessary [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps operation that triggers the plug-in or custom workflow activity to run.</span><span class="sxs-lookup"><span data-stu-id="0a917-119">Perform the necessary [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps operation that triggers the plug-in or custom workflow activity to run.</span></span>  
  
<span data-ttu-id="0a917-120">If all of the preceding steps were performed correctly, a message containing the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data context should be sent to a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] queue or topic and ultimately received by the listener application.</span><span class="sxs-lookup"><span data-stu-id="0a917-120">If all of the preceding steps were performed correctly, a message containing the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data context should be sent to a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] queue or topic and ultimately received by the listener application.</span></span> <span data-ttu-id="0a917-121">You can navigate to the **System Jobs** grid in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application and check the status of the related System Job to see if the post to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] succeeded.</span><span class="sxs-lookup"><span data-stu-id="0a917-121">You can navigate to the **System Jobs** grid in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application and check the status of the related System Job to see if the post to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] succeeded.</span></span> <span data-ttu-id="0a917-122">In case of errors, the message section of the System Job displays the error details.</span><span class="sxs-lookup"><span data-stu-id="0a917-122">In case of errors, the message section of the System Job displays the error details.</span></span>  
 
  
<!-- 
The following information is for on-premises only.
TODO: Review and add back relevant content when a v9 on-premise release ships

<a name="bkmk_obtain"></a>

## Get a public certificate

[!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] users can download a public certificate from the web application by going to **Settings** > **Customizations** > **Developer Resources**. On that page, click the **Download Certificate** link below **Microsoft Azure Issuer Certificate** to download and save the public certificate. In addition, write down the issuer name because you’ll need it later.  
  
For [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] on-premises and IFD installations, you can purchase a private certificate from an issuing authority. Import the certificate file into the Personal\Certificates store on your computer using the certificate [!INCLUDE[pn_Microsoft_Management_Console](../includes/pn-microsoft-management-console.md)] snap-in. Next, export a public key file of your certificate in Base64 format. This public certificate will be used in the next task. For more information, see the MMC Help.  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)]

<a name="bkmk_configurecrm"></a>

## Configure [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps for Azure integration
  
For [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] on-premises and IFD deployments, configuring the server for [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] integration involves storing the public certificate in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps configuration database and setting the proper security access to the certificate so [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps can read it. [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] comes pre-configured to work with [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)].
  
> [!IMPORTANT]
>  For the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] and [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] integration feature to work, the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps asynchronous service must have access to the Internet through the server’s firewall. The server where the Asynchronous Service role is installed must be exposed to the Internet, and the account that the service runs under must have Internet access. Only outbound connections on ports 80 and 443 are required. Inbound connection access is not required. Use the Windows Firewall control panel to enable outbound connections for the `CrmAsyncService.exe` application located on the server in the `%PROGRAMFILES%\Microsoft Dynamics CRM\Server\bin` folder.   -->
  

  
### <a name="see-also"></a><span data-ttu-id="0a917-123">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0a917-123">See also</span></span>

[<span data-ttu-id="0a917-124">Azure Extensions for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="0a917-124">Azure Extensions for Dynamics 365 for Customer Engagement apps</span></span>](azure-extensions.md)<br />
[<span data-ttu-id="0a917-125">Writing a Plug-in</span><span class="sxs-lookup"><span data-stu-id="0a917-125">Writing a Plug-in</span></span>](write-plugin.md)<br />
[<span data-ttu-id="0a917-126">Using the Provided Azure Plug-in</span><span class="sxs-lookup"><span data-stu-id="0a917-126">Using the Provided Azure Plug-in</span></span>](work-data-azure-solution.md)<br />
[<span data-ttu-id="0a917-127">Writing a Listener for a Azure Solution</span><span class="sxs-lookup"><span data-stu-id="0a917-127">Writing a Listener for a Azure Solution</span></span>](write-listener-application-azure-solution.md)<br />
[<span data-ttu-id="0a917-128">Azure Platform – Getting Started</span><span class="sxs-lookup"><span data-stu-id="0a917-128">Azure Platform – Getting Started</span></span>](http://www.microsoft.com/windowsazure/learn/get-started/)
