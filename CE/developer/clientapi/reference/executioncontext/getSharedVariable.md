---
title: getSharedVariable (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 702a13c1-f4ae-4de2-9e8b-95360ad9240c
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5308ca4da7ef19fffee5da77a9896ee9a6f859f4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386910"
---
# <a name="getsharedvariable-client-api-reference"></a><span data-ttu-id="a4ce7-102">getSharedVariable (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a4ce7-102">getSharedVariable (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a4ce7-103">Retrieves a variable set using the [setSharedVariable](setSharedVariable.md) method.</span><span class="sxs-lookup"><span data-stu-id="a4ce7-103">Retrieves a variable set using the [setSharedVariable](setSharedVariable.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4ce7-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="a4ce7-104">Syntax</span></span>

`ExecutionContextObj.getSharedVariable(key)`

## <a name="parameters"></a><span data-ttu-id="a4ce7-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="a4ce7-105">Parameters</span></span>

<span data-ttu-id="a4ce7-106">**khóa**</span><span class="sxs-lookup"><span data-stu-id="a4ce7-106">**key**</span></span>

   <span data-ttu-id="a4ce7-107">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="a4ce7-107">**Type**: String</span></span>

   <span data-ttu-id="a4ce7-108">**Description**: The name of the variable.</span><span class="sxs-lookup"><span data-stu-id="a4ce7-108">**Description**: The name of the variable.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4ce7-109">Return value</span><span class="sxs-lookup"><span data-stu-id="a4ce7-109">Return value</span></span>

<span data-ttu-id="a4ce7-110">**Type**: Object</span><span class="sxs-lookup"><span data-stu-id="a4ce7-110">**Type**: Object</span></span>

<span data-ttu-id="a4ce7-111">**Description**: The specific type depends on what the value object is.</span><span class="sxs-lookup"><span data-stu-id="a4ce7-111">**Description**: The specific type depends on what the value object is.</span></span>

### <a name="related-topics"></a><span data-ttu-id="a4ce7-112">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a4ce7-112">Related topics</span></span>
[<span data-ttu-id="a4ce7-113">setSharedVariable</span><span class="sxs-lookup"><span data-stu-id="a4ce7-113">setSharedVariable</span></span>](setSharedVariable.md)

[<span data-ttu-id="a4ce7-114">Execution context</span><span class="sxs-lookup"><span data-stu-id="a4ce7-114">Execution context</span></span>](../execution-context.md)





