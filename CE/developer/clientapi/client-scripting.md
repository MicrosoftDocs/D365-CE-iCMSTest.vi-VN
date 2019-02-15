---
title: Client scripting in Customer Engagement using JavaScript | MicrosoftDocs
description: Learn how to use Client API in Customer Engagement to apply custom business process logic for displaying data on a form.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 16271bd8-cfa8-4a7f-802a-60fbff7c3722
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5aeb97ac3ec355ac7cecd86fad6c6fcc8184ddca
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386595"
---
# <a name="client-scripting-in-customer-engagement-using-javascript"></a><span data-ttu-id="f093f-103">Client scripting in Customer Engagement using JavaScript</span><span class="sxs-lookup"><span data-stu-id="f093f-103">Client scripting in Customer Engagement using JavaScript</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f093f-104">Client-side scripting using JavaScript is one of the ways to apply custom business process logic for displaying data on a form in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="f093f-104">Client-side scripting using JavaScript is one of the ways to apply custom business process logic for displaying data on a form in Customer Engagement.</span></span> 

> [!NOTE]
> <span data-ttu-id="f093f-105">You can also use business rules, which provides a way for someone who does not know JavaScript and is not a developer, to apply business process logic in a form.</span><span class="sxs-lookup"><span data-stu-id="f093f-105">You can also use business rules, which provides a way for someone who does not know JavaScript and is not a developer, to apply business process logic in a form.</span></span> <span data-ttu-id="f093f-106">Thông tin khác: [Tạo quy tắc công việc và đề xuất để áp dụng lô-gic trong biểu mẫu](../../customize/create-business-rules-recommendations-apply-logic-form.md)</span><span class="sxs-lookup"><span data-stu-id="f093f-106">More information: [Create business rules and recommendations to apply logic in a form](../../customize/create-business-rules-recommendations-apply-logic-form.md)</span></span>  

<span data-ttu-id="f093f-107">Forms in Customer Engagement help display data to the user.</span><span class="sxs-lookup"><span data-stu-id="f093f-107">Forms in Customer Engagement help display data to the user.</span></span> <span data-ttu-id="f093f-108">A form in Customer Engagement can contain items such as fields, a quick form, or a grid.</span><span class="sxs-lookup"><span data-stu-id="f093f-108">A form in Customer Engagement can contain items such as fields, a quick form, or a grid.</span></span> <span data-ttu-id="f093f-109">An [event](events-forms-grids.md) occurs in Customer Engagement forms whenever:</span><span class="sxs-lookup"><span data-stu-id="f093f-109">An [event](events-forms-grids.md) occurs in Customer Engagement forms whenever:</span></span>
- <span data-ttu-id="f093f-110">A form loads</span><span class="sxs-lookup"><span data-stu-id="f093f-110">A form loads</span></span>
- <span data-ttu-id="f093f-111">Data is changed in a field or an item within the form</span><span class="sxs-lookup"><span data-stu-id="f093f-111">Data is changed in a field or an item within the form</span></span>
- <span data-ttu-id="f093f-112">Data is saved in a form</span><span class="sxs-lookup"><span data-stu-id="f093f-112">Data is saved in a form</span></span>

<span data-ttu-id="f093f-113">You can attach your JavaScript code to "react" to these events so that your code gets executed when the event occurs on the form.</span><span class="sxs-lookup"><span data-stu-id="f093f-113">You can attach your JavaScript code to "react" to these events so that your code gets executed when the event occurs on the form.</span></span> <span data-ttu-id="f093f-114">You attach your JavaScript code (scripts) to these events by using a [Script web resource](../script-jscript-web-resources.md) in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="f093f-114">You attach your JavaScript code (scripts) to these events by using a [Script web resource](../script-jscript-web-resources.md) in Customer Engagement.</span></span> 

<span data-ttu-id="f093f-115">Customer Engagement provides you a rich set of **client APIs** to interact with form objects and events to control what and when to display on a form.</span><span class="sxs-lookup"><span data-stu-id="f093f-115">Customer Engagement provides you a rich set of **client APIs** to interact with form objects and events to control what and when to display on a form.</span></span>

> [!NOTE]
> <span data-ttu-id="f093f-116">Some client APIs are deprecated in the current release of Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="f093f-116">Some client APIs are deprecated in the current release of Dynamics 365 for Customer Engagement apps.</span></span> <span data-ttu-id="f093f-117">Ensure that you are aware of these APIs as you write your client-side code for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="f093f-117">Ensure that you are aware of these APIs as you write your client-side code for Customer Engagement.</span></span> <span data-ttu-id="f093f-118">More information: [Deprecated client APIs](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated)</span><span class="sxs-lookup"><span data-stu-id="f093f-118">More information: [Deprecated client APIs](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated)</span></span>

## <a name="get-started"></a><span data-ttu-id="f093f-119">Bắt đầu</span><span class="sxs-lookup"><span data-stu-id="f093f-119">Get Started</span></span>

[<span data-ttu-id="f093f-120">Events in forms and grids</span><span class="sxs-lookup"><span data-stu-id="f093f-120">Events in forms and grids</span></span>](events-forms-grids.md)

[<span data-ttu-id="f093f-121">Understand the Client API object model</span><span class="sxs-lookup"><span data-stu-id="f093f-121">Understand the Client API object model</span></span>](understand-clientapi-object-model.md)

[<span data-ttu-id="f093f-122">Walkthrough: Write your first client script</span><span class="sxs-lookup"><span data-stu-id="f093f-122">Walkthrough: Write your first client script</span></span>](walkthrough-write-your-first-client-script.md)

## <a name="reference"></a><span data-ttu-id="f093f-123">Tham chiếu</span><span class="sxs-lookup"><span data-stu-id="f093f-123">Reference</span></span>

[<span data-ttu-id="f093f-124">Tham chiếu API máy khách</span><span class="sxs-lookup"><span data-stu-id="f093f-124">Client API reference</span></span>](reference.md)


## <a name="related-topics"></a><span data-ttu-id="f093f-125">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="f093f-125">Related topics</span></span>

[<span data-ttu-id="f093f-126">Web resources for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="f093f-126">Web resources for Customer Engagement</span></span>](../web-resources.md)

[<span data-ttu-id="f093f-127">Tùy chỉnh lệnh và ru băng</span><span class="sxs-lookup"><span data-stu-id="f093f-127">Customize commands and the ribbon</span></span>](../customize-dev/customize-commands-ribbon.md)
