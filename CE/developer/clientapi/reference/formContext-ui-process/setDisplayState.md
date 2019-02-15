---
title: setDisplayState (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 21368fac-d4bc-4f75-8a9c-cce098fa0b45
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f90e065ff3b7cc54ed6bbf450c60290485a6e08c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387818"
---
# <a name="setdisplaystate-client-api-reference"></a><span data-ttu-id="ded06-102">setDisplayState (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="ded06-102">setDisplayState (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setDisplayState-description.md](./includes/setDisplayState-description.md)]

## <a name="syntax"></a><span data-ttu-id="ded06-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="ded06-103">Syntax</span></span>

`formContext.ui.process.setDisplayState(state);`

## <a name="parameter"></a><span data-ttu-id="ded06-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="ded06-104">Parameter</span></span>

|<span data-ttu-id="ded06-105">Tên</span><span class="sxs-lookup"><span data-stu-id="ded06-105">Name</span></span>|<span data-ttu-id="ded06-106">Loại</span><span class="sxs-lookup"><span data-stu-id="ded06-106">Type</span></span>|<span data-ttu-id="ded06-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="ded06-107">Required</span></span>|<span data-ttu-id="ded06-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="ded06-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="ded06-109">state</span><span class="sxs-lookup"><span data-stu-id="ded06-109">state</span></span>|<span data-ttu-id="ded06-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="ded06-110">String</span></span>|<span data-ttu-id="ded06-111">Có</span><span class="sxs-lookup"><span data-stu-id="ded06-111">Yes</span></span>|<span data-ttu-id="ded06-112">Specify "expanded", "collapsed", or "floating".</span><span class="sxs-lookup"><span data-stu-id="ded06-112">Specify "expanded", "collapsed", or "floating".</span></span> <span data-ttu-id="ded06-113">The value "floating" is not supported on the web client.</span><span class="sxs-lookup"><span data-stu-id="ded06-113">The value "floating" is not supported on the web client.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="ded06-114">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="ded06-114">Related topics</span></span>

[<span data-ttu-id="ded06-115">getDisplayState</span><span class="sxs-lookup"><span data-stu-id="ded06-115">getDisplayState</span></span>](getDisplayState.md)

[<span data-ttu-id="ded06-116">formContext.ui.process</span><span class="sxs-lookup"><span data-stu-id="ded06-116">formContext.ui.process</span></span>](../formContext-ui-process.md)



