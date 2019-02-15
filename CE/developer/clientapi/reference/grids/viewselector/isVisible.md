---
title: isVisible (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d22cd046-064c-47ef-9e46-5cc4c8b6e280
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7e6b825078d268ebc1f1c9644b1fb4febe811511
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387164"
---
# <a name="isvisible-client-api-reference"></a><span data-ttu-id="1db38-102">isVisible (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="1db38-102">isVisible (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/isVisible-description.md](./includes/isVisible-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="1db38-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="1db38-103">Grid types supported</span></span>

<span data-ttu-id="1db38-104">Read-only grid</span><span class="sxs-lookup"><span data-stu-id="1db38-104">Read-only grid</span></span>

## <a name="syntax"></a><span data-ttu-id="1db38-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="1db38-105">Syntax</span></span>

`viewSelector.isVisible();`

## <a name="return-value"></a><span data-ttu-id="1db38-106">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="1db38-106">Return Value</span></span>

<span data-ttu-id="1db38-107">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="1db38-107">**Type**: Boolean</span></span>

<span data-ttu-id="1db38-108">**Description**: true if visible; false otherwise.</span><span class="sxs-lookup"><span data-stu-id="1db38-108">**Description**: true if visible; false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1db38-109">Chú thích</span><span class="sxs-lookup"><span data-stu-id="1db38-109">Remarks</span></span>

<span data-ttu-id="1db38-110">If the subgrid control is not configured to display the view selector, calling this method on the **ViewSelector** returned by the GridControl.getViewSelector method will throw an error.</span><span class="sxs-lookup"><span data-stu-id="1db38-110">If the subgrid control is not configured to display the view selector, calling this method on the **ViewSelector** returned by the GridControl.getViewSelector method will throw an error.</span></span>

<span data-ttu-id="1db38-111">To get the `viewSelector` object, see [ViewSelector](../viewselector.md).</span><span class="sxs-lookup"><span data-stu-id="1db38-111">To get the `viewSelector` object, see [ViewSelector](../viewselector.md).</span></span>



