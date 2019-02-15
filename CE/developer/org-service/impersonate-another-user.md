---
title: Impersonate another user (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn how to impersonate another user using Web API. You can do that by adding a request header named MSCRMCallerID with a GUID value equal to the impersonated user’s systemuserid before sending the request to the web service
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: fc54b5d4-00d7-4833-be95-3c66a920a84d
caps.latest.revision: 28
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8e5591730801dec2ca35e32fe14c9ad9ce513ce5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385927"
---
# <a name="impersonate-another-user"></a><span data-ttu-id="7e7e0-104">Impersonate another user</span><span class="sxs-lookup"><span data-stu-id="7e7e0-104">Impersonate another user</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7e7e0-105">Impersonation is used to execute business logic (code) on behalf of another [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps user to provide a desired feature or service using the appropriate role and object-based security of that impersonated user.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-105">Impersonation is used to execute business logic (code) on behalf of another [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps user to provide a desired feature or service using the appropriate role and object-based security of that impersonated user.</span></span> <span data-ttu-id="7e7e0-106">This is necessary because the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Web services can be called by various clients and services on behalf of a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps user, for example, in a workflow or custom ISV solution.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-106">This is necessary because the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Web services can be called by various clients and services on behalf of a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps user, for example, in a workflow or custom ISV solution.</span></span> <span data-ttu-id="7e7e0-107">Impersonation involves two different user accounts: one user account (A) is used when executing code to perform some task on behalf of another user (B).</span><span class="sxs-lookup"><span data-stu-id="7e7e0-107">Impersonation involves two different user accounts: one user account (A) is used when executing code to perform some task on behalf of another user (B).</span></span>  

## <a name="required-privileges"></a><span data-ttu-id="7e7e0-108">Đặc quyền yêu cầu</span><span class="sxs-lookup"><span data-stu-id="7e7e0-108">Required privileges</span></span>  
 <span data-ttu-id="7e7e0-109">User account (A) needs the privilege `prvActOnBehalfOfAnotherUser`, which is included in the **Delegate** security role.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-109">User account (A) needs the privilege `prvActOnBehalfOfAnotherUser`, which is included in the **Delegate** security role.</span></span>  

 <span data-ttu-id="7e7e0-110">The actual set of privileges that is used to modify data is the intersection of the privileges that the **Delegate** role user possesses with that of the user that is being impersonated.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-110">The actual set of privileges that is used to modify data is the intersection of the privileges that the **Delegate** role user possesses with that of the user that is being impersonated.</span></span> <span data-ttu-id="7e7e0-111">In other words, user A is allowed to do something if and only if user A and the impersonated user (B) have the privilege necessary for the action.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-111">In other words, user A is allowed to do something if and only if user A and the impersonated user (B) have the privilege necessary for the action.</span></span>  

## <a name="impersonate-a-user"></a><span data-ttu-id="7e7e0-112">Impersonate a user</span><span class="sxs-lookup"><span data-stu-id="7e7e0-112">Impersonate a user</span></span>  
 <span data-ttu-id="7e7e0-113">To impersonate a user, set the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.CallerId> property on an instance of <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy> before calling the service’s Web methods.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-113">To impersonate a user, set the <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.CallerId> property on an instance of <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy> before calling the service’s Web methods.</span></span>  

## <a name="deployment-specific-options"></a><span data-ttu-id="7e7e0-114">Deployment specific options</span><span class="sxs-lookup"><span data-stu-id="7e7e0-114">Deployment specific options</span></span>  
 <span data-ttu-id="7e7e0-115">Impersonation using a user account in the `PrivUserGroup` in [!INCLUDE[pn_Active_Directory](../../includes/pn-active-directory.md)] is no longer supported in the on-premises environment.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-115">Impersonation using a user account in the `PrivUserGroup` in [!INCLUDE[pn_Active_Directory](../../includes/pn-active-directory.md)] is no longer supported in the on-premises environment.</span></span>  <span data-ttu-id="7e7e0-116">In our ongoing design enhancement of the security protocol, we developed a better and more secure impersonation method.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-116">In our ongoing design enhancement of the security protocol, we developed a better and more secure impersonation method.</span></span>  <span data-ttu-id="7e7e0-117">The new method calls for using a [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] for Customer Enagement apps user and a [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] for Customer Engagement apps security role.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-117">The new method calls for using a [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] for Customer Enagement apps user and a [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] for Customer Engagement apps security role.</span></span>  <span data-ttu-id="7e7e0-118">With this method, the user’s privileges are managed through [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] for customer Engagement apps and activities are logged for the user.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-118">With this method, the user’s privileges are managed through [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] for customer Engagement apps and activities are logged for the user.</span></span> <span data-ttu-id="7e7e0-119">Please see the following table for details.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-119">Please see the following table for details.</span></span>  


|           <span data-ttu-id="7e7e0-120">Deployment Type</span><span class="sxs-lookup"><span data-stu-id="7e7e0-120">Deployment Type</span></span>            |                                                                                                                                                                                                                                    <span data-ttu-id="7e7e0-121">Deployment Type  Strategy</span><span class="sxs-lookup"><span data-stu-id="7e7e0-121">Deployment Type  Strategy</span></span>                                                                                                                                                                                                                                     |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                <span data-ttu-id="7e7e0-122">Trực tuyến</span><span class="sxs-lookup"><span data-stu-id="7e7e0-122">Online</span></span>                | <span data-ttu-id="7e7e0-123">-   Use the special  *application user* described in [Build web applications using Server-to-Server (S2S) authentication](../build-web-applications-server-server-s2s-authentication.md) to control the privileges that the [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] for Customer Engagement apps user has access to.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-123">-   Use the special  *application user* described in [Build web applications using Server-to-Server (S2S) authentication](../build-web-applications-server-server-s2s-authentication.md) to control the privileges that the [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] for Customer Engagement apps user has access to.</span></span><br /><span data-ttu-id="7e7e0-124">-   Grant the application user a security role that includes privileges for the tasks this user will perform on behalf of other users and the `prvActOnBehalfOfAnotherUser` privilege.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-124">-   Grant the application user a security role that includes privileges for the tasks this user will perform on behalf of other users and the `prvActOnBehalfOfAnotherUser` privilege.</span></span> |
| <span data-ttu-id="7e7e0-125">On-premises</span><span class="sxs-lookup"><span data-stu-id="7e7e0-125">On-premises</span></span><br /> <span data-ttu-id="7e7e0-126">hoặc</span><span class="sxs-lookup"><span data-stu-id="7e7e0-126">or</span></span><br /><span data-ttu-id="7e7e0-127">IFD/Claims</span><span class="sxs-lookup"><span data-stu-id="7e7e0-127">IFD/Claims</span></span> |                                                                                                        <span data-ttu-id="7e7e0-128">Create a new [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] user with a security role which includes the `prvActOnBehalfOfAnotherUser` privilege.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-128">Create a new [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] user with a security role which includes the `prvActOnBehalfOfAnotherUser` privilege.</span></span> <span data-ttu-id="7e7e0-129">Within this security role, also include privileges for the tasks this user account will perform on behalf of other users.</span><span class="sxs-lookup"><span data-stu-id="7e7e0-129">Within this security role, also include privileges for the tasks this user account will perform on behalf of other users.</span></span>                                                                                                         |

### <a name="see-also"></a><span data-ttu-id="7e7e0-130">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7e7e0-130">See also</span></span>  
 <span data-ttu-id="7e7e0-131">[Authenticate Users with Dynamics 365 for Customer Engagement Web Services](../authenticate-users.md) </span><span class="sxs-lookup"><span data-stu-id="7e7e0-131">[Authenticate Users with Dynamics 365 for Customer Engagement Web Services](../authenticate-users.md) </span></span>  
 <span data-ttu-id="7e7e0-132">[Implement Single Sign-on from an ASPX Webpage or IFRAME](../implement-single-sign-aspx-webpage-iframe.md)   </span><span class="sxs-lookup"><span data-stu-id="7e7e0-132">[Implement Single Sign-on from an ASPX Webpage or IFRAME](../implement-single-sign-aspx-webpage-iframe.md)   </span></span>  
 <span data-ttu-id="7e7e0-133">[How Role-Based Security Can Be Used to Control Access to Entities In Dynamics 365 for Customer Engagement apps](../security-dev/how-role-based-security-control-access-entities.md) </span><span class="sxs-lookup"><span data-stu-id="7e7e0-133">[How Role-Based Security Can Be Used to Control Access to Entities In Dynamics 365 for Customer Engagement apps](../security-dev/how-role-based-security-control-access-entities.md) </span></span>  
 [<span data-ttu-id="7e7e0-134">Sample: Impersonation using the ActOnBehalfOf privilege</span><span class="sxs-lookup"><span data-stu-id="7e7e0-134">Sample: Impersonation using the ActOnBehalfOf privilege</span></span>](sample-impersonate-actonbehalfof-privilege.md)