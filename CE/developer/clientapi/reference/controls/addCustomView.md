---
title: addCustomView (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 482b8cd4-e643-48ea-8a54-d8601271ec81
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: def8d71f5f6e7f67faf3bbbebe853e3cd5866379
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387582"
---
# <a name="addcustomview-client-api-reference"></a><span data-ttu-id="5933c-102">addCustomView (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="5933c-102">addCustomView (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5933c-103">Adds a new view for the lookup dialog box.</span><span class="sxs-lookup"><span data-stu-id="5933c-103">Adds a new view for the lookup dialog box.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="5933c-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="5933c-104">Control types supported</span></span>

<span data-ttu-id="5933c-105">Tra cứu</span><span class="sxs-lookup"><span data-stu-id="5933c-105">Lookup</span></span>

## <a name="syntax"></a><span data-ttu-id="5933c-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="5933c-106">Syntax</span></span>

`formContext.getControl(arg).addCustomView(viewId, entityName, viewDisplayName, fetchXml, layoutXml, isDefault)`

## <a name="parameters"></a><span data-ttu-id="5933c-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="5933c-107">Parameters</span></span>

- <span data-ttu-id="5933c-108">**viewId**: String.</span><span class="sxs-lookup"><span data-stu-id="5933c-108">**viewId**: String.</span></span> <span data-ttu-id="5933c-109">The string representation of a GUID for a view.</span><span class="sxs-lookup"><span data-stu-id="5933c-109">The string representation of a GUID for a view.</span></span>
    > [!NOTE]
    > <span data-ttu-id="5933c-110">This value is never saved and only needs to be unique among the other available views for the lookup.</span><span class="sxs-lookup"><span data-stu-id="5933c-110">This value is never saved and only needs to be unique among the other available views for the lookup.</span></span> <span data-ttu-id="5933c-111">A string for a non-valid GUID will work, for example “{00000000-0000-0000-0000-000000000001}”.</span><span class="sxs-lookup"><span data-stu-id="5933c-111">A string for a non-valid GUID will work, for example “{00000000-0000-0000-0000-000000000001}”.</span></span> <span data-ttu-id="5933c-112">It’s recommended that you use a tool like **guidgen.exe** to generate a valid GUID.</span><span class="sxs-lookup"><span data-stu-id="5933c-112">It’s recommended that you use a tool like **guidgen.exe** to generate a valid GUID.</span></span>  

- <span data-ttu-id="5933c-113">**entityName**: String.</span><span class="sxs-lookup"><span data-stu-id="5933c-113">**entityName**: String.</span></span> <span data-ttu-id="5933c-114">The name of the entity.</span><span class="sxs-lookup"><span data-stu-id="5933c-114">The name of the entity.</span></span>
- <span data-ttu-id="5933c-115">**viewDisplayName**: String.</span><span class="sxs-lookup"><span data-stu-id="5933c-115">**viewDisplayName**: String.</span></span> <span data-ttu-id="5933c-116">The name of the view.</span><span class="sxs-lookup"><span data-stu-id="5933c-116">The name of the view.</span></span>
- <span data-ttu-id="5933c-117">**fetchXml**: String.</span><span class="sxs-lookup"><span data-stu-id="5933c-117">**fetchXml**: String.</span></span> <span data-ttu-id="5933c-118">The fetchXml query for the view.</span><span class="sxs-lookup"><span data-stu-id="5933c-118">The fetchXml query for the view.</span></span>
- <span data-ttu-id="5933c-119">**layoutXml**: String.</span><span class="sxs-lookup"><span data-stu-id="5933c-119">**layoutXml**: String.</span></span> <span data-ttu-id="5933c-120">The XML that defines the layout of the view.</span><span class="sxs-lookup"><span data-stu-id="5933c-120">The XML that defines the layout of the view.</span></span>
- <span data-ttu-id="5933c-121">**isDefault**: Boolean: Indicates whether the view should be the default view.</span><span class="sxs-lookup"><span data-stu-id="5933c-121">**isDefault**: Boolean: Indicates whether the view should be the default view.</span></span>

## <a name="remarks"></a><span data-ttu-id="5933c-122">Chú thích</span><span class="sxs-lookup"><span data-stu-id="5933c-122">Remarks</span></span>

<span data-ttu-id="5933c-123">This method doesn’t work with **Owner** lookups.</span><span class="sxs-lookup"><span data-stu-id="5933c-123">This method doesn’t work with **Owner** lookups.</span></span> <span data-ttu-id="5933c-124">Owner lookups are used to assign user-owned records.</span><span class="sxs-lookup"><span data-stu-id="5933c-124">Owner lookups are used to assign user-owned records.</span></span>
