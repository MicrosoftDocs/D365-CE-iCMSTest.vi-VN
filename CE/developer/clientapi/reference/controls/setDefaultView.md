---
title: setDefaultView (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 8c918cd4-d0ce-45e5-91a3-1addf11258c7
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ee8ad9e6eb3c293566479346bb64ebfb146b5617
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386393"
---
# <a name="setdefaultview-client-api-reference"></a><span data-ttu-id="26a8c-102">setDefaultView (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="26a8c-102">setDefaultView (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="26a8c-103">Sets the default view for the lookup control dialog box.</span><span class="sxs-lookup"><span data-stu-id="26a8c-103">Sets the default view for the lookup control dialog box.</span></span>

## <a name="control-types-supported"></a><span data-ttu-id="26a8c-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="26a8c-104">Control types supported</span></span>

<span data-ttu-id="26a8c-105">Tra cứu</span><span class="sxs-lookup"><span data-stu-id="26a8c-105">Lookup</span></span>

## <a name="syntax"></a><span data-ttu-id="26a8c-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="26a8c-106">Syntax</span></span>

`formContext.getControl(arg).setDefaultView(viewId);`

## <a name="parameter"></a><span data-ttu-id="26a8c-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="26a8c-107">Parameter</span></span>

|<span data-ttu-id="26a8c-108">Tên</span><span class="sxs-lookup"><span data-stu-id="26a8c-108">Name</span></span>|<span data-ttu-id="26a8c-109">Loại</span><span class="sxs-lookup"><span data-stu-id="26a8c-109">Type</span></span>|<span data-ttu-id="26a8c-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="26a8c-110">Required</span></span>|<span data-ttu-id="26a8c-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="26a8c-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="26a8c-112">viewId</span><span class="sxs-lookup"><span data-stu-id="26a8c-112">viewId</span></span>|<span data-ttu-id="26a8c-113">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="26a8c-113">String</span></span>|<span data-ttu-id="26a8c-114">Có</span><span class="sxs-lookup"><span data-stu-id="26a8c-114">Yes</span></span>|<span data-ttu-id="26a8c-115">The ID of the view to be set as the default view.</span><span class="sxs-lookup"><span data-stu-id="26a8c-115">The ID of the view to be set as the default view.</span></span>|

## <a name="example"></a><span data-ttu-id="26a8c-116">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="26a8c-116">Example</span></span>

<span data-ttu-id="26a8c-117">This **setDefaultViewSample** function will set the **account** entity form primary contact lookup default view to the **My Active Contacts** view.</span><span class="sxs-lookup"><span data-stu-id="26a8c-117">This **setDefaultViewSample** function will set the **account** entity form primary contact lookup default view to the **My Active Contacts** view.</span></span>

```JavaScript
function setDefaultViewSample(executionContext) {
    var formContext = executionContext.getFormContext();
    formContext.getControl("primarycontactid").setDefaultView("{00000000-0000-0000-00AA-000010001003}");
}
```

### <a name="related-topics"></a><span data-ttu-id="26a8c-118">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="26a8c-118">Related topics</span></span>

[<span data-ttu-id="26a8c-119">getDefaultView</span><span class="sxs-lookup"><span data-stu-id="26a8c-119">getDefaultView</span></span>](getDefaultView.md) 


