---
title: setVisible (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 485d9843-5907-49e4-971b-0e86f3bd1eb8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d005ad5f4ed5a2d272a3866b5ff0bfd8a07d16fc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387233"
---
# <a name="setvisible-client-api-reference"></a><span data-ttu-id="d8978-102">setVisible (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="d8978-102">setVisible (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setVisible-description.md](./includes/setVisible-description.md)] 

## <a name="syntax"></a><span data-ttu-id="d8978-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="d8978-103">Syntax</span></span>

`tabObj.setVisible(bool);`

## <a name="parameter"></a><span data-ttu-id="d8978-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="d8978-104">Parameter</span></span>

|<span data-ttu-id="d8978-105">Tên</span><span class="sxs-lookup"><span data-stu-id="d8978-105">Name</span></span>|<span data-ttu-id="d8978-106">Loại</span><span class="sxs-lookup"><span data-stu-id="d8978-106">Type</span></span>|<span data-ttu-id="d8978-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="d8978-107">Required</span></span>|<span data-ttu-id="d8978-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="d8978-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="d8978-109">bool</span><span class="sxs-lookup"><span data-stu-id="d8978-109">bool</span></span>|<span data-ttu-id="d8978-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8978-110">Boolean</span></span>|<span data-ttu-id="d8978-111">Có</span><span class="sxs-lookup"><span data-stu-id="d8978-111">Yes</span></span>|<span data-ttu-id="d8978-112">Specify **true** to show the tab; **false** to hide the tab.</span><span class="sxs-lookup"><span data-stu-id="d8978-112">Specify **true** to show the tab; **false** to hide the tab.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d8978-113">Chú thích</span><span class="sxs-lookup"><span data-stu-id="d8978-113">Remarks</span></span>

<span data-ttu-id="d8978-114">Another way to hide a tab is to hide all the sections within it.</span><span class="sxs-lookup"><span data-stu-id="d8978-114">Another way to hide a tab is to hide all the sections within it.</span></span> <span data-ttu-id="d8978-115">If all the sections within a tab are not visible, the tab will not be visible.</span><span class="sxs-lookup"><span data-stu-id="d8978-115">If all the sections within a tab are not visible, the tab will not be visible.</span></span>

### <a name="related-topics"></a><span data-ttu-id="d8978-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="d8978-116">Related topics</span></span>

[<span data-ttu-id="d8978-117">getVisible</span><span class="sxs-lookup"><span data-stu-id="d8978-117">getVisible</span></span>](getVisible.md)



