---
title: getTotalRecordCount (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 8305f0cb-9959-4429-a721-a864ade4cd35
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0a10f8e6129f25bf5bd1bcaddd5f417e0d783887
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387635"
---
# <a name="gettotalrecordcount-client-api-reference"></a><span data-ttu-id="11da8-102">getTotalRecordCount (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="11da8-102">getTotalRecordCount (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getTotalRecordCount-description.md](./includes/getTotalRecordCount-description.md)]

- <span data-ttu-id="11da8-103">When the Dynamics 365 for Outlook client isn’t connected to the server, this number is limited to those records that the user has selected to take offline.</span><span class="sxs-lookup"><span data-stu-id="11da8-103">When the Dynamics 365 for Outlook client isn’t connected to the server, this number is limited to those records that the user has selected to take offline.</span></span>
- <span data-ttu-id="11da8-104">For Dynamics 365 for Customer Engagement mobile clients, this method will return the number of records in the subgrid.</span><span class="sxs-lookup"><span data-stu-id="11da8-104">For Dynamics 365 for Customer Engagement mobile clients, this method will return the number of records in the subgrid.</span></span>

## <a name="grid-types-supported"></a><span data-ttu-id="11da8-105">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="11da8-105">Grid types supported</span></span>

<span data-ttu-id="11da8-106">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="11da8-106">Read-only and editable grids</span></span>

## <a name="syntax"></a><span data-ttu-id="11da8-107">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="11da8-107">Syntax</span></span>

`var filteredRecordCount = gridContext.getGrid().getTotalRecordCount();`

## <a name="return-value"></a><span data-ttu-id="11da8-108">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="11da8-108">Return Value</span></span>

<span data-ttu-id="11da8-109">**Type**: Number</span><span class="sxs-lookup"><span data-stu-id="11da8-109">**Type**: Number</span></span>

<span data-ttu-id="11da8-110">**Description**: Total number of records that match the filter criteria of the view.</span><span class="sxs-lookup"><span data-stu-id="11da8-110">**Description**: Total number of records that match the filter criteria of the view.</span></span>

## <a name="remarks"></a><span data-ttu-id="11da8-111">Chú thích</span><span class="sxs-lookup"><span data-stu-id="11da8-111">Remarks</span></span>

<span data-ttu-id="11da8-112">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span><span class="sxs-lookup"><span data-stu-id="11da8-112">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span></span>

<span data-ttu-id="11da8-113">See [Collections (Client API reference)](../../collections.md) for information on the methods available to access data in a collection.</span><span class="sxs-lookup"><span data-stu-id="11da8-113">See [Collections (Client API reference)](../../collections.md) for information on the methods available to access data in a collection.</span></span>