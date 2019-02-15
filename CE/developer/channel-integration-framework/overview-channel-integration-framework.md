---
title: What is Dynamics 365 Channel Integration Framework (CIF) | Microsoft Docs
description: Learn what is Channel Integration Framework (CIF) for Microsoft Dynamics 365 and how to get started using it.
keywords: ''
ms.date: 12/10/2018
ms.service:
- dynamics-365-cross-app
ms.custom:
- dyn365-a11y
- dyn365-developer
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement Version 9.x
ms.assetid: e6d23c5f-e4ec-41f7-aff7-9cb50828357f
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: 88ce6710c4f9073db5039f08b8a563e025ada51a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387958"
---
# <a name="what-is-channel-integration-framework-for-microsoft-dynamics-365"></a><span data-ttu-id="b893f-103">What is Channel Integration Framework for Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b893f-103">What is Channel Integration Framework for Microsoft Dynamics 365</span></span>

<span data-ttu-id="b893f-104">Dynamics 365 Channel Integration Framework is a cloud-to-cloud extensible framework to integrate third-party channel providers with Dynamics 365 Unified Interface Apps using a browser-based JavaScript API library.</span><span class="sxs-lookup"><span data-stu-id="b893f-104">Dynamics 365 Channel Integration Framework is a cloud-to-cloud extensible framework to integrate third-party channel providers with Dynamics 365 Unified Interface Apps using a browser-based JavaScript API library.</span></span>

<span data-ttu-id="b893f-105">With this framework, you can integrate any third-party channel provider or channel aggregators into Unified Interface Apps, where the Channel Integration Framework acts as an interface between the providers or aggregators and Unified Interface Apps.</span><span class="sxs-lookup"><span data-stu-id="b893f-105">With this framework, you can integrate any third-party channel provider or channel aggregators into Unified Interface Apps, where the Channel Integration Framework acts as an interface between the providers or aggregators and Unified Interface Apps.</span></span>

<span data-ttu-id="b893f-106">Technically, Channel Integration Framework is a set of APIs (methods, events, and protocols) that enable developers and partners to build immersive communication experiences such that third party communication widgets running on channel provider cloud can interact with Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b893f-106">Technically, Channel Integration Framework is a set of APIs (methods, events, and protocols) that enable developers and partners to build immersive communication experiences such that third party communication widgets running on channel provider cloud can interact with Dynamics 365.</span></span> 

<span data-ttu-id="b893f-107">With the Channel Integration Framework application (solution), you can configure the channel in the Unified Interface app such that your agents can access to serve your customers.</span><span class="sxs-lookup"><span data-stu-id="b893f-107">With the Channel Integration Framework application (solution), you can configure the channel in the Unified Interface app such that your agents can access to serve your customers.</span></span>

## <a name="challenges-of-channel-provider-integration-systems"></a><span data-ttu-id="b893f-108">Challenges of channel provider integration systems</span><span class="sxs-lookup"><span data-stu-id="b893f-108">Challenges of channel provider integration systems</span></span>

<span data-ttu-id="b893f-109">Organizations expect their call centers to do more with fewer resources, and there is a constant drive to increase productivity in terms of call center agents handling more chats, phone calls, emails, and so on.</span><span class="sxs-lookup"><span data-stu-id="b893f-109">Organizations expect their call centers to do more with fewer resources, and there is a constant drive to increase productivity in terms of call center agents handling more chats, phone calls, emails, and so on.</span></span> <span data-ttu-id="b893f-110">Reducing the average time to handle customers can save companies millions of dollars.</span><span class="sxs-lookup"><span data-stu-id="b893f-110">Reducing the average time to handle customers can save companies millions of dollars.</span></span> <span data-ttu-id="b893f-111">Channel providers (Computer Telephony Integration (CTI), messaging, and email systems) in call centers are one of the key indicators for the success and customer satisfaction.</span><span class="sxs-lookup"><span data-stu-id="b893f-111">Channel providers (Computer Telephony Integration (CTI), messaging, and email systems) in call centers are one of the key indicators for the success and customer satisfaction.</span></span> <span data-ttu-id="b893f-112">On that context, some of the challenges that call center industry faces with the channel providers (CTI, messaging (SMS), and the email systems) are as follows:</span><span class="sxs-lookup"><span data-stu-id="b893f-112">On that context, some of the challenges that call center industry faces with the channel providers (CTI, messaging (SMS), and the email systems) are as follows:</span></span>

  - <span data-ttu-id="b893f-113">Integrating third-party channel providers into the Customer Relationship Management (CRM) platforms.</span><span class="sxs-lookup"><span data-stu-id="b893f-113">Integrating third-party channel providers into the Customer Relationship Management (CRM) platforms.</span></span>
  - <span data-ttu-id="b893f-114">Accessing and performing operations on the CRM from the CTI, messaging (SMS), and the email systems.</span><span class="sxs-lookup"><span data-stu-id="b893f-114">Accessing and performing operations on the CRM from the CTI, messaging (SMS), and the email systems.</span></span>
  - <span data-ttu-id="b893f-115">Developing and deploying CTI, messaging (SMS), and the email system needs writing adapters and complex custom codes for solution integration.</span><span class="sxs-lookup"><span data-stu-id="b893f-115">Developing and deploying CTI, messaging (SMS), and the email system needs writing adapters and complex custom codes for solution integration.</span></span>
  - <span data-ttu-id="b893f-116">Using APIs and out-of-box customization which are not supported for the production environment.</span><span class="sxs-lookup"><span data-stu-id="b893f-116">Using APIs and out-of-box customization which are not supported for the production environment.</span></span>
  - <span data-ttu-id="b893f-117">Channel providers (CTI, messaging (SMS), and the email systems) dependency on the operating system and web browsers.</span><span class="sxs-lookup"><span data-stu-id="b893f-117">Channel providers (CTI, messaging (SMS), and the email systems) dependency on the operating system and web browsers.</span></span>
  - <span data-ttu-id="b893f-118">Customizing the channel provider (CTI, messaging (SMS), and the email systems) based on the business and process workflows.</span><span class="sxs-lookup"><span data-stu-id="b893f-118">Customizing the channel provider (CTI, messaging (SMS), and the email systems) based on the business and process workflows.</span></span>

## <a name="advantages-and-value-propositions-of-channel-integration-framework"></a><span data-ttu-id="b893f-119">Advantages and value propositions of Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="b893f-119">Advantages and value propositions of Channel Integration Framework</span></span>

<span data-ttu-id="b893f-120">The value propositions of Channel Integration Framework are:</span><span class="sxs-lookup"><span data-stu-id="b893f-120">The value propositions of Channel Integration Framework are:</span></span>

<span data-ttu-id="b893f-121">**Bring your own channel providers (Integrate third-party channel providers):**</span><span class="sxs-lookup"><span data-stu-id="b893f-121">**Bring your own channel providers (Integrate third-party channel providers):**</span></span>

<span data-ttu-id="b893f-122">The Channel Integration Framework provides an extensible framework to integrate third-party cloud-based channel providers or channel aggregators with Dynamics 365 Unified Interface Apps.</span><span class="sxs-lookup"><span data-stu-id="b893f-122">The Channel Integration Framework provides an extensible framework to integrate third-party cloud-based channel providers or channel aggregators with Dynamics 365 Unified Interface Apps.</span></span>

<span data-ttu-id="b893f-123">**Channel agnostic:** The Channel Integration Framework is channel agnostic.</span><span class="sxs-lookup"><span data-stu-id="b893f-123">**Channel agnostic:** The Channel Integration Framework is channel agnostic.</span></span> <span data-ttu-id="b893f-124">That is, you can build channels like voice, video, chat, co-browse, social media, and any channels as long as they a JavaScript based widget.</span><span class="sxs-lookup"><span data-stu-id="b893f-124">That is, you can build channels like voice, video, chat, co-browse, social media, and any channels as long as they a JavaScript based widget.</span></span>

<span data-ttu-id="b893f-125">**Two-way communication:**</span><span class="sxs-lookup"><span data-stu-id="b893f-125">**Two-way communication:**</span></span>

<span data-ttu-id="b893f-126">The framework is extensible for the configuration of communication between the channel and Dynamics 365 Unified Interface Apps.</span><span class="sxs-lookup"><span data-stu-id="b893f-126">The framework is extensible for the configuration of communication between the channel and Dynamics 365 Unified Interface Apps.</span></span> <span data-ttu-id="b893f-127">The two-way communication enables to set the context of inbound and/or outbound according to your business and process workflows.</span><span class="sxs-lookup"><span data-stu-id="b893f-127">The two-way communication enables to set the context of inbound and/or outbound according to your business and process workflows.</span></span>

<span data-ttu-id="b893f-128">**Standard and supported APIs:**</span><span class="sxs-lookup"><span data-stu-id="b893f-128">**Standard and supported APIs:**</span></span>

<span data-ttu-id="b893f-129">The Channel Integration Framework exposes a JavaScript APIs which are the standard set of APIs that you can consume for the communication between the channels and Dynamics 365 Unified Interface Apps.</span><span class="sxs-lookup"><span data-stu-id="b893f-129">The Channel Integration Framework exposes a JavaScript APIs which are the standard set of APIs that you can consume for the communication between the channels and Dynamics 365 Unified Interface Apps.</span></span>

<span data-ttu-id="b893f-130">**Ease of development and deployment:**</span><span class="sxs-lookup"><span data-stu-id="b893f-130">**Ease of development and deployment:**</span></span>

<span data-ttu-id="b893f-131">Seamless development, implementation, and deployment experience of your channels to suit your business context and process workflows.</span><span class="sxs-lookup"><span data-stu-id="b893f-131">Seamless development, implementation, and deployment experience of your channels to suit your business context and process workflows.</span></span>

<span data-ttu-id="b893f-132">**Plug and play configuration:**</span><span class="sxs-lookup"><span data-stu-id="b893f-132">**Plug and play configuration:**</span></span>

<span data-ttu-id="b893f-133">You can seamlessly integrate several providers by using the Channel Integration Framework administration configuration App.</span><span class="sxs-lookup"><span data-stu-id="b893f-133">You can seamlessly integrate several providers by using the Channel Integration Framework administration configuration App.</span></span>

<span data-ttu-id="b893f-134">**Unified Interface App agnostic:**</span><span class="sxs-lookup"><span data-stu-id="b893f-134">**Unified Interface App agnostic:**</span></span>

<span data-ttu-id="b893f-135">The Channel Integration Framework is Dynamics 365 Unified Interface App agnostic.</span><span class="sxs-lookup"><span data-stu-id="b893f-135">The Channel Integration Framework is Dynamics 365 Unified Interface App agnostic.</span></span> <span data-ttu-id="b893f-136">You can build the channel integration one-time and enable it on the Unified Interface Apps of your choice based on the business requirements.</span><span class="sxs-lookup"><span data-stu-id="b893f-136">You can build the channel integration one-time and enable it on the Unified Interface Apps of your choice based on the business requirements.</span></span>

<span data-ttu-id="b893f-137">**Independent of operating systems and web browsers:**</span><span class="sxs-lookup"><span data-stu-id="b893f-137">**Independent of operating systems and web browsers:**</span></span>

<span data-ttu-id="b893f-138">The Channel Integration Framework is web browser and operating system agnostic, and lets you integrate the cloud-based channels of your choice that is best for your organization's requirement.</span><span class="sxs-lookup"><span data-stu-id="b893f-138">The Channel Integration Framework is web browser and operating system agnostic, and lets you integrate the cloud-based channels of your choice that is best for your organization's requirement.</span></span>

<span data-ttu-id="b893f-139">**Support for Screen pop:**</span><span class="sxs-lookup"><span data-stu-id="b893f-139">**Support for Screen pop:**</span></span>

<span data-ttu-id="b893f-140">You can configure screen pops to display the customer information that can aid the agents to start the conversation efficiently and effectively.</span><span class="sxs-lookup"><span data-stu-id="b893f-140">You can configure screen pops to display the customer information that can aid the agents to start the conversation efficiently and effectively.</span></span>

<span data-ttu-id="b893f-141">**Customize agent experience:**</span><span class="sxs-lookup"><span data-stu-id="b893f-141">**Customize agent experience:**</span></span>

<span data-ttu-id="b893f-142">You can customize the channel programmatically or manually to provide enhanced agent experience like maximizing, minimizing, show, hide, height, width, pop-out and so on.</span><span class="sxs-lookup"><span data-stu-id="b893f-142">You can customize the channel programmatically or manually to provide enhanced agent experience like maximizing, minimizing, show, hide, height, width, pop-out and so on.</span></span>

<span data-ttu-id="b893f-143">**Upgrade to new versions:**</span><span class="sxs-lookup"><span data-stu-id="b893f-143">**Upgrade to new versions:**</span></span>

<span data-ttu-id="b893f-144">Seamless upgrade to new versions of third-party channel providers or channel aggregators as the Channel Integration Framework provides the infrastructure framework to integrate the channels but does not control the channel versions.</span><span class="sxs-lookup"><span data-stu-id="b893f-144">Seamless upgrade to new versions of third-party channel providers or channel aggregators as the Channel Integration Framework provides the infrastructure framework to integrate the channels but does not control the channel versions.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="b893f-145">Architecture overview of Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="b893f-145">Architecture overview of Channel Integration Framework</span></span>](architecture-overview-channel-integration-framework.md)

## <a name="see-also"></a><span data-ttu-id="b893f-146">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b893f-146">See also</span></span>

[<span data-ttu-id="b893f-147">System requirements of Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="b893f-147">System requirements of Channel Integration Framework</span></span>](system-requirements-channel-integration-framework.md)

[<span data-ttu-id="b893f-148">FAQs</span><span class="sxs-lookup"><span data-stu-id="b893f-148">FAQs</span></span>](faq-channel-integration-framework.md)

[<span data-ttu-id="b893f-149">Get Channel Integration Framework (CIF)</span><span class="sxs-lookup"><span data-stu-id="b893f-149">Get Channel Integration Framework (CIF)</span></span>](get-channel-integration-framework.md)