---
title: Configure close confirmation window to prevent accidental closure of Unified Service Desk | MicrosoftDocs
description: Learn to configure the close confirmation window to prevent the accidental closure of Unified Service Desk.
keywords: ''
ms.date: 08/17/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD, dyn365-admin
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 30FC4B2F-99BD-4CB9-8792-C6062FC051C3
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
monikerRange: '>=dynamics-usd-4'
ms.openlocfilehash: e7b6433d9c255a11ab4ac487f322b8a09d3ccaa2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382422"
---
# <a name="how-to-configure-close-confirmation-window-to-prevent-accidental-closure-of-unified-service-desk"></a>How to configure close confirmation window to prevent accidental closure of Unified Service Desk

## <a name="accidental-closure-of-unified-service-desk"></a>Accidental closure of Unified Service Desk

A key measure at contact centers is customer satisfaction (CSAT). Here, agents strive to increase their CSAT scores by solving customer problems. If you are an agent working on an important case or attending to a customer call and you accidentally close [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], you could lose your unsaved work as well as the customer call. The sudden closure of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can impact your productivity and also lead to a low CSAT score. Preventing accidental closures of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is key for your business and customers. That's why we introduced the close confirmation window feature. 

## <a name="how-to-prevent-accidental-closure-of-unified-service-desk"></a>How to prevent accidental closure of Unified Service Desk

To avoid the accidental closure of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], the close confirmation window displays a message asking you to confirm the closure before continuing.  
  
  ![Close confirmation window in Unified Service Desk](../../unified-service-desk/media/usd-close-confirm-window.PNG "Close confirmation window in Unified Service Desk")

> [!NOTE]
> By default, the close confirmation window is enabled. To disable the close confirmation window, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] administrator must configure the **HideConfirmationDialog** option on the **Options** page and set it to **true**.

## <a name="enabledisable-close-confirmation-window"></a>Enable/disable close confirmation window

1. Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. Chọn **Tùy chọn**.  

4. click **New** on the **Active UII Options** page.

5. Choose **Others** for the **Global Option** field.

6. Type **HideConfirmationDialog** for the **Name** field.

7. Specify the value in the **Value** field. Specify **false** to enable and **true** to disable.

8. Bấm vào **Lưu**.

   ![Enable/disable HideConfirmationDialog option](../../unified-service-desk/media/crm-usd-hideconfirmationdialog-option.PNG "Enable/disable HideConfirmationDialog option")

## <a name="test-the-configuration-of-close-confirmation-window"></a>Test the configuration of close confirmation window

1. Bắt đầu ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] bằng cách nhấp đúp vào các phím tắt ứng dụng trên máy tính của bạn. More information: [Sign in to Unified Service Desk](../admin/connect-dynamics-365-instance-using-unified-service-desk-client.md#sign-in-to-unified-service-desk)

2. Select the **X** button to close [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].
</br>The close confirmation window appears, asking you to confirm the closure.

3. Choose **Yes** to close [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] or **No** to stay, save the changes, and continue working.

![Close Confirmation window](../../unified-service-desk/media/usd-test-close-window.PNG "Close Confirmation window")

## <a name="see-also"></a>Xem thêm

[Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md) 
