---
title: getTotalResultCount (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1f9169ce-cba3-4bb6-af20-f86140139cfe
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 23fd1bf802636bfd7022089c4e4cb54e7d937925
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385961"
---
# <a name="gettotalresultcount-client-api-reference"></a><span data-ttu-id="b8117-102">getTotalResultCount (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="b8117-102">getTotalResultCount (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b8117-103">Gets the count of results found in the search control.</span><span class="sxs-lookup"><span data-stu-id="b8117-103">Gets the count of results found in the search control.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="b8117-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="b8117-104">Control types supported</span></span>

<span data-ttu-id="b8117-105">knowledge base search control</span><span class="sxs-lookup"><span data-stu-id="b8117-105">knowledge base search control</span></span>

## <a name="syntax"></a><span data-ttu-id="b8117-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="b8117-106">Syntax</span></span>

```
var kbSearchControl = formContext.getControl("<name>");
var searchCount = kbSearchControl.getTotalResultCount();
```

## <a name="return-value"></a><span data-ttu-id="b8117-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="b8117-107">Return Value</span></span>

<span data-ttu-id="b8117-108">**Type**: Number</span><span class="sxs-lookup"><span data-stu-id="b8117-108">**Type**: Number</span></span>

<span data-ttu-id="b8117-109">**Description**: The count of the search result.</span><span class="sxs-lookup"><span data-stu-id="b8117-109">**Description**: The count of the search result.</span></span>
