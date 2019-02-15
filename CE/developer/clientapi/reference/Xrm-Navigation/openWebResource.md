---
title: openWebResource (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 07/13/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 798dc921-1e80-42bc-b8ca-2056728bcba4
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6221dcf64ee624f0ba6f2def70f46c9898489ffb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386843"
---
# <a name="openwebresource-client-api-reference"></a><span data-ttu-id="d2c83-102">openWebResource (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="d2c83-102">openWebResource (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openWebResource-description.md](./includes/openWebResource-description.md)]

## <a name="syntax"></a><span data-ttu-id="d2c83-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="d2c83-103">Syntax</span></span>

`Xrm.Navigation.openWebResource(webResourceName,windowOptions,data)`

## <a name="parameters"></a><span data-ttu-id="d2c83-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="d2c83-104">Parameters</span></span>

|<span data-ttu-id="d2c83-105">Tên</span><span class="sxs-lookup"><span data-stu-id="d2c83-105">Name</span></span> |<span data-ttu-id="d2c83-106">Loại</span><span class="sxs-lookup"><span data-stu-id="d2c83-106">Type</span></span> |<span data-ttu-id="d2c83-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="d2c83-107">Required</span></span> |<span data-ttu-id="d2c83-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="d2c83-108">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="d2c83-109">webResourceName</span><span class="sxs-lookup"><span data-stu-id="d2c83-109">webResourceName</span></span>|<span data-ttu-id="d2c83-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="d2c83-110">String</span></span>|<span data-ttu-id="d2c83-111">Có</span><span class="sxs-lookup"><span data-stu-id="d2c83-111">Yes</span></span>|<span data-ttu-id="d2c83-112">Name of the HTML web resource to open.</span><span class="sxs-lookup"><span data-stu-id="d2c83-112">Name of the HTML web resource to open.</span></span>|
|<span data-ttu-id="d2c83-113">windowOptions</span><span class="sxs-lookup"><span data-stu-id="d2c83-113">windowOptions</span></span>|<span data-ttu-id="d2c83-114">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="d2c83-114">Object</span></span>|<span data-ttu-id="d2c83-115">Không</span><span class="sxs-lookup"><span data-stu-id="d2c83-115">No</span></span>|<span data-ttu-id="d2c83-116">Window options for opening the web resource.</span><span class="sxs-lookup"><span data-stu-id="d2c83-116">Window options for opening the web resource.</span></span> <span data-ttu-id="d2c83-117">The object contains the following attributes:</span><span class="sxs-lookup"><span data-stu-id="d2c83-117">The object contains the following attributes:</span></span><br/><span data-ttu-id="d2c83-118">- **height**: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="d2c83-118">- **height**: (Optional) Number.</span></span> <span data-ttu-id="d2c83-119">Height of the window to open in pixels.</span><span class="sxs-lookup"><span data-stu-id="d2c83-119">Height of the window to open in pixels.</span></span><br/><span data-ttu-id="d2c83-120">- **width**: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="d2c83-120">- **width**: (Optional) Number.</span></span> <span data-ttu-id="d2c83-121">Width of the window to open in pixels.</span><span class="sxs-lookup"><span data-stu-id="d2c83-121">Width of the window to open in pixels.</span></span>|
|<span data-ttu-id="d2c83-122">dữ liệu</span><span class="sxs-lookup"><span data-stu-id="d2c83-122">data</span></span>|<span data-ttu-id="d2c83-123">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="d2c83-123">String</span></span>|<span data-ttu-id="d2c83-124">Không</span><span class="sxs-lookup"><span data-stu-id="d2c83-124">No</span></span>|<span data-ttu-id="d2c83-125">Data to be passed into the data parameter.</span><span class="sxs-lookup"><span data-stu-id="d2c83-125">Data to be passed into the data parameter.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d2c83-126">Chú thích</span><span class="sxs-lookup"><span data-stu-id="d2c83-126">Remarks</span></span>

<span data-ttu-id="d2c83-127">You must use this method to display web resources instead of the deprecated [Xrm.Utility.openWebResource](https://msdn.microsoft.com/library/jj602956.aspx#BKMK_OpenWebResource) method.</span><span class="sxs-lookup"><span data-stu-id="d2c83-127">You must use this method to display web resources instead of the deprecated [Xrm.Utility.openWebResource](https://msdn.microsoft.com/library/jj602956.aspx#BKMK_OpenWebResource) method.</span></span>

<span data-ttu-id="d2c83-128">An HTML web resource can accept the parameter values described in [Pass parameters to HTML web resources](../../../webpage-html-web-resources.md#BKMK_PassingParametersToWebResources).</span><span class="sxs-lookup"><span data-stu-id="d2c83-128">An HTML web resource can accept the parameter values described in [Pass parameters to HTML web resources](../../../webpage-html-web-resources.md#BKMK_PassingParametersToWebResources).</span></span> <span data-ttu-id="d2c83-129">This function only provides for passing in the optional data parameter.</span><span class="sxs-lookup"><span data-stu-id="d2c83-129">This function only provides for passing in the optional data parameter.</span></span> <span data-ttu-id="d2c83-130">To pass values for the other valid parameters, you must append them to the `webResourceName` parameter.</span><span class="sxs-lookup"><span data-stu-id="d2c83-130">To pass values for the other valid parameters, you must append them to the `webResourceName` parameter.</span></span>

> [!NOTE]
> <span data-ttu-id="d2c83-131">The **Xrm** object isn’t available in HTML web resources.</span><span class="sxs-lookup"><span data-stu-id="d2c83-131">The **Xrm** object isn’t available in HTML web resources.</span></span> <span data-ttu-id="d2c83-132">Therefore, scripts containing `Xrm.*` methods aren’t supported in HTML web resources.</span><span class="sxs-lookup"><span data-stu-id="d2c83-132">Therefore, scripts containing `Xrm.*` methods aren’t supported in HTML web resources.</span></span> <span data-ttu-id="d2c83-133">`parent.Xrm.*` will work if the HTML web resource is loaded in a form container.</span><span class="sxs-lookup"><span data-stu-id="d2c83-133">`parent.Xrm.*` will work if the HTML web resource is loaded in a form container.</span></span> <span data-ttu-id="d2c83-134">However, for other places, such as loading an HTML web resource as part of the SiteMap, `parent.Xrm.*` also won’t work.</span><span class="sxs-lookup"><span data-stu-id="d2c83-134">However, for other places, such as loading an HTML web resource as part of the SiteMap, `parent.Xrm.*` also won’t work.</span></span> <span data-ttu-id="d2c83-135">More information: [GetGlobalContext function and ClientGlobalContext.js.aspx](../GetGlobalContext-ClientGlobalContext.js.aspx.md)</span><span class="sxs-lookup"><span data-stu-id="d2c83-135">More information: [GetGlobalContext function and ClientGlobalContext.js.aspx](../GetGlobalContext-ClientGlobalContext.js.aspx.md)</span></span>



## <a name="examples"></a><span data-ttu-id="d2c83-136">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d2c83-136">Examples</span></span>

- <span data-ttu-id="d2c83-137">Open an HTML web resource named “new_webResource.htm”:</span><span class="sxs-lookup"><span data-stu-id="d2c83-137">Open an HTML web resource named “new_webResource.htm”:</span></span>
   
   `Xrm.Navigation.openWebResource("new_webResource.htm");`

- <span data-ttu-id="d2c83-138">Open an HTML web resource, setting the windowOptions:</span><span class="sxs-lookup"><span data-stu-id="d2c83-138">Open an HTML web resource, setting the windowOptions:</span></span>

  ```
  var windowOptions = { height: 400, width: 400 }
  Xrm.Navigation.openWebResource("new_webResource.htm",windowOptions);
  ```

- <span data-ttu-id="d2c83-139">Open an HTML web resource including a single item of data for the `data` parameter</span><span class="sxs-lookup"><span data-stu-id="d2c83-139">Open an HTML web resource including a single item of data for the `data` parameter</span></span>

  `Xrm.Navigation.openWebResource("new_webResource.htm",null,"dataItemValue");`

  ### <a name="related-topics"></a><span data-ttu-id="d2c83-140">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="d2c83-140">Related topics</span></span>

[<span data-ttu-id="d2c83-141">Xrm.Navigation</span><span class="sxs-lookup"><span data-stu-id="d2c83-141">Xrm.Navigation</span></span>](../xrm-navigation.md)

