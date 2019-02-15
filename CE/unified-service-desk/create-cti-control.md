---
title: Create a CTI Control | MicrosoftDocs
description: The topic explains on how to create a CTI control.
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
ms.assetid: c9e49c30-dc33-454e-b067-c90ecca6d659
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: d0884c890eb29e0f38eb52b746937d628bde572c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386496"
---
# <a name="create-a-cti-control"></a>Create a CTI Control
To manage agent states and call states, [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)] scenarios require the following user interface (UI) controls:  

- **Agent state management control**: Displays the current state of the agent within a [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] desktop (such as [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]. This control doesn’t need to be tied to the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system, but it allows you to map [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] agent states with the current agent state, which is the visual state of the agent desktop.  

- **Call control**: Provides buttons that the agent can use to make a call, answer a call, put a call on hold, transfer a call to another agent, or hang up.  

  Both of these controls are normal [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted controls that inherit from either the [HostedControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedcontrol) or [HostedWpfControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.aif.hostedapplication.hostedwpfcontrol) class. You can also choose to merge both the controls into a single [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Use UII hosted controls with Unified Service Desk](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md)  

## <a name="interfaces-for-implementing-a-cti-control"></a>Interfaces for implementing a CTI Control  
 Use the following interfaces to implement the user interface of a CTI Control.  

### <a name="ictiagentstatecontrol"></a>ICtiAgentStateControl  
 The [ICtiAgentStateControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictiagentstatecontrol) interface is a specialized interface for describing a hosted control that is used for processing and/or displaying agent state information. This interface contains the [Boolean)](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictiagentstatecontrol.setagentstate\(system.guid,system.string,system.string,system.boolean\)) method that’s used to set the state of an agent.  

### <a name="idesktopuseractionsconsumer"></a>IDesktopUserActionsConsumer  
 The [IDesktopUserActionsConsumer](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.core.idesktopuseractionsconsumer) interface is not specific to [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)], but it is typically used by the CTI Controls to provide access to desktop operations. It has two members:  

- [DesktopLoadingComplete](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.core.idesktopuseractionsconsumer.desktoploadingcomplete): Raised when the desktop has completed loading. This is raised in a separate thread from the main desktop UI thread.  

- [IDesktopUserActions)](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.core.idesktopuseractionsconsumer.setdesktopuseractionsaccess\(microsoft.uii.desktop.core.idesktopuseractions\)): Used by the desktop loader to set a pointer to itself in the hosted control that implemented the [ICtiEnabledControlConsumer](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictienabledcontrolconsumer) interface. It is the pointer to the desktop interface (shell).  

  By implementing this interface, you get access to all user actions, as shown in the following example.  

```  
bool AppExistsInUI(string applicationName);  
bool CloseDynamicApplication(string applicationName);  
bool CloseSession();  
bool CloseSession(Session sessionToClose);  
bool CreateDynamicApplication(string applicationName);  
WorkflowData GetCurrentWorkflowState();  
bool SetFocusOnApplication(string applicationName);  
string UserDefinedCommand(string command, string request);  

```  

### <a name="ictienabledcontrolconsumer"></a>ICtiEnabledControlConsumer  
 The [ICtiEnabledControlConsumer](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictienabledcontrolconsumer) interface describes a hosted control that will accept pointers to the [CtiCallStateManager](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.cticallstatemanager) and the [CtiAgentStateManager](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ctiagentstatemanager).  

 This interface has method definitions to perform following functions:  

- [Object)](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictienabledcontrolconsumer.setmanagers\(system.object,system.object\)): Called by UII when a control that implements this interface is initialized.  

- [SessionControllerEventArgs)](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictienabledcontrolconsumer.sessioncloseevent\(microsoft.uii.csr.sessioncontrollereventargs\)): Called by UII when a session is closing.  

  The [ICtiEnabledControlConsumer](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictienabledcontrolconsumer) interface uses the [IsManagersSet](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictienabledcontrolconsumer.ismanagersset) property to set or get whether the [Object)](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.cti.core.ictienabledcontrolconsumer.setmanagers\(system.object,system.object\)) method has been called successfully.  

<a name="Configure"></a>   
## <a name="configure-the-cti-control-hosted-control-in-unified-service-desk"></a>Configure the CTI Control hosted control in Unified Service Desk  

1. Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.  

2. On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement apps** > **Settings** > **Unified Service Desk**.  

3. Trên trang **Unified Service Desk**, bấm vào **Kiểm soát Tổ chức**.  

4. Trên trang **Kiểm soát Tổ chức**, bấm vào **Mới**.  

5. On the **New Hosted Control** page, specify the following values:  


   |         Trường         |                                                                                                                                                                                                 Value                                                                                                                                                                                                 |
   |-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |         Tên          |                                                                                                                                                                                            Specify a name.                                                                                                                                                                                            |
   |  USD Component Type   |                                                                                                                                                                                        CCA Hosted Application                                                                                                                                                                                         |
   |  Ứng dụng được lưu trữ   |                                                                                                                                                                                            Kiểm soát được lưu trữ                                                                                                                                                                                             |
   | Application is Global |                                                                                                                                                                                                Đã kiểm tra                                                                                                                                                                                                |
   |     Nhóm hiển thị     |                                                                                                                                                                                               CtiPanel                                                                                                                                                                                                |
   |        Bộ điều hợp        |                                                                                                                                                                                            Use No Adapter                                                                                                                                                                                             |
   |     URI cụm tổ hợp      |                                                                                                                                                          This is the name of your assembly (.dll) file that you built in the previous step.                                                                                                                                                           |
   |     Loại cụm tổ hợp     | This is the name of your assembly followed by a dot, and then the class name of your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] Control. For example, if your assembly (dll) name is `MyCtiControl`, and the name of the class of your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] project is `CtiControl`, type the following in this field: `MyCtiControl.CtiControl`. |


6. Choose **Save** to create the hosted control.  

### <a name="see-also"></a>Xem thêm  
 [Considerations for creating a CTI adapter for Unified Service Desk](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md)   
 [Tạo trình kết nối CTI](../unified-service-desk/create-cti-connector.md)   
 [Create a CTI Desktop Manager](../unified-service-desk/create-cti-desktop-manager.md)   
 [UII Computer Telephony Integration (CTI) framework](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)
