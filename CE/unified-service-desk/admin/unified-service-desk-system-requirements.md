---
title: Unified Service Desk for Dynamics 365 for Customer Engagement apps system requirements | MicrosoftDocs
description: 'Describes the supported dependent and optional components you need to install and use Unified Service Desk for Dynamics 365 for Customer Engagement apps. '
keywords: ''
ms.date: 11/02/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD, dyn365-admin
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 8a0e7dc4-5d32-412a-ae72-b6ce010c1c85
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.openlocfilehash: d733f3fef8dbaa5157d65ecdcdf560e73e8556c7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382570"
---
# <a name="requirements"></a>Yêu cầu
This topic provides information about the system requirements for installing the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application and deploying the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sample applications on a [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps instance.  

<a name="hardware"></a>   
## <a name="hardware-requirements-for-the-unified-service-desk-client"></a>Hardware requirements for the Unified Service Desk client  
 The following table lists the minimum and recommended hardware requirements when you run the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.  


| Thành phần |                                           Nhỏ nhất                                           |                                                                                                                                                                            Được đề xuất                                                                                                                                                                            |
|-----------|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bộ xử lý | x86- or x64-bit 1.9 gigahertz (GHz) dual core with SSE2 instruction set or faster processor |                                                                                                                                    x86- or x64-bit 1.9 gigahertz (GHz) dual core with SSE2 instruction set or faster processor                                                                                                                                    |
|  Bộ nhớ   |                                      ^2-GB RAM or more                                       |                                                                                                                                                                         ^4-GB RAM or more                                                                                                                                                                          |
| Đĩa cứng |                            \*1.5 GB dung lượng đĩa cứng trống                            | 12 GB of available hard disk space: 2 GB of available hard disk space for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application files and 10 GB additional available hard disk space for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client log files<br /><br /> 7200 RPM trở lên |

 ^The minimum and recommended memory are for running basic scenarios. The actual memory required for Unified Service Desk increases with the complex configurations and custom development (UI experience).
 
 *Requires disabling [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client logging. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Configure client diagnostic logging in Unified Service Desk](../../unified-service-desk/admin/configure-client-diagnostic-logging-unified-service-desk.md)  

<a name="client"></a>   
## <a name="software-requirements-for-the-unified-service-desk-client"></a>Software requirements for the Unified Service Desk client  
 Để cài đặt ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] trên một máy tính, cần thực hiện những thao tác sau đây:  

- [!INCLUDE[pn_windows_10](../../includes/pn-windows-10.md)], [!INCLUDE[pn_windows_8_1](../../includes/pn-windows-8-1.md)], [!INCLUDE[pn_windows8](../../includes/pn-windows8.md)], hoặc [!INCLUDE[pn_Windows_7](../../includes/pn-windows-7.md)]  

- [!INCLUDE[pn_ie_11](../../includes/pn-ie-11.md)], [!INCLUDE[pn_IE_10](../../includes/pn-ie-10.md)], hoặc <sup>*</sup>[!INCLUDE[pn_IE_9](../../includes/pn-ie-9.md)]  

  > [!Tip]
  > We recommend that you use [!INCLUDE[pn_windows_10](../../includes/pn-windows-10.md)] and [!INCLUDE[pn_ie_11](../../includes/pn-ie-11.md)].
  > 
  > [!IMPORTANT]
  >  Although [!INCLUDE[pn_microsoft_edge](../../includes/pn-microsoft-edge.md)] is currently not supported for use with the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client, you can use [!INCLUDE[pn_ie_11](../../includes/pn-ie-11.md)] with [!INCLUDE[pn_windows_10](../../includes/pn-windows-10.md)].  
  > 
  >  <sup>*</sup> [!INCLUDE[pn_IE_9](../../includes/pn-ie-9.md)] is supported for use only with [!INCLUDE[pn_crm_2013_sp](../../includes/pn-crm-2013-sp.md)] organizations. Also, [!INCLUDE[pn_IE_9](../../includes/pn-ie-9.md)] may work for systems that are not [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  

- [!INCLUDE[pn_NET_Framework_462_long](../../includes/pn-net-framework-462-long.md)] (installed during [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Setup if missing)  

> [!NOTE]
> - [!INCLUDE [pn-unified-service-desk-3-1](../../includes/pn-unified-service-desk-3-1.md)] or higher version installs [!INCLUDE[pn_NET_Framework_462_long](../../includes/pn-net-framework-462-long.md)]. 
> - [!INCLUDE [pn-unified-service-desk-3-0](../../includes/pn-unified-service-desk-3-0.md)] version installs [!INCLUDE[pn_NET_Framework_452_long](../../includes/pn-net-framework-452-long.md)].


- [!INCLUDE[pn_Windows_Identity_Foundation](../../includes/pn-windows-identity-foundation.md)] 3.5 (installed during [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Setup if missing)  

- Độ phân giải màn hình được đề xuất (theo điểm ảnh): 1920 x 1080  

- Mức độ thu phóng được đề xuất trong kính lúp: 100%  

<a name="SampleApps"></a>   
## <a name="software-requirements-for-deploying-unified-service-desk-sample-applications"></a>Software requirements for deploying Unified Service Desk sample applications  
 To deploy a [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sample application, an instance of [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps (online or on-premises), [!INCLUDE[pn_crm_2015](../../includes/pn-crm-2015.md)], or [!INCLUDE[pn_crm_2013_sp](../../includes/pn-crm-2013-sp.md)] is required.  

> [!IMPORTANT]
>  Although you can deploy and use [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sample applications with [!INCLUDE[pn_crm_2015](../../includes/pn-crm-2015.md)] or [!INCLUDE[pn_crm_2013_sp](../../includes/pn-crm-2013-sp.md)], we recommend that you upgrade to [!INCLUDE[pn_crm_2016](../../includes/pn-crm-2016.md)] so you can use the new features available.  
> We recommend that you use Unified Service Desk 4.0 with [!INCLUDE [pn-crm-9-0-0-online](../../includes/pn-crm-9-0-0-online.md)]. [Get Unified Service Desk 4.0 for Dynamics 365 for Customer Engagement apps now](https://go.microsoft.com/fwlink/p/?linkid=2007340).

 For information about the sample applications available for this release, see [Deploy sample Unified Service Desk applications to Dynamics 365 for Customer Engagement server using Package Deployer](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md).  

<a name="packdeploy"></a>   
## <a name="software-requirements-for-the-package-deployer-tool"></a>Software requirements for the Package Deployer tool  
 [!INCLUDE[pn_package_deployer_tool](../../includes/pn-package-deployer-tool.md)] được sử dụng để triển khai các ứng dụng mẫu [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. The tool supports and requires the following technologies:  

- For running the tool, use one of these [!INCLUDE[pn_Windows_Server](../../includes/pn-windows-server.md)] versions: [!INCLUDE[pn_windows_server_2012_r2](../../includes/pn-windows-server-2012-r2.md)], [!INCLUDE[pn_windowsserver2012](../../includes/pn-windowsserver2012.md)], [!INCLUDE[pn_Windows_Server_2008_R2](../../includes/pn-windows-server-2008-r2.md)].

- An instance of [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps (online or on-premises), [!INCLUDE[pn_crm_2015](../../includes/pn-crm-2015.md)], or [!INCLUDE[pn_crm_2013_sp](../../includes/pn-crm-2013-sp.md)].  

- Additionally, [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] 3.0 or later is required if you’ll be using [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] cmdlets for [!INCLUDE[pn_package_deployer_short](../../includes/pn-package-deployer-short.md)] to deploy sample applications. To check your [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] version, open a [!INCLUDE[pn_PowerShell_short](../../includes/pn-powershell-short.md)] window, and then run the following command: `$Host`  

<a name="appvirtual"></a>   
## <a name="software-requirements-for-citrix-xenapp-application-virtualization"></a>Software requirements for Citrix XenApp application virtualization  
 You can install and run the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client as a published app on Citrix XenApp 7.6. This allows agents to access the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client from a central location.  

 You can also configure a Windows application as a virtual application on Citrix XenApp 7.6 that run as a hosted application in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Integrate with Citrix applications](../integrate-citrix-applications.md)  

## <a name="see-also"></a>Xem thêm  
 [Cài đặt ứng dụng Unified Service Desk](../../unified-service-desk/admin/install-upgrade-unified-service-desk-client.md)   
 [Deploy Unified Service Desk packages to Dynamics 365 for Customer Engagement server using Package Deployer](../../unified-service-desk/admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)   
 [Install and Deploy Unified Service Desk](../../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)   