---
title: Comply with the General Data Protection Regulation (GDPR) (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about General Data Protection Regulation (GDPR) and how Unified Service Desk complies with GDPR.
ms.custom: ''
ms.date: 04/24/2018
ms.reviewer: ''
ms.service: usd
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: FA8D5702-C698-42B0-89BF-CD444BF3FB73
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 31c148210ac12be6065bd79e364af744bca736d8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382512"
---
# <a name="comply-with-the-general-data-protection-regulation-gdpr"></a><span data-ttu-id="a7488-103">Comply with the General Data Protection Regulation (GDPR)</span><span class="sxs-lookup"><span data-stu-id="a7488-103">Comply with the General Data Protection Regulation (GDPR)</span></span>

## <a name="introduction"></a><span data-ttu-id="a7488-104">Giới thiệu</span><span class="sxs-lookup"><span data-stu-id="a7488-104">Introduction</span></span>
<span data-ttu-id="a7488-105">The General Data Protection Regulation (GDPR) imposes new rules on organizations in the European Union (EU) and those that offer goods and services to people in the EU, or those that collect and analyze data tied to EU residents, regardless of where they are located.</span><span class="sxs-lookup"><span data-stu-id="a7488-105">The General Data Protection Regulation (GDPR) imposes new rules on organizations in the European Union (EU) and those that offer goods and services to people in the EU, or those that collect and analyze data tied to EU residents, regardless of where they are located.</span></span>

<span data-ttu-id="a7488-106">Fundamentally, the GDPR is about protecting and enabling the privacy rights of individuals.</span><span class="sxs-lookup"><span data-stu-id="a7488-106">Fundamentally, the GDPR is about protecting and enabling the privacy rights of individuals.</span></span> <span data-ttu-id="a7488-107">The GDPR establishes strict privacy requirements that govern how you manage and protect personal data while respecting individual choice—regardless of where data is sent, processed, or stored.</span><span class="sxs-lookup"><span data-stu-id="a7488-107">The GDPR establishes strict privacy requirements that govern how you manage and protect personal data while respecting individual choice—regardless of where data is sent, processed, or stored.</span></span>

## <a name="shared-responsibility-model"></a><span data-ttu-id="a7488-108">Shared responsibility model</span><span class="sxs-lookup"><span data-stu-id="a7488-108">Shared responsibility model</span></span>
<span data-ttu-id="a7488-109">Your compliance with the GDPR is an ongoing process and involves your role as a **controller** and, in some cases, Microsoft as a **processor**.</span><span class="sxs-lookup"><span data-stu-id="a7488-109">Your compliance with the GDPR is an ongoing process and involves your role as a **controller** and, in some cases, Microsoft as a **processor**.</span></span> <span data-ttu-id="a7488-110">Depending on which [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps applications your organization uses, you may find that you are both controller and processor or that you have a shared responsibility with Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a7488-110">Depending on which [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps applications your organization uses, you may find that you are both controller and processor or that you have a shared responsibility with Microsoft.</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="a7488-111">client application runs on-premises, so you hold both the controller and processor roles:</span><span class="sxs-lookup"><span data-stu-id="a7488-111">client application runs on-premises, so you hold both the controller and processor roles:</span></span>

- <span data-ttu-id="a7488-112">**Controller.**</span><span class="sxs-lookup"><span data-stu-id="a7488-112">**Controller.**</span></span> <span data-ttu-id="a7488-113">The natural or legal person, public authority, agency, or other body which, alone or jointly with others, determines the purposes and means of the processing of personal data.</span><span class="sxs-lookup"><span data-stu-id="a7488-113">The natural or legal person, public authority, agency, or other body which, alone or jointly with others, determines the purposes and means of the processing of personal data.</span></span> <span data-ttu-id="a7488-114">Within the context of the GDPR, a controller doesn't have to be located within the EU for the GDPR to apply.</span><span class="sxs-lookup"><span data-stu-id="a7488-114">Within the context of the GDPR, a controller doesn't have to be located within the EU for the GDPR to apply.</span></span>

- <span data-ttu-id="a7488-115">**Processor.**</span><span class="sxs-lookup"><span data-stu-id="a7488-115">**Processor.**</span></span> <span data-ttu-id="a7488-116">The natural or legal person, public authority, agency, or other body which processes personal data on behalf of the controller.</span><span class="sxs-lookup"><span data-stu-id="a7488-116">The natural or legal person, public authority, agency, or other body which processes personal data on behalf of the controller.</span></span>

## <a name="data-definitions"></a><span data-ttu-id="a7488-117">Data definitions</span><span class="sxs-lookup"><span data-stu-id="a7488-117">Data definitions</span></span>

<span data-ttu-id="a7488-118">The GDPR considers personal data to be any information related to an identified or identifiable natural person.</span><span class="sxs-lookup"><span data-stu-id="a7488-118">The GDPR considers personal data to be any information related to an identified or identifiable natural person.</span></span> <span data-ttu-id="a7488-119">That can include both direct identification (such as your legal name) and indirect identification (such as specific information that makes it clear that it's you the data references).</span><span class="sxs-lookup"><span data-stu-id="a7488-119">That can include both direct identification (such as your legal name) and indirect identification (such as specific information that makes it clear that it's you the data references).</span></span>
<span data-ttu-id="a7488-120">The GDPR makes clear that the concept of personal data includes online identifiers (such as IP addresses and mobile device IDs) and location data.</span><span class="sxs-lookup"><span data-stu-id="a7488-120">The GDPR makes clear that the concept of personal data includes online identifiers (such as IP addresses and mobile device IDs) and location data.</span></span>

## <a name="stages-of-gdpr"></a><span data-ttu-id="a7488-121">Stages of GDPR</span><span class="sxs-lookup"><span data-stu-id="a7488-121">Stages of GDPR</span></span>

<span data-ttu-id="a7488-122">![Four stages of GDPR are Discover, Manage, Protect, and Report](../../unified-service-desk/media/gdpr-four-stages-image.PNG "Four stages of GDPR")</span><span class="sxs-lookup"><span data-stu-id="a7488-122">![Four stages of GDPR are Discover, Manage, Protect, and Report](../../unified-service-desk/media/gdpr-four-stages-image.PNG "Four stages of GDPR")</span></span>

|<span data-ttu-id="a7488-123">Stages of GDPR</span><span class="sxs-lookup"><span data-stu-id="a7488-123">Stages of GDPR</span></span>| <span data-ttu-id="a7488-124">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a7488-124">Description</span></span>|
|------|------|
|<span data-ttu-id="a7488-125">Discover</span><span class="sxs-lookup"><span data-stu-id="a7488-125">Discover</span></span>|<span data-ttu-id="a7488-126">Identify what data under your control is subject to the GDPR.</span><span class="sxs-lookup"><span data-stu-id="a7488-126">Identify what data under your control is subject to the GDPR.</span></span> <span data-ttu-id="a7488-127">This analysis includes understanding what data you have and where it exists.</span><span class="sxs-lookup"><span data-stu-id="a7488-127">This analysis includes understanding what data you have and where it exists.</span></span>|
|<span data-ttu-id="a7488-128">Quản lý</span><span class="sxs-lookup"><span data-stu-id="a7488-128">Manage</span></span>|<span data-ttu-id="a7488-129">The GDPR provides more control over your data.</span><span class="sxs-lookup"><span data-stu-id="a7488-129">The GDPR provides more control over your data.</span></span> <span data-ttu-id="a7488-130">GDPR lets you to manage access and control how data is used and accessed.</span><span class="sxs-lookup"><span data-stu-id="a7488-130">GDPR lets you to manage access and control how data is used and accessed.</span></span>|
|<span data-ttu-id="a7488-131">Protect</span><span class="sxs-lookup"><span data-stu-id="a7488-131">Protect</span></span>|<span data-ttu-id="a7488-132">The GDPR require you to establish security controls to prevent, detect, and respond to the vulnerabilities and data breaches.</span><span class="sxs-lookup"><span data-stu-id="a7488-132">The GDPR require you to establish security controls to prevent, detect, and respond to the vulnerabilities and data breaches.</span></span>|
|<span data-ttu-id="a7488-133">Báo cáo</span><span class="sxs-lookup"><span data-stu-id="a7488-133">Report</span></span>|<span data-ttu-id="a7488-134">The GDPR sets new standards in transparency, accountability, execution, data requests, and report data breaches.</span><span class="sxs-lookup"><span data-stu-id="a7488-134">The GDPR sets new standards in transparency, accountability, execution, data requests, and report data breaches.</span></span>|

## <a name="see-also"></a><span data-ttu-id="a7488-135">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a7488-135">See also</span></span>

[<span data-ttu-id="a7488-136">Unified Service Desk data compliance under GDPR</span><span class="sxs-lookup"><span data-stu-id="a7488-136">Unified Service Desk data compliance under GDPR</span></span>](comply-unified-service-desk-data-gdpr.md)
