---
title: Configure email for incoming messages (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about configuring email for the incoming messages to deliver directly to a queue.
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
- email, configuring to deliver to a queue
- configuring email
- email, configuring address; delivery methods; router; and filtering
- email, approval of (ensuring unblocked)
ms.assetid: 24e17276-ee23-4414-a025-030b841ae166
caps.latest.revision: 51
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b3cd29ed5dace366a0147862ce692215126e8e78
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387161"
---
# <a name="configure-email-for-incoming-messages"></a><span data-ttu-id="3d7f7-103">Configure email for incoming messages</span><span class="sxs-lookup"><span data-stu-id="3d7f7-103">Configure email for incoming messages</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3d7f7-104">If you want incoming email messages to be delivered directly to a queue, specify the following information in the queue:</span><span class="sxs-lookup"><span data-stu-id="3d7f7-104">If you want incoming email messages to be delivered directly to a queue, specify the following information in the queue:</span></span>  
  
- <span data-ttu-id="3d7f7-105">An email address by using the `Queue.EmailAddress` attribute.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-105">An email address by using the `Queue.EmailAddress` attribute.</span></span> <span data-ttu-id="3d7f7-106">It must be a valid email address where emails that are sent to the queue are directed.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-106">It must be a valid email address where emails that are sent to the queue are directed.</span></span>  
  
- <span data-ttu-id="3d7f7-107">An incoming email delivery method by using the `Queue.IncomingEmailDeliveryMethod` attribute.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-107">An incoming email delivery method by using the `Queue.IncomingEmailDeliveryMethod` attribute.</span></span> <span data-ttu-id="3d7f7-108">You can specify email to be sent and received with the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)]Email Router or forwarded from another email address.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-108">You can specify email to be sent and received with the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)]Email Router or forwarded from another email address.</span></span> <span data-ttu-id="3d7f7-109">If you specify the email router, you have an option to include the user’s email server credentials to give the user access to the server for retrieving emails.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-109">If you specify the email router, you have an option to include the user’s email server credentials to give the user access to the server for retrieving emails.</span></span>  
  
- <span data-ttu-id="3d7f7-110">An outgoing email delivery method, such as email router, by using the `Queue.OutgoingEmailDeliveryMethod` attribute.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-110">An outgoing email delivery method, such as email router, by using the `Queue.OutgoingEmailDeliveryMethod` attribute.</span></span>  
  
- <span data-ttu-id="3d7f7-111">An incoming email filtering method by using the `Queue.IncomingEmailFilteringMethod` attribute.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-111">An incoming email filtering method by using the `Queue.IncomingEmailFilteringMethod` attribute.</span></span> <span data-ttu-id="3d7f7-112">You can specify to convert all incoming email messages to email activities or only email messages that relate to existing [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] records.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-112">You can specify to convert all incoming email messages to email activities or only email messages that relate to existing [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] records.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="3d7f7-113">The primary email address of the queue must be approved to ensure that the incoming and outgoing email messages are not blocked.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-113">The primary email address of the queue must be approved to ensure that the incoming and outgoing email messages are not blocked.</span></span> <span data-ttu-id="3d7f7-114">The `Queue.EmailRouterAccessApproval` attribute contains the status of the primary email address of the queue.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-114">The `Queue.EmailRouterAccessApproval` attribute contains the status of the primary email address of the queue.</span></span> <span data-ttu-id="3d7f7-115">The status must be set to 1 (Approved).</span><span class="sxs-lookup"><span data-stu-id="3d7f7-115">The status must be set to 1 (Approved).</span></span> <span data-ttu-id="3d7f7-116">You can update the queue record to change the attribute value to 1 (Approved), if it is not already in the approved state.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-116">You can update the queue record to change the attribute value to 1 (Approved), if it is not already in the approved state.</span></span> <span data-ttu-id="3d7f7-117">To update the attribute value, you must have the **prvApproveRejectEmailAddress** privilege.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-117">To update the attribute value, you must have the **prvApproveRejectEmailAddress** privilege.</span></span> <span data-ttu-id="3d7f7-118">You also must set the `Organization.RequireApprovalForQueueEmail` attribute to 1 (True).</span><span class="sxs-lookup"><span data-stu-id="3d7f7-118">You also must set the `Organization.RequireApprovalForQueueEmail` attribute to 1 (True).</span></span> <span data-ttu-id="3d7f7-119">If not set to 1 (True), the value provided in the `Queue.EmailRouterAccessApproval` attribute is ignored.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-119">If not set to 1 (True), the value provided in the `Queue.EmailRouterAccessApproval` attribute is ignored.</span></span>  
> 
>  <span data-ttu-id="3d7f7-120">It’s no longer possible to configure Email Router credentials by setting the `Queue.AllowEmailCredentials` attribute to `true` followed by specifying the user name and password in `Queue.EmailUserName` and `Queue.EmailPassword`.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-120">It’s no longer possible to configure Email Router credentials by setting the `Queue.AllowEmailCredentials` attribute to `true` followed by specifying the user name and password in `Queue.EmailUserName` and `Queue.EmailPassword`.</span></span> <span data-ttu-id="3d7f7-121">These attributes have been deprecated and made read-only.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-121">These attributes have been deprecated and made read-only.</span></span> <span data-ttu-id="3d7f7-122">The same restriction applies to the `UserSettings.EmailPassword` and `UserSettings.EmailUserName` attributes.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-122">The same restriction applies to the `UserSettings.EmailPassword` and `UserSettings.EmailUserName` attributes.</span></span> <span data-ttu-id="3d7f7-123">However, these attributes can be set in the Email Router configuration.</span><span class="sxs-lookup"><span data-stu-id="3d7f7-123">However, these attributes can be set in the Email Router configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="3d7f7-124">[Configure the Email Router](https://technet.microsoft.com/library/hh699786.aspx).</span><span class="sxs-lookup"><span data-stu-id="3d7f7-124">[Configure the Email Router](https://technet.microsoft.com/library/hh699786.aspx).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3d7f7-125">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3d7f7-125">See also</span></span>  
 <span data-ttu-id="3d7f7-126">[Queue Entities](queue-entities.md) </span><span class="sxs-lookup"><span data-stu-id="3d7f7-126">[Queue Entities](queue-entities.md) </span></span>  
 [<span data-ttu-id="3d7f7-127">Queue Entity</span><span class="sxs-lookup"><span data-stu-id="3d7f7-127">Queue Entity</span></span>](entities/queue.md)
