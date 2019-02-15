---
title: Install the Unified Service Desk for Dynamics 365 for Customer Engagement apps client | MicrosoftDocs
description: Learn how  to install the Unified Service Desk for Dynamics 365 for Customer Engagement apps client.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 01/25/2018
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
ms.assetid: d1ad62d9-a401-4941-828f-d3b13d80b38d
author: kabala123
ms.author: kabala
manager: shujoshi
tags:
- MigrationHO
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: b7bac6b2b4e7c93f0b875ff3e4e9dfe1dcb08cbf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382456"
---
# <a name="installing-the-unified-service-desk-client"></a>Installing the Unified Service Desk client
Make sure your computer meets all requirements before you install the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Unified Service Desk system requirements](../../unified-service-desk/admin/unified-service-desk-system-requirements.md)  
  
 [Tải xuống](../download-unified-service-desk.md) tệp thiết lập ứng dụng khách [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] thích hợp (.exe) và lưu vào máy tính của bạn:  
  
- For a 32-bit version of [!INCLUDE[pn_ms_Windows_short](../../includes/pn-ms-windows-short.md)], download the Dynamics365-USD-3.x.x.xxx-i386.exe file.  
  
- For a 64-bit version of [!INCLUDE[pn_ms_Windows_short](../../includes/pn-ms-windows-short.md)], download the Dynamics365-USD-3.x.x.xxx-amd64.exe file.  
  
  
<a name="BKMK_USDwizard"></a>   
## <a name="install-the-unified-service-desk-client-using-the-setup-wizard"></a>Install the Unified Service Desk client using the Setup Wizard  
  
1. Sign in as a user with local Administrators group membership, and then double-click the downloaded file to begin Setup.  
  
2. The [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client installer starts automatically. If it doesn’t, go to the  folder where the extracted installation files are located and run the SetupUnifiedServiceDesk.exe file to start the installation.  
  
3. On the **Microsoft Dynamics 365 for Customer Engagement apps Unified Service Desk** screen, keep the default location or enter the complete path where the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application files will be installed, and then click **Next**.  
  
4. On the **Microsoft Dynamics 365 for Customer Engagement apps Unified Service Desk Installation** screen, choose from the following options:  
  
   - The [!INCLUDE[pn_Microsoft_.Net_Framework](../../includes/pn-microsoft-net-framework.md)] and [!INCLUDE[pn_Windows_Identity_Foundation](../../includes/pn-windows-identity-foundation.md)] prerequisites. You can’t remove these from the installation if these prerequisites are not already installed.  
  
   - **Unified Service Desk**. Because [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is the core component of setup, you cannot continue unless it is selected.  
  
   - **Create a desktop shortcut for Unified Service Desk**. By default, a shortcut will be created for easy launching of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client from the desktop.  
  
   <!--**Keep Unified Service Desk up to date with Windows Update**.   We recommend that you select this option to use Windows Update to automatically apply updates to [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. This option was first introduced in [!INCLUDE[pn_unified_service_desk_2_1](../../includes/pn-unified-service-desk-2-1.md)] and  you'll see it when the computer where you install the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client is not already using Windows Update.   For more information about Windows Update, see [Keep your PC up to date](http://go.microsoft.com/fwlink/p/?LinkId=784862). For information about how to fully manage the distribution of updates released through Microsoft Update, see [Windows Server Update Services](https://technet.microsoft.com/library/bb332157.aspx).-->  
  
5. Bấm vào **cài đặt**.  
  
6. The next screen shows the installation status of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client. When you are prompted to authorize the installation (as a result of User Account Control), click **Yes**.  
  
7. Một thông báo xác nhận xuất hiện khi cài đặt thành công ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. Click **X** to exit the installer or click **Launch** to start the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.  
  
<a name="BKMK_USDupgrade"></a>   
## <a name="upgrade-the-unified-service-desk-client-using-the-setup-wizard"></a>Upgrade the Unified Service Desk client using the Setup Wizard  
  
1. On a computer where a previous version of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client is installed, sign in to the computer as a user with local Administrators group membership, and then double-click the SetupUnifiedServiceDesk.exe file to begin the upgrade.  
  
2. When setup detects the previous version of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client, you'll see the following information:  
  
   **An older version of Unified Service Desk is already installed on your computer. Setup will upgrade Unified Service Desk on your computer**.  
  
3. Bấm vào **tiếp theo**.  
  
4. On the Unified Service Desk Upgrade screen, decide if you want to create a shortcut for the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client. 
   <!--Use Windows Update if the computer is not already set to do so, and then click **Upgrade**.-->
  
5. The next screen shows the installation status of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.  
  
6. A confirmation message appears on successful upgrade of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client. Click **X** to exit the installer or click **Launch** to start the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.  
  
<a name="BKMK_USDsilent"></a>   
## <a name="install-or-upgrade-the-unified-service-desk-client-in-silent-mode"></a>Install or upgrade the Unified Service Desk client in silent mode  
 When [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] setup runs in silent mode, no user interface (UI) is displayed. Instead, you supply the required information at the command prompt.  
  
> [!NOTE]
> - You may be prompted to supply the information due to the computer’s User Account Control Settings. To suppress this message when setup runs, set the User Account Control Setting to **Never notify**. After setup is complete, we recommend you set the User Account Control Setting back to the original notification level.  
> - When the [!INCLUDE[pn_NET_Framework](../../includes/pn-net-framework.md)] is installed as part of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client setup, a restart may be required for setup to continue.  
  
### <a name="command-line-syntax"></a>Command line syntax  
 SetupUnifiedServiceDesk.exe [destination] [Shortcut = [y &#124; n]] [/S] [install/uninstall/help] <!--[optin = [y &#124; n]]-->
  
### <a name="parameters"></a>Tham số  
  
|                   Tham số                    |                                                                                                                                                                                                                                                                                             Mô tả                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| install<br /><br /> uninstall<br /><br /> trợ giúp | Required parameter that performs one of the following functions depending on which parameter you choose:<br /><br /> -   Install. Installs or, if a previous version exists, upgrades the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.<br />-   Uninstall. Uninstalls the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client. Tùy chọn chế độ bảo trì này chỉ có sẵn khi ứng dụng đã được cài đặt.<br />-   Help. Shows information about setup, such as supported parameters and usage. |
|                       /S                       |                                                                                                                                                                                                                                                                                Silent mode. No setup UI is displayed.                                                                                                                                                                                                                                                                                |
|                  điểm đến                   |                                                                                                                                               The folder where the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client files will be installed. By default, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is installed in the c:\program files\Microsoft Dynamics 365 for Customer Engagement USD\ folder.                                                                                                                                                |
|            Shortcut = [y &#124; n]             |                                                                                                                                                           Shortcut=y creates a shortcut to the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] application on the user’s desktop. If you don’t set this parameter, the shortcut is defaulted to y. When you specify Shortcut=n, a shortcut is not created.                                                                                                                                                            |
|                      trợ giúp                      |                                                                                                                                                                                                                                                                                  Shows a list of valid parameters.                                                                                                                                                                                                                                                                                   |

<!-- |/M|Manual mode. Minimal UI is displayed for information to be entered only as needed. If setup has enough information to complete the install, no UI will be displayed when using this parameter. You cannot specify both /S and /M.| removed the content for 3.2.0 (kabala)
|optin = [y &#124; n]|optin = y uses Windows Update to automatically apply updates to [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. If not specified the default is no, which does not use Windows Update for the computer that is not already set to do so.|-->
  
### <a name="examples"></a>Ví dụ  
 This example installs or upgrades the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client in silent mode, creates a shortcut on the desktop.
 <!--uses Windows Update to apply updates to [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].-->
  
```  
SetupUnifiedServiceDesk.exe install Shortcut=y /S  
```  
  <!--optin=y--> This example uninstalls the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client. Note that no UI displays, even when the /S parameter is not used.  
  
```  
SetupUnifiedServiceDesk.exe uninstall  
```  
  
<a name="BKMK_USDNext"></a>   
## <a name="next-step"></a>Bước tiếp theo  
 Deploy the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sample packages on the [!INCLUDE[pn_microsoftcrm_server](../../includes/pn-microsoftcrm-server.md)]. For more information, see [Deploy Unified Service Desk packages to Dynamics 365 for Customer Engagement server using Package Deployer](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md).  
  
<a name="knownissues"></a>   
## <a name="known-issues"></a>Sự cố đã biết  
  
### <a name="unified-service-desk-client-setup-setupunifiedservicedeskexe-hangs-after-you-click-install"></a>Unified Service Desk client setup (SetupUnifiedServiceDesk.exe) hangs after you click Install  
 This can happen when you run setup as a user who does not have local Administrators group membership, using “Run as different user”, and when some Windows User Account Control (UAC) settings have been changed from the default, for example, if the **Admin Approval Mode for the Built-in Administrator account** UAC setting is set to **Disabled** on the local computer where setup runs. By default, Admin Approval Mode for the built-in Administrator account is enabled, but can be disabled through a Group Policy change.  
  
## <a name="see-also"></a>Xem thêm  
 [Install and Deploy Unified Service Desk](../../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)   
 [Cập nhật Unified Service Desk](../../unified-service-desk/admin/update-unified-service-desk-solution.md)   
 
