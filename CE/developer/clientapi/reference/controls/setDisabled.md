---
title: setDisabled (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 86383cb1-c4c8-4e82-9f60-1dc4588b519d
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9b4f7d8a23631211d4bb08ffd80799d0b3df61c9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388440"
---
# <a name="setdisabled-client-api-reference"></a><span data-ttu-id="e7b7b-102">setDisabled (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e7b7b-102">setDisabled (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e7b7b-103">Sets whether the control is disabled.</span><span class="sxs-lookup"><span data-stu-id="e7b7b-103">Sets whether the control is disabled.</span></span>

## <a name="control-types-supported"></a><span data-ttu-id="e7b7b-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="e7b7b-104">Control types supported</span></span>

<span data-ttu-id="e7b7b-105">All except **kbsearch** control type</span><span class="sxs-lookup"><span data-stu-id="e7b7b-105">All except **kbsearch** control type</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b7b-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="e7b7b-106">Syntax</span></span>

`formContext.getControl(arg).setDisabled(bool);`

## <a name="parameter"></a><span data-ttu-id="e7b7b-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="e7b7b-107">Parameter</span></span>

|<span data-ttu-id="e7b7b-108">Tên</span><span class="sxs-lookup"><span data-stu-id="e7b7b-108">Name</span></span>|<span data-ttu-id="e7b7b-109">Loại</span><span class="sxs-lookup"><span data-stu-id="e7b7b-109">Type</span></span>|<span data-ttu-id="e7b7b-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="e7b7b-110">Required</span></span>|<span data-ttu-id="e7b7b-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e7b7b-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="e7b7b-112">bool</span><span class="sxs-lookup"><span data-stu-id="e7b7b-112">bool</span></span>|<span data-ttu-id="e7b7b-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="e7b7b-113">Boolean</span></span>|<span data-ttu-id="e7b7b-114">Có</span><span class="sxs-lookup"><span data-stu-id="e7b7b-114">Yes</span></span>|<span data-ttu-id="e7b7b-115">Specify **true** or **false** to disable or enable the control.</span><span class="sxs-lookup"><span data-stu-id="e7b7b-115">Specify **true** or **false** to disable or enable the control.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="e7b7b-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="e7b7b-116">Related topics</span></span>

[<span data-ttu-id="e7b7b-117">getDisabled</span><span class="sxs-lookup"><span data-stu-id="e7b7b-117">getDisabled</span></span>](getDisabled.md)



