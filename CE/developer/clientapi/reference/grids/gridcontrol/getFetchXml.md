---
title: getFetchXml (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 12/23/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d0f1da4591726e3a57d138467ae2773cec45637a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385537"
---
# <a name="getfetchxml-client-api-reference"></a><span data-ttu-id="4a2f5-102">getFetchXml (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="4a2f5-102">getFetchXml (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getFetchXml-description.md](./includes/getFetchXml-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="4a2f5-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="4a2f5-103">Grid types supported</span></span>

<span data-ttu-id="4a2f5-104">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="4a2f5-104">Read-only and editable grids</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2f5-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="4a2f5-105">Syntax</span></span>

`var result = gridContext.getFetchXml();`

## <a name="return-value"></a><span data-ttu-id="4a2f5-106">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="4a2f5-106">Return Value</span></span>

<span data-ttu-id="4a2f5-107">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="4a2f5-107">**Type**: String</span></span>

<span data-ttu-id="4a2f5-108">**Description**: The FetchXML query.</span><span class="sxs-lookup"><span data-stu-id="4a2f5-108">**Description**: The FetchXML query.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a2f5-109">Chú thích</span><span class="sxs-lookup"><span data-stu-id="4a2f5-109">Remarks</span></span>

<span data-ttu-id="4a2f5-110">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext)</span><span class="sxs-lookup"><span data-stu-id="4a2f5-110">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext)</span></span> 

## <a name="example"></a><span data-ttu-id="4a2f5-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="4a2f5-111">Example</span></span>

<span data-ttu-id="4a2f5-112">The following example displays the retrieved FetchXML of the Contacts subgrid in the Console:</span><span class="sxs-lookup"><span data-stu-id="4a2f5-112">The following example displays the retrieved FetchXML of the Contacts subgrid in the Console:</span></span>

```JavaScript
function myFunction(executionContext) {
    var formContext = executionContext.getFormContext(); // get the form context
    var gridContext = formContext.getControl("Contacts"); // get the grid context
    var retrieveFetchXML = function () {
        var result = gridContext.getFetchXml();
        console.log(result)
    };
    gridContext.addOnLoad(retrieveFetchXML);    
}
```


