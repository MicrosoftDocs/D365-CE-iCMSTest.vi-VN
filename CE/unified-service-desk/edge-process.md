---
title: Edge Process hosting method for your controls in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn about the Edge Process hosting methods for your controls in Unified Service Desk.
ms.custom:
- dyn365-USD
ms.date: 12/19/2018
ms.service: dynamics-365-customerservice
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 (online)
- Dynamics 365 (on-premises)
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: D9E7AED8-1D3A-4E62-BD15-7C5CF153EB4E
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
monikerRange: '>= dynamics-usd-4'
ms.openlocfilehash: 0de3a2bf3b451074fb7fac04821484e909e3cc0c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385517"
---
# <a name="preview-edge-process"></a>Preview: Edge Process

[!INCLUDE[cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

The Edge Process browser control hosts your controls in individual Edge process instances and displays them in tabs in the Unified Service Desk client application. It facilitates predictable and secure page rendering by making sure that if your web application works in Edge, it will work in Unified Service Desk. You can select **Edge Process** as the hosting method for the **CRM Dialog**, **CRM Page**, **KM Control**, **Unified Interface Page**, **Unified Interface KM Control** and **Standard Web Application** type of hosted controls.

![Edge process hosted control setting](media/edge-process-hosted-control-setting.gif "Edge process hosted control setting")

The advantages of using the Edge process hosting method are as follows:

![Advantages of Edge Process](media/advantages-edge-process.PNG "Advantages of Edge Process")

- Webpages, including Dynamics 365 pages, render faster in Microsoft Edge.
- Microsoft Edge is a modern browser with better process and memory management.
- Microsoft Edge is the default browser for the Windows 10 operating system.
- it provides easy configurations to host the applications in Unified Service Desk.
- It provides improved reliability and supportability for browser-specific issues

> [!NOTE]
> To use **Edge Process**, you must have the latest Windows 10 operating system (Windows 10 October 2018 release).

## <a name="edge-process-settings"></a>Edge Process settings

You can set the **Edge Process** on the hosted controls (exisitng hosted controls and new hosted controls) to host applications. This allows you to choose the hosted controls that uses **Edge Process** based on your requirements. More information: [Create a hosted control with hosting type as Edge](edge-process.md#create-a-hosted-control-with-hosting-type-as-edge)

If you want to set the **Edge Process** to host the applications for an entire organization, then use the **GlobalBrowserMode** Global UII option and specify the value as **Edge**. More information: [Enable Edge for Unified Service Desk on client desktop](edge-process.md#enable-edge-for-unified-service-desk-on-client-desktop)

If you want to set the **Edge Process** only for some agents in your organization, then in the **UnifiedServiceDesk.exe.config** file, add the **GlobalBrowserMode** key with the value as **Edge**. More information: [Enables Edge for an entire organization](edge-process.md#enable-edge-for-an-entire-organization)

### <a name="order-of-precedence"></a>Order of precedence

- Setting the **GlobalBrowserMode** Global UII option value as **Edge**, takes precedence over the individual hosted control settings. <br><br>For example, some hosted controls have hosting type as **IE Process** and/or **Internal WPF**. At the organization level, you set **GlobalBrowserMode** Global UII option value as **Edge**. In this scenario, the Global UII option takes precedence and configuration uses the **Edge Process** to host the applications. 

- Setting the **GlobalBrowser** mode key to **Edge** in the **UnifiedServiceDesk.exe.config** file for a particular client desktop, takes precedence over the individual hosted control settings.<br><br>For example, some hosted controls have hosting type as **IE Process** and/or **Internal WPF**. For a few agents, in their client desktops, you have set **GlobalBrowser** mode key to **Edge** in the **UnifiedServiceDesk.exe.config** file. The value set in the **UnifiedServiceDesk.exe.config** file take precedence and configuration uses the **Edge Process** to host the applications.

Setting the **GlobalBrowser** mode key to **Edge** in the **UnifiedServiceDesk.exe.config** file for a particular client desktop, takes the precedence over other settings. 

## <a name="enable-edge-process"></a>Enable Edge Process

Enable the **Edge Process** by doing one of the following ways:

- Create a individual hosted control with hosting type as Edge
- Enable for individual client desktops
- Enable for entire an organization

> [!NOTE]
> Enable the **Edge Process** either for individual client desktops or for entire organization.

### <a name="create-a-hosted-control-with-hosting-type-as-edge"></a>Create a hosted control with hosting type as Edge

When you are creating a new hosted control, you can select **Edge Process** as the **Hosting Type**.

1. Sign in to Dynamics 365.

2. Go to **Settings** > **Unified Service Desk**.

3. Select **Hosted Controls**. Trang Hiển thị có kiểm soát tổ chức có sẵn.

4. To create a new hosted control, select **New**.

5. On the **New Hosted Control** page, specify the details and select **Edge process** from the **Hosting Type** drop-down.<br>
![Edge Process hosted control](media/edge-process-hosted-control.PNG "Edge Process hosted control")

6. Select **Save** to create the hosted control.

### <a name="enable-edge-for-unified-service-desk-on-client-desktop"></a>Enable Edge for Unified Service Desk on client desktop

1. Go to directory where you have installed Unified Service Desk and double-click to open the **UnifiedServiceDesk.exe.config** file.
Example path: `C:\Program Files\Microsoft Dynamics CRM USD\USD`

2. Under the `<appSettings>` section add the new key.<br>
`<add key="GlobalBrowserMode" value="Edge"/>`

  > [!div class="mx-imageBorder"]
  > ![Edge Process configuration setting key](media/edge-process-app-config-file-setting.PNG "Edge Process configuration setting key")

3. Save the file.

### <a name="enable-edge-for-an-entire-organization"></a>Enable Edge for an entire organization

Add a new Global UII option for your organization named **GlobalBrowserMode**. Specify the value as **Edge**.

![Edge process global uii option](media/edge-process-global-uii-option.gif "Edge process global uii option")

1. Sign in to Dynamics 365.

2. Go to **Settings** > **Unified Service Desk** > **Options**.

3. On the **Active UII Options** page, select **New**.

4. Choose **Others** for the **Global Option** field.

5. Type **GlobalBrowserMode** for the **Name** field.

6. Type **Edge** for the **Value** field.

7. Chọn **Lưu**.

## <a name="debug-edge-process-using-microsoft-edge-devtools-preview"></a>Debug Edge Process using Microsoft Edge DevTools Preview

With Edge process, you can use the **Microsoft Edge DevTools Preview** tool as a JavaScript debugger. Edge DevTools helps you debug the webpage locally or remotely.

In the panel, you can see all the active Edge process. Select the desired webpage from the active list to open a new instance.

More information: [Microsoft Edge DevTools Preview](https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide)

## <a name="runscript-action-is-asynchronous-in-edge-process"></a>RunScript action is asynchronous in Edge Process

The Edge browser support only the asynchronous operations, and the RunScript action will be asynchronous.
If your custom code execution is dependent on the return value provided by RunScript action that injects JavaScript into the main frame of the application, then your custom code execution may fail.

For example, Your custom code has a RunScript actions that injects the JavaScript into the main frame of the application followed by an operation or another RunScript action. The RunScript action is invoked and returns a value after the JavaScript injection. If the subsequent operation or another RunScript action executes based on the return value provided by the executed RunScript action, then subsequent operations of your custom code will fail.

### <a name="scenario-example"></a>Scenario example 

Whenever you open a case, verify whether the case has been open for 10 or more days, then display a message in a dialog. When you perform an action on the dialog box, the phone call page is opened for further operations.

To perform the above-mentioned scenario, you must have an action call that executes a **RunScript** action and returns a value for the next operation. The data on the action call calculates the number of days a case is open. 

Now, you must create an action call with action as **ExecuteOnDataAvailable**, and the data field must have the return value of the first action call. That is, the return value will have the form `[[$Return.ActionCallName]]`. This ensures that after the first action is executed and the return is available, this action call will be executed.

Next, you must create a sub action call to show the number of days a case is in the open state. The data field will use the return value form the first action call, that is, `[[$Return.ActionCallName]]`.

You must create another sub action call to open the phone call page and perform the next operation. After seeing the message, you select the **OK** button on the dialog, and this causes the phone call page to opens.

Let us see what configurations you need to do create for the above-mentioned scenario.

### <a name="step-1-create-a-hosted-control"></a>Step 1: Create a hosted control

1. Go to **Settings** > **Unified Service Desk** > **Hosted Controls**.

2. Chọn **+ Mới**.

3. Add the following details and save the hosted control.

| Trường | Value |
|--------|---------|
| Tên | Sự cố |
| Tên Hiển thị | `[[incident.title]]` |
| Unified Service Desk Component Type | Unified Interface Page |
| Loại lưu trữ | Edge Process |
| Nhóm hiển thị | Bảng điều khiển chính |

### <a name="step-2-create-two-action-calls"></a>Step 2: Create two action calls

1. Go to  **Settings** > **Unified Service Desk** > **Action Calls**.

2. Select **+ New**.

3. Add the following details and save the action call.

| Trường | Value |
|--------|---------|
| Tên | FindNoOfDaysCaseBeingOpened |
| Thứ tự | 1 |
| Kiểm soát được lưu trữ | Sự cố |
| Hành động | Chạy mã lệnh |
| Dữ liệu | function findAge(dateString)</br>{</br>if("[[incident.statuscode]]".indexOf("1") > -1){</br>var date1 =new Date(dateString);</br>var date2 =new Date();</br>var timeDiff = Math.abs(date2.getTime() - date1.getTime());</br>var diffDays = Math.ceil(timeDiff / (1000 * 3600 * 24));</br>return diffDays.toString();</br>}</br>return 0;</br>}</br>findAge("[[incident.createdon]]"); |

4. Repeat steps 2 and 3 to create another action call.

| Trường | Value |
|--------|---------|
| Tên | DaysValue|
| Thứ tự | 2 |
| Kiểm soát được lưu trữ | CRM Global Manager |
| Hành động | ExecuteOnDataAvailable |
| Dữ liệu | `[[$Return.FindNoOfDaysCaseBeingOpened]]` |

#### <a name="step-3-create-two-action-calls-and-add-them-under-the-daysvalue-action-call"></a>Step 3: Create two action calls, and add them under the DaysValue action call

1. Go to **Settings** > **Unified Service Desk** > **Action Calls**.

2. Select **+ New**.

3. Add the following details and save the action call.

| Trường | Value |
|--------|---------|
| Tên | DisplayMessageForCaseOpen |
| Kiểm soát được lưu trữ | CRM Global Manager |
| Hành động | DisplayMessage |
| Dữ liệu |    text=No of days case is in open state: [[$Return.FindNoOfDaysCaseBeingOpened]]<br>
caption=Case is open |

4. Repeat steps 2 and 3 to create another action call.

| Trường | Value |
|--------|---------|
| Tên | OpenPhoneCallPage |
| Kiểm soát được lưu trữ | Cuộc gọi Điện thoại  |
| Hành động | New_CRM_Page |
| Dữ liệu |        LogicalName=phonecall<br>description=Long pending case more than 9 days <br> subject=Long pending case <br> |
| Điều kiện | "[[$Return.FindNoOfDaysCaseBeingOpened]]">9 |

5. From the list of action calls, select the **DaysValue** action call.

6. In the navigation bar, next to the **DaysValue** action call, select the *>* icon, and select **Sub Action Call**.

7. Select the **ADD EXISTING ACTION CALL** option. In the search field, type the action **DisplayMessageForCaseOpen**, and select the search icon.

8. To add the action call, select the action call name that appears.

9. Perform the steps 7 and 8 to add the **OpenPhoneCallPage** action call.

10. Lưu các thay đổi.

#### <a name="step-4-add-the-action-calls-to-the-pageready-event"></a>Step 4: Add the action calls to the PageReady event

1. Go to  **Settings** > **Unified Service Desk** > **Events**.

2. Select the **PageReady** event for the **Incident** hosted control from the list of events.

3. On the event page, under the **Active Actions** area, click **+** to add action calls.

4. A search box appears, type **FindNoOfDaysCaseBeingOpened** and select the search icon and select the action call. The action call appears under the **Active Actions** area.

5. Repeat step 4 to add the **DaysValue** action.

6. Save the changes.

## <a name="edgesingleprocess-global-uii-option"></a>EdgeSingleProcess global UII option

With the Edge WebView control, each domain will have its own process. If your organization requires common authentication modes across different domains, the Edge process might not support the same authentication.

To use common authentication mode across different domains, use the `EdgeSingleProcess` global UII option to ensure all the processes with different domains are created in a single process at the run-time. 

To use the `EdgeSingleProcess`, you must add the UII option and set the value to `True`. More information: [EdgeSingleProcess](admin/manage-options-unified-service-desk.md)

### <a name="add-the-uii-option"></a>Add the UII option

1. Đăng nhập vào [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]

3. Select **Options**.  

4. Select **New** on the **Active UII Options** page.

5. Choose **Others** for the **Global Option** field.

6. Type **EdgeSingleProcess** for the **Name** field.

7. Type **True** for the **Value** field.

8. Chọn **Lưu**.

> [!NOTE]
> If you set the value as `False` or leave the field blank, the option will be disabled.


## <a name="sign-out-from-sessions-when-using-the-edge-process"></a>Sign out from sessions when using the Edge Process

To sign out from sessions when using the Edge process, you must configure the sign-out URL using the **Navigate** action on the hosted control. For example, the sign-out URL of Dynamics 365 for Customer Engagement apps is `url=/main.aspx?signout=1`.

## <a name="limitations"></a>Giới hạn

To learn about the limitations of the Edge process, see [Edge process limitations](release-notes.md)

## <a name="see-also"></a>Xem thêm  
 [Tạo hoặc chỉnh sửa kiểm soát tổ chức](../unified-service-desk/create-edit-hosted-control.md)  

 [Tham chiếu loại kiểm soát tổ chức và hoạt động/sự kiện](../unified-service-desk/hosted-control-types-action-event-reference.md)   

 [Quản lý kiểm soát tổ chức, hành động và sự kiện](../unified-service-desk/manage-hosted-controls-actions-events.md)
