---
title: Server-side synchronization entities (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: In Dynamics 365 for Customer Engagement (online), server-side synchronization provides an interface between Dynamics 365 for Customer Engagement and one or more Exchange servers or POP3 servers for incoming email, and one or more SMTP or Exchange servers for outgoing email
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8595e377-7496-456d-ba2f-8671d066098a
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 93bf1a27346dc07e4af231537c1f1d46359e2539
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385584"
---
# <a name="server-side-synchronization-entities"></a><span data-ttu-id="61993-103">Server-side synchronization entities</span><span class="sxs-lookup"><span data-stu-id="61993-103">Server-side synchronization entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="61993-104">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], server-side synchronization provides an interface between [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] and one or more [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] servers or POP3 servers for incoming email, and one or more [!INCLUDE[pn_SMTP](../includes/pn-smtp.md)] or [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] servers for outgoing email.</span><span class="sxs-lookup"><span data-stu-id="61993-104">In [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)], server-side synchronization provides an interface between [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] and one or more [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] servers or POP3 servers for incoming email, and one or more [!INCLUDE[pn_SMTP](../includes/pn-smtp.md)] or [!INCLUDE[pn_Exchange](../includes/pn-exchange.md)] servers for outgoing email.</span></span> <span data-ttu-id="61993-105">It retrieves and evaluates emails for relevance to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] and accordingly creates corresponding email activities in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="61993-105">It retrieves and evaluates emails for relevance to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] and accordingly creates corresponding email activities in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="61993-106">It also picks emails from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] and sends them through the configured email server for [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] users and queues.</span><span class="sxs-lookup"><span data-stu-id="61993-106">It also picks emails from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] and sends them through the configured email server for [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] users and queues.</span></span> <span data-ttu-id="61993-107">It also allows synchronization of appointments, contacts, and tasks with [!INCLUDE[pn_ms_Exchange_Server_2010_short](../includes/pn-ms-exchange-server-2010-short.md)] and [!INCLUDE[pn_Exchange_Server_2013_short](../includes/pn-exchange-server-2013-short.md)].</span><span class="sxs-lookup"><span data-stu-id="61993-107">It also allows synchronization of appointments, contacts, and tasks with [!INCLUDE[pn_ms_Exchange_Server_2010_short](../includes/pn-ms-exchange-server-2010-short.md)] and [!INCLUDE[pn_Exchange_Server_2013_short](../includes/pn-exchange-server-2013-short.md)].</span></span>  
  
 <span data-ttu-id="61993-108">With the centralized email configuration, the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] entity model allows having common user interface (UI) settings (like user name, password, email address, and synchronization methods) for users, queues, and forward mailboxes.</span><span class="sxs-lookup"><span data-stu-id="61993-108">With the centralized email configuration, the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] entity model allows having common user interface (UI) settings (like user name, password, email address, and synchronization methods) for users, queues, and forward mailboxes.</span></span> <span data-ttu-id="61993-109">Each [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] user or a queue can have mailboxes, which can be monitored through either server-side synchronization or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)].</span><span class="sxs-lookup"><span data-stu-id="61993-109">Each [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] user or a queue can have mailboxes, which can be monitored through either server-side synchronization or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../includes/pn-microsoft-dynamics-crm-for-outlook.md)].</span></span> <span data-ttu-id="61993-110">The `EmailServerProfile` entity represents the email server profile for an organization.</span><span class="sxs-lookup"><span data-stu-id="61993-110">The `EmailServerProfile` entity represents the email server profile for an organization.</span></span> <span data-ttu-id="61993-111">The `Mailbox` entity represents the appointments, contacts, and tasks delivery method of the mailbox.</span><span class="sxs-lookup"><span data-stu-id="61993-111">The `Mailbox` entity represents the appointments, contacts, and tasks delivery method of the mailbox.</span></span> <span data-ttu-id="61993-112">Currently, the user entity is restricted to have only one mailbox record per user and the queues entity to have only one mailbox record per queue, as shown in the following illustration.</span><span class="sxs-lookup"><span data-stu-id="61993-112">Currently, the user entity is restricted to have only one mailbox record per user and the queues entity to have only one mailbox record per queue, as shown in the following illustration.</span></span>  
  
 <span data-ttu-id="61993-113">![Email connector entity model](media/email-connector-entity-model.png "Email connector entity model")</span><span class="sxs-lookup"><span data-stu-id="61993-113">![Email connector entity model](media/email-connector-entity-model.png "Email connector entity model")</span></span>  
  
 <span data-ttu-id="61993-114">Server-side synchronization offers the following capabilities:</span><span class="sxs-lookup"><span data-stu-id="61993-114">Server-side synchronization offers the following capabilities:</span></span>  
  
- <span data-ttu-id="61993-115">Process emails of a user and a queue using the email address, email delivery method, and credentials from the related mailbox record.</span><span class="sxs-lookup"><span data-stu-id="61993-115">Process emails of a user and a queue using the email address, email delivery method, and credentials from the related mailbox record.</span></span>  
  
- <span data-ttu-id="61993-116">Process appointments, contacts, and tasks.</span><span class="sxs-lookup"><span data-stu-id="61993-116">Process appointments, contacts, and tasks.</span></span>  
  
- <span data-ttu-id="61993-117">Use mailbox records to process emails for users and queues having the incoming delivery method set as Forward Mailbox.</span><span class="sxs-lookup"><span data-stu-id="61993-117">Use mailbox records to process emails for users and queues having the incoming delivery method set as Forward Mailbox.</span></span>  
  
- <span data-ttu-id="61993-118">Use information from a related email profile record to process emails for all mailboxes.</span><span class="sxs-lookup"><span data-stu-id="61993-118">Use information from a related email profile record to process emails for all mailboxes.</span></span>  
  
- <span data-ttu-id="61993-119">Prevent email processing for inactive mailboxes or for mailboxes that don’t have an associated email profile.</span><span class="sxs-lookup"><span data-stu-id="61993-119">Prevent email processing for inactive mailboxes or for mailboxes that don’t have an associated email profile.</span></span>  
  
- <span data-ttu-id="61993-120">Automatically relate an associated mailbox to the default email profile when a user or a queue is created with the email delivery method set as server-side synchronization.</span><span class="sxs-lookup"><span data-stu-id="61993-120">Automatically relate an associated mailbox to the default email profile when a user or a queue is created with the email delivery method set as server-side synchronization.</span></span>  
  
- <span data-ttu-id="61993-121">Automatically track [!INCLUDE[pn_Microsoft_Exchange](../includes/pn-microsoft-exchange.md)] emails in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] for a user based on the folder-level tracking rules.</span><span class="sxs-lookup"><span data-stu-id="61993-121">Automatically track [!INCLUDE[pn_Microsoft_Exchange](../includes/pn-microsoft-exchange.md)] emails in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] for a user based on the folder-level tracking rules.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="61993-122">In This Section</span><span class="sxs-lookup"><span data-stu-id="61993-122">In This Section</span></span>  
 [<span data-ttu-id="61993-123">Configure folder level tracking rules</span><span class="sxs-lookup"><span data-stu-id="61993-123">Configure folder level tracking rules</span></span>](configure-exchange-folder-level-tracking-rules.md)  
  
 [<span data-ttu-id="61993-124">EmailServerProfile Entity</span><span class="sxs-lookup"><span data-stu-id="61993-124">EmailServerProfile Entity</span></span>](entities/emailserverprofile.md)  
  
 [<span data-ttu-id="61993-125">ExchangeSyncIdMapping Entity</span><span class="sxs-lookup"><span data-stu-id="61993-125">ExchangeSyncIdMapping Entity</span></span>](entities/exchangesyncidmapping.md)  
  
 [<span data-ttu-id="61993-126">Mailbox Entity</span><span class="sxs-lookup"><span data-stu-id="61993-126">Mailbox Entity</span></span>](entities/mailbox.md)  
  
 [<span data-ttu-id="61993-127">MailboxTrackingFolder Entity</span><span class="sxs-lookup"><span data-stu-id="61993-127">MailboxTrackingFolder Entity</span></span>](entities/mailboxtrackingfolder.md) 
  
## <a name="related-sections"></a><span data-ttu-id="61993-128">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="61993-128">Related Sections</span></span>

 [<span data-ttu-id="61993-129">Model Your Business Data With Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="61993-129">Model Your Business Data With Dynamics 365 for Customer Engagement apps</span></span>](model-business-data.md)  
  
 [<span data-ttu-id="61993-130">Goal Management Entities</span><span class="sxs-lookup"><span data-stu-id="61993-130">Goal Management Entities</span></span>](goal-management-entities.md)  
  
 [<span data-ttu-id="61993-131">Product Catalog Entities</span><span class="sxs-lookup"><span data-stu-id="61993-131">Product Catalog Entities</span></span>](product-catalog-entities.md)  
  
 [<span data-ttu-id="61993-132">Sales Literature Entities</span><span class="sxs-lookup"><span data-stu-id="61993-132">Sales Literature Entities</span></span>](sales-literature-entities.md)  
  
 [<span data-ttu-id="61993-133">Schedule and Appointment Entities</span><span class="sxs-lookup"><span data-stu-id="61993-133">Schedule and Appointment Entities</span></span>](schedule-appointment-entities.md)
