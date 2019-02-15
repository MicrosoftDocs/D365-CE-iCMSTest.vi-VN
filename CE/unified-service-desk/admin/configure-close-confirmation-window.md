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
# <a name="how-to-configure-close-confirmation-window-to-prevent-accidental-closure-of-unified-service-desk"></a><span data-ttu-id="1b022-103">How to configure close confirmation window to prevent accidental closure of Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="1b022-103">How to configure close confirmation window to prevent accidental closure of Unified Service Desk</span></span>

## <a name="accidental-closure-of-unified-service-desk"></a><span data-ttu-id="1b022-104">Accidental closure of Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="1b022-104">Accidental closure of Unified Service Desk</span></span>

<span data-ttu-id="1b022-105">A key measure at contact centers is customer satisfaction (CSAT).</span><span class="sxs-lookup"><span data-stu-id="1b022-105">A key measure at contact centers is customer satisfaction (CSAT).</span></span> <span data-ttu-id="1b022-106">Here, agents strive to increase their CSAT scores by solving customer problems.</span><span class="sxs-lookup"><span data-stu-id="1b022-106">Here, agents strive to increase their CSAT scores by solving customer problems.</span></span> <span data-ttu-id="1b022-107">If you are an agent working on an important case or attending to a customer call and you accidentally close [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], you could lose your unsaved work as well as the customer call.</span><span class="sxs-lookup"><span data-stu-id="1b022-107">If you are an agent working on an important case or attending to a customer call and you accidentally close [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], you could lose your unsaved work as well as the customer call.</span></span> <span data-ttu-id="1b022-108">The sudden closure of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can impact your productivity and also lead to a low CSAT score.</span><span class="sxs-lookup"><span data-stu-id="1b022-108">The sudden closure of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can impact your productivity and also lead to a low CSAT score.</span></span> <span data-ttu-id="1b022-109">Preventing accidental closures of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is key for your business and customers.</span><span class="sxs-lookup"><span data-stu-id="1b022-109">Preventing accidental closures of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is key for your business and customers.</span></span> <span data-ttu-id="1b022-110">That's why we introduced the close confirmation window feature.</span><span class="sxs-lookup"><span data-stu-id="1b022-110">That's why we introduced the close confirmation window feature.</span></span> 

## <a name="how-to-prevent-accidental-closure-of-unified-service-desk"></a><span data-ttu-id="1b022-111">How to prevent accidental closure of Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="1b022-111">How to prevent accidental closure of Unified Service Desk</span></span>

<span data-ttu-id="1b022-112">To avoid the accidental closure of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], the close confirmation window displays a message asking you to confirm the closure before continuing.</span><span class="sxs-lookup"><span data-stu-id="1b022-112">To avoid the accidental closure of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], the close confirmation window displays a message asking you to confirm the closure before continuing.</span></span>  
  
  <span data-ttu-id="1b022-113">![Close confirmation window in Unified Service Desk](../../unified-service-desk/media/usd-close-confirm-window.PNG "Close confirmation window in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="1b022-113">![Close confirmation window in Unified Service Desk](../../unified-service-desk/media/usd-close-confirm-window.PNG "Close confirmation window in Unified Service Desk")</span></span>

> [!NOTE]
> <span data-ttu-id="1b022-114">By default, the close confirmation window is enabled.</span><span class="sxs-lookup"><span data-stu-id="1b022-114">By default, the close confirmation window is enabled.</span></span> <span data-ttu-id="1b022-115">To disable the close confirmation window, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] administrator must configure the **HideConfirmationDialog** option on the **Options** page and set it to **true**.</span><span class="sxs-lookup"><span data-stu-id="1b022-115">To disable the close confirmation window, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] administrator must configure the **HideConfirmationDialog** option on the **Options** page and set it to **true**.</span></span>

## <a name="enabledisable-close-confirmation-window"></a><span data-ttu-id="1b022-116">Enable/disable close confirmation window</span><span class="sxs-lookup"><span data-stu-id="1b022-116">Enable/disable close confirmation window</span></span>

1. <span data-ttu-id="1b022-117">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="1b022-117">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. <span data-ttu-id="1b022-118">Chọn **Tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="1b022-118">Choose **Options**.</span></span>  

4. <span data-ttu-id="1b022-119">click **New** on the **Active UII Options** page.</span><span class="sxs-lookup"><span data-stu-id="1b022-119">click **New** on the **Active UII Options** page.</span></span>

5. <span data-ttu-id="1b022-120">Choose **Others** for the **Global Option** field.</span><span class="sxs-lookup"><span data-stu-id="1b022-120">Choose **Others** for the **Global Option** field.</span></span>

6. <span data-ttu-id="1b022-121">Type **HideConfirmationDialog** for the **Name** field.</span><span class="sxs-lookup"><span data-stu-id="1b022-121">Type **HideConfirmationDialog** for the **Name** field.</span></span>

7. <span data-ttu-id="1b022-122">Specify the value in the **Value** field.</span><span class="sxs-lookup"><span data-stu-id="1b022-122">Specify the value in the **Value** field.</span></span> <span data-ttu-id="1b022-123">Specify **false** to enable and **true** to disable.</span><span class="sxs-lookup"><span data-stu-id="1b022-123">Specify **false** to enable and **true** to disable.</span></span>

8. <span data-ttu-id="1b022-124">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="1b022-124">Click **Save**.</span></span>

   <span data-ttu-id="1b022-125">![Enable/disable HideConfirmationDialog option](../../unified-service-desk/media/crm-usd-hideconfirmationdialog-option.PNG "Enable/disable HideConfirmationDialog option")</span><span class="sxs-lookup"><span data-stu-id="1b022-125">![Enable/disable HideConfirmationDialog option](../../unified-service-desk/media/crm-usd-hideconfirmationdialog-option.PNG "Enable/disable HideConfirmationDialog option")</span></span>

## <a name="test-the-configuration-of-close-confirmation-window"></a><span data-ttu-id="1b022-126">Test the configuration of close confirmation window</span><span class="sxs-lookup"><span data-stu-id="1b022-126">Test the configuration of close confirmation window</span></span>

1. <span data-ttu-id="1b022-127">Bắt đầu ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] bằng cách nhấp đúp vào các phím tắt ứng dụng trên máy tính của bạn.</span><span class="sxs-lookup"><span data-stu-id="1b022-127">Start the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client by double-clicking the application shortcut on your desktop.</span></span> <span data-ttu-id="1b022-128">More information: [Sign in to Unified Service Desk](../admin/connect-dynamics-365-instance-using-unified-service-desk-client.md#sign-in-to-unified-service-desk)</span><span class="sxs-lookup"><span data-stu-id="1b022-128">More information: [Sign in to Unified Service Desk](../admin/connect-dynamics-365-instance-using-unified-service-desk-client.md#sign-in-to-unified-service-desk)</span></span>

2. <span data-ttu-id="1b022-129">Select the **X** button to close [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="1b022-129">Select the **X** button to close [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].</span></span>
</br><span data-ttu-id="1b022-130">The close confirmation window appears, asking you to confirm the closure.</span><span class="sxs-lookup"><span data-stu-id="1b022-130">The close confirmation window appears, asking you to confirm the closure.</span></span>

3. <span data-ttu-id="1b022-131">Choose **Yes** to close [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] or **No** to stay, save the changes, and continue working.</span><span class="sxs-lookup"><span data-stu-id="1b022-131">Choose **Yes** to close [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] or **No** to stay, save the changes, and continue working.</span></span>

<span data-ttu-id="1b022-132">![Close Confirmation window](../../unified-service-desk/media/usd-test-close-window.PNG "Close Confirmation window")</span><span class="sxs-lookup"><span data-stu-id="1b022-132">![Close Confirmation window](../../unified-service-desk/media/usd-test-close-window.PNG "Close Confirmation window")</span></span>

## <a name="see-also"></a><span data-ttu-id="1b022-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1b022-133">See also</span></span>

[<span data-ttu-id="1b022-134">Manage Options for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="1b022-134">Manage Options for Unified Service Desk</span></span>](../../unified-service-desk/admin/manage-options-unified-service-desk.md) 
