---
title: Email activity entities (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: The email activity in Dynamics 365 for Customer Engagement lets you track and manage email communications with customers.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- bulk email, process sequence
- email activity entities, attaching files to email
- email activity entities, process sequence for bulk email
- attaching files to email
- tracking and managing customer email
- email attachments, maximum and default sizes
- email activity entities, introduction
- email activity entities, sending bulk email
- email activity entities, blocked email
- using email templates
- sending bulk email
- email routing, software for
- email activity entities, email templates
- email activity entities, tracking and managing customer email
- email activity entities, approved users and queues
- templates, email
- blocked email
- configuring email delivery
- email attachments, reusing (saved as BLOBs)
- email routing, supported protocols
- email activity entities
- email attachments, about
- email actions, creating, retrieving, updating, deleting
- email activity entities, configuring delivery
- email activity entities, routing email
ms.assetid: 4c27c9ae-c0e8-4de4-bba7-bf957a873ff5
caps.latest.revision: 42
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 821af1963a75ccb1b8f47bd0192c9670d6d6591f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388169"
---
# <a name="email-activity-entities"></a><span data-ttu-id="ea9c2-103">Email activity entities</span><span class="sxs-lookup"><span data-stu-id="ea9c2-103">Email activity entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ea9c2-104">The email activity lets you track and manage email communications with customers.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-104">The email activity lets you track and manage email communications with customers.</span></span> [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="ea9c2-105">includes the Email Router software that manages the routing of email to or from [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="ea9c2-105">includes the Email Router software that manages the routing of email to or from [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> <span data-ttu-id="ea9c2-106">The email activity is delivered using email protocols.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-106">The email activity is delivered using email protocols.</span></span> <span data-ttu-id="ea9c2-107">Email Router supports the following email protocols: Exchange Web services, POP3, and SMTP.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-107">Email Router supports the following email protocols: Exchange Web services, POP3, and SMTP.</span></span> <span data-ttu-id="ea9c2-108">In addition to the Email Router software, the email activity can also be delivered by using [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)].</span><span class="sxs-lookup"><span data-stu-id="ea9c2-108">In addition to the Email Router software, the email activity can also be delivered by using [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)].</span></span>  
  
<a name="Actions"></a>   
## <a name="actions-on-an-email-activity"></a><span data-ttu-id="ea9c2-109">Actions on an Email Activity</span><span class="sxs-lookup"><span data-stu-id="ea9c2-109">Actions on an Email Activity</span></span>  
 <span data-ttu-id="ea9c2-110">Using [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)], you can perform the following actions on an email activity:</span><span class="sxs-lookup"><span data-stu-id="ea9c2-110">Using [!INCLUDE[cc-dyn365-ce-web-services](../includes/cc-dyn365-ce-web-services.md)], you can perform the following actions on an email activity:</span></span>  
  
- <span data-ttu-id="ea9c2-111">Create, retrieve, update, and delete the email activity.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-111">Create, retrieve, update, and delete the email activity.</span></span>  
  
- <span data-ttu-id="ea9c2-112">Send email messages, or send email messages by using email templates (`Template`).</span><span class="sxs-lookup"><span data-stu-id="ea9c2-112">Send email messages, or send email messages by using email templates (`Template`).</span></span> <span data-ttu-id="ea9c2-113">For more information about email templates, see [Template Entity](entities/template.md).</span><span class="sxs-lookup"><span data-stu-id="ea9c2-113">For more information about email templates, see [Template Entity](entities/template.md).</span></span>  
  
- <span data-ttu-id="ea9c2-114">Attach files as attachments by using the (`ActivityMimeAttachment`) attribute in the email message.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-114">Attach files as attachments by using the (`ActivityMimeAttachment`) attribute in the email message.</span></span>  
  
- <span data-ttu-id="ea9c2-115">Send mass or bulk email messages.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-115">Send mass or bulk email messages.</span></span>  
  
- <span data-ttu-id="ea9c2-116">Configure incoming email messages to be delivered from [!INCLUDE[pn_Exchange_Server_full](../includes/pn-exchange-server-full.md)] to any user or queue, or outgoing messages to be sent from any user or queue to [!INCLUDE[pn_Exchange_Server_full](../includes/pn-exchange-server-full.md)].</span><span class="sxs-lookup"><span data-stu-id="ea9c2-116">Configure incoming email messages to be delivered from [!INCLUDE[pn_Exchange_Server_full](../includes/pn-exchange-server-full.md)] to any user or queue, or outgoing messages to be sent from any user or queue to [!INCLUDE[pn_Exchange_Server_full](../includes/pn-exchange-server-full.md)].</span></span> <span data-ttu-id="ea9c2-117">For information about how to configure incoming email messages for queues, see  [Configure email for incoming messages](configure-email-incoming-messages.md).</span><span class="sxs-lookup"><span data-stu-id="ea9c2-117">For information about how to configure incoming email messages for queues, see  [Configure email for incoming messages](configure-email-incoming-messages.md).</span></span>  
  
   <span data-ttu-id="ea9c2-118">If the `Organization.RequireApprovalForuserEmail` and `Organization.RequireApprovalForQueueEmail` (process emails only for approved users/queues) organization attributes are set to **true** (1),  the following occurs: email messages are delivered or sent from a user or queue only if the primary email address of the user or queue is approved.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-118">If the `Organization.RequireApprovalForuserEmail` and `Organization.RequireApprovalForQueueEmail` (process emails only for approved users/queues) organization attributes are set to **true** (1),  the following occurs: email messages are delivered or sent from a user or queue only if the primary email address of the user or queue is approved.</span></span> <span data-ttu-id="ea9c2-119">The `SystemUser.EmailRouterAccessApproval` and the `Queue.EmailRouterAccessApproval` attributes indicate the status of the primary email address of the user and queue respectively, and the value must be set to 1.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-119">The `SystemUser.EmailRouterAccessApproval` and the `Queue.EmailRouterAccessApproval` attributes indicate the status of the primary email address of the user and queue respectively, and the value must be set to 1.</span></span> <span data-ttu-id="ea9c2-120">Otherwise, the incoming and outgoing messages will be blocked.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-120">Otherwise, the incoming and outgoing messages will be blocked.</span></span> <span data-ttu-id="ea9c2-121">You can update the user or queue record to change the attribute value, if it is not already in the approved state, provided your user account has the **prvApproveRejectEmailAddress** privilege assigned.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-121">You can update the user or queue record to change the attribute value, if it is not already in the approved state, provided your user account has the **prvApproveRejectEmailAddress** privilege assigned.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="ea9c2-122">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], the `Email.StatusCode` attribute cannot be **null**.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-122">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], the `Email.StatusCode` attribute cannot be **null**.</span></span>  
  
<a name="BulkE-Mail"></a>   
## <a name="bulk-email"></a><span data-ttu-id="ea9c2-123">Bulk Email</span><span class="sxs-lookup"><span data-stu-id="ea9c2-123">Bulk Email</span></span>  
 [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="ea9c2-124">supports sending email to a large list of recipients through a bulk email request.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-124">supports sending email to a large list of recipients through a bulk email request.</span></span> <span data-ttu-id="ea9c2-125">When a bulk email request is sent to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], an asynchronous operation is created in the asynchronous service queue that sends the email messages by using a background process.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-125">When a bulk email request is sent to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)], an asynchronous operation is created in the asynchronous service queue that sends the email messages by using a background process.</span></span> <span data-ttu-id="ea9c2-126">This gives you improved system performance.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-126">This gives you improved system performance.</span></span>  
  
 <span data-ttu-id="ea9c2-127">The <xref:Microsoft.Crm.Sdk.Messages.SendBulkMailRequest> and <xref:Microsoft.Crm.Sdk.Messages.BackgroundSendEmailRequest> messages are used for sending bulk email messages.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-127">The <xref:Microsoft.Crm.Sdk.Messages.SendBulkMailRequest> and <xref:Microsoft.Crm.Sdk.Messages.BackgroundSendEmailRequest> messages are used for sending bulk email messages.</span></span> <span data-ttu-id="ea9c2-128">The following lists the sequence used to send bulk email:</span><span class="sxs-lookup"><span data-stu-id="ea9c2-128">The following lists the sequence used to send bulk email:</span></span>  
  
1. <span data-ttu-id="ea9c2-129">Execute the `SendBulkMail` request.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-129">Execute the `SendBulkMail` request.</span></span> <span data-ttu-id="ea9c2-130">This request contains a query that selects the target email recipients and an email template for composing each email.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-130">This request contains a query that selects the target email recipients and an email template for composing each email.</span></span>  
  
2. <span data-ttu-id="ea9c2-131">The asynchronous service creates the email activities for each recipient.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-131">The asynchronous service creates the email activities for each recipient.</span></span>  
  
3. <span data-ttu-id="ea9c2-132">The asynchronous service sends each email message.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-132">The asynchronous service sends each email message.</span></span> <span data-ttu-id="ea9c2-133">The email messages have a "pending" send status.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-133">The email messages have a "pending" send status.</span></span>  
  
4. <span data-ttu-id="ea9c2-134">The email router, [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)], or a third-party email send component polls [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] for pending email messages, and if one is found, downloads it by using the `BackgroundSendEmail` request.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-134">The email router, [!INCLUDE[pn_crm_for_outlook_full](../includes/pn-crm-for-outlook-full.md)], or a third-party email send component polls [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] for pending email messages, and if one is found, downloads it by using the `BackgroundSendEmail` request.</span></span>  
  
5. <span data-ttu-id="ea9c2-135">The `BackgroundSendEmail` request performs the following operations: checks if pending email messages are present, downloads the email to the caller of the <xref:Microsoft.Crm.Sdk.Messages.BackgroundSendEmailRequest> message, and synchronizes the downloads if there are multiple callers.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-135">The `BackgroundSendEmail` request performs the following operations: checks if pending email messages are present, downloads the email to the caller of the <xref:Microsoft.Crm.Sdk.Messages.BackgroundSendEmailRequest> message, and synchronizes the downloads if there are multiple callers.</span></span>  
  
6. <span data-ttu-id="ea9c2-136">The caller of the <xref:Microsoft.Crm.Sdk.Messages.BackgroundSendEmailRequest> message receives the downloaded email message, and sends it out.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-136">The caller of the <xref:Microsoft.Crm.Sdk.Messages.BackgroundSendEmailRequest> message receives the downloaded email message, and sends it out.</span></span>  
  
<a name="E-MailAttachments"></a>   
## <a name="email-attachments"></a><span data-ttu-id="ea9c2-137">Email Attachments</span><span class="sxs-lookup"><span data-stu-id="ea9c2-137">Email Attachments</span></span>  
 <span data-ttu-id="ea9c2-138">Email attachments are files that can be attached to email messages or email templates.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-138">Email attachments are files that can be attached to email messages or email templates.</span></span> <span data-ttu-id="ea9c2-139">An attached file can be in any standard computer file format such as [!INCLUDE[pn_MS_Word_Full](../includes/pn-ms-word-full.md)] documents, [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)] spreadsheets, CAD files, and PDF files.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-139">An attached file can be in any standard computer file format such as [!INCLUDE[pn_MS_Word_Full](../includes/pn-ms-word-full.md)] documents, [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)] spreadsheets, CAD files, and PDF files.</span></span> <span data-ttu-id="ea9c2-140">You can attach multiple files as email attachments to an email or email template.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-140">You can attach multiple files as email attachments to an email or email template.</span></span> [!INCLUDE[sdk_MaxUploadFileSize](../includes/sdk-maxuploadfilesize.md)]  
  
 <span data-ttu-id="ea9c2-141">To attach an email attachment with an email message or template, you use the `ActivityMimeAttachment.ObjectId` and `ActivityMimeAttachment.ObjectTypeCode` attributes while you are creating or updating an activity mime attachment record.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-141">To attach an email attachment with an email message or template, you use the `ActivityMimeAttachment.ObjectId` and `ActivityMimeAttachment.ObjectTypeCode` attributes while you are creating or updating an activity mime attachment record.</span></span>  
  
 <span data-ttu-id="ea9c2-142">The following code sample shows how to attach an email attachment to an email:</span><span class="sxs-lookup"><span data-stu-id="ea9c2-142">The following code sample shows how to attach an email attachment to an email:</span></span>  
  
```csharp  
ActivityMimeAttachment _sampleAttachment = new ActivityMimeAttachment{  
    ObjectId = new EntityReference(Email.EntityLogicalName, _emailId),  
    ObjectTypeCode = Email.EntityLogicalName,  
    Subject = "Sample Attachment”,  
    Body = System.Convert.ToBase64String(new ASCIIEncoding().GetBytes("Example Attachment")),  
    FileName = "ExampleAttachment.txt"};  
```  
  
 <span data-ttu-id="ea9c2-143">Similarly, to attach the email attachment to a template instead of an email, you will replace the values of the `ActivityMimeAttachment.ObjectId` and `ActivityMimeAttachment.ObjectTypeCode` attributes as follows in the above code:</span><span class="sxs-lookup"><span data-stu-id="ea9c2-143">Similarly, to attach the email attachment to a template instead of an email, you will replace the values of the `ActivityMimeAttachment.ObjectId` and `ActivityMimeAttachment.ObjectTypeCode` attributes as follows in the above code:</span></span>  
  
```csharp  
ObjectId = new EntityReference(Template.EntityLogicalName, _templateId), ObjectTypeCode = Template.EntityLogicalName,  
```  
  
 <span data-ttu-id="ea9c2-144">For complete code sample about how to create email attachments, see [Sample: Create, Retrieve, Update, and Delete an E-Mail Attachment](sample-create-retrieve-update-delete-email-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="ea9c2-144">For complete code sample about how to create email attachments, see [Sample: Create, Retrieve, Update, and Delete an E-Mail Attachment](sample-create-retrieve-update-delete-email-attachment.md).</span></span>  
  
### <a name="reusing-email-attachments"></a><span data-ttu-id="ea9c2-145">Reusing Email Attachments</span><span class="sxs-lookup"><span data-stu-id="ea9c2-145">Reusing Email Attachments</span></span>  
 <span data-ttu-id="ea9c2-146">When you create an email attachment record, the attached file is saved as a file BLOB.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-146">When you create an email attachment record, the attached file is saved as a file BLOB.</span></span> <span data-ttu-id="ea9c2-147">The `ActivityMimeAttachment.AttachmentId` attribute of the email attachment record uniquely identifies the file BLOB.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-147">The `ActivityMimeAttachment.AttachmentId` attribute of the email attachment record uniquely identifies the file BLOB.</span></span> <span data-ttu-id="ea9c2-148">This is done to facilitate the reuse of the file attachments with other email and email template records, without creating and storing multiple copies of the same file in the database.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-148">This is done to facilitate the reuse of the file attachments with other email and email template records, without creating and storing multiple copies of the same file in the database.</span></span>  
  
 <span data-ttu-id="ea9c2-149">To reuse an existing file attachment:</span><span class="sxs-lookup"><span data-stu-id="ea9c2-149">To reuse an existing file attachment:</span></span>  
  
1.  <span data-ttu-id="ea9c2-150">Retrieve the `ActivityMimeAttachment` record that contains the attachment file that you want to re-use, as shown in the following code example:</span><span class="sxs-lookup"><span data-stu-id="ea9c2-150">Retrieve the `ActivityMimeAttachment` record that contains the attachment file that you want to re-use, as shown in the following code example:</span></span>  
  
    ```csharp  
    ActivityMimeAttachment retrievedAttachment = (ActivityMimeAttachment)_serviceProxy.Retrieve(ActivityMimeAttachment.EntityLogicalName, _emailAttachmentId, new ColumnSet(true));  
    ```  
  
2.  <span data-ttu-id="ea9c2-151">Create a new email attachment record, associate it with the required email or email template record, and point it to the attached file of the retrieved `ActivityMimeAttachment` record, as shown in the following code example:</span><span class="sxs-lookup"><span data-stu-id="ea9c2-151">Create a new email attachment record, associate it with the required email or email template record, and point it to the attached file of the retrieved `ActivityMimeAttachment` record, as shown in the following code example:</span></span>  
  
    ```csharp  
    ActivityMimeAttachment _reuseAttachment = new ActivityMimeAttachment{  
        ObjectId = new EntityReference(Email.EntityLogicalName, _emailId),  
        ObjectTypeCode = Email.EntityLogicalName,  
        Subject = "Sample Attachment”,  
        AttachmentId = retrievedAttachment.AttachmentId};  
    ```  
  
     <span data-ttu-id="ea9c2-152">Because you are reusing an existing attachment file, you do not have to specify the `ActivityMimeAttachment.Body` and `ActivityMimeAttachment.FileName` attribute values while you are creating and associating email attachment records to emails or email templates.</span><span class="sxs-lookup"><span data-stu-id="ea9c2-152">Because you are reusing an existing attachment file, you do not have to specify the `ActivityMimeAttachment.Body` and `ActivityMimeAttachment.FileName` attribute values while you are creating and associating email attachment records to emails or email templates.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ea9c2-153">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ea9c2-153">See also</span></span>  
 <span data-ttu-id="ea9c2-154">[Activity Entities](activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="ea9c2-154">[Activity Entities](activity-entities.md) </span></span>  
 <span data-ttu-id="ea9c2-155">[Sample code for activity entities](sample-code-activity-entities.md) </span><span class="sxs-lookup"><span data-stu-id="ea9c2-155">[Sample code for activity entities](sample-code-activity-entities.md) </span></span>  
 <span data-ttu-id="ea9c2-156">[Email Entity](entities/email.md) </span><span class="sxs-lookup"><span data-stu-id="ea9c2-156">[Email Entity](entities/email.md) </span></span>  
 [<span data-ttu-id="ea9c2-157">ActivityMimeAttachment Entity</span><span class="sxs-lookup"><span data-stu-id="ea9c2-157">ActivityMimeAttachment Entity</span></span>](entities/activitymimeattachment.md)
