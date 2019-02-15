---
title: Form OnSave Event (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b35c2c8cc8bd7d893b1262b065a83e2b69153e57
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388813"
---
# <a name="form-onsave-event-client-api-reference-in-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="006af-102">Form OnSave Event (Client API reference) in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="006af-102">Form OnSave Event (Client API reference) in Dynamics 365 for Customer Engagement apps</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="006af-103">The `OnSave` event occurs when:</span><span class="sxs-lookup"><span data-stu-id="006af-103">The `OnSave` event occurs when:</span></span>
- <span data-ttu-id="006af-104">The user clicks the **Save** icon in the lower right corner of the form, even when there is no changed data to be saved.</span><span class="sxs-lookup"><span data-stu-id="006af-104">The user clicks the **Save** icon in the lower right corner of the form, even when there is no changed data to be saved.</span></span>
- <span data-ttu-id="006af-105">Code executes the [formContext.data.entity.save](../formContext-data-entity/save.md) method, even when there is no changed data to be saved.</span><span class="sxs-lookup"><span data-stu-id="006af-105">Code executes the [formContext.data.entity.save](../formContext-data-entity/save.md) method, even when there is no changed data to be saved.</span></span>
- <span data-ttu-id="006af-106">The user navigates away from the form and there is unsaved data in the form.</span><span class="sxs-lookup"><span data-stu-id="006af-106">The user navigates away from the form and there is unsaved data in the form.</span></span>
- <span data-ttu-id="006af-107">The auto-save option is enabled, 30 seconds after data has changed and there is unsaved data in the form.</span><span class="sxs-lookup"><span data-stu-id="006af-107">The auto-save option is enabled, 30 seconds after data has changed and there is unsaved data in the form.</span></span>
- <span data-ttu-id="006af-108">Code executes the [formContext.data.save](../formContext-data/save.md) method and there is unsaved data in the form.</span><span class="sxs-lookup"><span data-stu-id="006af-108">Code executes the [formContext.data.save](../formContext-data/save.md) method and there is unsaved data in the form.</span></span>
- <span data-ttu-id="006af-109">Code executes the [formContext.data.refresh](../formContext-data/refresh.md) method passing a true value as the first parameter and there is unsaved data in the form.</span><span class="sxs-lookup"><span data-stu-id="006af-109">Code executes the [formContext.data.refresh](../formContext-data/refresh.md) method passing a true value as the first parameter and there is unsaved data in the form.</span></span>

<span data-ttu-id="006af-110">To determine which button was clicked to perform the save, use the getSaveMode method.</span><span class="sxs-lookup"><span data-stu-id="006af-110">To determine which button was clicked to perform the save, use the getSaveMode method.</span></span>

<span data-ttu-id="006af-111">You can cancel the save action by using the preventDefault method within the event arguments object.</span><span class="sxs-lookup"><span data-stu-id="006af-111">You can cancel the save action by using the preventDefault method within the event arguments object.</span></span> <span data-ttu-id="006af-112">The preventDefault method which is accessible by using the getEventArgs method that is part of the execution context.</span><span class="sxs-lookup"><span data-stu-id="006af-112">The preventDefault method which is accessible by using the getEventArgs method that is part of the execution context.</span></span> <span data-ttu-id="006af-113">Execution context is automatically passed to the form event handler.</span><span class="sxs-lookup"><span data-stu-id="006af-113">Execution context is automatically passed to the form event handler.</span></span>

### <a name="related-topic"></a><span data-ttu-id="006af-114">Related topic</span><span class="sxs-lookup"><span data-stu-id="006af-114">Related topic</span></span>
[<span data-ttu-id="006af-115">Grid OnSave Event</span><span class="sxs-lookup"><span data-stu-id="006af-115">Grid OnSave Event</span></span>](grid-onsave.md)  