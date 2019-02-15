---
title: Build web applications using Server-to-Server (S2S) authentication (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Read how you can use server-to-server (S2S) authentication to securely and seamlessly communicate with Dynamics 365 for Customer Engagement apps through your web applications and services and know about various scenarios where you can use S2S authentication
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 11ce3adf-8a27-430e-a153-124522787ad9
caps.latest.revision: 9
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ac4b525c7d10beb3b5d5187df389068d75c135c6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387192"
---
# <a name="build-web-applications-using-server-to-server-s2s-authentication"></a>Build web applications using Server-to-Server (S2S) authentication

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Tính năng này được đưa ra trong [!INCLUDE[pn_crm_8_2_0_online](../includes/pn-crm-8-2-0-online.md)].  

 Use server-to-server (S2S) authentication to securely and seamlessly communicate with [!INCLUDE[pn_crm_8_2_0_online_subsequent](../includes/pn-crm-8-2-0-online-subsequent.md)] with your web applications and services. Xác thực S2S là cách thông thường mà ứng dụng đã đăng ký trên [!INCLUDE[pn_microsoft_appsource](../includes/pn-microsoft-appsource.md)] sử dụng để truy cập dữ liệu [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] của người đăng ký của họ.  

 S2S authentication means you don’t need to use a paid [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] user license when you connect to [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] tenants. There is no license fee for the special *application user* account you will use with S2S authentication. With S2S authentication a special [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] unlicensed application user account is created and includes information about your application registered with [!INCLUDE[pn_azure_active_directory](../includes/pn-azure-active-directory.md)] (Azure AD). Rather than user credentials, the application is authenticated based on a service principal identified by an Azure AD Object ID value which is stored in the [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] application user record. The [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] application user is associated with a custom security role which controls the kinds of data and operations the application is allowed to perform.  

 Tất cả hoạt động do ứng dụng hoặc dịch vụ của bạn sử dụng S2S sẽ được thực hiện dưới dạng người dùng ứng dụng bạn cung cấp hơn là người dùng đang truy cập ứng dụng của bạn. If you want your application to perform data operations on behalf of a specific user, such as the one who is interacting with your application, you can apply impersonation when the custom security role applied to your application service principal has the privileges required. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Impersonate another user](org-service/impersonate-another-user.md)  

 A web application or service which uses S2S authentication is responsible for controlling access to the data that it has access to. This is typically done using an OpenID Connect provider. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [http://openid.net/connect/](http://openid.net/connect/).  

## <a name="server-to-server-authentication-scenarios"></a>Server-to-Server authentication scenarios  
 There are two scenarios where you can apply S2S authentication.  


|   Kịch bản    |  Mô tả |
|---------------|--------------|
| Multi-Tenant  | This is the most common scenario and the one which is used for apps distributed using [!INCLUDE[pn_microsoft_appsource](../includes/pn-microsoft-appsource.md)].<br /><br /> Each [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] tenant is associated with an Azure AD tenant. Your web application or service is registered with your Azure AD tenant.<br /><br /> In this scenario any [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] tenant can potentially use your multi-tenant application after they grant consent for the application to access data in their tenant. |
| Single-Tenant | This scenario typically applies to [!INCLUDE[pn_crm_8_2_0_online_subsequent](../includes/pn-crm-8-2-0-online-subsequent.md)] organizations who want to develop apps for their own tenant and who don’t intend to distribute them to other [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] organizations.<br /><br /> An enterprise can create a web application or service to connect to all the [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] organizations for their tenant.<br /><br /> In this scenario, your web application or service will only be able to connect to [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] organizations using the same Azure AD tenant. |

 Both scenarios have common elements but there are some differences. Since multi-tenant is the most common scenario, the [Use Multi-Tenant Server-to-server authentication](use-multi-tenant-server-server-authentication.md) content will describe how you can use S2S in this scenario and include notes where the options for single-tenant configuration is different. [Use Single-Tenant Server-to-server authentication](use-single-tenant-server-server-authentication.md) will provide an overview of this scenario and refer to the procedures described in the multi-tenant S2S authentication content.  

### <a name="see-also"></a>Xem thêm  
 [Walkthrough: Multi-tenant server-to-server authentication](walkthrough-multi-tenant-server-server-authentication.md)   
 [Use Single-Tenant Server-to-server authentication](use-single-tenant-server-server-authentication.md)   
 [Build web applications using Server-to-Server (S2S) authentication](build-web-applications-server-server-s2s-authentication.md)   
 [Connect to Dynamics 365 for Customer Engagement apps](connect-customer-engagement.md)
