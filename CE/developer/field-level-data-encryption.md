---
title: Field-level data encryption (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Dynamics 365 for Customer Engagement (online) uses standard SQL Server cell level encryption for a set of default entity attributes that contain sensitive information, such as user names and email passwords. This feature can help organizations meet the compliance requirements associated with FIPS 140-2.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 02ec284f-11bb-4537-b2da-04a69f349815
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4cbda3a4e9b19cbf5d53a977b12277c8aea491f3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385777"
---
# <a name="field-level-data-encryption"></a>Field-level data encryption

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] sử dụng mã hóa mức ô [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] tiêu chuẩn cho tập hợp các thuộc tính thực thể mặc định chứa các thông tin nhạy cảm chẳng hạn như tên người dùng và mật khẩu email. This feature can help organizations meet the compliance requirements associated with FIPS 140-2. Field-level data encryption is especially important in scenarios that leverage the [!INCLUDE[pn_CRM_E-Mail_Router](../includes/pn-crm-e-mail-router.md)], which must store user names and passwords to enable integration between a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance and an email service such as [!INCLUDE[pn_Microsoft_Exchange](../includes/pn-microsoft-exchange.md)].  
  
 [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] users who have the system administrator security role can activate data encryption (or change the encryption key after data encryption is enabled) in the **Settings** > **Data Management** > **Data Encryption** area. After data encryption is activated, it cannot be turned off.  
  
> [!IMPORTANT]
>  For both [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], all new and upgraded organizations have data encryption activated.  
> 
>  When considering the use of data encryption, be sure to keep in mind the following key points:  
> 
> - To help ensure the highest level of security, we recommend that you change the encryption key immediately after creating or updating an organization, and thereafter about once a year.  
>   - Changing the encryption key requires that [!INCLUDE[pn_ssl_short](../includes/pn-ssl-short.md)] be configured on the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] website.  
>   - Auditing cannot be enabled on encrypted fields.  
>   - Encrypted fields cannot be customized.  
>   - Encrypted fields cannot be indexed.  
>   - Encrypted fields can be set and updated by using standard Create, Update, and Delete methods.  
>   - When doing a retrieve of an encrypted field’s value, a **null** is returned.  
  
 The encryption key is required to activate data encryption when you import an organization database into a new deployment or into a deployment that has had the configuration database (MSCRM_CONFIG) recreated after the organization was encrypted. You can copy the original encryption key to Notepad and then paste it into the **Settings** > **Data Management** > **Data Encryption** dialog box after the organization import is completed. When activating data encryption after redeployment, we recommend that you use [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] to paste the encryption key into the **Data Encryption** dialog box.  
  
## <a name="encrypted-attributes"></a>Encrypted attributes  
 The entity attributes that are configured for field-level data encryption are listed in the following table.  
  
|Thực thể|Thuộc tính|  
|------------|---------------|  
|Cấu hình Máy chủ Email|IncomingPassword|  
|Cấu hình Máy chủ Email|OutgoingPassword|  
|Hộp thư|Mật khẩu|  
|Hàng đợi|EmailPassword|  
|UserSettings|EmailPassword|  
  
## <a name="messages"></a>Messages  
 The messages that can be used for field-level data encryption are listed in the following table.  
  
|Request class name|Thêm thông tin|  
|------------------------|----------------------|  
|<xref:Microsoft.Xrm.Sdk.Messages.IsDataEncryptionActiveRequest>|Checks if data encryption is currently running (active or inactive).|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveDataEncryptionKeyRequest>|Retrieves the data encryption key value.|  
|<xref:Microsoft.Xrm.Sdk.Messages.SetDataEncryptionKeyRequest>|Sets or restores the data encryption key. To prevent accidentally running multiple change requests in parallel, this SDK message will be throttled so that only one request can run at a time.|  
  
> [!NOTE]
>  You must use [!INCLUDE[pn_ssl_short](../includes/pn-ssl-short.md)] when you use these messages. When you execute these messages, a check will ensure that the user’s client/server connectivity is using the HTTPS protocol. If not, an exception is returned if the requests are submitted without using HTTPS.  
  
### <a name="see-also"></a>Xem thêm  
 [Administration Guide: Data encryption](https://technet.microsoft.com/library/dn531199\(v=crm.7\).aspx)
