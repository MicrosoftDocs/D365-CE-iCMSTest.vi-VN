---
title: Types of HAT automation activities in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about various automation activities that you can use to automate your hosted applications in Unified Service Desk.
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
ms.assetid: 3a4fa988-8eaf-4039-9296-905436f6a706
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 39156e897b77f435fc5a7f4f41fccc18ef387bd9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387970"
---
# <a name="types-of-hat-automation-activities-in-unified-service-desk"></a><span data-ttu-id="05a37-103">Types of HAT automation activities in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="05a37-103">Types of HAT automation activities in Unified Service Desk</span></span>
<span data-ttu-id="05a37-104">There are various types of [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] automation activities that you can use to automate your hosted applications.</span><span class="sxs-lookup"><span data-stu-id="05a37-104">There are various types of [!INCLUDE[pn_hosted_application_toolkit_hat](../includes/pn-hosted-application-toolkit-hat.md)] automation activities that you can use to automate your hosted applications.</span></span> <span data-ttu-id="05a37-105">To view and use the [!INCLUDE[pn_hat](../includes/pn-hat.md)] automation activities, see [Use HAT automation activities](../unified-service-desk/use-hat-automation-activities.md).</span><span class="sxs-lookup"><span data-stu-id="05a37-105">To view and use the [!INCLUDE[pn_hat](../includes/pn-hat.md)] automation activities, see [Use HAT automation activities](../unified-service-desk/use-hat-automation-activities.md).</span></span>  
  
<a name="AIF"></a>   
## <a name="application-integration-framework-aif-action-activities"></a><span data-ttu-id="05a37-106">Application Integration Framework (AIF) action activities</span><span class="sxs-lookup"><span data-stu-id="05a37-106">Application Integration Framework (AIF) action activities</span></span>  
 <span data-ttu-id="05a37-107">Action activities provide functionality to access and manage [UII actions](../unified-service-desk/uii-actions.md).</span><span class="sxs-lookup"><span data-stu-id="05a37-107">Action activities provide functionality to access and manage [UII actions](../unified-service-desk/uii-actions.md).</span></span> <span data-ttu-id="05a37-108">Here are the various action activities available.</span><span class="sxs-lookup"><span data-stu-id="05a37-108">Here are the various action activities available.</span></span>  
  
 `DoAction`  
 <span data-ttu-id="05a37-109">Executes an action either in the same application or in another hosted application.</span><span class="sxs-lookup"><span data-stu-id="05a37-109">Executes an action either in the same application or in another hosted application.</span></span> <span data-ttu-id="05a37-110">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-110">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-111">`ApplicationName`: The application on which to execute the `DoAction`.</span><span class="sxs-lookup"><span data-stu-id="05a37-111">`ApplicationName`: The application on which to execute the `DoAction`.</span></span> <span data-ttu-id="05a37-112">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="05a37-112">Mandatory.</span></span>  
  
- <span data-ttu-id="05a37-113">`ActionData`: Data required for performing the action.</span><span class="sxs-lookup"><span data-stu-id="05a37-113">`ActionData`: Data required for performing the action.</span></span> <span data-ttu-id="05a37-114">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="05a37-114">Optional.</span></span>  
  
- <span data-ttu-id="05a37-115">**ActionName** Name of the action that is registered with the hosted application specified in the `ApplicationName` property.</span><span class="sxs-lookup"><span data-stu-id="05a37-115">**ActionName** Name of the action that is registered with the hosted application specified in the `ApplicationName` property.</span></span> <span data-ttu-id="05a37-116">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="05a37-116">Mandatory.</span></span>  
  
  `GetActionData`  
  <span data-ttu-id="05a37-117">Retrieves the data from the action that invoked the workflow or automation.</span><span class="sxs-lookup"><span data-stu-id="05a37-117">Retrieves the data from the action that invoked the workflow or automation.</span></span> <span data-ttu-id="05a37-118">The value will be returned in the `ActionData` property.</span><span class="sxs-lookup"><span data-stu-id="05a37-118">The value will be returned in the `ActionData` property.</span></span>  
  
  `SetActionData`  
  <span data-ttu-id="05a37-119">Adds data to the current action.</span><span class="sxs-lookup"><span data-stu-id="05a37-119">Adds data to the current action.</span></span>  
  
  <span data-ttu-id="05a37-120">Specify the data that is required for the action in the `ActionData` parameter.</span><span class="sxs-lookup"><span data-stu-id="05a37-120">Specify the data that is required for the action in the `ActionData` parameter.</span></span>  
  
  `RegisterActionForEvent`  
  <span data-ttu-id="05a37-121">Registers an action to be initiated every time an event occurs.</span><span class="sxs-lookup"><span data-stu-id="05a37-121">Registers an action to be initiated every time an event occurs.</span></span> <span data-ttu-id="05a37-122">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-122">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-123">`ActionApplication`: Name of the application with which the UII action is registered.</span><span class="sxs-lookup"><span data-stu-id="05a37-123">`ActionApplication`: Name of the application with which the UII action is registered.</span></span> <span data-ttu-id="05a37-124">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="05a37-124">Mandatory.</span></span>  
  
- <span data-ttu-id="05a37-125">`ActionName`: Name of the action for the application that will be executed when the event is initiated.</span><span class="sxs-lookup"><span data-stu-id="05a37-125">`ActionName`: Name of the action for the application that will be executed when the event is initiated.</span></span> <span data-ttu-id="05a37-126">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="05a37-126">Mandatory.</span></span>  
  
- <span data-ttu-id="05a37-127">`ApplicationName`: Name of the application that initiates the event.</span><span class="sxs-lookup"><span data-stu-id="05a37-127">`ApplicationName`: Name of the application that initiates the event.</span></span> <span data-ttu-id="05a37-128">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="05a37-128">Mandatory.</span></span>  
  
- <span data-ttu-id="05a37-129">`ControlName`: Name of the control that initiates the event.</span><span class="sxs-lookup"><span data-stu-id="05a37-129">`ControlName`: Name of the control that initiates the event.</span></span> <span data-ttu-id="05a37-130">Tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="05a37-130">Optional.</span></span>  
  
- <span data-ttu-id="05a37-131">`EventName`: Name of the event initiated by the application/control.</span><span class="sxs-lookup"><span data-stu-id="05a37-131">`EventName`: Name of the event initiated by the application/control.</span></span>  
  
  `UnRegisterActionForEvent`  
  <span data-ttu-id="05a37-132">Unregisters an action that was previously registered using the `RegisterActionForEvent` activity.</span><span class="sxs-lookup"><span data-stu-id="05a37-132">Unregisters an action that was previously registered using the `RegisterActionForEvent` activity.</span></span> <span data-ttu-id="05a37-133">The unregistered event won’t be executed anymore.</span><span class="sxs-lookup"><span data-stu-id="05a37-133">The unregistered event won’t be executed anymore.</span></span> <span data-ttu-id="05a37-134">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-134">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-135">`ActionApplicationName`: Name of the application with which the UII action is registered.</span><span class="sxs-lookup"><span data-stu-id="05a37-135">`ActionApplicationName`: Name of the application with which the UII action is registered.</span></span>  
  
- <span data-ttu-id="05a37-136">`ActionName`: Name of the action for the application that would have executed when the event was initiated.</span><span class="sxs-lookup"><span data-stu-id="05a37-136">`ActionName`: Name of the action for the application that would have executed when the event was initiated.</span></span>  
  
- <span data-ttu-id="05a37-137">`ApplicationName`: Name of the application that initiates the event.</span><span class="sxs-lookup"><span data-stu-id="05a37-137">`ApplicationName`: Name of the application that initiates the event.</span></span>  
  
- <span data-ttu-id="05a37-138">`ControlName`: Name of the control that initiates the event.</span><span class="sxs-lookup"><span data-stu-id="05a37-138">`ControlName`: Name of the control that initiates the event.</span></span>  
  
- <span data-ttu-id="05a37-139">`EventName`: Name of the event initiated by the application or control.</span><span class="sxs-lookup"><span data-stu-id="05a37-139">`EventName`: Name of the event initiated by the application or control.</span></span>  
  
  `CloseDynamicApp`  
  <span data-ttu-id="05a37-140">Closes a dynamic hosted application from within the automation.</span><span class="sxs-lookup"><span data-stu-id="05a37-140">Closes a dynamic hosted application from within the automation.</span></span> <span data-ttu-id="05a37-141">You can use this action to programmatically close a dynamic hosted application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="05a37-141">You can use this action to programmatically close a dynamic hosted application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
  <span data-ttu-id="05a37-142">Specify the name of the dynamic hosted application in the `ApplicationName` parameter that you want to close.</span><span class="sxs-lookup"><span data-stu-id="05a37-142">Specify the name of the dynamic hosted application in the `ApplicationName` parameter that you want to close.</span></span>  
  
  <span data-ttu-id="05a37-143">For more information about dynamic hosted applications, see [Dynamic UII hosted applications](../unified-service-desk/uii-hosted-applications.md#Dynamic).</span><span class="sxs-lookup"><span data-stu-id="05a37-143">For more information about dynamic hosted applications, see [Dynamic UII hosted applications](../unified-service-desk/uii-hosted-applications.md#Dynamic).</span></span>  
  
  `StartDynamicApp`  
  <span data-ttu-id="05a37-144">Starts a dynamic hosted application from within the automation.</span><span class="sxs-lookup"><span data-stu-id="05a37-144">Starts a dynamic hosted application from within the automation.</span></span>  
  
  <span data-ttu-id="05a37-145">Specify the name of the dynamic hosted application in the `ApplicationName` parameter that you want to start.</span><span class="sxs-lookup"><span data-stu-id="05a37-145">Specify the name of the dynamic hosted application in the `ApplicationName` parameter that you want to start.</span></span>  
  
  `FocusApp`  
  <span data-ttu-id="05a37-146">Sets focus on an application from within the automation.</span><span class="sxs-lookup"><span data-stu-id="05a37-146">Sets focus on an application from within the automation.</span></span>  
  
  <span data-ttu-id="05a37-147">Specify the name of the hosted application in the `ApplicationName` parameter that you want to set focus on.</span><span class="sxs-lookup"><span data-stu-id="05a37-147">Specify the name of the hosted application in the `ApplicationName` parameter that you want to set focus on.</span></span>  
  
<a name="AIFContext"></a>   
## <a name="aif-context-activities"></a><span data-ttu-id="05a37-148">AIF context activities</span><span class="sxs-lookup"><span data-stu-id="05a37-148">AIF context activities</span></span>  
 <span data-ttu-id="05a37-149">Context activities allow accessing the AIF context from the automation.</span><span class="sxs-lookup"><span data-stu-id="05a37-149">Context activities allow accessing the AIF context from the automation.</span></span> <span data-ttu-id="05a37-150">Here are the various context activities available.</span><span class="sxs-lookup"><span data-stu-id="05a37-150">Here are the various context activities available.</span></span>  
  
 `GetContext`  
 <span data-ttu-id="05a37-151">Retrieves a value for the specified key from the context.</span><span class="sxs-lookup"><span data-stu-id="05a37-151">Retrieves a value for the specified key from the context.</span></span> <span data-ttu-id="05a37-152">The value is returned in the `ContextValue` property.</span><span class="sxs-lookup"><span data-stu-id="05a37-152">The value is returned in the `ContextValue` property.</span></span>  
  
 <span data-ttu-id="05a37-153">Specify the key of the context to be retrieved in the `ContextKey` property.</span><span class="sxs-lookup"><span data-stu-id="05a37-153">Specify the key of the context to be retrieved in the `ContextKey` property.</span></span>  
  
 `SetContext`  
 <span data-ttu-id="05a37-154">Sets the value for the specified key in the context.</span><span class="sxs-lookup"><span data-stu-id="05a37-154">Sets the value for the specified key in the context.</span></span> <span data-ttu-id="05a37-155">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-155">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-156">`ContextKey`: Key of the context to be set.</span><span class="sxs-lookup"><span data-stu-id="05a37-156">`ContextKey`: Key of the context to be set.</span></span>  
  
- <span data-ttu-id="05a37-157">`ContextData`: Optionally, enter the data to be set to the context specified in `ContextKey`.</span><span class="sxs-lookup"><span data-stu-id="05a37-157">`ContextData`: Optionally, enter the data to be set to the context specified in `ContextKey`.</span></span>  
  
  `GetCredential`  
  <span data-ttu-id="05a37-158">Retrieves user credentials from the context for the specified application.</span><span class="sxs-lookup"><span data-stu-id="05a37-158">Retrieves user credentials from the context for the specified application.</span></span> <span data-ttu-id="05a37-159">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-159">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-160">`ApplicationName`: Name of the application.</span><span class="sxs-lookup"><span data-stu-id="05a37-160">`ApplicationName`: Name of the application.</span></span>  
  
- <span data-ttu-id="05a37-161">`UserName`: User name.</span><span class="sxs-lookup"><span data-stu-id="05a37-161">`UserName`: User name.</span></span>  
  
- <span data-ttu-id="05a37-162">`Password`:  Password.</span><span class="sxs-lookup"><span data-stu-id="05a37-162">`Password`:  Password.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="05a37-163">To retrieve the credentials from a custom store, the developer needs to provide a class that implements the [Microsoft.Uii.AifServices.ISsoLookupService](https://docs.microsoft.com/dotnet/api/Microsoft.Uii.AifServices.ISsoLookupService) interface.</span><span class="sxs-lookup"><span data-stu-id="05a37-163">To retrieve the credentials from a custom store, the developer needs to provide a class that implements the [Microsoft.Uii.AifServices.ISsoLookupService](https://docs.microsoft.com/dotnet/api/Microsoft.Uii.AifServices.ISsoLookupService) interface.</span></span>  
  
 `HostApplication`  
 <span data-ttu-id="05a37-164">Hosts the UI of the application.</span><span class="sxs-lookup"><span data-stu-id="05a37-164">Hosts the UI of the application.</span></span> <span data-ttu-id="05a37-165">It uses the **Application Hosting** configuration data specified while configuring the hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] on the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server to determine the hosting mode.</span><span class="sxs-lookup"><span data-stu-id="05a37-165">It uses the **Application Hosting** configuration data specified while configuring the hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] on the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server to determine the hosting mode.</span></span> <span data-ttu-id="05a37-166">For more information about specifying the hosting mode for an application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Create and manage UII hosted applications](../unified-service-desk/create-manage-uii-hosted-applications.md).</span><span class="sxs-lookup"><span data-stu-id="05a37-166">For more information about specifying the hosting mode for an application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Create and manage UII hosted applications](../unified-service-desk/create-manage-uii-hosted-applications.md).</span></span>  
  
<a name="DDA"></a>   
## <a name="dda-activities"></a><span data-ttu-id="05a37-167">DDA activities</span><span class="sxs-lookup"><span data-stu-id="05a37-167">DDA activities</span></span>  
 <span data-ttu-id="05a37-168">Data-driven adapter (DDA) activities provide access to controls specified in the bindings.</span><span class="sxs-lookup"><span data-stu-id="05a37-168">Data-driven adapter (DDA) activities provide access to controls specified in the bindings.</span></span> <span data-ttu-id="05a37-169">Here are the various DDA activities.</span><span class="sxs-lookup"><span data-stu-id="05a37-169">Here are the various DDA activities.</span></span>  
  
 `Audit`  
 <span data-ttu-id="05a37-170">Creates audit entries from within the automation.</span><span class="sxs-lookup"><span data-stu-id="05a37-170">Creates audit entries from within the automation.</span></span> <span data-ttu-id="05a37-171">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-171">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-172">`Audit Flag`: Name of the audit flag.</span><span class="sxs-lookup"><span data-stu-id="05a37-172">`Audit Flag`: Name of the audit flag.</span></span>  
  
- <span data-ttu-id="05a37-173">`Log data`: Value of the audit flag value.</span><span class="sxs-lookup"><span data-stu-id="05a37-173">`Log data`: Value of the audit flag value.</span></span>  
  
  <span data-ttu-id="05a37-174">For information about various audit flags in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Configure auditing and diagnostics in Unified Service Desk](../unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="05a37-174">For information about various audit flags in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Configure auditing and diagnostics in Unified Service Desk](../unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk.md).</span></span>  
  
  `ControlFinder`  
  <span data-ttu-id="05a37-175">Locates a control in the hosted application.</span><span class="sxs-lookup"><span data-stu-id="05a37-175">Locates a control in the hosted application.</span></span> <span data-ttu-id="05a37-176">The action returns `True` if the control is found in the `ControlFound` property; otherwise, returns `False`.</span><span class="sxs-lookup"><span data-stu-id="05a37-176">The action returns `True` if the control is found in the `ControlFound` property; otherwise, returns `False`.</span></span> <span data-ttu-id="05a37-177">You can set the `ExceptionsMask` property if you want to use the exception handler to execute depending activities.</span><span class="sxs-lookup"><span data-stu-id="05a37-177">You can set the `ExceptionsMask` property if you want to use the exception handler to execute depending activities.</span></span> <span data-ttu-id="05a37-178">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-178">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-179">`ApplicationName`: Name of the application that hosts the control.</span><span class="sxs-lookup"><span data-stu-id="05a37-179">`ApplicationName`: Name of the application that hosts the control.</span></span> <span data-ttu-id="05a37-180">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="05a37-180">Mandatory.</span></span>  
  
- <span data-ttu-id="05a37-181">`ControlName`: Name of the control in the application.</span><span class="sxs-lookup"><span data-stu-id="05a37-181">`ControlName`: Name of the control in the application.</span></span>  
  
- <span data-ttu-id="05a37-182">`ExceptionsMask`: Indicates whether you want to show an exception if the control isn’t found.</span><span class="sxs-lookup"><span data-stu-id="05a37-182">`ExceptionsMask`: Indicates whether you want to show an exception if the control isn’t found.</span></span> <span data-ttu-id="05a37-183">The default setting is `False`.</span><span class="sxs-lookup"><span data-stu-id="05a37-183">The default setting is `False`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="05a37-184">If a workflow that you configured is blocking the UI thread and you have specified SleepInterval and Timeout parameters for the `ControlFinder` activity, the action should be configured to run asynchronously.</span><span class="sxs-lookup"><span data-stu-id="05a37-184">If a workflow that you configured is blocking the UI thread and you have specified SleepInterval and Timeout parameters for the `ControlFinder` activity, the action should be configured to run asynchronously.</span></span>  
  
 `ExecuteControlAction`  
 <span data-ttu-id="05a37-185">Executes the default action of a control.</span><span class="sxs-lookup"><span data-stu-id="05a37-185">Executes the default action of a control.</span></span> <span data-ttu-id="05a37-186">For example, if the control is a button, the default action is click.</span><span class="sxs-lookup"><span data-stu-id="05a37-186">For example, if the control is a button, the default action is click.</span></span> <span data-ttu-id="05a37-187">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-187">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-188">`ApplicationName`: Name of the application that hosts the control.</span><span class="sxs-lookup"><span data-stu-id="05a37-188">`ApplicationName`: Name of the application that hosts the control.</span></span>  
  
- <span data-ttu-id="05a37-189">`ControlName`: Name of the control in the application.</span><span class="sxs-lookup"><span data-stu-id="05a37-189">`ControlName`: Name of the control in the application.</span></span>  
  
  `GetControlValue`  
  <span data-ttu-id="05a37-190">Retrieves a value from a control in the application.</span><span class="sxs-lookup"><span data-stu-id="05a37-190">Retrieves a value from a control in the application.</span></span> <span data-ttu-id="05a37-191">The value is returned in the `ControlValue` property.</span><span class="sxs-lookup"><span data-stu-id="05a37-191">The value is returned in the `ControlValue` property.</span></span> <span data-ttu-id="05a37-192">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-192">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-193">`ApplicationName`: Name of the application that hosts the control.</span><span class="sxs-lookup"><span data-stu-id="05a37-193">`ApplicationName`: Name of the application that hosts the control.</span></span>  
  
- <span data-ttu-id="05a37-194">`ControlName`: Name of the control in the application whose value has to be retrieved.</span><span class="sxs-lookup"><span data-stu-id="05a37-194">`ControlName`: Name of the control in the application whose value has to be retrieved.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="05a37-195">When using the `GetControlValue` activity with a multi-line text control, all new line characters will be ignored and a single string is returned.</span><span class="sxs-lookup"><span data-stu-id="05a37-195">When using the `GetControlValue` activity with a multi-line text control, all new line characters will be ignored and a single string is returned.</span></span>  
  
 `SetControlValue`  
 <span data-ttu-id="05a37-196">Sets the value of a control in the application.</span><span class="sxs-lookup"><span data-stu-id="05a37-196">Sets the value of a control in the application.</span></span> <span data-ttu-id="05a37-197">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-197">This action has the following properties:</span></span>  
  
-   <span data-ttu-id="05a37-198">`ApplicationName`: Name of the application that hosts the control.</span><span class="sxs-lookup"><span data-stu-id="05a37-198">`ApplicationName`: Name of the application that hosts the control.</span></span>  
  
-   <span data-ttu-id="05a37-199">`ControlName`: Name of the control in the application whose value has to be set.</span><span class="sxs-lookup"><span data-stu-id="05a37-199">`ControlName`: Name of the control in the application whose value has to be set.</span></span>  
  
-   <span data-ttu-id="05a37-200">`ControlValue`: Enter the value to be set.</span><span class="sxs-lookup"><span data-stu-id="05a37-200">`ControlValue`: Enter the value to be set.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="05a37-201">When using the `SetControlValue` activity with a multi-line text control, all new line characters will be ignored and a single string is returned.</span><span class="sxs-lookup"><span data-stu-id="05a37-201">When using the `SetControlValue` activity with a multi-line text control, all new line characters will be ignored and a single string is returned.</span></span>  
  
 `Navigate`  
 <span data-ttu-id="05a37-202">Specifies a URL that a web application navigates to.</span><span class="sxs-lookup"><span data-stu-id="05a37-202">Specifies a URL that a web application navigates to.</span></span> <span data-ttu-id="05a37-203">For example, you can use the `Navigate` activity to force a web application to navigate to a specific URL when a user performs a task.</span><span class="sxs-lookup"><span data-stu-id="05a37-203">For example, you can use the `Navigate` activity to force a web application to navigate to a specific URL when a user performs a task.</span></span> <span data-ttu-id="05a37-204">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-204">This action has the following properties:</span></span>  
  
-   <span data-ttu-id="05a37-205">`ApplicationName`: Name of the application that hosts the control.</span><span class="sxs-lookup"><span data-stu-id="05a37-205">`ApplicationName`: Name of the application that hosts the control.</span></span>  
  
-   <span data-ttu-id="05a37-206">`URL`: Specify the URL along with the query string.</span><span class="sxs-lookup"><span data-stu-id="05a37-206">`URL`: Specify the URL along with the query string.</span></span>  
  
> [!NOTE]
> - <span data-ttu-id="05a37-207">The `Navigate` activity shouldn’t be called concurrently on the web browser.</span><span class="sxs-lookup"><span data-stu-id="05a37-207">The `Navigate` activity shouldn’t be called concurrently on the web browser.</span></span> <span data-ttu-id="05a37-208">If it is, you’ll receive the following errors:</span><span class="sxs-lookup"><span data-stu-id="05a37-208">If it is, you’ll receive the following errors:</span></span>  
> 
>   ```Output  
>   AutomationAdapter (app=Contact,action=__SetControlValue__): Posted implicit action exception:  Microsoft.Uii.HostedApplicationToolkit.DataDrivenAdapter.DataDrivenAdapterException: DDA0301: Web browser is busy and cannot be stopped.   
> 
>   WF/Automation <GUID> exception: Microsoft.Uii.HostedApplicationToolkit.DataDrivenAdapter.DataDrivenAdapterException: DDA0301: Web browser is busy and cannot be stopped.  
>   ```  
>   - <span data-ttu-id="05a37-209">For the `Navigate` activity to work on the target application, you must configure the hosted application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to use **Automation Adapter (HAT)**, and provide the following binding in the Automation XML field:</span><span class="sxs-lookup"><span data-stu-id="05a37-209">For the `Navigate` activity to work on the target application, you must configure the hosted application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to use **Automation Adapter (HAT)**, and provide the following binding in the Automation XML field:</span></span>  
> 
>   ```  
>   <DataDrivenAdapterBindingsCollection>  
>     <DataDrivenAdapterBindings>  
>        <Type>Microsoft.Uii.HostedApplicationToolkit.DataDrivenAdapter.WebDataDrivenAdapter, Microsoft.Uii.HostedApplicationToolkit.DataDrivenAdapter</Type>  
>        <Controls/>  
>     </DataDrivenAdapterBindings>  
>   </DataDrivenAdapterBindingsCollection>  
>   ```  
> 
>   <span data-ttu-id="05a37-210">For more information about configuring hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Create and manage UII hosted applications](../unified-service-desk/create-manage-uii-hosted-applications.md).</span><span class="sxs-lookup"><span data-stu-id="05a37-210">For more information about configuring hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Create and manage UII hosted applications](../unified-service-desk/create-manage-uii-hosted-applications.md).</span></span>  
  
 `ConfigReader`  
 <span data-ttu-id="05a37-211">Reads a configuration value from within the automation.</span><span class="sxs-lookup"><span data-stu-id="05a37-211">Reads a configuration value from within the automation.</span></span> <span data-ttu-id="05a37-212">This activity will either read configuration from the **Option** settings in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] or the application configuration file.</span><span class="sxs-lookup"><span data-stu-id="05a37-212">This activity will either read configuration from the **Option** settings in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] or the application configuration file.</span></span> <span data-ttu-id="05a37-213">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-213">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-214">`OptionKey` as string: Used to read the **Option** setting from [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="05a37-214">`OptionKey` as string: Used to read the **Option** setting from [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="05a37-215">For more information about various options, see [Manage Options for Unified Service Desk](../unified-service-desk/admin/manage-options-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="05a37-215">For more information about various options, see [Manage Options for Unified Service Desk](../unified-service-desk/admin/manage-options-unified-service-desk.md).</span></span>  
  
- <span data-ttu-id="05a37-216">`XPath` as string: Used to read the application configuration file.</span><span class="sxs-lookup"><span data-stu-id="05a37-216">`XPath` as string: Used to read the application configuration file.</span></span>  
  
- <span data-ttu-id="05a37-217">`QueryResult` as string: Result of the search.</span><span class="sxs-lookup"><span data-stu-id="05a37-217">`QueryResult` as string: Result of the search.</span></span>  
  
  `InitstringReader`  
  <span data-ttu-id="05a37-218">Enables you to read the `InitString` content from within the automation.</span><span class="sxs-lookup"><span data-stu-id="05a37-218">Enables you to read the `InitString` content from within the automation.</span></span> <span data-ttu-id="05a37-219">This action has the following properties:</span><span class="sxs-lookup"><span data-stu-id="05a37-219">This action has the following properties:</span></span>  
  
- <span data-ttu-id="05a37-220">`XPath` as string: Used to read the application configuration file.</span><span class="sxs-lookup"><span data-stu-id="05a37-220">`XPath` as string: Used to read the application configuration file.</span></span>  
  
- <span data-ttu-id="05a37-221">`QueryResult` as string: Result of the search.</span><span class="sxs-lookup"><span data-stu-id="05a37-221">`QueryResult` as string: Result of the search.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="05a37-222">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="05a37-222">See also</span></span>  
 <span data-ttu-id="05a37-223">[Create a HAT automation](../unified-service-desk/create-hat-automation.md) </span><span class="sxs-lookup"><span data-stu-id="05a37-223">[Create a HAT automation](../unified-service-desk/create-hat-automation.md) </span></span>  
 <span data-ttu-id="05a37-224">[UII Application Integration Framework](../unified-service-desk/uii-application-integration-framework.md) </span><span class="sxs-lookup"><span data-stu-id="05a37-224">[UII Application Integration Framework](../unified-service-desk/uii-application-integration-framework.md) </span></span>  
 [<span data-ttu-id="05a37-225">Use Data Driven Adapters</span><span class="sxs-lookup"><span data-stu-id="05a37-225">Use Data Driven Adapters</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
