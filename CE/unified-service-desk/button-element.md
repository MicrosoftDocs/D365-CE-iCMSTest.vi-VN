---
title: ButtonElement | MicrosoftDocs
description: The topic explains about <ButtonElement> element syntax and the elements, which is one of the binding elements of the WebDDA.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: a67be8bc-6d28-4c99-a62a-397169a92eec
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 33ab4a99c2931b678ef70db9211b9241d116873c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387194"
---
# <a name="buttonelement"></a><span data-ttu-id="6ad57-103">ButtonElement</span><span class="sxs-lookup"><span data-stu-id="6ad57-103">ButtonElement</span></span>
<span data-ttu-id="6ad57-104">`<ButtonElement>` là một trong các yếu tố liên kết của WebDDA.</span><span class="sxs-lookup"><span data-stu-id="6ad57-104">`<ButtonElement>` is one of the binding elements of WebDDA.</span></span> <span data-ttu-id="6ad57-105">Chủ đề này mô tả cú pháp và các yếu tố của `<ButtonElement>`</span><span class="sxs-lookup"><span data-stu-id="6ad57-105">This topic describes the syntax and the elements of `<ButtonElement>`</span></span>  
  
## <a name="buttonelement-syntax"></a><span data-ttu-id="6ad57-106">\<ButtonElement> syntax</span><span class="sxs-lookup"><span data-stu-id="6ad57-106">\<ButtonElement> syntax</span></span>  
 <span data-ttu-id="6ad57-107">Yếu tố `<ButtonElement>` liên kết kiểm soát có tên với yếu tố `<button/> HTML`.</span><span class="sxs-lookup"><span data-stu-id="6ad57-107">The `<ButtonElement>` element associates a named control to a `<button/> HTML` element.</span></span> <span data-ttu-id="6ad57-108">Đoạn mã sau hiển thị cách sử dụng `<ButtonElement>`:</span><span class="sxs-lookup"><span data-stu-id="6ad57-108">The following code snippet shows how `<ButtonElement>` is used:</span></span>  
  
```xml  
<ButtonElement name="control name">  
Search Path Elements  
</ButtonElement>  
  
```  
  
## <a name="elements-of-buttonelement"></a><span data-ttu-id="6ad57-109">Elements of \<ButtonElement></span><span class="sxs-lookup"><span data-stu-id="6ad57-109">Elements of \<ButtonElement></span></span>  
 <span data-ttu-id="6ad57-110">Bảng sau mô tả các yếu tố của `<ButtonElement>`</span><span class="sxs-lookup"><span data-stu-id="6ad57-110">The following table describes the elements of `<ButtonElement>`</span></span>  
  
|<span data-ttu-id="6ad57-111">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="6ad57-111">Element</span></span>|<span data-ttu-id="6ad57-112">Mô tả</span><span class="sxs-lookup"><span data-stu-id="6ad57-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6ad57-113">FindControl</span><span class="sxs-lookup"><span data-stu-id="6ad57-113">FindControl</span></span>|<span data-ttu-id="6ad57-114">Trả về `True` hoặc `False` tùy theo kiểm soát có thể được tìm thấy trên UI hay không.</span><span class="sxs-lookup"><span data-stu-id="6ad57-114">Returns `True` or `False` depending on whether the control can be found on the UI.</span></span>|  
|<span data-ttu-id="6ad57-115">GetControlValue</span><span class="sxs-lookup"><span data-stu-id="6ad57-115">GetControlValue</span></span>|<span data-ttu-id="6ad57-116">Trả về văn bản URL.</span><span class="sxs-lookup"><span data-stu-id="6ad57-116">Returns the URL text.</span></span>|  
|<span data-ttu-id="6ad57-117">SetControlValue</span><span class="sxs-lookup"><span data-stu-id="6ad57-117">SetControlValue</span></span>|<span data-ttu-id="6ad57-118">Bỏ một ngoại lệ `UnsupportedControlOperation`.</span><span class="sxs-lookup"><span data-stu-id="6ad57-118">Throws an `UnsupportedControlOperation` exception.</span></span>|  
|<span data-ttu-id="6ad57-119">ExecuteControlAction</span><span class="sxs-lookup"><span data-stu-id="6ad57-119">ExecuteControlAction</span></span>|<span data-ttu-id="6ad57-120">Thực hiện một lệnh `Click()` trên kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="6ad57-120">Executes a `Click()` command on the control.</span></span>|  
  
### <a name="see-also"></a><span data-ttu-id="6ad57-121">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6ad57-121">See also</span></span>  
 <span data-ttu-id="6ad57-122">[WebDDA](../unified-service-desk/web-dda.md) </span><span class="sxs-lookup"><span data-stu-id="6ad57-122">[WebDDA](../unified-service-desk/web-dda.md) </span></span>  
 [<span data-ttu-id="6ad57-123">Use Data Driven Adapters (DDAs)</span><span class="sxs-lookup"><span data-stu-id="6ad57-123">Use Data Driven Adapters (DDAs)</span></span>](../unified-service-desk/use-data-driven-adapters-ddas.md)
