---
title: Grid OnSave Event (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 1267b8cb1b9f0ea08429728a4a8b240671b77d65
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385469"
---
# <a name="grid-onsave-event-client-api-reference"></a><span data-ttu-id="e7732-102">Grid OnSave Event (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e7732-102">Grid OnSave Event (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e7732-103">The `OnSave` event occurs before sending the updated information to the server, and when any of the following occurs:</span><span class="sxs-lookup"><span data-stu-id="e7732-103">The `OnSave` event occurs before sending the updated information to the server, and when any of the following occurs:</span></span> 
- <span data-ttu-id="e7732-104">There is a change in the record selection.</span><span class="sxs-lookup"><span data-stu-id="e7732-104">There is a change in the record selection.</span></span>
- <span data-ttu-id="e7732-105">The user explicitly triggers a save operation using the editable grid’s save button.</span><span class="sxs-lookup"><span data-stu-id="e7732-105">The user explicitly triggers a save operation using the editable grid’s save button.</span></span>
- <span data-ttu-id="e7732-106">The user applies a sort, filter, group, pagination, or navigation operation from the editable grid while there are pending changes.</span><span class="sxs-lookup"><span data-stu-id="e7732-106">The user applies a sort, filter, group, pagination, or navigation operation from the editable grid while there are pending changes.</span></span>

<span data-ttu-id="e7732-107">Some important points to consider for the `OnSave` event:</span><span class="sxs-lookup"><span data-stu-id="e7732-107">Some important points to consider for the `OnSave` event:</span></span> 
- <span data-ttu-id="e7732-108">If a user edits multiple columns of the same record in sequence, the OnSave event will only be fired once to ensure optimal performance and form behavior compatibility.</span><span class="sxs-lookup"><span data-stu-id="e7732-108">If a user edits multiple columns of the same record in sequence, the OnSave event will only be fired once to ensure optimal performance and form behavior compatibility.</span></span>
- <span data-ttu-id="e7732-109">Editable grid and the parent form have separate save buttons.</span><span class="sxs-lookup"><span data-stu-id="e7732-109">Editable grid and the parent form have separate save buttons.</span></span> <span data-ttu-id="e7732-110">Clicking the save button in one will not save changes in the other.</span><span class="sxs-lookup"><span data-stu-id="e7732-110">Clicking the save button in one will not save changes in the other.</span></span>
- <span data-ttu-id="e7732-111">Editable grid does not save pending changes when navigation operations are performed outside of its context.</span><span class="sxs-lookup"><span data-stu-id="e7732-111">Editable grid does not save pending changes when navigation operations are performed outside of its context.</span></span> <span data-ttu-id="e7732-112">If the control has unsaved data, that data may be lost.</span><span class="sxs-lookup"><span data-stu-id="e7732-112">If the control has unsaved data, that data may be lost.</span></span> <span data-ttu-id="e7732-113">Consequently, the `OnSave` event may not fire.</span><span class="sxs-lookup"><span data-stu-id="e7732-113">Consequently, the `OnSave` event may not fire.</span></span> <span data-ttu-id="e7732-114">For example, this could happen when navigating to a different record using a form lookup field or through the ribbon.</span><span class="sxs-lookup"><span data-stu-id="e7732-114">For example, this could happen when navigating to a different record using a form lookup field or through the ribbon.</span></span>
- <span data-ttu-id="e7732-115">Pressing the refresh button in the editable grid causes it to discard any pending changes, and the `OnSave` event won't be fired.</span><span class="sxs-lookup"><span data-stu-id="e7732-115">Pressing the refresh button in the editable grid causes it to discard any pending changes, and the `OnSave` event won't be fired.</span></span>
- <span data-ttu-id="e7732-116">Editable grid control does not implement an auto-save timer.</span><span class="sxs-lookup"><span data-stu-id="e7732-116">Editable grid control does not implement an auto-save timer.</span></span>
<span data-ttu-id="e7732-117">Editable grid suppresses duplicate detection rules.</span><span class="sxs-lookup"><span data-stu-id="e7732-117">Editable grid suppresses duplicate detection rules.</span></span>

### <a name="related-topic"></a><span data-ttu-id="e7732-118">Related topic</span><span class="sxs-lookup"><span data-stu-id="e7732-118">Related topic</span></span>
[<span data-ttu-id="e7732-119">Form OnSave Event</span><span class="sxs-lookup"><span data-stu-id="e7732-119">Form OnSave Event</span></span>](form-onsave.md)



