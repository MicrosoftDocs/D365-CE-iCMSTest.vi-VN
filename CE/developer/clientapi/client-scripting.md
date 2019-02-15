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
# <a name="client-scripting-in-customer-engagement-using-javascript"></a>Client scripting in Customer Engagement using JavaScript

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

Client-side scripting using JavaScript is one of the ways to apply custom business process logic for displaying data on a form in Customer Engagement. 

> [!NOTE]
> You can also use business rules, which provides a way for someone who does not know JavaScript and is not a developer, to apply business process logic in a form. Thông tin khác: [Tạo quy tắc công việc và đề xuất để áp dụng lô-gic trong biểu mẫu](../../customize/create-business-rules-recommendations-apply-logic-form.md)  

Forms in Customer Engagement help display data to the user. A form in Customer Engagement can contain items such as fields, a quick form, or a grid. An [event](events-forms-grids.md) occurs in Customer Engagement forms whenever:
- A form loads
- Data is changed in a field or an item within the form
- Data is saved in a form

You can attach your JavaScript code to "react" to these events so that your code gets executed when the event occurs on the form. You attach your JavaScript code (scripts) to these events by using a [Script web resource](../script-jscript-web-resources.md) in Customer Engagement. 

Customer Engagement provides you a rich set of **client APIs** to interact with form objects and events to control what and when to display on a form.

> [!NOTE]
> Some client APIs are deprecated in the current release of Dynamics 365 for Customer Engagement apps. Ensure that you are aware of these APIs as you write your client-side code for Customer Engagement. More information: [Deprecated client APIs](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated)

## <a name="get-started"></a>Bắt đầu

[Events in forms and grids](events-forms-grids.md)

[Understand the Client API object model](understand-clientapi-object-model.md)

[Walkthrough: Write your first client script](walkthrough-write-your-first-client-script.md)

## <a name="reference"></a>Tham chiếu

[Tham chiếu API máy khách](reference.md)


## <a name="related-topics"></a>Chủ đề liên quan

[Web resources for Customer Engagement](../web-resources.md)

[Tùy chỉnh lệnh và ru băng](../customize-dev/customize-commands-ribbon.md)
