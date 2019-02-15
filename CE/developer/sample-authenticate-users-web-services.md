---
title: 'Sample: Authenticate users with Dynamics 365 for Customer Engagement web services (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs'
description: This sample shows how to authenticate a user with any Microsoft Dynamics 365 for Customer Engagement deployment and obtain a reference to the web services.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 3bde1482-60d4-489b-8379-49d3bc2f4abc
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- authenticating users with Microsoft Dynamics CRM web services sample
- authenticating users with Microsoft Dynamics CRM web services, authentication sample
- sample for authenticating users with Microsoft Dynamics CRM web services
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c629bd4e94be7992e1140fd565d24798ee57afd2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385563"
---
# <a name="sample-authenticate-users-with-dynamics-365-for-customer-engagement-web-services"></a><span data-ttu-id="d9961-103">Sample: Authenticate users with Dynamics 365 for Customer Engagement web services</span><span class="sxs-lookup"><span data-stu-id="d9961-103">Sample: Authenticate users with Dynamics 365 for Customer Engagement web services</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d9961-104">This sample shows how to authenticate a user with any [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement deployment and obtain a reference to the web services.</span><span class="sxs-lookup"><span data-stu-id="d9961-104">This sample shows how to authenticate a user with any [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement deployment and obtain a reference to the web services.</span></span> <span data-ttu-id="d9961-105">This sample includes support for [!INCLUDE[pn_MS_Office_365](../includes/pn-ms-office-365.md)] users provisioned in [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="d9961-105">This sample includes support for [!INCLUDE[pn_MS_Office_365](../includes/pn-ms-office-365.md)] users provisioned in [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span></span>  
  
 <span data-ttu-id="d9961-106">Download the sample: [Authenticate users with Microsoft Dynamics 365 for Customer Engagement web services](https://code.msdn.microsoft.com/Authenticate-users-with-707e0375).</span><span class="sxs-lookup"><span data-stu-id="d9961-106">Download the sample: [Authenticate users with Microsoft Dynamics 365 for Customer Engagement web services](https://code.msdn.microsoft.com/Authenticate-users-with-707e0375).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d9961-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="d9961-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="d9961-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="d9961-108">Demonstrates</span></span>  
 <span data-ttu-id="d9961-109">This sample demonstrates how to authenticate a user with any [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] deployment and make web service calls.</span><span class="sxs-lookup"><span data-stu-id="d9961-109">This sample demonstrates how to authenticate a user with any [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] deployment and make web service calls.</span></span> <span data-ttu-id="d9961-110">This sample doesn’t rely on the CrmServiceHelpers.cs helper code.</span><span class="sxs-lookup"><span data-stu-id="d9961-110">This sample doesn’t rely on the CrmServiceHelpers.cs helper code.</span></span> <span data-ttu-id="d9961-111">For a sample that does use helper code, see [Sample: QuickStart sample program](sample-quick-start.md).</span><span class="sxs-lookup"><span data-stu-id="d9961-111">For a sample that does use helper code, see [Sample: QuickStart sample program](sample-quick-start.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d9961-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d9961-112">Example</span></span>  
 [!code-csharp[authenticatewithnohelp#authenticatewithnohelp](../snippets/csharp/CRMV8/authenticatewithnohelp/cs/authenticatewithnohelp.cs#authenticatewithnohelp)]  
  
### <a name="see-also"></a><span data-ttu-id="d9961-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d9961-113">See also</span></span>  
 <span data-ttu-id="d9961-114">[Authenticate Users with Dynamics 365 for Customer Engagement Web Services](authenticate-users.md) </span><span class="sxs-lookup"><span data-stu-id="d9961-114">[Authenticate Users with Dynamics 365 for Customer Engagement Web Services](authenticate-users.md) </span></span>  
 <span data-ttu-id="d9961-115">[Helper Code: ServerConnection Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="d9961-115">[Helper Code: ServerConnection Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="d9961-116">[Authenticate Office 365 Users with Dynamics 365 for Customer Engagement apps (online) Web Services](authenticate-office-365-users-customer-engagement-web-services.md) </span><span class="sxs-lookup"><span data-stu-id="d9961-116">[Authenticate Office 365 Users with Dynamics 365 for Customer Engagement apps (online) Web Services](authenticate-office-365-users-customer-engagement-web-services.md) </span></span>  
 [<span data-ttu-id="d9961-117">Connect with Microsoft Office 365 and Dynamics 365 for Customer Engagement apps (online)</span><span class="sxs-lookup"><span data-stu-id="d9961-117">Connect with Microsoft Office 365 and Dynamics 365 for Customer Engagement apps (online)</span></span>](connect-microsoft-office-365.md)
