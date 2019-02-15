---
title: Offline use of the Dynamics 365 for Customer Engagement services (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn about how various Dynamics 365 for Customer Engagement services can be used offline. There are several messages that are supported offline. You can also determine whether a IOrganizationService message works offline by checking the SdkMessage.Availability attribute for the desired message
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 7bd0c158-6def-410f-987e-7a376f7a7fae
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 38a9d537c1f2dec08abe077ae43f9fb927cc619c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388812"
---
# <a name="offline-use-of-the-dynamics-365-for-customer-engagement-services"></a><span data-ttu-id="b8006-105">Offline use of the Dynamics 365 for Customer Engagement services</span><span class="sxs-lookup"><span data-stu-id="b8006-105">Offline use of the Dynamics 365 for Customer Engagement services</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_crm_outlook_offline_access](../../includes/pn-crm-outlook-offline-access.md)] <span data-ttu-id="b8006-106">enables you to continue your work when you are disconnected from the server.</span><span class="sxs-lookup"><span data-stu-id="b8006-106">enables you to continue your work when you are disconnected from the server.</span></span>  
  
 <span data-ttu-id="b8006-107">In addition, the event and plug-in infrastructure lets you leverage development investments across solutions by using the same APIs and programming model.</span><span class="sxs-lookup"><span data-stu-id="b8006-107">In addition, the event and plug-in infrastructure lets you leverage development investments across solutions by using the same APIs and programming model.</span></span> <span data-ttu-id="b8006-108">The <xref:Microsoft.Xrm.Sdk.IOrganizationService> methods and the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps OData service methods function both online and offline.</span><span class="sxs-lookup"><span data-stu-id="b8006-108">The <xref:Microsoft.Xrm.Sdk.IOrganizationService> methods and the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps OData service methods function both online and offline.</span></span> <span data-ttu-id="b8006-109">When using a method such as `Create` or `Update` offline, the data is written locally and then when the user connects to the server, the actions are played back to the server.</span><span class="sxs-lookup"><span data-stu-id="b8006-109">When using a method such as `Create` or `Update` offline, the data is written locally and then when the user connects to the server, the actions are played back to the server.</span></span>  
  
 <span data-ttu-id="b8006-110">For more information about whether a message is supported offline, see <xref:Microsoft.Crm.Sdk.Messages>.</span><span class="sxs-lookup"><span data-stu-id="b8006-110">For more information about whether a message is supported offline, see <xref:Microsoft.Crm.Sdk.Messages>.</span></span> <span data-ttu-id="b8006-111">You can also determine whether a <xref:Microsoft.Xrm.Sdk.IOrganizationService> message works offline by checking the `SdkMessage.Availability` attribute for the desired message.</span><span class="sxs-lookup"><span data-stu-id="b8006-111">You can also determine whether a <xref:Microsoft.Xrm.Sdk.IOrganizationService> message works offline by checking the `SdkMessage.Availability` attribute for the desired message.</span></span> <span data-ttu-id="b8006-112">If the message works for multiple entity types, you must also check the `SdkMessageFilter.Availability` attribute to see whether the message is available offline for the entity you want to work with.</span><span class="sxs-lookup"><span data-stu-id="b8006-112">If the message works for multiple entity types, you must also check the `SdkMessageFilter.Availability` attribute to see whether the message is available offline for the entity you want to work with.</span></span> <span data-ttu-id="b8006-113">For example, the `Create` message is available offline, but not for the queue, user, or site entities.</span><span class="sxs-lookup"><span data-stu-id="b8006-113">For example, the `Create` message is available offline, but not for the queue, user, or site entities.</span></span>  
  
 <span data-ttu-id="b8006-114">Tracing can be enabled on the [!INCLUDE[pn_crm_outlook_offline_access](../../includes/pn-crm-outlook-offline-access.md)] for debugging.</span><span class="sxs-lookup"><span data-stu-id="b8006-114">Tracing can be enabled on the [!INCLUDE[pn_crm_outlook_offline_access](../../includes/pn-crm-outlook-offline-access.md)] for debugging.</span></span> <span data-ttu-id="b8006-115">For more information about the event viewer and platform tracing, see [Monitoring and troubleshooting Dynamics 365 for Customer Engagement apps](https://technet.microsoft.com/library/hh699694.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8006-115">For more information about the event viewer and platform tracing, see [Monitoring and troubleshooting Dynamics 365 for Customer Engagement apps](https://technet.microsoft.com/library/hh699694.aspx).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b8006-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b8006-116">See also</span></span>  
 <span data-ttu-id="b8006-117">[Extend Dynamics 365 for Customer Engagement apps on the server](../extend-dynamics-365-server.md) </span><span class="sxs-lookup"><span data-stu-id="b8006-117">[Extend Dynamics 365 for Customer Engagement apps on the server](../extend-dynamics-365-server.md) </span></span>  
 <span data-ttu-id="b8006-118">[Troubleshooting and error handling](troubleshooting-error-handling.md) </span><span class="sxs-lookup"><span data-stu-id="b8006-118">[Troubleshooting and error handling](troubleshooting-error-handling.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <span data-ttu-id="b8006-119">[Organization Service Methods](organization-service-methods.md) </span><span class="sxs-lookup"><span data-stu-id="b8006-119">[Organization Service Methods](organization-service-methods.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>
