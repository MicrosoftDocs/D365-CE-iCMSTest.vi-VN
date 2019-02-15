---
title: FAQs for Channel Integration Framework (CIF) in Dynamics 365 | MicrosoftDocs
description: Frequently asked questions about the Channel Integration Framework (CIF) and its APIs for Dynamics 365.
keywords: ''
ms.date: 12/10/2018
ms.service:
- dynamics-365-cross-app
ms.custom:
- dyn365-a11y
- dyn365-developer
ms.topic: reference
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement Version 9.x
ms.assetid: 25004203-DE03-4DEC-BE4A-E4E89784A4F3
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: 624469901eda5c4a9f4714dc1261590454ec548c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387658"
---
# <a name="frequently-asked-questions-faqs-for-dynamics-365-channel-integration-framework-cif"></a><span data-ttu-id="dd661-103">Frequently asked questions (FAQs) for Dynamics 365 Channel Integration Framework (CIF)</span><span class="sxs-lookup"><span data-stu-id="dd661-103">Frequently asked questions (FAQs) for Dynamics 365 Channel Integration Framework (CIF)</span></span>

## <a name="what-is-dynamics-365-channel-integration-framework"></a><span data-ttu-id="dd661-104">What is Dynamics 365 Channel Integration Framework?</span><span class="sxs-lookup"><span data-stu-id="dd661-104">What is Dynamics 365 Channel Integration Framework?</span></span>
<span data-ttu-id="dd661-105">Dynamics 365 Channel Integration Framework is a cloud-to-cloud extensible framework to integrate third-party channel providers with Dynamics 365 Unified Interface Apps using a browser-based JavaScript API library.</span><span class="sxs-lookup"><span data-stu-id="dd661-105">Dynamics 365 Channel Integration Framework is a cloud-to-cloud extensible framework to integrate third-party channel providers with Dynamics 365 Unified Interface Apps using a browser-based JavaScript API library.</span></span>

## <a name="can-i-integrate-a-two-way-communication-channel"></a><span data-ttu-id="dd661-106">Can I integrate a two-way communication channel?</span><span class="sxs-lookup"><span data-stu-id="dd661-106">Can I integrate a two-way communication channel?</span></span>
<span data-ttu-id="dd661-107">Yes, you can integrate two-way communication that enables you to set the context of inbound and/or outbound according to your business and process workflows.</span><span class="sxs-lookup"><span data-stu-id="dd661-107">Yes, you can integrate two-way communication that enables you to set the context of inbound and/or outbound according to your business and process workflows.</span></span>

## <a name="does-channel-integration-framework-work-with-unified-interface-apps"></a><span data-ttu-id="dd661-108">Does Channel Integration Framework work with Unified Interface Apps?</span><span class="sxs-lookup"><span data-stu-id="dd661-108">Does Channel Integration Framework work with Unified Interface Apps?</span></span>
<span data-ttu-id="dd661-109">Yes, Channel Integration Framework works only with Unified Interface Apps.</span><span class="sxs-lookup"><span data-stu-id="dd661-109">Yes, Channel Integration Framework works only with Unified Interface Apps.</span></span> <span data-ttu-id="dd661-110">As of now, Channel Integration Framework does not support Web Client.</span><span class="sxs-lookup"><span data-stu-id="dd661-110">As of now, Channel Integration Framework does not support Web Client.</span></span>

## <a name="is-channel-integration-framework-a-softphone"></a><span data-ttu-id="dd661-111">Is Channel Integration Framework a softphone?</span><span class="sxs-lookup"><span data-stu-id="dd661-111">Is Channel Integration Framework a softphone?</span></span>
<span data-ttu-id="dd661-112">No, Channel Integration Framework provides an extensible framework to integrate third-party channel providers (softphones, chat, and SMS) with Dynamics 365 Unified Interface Apps.</span><span class="sxs-lookup"><span data-stu-id="dd661-112">No, Channel Integration Framework provides an extensible framework to integrate third-party channel providers (softphones, chat, and SMS) with Dynamics 365 Unified Interface Apps.</span></span>

## <a name="does-channel-integration-framework-make-calls-or-send-messages"></a><span data-ttu-id="dd661-113">Does Channel Integration Framework make calls or send messages?</span><span class="sxs-lookup"><span data-stu-id="dd661-113">Does Channel Integration Framework make calls or send messages?</span></span>
<span data-ttu-id="dd661-114">No, Channel Integration Framework provides an extensible framework to configure the channel provider to make inbound or/and outbound calls or messages.</span><span class="sxs-lookup"><span data-stu-id="dd661-114">No, Channel Integration Framework provides an extensible framework to configure the channel provider to make inbound or/and outbound calls or messages.</span></span>

## <a name="is-channel-integration-framework-a-server-side-api"></a><span data-ttu-id="dd661-115">Is Channel Integration Framework a server-side API?</span><span class="sxs-lookup"><span data-stu-id="dd661-115">Is Channel Integration Framework a server-side API?</span></span>
<span data-ttu-id="dd661-116">No, Channel Integration Framework provides a JavaScript library that exposes APIs that you can consume to perform the following operations:</span><span class="sxs-lookup"><span data-stu-id="dd661-116">No, Channel Integration Framework provides a JavaScript library that exposes APIs that you can consume to perform the following operations:</span></span>
- <span data-ttu-id="dd661-117">Create, retrieve, update, and delete entity records</span><span class="sxs-lookup"><span data-stu-id="dd661-117">Create, retrieve, update, and delete entity records</span></span>
- <span data-ttu-id="dd661-118">Getting and setting Click-to-Act functionality</span><span class="sxs-lookup"><span data-stu-id="dd661-118">Getting and setting Click-to-Act functionality</span></span>
- <span data-ttu-id="dd661-119">Search among records of a particular entity type</span><span class="sxs-lookup"><span data-stu-id="dd661-119">Search among records of a particular entity type</span></span>
- <span data-ttu-id="dd661-120">Getting and setting the panel width and so on</span><span class="sxs-lookup"><span data-stu-id="dd661-120">Getting and setting the panel width and so on</span></span>

<span data-ttu-id="dd661-121">More information: [Microsoft.CIFramework methods (CIF JavaScript API reference)](reference/microsoft-ciframework.md).</span><span class="sxs-lookup"><span data-stu-id="dd661-121">More information: [Microsoft.CIFramework methods (CIF JavaScript API reference)](reference/microsoft-ciframework.md).</span></span>

## <a name="does-channel-integration-framework-manage-call-or-chat-sessions"></a><span data-ttu-id="dd661-122">Does Channel Integration Framework manage call or chat sessions?</span><span class="sxs-lookup"><span data-stu-id="dd661-122">Does Channel Integration Framework manage call or chat sessions?</span></span>
<span data-ttu-id="dd661-123">No, Channel Integration Framework does not manage call or chat sessions.</span><span class="sxs-lookup"><span data-stu-id="dd661-123">No, Channel Integration Framework does not manage call or chat sessions.</span></span>

## <a name="is-channel-integration-framework-dependent-on-operating-systems-and-browsers"></a><span data-ttu-id="dd661-124">Is Channel Integration Framework dependent on operating systems and browsers?</span><span class="sxs-lookup"><span data-stu-id="dd661-124">Is Channel Integration Framework dependent on operating systems and browsers?</span></span>
<span data-ttu-id="dd661-125">No, Channel Integration Framework is operating system and web browser agnostic and lets you integrate the cloud-based channels of your choice that are best for organization requirements.</span><span class="sxs-lookup"><span data-stu-id="dd661-125">No, Channel Integration Framework is operating system and web browser agnostic and lets you integrate the cloud-based channels of your choice that are best for organization requirements.</span></span>

## <a name="which-web-browsers-does-channel-integration-framework-support"></a><span data-ttu-id="dd661-126">Which web browsers does Channel Integration Framework support?</span><span class="sxs-lookup"><span data-stu-id="dd661-126">Which web browsers does Channel Integration Framework support?</span></span>
<span data-ttu-id="dd661-127">Channel Integration Framework is supported on Microsoft Edge and Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="dd661-127">Channel Integration Framework is supported on Microsoft Edge and Google Chrome.</span></span> 

> [!NOTE]
> <span data-ttu-id="dd661-128">The widget domain needs to be accorded permission to use appropriate media like pop-ups and microphone as required.</span><span class="sxs-lookup"><span data-stu-id="dd661-128">The widget domain needs to be accorded permission to use appropriate media like pop-ups and microphone as required.</span></span> <span data-ttu-id="dd661-129">For Edge to permanently accord the required permissions, the required domain needs to be accessed via a regular window; permanent exception cannot be granted when the domain is accessed in private mode.</span><span class="sxs-lookup"><span data-stu-id="dd661-129">For Edge to permanently accord the required permissions, the required domain needs to be accessed via a regular window; permanent exception cannot be granted when the domain is accessed in private mode.</span></span>

## <a name="are-there-any-browsers-that-channel-integration-framework-does-not-support"></a><span data-ttu-id="dd661-130">Are there any browsers that Channel Integration Framework does not support?</span><span class="sxs-lookup"><span data-stu-id="dd661-130">Are there any browsers that Channel Integration Framework does not support?</span></span>
<span data-ttu-id="dd661-131">Yes, Channel Integration Framework does not support Internet Explorer and Firefox browsers.</span><span class="sxs-lookup"><span data-stu-id="dd661-131">Yes, Channel Integration Framework does not support Internet Explorer and Firefox browsers.</span></span>

## <a name="can-partners-package-solutions-that-have-a-dependency-on-the-channel-integration-framework-cif-solution-together-with-the-cif-solution"></a><span data-ttu-id="dd661-132">Can partners package solutions that have a dependency on the Channel Integration Framework (CIF) solution, together with the CIF solution?</span><span class="sxs-lookup"><span data-stu-id="dd661-132">Can partners package solutions that have a dependency on the Channel Integration Framework (CIF) solution, together with the CIF solution?</span></span>
<span data-ttu-id="dd661-133">No, the Channel Integration Framework (CIF) solution should not be bundled with another solution.</span><span class="sxs-lookup"><span data-stu-id="dd661-133">No, the Channel Integration Framework (CIF) solution should not be bundled with another solution.</span></span> <span data-ttu-id="dd661-134">Partners can create solutions that add a check to their package looking for the Channel Integration Framework (CIF) solution (also mentioning the minimum supported version), which causes installation to fail in case the CIF solution is not present.</span><span class="sxs-lookup"><span data-stu-id="dd661-134">Partners can create solutions that add a check to their package looking for the Channel Integration Framework (CIF) solution (also mentioning the minimum supported version), which causes installation to fail in case the CIF solution is not present.</span></span>

<span data-ttu-id="dd661-135">Also, you can add Configuration Experience to the acquire flow that will allow the solution to detect the state of the target instance, and decide how to install.</span><span class="sxs-lookup"><span data-stu-id="dd661-135">Also, you can add Configuration Experience to the acquire flow that will allow the solution to detect the state of the target instance, and decide how to install.</span></span> <span data-ttu-id="dd661-136">This will also let the solution do any additional setup or license acquisition remotely before installing.</span><span class="sxs-lookup"><span data-stu-id="dd661-136">This will also let the solution do any additional setup or license acquisition remotely before installing.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd661-137">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="dd661-137">See also</span></span>

[<span data-ttu-id="dd661-138">Dynamics 365 Channel Integration Framework Guide</span><span class="sxs-lookup"><span data-stu-id="dd661-138">Dynamics 365 Channel Integration Framework Guide</span></span>](index.md)<br />
[<span data-ttu-id="dd661-139">Overview of Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="dd661-139">Overview of Channel Integration Framework</span></span>](overview-channel-integration-framework.md)<br />
[<span data-ttu-id="dd661-140">System requirements of Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="dd661-140">System requirements of Channel Integration Framework</span></span>](system-requirements-channel-integration-framework.md)

