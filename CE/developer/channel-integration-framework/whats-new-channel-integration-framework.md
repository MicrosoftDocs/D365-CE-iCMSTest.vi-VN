---
title: What's new in Channel Integration Framework (CIF)| Microsoft Docs
description: Read about the new features provided in the latest release of Channel Integration Framework (CIF).
keywords: ''
ms.date: 12/10/2018
ms.service:
- dynamics-365-cross-app
ms.custom:
- dyn365-a11y
- dyn365-developer
ms.topic: get-started-article
applies_to:
- Dynamics 365 (online)
- Dynamics 365 Version 9.x
ms.assetid: 42BEC0F2-AAA7-44A1-9BD7-EA2A04F5ACDB
author: susikka
ms.author: susikka
manager: shujoshi
ms.openlocfilehash: 5c798b956accad674baa687453cc160b44ce0e82
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387862"
---
# <a name="whats-new-in-channel-integration-framework-cif"></a><span data-ttu-id="31de2-103">What's new in Channel Integration Framework (CIF)</span><span class="sxs-lookup"><span data-stu-id="31de2-103">What's new in Channel Integration Framework (CIF)</span></span>

<span data-ttu-id="31de2-104">The topic provides the list of new features introduced for Dynamics 365 Channel Integration Framework (CIF) version 1.0.</span><span class="sxs-lookup"><span data-stu-id="31de2-104">The topic provides the list of new features introduced for Dynamics 365 Channel Integration Framework (CIF) version 1.0.</span></span>

## <a name="javascript-channel-integration-framework-apis"></a><span data-ttu-id="31de2-105">JavaScript Channel Integration Framework APIs</span><span class="sxs-lookup"><span data-stu-id="31de2-105">JavaScript Channel Integration Framework APIs</span></span>

| <span data-ttu-id="31de2-106">JavaScript API</span><span class="sxs-lookup"><span data-stu-id="31de2-106">JavaScript API</span></span> | <span data-ttu-id="31de2-107">Mô tả</span><span class="sxs-lookup"><span data-stu-id="31de2-107">Description</span></span> |
|-----|-----|
| [<span data-ttu-id="31de2-108">Microsoft.CIFramework.getEntityMetadata</span><span class="sxs-lookup"><span data-stu-id="31de2-108">Microsoft.CIFramework.getEntityMetadata</span></span>](reference/microsoft-ciframework/getEntityMetadata.md) | [!INCLUDE[getEntityMetadata-description](reference/microsoft-ciframework/includes/getEntityMetadata-description.md)] |
| [<span data-ttu-id="31de2-109">Microsoft.CIFramework.renderSearchPage</span><span class="sxs-lookup"><span data-stu-id="31de2-109">Microsoft.CIFramework.renderSearchPage</span></span>](reference/microsoft-ciframework/renderSearchPage.md) | [!INCLUDE[renderSearchPage-description](reference/microsoft-ciframework/includes/renderSearchPage-description.md)] |

## <a name="ability-to-pass-dynamics-365-url-to-widget-library"></a><span data-ttu-id="31de2-110">Ability to pass Dynamics 365 URL to widget library</span><span class="sxs-lookup"><span data-stu-id="31de2-110">Ability to pass Dynamics 365 URL to widget library</span></span>

<span data-ttu-id="31de2-111">To access the Dynamics 365 Channel Integration Framework (CIF) APIs, you need to load the `msdyn_cilibrary.js` file inside your communication widget.</span><span class="sxs-lookup"><span data-stu-id="31de2-111">To access the Dynamics 365 Channel Integration Framework (CIF) APIs, you need to load the `msdyn_cilibrary.js` file inside your communication widget.</span></span> <span data-ttu-id="31de2-112">Since the widget is in a different domain, the JavaScript API library needs to identify the Dynamics 365 domain to interact.</span><span class="sxs-lookup"><span data-stu-id="31de2-112">Since the widget is in a different domain, the JavaScript API library needs to identify the Dynamics 365 domain to interact.</span></span> <span data-ttu-id="31de2-113">To enable the communication between the different domains, you must pass your Dynamics 365 instance URL to the widget library.</span><span class="sxs-lookup"><span data-stu-id="31de2-113">To enable the communication between the different domains, you must pass your Dynamics 365 instance URL to the widget library.</span></span>

<span data-ttu-id="31de2-114">There are two ways to pass the URL to widget library:</span><span class="sxs-lookup"><span data-stu-id="31de2-114">There are two ways to pass the URL to widget library:</span></span>
1. <span data-ttu-id="31de2-115">By adding attributes to a script tag</span><span class="sxs-lookup"><span data-stu-id="31de2-115">By adding attributes to a script tag</span></span>
2. <span data-ttu-id="31de2-116">By adding a parameter `ucilib` in the URL</span><span class="sxs-lookup"><span data-stu-id="31de2-116">By adding a parameter `ucilib` in the URL</span></span>

<span data-ttu-id="31de2-117">More information: [Pass a Dynamics 365 URL to a widget library](pass-url-widget-library.md)</span><span class="sxs-lookup"><span data-stu-id="31de2-117">More information: [Pass a Dynamics 365 URL to a widget library](pass-url-widget-library.md)</span></span>

## <a name="ability-to-add-another-trusted-domain"></a><span data-ttu-id="31de2-118">Ability to add another trusted domain</span><span class="sxs-lookup"><span data-stu-id="31de2-118">Ability to add another trusted domain</span></span>

<span data-ttu-id="31de2-119">Channel Integration Framework allows you to add an additional trusted domain if the initial landing URL and the final domain from which the communication widget is hosted are different.</span><span class="sxs-lookup"><span data-stu-id="31de2-119">Channel Integration Framework allows you to add an additional trusted domain if the initial landing URL and the final domain from which the communication widget is hosted are different.</span></span> <span data-ttu-id="31de2-120">More information: [Configure channel provider in Channel Integration Framework](configure-channel-provider-channel-integration-framework.md).</span><span class="sxs-lookup"><span data-stu-id="31de2-120">More information: [Configure channel provider in Channel Integration Framework](configure-channel-provider-channel-integration-framework.md).</span></span>

## <a name="custom-parameters-field-in-the-channel-provider-configuration"></a><span data-ttu-id="31de2-121">Custom Parameters field in the Channel provider configuration</span><span class="sxs-lookup"><span data-stu-id="31de2-121">Custom Parameters field in the Channel provider configuration</span></span>

<span data-ttu-id="31de2-122">Custom Parameters field takes a text blob as input and [Microsoft.CIFramework.getEnvironment](reference/microsoft-ciframework/getEnvironment.md) returns this as a value of key `customParams`.</span><span class="sxs-lookup"><span data-stu-id="31de2-122">Custom Parameters field takes a text blob as input and [Microsoft.CIFramework.getEnvironment](reference/microsoft-ciframework/getEnvironment.md) returns this as a value of key `customParams`.</span></span> 

<span data-ttu-id="31de2-123">More information: [Configure channel provider in Channel Integration Framework](configure-channel-provider-channel-integration-framework.md).</span><span class="sxs-lookup"><span data-stu-id="31de2-123">More information: [Configure channel provider in Channel Integration Framework](configure-channel-provider-channel-integration-framework.md).</span></span>


## <a name="download-dynamics-365-channel-integration-framework"></a><span data-ttu-id="31de2-124">Download Dynamics 365 Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="31de2-124">Download Dynamics 365 Channel Integration Framework</span></span>

<span data-ttu-id="31de2-125">Download link for Channel Integration Framework solution: [Channel Integration Framework](https://go.microsoft.com/fwlink/p/?linkid=2050102).</span><span class="sxs-lookup"><span data-stu-id="31de2-125">Download link for Channel Integration Framework solution: [Channel Integration Framework](https://go.microsoft.com/fwlink/p/?linkid=2050102).</span></span>

## <a name="see-also"></a><span data-ttu-id="31de2-126">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="31de2-126">See also</span></span>

[<span data-ttu-id="31de2-127">Dynamics 365 Channel Integration Framework Guide</span><span class="sxs-lookup"><span data-stu-id="31de2-127">Dynamics 365 Channel Integration Framework Guide</span></span>](index.md)

[<span data-ttu-id="31de2-128">Download Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="31de2-128">Download Channel Integration Framework</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2050102)
