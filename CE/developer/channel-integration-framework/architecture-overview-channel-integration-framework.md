---
title: Architecture overview of Channel Integration Framework (CIF) helps| Microsoft Docs
description: Learn the architecture overview of Channel Integration Framework (CIF) for Microsoft Dynamics 365.
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
ms.assetid: 937bd2df-0b5c-48c8-b415-285820b246c9
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: e21b77e031c77fe03a780776583c1b5a27f4ee54
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387187"
---
# <a name="architecture-overview-of-dynamics-365-channel-integration-framework"></a><span data-ttu-id="4e400-103">Architecture overview of Dynamics 365 Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="4e400-103">Architecture overview of Dynamics 365 Channel Integration Framework</span></span> 

<span data-ttu-id="4e400-104">Dynamics 365 Channel Integration Framework provides an extensible framework to integrate third-party Computer Telephony Integration (CTI) systems to serve your customers with more focus and agility.</span><span class="sxs-lookup"><span data-stu-id="4e400-104">Dynamics 365 Channel Integration Framework provides an extensible framework to integrate third-party Computer Telephony Integration (CTI) systems to serve your customers with more focus and agility.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="4e400-105">![High level architecture diagram of the channel integration framework](media/cif-high-level-architecture.PNG "High level architecture diagram of the channel integration framework")</span><span class="sxs-lookup"><span data-stu-id="4e400-105">![High level architecture diagram of the channel integration framework](media/cif-high-level-architecture.PNG "High level architecture diagram of the channel integration framework")</span></span>

<span data-ttu-id="4e400-106">**1 - Microsoft Dynamics 365**</span><span class="sxs-lookup"><span data-stu-id="4e400-106">**1 - Microsoft Dynamics 365**</span></span><br>
<span data-ttu-id="4e400-107">Dynamics 365 instance where you have the Channel Integration Framework app is present to create and manage the certain configurations required for third-party communication widget to interact with Unified Interface app.</span><span class="sxs-lookup"><span data-stu-id="4e400-107">Dynamics 365 instance where you have the Channel Integration Framework app is present to create and manage the certain configurations required for third-party communication widget to interact with Unified Interface app.</span></span>

<span data-ttu-id="4e400-108">**2 - Unified Interface App**</span><span class="sxs-lookup"><span data-stu-id="4e400-108">**2 - Unified Interface App**</span></span><br>
<span data-ttu-id="4e400-109">The Dynamics 365 (Online) Unified Interface app exposes the Channel integration Framework panel to host the third-party communication widget (channel provider).</span><span class="sxs-lookup"><span data-stu-id="4e400-109">The Dynamics 365 (Online) Unified Interface app exposes the Channel integration Framework panel to host the third-party communication widget (channel provider).</span></span>

<span data-ttu-id="4e400-110">**3 - Channel Integration Framework Adapter**</span><span class="sxs-lookup"><span data-stu-id="4e400-110">**3 - Channel Integration Framework Adapter**</span></span><br>
<span data-ttu-id="4e400-111">The Channel Integration Framework Adapter enables the communication between the Dynamics 365 and the capabilities of the channel provider.</span><span class="sxs-lookup"><span data-stu-id="4e400-111">The Channel Integration Framework Adapter enables the communication between the Dynamics 365 and the capabilities of the channel provider.</span></span>

<span data-ttu-id="4e400-112">**4 - Web-based communication widget**</span><span class="sxs-lookup"><span data-stu-id="4e400-112">**4 - Web-based communication widget**</span></span><br>
<span data-ttu-id="4e400-113">The web-based communication channel (third-party) is hosted in the widget that Channel Integration Framework provides.</span><span class="sxs-lookup"><span data-stu-id="4e400-113">The web-based communication channel (third-party) is hosted in the widget that Channel Integration Framework provides.</span></span> <span data-ttu-id="4e400-114">This is a multi-purpose communication widget wherein you can host a CTI, chat, or email channels of your choice.</span><span class="sxs-lookup"><span data-stu-id="4e400-114">This is a multi-purpose communication widget wherein you can host a CTI, chat, or email channels of your choice.</span></span>

<span data-ttu-id="4e400-115">**5 - Cloud Channel Provider**</span><span class="sxs-lookup"><span data-stu-id="4e400-115">**5 - Cloud Channel Provider**</span></span><br>
<span data-ttu-id="4e400-116">The Cloud Channel Provider is the service that you want to integrate and interact with Dynamics 365 using the Channel Integration Framework.</span><span class="sxs-lookup"><span data-stu-id="4e400-116">The Cloud Channel Provider is the service that you want to integrate and interact with Dynamics 365 using the Channel Integration Framework.</span></span> <span data-ttu-id="4e400-117">The capabilities of a channel are voice, SMS, chat, email and so on.</span><span class="sxs-lookup"><span data-stu-id="4e400-117">The capabilities of a channel are voice, SMS, chat, email and so on.</span></span> <span data-ttu-id="4e400-118">These capabilities of a channel are specific to the channel provider and Channel Integration Framework is agnostic on the working of the channel.</span><span class="sxs-lookup"><span data-stu-id="4e400-118">These capabilities of a channel are specific to the channel provider and Channel Integration Framework is agnostic on the working of the channel.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="4e400-119">System requirements of Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="4e400-119">System requirements of Channel Integration Framework</span></span>](system-requirements-channel-integration-framework.md)


## <a name="see-also"></a><span data-ttu-id="4e400-120">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4e400-120">See also</span></span>

[<span data-ttu-id="4e400-121">Overview of Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="4e400-121">Overview of Channel Integration Framework</span></span>](overview-channel-integration-framework.md)
