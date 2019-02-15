---
title: Geo to geo migrations for Dynamics 365 for Customer Engagement apps (online) | MicrosoftDocs
ms.custom: ''
ms.date: 07/12/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement  (online)
- Dynamics 365 for Customer Engagement  Version 9.x
ms.assetid: c5b836a1-8f9d-42bd-8c11-cb81c68b97d3
caps.latest.revision: 17
author: jimholtz
ms.author: jimholtz
manager: kvivek
search.audienceType:
- admin
search.app:
- D365CE
- Powerplatform
ms.openlocfilehash: 77dc507ca82881b71142ee7c7f10334a691744da
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385431"
---
# <a name="geo-to-geo-migrations"></a>Di chuyển theo vùng địa lý

[!INCLUDE[cc-applies-to-update-9-0-0](../../includes/cc_applies_to_update_9_0_0.md)]

We continue to open new datacenter regions for [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] for business services, and to add datacenters to existing regions.  

 The Geo Migration feature for [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] will allow customers to move their instances in a single tenant from one region to another. Giao diện người dùng hoặc phiên bản không bị thay đổi trong quá trình này. In the case of a [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] instance residing in an [!INCLUDE[pn_Office_365](../../includes/pn-office-365.md)] instance in a single tenant, moving the [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] instance doesn’t move the [!INCLUDE[pn_Office_365](../../includes/pn-office-365.md)] instance; they are separate services. Your [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] instance will still appear in your tenant alongside the [!INCLUDE[pn_Office_365](../../includes/pn-office-365.md)] instance.  

> [!IMPORTANT]
>  For versions prior to [!INCLUDE [pn-crm-9-0-0-online](../../includes/pn-crm-9-0-0-online.md)], you can move individual [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] instances from one geographical region to another. When you do so, your tenant becomes a multiregional tenant. Regional features are enabled in the [!INCLUDE[pn_dyn_365_admin_center](../../includes/pn-dyn-365-admin-center.md)].  
> 
>  To request a regional migration, please contact your account manager or  see [Technical Support](../../admin/contact-technical-support.md).  
> 
>  [!INCLUDE [pn-crm-9-0-0-online](../../includes/pn-crm-9-0-0-online.md)] does not currently support regional migration. Hãy quay lại sau để kiểm tra tính khả dụng. 

## <a name="impact-of-migrating"></a>Impact of migrating  
 Moving an instance to a different region changes your tenant to be multiregional - enabling regional features in the [!INCLUDE[pn_dyn_365_admin_center](../../includes/pn-dyn-365-admin-center.md)].  

 The other significant change is to your organization URL. Each of the [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] regional datacenters has a unique identifier in the URL. When your organization is moved from one regional datacenter to another this identifier will change. Ví dụ:  

-   South America (LATAM/SAM) = .crm2.dynamics.com  

-   Canada (CAN) = .crm3.dynamics.com  

-   Europe, Middle East, Africa (EMEA) = .crm4.dynamics.com  

-   Asia Pacific (APAC) = *.crm5.dynamics.com  

-   Australia (OCE) = *.crm6.dynamics.com  

-   Japan (JPN) = *.crm7.dynamics.com  

-   India (IND) = *.crm8.dynamics.com  

-   United Kingdom (UK) = *.crm11.dynamics.com  

 [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Direct sign in to Dynamics 365 for Customer Engagement apps (online)](../../admin/sign-in-office-365-apps.md#BKMK_directsignin) and [Discover the URL for your organization using the Organization Service](../../developer/org-service/discover-url-organization-organization-service.md)

 For example, if your existing organization URL is https://myorg.crm<strong>5</strong>.dynamics.com and you request it to be moved to Australia, the new organization URL will be https://myorg.crm<strong>6</strong>.dynamics.com.  

 You’ll need to update any direct references to your [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)] organization URL.  

> [!NOTE]
>  Organization URLs must be unique. If your organization name has already been reserved in the destination datacenter, it won’t be available. In the unlikely event this happens, we will work with you to decide how to proceed.  

 To see the datacenter regions, go to [Where is my data?](http://o365datacentermap.azurewebsites.net/) and then click **Select Your Region**.  

 The following topics have information that could be helpful to understand the move process:  

-   [New datacenter regions for Dynamics 365 for Customer Engagement apps (online)](new-datacenter-regions.md)  

-   [About Microsoft Cloud Australia](about-microsoft-cloud-australia.md)  

-   [About Microsoft Cloud Canada](about-microsoft-cloud-canada.md)  

-   [Giới thiệu về trung tâm dữ liệu Microsoft Cloud Germany](about-microsoft-cloud-germany.md)

-   [About Microsoft Cloud Japan](about-microsoft-cloud-japan.md)  

-   [About Microsoft Cloud India](about-microsoft-cloud-india.md)  

## <a name="how-the-move-works"></a>Cách di chuyển  
 You’ll be provided with a list of prerequisites and post-requisites for your migration. For more information, download [Geo to geo migration information for CRM Online](http://go.microsoft.com/fwlink/p/?LinkID=619083). The following table describes what [!INCLUDE[cc_Microsoft](../../includes/cc-microsoft.md)] does before, during, and after your move.  


|                         |                                                         Trước khi di chuyển                                                          |                                                                                                                                                                                                                                                  Trong quá trình di chuyển                                                                                                                                                                                                                                                  |                                                                                                                                                   Sau khi di chuyển                                                                                                                                                   |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Việc Microsoft làm** | **Thông báo**<br /><br /> Your support representative or Account Manager will work with you to request a move and scheduling. | **Chuyển tiếp**<br /><br /> Cut-over times for each service depend on the number of users and the amount of data. This step can take 1 to 6 hours for smaller organizations, but may take up to 48 hours for large organizations. The cut-over is done during the evening or over a weekend.<br /><br /> There is a step that will require your involvement, which is to re-enter the encryption key in [!INCLUDE[pn_crm_online_shortest](../../includes/pn-crm-online-shortest.md)]. This can happen at a time that suits you but the migration process will be on hold until you complete this action. | **Thông báo và hỗ trợ**<br /><br /> You will be alerted by email or telephone when your instance is migrated to the new datacenter.<br /><br /> After your geo has migrated you can perform the post requisite steps - primarily changing your new URLs with any associated Dynamics 365 for Customer Engagement apps plugins or services. |

 Chúng tôi sẽ tuân theo các điều khoản của [Thỏa thuận cấp độ dịch vụ của Microsoft Online Services](http://go.microsoft.com/fwlink/p/?LinkID=523897) đối với mọi quá trình di chuyển.  

### <a name="see-also"></a>Xem thêm  
 [Dynamics 365 for Customer Engagement apps (online) terminology](../../admin/online-terminology.md)   
 [Thêm và chỉnh sửa các phiên bản đa vùng](../../admin/add-edit-multiregional-instances.md)   
 [Manage Microsoft Dynamics 365 for Customer Engagement apps (online) instances](../../admin/manage-online-instances.md)
