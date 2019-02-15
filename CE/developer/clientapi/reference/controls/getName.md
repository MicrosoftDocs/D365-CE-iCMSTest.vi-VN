---
title: getName (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: cacd309c0853370ecd55725bf892249f9e313cfd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387458"
---
# <a name="getname-client-api-reference"></a><span data-ttu-id="f6b82-102">getName (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="f6b82-102">getName (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f6b82-103">Returns the name assigned to the control.</span><span class="sxs-lookup"><span data-stu-id="f6b82-103">Returns the name assigned to the control.</span></span>

>[!NOTE]
><span data-ttu-id="f6b82-104">The name assigned to a control is not determined until the form loads.</span><span class="sxs-lookup"><span data-stu-id="f6b82-104">The name assigned to a control is not determined until the form loads.</span></span> <span data-ttu-id="f6b82-105">Changes to the form may change the name assigned to a given control.</span><span class="sxs-lookup"><span data-stu-id="f6b82-105">Changes to the form may change the name assigned to a given control.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="f6b82-106">Control types supported</span><span class="sxs-lookup"><span data-stu-id="f6b82-106">Control types supported</span></span>

<span data-ttu-id="f6b82-107">Tất cả</span><span class="sxs-lookup"><span data-stu-id="f6b82-107">All</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b82-108">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="f6b82-108">Syntax</span></span>

`formContext.getControl(arg).getName();`

## <a name="return-value"></a><span data-ttu-id="f6b82-109">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="f6b82-109">Return Value</span></span>

<span data-ttu-id="f6b82-110">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="f6b82-110">**Type**: String</span></span>

<span data-ttu-id="f6b82-111">**Description**: The name of the control.</span><span class="sxs-lookup"><span data-stu-id="f6b82-111">**Description**: The name of the control.</span></span>

### <a name="related-topics"></a><span data-ttu-id="f6b82-112">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="f6b82-112">Related topics</span></span>

[<span data-ttu-id="f6b82-113">Kiểm soát</span><span class="sxs-lookup"><span data-stu-id="f6b82-113">Controls</span></span>](../controls.md)

