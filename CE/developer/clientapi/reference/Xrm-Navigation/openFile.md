---
title: openFile (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 6a2497fe-08ad-4953-b3ff-44c72bc25082
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 272ee6bc12e9a96ad88b8a336d0ed6a6ccc24f69
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388488"
---
# <a name="openfile-client-api-reference"></a><span data-ttu-id="46666-102">openFile (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="46666-102">openFile (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openFile-description.md](./includes/openFile-description.md)]

## <a name="syntax"></a><span data-ttu-id="46666-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="46666-103">Syntax</span></span>

`Xrm.Navigation.openFile(file,openFileOptions)`

## <a name="parameters"></a><span data-ttu-id="46666-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="46666-104">Parameters</span></span>

| <span data-ttu-id="46666-105">Parameter Name</span><span class="sxs-lookup"><span data-stu-id="46666-105">Parameter Name</span></span>        | <span data-ttu-id="46666-106">Loại</span><span class="sxs-lookup"><span data-stu-id="46666-106">Type</span></span>           | <span data-ttu-id="46666-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="46666-107">Required</span></span>  |<span data-ttu-id="46666-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="46666-108">Description</span></span>  |
| ------------- |-------------| -----|-----|
|<span data-ttu-id="46666-109">file</span><span class="sxs-lookup"><span data-stu-id="46666-109">file</span></span> |<span data-ttu-id="46666-110">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="46666-110">Object</span></span> | <span data-ttu-id="46666-111">Có</span><span class="sxs-lookup"><span data-stu-id="46666-111">Yes</span></span>|<span data-ttu-id="46666-112">An object describing the file to open.</span><span class="sxs-lookup"><span data-stu-id="46666-112">An object describing the file to open.</span></span> <span data-ttu-id="46666-113">The object has the following attributes:</span><span class="sxs-lookup"><span data-stu-id="46666-113">The object has the following attributes:</span></span><br/><span data-ttu-id="46666-114">- **fileContent**: String.</span><span class="sxs-lookup"><span data-stu-id="46666-114">- **fileContent**: String.</span></span> <span data-ttu-id="46666-115">Contents of the file.</span><span class="sxs-lookup"><span data-stu-id="46666-115">Contents of the file.</span></span>  <br/><span data-ttu-id="46666-116">- **fileName**: String.</span><span class="sxs-lookup"><span data-stu-id="46666-116">- **fileName**: String.</span></span> <span data-ttu-id="46666-117">Name of the file.</span><span class="sxs-lookup"><span data-stu-id="46666-117">Name of the file.</span></span><br/><span data-ttu-id="46666-118">- **fileSize**: Number.</span><span class="sxs-lookup"><span data-stu-id="46666-118">- **fileSize**: Number.</span></span> <span data-ttu-id="46666-119">Size of the file in KB.</span><span class="sxs-lookup"><span data-stu-id="46666-119">Size of the file in KB.</span></span><br/><span data-ttu-id="46666-120">- **mimeType**: String.</span><span class="sxs-lookup"><span data-stu-id="46666-120">- **mimeType**: String.</span></span> <span data-ttu-id="46666-121">MIME type of the file.</span><span class="sxs-lookup"><span data-stu-id="46666-121">MIME type of the file.</span></span>|
|<span data-ttu-id="46666-122">openFileOptions</span><span class="sxs-lookup"><span data-stu-id="46666-122">openFileOptions</span></span> |<span data-ttu-id="46666-123">Số</span><span class="sxs-lookup"><span data-stu-id="46666-123">Number</span></span> | <span data-ttu-id="46666-124">Không</span><span class="sxs-lookup"><span data-stu-id="46666-124">No</span></span>|<span data-ttu-id="46666-125">Specify whether to open or save the file:</span><span class="sxs-lookup"><span data-stu-id="46666-125">Specify whether to open or save the file:</span></span><br/> `1:Open`<br/> `2:Save`<br/><span data-ttu-id="46666-126">If you do not specify this parameter, by default **1** (open) is passed.</span><span class="sxs-lookup"><span data-stu-id="46666-126">If you do not specify this parameter, by default **1** (open) is passed.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="46666-127">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="46666-127">Related topics</span></span>

[<span data-ttu-id="46666-128">Xrm.Navigation</span><span class="sxs-lookup"><span data-stu-id="46666-128">Xrm.Navigation</span></span>](../xrm-navigation.md)
