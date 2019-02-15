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
# <a name="field-level-data-encryption"></a><span data-ttu-id="7dc0c-104">Field-level data encryption</span><span class="sxs-lookup"><span data-stu-id="7dc0c-104">Field-level data encryption</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="7dc0c-105">sử dụng mã hóa mức ô [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] tiêu chuẩn cho tập hợp các thuộc tính thực thể mặc định chứa các thông tin nhạy cảm chẳng hạn như tên người dùng và mật khẩu email.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-105">uses standard [!INCLUDE[pn_MS_SQL_Server](../includes/pn-ms-sql-server.md)] cell level encryption for a set of default entity attributes that contain sensitive information, such as user names and email passwords.</span></span> <span data-ttu-id="7dc0c-106">This feature can help organizations meet the compliance requirements associated with FIPS 140-2.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-106">This feature can help organizations meet the compliance requirements associated with FIPS 140-2.</span></span> <span data-ttu-id="7dc0c-107">Field-level data encryption is especially important in scenarios that leverage the [!INCLUDE[pn_CRM_E-Mail_Router](../includes/pn-crm-e-mail-router.md)], which must store user names and passwords to enable integration between a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance and an email service such as [!INCLUDE[pn_Microsoft_Exchange](../includes/pn-microsoft-exchange.md)].</span><span class="sxs-lookup"><span data-stu-id="7dc0c-107">Field-level data encryption is especially important in scenarios that leverage the [!INCLUDE[pn_CRM_E-Mail_Router](../includes/pn-crm-e-mail-router.md)], which must store user names and passwords to enable integration between a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance and an email service such as [!INCLUDE[pn_Microsoft_Exchange](../includes/pn-microsoft-exchange.md)].</span></span>  
  
 [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="7dc0c-108">users who have the system administrator security role can activate data encryption (or change the encryption key after data encryption is enabled) in the **Settings** > **Data Management** > **Data Encryption** area.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-108">users who have the system administrator security role can activate data encryption (or change the encryption key after data encryption is enabled) in the **Settings** > **Data Management** > **Data Encryption** area.</span></span> <span data-ttu-id="7dc0c-109">After data encryption is activated, it cannot be turned off.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-109">After data encryption is activated, it cannot be turned off.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="7dc0c-110">For both [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], all new and upgraded organizations have data encryption activated.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-110">For both [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], all new and upgraded organizations have data encryption activated.</span></span>  
> 
>  <span data-ttu-id="7dc0c-111">When considering the use of data encryption, be sure to keep in mind the following key points:</span><span class="sxs-lookup"><span data-stu-id="7dc0c-111">When considering the use of data encryption, be sure to keep in mind the following key points:</span></span>  
> 
> - <span data-ttu-id="7dc0c-112">To help ensure the highest level of security, we recommend that you change the encryption key immediately after creating or updating an organization, and thereafter about once a year.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-112">To help ensure the highest level of security, we recommend that you change the encryption key immediately after creating or updating an organization, and thereafter about once a year.</span></span>  
>   - <span data-ttu-id="7dc0c-113">Changing the encryption key requires that [!INCLUDE[pn_ssl_short](../includes/pn-ssl-short.md)] be configured on the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] website.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-113">Changing the encryption key requires that [!INCLUDE[pn_ssl_short](../includes/pn-ssl-short.md)] be configured on the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] website.</span></span>  
>   - <span data-ttu-id="7dc0c-114">Auditing cannot be enabled on encrypted fields.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-114">Auditing cannot be enabled on encrypted fields.</span></span>  
>   - <span data-ttu-id="7dc0c-115">Encrypted fields cannot be customized.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-115">Encrypted fields cannot be customized.</span></span>  
>   - <span data-ttu-id="7dc0c-116">Encrypted fields cannot be indexed.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-116">Encrypted fields cannot be indexed.</span></span>  
>   - <span data-ttu-id="7dc0c-117">Encrypted fields can be set and updated by using standard Create, Update, and Delete methods.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-117">Encrypted fields can be set and updated by using standard Create, Update, and Delete methods.</span></span>  
>   - <span data-ttu-id="7dc0c-118">When doing a retrieve of an encrypted field’s value, a **null** is returned.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-118">When doing a retrieve of an encrypted field’s value, a **null** is returned.</span></span>  
  
 <span data-ttu-id="7dc0c-119">The encryption key is required to activate data encryption when you import an organization database into a new deployment or into a deployment that has had the configuration database (MSCRM_CONFIG) recreated after the organization was encrypted.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-119">The encryption key is required to activate data encryption when you import an organization database into a new deployment or into a deployment that has had the configuration database (MSCRM_CONFIG) recreated after the organization was encrypted.</span></span> <span data-ttu-id="7dc0c-120">You can copy the original encryption key to Notepad and then paste it into the **Settings** > **Data Management** > **Data Encryption** dialog box after the organization import is completed.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-120">You can copy the original encryption key to Notepad and then paste it into the **Settings** > **Data Management** > **Data Encryption** dialog box after the organization import is completed.</span></span> <span data-ttu-id="7dc0c-121">When activating data encryption after redeployment, we recommend that you use [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] to paste the encryption key into the **Data Encryption** dialog box.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-121">When activating data encryption after redeployment, we recommend that you use [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] to paste the encryption key into the **Data Encryption** dialog box.</span></span>  
  
## <a name="encrypted-attributes"></a><span data-ttu-id="7dc0c-122">Encrypted attributes</span><span class="sxs-lookup"><span data-stu-id="7dc0c-122">Encrypted attributes</span></span>  
 <span data-ttu-id="7dc0c-123">The entity attributes that are configured for field-level data encryption are listed in the following table.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-123">The entity attributes that are configured for field-level data encryption are listed in the following table.</span></span>  
  
|<span data-ttu-id="7dc0c-124">Thực thể</span><span class="sxs-lookup"><span data-stu-id="7dc0c-124">Entity</span></span>|<span data-ttu-id="7dc0c-125">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="7dc0c-125">Attribute</span></span>|  
|------------|---------------|  
|<span data-ttu-id="7dc0c-126">Cấu hình Máy chủ Email</span><span class="sxs-lookup"><span data-stu-id="7dc0c-126">EmailServerProfile</span></span>|<span data-ttu-id="7dc0c-127">IncomingPassword</span><span class="sxs-lookup"><span data-stu-id="7dc0c-127">IncomingPassword</span></span>|  
|<span data-ttu-id="7dc0c-128">Cấu hình Máy chủ Email</span><span class="sxs-lookup"><span data-stu-id="7dc0c-128">EmailServerProfile</span></span>|<span data-ttu-id="7dc0c-129">OutgoingPassword</span><span class="sxs-lookup"><span data-stu-id="7dc0c-129">OutgoingPassword</span></span>|  
|<span data-ttu-id="7dc0c-130">Hộp thư</span><span class="sxs-lookup"><span data-stu-id="7dc0c-130">Mailbox</span></span>|<span data-ttu-id="7dc0c-131">Mật khẩu</span><span class="sxs-lookup"><span data-stu-id="7dc0c-131">Password</span></span>|  
|<span data-ttu-id="7dc0c-132">Hàng đợi</span><span class="sxs-lookup"><span data-stu-id="7dc0c-132">Queue</span></span>|<span data-ttu-id="7dc0c-133">EmailPassword</span><span class="sxs-lookup"><span data-stu-id="7dc0c-133">EmailPassword</span></span>|  
|<span data-ttu-id="7dc0c-134">UserSettings</span><span class="sxs-lookup"><span data-stu-id="7dc0c-134">UserSettings</span></span>|<span data-ttu-id="7dc0c-135">EmailPassword</span><span class="sxs-lookup"><span data-stu-id="7dc0c-135">EmailPassword</span></span>|  
  
## <a name="messages"></a><span data-ttu-id="7dc0c-136">Messages</span><span class="sxs-lookup"><span data-stu-id="7dc0c-136">Messages</span></span>  
 <span data-ttu-id="7dc0c-137">The messages that can be used for field-level data encryption are listed in the following table.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-137">The messages that can be used for field-level data encryption are listed in the following table.</span></span>  
  
|<span data-ttu-id="7dc0c-138">Request class name</span><span class="sxs-lookup"><span data-stu-id="7dc0c-138">Request class name</span></span>|<span data-ttu-id="7dc0c-139">Thêm thông tin</span><span class="sxs-lookup"><span data-stu-id="7dc0c-139">More information</span></span>|  
|------------------------|----------------------|  
|<xref:Microsoft.Xrm.Sdk.Messages.IsDataEncryptionActiveRequest>|<span data-ttu-id="7dc0c-140">Checks if data encryption is currently running (active or inactive).</span><span class="sxs-lookup"><span data-stu-id="7dc0c-140">Checks if data encryption is currently running (active or inactive).</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveDataEncryptionKeyRequest>|<span data-ttu-id="7dc0c-141">Retrieves the data encryption key value.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-141">Retrieves the data encryption key value.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Messages.SetDataEncryptionKeyRequest>|<span data-ttu-id="7dc0c-142">Sets or restores the data encryption key.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-142">Sets or restores the data encryption key.</span></span> <span data-ttu-id="7dc0c-143">To prevent accidentally running multiple change requests in parallel, this SDK message will be throttled so that only one request can run at a time.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-143">To prevent accidentally running multiple change requests in parallel, this SDK message will be throttled so that only one request can run at a time.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="7dc0c-144">You must use [!INCLUDE[pn_ssl_short](../includes/pn-ssl-short.md)] when you use these messages.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-144">You must use [!INCLUDE[pn_ssl_short](../includes/pn-ssl-short.md)] when you use these messages.</span></span> <span data-ttu-id="7dc0c-145">When you execute these messages, a check will ensure that the user’s client/server connectivity is using the HTTPS protocol.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-145">When you execute these messages, a check will ensure that the user’s client/server connectivity is using the HTTPS protocol.</span></span> <span data-ttu-id="7dc0c-146">If not, an exception is returned if the requests are submitted without using HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7dc0c-146">If not, an exception is returned if the requests are submitted without using HTTPS.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7dc0c-147">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7dc0c-147">See also</span></span>  
 <span data-ttu-id="7dc0c-148">[Administration Guide: Data encryption](https://technet.microsoft.com/library/dn531199\(v=crm.7\).aspx)</span><span class="sxs-lookup"><span data-stu-id="7dc0c-148">[Administration Guide: Data encryption](https://technet.microsoft.com/library/dn531199\(v=crm.7\).aspx)</span></span>
