---
title: Attribute OnChange Event in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: bc70916a06ee5ae79a5b5e7ac914857138af89fc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386630"
---
# <a name="attribute-onchange-event-client-api-reference"></a><span data-ttu-id="2b369-102">Attribute OnChange Event (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="2b369-102">Attribute OnChange Event (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2b369-103">The `OnChange` event occurs in the following situations:</span><span class="sxs-lookup"><span data-stu-id="2b369-103">The `OnChange` event occurs in the following situations:</span></span>
- <span data-ttu-id="2b369-104">Data in a form field has changed and focus is lost.</span><span class="sxs-lookup"><span data-stu-id="2b369-104">Data in a form field has changed and focus is lost.</span></span> <span data-ttu-id="2b369-105">There is an exception to this behavior that applies to Two-Option (Boolean) fields that are formatted to use radio buttons or check boxes.</span><span class="sxs-lookup"><span data-stu-id="2b369-105">There is an exception to this behavior that applies to Two-Option (Boolean) fields that are formatted to use radio buttons or check boxes.</span></span> <span data-ttu-id="2b369-106">In these cases the event occurs immediately.</span><span class="sxs-lookup"><span data-stu-id="2b369-106">In these cases the event occurs immediately.</span></span>
- <span data-ttu-id="2b369-107">Data changes on the server are retrieved to update a field when the form is refreshed, such as after a record is saved.</span><span class="sxs-lookup"><span data-stu-id="2b369-107">Data changes on the server are retrieved to update a field when the form is refreshed, such as after a record is saved.</span></span>
- <span data-ttu-id="2b369-108">The attribute.[fireOnchange](../attributes/fireOnChange.md) method is used.</span><span class="sxs-lookup"><span data-stu-id="2b369-108">The attribute.[fireOnchange](../attributes/fireOnChange.md) method is used.</span></span>

<span data-ttu-id="2b369-109">All fields support the `OnChange` event.</span><span class="sxs-lookup"><span data-stu-id="2b369-109">All fields support the `OnChange` event.</span></span> <span data-ttu-id="2b369-110">Data in the field is validated before and after the `OnChange` event.</span><span class="sxs-lookup"><span data-stu-id="2b369-110">Data in the field is validated before and after the `OnChange` event.</span></span>

<span data-ttu-id="2b369-111">The `OnChange` event does not occur if the field is changed programmatically using the attribute.[setValue](../attributes/setValue.md) method.</span><span class="sxs-lookup"><span data-stu-id="2b369-111">The `OnChange` event does not occur if the field is changed programmatically using the attribute.[setValue](../attributes/setValue.md) method.</span></span> <span data-ttu-id="2b369-112">If you want event handlers for the `OnChange` event to run after you set the value you must use the `formContext.data.entity attribute.`[fireOnchange](../attributes/fireOnChange.md) method in your code.</span><span class="sxs-lookup"><span data-stu-id="2b369-112">If you want event handlers for the `OnChange` event to run after you set the value you must use the `formContext.data.entity attribute.`[fireOnchange](../attributes/fireOnChange.md) method in your code.</span></span> 

> [!NOTE]
> <span data-ttu-id="2b369-113">Although the **Status** field supports the`OnChange` event, the field is read-only on the form so the event cannot occur through user interaction.</span><span class="sxs-lookup"><span data-stu-id="2b369-113">Although the **Status** field supports the`OnChange` event, the field is read-only on the form so the event cannot occur through user interaction.</span></span> <span data-ttu-id="2b369-114">Another script could cause this event to occur by using the [fireOnchange](../attributes/fireOnChange.md) method on the field.</span><span class="sxs-lookup"><span data-stu-id="2b369-114">Another script could cause this event to occur by using the [fireOnchange](../attributes/fireOnChange.md) method on the field.</span></span>

## <a name="methods-supported-for-this-event"></a><span data-ttu-id="2b369-115">Methods supported for this event</span><span class="sxs-lookup"><span data-stu-id="2b369-115">Methods supported for this event</span></span>
<span data-ttu-id="2b369-116">There are three methods you can use to work with the `OnChange` event for an attribute:</span><span class="sxs-lookup"><span data-stu-id="2b369-116">There are three methods you can use to work with the `OnChange` event for an attribute:</span></span>
- [<span data-ttu-id="2b369-117">addOnChange</span><span class="sxs-lookup"><span data-stu-id="2b369-117">addOnChange</span></span>](../attributes/addOnChange.md)
- [<span data-ttu-id="2b369-118">fireOnChange</span><span class="sxs-lookup"><span data-stu-id="2b369-118">fireOnChange</span></span>](../attributes/fireOnChange.md)
- [<span data-ttu-id="2b369-119">removeOnChange</span><span class="sxs-lookup"><span data-stu-id="2b369-119">removeOnChange</span></span>](../attributes/removeOnChange.md)

### <a name="related-topics"></a><span data-ttu-id="2b369-120">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="2b369-120">Related topics</span></span>
[<span data-ttu-id="2b369-121">attributes (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="2b369-121">attributes (Client API reference)</span></span>](../attributes.md)
 



