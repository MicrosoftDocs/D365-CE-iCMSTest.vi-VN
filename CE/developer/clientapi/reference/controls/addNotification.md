---
title: addNotification (Client API reference) in Dynamics 365 for Customer Engagement apps| MicrosoftDocs
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
ms.openlocfilehash: b082abbfd3fd05a96ec5527f11e823f53eb4c350
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387583"
---
# <a name="addnotification-client-api-reference"></a><span data-ttu-id="19b6d-102">addNotification (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="19b6d-102">addNotification (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="19b6d-103">Displays an error or recommendation notification for a control, and lets you specify actions to execute based on the notification.</span><span class="sxs-lookup"><span data-stu-id="19b6d-103">Displays an error or recommendation notification for a control, and lets you specify actions to execute based on the notification.</span></span> <span data-ttu-id="19b6d-104">When you specify an error type of notification, a red "X" icon appears next to the control.</span><span class="sxs-lookup"><span data-stu-id="19b6d-104">When you specify an error type of notification, a red "X" icon appears next to the control.</span></span> <span data-ttu-id="19b6d-105">When you specify a recommendation type of notification, an "i" icon appears next to the control.</span><span class="sxs-lookup"><span data-stu-id="19b6d-105">When you specify a recommendation type of notification, an "i" icon appears next to the control.</span></span> <span data-ttu-id="19b6d-106">On Dynamics 365 for Customer Engagement apps mobile clients, tapping on the icon will display the message, and let you perform the configured action by clicking the **Apply** button or dismiss the message.</span><span class="sxs-lookup"><span data-stu-id="19b6d-106">On Dynamics 365 for Customer Engagement apps mobile clients, tapping on the icon will display the message, and let you perform the configured action by clicking the **Apply** button or dismiss the message.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="19b6d-107">Control types supported</span><span class="sxs-lookup"><span data-stu-id="19b6d-107">Control types supported</span></span>

<span data-ttu-id="19b6d-108">Tất cả</span><span class="sxs-lookup"><span data-stu-id="19b6d-108">All</span></span>

## <a name="syntax"></a><span data-ttu-id="19b6d-109">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="19b6d-109">Syntax</span></span>

`formContext.getControl(arg).addNotification(notification);`

## <a name="parameters"></a><span data-ttu-id="19b6d-110">Tham số</span><span class="sxs-lookup"><span data-stu-id="19b6d-110">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="19b6d-111">Tên</span><span class="sxs-lookup"><span data-stu-id="19b6d-111">Name</span></span></th>
<th><span data-ttu-id="19b6d-112">Loại</span><span class="sxs-lookup"><span data-stu-id="19b6d-112">Type</span></span></th>
<th><span data-ttu-id="19b6d-113">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="19b6d-113">Required</span></span></th>
<th><span data-ttu-id="19b6d-114">Mô tả</span><span class="sxs-lookup"><span data-stu-id="19b6d-114">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="19b6d-115">notification</span><span class="sxs-lookup"><span data-stu-id="19b6d-115">notification</span></span></td>
<td><span data-ttu-id="19b6d-116">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="19b6d-116">Object</span></span></td>
<td><span data-ttu-id="19b6d-117">Có</span><span class="sxs-lookup"><span data-stu-id="19b6d-117">Yes</span></span></td>
<td><span data-ttu-id="19b6d-118">The notification to add.</span><span class="sxs-lookup"><span data-stu-id="19b6d-118">The notification to add.</span></span> <span data-ttu-id="19b6d-119">The object contains the following attributes:</span><span class="sxs-lookup"><span data-stu-id="19b6d-119">The object contains the following attributes:</span></span>
<ul>
<li><span data-ttu-id="19b6d-120"><b>actions</b>: (Optional) Array of objects.</span><span class="sxs-lookup"><span data-stu-id="19b6d-120"><b>actions</b>: (Optional) Array of objects.</span></span> <span data-ttu-id="19b6d-121">A collection of objects with the following attributes:</span><span class="sxs-lookup"><span data-stu-id="19b6d-121">A collection of objects with the following attributes:</span></span>
<ul>
<li><span data-ttu-id="19b6d-122"><b>message</b>: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="19b6d-122"><b>message</b>: (Optional) String.</span></span> <span data-ttu-id="19b6d-123">The body message of the notification to be displayed to the user.</span><span class="sxs-lookup"><span data-stu-id="19b6d-123">The body message of the notification to be displayed to the user.</span></span> <span data-ttu-id="19b6d-124">Limit your message to 100 characters for optimal user experience.</span><span class="sxs-lookup"><span data-stu-id="19b6d-124">Limit your message to 100 characters for optimal user experience.</span></span></li>
<li><span data-ttu-id="19b6d-125"><b>actions</b>: (Optional) Array of functions.</span><span class="sxs-lookup"><span data-stu-id="19b6d-125"><b>actions</b>: (Optional) Array of functions.</span></span> <span data-ttu-id="19b6d-126">The corresponding actions for the message.</span><span class="sxs-lookup"><span data-stu-id="19b6d-126">The corresponding actions for the message.</span></span></li>
</ul>
<li><span data-ttu-id="19b6d-127"><b>messages</b>: Array of Strings.</span><span class="sxs-lookup"><span data-stu-id="19b6d-127"><b>messages</b>: Array of Strings.</span></span> <span data-ttu-id="19b6d-128">The message to display in the notification.</span><span class="sxs-lookup"><span data-stu-id="19b6d-128">The message to display in the notification.</span></span> <span data-ttu-id="19b6d-129">In the current release, only the first message specified in this array will be displayed.</span><span class="sxs-lookup"><span data-stu-id="19b6d-129">In the current release, only the first message specified in this array will be displayed.</span></span> <span data-ttu-id="19b6d-130">The string that you specify here appears as bold text in the notification, and is typically used for title or subject of the notification.</span><span class="sxs-lookup"><span data-stu-id="19b6d-130">The string that you specify here appears as bold text in the notification, and is typically used for title or subject of the notification.</span></span> <span data-ttu-id="19b6d-131">You should limit your message to 50 characters for optimal user experience.</span><span class="sxs-lookup"><span data-stu-id="19b6d-131">You should limit your message to 50 characters for optimal user experience.</span></span></li>
<li><span data-ttu-id="19b6d-132"><b>notificationLevel</b>: String.</span><span class="sxs-lookup"><span data-stu-id="19b6d-132"><b>notificationLevel</b>: String.</span></span> <span data-ttu-id="19b6d-133">Defines the type of notification.</span><span class="sxs-lookup"><span data-stu-id="19b6d-133">Defines the type of notification.</span></span> <span data-ttu-id="19b6d-134">Valid values are ERROR or RECOMMENDATION.</span><span class="sxs-lookup"><span data-stu-id="19b6d-134">Valid values are ERROR or RECOMMENDATION.</span></span></li>
<li><span data-ttu-id="19b6d-135"><b>uniqueId</b>: String.</span><span class="sxs-lookup"><span data-stu-id="19b6d-135"><b>uniqueId</b>: String.</span></span> <span data-ttu-id="19b6d-136">The ID to use to clear this notification when using the <b>clearNotification</b> method.</span><span class="sxs-lookup"><span data-stu-id="19b6d-136">The ID to use to clear this notification when using the <b>clearNotification</b> method.</span></span></li>
</ul></td>
</tr>

</table>

## <a name="return-value"></a><span data-ttu-id="19b6d-137">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="19b6d-137">Return Value</span></span>

<span data-ttu-id="19b6d-138">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="19b6d-138">**Type**: Boolean</span></span>

<span data-ttu-id="19b6d-139">**Description**: Indicates whether the method succeeded.</span><span class="sxs-lookup"><span data-stu-id="19b6d-139">**Description**: Indicates whether the method succeeded.</span></span>


## <a name="remarks"></a><span data-ttu-id="19b6d-140">Chú thích</span><span class="sxs-lookup"><span data-stu-id="19b6d-140">Remarks</span></span>

<span data-ttu-id="19b6d-141">The **addNotification** method displays a notification with the messages you specified and two standard buttons: **Apply** and **Dismiss**.</span><span class="sxs-lookup"><span data-stu-id="19b6d-141">The **addNotification** method displays a notification with the messages you specified and two standard buttons: **Apply** and **Dismiss**.</span></span> <span data-ttu-id="19b6d-142">Clicking **Apply** executes the action you define; clicking **Dismiss** closes the notification message.</span><span class="sxs-lookup"><span data-stu-id="19b6d-142">Clicking **Apply** executes the action you define; clicking **Dismiss** closes the notification message.</span></span> 

## <a name="example"></a><span data-ttu-id="19b6d-143">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="19b6d-143">Example</span></span>

<span data-ttu-id="19b6d-144">The following sample code displays a notification on the **Account Name** field of the account form to set the **Ticker Symbol** if the **Account Name** field contains "Microsoft", and the ticker symbol is not already set to "MSFT".</span><span class="sxs-lookup"><span data-stu-id="19b6d-144">The following sample code displays a notification on the **Account Name** field of the account form to set the **Ticker Symbol** if the **Account Name** field contains "Microsoft", and the ticker symbol is not already set to "MSFT".</span></span> <span data-ttu-id="19b6d-145">Clicking **Apply** in the notification will set the **Ticker Symbol** field to "MSFT".</span><span class="sxs-lookup"><span data-stu-id="19b6d-145">Clicking **Apply** in the notification will set the **Ticker Symbol** field to "MSFT".</span></span>

```JavaScript
function addTickerSymbolRecommendation(executionContext) {
    var formContext = executionContext.getFormContext();
    var myControl = formContext.getControl('name');
    var accountName = formContext.data.entity.attributes.get('name');
    var tickerSymbol = formContext.data.entity.attributes.get('tickersymbol');

    if (accountName.getValue() == 'Microsoft' && tickerSymbol.getValue() != 'MSFT') {
        var actionCollection = {
            message: 'Set the Ticker Symbol to MSFT?',
            actions: null
        };

        actionCollection.actions = [function () {
            tickerSymbol.setValue('MSFT');
            myControl.clearNotification('my_unique_id');
        }];

        myControl.addNotification({
            messages: ['Set Ticker Symbol'],
            notificationLevel: 'RECOMMENDATION',
            uniqueId: 'my_unique_id',
            actions: [actionCollection]
        });
    }
    else
        console.log("Notification not set");
}
```

### <a name="related-topics"></a><span data-ttu-id="19b6d-146">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="19b6d-146">Related topics</span></span>

[<span data-ttu-id="19b6d-147">clearNotification</span><span class="sxs-lookup"><span data-stu-id="19b6d-147">clearNotification</span></span>](clearNotification.md)

[<span data-ttu-id="19b6d-148">setNotification</span><span class="sxs-lookup"><span data-stu-id="19b6d-148">setNotification</span></span>](setNotification.md)
