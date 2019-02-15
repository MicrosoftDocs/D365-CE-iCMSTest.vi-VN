---
title: Create a CTI Desktop Manager | MicrosoftDocs
description: The CTI Desktop Manager component is the interface between the computer telephony integration (CTI) system and Unified Service Desk or User Interface Integration (UII). The CTI Desktop Manager component creates the following two objects that collectively manage the state and data in a call- CallStateManager and AgentStateManager.
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
ms.assetid: eda74fb2-c74a-413d-b1b8-921328dd365e
caps.latest.revision: 8
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: e317a00b4a3ab798d43420b630a96be3d35ca7a4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387479"
---
# <a name="create-a-cti-desktop-manager-in-unified-service-desk"></a><span data-ttu-id="33bd4-104">Create a CTI Desktop Manager in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="33bd4-104">Create a CTI Desktop Manager in Unified Service Desk</span></span>
<span data-ttu-id="33bd4-105">The CTI Desktop Manager component is the interface between the computer telephony integration (CTI) system and [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] or [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)].</span><span class="sxs-lookup"><span data-stu-id="33bd4-105">The CTI Desktop Manager component is the interface between the computer telephony integration (CTI) system and [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] or [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)].</span></span> <span data-ttu-id="33bd4-106">The CTI Desktop Manager component creates the following two objects that collectively manage the state and data in a call:</span><span class="sxs-lookup"><span data-stu-id="33bd4-106">The CTI Desktop Manager component creates the following two objects that collectively manage the state and data in a call:</span></span>  
  
-   <span data-ttu-id="33bd4-107">`CallStateManager`: The [CtiCallStateManager](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.cticallstatemanager) class is used as the base class that contains properties, methods, and events for communicating with the CTI Connector component to issue commands related to call management such as answer call, hang up, hold call, and transfer call.</span><span class="sxs-lookup"><span data-stu-id="33bd4-107">`CallStateManager`: The [CtiCallStateManager](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.cticallstatemanager) class is used as the base class that contains properties, methods, and events for communicating with the CTI Connector component to issue commands related to call management such as answer call, hang up, hold call, and transfer call.</span></span> <span data-ttu-id="33bd4-108">It provides multi-call management features and pre-wired events for the CTI Controls (user interface) to connect to, and base implementation and extensibility points for vendor specific customizations.</span><span class="sxs-lookup"><span data-stu-id="33bd4-108">It provides multi-call management features and pre-wired events for the CTI Controls (user interface) to connect to, and base implementation and extensibility points for vendor specific customizations.</span></span>  
  
-   <span data-ttu-id="33bd4-109">`AgentStateManager`: The [CtiAgentStateManager](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctiagentstatemanager) is used as the base class that contains properties, methods, and events for communicating with the CTI Connector component related to agent state management (agent’s availability such as available, busy, and away).</span><span class="sxs-lookup"><span data-stu-id="33bd4-109">`AgentStateManager`: The [CtiAgentStateManager](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctiagentstatemanager) is used as the base class that contains properties, methods, and events for communicating with the CTI Connector component related to agent state management (agent’s availability such as available, busy, and away).</span></span> <span data-ttu-id="33bd4-110">It provides pre-wired events for the CTI Controls (user interface) to connect to, and base implementation and extensibility points for vendor specific customizations.</span><span class="sxs-lookup"><span data-stu-id="33bd4-110">It provides pre-wired events for the CTI Controls (user interface) to connect to, and base implementation and extensibility points for vendor specific customizations.</span></span>  
  
<a name="define"></a>   
## <a name="define-a-cti-desktop-manager-component"></a><span data-ttu-id="33bd4-111">Define a CTI Desktop Manager component</span><span class="sxs-lookup"><span data-stu-id="33bd4-111">Define a CTI Desktop Manager component</span></span>  
 <span data-ttu-id="33bd4-112">The CTI Desktop Manager implements the following interfaces:</span><span class="sxs-lookup"><span data-stu-id="33bd4-112">The CTI Desktop Manager implements the following interfaces:</span></span>  
  
- [<span data-ttu-id="33bd4-113">ICtiAgentStateManager</span><span class="sxs-lookup"><span data-stu-id="33bd4-113">ICtiAgentStateManager</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictiagentstatemanager)  
  
- [<span data-ttu-id="33bd4-114">ICtiCallStateManager</span><span class="sxs-lookup"><span data-stu-id="33bd4-114">ICtiCallStateManager</span></span>](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.icticallstatemanager)  
  
  <span data-ttu-id="33bd4-115">You define a CTI Desktop Manager component in the same project as the one that you use for defining your CTI Connector using the **USD CTI Connector** project template.</span><span class="sxs-lookup"><span data-stu-id="33bd4-115">You define a CTI Desktop Manager component in the same project as the one that you use for defining your CTI Connector using the **USD CTI Connector** project template.</span></span> <span data-ttu-id="33bd4-116">For more information about using this template, see [Create a CTI Connector](../unified-service-desk/create-cti-connector.md).</span><span class="sxs-lookup"><span data-stu-id="33bd4-116">For more information about using this template, see [Create a CTI Connector](../unified-service-desk/create-cti-connector.md).</span></span>  
  
  <span data-ttu-id="33bd4-117">Use the BaseCtiDesktopManagerControl.cs file in the **USD CTI Connector** project template to configure your CTI Desktop Manager, and the AgentStateManager.cs and CallStateManager.cs files in to configure call and agent states.</span><span class="sxs-lookup"><span data-stu-id="33bd4-117">Use the BaseCtiDesktopManagerControl.cs file in the **USD CTI Connector** project template to configure your CTI Desktop Manager, and the AgentStateManager.cs and CallStateManager.cs files in to configure call and agent states.</span></span> <span data-ttu-id="33bd4-118">These files provide pre-wired methods and instructions (in the form of comments) to help you create a CTI Desktop Manager component.</span><span class="sxs-lookup"><span data-stu-id="33bd4-118">These files provide pre-wired methods and instructions (in the form of comments) to help you create a CTI Desktop Manager component.</span></span>  
  
  <span data-ttu-id="33bd4-119">![Manage CTI Desktop Manager](../unified-service-desk/media/usd-manage-cti-desktop-manager.png "Manage CTI Desktop Manager")</span><span class="sxs-lookup"><span data-stu-id="33bd4-119">![Manage CTI Desktop Manager](../unified-service-desk/media/usd-manage-cti-desktop-manager.png "Manage CTI Desktop Manager")</span></span>  
  
<a name="CustLookup"></a>   
## <a name="raise-a-search-request-when-a-call-arrives"></a><span data-ttu-id="33bd4-120">Raise a search request when a call arrives</span><span class="sxs-lookup"><span data-stu-id="33bd4-120">Raise a search request when a call arrives</span></span>  
 <span data-ttu-id="33bd4-121">When a new call arrives, you can invoke a search request to look up the automatic number identification (ANI) number in a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps repository, get extra information, such as first name, last name, and so on, and create a session.</span><span class="sxs-lookup"><span data-stu-id="33bd4-121">When a new call arrives, you can invoke a search request to look up the automatic number identification (ANI) number in a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps repository, get extra information, such as first name, last name, and so on, and create a session.</span></span> [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] <span data-ttu-id="33bd4-122">provides the [CtiLookupRequest](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctilookuprequest) class that describes a customer lookup request that the CTI system sends to a customer search provider.</span><span class="sxs-lookup"><span data-stu-id="33bd4-122">provides the [CtiLookupRequest](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctilookuprequest) class that describes a customer lookup request that the CTI system sends to a customer search provider.</span></span> <span data-ttu-id="33bd4-123">This class describes common data elements that the CTI system will provide.</span><span class="sxs-lookup"><span data-stu-id="33bd4-123">This class describes common data elements that the CTI system will provide.</span></span> <span data-ttu-id="33bd4-124">It also gives you the ability to add custom data to the request.</span><span class="sxs-lookup"><span data-stu-id="33bd4-124">It also gives you the ability to add custom data to the request.</span></span>  
  
 <span data-ttu-id="33bd4-125">The customer lookup or search is implemented depending on whether you are searching in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] or UII:</span><span class="sxs-lookup"><span data-stu-id="33bd4-125">The customer lookup or search is implemented depending on whether you are searching in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] or UII:</span></span>  
  
- <span data-ttu-id="33bd4-126">**Unified Service Desk**: The search request is handled by the Global Manager hosted control.</span><span class="sxs-lookup"><span data-stu-id="33bd4-126">**Unified Service Desk**: The search request is handled by the Global Manager hosted control.</span></span>  
  
- <span data-ttu-id="33bd4-127">**User Interface Integration (UII)**: The lookup request is sent to [ICustomerSearch](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.core.icustomersearch), and it is up to you how you want to implement the search control.</span><span class="sxs-lookup"><span data-stu-id="33bd4-127">**User Interface Integration (UII)**: The lookup request is sent to [ICustomerSearch](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.core.icustomersearch), and it is up to you how you want to implement the search control.</span></span> <span data-ttu-id="33bd4-128">You can also send additional data to the search request using the [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctilookuprequest.addlookuprequestitem\(system.string,system.string\)) method.</span><span class="sxs-lookup"><span data-stu-id="33bd4-128">You can also send additional data to the search request using the [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctilookuprequest.addlookuprequestitem\(system.string,system.string\)) method.</span></span> <span data-ttu-id="33bd4-129">UII provides you project templates to create a Windows Forms-based or WPF-based customer search control with the CTI search request pre-wired.</span><span class="sxs-lookup"><span data-stu-id="33bd4-129">UII provides you project templates to create a Windows Forms-based or WPF-based customer search control with the CTI search request pre-wired.</span></span>  
  
<a name="CallData"></a>   
## <a name="access-call-data-and-events"></a><span data-ttu-id="33bd4-130">Access call data and events</span><span class="sxs-lookup"><span data-stu-id="33bd4-130">Access call data and events</span></span>  
 <span data-ttu-id="33bd4-131">Use the [CallInfoData](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.callinfodata) class to access information about a call that is in process in [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] desktop (such as [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]).</span><span class="sxs-lookup"><span data-stu-id="33bd4-131">Use the [CallInfoData](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.callinfodata) class to access information about a call that is in process in [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] desktop (such as [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]).</span></span> <span data-ttu-id="33bd4-132">The following example shows the syntax of this class:</span><span class="sxs-lookup"><span data-stu-id="33bd4-132">The following example shows the syntax of this class:</span></span>  
  
```  
CallInfoData calldata = GetCallInfoData(ctiCallRefCallId);  
```  
  
<a name="CallActions"></a>   
## <a name="enable-or-disable-call-actions"></a><span data-ttu-id="33bd4-133">Enable or disable call actions</span><span class="sxs-lookup"><span data-stu-id="33bd4-133">Enable or disable call actions</span></span>  
 <span data-ttu-id="33bd4-134">Use the [CtiCallActionOptions](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.cticallactionoptions) class to enable or disable call actions.</span><span class="sxs-lookup"><span data-stu-id="33bd4-134">Use the [CtiCallActionOptions](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.cticallactionoptions) class to enable or disable call actions.</span></span> <span data-ttu-id="33bd4-135">The following example code shows how to use this class to handle a call.</span><span class="sxs-lookup"><span data-stu-id="33bd4-135">The following example code shows how to use this class to handle a call.</span></span>  
  
```csharp  
public override void OnCallStateChanged(CtiCoreEventArgs e)  
{  
   CallEventArgs CallArgs = (CallEventArgs)e.EventInfo;  
  
   // Set the state of the call in the call list.   
   CallInfoData calldata = GetCallInfoData(CallArgs.Call.CallID.ToString(CultureInfo.CurrentUICulture));  
   if (calldata != null)  
      calldata.CurrentCallState = string.IsNullOrEmpty(CallArgs.State.ToString()) ? string.Empty : CallArgs.State.ToString();  
  
   UpdateCallInfoItemEntry(calldata); // update call data..   
  
   CtiCallEventArgs args = null;  
   switch (CallArgs.State)  
   {  
      case CallClassProvider.CallState.Connected:  
      args = new CtiCallEventArgs(calldata.GetCtiCallRefId, CtiCallStates.OFFHOOK, new CtiCallActionOptions());  
      break;  
  
      case CallClassProvider.CallState.Disconnected:  
      args = new CtiCallEventArgs(calldata.GetCtiCallRefId, CtiCallStates.DISCONNECTED, new CtiCallActionOptions());  
      break;  
  
      case CallClassProvider.CallState.Hold:  
      args = new CtiCallEventArgs(calldata.GetCtiCallRefId, CtiCallStates.ONHOLD, new CtiCallActionOptions());  
      break;  
  
      case CallClassProvider.CallState.Idle:  
      args = new CtiCallEventArgs(calldata.GetCtiCallRefId, CtiCallStates.DISCONNECTED, new CtiCallActionOptions());  
      break;  
  
      case CallClassProvider.CallState.Incoming_Call:  
      args = new CtiCallEventArgs(calldata.GetCtiCallRefId, CtiCallStates.PICKUPPENDING, new CtiCallActionOptions());  
      break;  
  
      case CallClassProvider.CallState.Ringing:  
      args = new CtiCallEventArgs(calldata.GetCtiCallRefId, CtiCallStates.RINGING, new CtiCallActionOptions());  
      break;  
  
      default:  
      System.Diagnostics.Trace.WriteLine(ResourceStrings.UNSUPPORTEDEVENT + CallArgs.State.ToString());  
      break;  
   }  
   // Raise status change event.   
   RaiseCallStateChangeEvent(args);  
}  
  
```  
  
<a name="Configure"></a>   
## <a name="configure-cti-desktop-manager-hosted-control-in-unified-service-desk"></a><span data-ttu-id="33bd4-136">Configure CTI Desktop Manager hosted control in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="33bd4-136">Configure CTI Desktop Manager hosted control in Unified Service Desk</span></span>  
 <span data-ttu-id="33bd4-137">After you have created the CTI Desktop Manager along with your CTI connector, you must configure these as hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="33bd4-137">After you have created the CTI Desktop Manager along with your CTI connector, you must configure these as hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="33bd4-138">provides a hosted control of type **CTI Desktop Manager**  that can be used to configure your CTI Desktop Manager in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="33bd4-138">provides a hosted control of type **CTI Desktop Manager**  that can be used to configure your CTI Desktop Manager in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="33bd4-139">The CTI Connector should be configured as a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control.</span><span class="sxs-lookup"><span data-stu-id="33bd4-139">The CTI Connector should be configured as a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="33bd4-140">[Configure a hosted control for CTI Connector in Unified Service Desk](../unified-service-desk/create-cti-connector.md#Configure)</span><span class="sxs-lookup"><span data-stu-id="33bd4-140">[Configure a hosted control for CTI Connector in Unified Service Desk](../unified-service-desk/create-cti-connector.md#Configure)</span></span>  
  
1. <span data-ttu-id="33bd4-141">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="33bd4-141">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="33bd4-142">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement apps** > **Settings** > **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="33bd4-142">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement apps** > **Settings** > **Unified Service Desk**.</span></span>  
  
3. <span data-ttu-id="33bd4-143">On the **Unified Service Desk** page, click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="33bd4-143">On the **Unified Service Desk** page, click **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="33bd4-144">Trên trang **Kiểm soát Tổ chức**, bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="33bd4-144">On the **Hosted Controls** page, click **New**.</span></span>  
  
5. <span data-ttu-id="33bd4-145">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="33bd4-145">On the **New Hosted Control** page, specify the following values:</span></span>  
  
   |<span data-ttu-id="33bd4-146">Trường</span><span class="sxs-lookup"><span data-stu-id="33bd4-146">Field</span></span>|<span data-ttu-id="33bd4-147">Value</span><span class="sxs-lookup"><span data-stu-id="33bd4-147">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="33bd4-148">Tên</span><span class="sxs-lookup"><span data-stu-id="33bd4-148">Name</span></span>|<span data-ttu-id="33bd4-149">Give name as per your choice.</span><span class="sxs-lookup"><span data-stu-id="33bd4-149">Give name as per your choice.</span></span>|  
   |<span data-ttu-id="33bd4-150">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="33bd4-150">USD Component Type</span></span>|<span data-ttu-id="33bd4-151">CTI Desktop Manager</span><span class="sxs-lookup"><span data-stu-id="33bd4-151">CTI Desktop Manager</span></span>|  
   |<span data-ttu-id="33bd4-152">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="33bd4-152">Display Group</span></span>|<span data-ttu-id="33bd4-153">Bảng điều khiển bị ẩn</span><span class="sxs-lookup"><span data-stu-id="33bd4-153">HiddenPanel</span></span>|  
   |<span data-ttu-id="33bd4-154">URI cụm tổ hợp</span><span class="sxs-lookup"><span data-stu-id="33bd4-154">Assembly URI</span></span>|<span data-ttu-id="33bd4-155">This is the name of your assembly (.dll) file that you built in the previous step.</span><span class="sxs-lookup"><span data-stu-id="33bd4-155">This is the name of your assembly (.dll) file that you built in the previous step.</span></span>|  
   |<span data-ttu-id="33bd4-156">Loại cụm tổ hợp</span><span class="sxs-lookup"><span data-stu-id="33bd4-156">Assembly Type</span></span>|<span data-ttu-id="33bd4-157">This is the name of your assembly followed by a dot, and then the class name of your CTI Connector.</span><span class="sxs-lookup"><span data-stu-id="33bd4-157">This is the name of your assembly followed by a dot, and then the class name of your CTI Connector.</span></span> <span data-ttu-id="33bd4-158">For example, if your assembly name is MyCtiManager, and the name of the class of your CTI project is DesktopManager, then you must type the following in this field: MyCtiManager.DesktopManager.</span><span class="sxs-lookup"><span data-stu-id="33bd4-158">For example, if your assembly name is MyCtiManager, and the name of the class of your CTI project is DesktopManager, then you must type the following in this field: MyCtiManager.DesktopManager.</span></span>|  
  
   <span data-ttu-id="33bd4-159">![Configure a CTI Desktop Manager hosted control](../unified-service-desk/media/usd-cti-desktop-manager-hosted-control.png "Configure a CTI Desktop Manager hosted control")</span><span class="sxs-lookup"><span data-stu-id="33bd4-159">![Configure a CTI Desktop Manager hosted control](../unified-service-desk/media/usd-cti-desktop-manager-hosted-control.png "Configure a CTI Desktop Manager hosted control")</span></span>  
  
6. <span data-ttu-id="33bd4-160">Click **Save** to create the hosted control.</span><span class="sxs-lookup"><span data-stu-id="33bd4-160">Click **Save** to create the hosted control.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="33bd4-161">After you have configured the CTI Desktop Manager hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], you must configure:</span><span class="sxs-lookup"><span data-stu-id="33bd4-161">After you have configured the CTI Desktop Manager hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], you must configure:</span></span>  
> 
> - <span data-ttu-id="33bd4-162">Actions for your CTI Desktop Manager hosted control.</span><span class="sxs-lookup"><span data-stu-id="33bd4-162">Actions for your CTI Desktop Manager hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="33bd4-163">[Actions supported for telephony functions](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md#Actions)</span><span class="sxs-lookup"><span data-stu-id="33bd4-163">[Actions supported for telephony functions](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md#Actions)</span></span>  
>   - <span data-ttu-id="33bd4-164">Window navigation rules to route the CTI search requests appropriately to create sessions and display the search results in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)][!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [CTI search](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md#CTISearch)</span><span class="sxs-lookup"><span data-stu-id="33bd4-164">Window navigation rules to route the CTI search requests appropriately to create sessions and display the search results in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)][!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [CTI search](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md#CTISearch)</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="33bd4-165">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="33bd4-165">See also</span></span>  
 <span data-ttu-id="33bd4-166">[Configure the CTI Desktop Manager hosted control for generic listener adapter](../unified-service-desk/use-generic-listener-adapter-unified-service-desk.md#Configure) </span><span class="sxs-lookup"><span data-stu-id="33bd4-166">[Configure the CTI Desktop Manager hosted control for generic listener adapter](../unified-service-desk/use-generic-listener-adapter-unified-service-desk.md#Configure) </span></span>  
 <span data-ttu-id="33bd4-167">[Create a CTI Connector](../unified-service-desk/create-cti-connector.md) </span><span class="sxs-lookup"><span data-stu-id="33bd4-167">[Create a CTI Connector](../unified-service-desk/create-cti-connector.md) </span></span>  
 <span data-ttu-id="33bd4-168">[Create a CTI Control](../unified-service-desk/create-cti-control.md) </span><span class="sxs-lookup"><span data-stu-id="33bd4-168">[Create a CTI Control](../unified-service-desk/create-cti-control.md) </span></span>  
 <span data-ttu-id="33bd4-169">[Walkthrough: Use CTI Desktop Manager ro create a CTI adapter](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md) </span><span class="sxs-lookup"><span data-stu-id="33bd4-169">[Walkthrough: Use CTI Desktop Manager ro create a CTI adapter](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md) </span></span>  
 [<span data-ttu-id="33bd4-170">UII Computer Telephony Integration (CTI) framework</span><span class="sxs-lookup"><span data-stu-id="33bd4-170">UII Computer Telephony Integration (CTI) framework</span></span>](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)
