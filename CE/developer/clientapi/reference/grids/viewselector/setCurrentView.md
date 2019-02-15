---
title: setCurrentView (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: f5ee65bf-2964-49c9-9dd2-d81416353bf3
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2f4c8fa86003954a0583743367f901d4a6f7d24e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386054"
---
# <a name="setcurrentview-client-api-reference"></a><span data-ttu-id="d93c8-102">setCurrentView (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="d93c8-102">setCurrentView (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setCurrentView-description.md](./includes/setCurrentView-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="d93c8-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="d93c8-103">Grid types supported</span></span>

<span data-ttu-id="d93c8-104">Read-only grid</span><span class="sxs-lookup"><span data-stu-id="d93c8-104">Read-only grid</span></span>

## <a name="syntax"></a><span data-ttu-id="d93c8-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="d93c8-105">Syntax</span></span>

`viewSelector.setCurrentView(object);`

## <a name="parameter"></a><span data-ttu-id="d93c8-106">Tham số</span><span class="sxs-lookup"><span data-stu-id="d93c8-106">Parameter</span></span>

|<span data-ttu-id="d93c8-107">Tên</span><span class="sxs-lookup"><span data-stu-id="d93c8-107">Name</span></span>|<span data-ttu-id="d93c8-108">Loại</span><span class="sxs-lookup"><span data-stu-id="d93c8-108">Type</span></span>|<span data-ttu-id="d93c8-109">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="d93c8-109">Required</span></span>|<span data-ttu-id="d93c8-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="d93c8-110">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="d93c8-111">đối tượng</span><span class="sxs-lookup"><span data-stu-id="d93c8-111">object</span></span>|<span data-ttu-id="d93c8-112">Lookup object</span><span class="sxs-lookup"><span data-stu-id="d93c8-112">Lookup object</span></span>|<span data-ttu-id="d93c8-113">Có</span><span class="sxs-lookup"><span data-stu-id="d93c8-113">Yes</span></span>|<span data-ttu-id="d93c8-114">Specify the Lookup object that has the following attributes:</span><span class="sxs-lookup"><span data-stu-id="d93c8-114">Specify the Lookup object that has the following attributes:</span></span><br/><span data-ttu-id="d93c8-115">- **entityType**: Number.</span><span class="sxs-lookup"><span data-stu-id="d93c8-115">- **entityType**: Number.</span></span> <span data-ttu-id="d93c8-116">The object type code for the SavedQuery (1039) or UserQuery (4230) that represents the view the user can select.</span><span class="sxs-lookup"><span data-stu-id="d93c8-116">The object type code for the SavedQuery (1039) or UserQuery (4230) that represents the view the user can select.</span></span><br/><span data-ttu-id="d93c8-117">- **id**: String.</span><span class="sxs-lookup"><span data-stu-id="d93c8-117">- **id**: String.</span></span> <span data-ttu-id="d93c8-118">The Id for the view the user can select.</span><span class="sxs-lookup"><span data-stu-id="d93c8-118">The Id for the view the user can select.</span></span><br/><span data-ttu-id="d93c8-119">- **name**: String.</span><span class="sxs-lookup"><span data-stu-id="d93c8-119">- **name**: String.</span></span> <span data-ttu-id="d93c8-120">The name of the view the user can select.</span><span class="sxs-lookup"><span data-stu-id="d93c8-120">The name of the view the user can select.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d93c8-121">Chú thích</span><span class="sxs-lookup"><span data-stu-id="d93c8-121">Remarks</span></span>

<span data-ttu-id="d93c8-122">If the subgrid control is not configured to display the view selector, calling this method on the `viewSelector` object will throw an error.</span><span class="sxs-lookup"><span data-stu-id="d93c8-122">If the subgrid control is not configured to display the view selector, calling this method on the `viewSelector` object will throw an error.</span></span>

<span data-ttu-id="d93c8-123">To get the `viewSelector` object, see [ViewSelector](../viewselector.md).</span><span class="sxs-lookup"><span data-stu-id="d93c8-123">To get the `viewSelector` object, see [ViewSelector](../viewselector.md).</span></span>

## <a name="example"></a><span data-ttu-id="d93c8-124">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d93c8-124">Example</span></span>

```JavaScript
function setView(executionContext) {
    var ContactsIFollow = {
        entityType: 1039, // SavedQuery
        id: "3A282DA1-5D90-E011-95AE-00155D9CFA02",
        name: "Contacts I Follow"
    }
    // Get the gridContext
    var formContext = executionContext.getFormContext();
    var gridContext = formContext.getControl("Contacts");

    // Set the view using ContactsIFollow
    gridContext.getViewSelector().setCurrentView(ContactsIFollow);
}
```

### <a name="related-topics"></a><span data-ttu-id="d93c8-125">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="d93c8-125">Related topics</span></span>

[<span data-ttu-id="d93c8-126">ViewSelector</span><span class="sxs-lookup"><span data-stu-id="d93c8-126">ViewSelector</span></span>](../viewselector.md)




