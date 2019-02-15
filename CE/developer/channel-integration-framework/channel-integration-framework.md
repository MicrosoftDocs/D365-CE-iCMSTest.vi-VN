---
title: Dynamics 365 Channel Integration Framework (CIF) Guide | Microsoft Docs
description: Channel Integration Framework (CIF) for Microsoft Dynamics 365 is a cloud-to-cloud extensible framework to integrate third-party Computer Telephony Integration (CTI) systems with Dynamics 365 Unified Interface Apps using a browser-based JavaScript API library.
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
ms.assetid: 7923e36d-3640-49f7-9f2f-c97358a632db
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: 50ddd8c2235a23b6b411bf2c55e88d0c1d7a0fca
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387279"
---
# <a name="dynamics-365-channel-integration-framework-guide"></a><span data-ttu-id="24c71-103">Dynamics 365 Channel Integration Framework Guide</span><span class="sxs-lookup"><span data-stu-id="24c71-103">Dynamics 365 Channel Integration Framework Guide</span></span>

<table>
<tr>
<td>

<h2> <span data-ttu-id="24c71-104">Bắt đầu</span><span class="sxs-lookup"><span data-stu-id="24c71-104">Get started</span></span> </h2>
<li><span data-ttu-id="24c71-105"><a href="overview-channel-integration-framework.md" data-raw-source="[Channel Integration Framework overview](overview-channel-integration-framework.md)">Channel Integration Framework overview</a></span><span class="sxs-lookup"><span data-stu-id="24c71-105"><a href="overview-channel-integration-framework.md" data-raw-source="[Channel Integration Framework overview](overview-channel-integration-framework.md)">Channel Integration Framework overview</a></span></span></li>
<li><span data-ttu-id="24c71-106"><a href="architecture-overview-channel-integration-framework.md" data-raw-source="[Architecture overview of Channel Integration Framework (CIF)](architecture-overview-channel-integration-framework.md)">Architecture overview of Channel Integration Framework (CIF)</a></span><span class="sxs-lookup"><span data-stu-id="24c71-106"><a href="architecture-overview-channel-integration-framework.md" data-raw-source="[Architecture overview of Channel Integration Framework (CIF)](architecture-overview-channel-integration-framework.md)">Architecture overview of Channel Integration Framework (CIF)</a></span></span></li>
<li><span data-ttu-id="24c71-107"><a href="system-requirements-channel-integration-framework.md" data-raw-source="[System requirements of Channel Integration Framework](system-requirements-channel-integration-framework.md)">System requirements of Channel Integration Framework</a></span><span class="sxs-lookup"><span data-stu-id="24c71-107"><a href="system-requirements-channel-integration-framework.md" data-raw-source="[System requirements of Channel Integration Framework](system-requirements-channel-integration-framework.md)">System requirements of Channel Integration Framework</a></span></span></li>
</td>
<td>

<h2> <span data-ttu-id="24c71-108">Download</span><span class="sxs-lookup"><span data-stu-id="24c71-108">Download</span></span> </h2>

<li><span data-ttu-id="24c71-109"><a href="get-channel-integration-framework.md" data-raw-source="[Get Channel Integration Framework (CIF)](get-channel-integration-framework.md)">Get Channel Integration Framework (CIF)</a></span><span class="sxs-lookup"><span data-stu-id="24c71-109"><a href="get-channel-integration-framework.md" data-raw-source="[Get Channel Integration Framework (CIF)](get-channel-integration-framework.md)">Get Channel Integration Framework (CIF)</a></span></span></li>
<li><span data-ttu-id="24c71-110"><a href="sample-softphone-integration.md" data-raw-source="[Download sample code for softphone integration](sample-softphone-integration.md)">Download sample code for softphone integration</a></span><span class="sxs-lookup"><span data-stu-id="24c71-110"><a href="sample-softphone-integration.md" data-raw-source="[Download sample code for softphone integration](sample-softphone-integration.md)">Download sample code for softphone integration</a></span></span></li>
</td>
</tr>
<tr>
<td>

<h2> <span data-ttu-id="24c71-111">How-to</span><span class="sxs-lookup"><span data-stu-id="24c71-111">How-to</span></span> </h2>

<li><span data-ttu-id="24c71-112"><a href="configure-channel-provider-channel-integration-framework.md" data-raw-source="[How to configure a channel provider ifor your organization](configure-channel-provide-channel-integration-framework.md)">How to configure a channel provider for your organization</a></span><span class="sxs-lookup"><span data-stu-id="24c71-112"><a href="configure-channel-provider-channel-integration-framework.md" data-raw-source="[How to configure a channel provider ifor your organization](configure-channel-provide-channel-integration-framework.md)">How to configure a channel provider for your organization</a></span></span></li>
<li><span data-ttu-id="24c71-113"><a href="enable-outbound-communication-clicktoact.md" data-raw-source="[How to enable outbound communication (ClickTOAct)](enable-outbound-communication-clicktoact.md)">How to enable outbound communication (ClickTOAct)</a></span><span class="sxs-lookup"><span data-stu-id="24c71-113"><a href="enable-outbound-communication-clicktoact.md" data-raw-source="[How to enable outbound communication (ClickTOAct)](enable-outbound-communication-clicktoact.md)">How to enable outbound communication (ClickTOAct)</a></span></span></li>
<li><span data-ttu-id="24c71-114"><a href="add-cif-solution-dependent-solution.md" data-raw-source="[Add CIF solution as a dependent solution](add-cif-solution-dependent-solution.md)">Add CIF solution as a dependent solution</a></span><span class="sxs-lookup"><span data-stu-id="24c71-114"><a href="add-cif-solution-dependent-solution.md" data-raw-source="[Add CIF solution as a dependent solution](add-cif-solution-dependent-solution.md)">Add CIF solution as a dependent solution</a></span></span></li>
<li><span data-ttu-id="24c71-115"><a href="authenticate-channel-users.md" data-raw-source="[Authenticate channel users to the channel (widget)](authenticate-channel-users.md)">Authenticate channel users to the channel (widget)</a></span><span class="sxs-lookup"><span data-stu-id="24c71-115"><a href="authenticate-channel-users.md" data-raw-source="[Authenticate channel users to the channel (widget)](authenticate-channel-users.md)">Authenticate channel users to the channel (widget)</a></span></span></li>
<li><span data-ttu-id="24c71-116"><a href="pass-url-widget-library.md" data-raw-source="[Pass Dynamics 365 URL to widget library](pass-url-widget-library.md)">Pass Dynamics 365 URL to widget library</a></span><span class="sxs-lookup"><span data-stu-id="24c71-116"><a href="pass-url-widget-library.md" data-raw-source="[Pass Dynamics 365 URL to widget library](pass-url-widget-library.md)">Pass Dynamics 365 URL to widget library</a></span></span></li>
</td>
<td>

<h2> <span data-ttu-id="24c71-117">JavaScript reference</span><span class="sxs-lookup"><span data-stu-id="24c71-117">JavaScript reference</span></span> </h2>

<li><span data-ttu-id="24c71-118"><a href="reference/microsoft-ciframework.md" data-raw-source="[Microsoft.CIFramework
 methods](reference/microsoft-ciframework.md)">Microsoft.CIFramework</a></span><span class="sxs-lookup"><span data-stu-id="24c71-118"><a href="reference/microsoft-ciframework.md" data-raw-source="[Microsoft.CIFramework
 methods](reference/microsoft-ciframework.md)">Microsoft.CIFramework</a></span></span></li>
<li><span data-ttu-id="24c71-119"><a href="reference/client-side-events.md" data-raw-source="[Client-side events](reference/client-side-events.md)">Client-side events</a>
</span><span class="sxs-lookup"><span data-stu-id="24c71-119"><a href="reference/client-side-events.md" data-raw-source="[Client-side events](reference/client-side-events.md)">Client-side events</a>
</span></span><li><span data-ttu-id="24c71-120"><a href="reference/entities-attributes/msdyn-ciprovider.md" data-raw-source="[Entity reference](reference/entities-attributes/msdyn-ciprovider.md)">Tham chiếu thực thể</a>

</td>
</tr>
</span><span class="sxs-lookup"><span data-stu-id="24c71-120"><a href="reference/entities-attributes/msdyn-ciprovider.md" data-raw-source="[Entity reference](reference/entities-attributes/msdyn-ciprovider.md)">Entity reference</a>

</td>
</tr>
</span></span><tr>
<td>

<h2> <span data-ttu-id="24c71-121">CÂU HỎI THƯỜNG GẶP</span><span class="sxs-lookup"><span data-stu-id="24c71-121">FAQ</span></span> </h2>

<li><span data-ttu-id="24c71-122"><a href="faq-channel-integration-framework.md" data-raw-source="[Frequently Asked Questions](faq-channel-integration-framework.md)">Câu hỏi Thường Gặp</a></span><span class="sxs-lookup"><span data-stu-id="24c71-122"><a href="faq-channel-integration-framework.md" data-raw-source="[Frequently Asked Questions](faq-channel-integration-framework.md)">Frequently Asked Questions</a></span></span></li>

</td>
</tr>
</table>