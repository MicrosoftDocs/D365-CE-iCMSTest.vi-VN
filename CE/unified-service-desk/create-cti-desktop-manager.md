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
# <a name="create-a-cti-desktop-manager-in-unified-service-desk"></a>Create a CTI Desktop Manager in Unified Service Desk
The CTI Desktop Manager component is the interface between the computer telephony integration (CTI) system and [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] or [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)]. The CTI Desktop Manager component creates the following two objects that collectively manage the state and data in a call:  
  
-   `CallStateManager`: The [CtiCallStateManager](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.cticallstatemanager) class is used as the base class that contains properties, methods, and events for communicating with the CTI Connector component to issue commands related to call management such as answer call, hang up, hold call, and transfer call. It provides multi-call management features and pre-wired events for the CTI Controls (user interface) to connect to, and base implementation and extensibility points for vendor specific customizations.  
  
-   `AgentStateManager`: The [CtiAgentStateManager](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctiagentstatemanager) is used as the base class that contains properties, methods, and events for communicating with the CTI Connector component related to agent state management (agent’s availability such as available, busy, and away). It provides pre-wired events for the CTI Controls (user interface) to connect to, and base implementation and extensibility points for vendor specific customizations.  
  
<a name="define"></a>   
## <a name="define-a-cti-desktop-manager-component"></a>Define a CTI Desktop Manager component  
 The CTI Desktop Manager implements the following interfaces:  
  
- [ICtiAgentStateManager](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictiagentstatemanager)  
  
- [ICtiCallStateManager](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.icticallstatemanager)  
  
  You define a CTI Desktop Manager component in the same project as the one that you use for defining your CTI Connector using the **USD CTI Connector** project template. For more information about using this template, see [Create a CTI Connector](../unified-service-desk/create-cti-connector.md).  
  
  Use the BaseCtiDesktopManagerControl.cs file in the **USD CTI Connector** project template to configure your CTI Desktop Manager, and the AgentStateManager.cs and CallStateManager.cs files in to configure call and agent states. These files provide pre-wired methods and instructions (in the form of comments) to help you create a CTI Desktop Manager component.  
  
  ![Manage CTI Desktop Manager](../unified-service-desk/media/usd-manage-cti-desktop-manager.png "Manage CTI Desktop Manager")  
  
<a name="CustLookup"></a>   
## <a name="raise-a-search-request-when-a-call-arrives"></a>Raise a search request when a call arrives  
 When a new call arrives, you can invoke a search request to look up the automatic number identification (ANI) number in a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps repository, get extra information, such as first name, last name, and so on, and create a session. [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] provides the [CtiLookupRequest](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctilookuprequest) class that describes a customer lookup request that the CTI system sends to a customer search provider. This class describes common data elements that the CTI system will provide. It also gives you the ability to add custom data to the request.  
  
 The customer lookup or search is implemented depending on whether you are searching in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] or UII:  
  
- **Unified Service Desk**: The search request is handled by the Global Manager hosted control.  
  
- **User Interface Integration (UII)**: The lookup request is sent to [ICustomerSearch](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.core.icustomersearch), and it is up to you how you want to implement the search control. You can also send additional data to the search request using the [String)](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctilookuprequest.addlookuprequestitem\(system.string,system.string\)) method. UII provides you project templates to create a Windows Forms-based or WPF-based customer search control with the CTI search request pre-wired.  
  
<a name="CallData"></a>   
## <a name="access-call-data-and-events"></a>Access call data and events  
 Use the [CallInfoData](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.callinfodata) class to access information about a call that is in process in [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] desktop (such as [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]). The following example shows the syntax of this class:  
  
```  
CallInfoData calldata = GetCallInfoData(ctiCallRefCallId);  
```  
  
<a name="CallActions"></a>   
## <a name="enable-or-disable-call-actions"></a>Enable or disable call actions  
 Use the [CtiCallActionOptions](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.cticallactionoptions) class to enable or disable call actions. The following example code shows how to use this class to handle a call.  
  
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
## <a name="configure-cti-desktop-manager-hosted-control-in-unified-service-desk"></a>Configure CTI Desktop Manager hosted control in Unified Service Desk  
 After you have created the CTI Desktop Manager along with your CTI connector, you must configure these as hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] provides a hosted control of type **CTI Desktop Manager**  that can be used to configure your CTI Desktop Manager in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. The CTI Connector should be configured as a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure a hosted control for CTI Connector in Unified Service Desk](../unified-service-desk/create-cti-connector.md#Configure)  
  
1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  
  
2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement apps** > **Settings** > **Unified Service Desk**.  
  
3. On the **Unified Service Desk** page, click **Hosted Controls**.  
  
4. Trên trang **Kiểm soát Tổ chức**, bấm vào **Mới**.  
  
5. On the **New Hosted Control** page, specify the following values:  
  
   |Trường|Value|  
   |-----------|-----------|  
   |Tên|Give name as per your choice.|  
   |USD Component Type|CTI Desktop Manager|  
   |Nhóm hiển thị|Bảng điều khiển bị ẩn|  
   |URI cụm tổ hợp|This is the name of your assembly (.dll) file that you built in the previous step.|  
   |Loại cụm tổ hợp|This is the name of your assembly followed by a dot, and then the class name of your CTI Connector. For example, if your assembly name is MyCtiManager, and the name of the class of your CTI project is DesktopManager, then you must type the following in this field: MyCtiManager.DesktopManager.|  
  
   ![Configure a CTI Desktop Manager hosted control](../unified-service-desk/media/usd-cti-desktop-manager-hosted-control.png "Configure a CTI Desktop Manager hosted control")  
  
6. Click **Save** to create the hosted control.  
  
> [!IMPORTANT]
>  After you have configured the CTI Desktop Manager hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], you must configure:  
> 
> - Actions for your CTI Desktop Manager hosted control. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Actions supported for telephony functions](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md#Actions)  
>   - Window navigation rules to route the CTI search requests appropriately to create sessions and display the search results in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)][!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [CTI search](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md#CTISearch)  
  
### <a name="see-also"></a>Xem thêm  
 [Configure the CTI Desktop Manager hosted control for generic listener adapter](../unified-service-desk/use-generic-listener-adapter-unified-service-desk.md#Configure)   
 [Create a CTI Connector](../unified-service-desk/create-cti-connector.md)   
 [Create a CTI Control](../unified-service-desk/create-cti-control.md)   
 [Walkthrough: Use CTI Desktop Manager ro create a CTI adapter](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md)   
 [UII Computer Telephony Integration (CTI) framework](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)
