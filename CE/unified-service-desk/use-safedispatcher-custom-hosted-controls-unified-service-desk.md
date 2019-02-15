---
title: Use SafeDispatcher for custom hosted controls in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use SafeDispatcher to provide out-of-box logging for unhandled exceptions with detailed information about the source and cause of the exception in Unified Service Desk.
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
ms.assetid: 4f6c8c7e-4326-4780-9d4c-f24e097b934c
caps.latest.revision: 26
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: edbd2c06d58093c4a084b74e512099b5fe87317b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385882"
---
# <a name="use-safedispatcher-for-custom-hosted-controls-in-unified-service-desk"></a><span data-ttu-id="15dca-103">Use SafeDispatcher for custom hosted controls in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="15dca-103">Use SafeDispatcher for custom hosted controls in Unified Service Desk</span></span>
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="15dca-104">is a [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)]-based application where all the operations in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] are executed on the main *WPF Dispatcher* thread.</span><span class="sxs-lookup"><span data-stu-id="15dca-104">is a [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)]-based application where all the operations in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] are executed on the main *WPF Dispatcher* thread.</span></span> <span data-ttu-id="15dca-105">The [WPF Dispatcher](https://msdn.microsoft.com/library/system.windows.threading.dispatcher\(v=vs.110\).aspx) class provides services for managing the queue of work items for a thread.</span><span class="sxs-lookup"><span data-stu-id="15dca-105">The [WPF Dispatcher](https://msdn.microsoft.com/library/system.windows.threading.dispatcher\(v=vs.110\).aspx) class provides services for managing the queue of work items for a thread.</span></span>  
  
 <span data-ttu-id="15dca-106">You can extend [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by creating custom controls and hosting it within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="15dca-106">You can extend [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by creating custom controls and hosting it within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="15dca-107">However, if a custom hosted control contains faulty code or executes operations using new threads without appropriately handling exceptions during code execution, it may cause stability issues in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and might even cause the  client application to freeze or become unresponsive.</span><span class="sxs-lookup"><span data-stu-id="15dca-107">However, if a custom hosted control contains faulty code or executes operations using new threads without appropriately handling exceptions during code execution, it may cause stability issues in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and might even cause the  client application to freeze or become unresponsive.</span></span> <span data-ttu-id="15dca-108">The unhandled exceptions in third-party custom controls  makes it challenging to identify, troubleshoot, and resolve the issue by the product/support team as they might not have access to the information why an error/exception occurred in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and the exact code that caused the error.</span><span class="sxs-lookup"><span data-stu-id="15dca-108">The unhandled exceptions in third-party custom controls  makes it challenging to identify, troubleshoot, and resolve the issue by the product/support team as they might not have access to the information why an error/exception occurred in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and the exact code that caused the error.</span></span>  
  
 <span data-ttu-id="15dca-109">Introducing *SafeDispatcher* that provides a powerful and informative exception handling mechanism for custom hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by providing out-of-box logging for unhandled exceptions with detailed information about the source and cause of the exception, and allowing you to configure or  overwrite the SafeDispatcher exception handling to perform some other steps.</span><span class="sxs-lookup"><span data-stu-id="15dca-109">Introducing *SafeDispatcher* that provides a powerful and informative exception handling mechanism for custom hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by providing out-of-box logging for unhandled exceptions with detailed information about the source and cause of the exception, and allowing you to configure or  overwrite the SafeDispatcher exception handling to perform some other steps.</span></span> <span data-ttu-id="15dca-110">This also prevents the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client from becoming unresponsive because of unhandled exceptions in the custom hosted control code.</span><span class="sxs-lookup"><span data-stu-id="15dca-110">This also prevents the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client from becoming unresponsive because of unhandled exceptions in the custom hosted control code.</span></span>
  
<a name="What"></a>   
## <a name="what-is-safedispatcher"></a><span data-ttu-id="15dca-111">What is SafeDispatcher?</span><span class="sxs-lookup"><span data-stu-id="15dca-111">What is SafeDispatcher?</span></span>  
 <span data-ttu-id="15dca-112">[SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher) is built on the same lines as the [WPF Dispatcher](https://msdn.microsoft.com/library/system.windows.threading.dispatcher\(v=vs.110\).aspx), and provides resilient and informative exception handling for  custom hosted controls within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="15dca-112">[SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher) is built on the same lines as the [WPF Dispatcher](https://msdn.microsoft.com/library/system.windows.threading.dispatcher\(v=vs.110\).aspx), and provides resilient and informative exception handling for  custom hosted controls within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="15dca-113">It is exposed as a protected property, [SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol.safedispatcher), on the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class, which makes SafeDispatcher automatically available for all [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] custom hosted controls that are derived from the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class.</span><span class="sxs-lookup"><span data-stu-id="15dca-113">It is exposed as a protected property, [SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol.safedispatcher), on the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class, which makes SafeDispatcher automatically available for all [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] custom hosted controls that are derived from the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="15dca-114">Do not use the [SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher) class  in your code to work with SafeDispatcher.</span><span class="sxs-lookup"><span data-stu-id="15dca-114">Do not use the [SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher) class  in your code to work with SafeDispatcher.</span></span> <span data-ttu-id="15dca-115">Instead, you must use the [SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol.safedispatcher) property on your custom hosted control instance that is derived from the  [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class to use SafeDispatcher.</span><span class="sxs-lookup"><span data-stu-id="15dca-115">Instead, you must use the [SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol.safedispatcher) property on your custom hosted control instance that is derived from the  [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class to use SafeDispatcher.</span></span>  
  
 <span data-ttu-id="15dca-116">Just like [WPF Dispatcher](https://msdn.microsoft.com/library/system.windows.threading.dispatcher\(v=vs.110\).aspx), SafeDispatcher provides methods such as [BeginInvoke](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher.begininvoke), [Invoke](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher.invoke), and [InvokeAsync](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher.invokeasync) to run operations synchronously or asynchronously on SafeDispatcher with an additional boolean parameter, `runOnMainUiThread`, that controls whether to run SafeDispatcher on UI thread or not.</span><span class="sxs-lookup"><span data-stu-id="15dca-116">Just like [WPF Dispatcher](https://msdn.microsoft.com/library/system.windows.threading.dispatcher\(v=vs.110\).aspx), SafeDispatcher provides methods such as [BeginInvoke](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher.begininvoke), [Invoke](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher.invoke), and [InvokeAsync](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher.invokeasync) to run operations synchronously or asynchronously on SafeDispatcher with an additional boolean parameter, `runOnMainUiThread`, that controls whether to run SafeDispatcher on UI thread or not.</span></span>  
  
 <span data-ttu-id="15dca-117">SafeDispatcher provides the following benefits:</span><span class="sxs-lookup"><span data-stu-id="15dca-117">SafeDispatcher provides the following benefits:</span></span>  
  
- <span data-ttu-id="15dca-118">**Protected UI Dispatcher thread**: Developers can run all UI-dependent operations on SafeDispatcher by setting the `runOnMainUiThread` parameter  to "true" in the invoke method to run the SafeDispatcher on UI thread.</span><span class="sxs-lookup"><span data-stu-id="15dca-118">**Protected UI Dispatcher thread**: Developers can run all UI-dependent operations on SafeDispatcher by setting the `runOnMainUiThread` parameter  to "true" in the invoke method to run the SafeDispatcher on UI thread.</span></span> <span data-ttu-id="15dca-119">Any unhandled exception raised on main UI dispatcher will be handled safely at the hosted control level instead of bubbling up to the global [DispatcherUnhandledException Event](https://msdn.microsoft.com/library/system.windows.application.dispatcherunhandledexception\(v=vs.110\).aspx) handler.</span><span class="sxs-lookup"><span data-stu-id="15dca-119">Any unhandled exception raised on main UI dispatcher will be handled safely at the hosted control level instead of bubbling up to the global [DispatcherUnhandledException Event](https://msdn.microsoft.com/library/system.windows.application.dispatcherunhandledexception\(v=vs.110\).aspx) handler.</span></span>  
  
- <span data-ttu-id="15dca-120">**Protected non-UI Dispatcher thread**: Developers can run all UI-independent code on SafeDispatcher.</span><span class="sxs-lookup"><span data-stu-id="15dca-120">**Protected non-UI Dispatcher thread**: Developers can run all UI-independent code on SafeDispatcher.</span></span> <span data-ttu-id="15dca-121">by setting the `runOnMainUiThread` parameter to "false" in the invoke method to run the SafeDispatcher on non-UI thread.</span><span class="sxs-lookup"><span data-stu-id="15dca-121">by setting the `runOnMainUiThread` parameter to "false" in the invoke method to run the SafeDispatcher on non-UI thread.</span></span> <span data-ttu-id="15dca-122">Any unhandled exception raised on main non-UI dispatcher will be handled safely at the hosted control level instead of  bubbling up to the global [DispatcherUnhandledException Event](https://msdn.microsoft.com/library/system.windows.application.dispatcherunhandledexception\(v=vs.110\).aspx) handler.</span><span class="sxs-lookup"><span data-stu-id="15dca-122">Any unhandled exception raised on main non-UI dispatcher will be handled safely at the hosted control level instead of  bubbling up to the global [DispatcherUnhandledException Event](https://msdn.microsoft.com/library/system.windows.application.dispatcherunhandledexception\(v=vs.110\).aspx) handler.</span></span>  
  
- <span data-ttu-id="15dca-123">**Detailed information about exception source and cause:**: The SafeDispatcher exception handler is raised when an unhandled exception is raised at the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) level by the UI or non-UI thread, which allows [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to capture critical information at the hosted control level such as hosted control name, hosted control type, method name, and complete stack trace to identify the exact location and cause of the exception.</span><span class="sxs-lookup"><span data-stu-id="15dca-123">**Detailed information about exception source and cause:**: The SafeDispatcher exception handler is raised when an unhandled exception is raised at the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) level by the UI or non-UI thread, which allows [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to capture critical information at the hosted control level such as hosted control name, hosted control type, method name, and complete stack trace to identify the exact location and cause of the exception.</span></span>  
  
- <span data-ttu-id="15dca-124">**Configure or override SafeDispatcher exception handler**: Developers can leverage the out-of-box behavior of the SafeDispatcher exception handler to prompt the user with information about the unhandled exception or override the behavior as per their business requirement such as configure additional logging, close session based controls, or  exit the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span><span class="sxs-lookup"><span data-stu-id="15dca-124">**Configure or override SafeDispatcher exception handler**: Developers can leverage the out-of-box behavior of the SafeDispatcher exception handler to prompt the user with information about the unhandled exception or override the behavior as per their business requirement such as configure additional logging, close session based controls, or  exit the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span></span>  
  
<a name="How"></a>   
## <a name="how-to-use-safedispatcher"></a><span data-ttu-id="15dca-125">How to use SafeDispatcher?</span><span class="sxs-lookup"><span data-stu-id="15dca-125">How to use SafeDispatcher?</span></span>  
 <span data-ttu-id="15dca-126">The [SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol.safedispatcher) property is available for all [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] custom hosted control instances that are derived from the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class.</span><span class="sxs-lookup"><span data-stu-id="15dca-126">The [SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol.safedispatcher) property is available for all [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] custom hosted control instances that are derived from the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class.</span></span> <span data-ttu-id="15dca-127">A [SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher) instance will be available to run on UI thread when the custom hosted control is initialized.</span><span class="sxs-lookup"><span data-stu-id="15dca-127">A [SafeDispatcher](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.utilities.safedispatcher) instance will be available to run on UI thread when the custom hosted control is initialized.</span></span> <span data-ttu-id="15dca-128">However, a SafeDispatcher instance will only be available to run on  non-UI thread when you execute the invoke method for the first time.</span><span class="sxs-lookup"><span data-stu-id="15dca-128">However, a SafeDispatcher instance will only be available to run on  non-UI thread when you execute the invoke method for the first time.</span></span>  
  
-   <span data-ttu-id="15dca-129">Synchronously invoke a UI-specific function using the SafeDispatcher</span><span class="sxs-lookup"><span data-stu-id="15dca-129">Synchronously invoke a UI-specific function using the SafeDispatcher</span></span>  
  
    ```csharp  
    SafeDispatcher.Invoke(() =>  
                {  
                    ProcessData();  
                }, DispatcherPriority.Normal, CancellationToken.None, true);  
    ```  
  
     <span data-ttu-id="15dca-130">HOẶC</span><span class="sxs-lookup"><span data-stu-id="15dca-130">OR</span></span>  
  
    ```csharp  
    SafeDispatcher.Invoke(() =>  
                {  
                    ProcessData();  
                }, DispatcherPriority.Normal, CancellationToken.None);  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="15dca-131">For UI-specific function, you should set the `runOnMainUiThread` optional parameter to "true".</span><span class="sxs-lookup"><span data-stu-id="15dca-131">For UI-specific function, you should set the `runOnMainUiThread` optional parameter to "true".</span></span> <span data-ttu-id="15dca-132">If you do not specify a value for this parameter, by default "true" is passed.</span><span class="sxs-lookup"><span data-stu-id="15dca-132">If you do not specify a value for this parameter, by default "true" is passed.</span></span> <span data-ttu-id="15dca-133">So, any of the above method definition works fine.</span><span class="sxs-lookup"><span data-stu-id="15dca-133">So, any of the above method definition works fine.</span></span>  
  
-   <span data-ttu-id="15dca-134">Asynchronously invoke a UI-specific function using SafeDispatcher.</span><span class="sxs-lookup"><span data-stu-id="15dca-134">Asynchronously invoke a UI-specific function using SafeDispatcher.</span></span> <span data-ttu-id="15dca-135">You can use either the `BeginInvoke` or `InvokeAsync` method.</span><span class="sxs-lookup"><span data-stu-id="15dca-135">You can use either the `BeginInvoke` or `InvokeAsync` method.</span></span>  
  
    ```csharp  
    SafeDispatcher.BeginInvoke(new Action(() =>  
                {  
                   ProcessData();  
                }));  
  
    ```  
  
     <span data-ttu-id="15dca-136">HOẶC</span><span class="sxs-lookup"><span data-stu-id="15dca-136">OR</span></span>  
  
    ```csharp  
    SafeDispatcher.InvokeAsync(new Action(() =>  
                {  
                   ProcessData();  
                }));  
  
    ```  
  
## <a name="customize-the-safedispatcher-exception-handler"></a><span data-ttu-id="15dca-137">Customize the SafeDispatcher exception handler</span><span class="sxs-lookup"><span data-stu-id="15dca-137">Customize the SafeDispatcher exception handler</span></span>  
 <span data-ttu-id="15dca-138">With the introduction of SafeDispatcher, all unhandled exceptions in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] will raise the [SafeDispatcherUnhandledException Event](http://msdn.microsoft.com/en-us/5c67a00b-f949-4f83-9b14-f7ee396dd657) instead of the  global [DispatcherUnhandledException Event](https://msdn.microsoft.com/library/system.windows.application.dispatcherunhandledexception\(v=vs.110\).aspx).</span><span class="sxs-lookup"><span data-stu-id="15dca-138">With the introduction of SafeDispatcher, all unhandled exceptions in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] will raise the [SafeDispatcherUnhandledException Event](http://msdn.microsoft.com/en-us/5c67a00b-f949-4f83-9b14-f7ee396dd657) instead of the  global [DispatcherUnhandledException Event](https://msdn.microsoft.com/library/system.windows.application.dispatcherunhandledexception\(v=vs.110\).aspx).</span></span> <span data-ttu-id="15dca-139">The [SafeDispatcherUnhandledExceptionHandler Method](http://msdn.microsoft.com/en-us/a394320e-4f98-4ee0-85e0-b61c49fd9a6b) provides an out-of-box exception handler for SafeDispatcher to display information to the Unified Service Desk user with the following details: source control where the exception occurred and detailed info about the exception.</span><span class="sxs-lookup"><span data-stu-id="15dca-139">The [SafeDispatcherUnhandledExceptionHandler Method](http://msdn.microsoft.com/en-us/a394320e-4f98-4ee0-85e0-b61c49fd9a6b) provides an out-of-box exception handler for SafeDispatcher to display information to the Unified Service Desk user with the following details: source control where the exception occurred and detailed info about the exception.</span></span>  
  
 <span data-ttu-id="15dca-140">You can also override the out-of-box exception handling for SafeDispatcher to perform other operation such as prompt the user to close a session-based non-dynamic hosted control.</span><span class="sxs-lookup"><span data-stu-id="15dca-140">You can also override the out-of-box exception handling for SafeDispatcher to perform other operation such as prompt the user to close a session-based non-dynamic hosted control.</span></span>  
  
 <span data-ttu-id="15dca-141">The following sample code demonstrates how you can override the out-of-box SafeDispatcher exception handler to display a message box to prompt the user to close the custom hosted control when an exception occurs:</span><span class="sxs-lookup"><span data-stu-id="15dca-141">The following sample code demonstrates how you can override the out-of-box SafeDispatcher exception handler to display a message box to prompt the user to close the custom hosted control when an exception occurs:</span></span>  
  
```csharp  
protected override void SafeDispatcherUnhandledExceptionHandler(object sender, SafeDispatcherUnhandledExceptionEventArgs ex)  
{  
    string error = String.Format(CultureInfo.InvariantCulture,  
        "Error in hosted control  Application:{0} - Exception : {1} \r\nInnerException\r\n {2}", this.ApplicationName, ex.Exception, ex.InnerException);  
    DynamicsLogger.Logger.Log(error, TraceEventType.Error);  
    if (MessageBox.Show("Exception occurred in hosted control - " + this.ApplicationName + ".Do you wish to close it ?", "Question", MessageBoxButton.YesNo,  
        MessageBoxImage.Warning) == MessageBoxResult.Yes)  
    {  
        SafeDispatcher.BeginInvoke(() => { this.desktopAccess.CloseDynamicApplication(this.ApplicationName); });  
    }  
}  
```  
  
<a name="Migrating"></a>   
## <a name="migrating-from-wpf-dispatcher-to-safedispatcher-in-existing-custom-hosted-controls"></a><span data-ttu-id="15dca-142">Migrating from WPF Dispatcher to SafeDispatcher in existing custom hosted controls</span><span class="sxs-lookup"><span data-stu-id="15dca-142">Migrating from WPF Dispatcher to SafeDispatcher in existing custom hosted controls</span></span>  
 <span data-ttu-id="15dca-143">As the contract between WPF Dispatcher and SafeDispatcher is almost identical, the effort to move from WPF Dispatcher to SafeDispatcher is minimal.</span><span class="sxs-lookup"><span data-stu-id="15dca-143">As the contract between WPF Dispatcher and SafeDispatcher is almost identical, the effort to move from WPF Dispatcher to SafeDispatcher is minimal.</span></span> <span data-ttu-id="15dca-144">To migrate any hosted control instance derived from the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class, replace all "Dispatcher" instances with "SafeDispatcher".</span><span class="sxs-lookup"><span data-stu-id="15dca-144">To migrate any hosted control instance derived from the [DynamicsBaseHostedControl](https://docs.microsoft.com/dotnet/api/microsoft.crm.unifiedservicedesk.dynamics.dynamicsbasehostedcontrol) class, replace all "Dispatcher" instances with "SafeDispatcher".</span></span>  
  
 <span data-ttu-id="15dca-145">For example, consider the following code:</span><span class="sxs-lookup"><span data-stu-id="15dca-145">For example, consider the following code:</span></span>  
  
```csharp  
Dispatcher.Invoke((System.Action)delegate()  
{  
    DynamicsLogger.Logger.Log("Raising SetupHotKey's", TraceEventType.Verbose);  
    SetupHotkeys();  
    CRMGlobalManager.AppWithFocusChanged += CRMGlobalManager_AppWithFocusChanged;  
    FireEvent("DesktopReady");  
    InitializeFocusSelection();  
});  
```  
  
 <span data-ttu-id="15dca-146">Replace `Dispatcher` in the above code with `SafeDispatcher`; rest of the code remains the same:</span><span class="sxs-lookup"><span data-stu-id="15dca-146">Replace `Dispatcher` in the above code with `SafeDispatcher`; rest of the code remains the same:</span></span>  
  
```csharp  
SafeDispatcher.Invoke((System.Action)delegate()  
{  
    DynamicsLogger.Logger.Log("Raising SetupHotKey's", TraceEventType.Verbose);  
    SetupHotkeys();  
    CRMGlobalManager.AppWithFocusChanged += CRMGlobalManager_AppWithFocusChanged;  
    FireEvent("DesktopReady");  
    InitializeFocusSelection();  
});  
```  
  
<a name="Considerations"></a>   
## <a name="things-to-consider-when-using-safedispatcher"></a><span data-ttu-id="15dca-147">Things to consider when using SafeDispatcher</span><span class="sxs-lookup"><span data-stu-id="15dca-147">Things to consider when using SafeDispatcher</span></span>  
 <span data-ttu-id="15dca-148">SafeDispatcher offers a multithreaded model that is highly beneficial in dispatching functions synchronously or asynchronously to UI or non-UI threads.</span><span class="sxs-lookup"><span data-stu-id="15dca-148">SafeDispatcher offers a multithreaded model that is highly beneficial in dispatching functions synchronously or asynchronously to UI or non-UI threads.</span></span>  <span data-ttu-id="15dca-149">Operations that need to be run on threads that are available with fault tolerance should be executed on SafeDispatcher.</span><span class="sxs-lookup"><span data-stu-id="15dca-149">Operations that need to be run on threads that are available with fault tolerance should be executed on SafeDispatcher.</span></span> <span data-ttu-id="15dca-150">However multi-threading should be implemented very carefully to avoid deadlock between threads.</span><span class="sxs-lookup"><span data-stu-id="15dca-150">However multi-threading should be implemented very carefully to avoid deadlock between threads.</span></span> <span data-ttu-id="15dca-151">One such example is dispatching from non-UI thread to main WPF Dispatcher synchronously.</span><span class="sxs-lookup"><span data-stu-id="15dca-151">One such example is dispatching from non-UI thread to main WPF Dispatcher synchronously.</span></span> <span data-ttu-id="15dca-152">Lets consider this example:</span><span class="sxs-lookup"><span data-stu-id="15dca-152">Lets consider this example:</span></span>  
  
```csharp  
Thread thread = new Thread(() =>  
{  
    Dispatcher.Invoke(ProcessData);  
});  
thread.SetApartmentState(ApartmentState.STA);  
thread.Priority = ThreadPriority.Highest;  
thread.IsBackground = true;  
thread.Start();  
thread.Join();  
```  
  
 <span data-ttu-id="15dca-153">The `thread.Join()` method is causing the main thread to get blocked waiting for the termination of single-threaded apartment (STA) thread, but the STA thread is waiting for the  main thread to finish the execution of `ProcessData`.</span><span class="sxs-lookup"><span data-stu-id="15dca-153">The `thread.Join()` method is causing the main thread to get blocked waiting for the termination of single-threaded apartment (STA) thread, but the STA thread is waiting for the  main thread to finish the execution of `ProcessData`.</span></span> <span data-ttu-id="15dca-154">This causes your app in a deadlock situation.</span><span class="sxs-lookup"><span data-stu-id="15dca-154">This causes your app in a deadlock situation.</span></span>  
  
 <span data-ttu-id="15dca-155">Similarly, consider the following example:</span><span class="sxs-lookup"><span data-stu-id="15dca-155">Similarly, consider the following example:</span></span>  
  
```csharp  
// Invoke on STA thread  
SafeDispatcher.Invoke(() =>  
{  
    // Invoke back on main dispatcher  
    SafeDispatcher.Invoke(() =>  
    {  
        ProcessData();  
    });  
}, false);  
```  
  
 <span data-ttu-id="15dca-156">The [SafeDispatcherUnhandledExceptionHandler](https://docs.microsoft.com/dotnet/api/Microsoft.Crm.UnifiedServiceDesk.Dynamics.DynamicsBaseHostedControl.SafeDispatcherUnhandledExceptionHandler) method will be called if an exception happens on the WPF Dispatcher or on the STA non-UI thread and will be raised on the respective thread on which the exception happened.</span><span class="sxs-lookup"><span data-stu-id="15dca-156">The [SafeDispatcherUnhandledExceptionHandler](https://docs.microsoft.com/dotnet/api/Microsoft.Crm.UnifiedServiceDesk.Dynamics.DynamicsBaseHostedControl.SafeDispatcherUnhandledExceptionHandler) method will be called if an exception happens on the WPF Dispatcher or on the STA non-UI thread and will be raised on the respective thread on which the exception happened.</span></span> <span data-ttu-id="15dca-157">You should be careful in making sure you don’t place the above combination in this handler, that is, if the exception occurred on non-UI thread, do not dispatch synchronously to the main UI dispatcher.</span><span class="sxs-lookup"><span data-stu-id="15dca-157">You should be careful in making sure you don’t place the above combination in this handler, that is, if the exception occurred on non-UI thread, do not dispatch synchronously to the main UI dispatcher.</span></span>  
  
```csharp  
protected override void SafeDispatcherUnhandledExceptionHandler(object sender, SafeDispatcherUnhandledExceptionEventArgs ex)  
{  
    Dispatcher.Invoke(LogException);            // Incorrect  
    SafeDispatcher.Invoke(LogException);        // Incorrect  
    SafeDispatcher.BeginInvoke(LogException);   // Correct  
    SafeDispatcher.InvokeAsync(LogException);   // Correct  
}  
```  
  
### <a name="see-also"></a><span data-ttu-id="15dca-158">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="15dca-158">See also</span></span>  
 <span data-ttu-id="15dca-159">[Tạo kiểm soát tổ chức Unified Service Desk tùy chỉnh](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="15dca-159">[Create custom Unified Service Desk hosted control](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md) </span></span>  
 <span data-ttu-id="15dca-160">[Mở rộng Unified Service Desk](../unified-service-desk/extend-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="15dca-160">[Extend Unified Service Desk](../unified-service-desk/extend-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="15dca-161">Configure client diagnostic logging in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="15dca-161">Configure client diagnostic logging in Unified Service Desk</span></span>](admin/configure-client-diagnostic-logging-unified-service-desk.md)
