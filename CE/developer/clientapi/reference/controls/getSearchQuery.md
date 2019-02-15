---
title: getSearchQuery (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
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
ms.openlocfilehash: f0c6ffd522f88effbc13f14f3617bfb00f0ff951
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387179"
---
# <a name="getsearchquery-client-api-reference"></a><span data-ttu-id="a4ac6-102">getSearchQuery (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a4ac6-102">getSearchQuery (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a4ac6-103">Gets the text used as the search criteria for the knowledge base management control.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-103">Gets the text used as the search criteria for the knowledge base management control.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="a4ac6-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="a4ac6-104">Control types supported</span></span>

<span data-ttu-id="a4ac6-105">knowledge base search control</span><span class="sxs-lookup"><span data-stu-id="a4ac6-105">knowledge base search control</span></span>

## <a name="syntax"></a><span data-ttu-id="a4ac6-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="a4ac6-106">Syntax</span></span>

```
var kbSearchControl = formContext.getControl("<name>");
var searchQuery = kbSearchControl.getSearchQuery();
```

## <a name="return-value"></a><span data-ttu-id="a4ac6-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="a4ac6-107">Return Value</span></span>

<span data-ttu-id="a4ac6-108">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="a4ac6-108">**Type**: String</span></span>

<span data-ttu-id="a4ac6-109">**Description**: The text of the search query.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-109">**Description**: The text of the search query.</span></span>

### <a name="related-topics"></a><span data-ttu-id="a4ac6-110">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a4ac6-110">Related topics</span></span>

[<span data-ttu-id="a4ac6-111">setSearchQuery</span><span class="sxs-lookup"><span data-stu-id="a4ac6-111">setSearchQuery</span></span>](setSearchQuery.md)

