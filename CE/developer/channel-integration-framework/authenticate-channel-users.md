---
title: Authenticate channel users in Channel Integration Framework (CIF) | Microsoft Docs
description: Learn how to authenticate channel users in the Channel Integration Framework (CIF) for Microsoft Dynamics 365 for Customer Engagement apps. The Channel Integration Framework supports the SAML based Single Sign-On (SSO) for your agents or users to log in to the widget (channel).
keywords: ''
ms.date: 12/10/2018
ms.service:
- dynamics-365-cross-app
ms.custom:
- dyn365-a11y
- dyn365-developer
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement Version 9.x
ms.assetid: 47B90869-152B-48A6-A249-F37059FF9C12
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: 06eb248ba1011e60f0c1e58cfa50f76b3030d3a5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385617"
---
# <a name="authenticate-channel-users-to-the-log-in-to-the-channel"></a><span data-ttu-id="8fb49-104">Authenticate channel users to the log in to the channel</span><span class="sxs-lookup"><span data-stu-id="8fb49-104">Authenticate channel users to the log in to the channel</span></span>

<span data-ttu-id="8fb49-105">The Dynamics 365 Channel Integration Framework supports the SAML based Single Sign-On (SSO) for your users (agents) to log in to the channel (widget).</span><span class="sxs-lookup"><span data-stu-id="8fb49-105">The Dynamics 365 Channel Integration Framework supports the SAML based Single Sign-On (SSO) for your users (agents) to log in to the channel (widget).</span></span> <span data-ttu-id="8fb49-106">The SAML based SSO is available for Dynamics 365 online where the communication widget hosts the channel.</span><span class="sxs-lookup"><span data-stu-id="8fb49-106">The SAML based SSO is available for Dynamics 365 online where the communication widget hosts the channel.</span></span> <span data-ttu-id="8fb49-107">To enable SAML based SSO for the channel (widget), you must (administrator) register the channel (widget) in the Azure Active Directory portal as a multi-tenant application, where you have registered the Dynamics 365 Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="8fb49-107">To enable SAML based SSO for the channel (widget), you must (administrator) register the channel (widget) in the Azure Active Directory portal as a multi-tenant application, where you have registered the Dynamics 365 Unified Interface App.</span></span>

<span data-ttu-id="8fb49-108">After you register, the Azure Active Directory administrator must grant access to the channel (widget) to the users (agents).</span><span class="sxs-lookup"><span data-stu-id="8fb49-108">After you register, the Azure Active Directory administrator must grant access to the channel (widget) to the users (agents).</span></span>

<span data-ttu-id="8fb49-109">If you enable SAML based SSO, the channel (widget) aligns with the Dynamics 365 Unified Interface App inactivity timeout period and signs-out the users (agents) from both the channel (widget) and Dynamics 365 Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="8fb49-109">If you enable SAML based SSO, the channel (widget) aligns with the Dynamics 365 Unified Interface App inactivity timeout period and signs-out the users (agents) from both the channel (widget) and Dynamics 365 Unified Interface App.</span></span>

<span data-ttu-id="8fb49-110">To enable SSO for the channel (widget), perform the following:</span><span class="sxs-lookup"><span data-stu-id="8fb49-110">To enable SSO for the channel (widget), perform the following:</span></span>

1. <span data-ttu-id="8fb49-111">Register the third-party widget (channel) in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8fb49-111">Register the third-party widget (channel) in Azure Active Directory.</span></span>
    <span data-ttu-id="8fb49-112">a.</span><span class="sxs-lookup"><span data-stu-id="8fb49-112">a.</span></span> <span data-ttu-id="8fb49-113">Enter basic SAML configuration.</span><span class="sxs-lookup"><span data-stu-id="8fb49-113">Enter basic SAML configuration.</span></span>
    <span data-ttu-id="8fb49-114">b.</span><span class="sxs-lookup"><span data-stu-id="8fb49-114">b.</span></span> <span data-ttu-id="8fb49-115">Review or customize the claims issued in the SAML token.</span><span class="sxs-lookup"><span data-stu-id="8fb49-115">Review or customize the claims issued in the SAML token.</span></span>
    <span data-ttu-id="8fb49-116">c.</span><span class="sxs-lookup"><span data-stu-id="8fb49-116">c.</span></span> <span data-ttu-id="8fb49-117">Review certificate expiration data, status, and email notification.</span><span class="sxs-lookup"><span data-stu-id="8fb49-117">Review certificate expiration data, status, and email notification.</span></span>
    <span data-ttu-id="8fb49-118">d.</span><span class="sxs-lookup"><span data-stu-id="8fb49-118">d.</span></span> <span data-ttu-id="8fb49-119">Set up the target application.</span><span class="sxs-lookup"><span data-stu-id="8fb49-119">Set up the target application.</span></span>
    <span data-ttu-id="8fb49-120">e.</span><span class="sxs-lookup"><span data-stu-id="8fb49-120">e.</span></span> <span data-ttu-id="8fb49-121">Assign users and groups to your SAML application.</span><span class="sxs-lookup"><span data-stu-id="8fb49-121">Assign users and groups to your SAML application.</span></span>
    <span data-ttu-id="8fb49-122">f.</span><span class="sxs-lookup"><span data-stu-id="8fb49-122">f.</span></span> <span data-ttu-id="8fb49-123">Test the SAML application.</span><span class="sxs-lookup"><span data-stu-id="8fb49-123">Test the SAML application.</span></span>

<span data-ttu-id="8fb49-124">For more information on how to register and configure the channel (widget), visit [Configure SSO to applications](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/configure-single-sign-on-non-gallery-applications).</span><span class="sxs-lookup"><span data-stu-id="8fb49-124">For more information on how to register and configure the channel (widget), visit [Configure SSO to applications](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/configure-single-sign-on-non-gallery-applications).</span></span>

2. <span data-ttu-id="8fb49-125">Authorize access to Azure Active Directory web applications using the OAuth 2.0 code grant flow.</span><span class="sxs-lookup"><span data-stu-id="8fb49-125">Authorize access to Azure Active Directory web applications using the OAuth 2.0 code grant flow.</span></span>
    <span data-ttu-id="8fb49-126">a.</span><span class="sxs-lookup"><span data-stu-id="8fb49-126">a.</span></span> <span data-ttu-id="8fb49-127">Request an authorization code.</span><span class="sxs-lookup"><span data-stu-id="8fb49-127">Request an authorization code.</span></span>
    <span data-ttu-id="8fb49-128">b.</span><span class="sxs-lookup"><span data-stu-id="8fb49-128">b.</span></span> <span data-ttu-id="8fb49-129">Use the authorization code to request an access token.</span><span class="sxs-lookup"><span data-stu-id="8fb49-129">Use the authorization code to request an access token.</span></span>
    <span data-ttu-id="8fb49-130">c.</span><span class="sxs-lookup"><span data-stu-id="8fb49-130">c.</span></span> <span data-ttu-id="8fb49-131">Use the access token to access the resource.</span><span class="sxs-lookup"><span data-stu-id="8fb49-131">Use the access token to access the resource.</span></span>
    <span data-ttu-id="8fb49-132">d.</span><span class="sxs-lookup"><span data-stu-id="8fb49-132">d.</span></span> <span data-ttu-id="8fb49-133">Refreshing the access tokens.</span><span class="sxs-lookup"><span data-stu-id="8fb49-133">Refreshing the access tokens.</span></span>

<span data-ttu-id="8fb49-134">For more information on how to authorize access to Azure Active Directory web applications, visit [OAuth 2.0](https://docs.microsoft.com/en-us/azure/active-directory/develop/v1-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="8fb49-134">For more information on how to authorize access to Azure Active Directory web applications, visit [OAuth 2.0](https://docs.microsoft.com/en-us/azure/active-directory/develop/v1-protocols-oauth-code).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="8fb49-135">Pass Dynamics 365 URL to widget library</span><span class="sxs-lookup"><span data-stu-id="8fb49-135">Pass Dynamics 365 URL to widget library</span></span>](pass-url-widget-library.md)

## <a name="see-also"></a><span data-ttu-id="8fb49-136">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8fb49-136">See Also</span></span>

[<span data-ttu-id="8fb49-137">Configure channel provider for your Dynamics 365 organization</span><span class="sxs-lookup"><span data-stu-id="8fb49-137">Configure channel provider for your Dynamics 365 organization</span></span>](configure-channel-provider-channel-integration-framework.md)<br />
[<span data-ttu-id="8fb49-138">Enable outbound communication (ClickToAct)</span><span class="sxs-lookup"><span data-stu-id="8fb49-138">Enable outbound communication (ClickToAct)</span></span>](enable-outbound-communication-clicktoact.md)<br />
[<span data-ttu-id="8fb49-139">Add Channel Integration Framework solution as a dependent solution</span><span class="sxs-lookup"><span data-stu-id="8fb49-139">Add Channel Integration Framework solution as a dependent solution</span></span>](add-cif-solution-dependent-solution.md)<br />
[<span data-ttu-id="8fb49-140">Pass Dynamics 365 URL to widget library</span><span class="sxs-lookup"><span data-stu-id="8fb49-140">Pass Dynamics 365 URL to widget library</span></span>](pass-url-widget-library.md)