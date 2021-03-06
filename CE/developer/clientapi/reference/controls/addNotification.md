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
# <a name="addnotification-client-api-reference"></a>addNotification (Client API reference)

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

Displays an error or recommendation notification for a control, and lets you specify actions to execute based on the notification. When you specify an error type of notification, a red "X" icon appears next to the control. When you specify a recommendation type of notification, an "i" icon appears next to the control. On Dynamics 365 for Customer Engagement apps mobile clients, tapping on the icon will display the message, and let you perform the configured action by clicking the **Apply** button or dismiss the message. 

## <a name="control-types-supported"></a>Control types supported

Tất cả

## <a name="syntax"></a>Cú pháp

`formContext.getControl(arg).addNotification(notification);`

## <a name="parameters"></a>Tham số

<table style="width:100%">
<tr>
<th>Tên</th>
<th>Loại</th>
<th>Bắt buộc</th>
<th>Mô tả</th>
</tr>
<tr>
<td>notification</td>
<td>Đối tượng</td>
<td>Có</td>
<td>The notification to add. The object contains the following attributes:
<ul>
<li><b>actions</b>: (Optional) Array of objects. A collection of objects with the following attributes:
<ul>
<li><b>message</b>: (Optional) String. The body message of the notification to be displayed to the user. Limit your message to 100 characters for optimal user experience.</li>
<li><b>actions</b>: (Optional) Array of functions. The corresponding actions for the message.</li>
</ul>
<li><b>messages</b>: Array of Strings. The message to display in the notification. In the current release, only the first message specified in this array will be displayed. The string that you specify here appears as bold text in the notification, and is typically used for title or subject of the notification. You should limit your message to 50 characters for optimal user experience.</li>
<li><b>notificationLevel</b>: String. Defines the type of notification. Valid values are ERROR or RECOMMENDATION.</li>
<li><b>uniqueId</b>: String. The ID to use to clear this notification when using the <b>clearNotification</b> method.</li>
</ul></td>
</tr>

</table>

## <a name="return-value"></a>Giá trị trả lại

**Type**: Boolean

**Description**: Indicates whether the method succeeded.


## <a name="remarks"></a>Chú thích

The **addNotification** method displays a notification with the messages you specified and two standard buttons: **Apply** and **Dismiss**. Clicking **Apply** executes the action you define; clicking **Dismiss** closes the notification message. 

## <a name="example"></a>Ví dụ

The following sample code displays a notification on the **Account Name** field of the account form to set the **Ticker Symbol** if the **Account Name** field contains "Microsoft", and the ticker symbol is not already set to "MSFT". Clicking **Apply** in the notification will set the **Ticker Symbol** field to "MSFT".

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

### <a name="related-topics"></a>Chủ đề liên quan

[clearNotification](clearNotification.md)

[setNotification](setNotification.md)
