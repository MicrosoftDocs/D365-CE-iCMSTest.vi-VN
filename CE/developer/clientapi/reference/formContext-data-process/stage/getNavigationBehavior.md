---
title: getNavigationBehavior (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 01/22/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 649fe7b0-016d-409f-ba3c-b14e0f1953e0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4d78e357fe727c04b3b1924179f8c8e291ddd8ad
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385518"
---
# <a name="getnavigationbehavior-client-api-reference"></a><span data-ttu-id="8ff12-102">getNavigationBehavior (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="8ff12-102">getNavigationBehavior (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getNavigationBehavior-description.md](./includes/getNavigationBehavior-description.md)]

> [!NOTE]
> <span data-ttu-id="8ff12-103">This method is available only for [Unified Interface](/dynamics365/get-started/whats-new/customer-engagement/new-in-version-9#unified-interface-framework-for-new-apps).</span><span class="sxs-lookup"><span data-stu-id="8ff12-103">This method is available only for [Unified Interface](/dynamics365/get-started/whats-new/customer-engagement/new-in-version-9#unified-interface-framework-for-new-apps).</span></span> 

## <a name="syntax"></a><span data-ttu-id="8ff12-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="8ff12-104">Syntax</span></span>

```
stageObj.getNavigationBehavior().allowCreateNew = function () {
    return true|false;
}
```

## <a name="returns"></a><span data-ttu-id="8ff12-105">Returns</span><span class="sxs-lookup"><span data-stu-id="8ff12-105">Returns</span></span>

<span data-ttu-id="8ff12-106">**Type**: Object</span><span class="sxs-lookup"><span data-stu-id="8ff12-106">**Type**: Object</span></span> 

<span data-ttu-id="8ff12-107">**Description**: An object with the `allowCreateNew` property that lets you define whether the **Create** button will be available in a stage so that user can create an instance of entityB from the entityA form in a cross-entity business process flow navigation scenario.</span><span class="sxs-lookup"><span data-stu-id="8ff12-107">**Description**: An object with the `allowCreateNew` property that lets you define whether the **Create** button will be available in a stage so that user can create an instance of entityB from the entityA form in a cross-entity business process flow navigation scenario.</span></span> 

<span data-ttu-id="8ff12-108">For example, here is the **Create** button in the **Develop** stage of the **AccountToContactProcess** sample business process flow that lets you create a Contact record from the Account form.</span><span class="sxs-lookup"><span data-stu-id="8ff12-108">For example, here is the **Create** button in the **Develop** stage of the **AccountToContactProcess** sample business process flow that lets you create a Contact record from the Account form.</span></span>

![](../../../../media/clientapi_getNavigationBehavior.png)

<span data-ttu-id="8ff12-109">The `allowCreateNew` property will return **undefined** for business process flow records that do not implement cross-entity navigation.</span><span class="sxs-lookup"><span data-stu-id="8ff12-109">The `allowCreateNew` property will return **undefined** for business process flow records that do not implement cross-entity navigation.</span></span>

## <a name="example"></a><span data-ttu-id="8ff12-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="8ff12-110">Example</span></span>

<span data-ttu-id="8ff12-111">The following sample code shows how you can hide or display the **Create** button for an active stage of a business process flow depending on its name.</span><span class="sxs-lookup"><span data-stu-id="8ff12-111">The following sample code shows how you can hide or display the **Create** button for an active stage of a business process flow depending on its name.</span></span>

```JavaScript
function sampleFunction(executionContext) {
    var formContext = executionContext.getFormContext();
    formContext.data.process.getActiveStage.getNavigationBehavior().allowCreateNew = function () {
        if (formContext.data.process.getName() === 'Test Process') {
            return false; // Create button is not available
        }
        else {
            return true; // Create button is available
        }
    }
}
```

### <a name="related-topics"></a><span data-ttu-id="8ff12-112">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="8ff12-112">Related topics</span></span>
 
[<span data-ttu-id="8ff12-113">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="8ff12-113">formContext.data.process</span></span>](../../formContext-data-process.md)

