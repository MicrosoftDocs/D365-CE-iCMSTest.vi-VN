---
title: setEntityTypes (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 93154168-1e9f-4849-b4bb-be8804f86f81
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d27196d86060e348185bb242aef60994b319b9ec
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387522"
---
# <a name="setentitytypes-client-api-reference"></a><span data-ttu-id="58bfe-102">setEntityTypes (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="58bfe-102">setEntityTypes (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="58bfe-103">Sets the types of entities allowed in the lookup control.</span><span class="sxs-lookup"><span data-stu-id="58bfe-103">Sets the types of entities allowed in the lookup control.</span></span>

## <a name="control-types-supported"></a><span data-ttu-id="58bfe-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="58bfe-104">Control types supported</span></span>

<span data-ttu-id="58bfe-105">Lookup control</span><span class="sxs-lookup"><span data-stu-id="58bfe-105">Lookup control</span></span>

## <a name="syntax"></a><span data-ttu-id="58bfe-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="58bfe-106">Syntax</span></span>

`formContext.getControl(arg).setEntityTypes([entityLogicalNames]);`

## <a name="parameter"></a><span data-ttu-id="58bfe-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="58bfe-107">Parameter</span></span>

|<span data-ttu-id="58bfe-108">Tên</span><span class="sxs-lookup"><span data-stu-id="58bfe-108">Name</span></span>|<span data-ttu-id="58bfe-109">Loại</span><span class="sxs-lookup"><span data-stu-id="58bfe-109">Type</span></span>|<span data-ttu-id="58bfe-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="58bfe-110">Required</span></span>|<span data-ttu-id="58bfe-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="58bfe-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="58bfe-112">entityLogicalNames</span><span class="sxs-lookup"><span data-stu-id="58bfe-112">entityLogicalNames</span></span>|<span data-ttu-id="58bfe-113">Array of String</span><span class="sxs-lookup"><span data-stu-id="58bfe-113">Array of String</span></span>|<span data-ttu-id="58bfe-114">Có</span><span class="sxs-lookup"><span data-stu-id="58bfe-114">Yes</span></span>|<span data-ttu-id="58bfe-115">Specify the logical name of the entities allowed in the lookup control.</span><span class="sxs-lookup"><span data-stu-id="58bfe-115">Specify the logical name of the entities allowed in the lookup control.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="58bfe-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="58bfe-116">Related topics</span></span>

[<span data-ttu-id="58bfe-117">getEntityTypes</span><span class="sxs-lookup"><span data-stu-id="58bfe-117">getEntityTypes</span></span>](getEntityTypes.md)

 


