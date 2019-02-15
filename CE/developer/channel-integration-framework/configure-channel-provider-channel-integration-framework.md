---
title: Configure channel provider in Channel Integration Framework (CIF) | Microsoft Docs
description: Learn how to configure a channel provider install and setup Channel Integration Framework (CIF) for Microsoft Dynamics 365.
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
ms.assetid: 5612019a-a4b5-4ba5-a232-6b7d66bdfc21
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: f1468992e4b761bba6b840a97a8dbc91fc862e77
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388499"
---
# <a name="how-to-configure-a-channel-provider-for-your-dynamics-365-organization"></a><span data-ttu-id="355df-103">How to configure a channel provider for your Dynamics 365 organization</span><span class="sxs-lookup"><span data-stu-id="355df-103">How to configure a channel provider for your Dynamics 365 organization</span></span>

<span data-ttu-id="355df-104">Using the Dynamics 365 Channel Integration Framework solution, you can configure channel providers.</span><span class="sxs-lookup"><span data-stu-id="355df-104">Using the Dynamics 365 Channel Integration Framework solution, you can configure channel providers.</span></span>
<span data-ttu-id="355df-105">To configure channel providers:</span><span class="sxs-lookup"><span data-stu-id="355df-105">To configure channel providers:</span></span>

1. <span data-ttu-id="355df-106">Sign-in to Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="355df-106">Sign-in to Dynamics 365.</span></span>

2. <span data-ttu-id="355df-107">Select the drop-down button on the Dynamics 365 and select **Channel Integration Framework**.</span><span class="sxs-lookup"><span data-stu-id="355df-107">Select the drop-down button on the Dynamics 365 and select **Channel Integration Framework**.</span></span>

  <span data-ttu-id="355df-108">![Dynamics 365 drop-down button to find Channel Integration Framework](media/cif-app-navigation.png "Dynamics 365 drop-down button to find Channel Integration Framework")</span><span class="sxs-lookup"><span data-stu-id="355df-108">![Dynamics 365 drop-down button to find Channel Integration Framework](media/cif-app-navigation.png "Dynamics 365 drop-down button to find Channel Integration Framework")</span></span>

3.  <span data-ttu-id="355df-109">Select **+ New** to add a new provider.</span><span class="sxs-lookup"><span data-stu-id="355df-109">Select **+ New** to add a new provider.</span></span>

4.  <span data-ttu-id="355df-110">In the **New Channel** page, specify the following:</span><span class="sxs-lookup"><span data-stu-id="355df-110">In the **New Channel** page, specify the following:</span></span>

  | <span data-ttu-id="355df-111">Trường</span><span class="sxs-lookup"><span data-stu-id="355df-111">Field</span></span> | <span data-ttu-id="355df-112">Mô tả</span><span class="sxs-lookup"><span data-stu-id="355df-112">Description</span></span> |
  |-------|-------|
  |<span data-ttu-id="355df-113">Tên</span><span class="sxs-lookup"><span data-stu-id="355df-113">Name</span></span>|<span data-ttu-id="355df-114">Name of the channel provider.</span><span class="sxs-lookup"><span data-stu-id="355df-114">Name of the channel provider.</span></span>|
  |<span data-ttu-id="355df-115">Nhãn</span><span class="sxs-lookup"><span data-stu-id="355df-115">Label</span></span>|<span data-ttu-id="355df-116">The label is displayed as the title on the widget.</span><span class="sxs-lookup"><span data-stu-id="355df-116">The label is displayed as the title on the widget.</span></span>|
  |<span data-ttu-id="355df-117">Channel URL</span><span class="sxs-lookup"><span data-stu-id="355df-117">Channel URL</span></span>|<span data-ttu-id="355df-118">The URL of the provider to host in the widget.</span><span class="sxs-lookup"><span data-stu-id="355df-118">The URL of the provider to host in the widget.</span></span> <span data-ttu-id="355df-119">See the JavaScript APIs on how to develop communication widget with Dynamics 365 Channel Integration Framework.</span><span class="sxs-lookup"><span data-stu-id="355df-119">See the JavaScript APIs on how to develop communication widget with Dynamics 365 Channel Integration Framework.</span></span>|
  |<span data-ttu-id="355df-120">Enable Outbound Communication</span><span class="sxs-lookup"><span data-stu-id="355df-120">Enable Outbound Communication</span></span>|<span data-ttu-id="355df-121">Clicking on a phone number in the Dynamics 365 Unified Interface page, the widget initiates the call or outbound communication.</span><span class="sxs-lookup"><span data-stu-id="355df-121">Clicking on a phone number in the Dynamics 365 Unified Interface page, the widget initiates the call or outbound communication.</span></span>|
  |<span data-ttu-id="355df-122">Channel Order</span><span class="sxs-lookup"><span data-stu-id="355df-122">Channel Order</span></span>|<span data-ttu-id="355df-123">The order precedence of the channel providers.</span><span class="sxs-lookup"><span data-stu-id="355df-123">The order precedence of the channel providers.</span></span> <span data-ttu-id="355df-124">That is, the priority to display the channel for the agents and unified Interface Apps.</span><span class="sxs-lookup"><span data-stu-id="355df-124">That is, the priority to display the channel for the agents and unified Interface Apps.</span></span>|
  |<span data-ttu-id="355df-125">API Version</span><span class="sxs-lookup"><span data-stu-id="355df-125">API Version</span></span>|<span data-ttu-id="355df-126">The version of the Channel Integration Framework APIs.</span><span class="sxs-lookup"><span data-stu-id="355df-126">The version of the Channel Integration Framework APIs.</span></span>|
  |<span data-ttu-id="355df-127">Trusted Domain</span><span class="sxs-lookup"><span data-stu-id="355df-127">Trusted Domain</span></span>| <span data-ttu-id="355df-128">An additional domain if the initial landing URL and the final domain from which the communication widget is hosted are different.</span><span class="sxs-lookup"><span data-stu-id="355df-128">An additional domain if the initial landing URL and the final domain from which the communication widget is hosted are different.</span></span> <span data-ttu-id="355df-129">Add the domain (URL) to access the Channel Integration Framework APIs.</span><span class="sxs-lookup"><span data-stu-id="355df-129">Add the domain (URL) to access the Channel Integration Framework APIs.</span></span> |
  |<span data-ttu-id="355df-130">Select the Unified Interface Apps for the Channel</span><span class="sxs-lookup"><span data-stu-id="355df-130">Select the Unified Interface Apps for the Channel</span></span>| <span data-ttu-id="355df-131">The list of Unified Interface Apps where the channel is displayed for the agents.</span><span class="sxs-lookup"><span data-stu-id="355df-131">The list of Unified Interface Apps where the channel is displayed for the agents.</span></span> |
  |<span data-ttu-id="355df-132">Select Roles for the Channel</span><span class="sxs-lookup"><span data-stu-id="355df-132">Select Roles for the Channel</span></span>|<span data-ttu-id="355df-133">The security roles that are present in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="355df-133">The security roles that are present in Dynamics 365.</span></span><br><span data-ttu-id="355df-134">**Note:** If you do not assign any role, the channel provider is shown to all users assigned for the Dynamics 365 Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="355df-134">**Note:** If you do not assign any role, the channel provider is shown to all users assigned for the Dynamics 365 Unified Interface App.</span></span>|
  |<span data-ttu-id="355df-135">Tham số Tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="355df-135">Custom Parameter</span></span>|<span data-ttu-id="355df-136">This takes a text blob as input and [Microsoft.CIFramework.getEnvironment](reference/microsoft-ciframework/getEnvironment.md) will return this as value of key `customParams`.</span><span class="sxs-lookup"><span data-stu-id="355df-136">This takes a text blob as input and [Microsoft.CIFramework.getEnvironment](reference/microsoft-ciframework/getEnvironment.md) will return this as value of key `customParams`.</span></span>|
  
  <span data-ttu-id="355df-137">![Channel provider configuration](media/channel-provider-configuration.PNG "Channel provider configuration")</span><span class="sxs-lookup"><span data-stu-id="355df-137">![Channel provider configuration](media/channel-provider-configuration.PNG "Channel provider configuration")</span></span>

  > [!Note]
  > <span data-ttu-id="355df-138">The msdyn_ciprovider entity is accessible only for the administrator roles and hence the panel will not load for a non-administrator roles.</span><span class="sxs-lookup"><span data-stu-id="355df-138">The msdyn_ciprovider entity is accessible only for the administrator roles and hence the panel will not load for a non-administrator roles.</span></span> <span data-ttu-id="355df-139">To load the panel for the non-administrator roles, create a new role and provide read-access to the msdyn_ciprovider entity.</span><span class="sxs-lookup"><span data-stu-id="355df-139">To load the panel for the non-administrator roles, create a new role and provide read-access to the msdyn_ciprovider entity.</span></span> <span data-ttu-id="355df-140">Now, add the role to the users who will be accessing the Channel Integration Framework.</span><span class="sxs-lookup"><span data-stu-id="355df-140">Now, add the role to the users who will be accessing the Channel Integration Framework.</span></span>

5. <span data-ttu-id="355df-141">Launch the Unified Interface App to see the communication widget on the right side.</span><span class="sxs-lookup"><span data-stu-id="355df-141">Launch the Unified Interface App to see the communication widget on the right side.</span></span><br><br>
<span data-ttu-id="355df-142">**The communication widget in the minimized mode**</span><span class="sxs-lookup"><span data-stu-id="355df-142">**The communication widget in the minimized mode**</span></span><br><br>
<span data-ttu-id="355df-143">![communication widget in the minimized mode](media/widget-minimized-mode.PNG "communication widget in the minimized mode")</span><span class="sxs-lookup"><span data-stu-id="355df-143">![communication widget in the minimized mode](media/widget-minimized-mode.PNG "communication widget in the minimized mode")</span></span>
<br><br>
<span data-ttu-id="355df-144">**The communication widget in the expanded mode**</span><span class="sxs-lookup"><span data-stu-id="355df-144">**The communication widget in the expanded mode**</span></span><br><br>
<span data-ttu-id="355df-145">![communication widget in the expanded mode](media/widget-expanded-mode.PNG "communication widget in the expanded mode")</span><span class="sxs-lookup"><span data-stu-id="355df-145">![communication widget in the expanded mode](media/widget-expanded-mode.PNG "communication widget in the expanded mode")</span></span>

> [!div class ="nextstepaction"]
> [<span data-ttu-id="355df-146">Enable outbound communication (ClickToAct)</span><span class="sxs-lookup"><span data-stu-id="355df-146">Enable outbound communication (ClickToAct)</span></span>](enable-outbound-communication-clicktoact.md)