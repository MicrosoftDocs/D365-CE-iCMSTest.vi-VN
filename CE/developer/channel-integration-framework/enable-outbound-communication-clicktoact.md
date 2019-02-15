---
title: How to enable outbound communication (ClickToAct) in Dynamics 365 Channel Integration Framework (CIF) | Microsoft Docs
description: Learn enable or configure outbound communication (ClickToAct) in Channel Integration Framework (CIF) for Microsoft Dynamics 365.
keywords: ''
ms.date: 12/10/2018
ms.service:
- dynamics-365-cross-app
ms.custom:
- dyn365-a11y
- dyn365-developer
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement Version 9.x
ms.assetid: E0E45AC7-E516-46B5-ADBC-77254CBA8A2F
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: 4899b337ef609c19680c40ef78f9ec5ee8fb2430
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385742"
---
# <a name="how-to-enable-outbound-communication-clicktoact-in-channel-integration-framework"></a><span data-ttu-id="a099f-103">How to enable outbound communication (ClickTOAct) in Channel Integration Framework?</span><span class="sxs-lookup"><span data-stu-id="a099f-103">How to enable outbound communication (ClickTOAct) in Channel Integration Framework?</span></span>

<span data-ttu-id="a099f-104">To enable outbound communication for your channel, you must perform the following:</span><span class="sxs-lookup"><span data-stu-id="a099f-104">To enable outbound communication for your channel, you must perform the following:</span></span>

- <span data-ttu-id="a099f-105">**Step 1:** In the channel provider configurations, set the **Enable Outbound Communication** field to **Yes**.</span><span class="sxs-lookup"><span data-stu-id="a099f-105">**Step 1:** In the channel provider configurations, set the **Enable Outbound Communication** field to **Yes**.</span></span>

- <span data-ttu-id="a099f-106">**Step 2:** In the Unified Interface form, add the **Channel communication control** to the **Phone** field for which you want to enable outbound communication (ClickToAct), and publish the customizations.</span><span class="sxs-lookup"><span data-stu-id="a099f-106">**Step 2:** In the Unified Interface form, add the **Channel communication control** to the **Phone** field for which you want to enable outbound communication (ClickToAct), and publish the customizations.</span></span>

- <span data-ttu-id="a099f-107">**Step 3:** Register the addhandler in your JavaScript code using `Microsoft.CIFramework.addHandler("onclicktoact", <handlerFunction>)`</span><span class="sxs-lookup"><span data-stu-id="a099f-107">**Step 3:** Register the addhandler in your JavaScript code using `Microsoft.CIFramework.addHandler("onclicktoact", <handlerFunction>)`</span></span> 

## <a name="step-1-set-the-enable-outbound-communication-field-value-in-the-channel-provider-configuration"></a><span data-ttu-id="a099f-108">Step 1: Set the Enable Outbound Communication field value in the channel provider configuration</span><span class="sxs-lookup"><span data-stu-id="a099f-108">Step 1: Set the Enable Outbound Communication field value in the channel provider configuration</span></span>

1. <span data-ttu-id="a099f-109">Sign-in to Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a099f-109">Sign-in to Dynamics 365.</span></span>

2. <span data-ttu-id="a099f-110">Select the drop-down button on the Dynamics 365 and select **Channel Integration Framework**.</span><span class="sxs-lookup"><span data-stu-id="a099f-110">Select the drop-down button on the Dynamics 365 and select **Channel Integration Framework**.</span></span>

3. <span data-ttu-id="a099f-111">Select a channel provider from the **Active Channel Providers** list.</span><span class="sxs-lookup"><span data-stu-id="a099f-111">Select a channel provider from the **Active Channel Providers** list.</span></span>

4. <span data-ttu-id="a099f-112">Set the **Enable Outbound Communication** field to **Yes**, and save the changes.</span><span class="sxs-lookup"><span data-stu-id="a099f-112">Set the **Enable Outbound Communication** field to **Yes**, and save the changes.</span></span>

## <a name="step-2-add-the-channel-communication-control-to-the-unified-interface-form"></a><span data-ttu-id="a099f-113">Step 2: Add the Channel Communication Control to the Unified Interface form</span><span class="sxs-lookup"><span data-stu-id="a099f-113">Step 2: Add the Channel Communication Control to the Unified Interface form</span></span>

<span data-ttu-id="a099f-114">You can add the Channel Communication Control based on your organization and business requirements.</span><span class="sxs-lookup"><span data-stu-id="a099f-114">You can add the Channel Communication Control based on your organization and business requirements.</span></span> <span data-ttu-id="a099f-115">The steps mentioned below illustrate adding the **Channel Communication Control** for the **Contact** form of **Main** type under the **Contact** entity.</span><span class="sxs-lookup"><span data-stu-id="a099f-115">The steps mentioned below illustrate adding the **Channel Communication Control** for the **Contact** form of **Main** type under the **Contact** entity.</span></span>

1. <span data-ttu-id="a099f-116">Sign-in to Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a099f-116">Sign-in to Dynamics 365.</span></span>

2. <span data-ttu-id="a099f-117">Chuyển tới **Thiết đặt** > **Tùy chỉnh**.</span><span class="sxs-lookup"><span data-stu-id="a099f-117">Go to **Settings** > **Customizations**.</span></span>

3. <span data-ttu-id="a099f-118">Expand **Entites** > **Contact** and select **Forms**.</span><span class="sxs-lookup"><span data-stu-id="a099f-118">Expand **Entites** > **Contact** and select **Forms**.</span></span><br>
<span data-ttu-id="a099f-119">![Expand contact entity and select forms](media/contact-entity-forms.PNG "Expand contact entity and select forms")</span><span class="sxs-lookup"><span data-stu-id="a099f-119">![Expand contact entity and select forms](media/contact-entity-forms.PNG "Expand contact entity and select forms")</span></span>

4. <span data-ttu-id="a099f-120">Select the **Contact** form of the **Main** type from the list.</span><span class="sxs-lookup"><span data-stu-id="a099f-120">Select the **Contact** form of the **Main** type from the list.</span></span><br>
<span data-ttu-id="a099f-121">![Select contact form of Main type](media/contact-main-form.PNG "Select contact form of Main type")</span><span class="sxs-lookup"><span data-stu-id="a099f-121">![Select contact form of Main type](media/contact-main-form.PNG "Select contact form of Main type")</span></span>

5. <span data-ttu-id="a099f-122">Select the phone field for which you want to add the control.</span><span class="sxs-lookup"><span data-stu-id="a099f-122">Select the phone field for which you want to add the control.</span></span> <span data-ttu-id="a099f-123">Double-click the **Business Phone** or **Mobile Phone** field.</span><span class="sxs-lookup"><span data-stu-id="a099f-123">Double-click the **Business Phone** or **Mobile Phone** field.</span></span><br> <span data-ttu-id="a099f-124">The **Field Properties** dialog appears.</span><span class="sxs-lookup"><span data-stu-id="a099f-124">The **Field Properties** dialog appears.</span></span>

6. <span data-ttu-id="a099f-125">In the **Field Properties** dialog, choose **Controls** tab, and select the **Add control...** option.</span><span class="sxs-lookup"><span data-stu-id="a099f-125">In the **Field Properties** dialog, choose **Controls** tab, and select the **Add control...** option.</span></span> <br>
<span data-ttu-id="a099f-126">![Select phone, then select the Controls tab, and select the Add control option](media/add-custom-control.PNG "Select business or mobile phone, then select the Controls tab, and select the Add control option")</span><span class="sxs-lookup"><span data-stu-id="a099f-126">![Select phone, then select the Controls tab, and select the Add control option](media/add-custom-control.PNG "Select business or mobile phone, then select the Controls tab, and select the Add control option")</span></span>

7. <span data-ttu-id="a099f-127">In the **Add Control** dialog, choose **Channel Communication Control**, and select **Add**.</span><span class="sxs-lookup"><span data-stu-id="a099f-127">In the **Add Control** dialog, choose **Channel Communication Control**, and select **Add**.</span></span><br>
<span data-ttu-id="a099f-128">![Choose Channel Communication Control and select add](media/add-control.PNG "Choose Channel Communication Control and select add")</span><span class="sxs-lookup"><span data-stu-id="a099f-128">![Choose Channel Communication Control and select add](media/add-control.PNG "Choose Channel Communication Control and select add")</span></span>

8. <span data-ttu-id="a099f-129">In the **Field Properties** dialog, select the radio buttons for **Web**, **Phone**, and **Tablet**, and then select **Ok**.</span><span class="sxs-lookup"><span data-stu-id="a099f-129">In the **Field Properties** dialog, select the radio buttons for **Web**, **Phone**, and **Tablet**, and then select **Ok**.</span></span><br>
<span data-ttu-id="a099f-130">![Select the radio buttons of web, phone, and tablet](media/select-radio-buttons.PNG "Select the radio buttons pf web, phone, and tablet")</span><span class="sxs-lookup"><span data-stu-id="a099f-130">![Select the radio buttons of web, phone, and tablet](media/select-radio-buttons.PNG "Select the radio buttons pf web, phone, and tablet")</span></span> 

9. <span data-ttu-id="a099f-131">Select **Save**, and then select **Publish** to publish all customizations.</span><span class="sxs-lookup"><span data-stu-id="a099f-131">Select **Save**, and then select **Publish** to publish all customizations.</span></span>

## <a name="step-3-register-the-addhandler-in-javascript-code-using-the-onclicktoact-event"></a><span data-ttu-id="a099f-132">Step 3: Register the addHandler in JavaScript code using the onclicktoact event</span><span class="sxs-lookup"><span data-stu-id="a099f-132">Step 3: Register the addHandler in JavaScript code using the onclicktoact event</span></span>

<span data-ttu-id="a099f-133">During the initialization of the function, register the handler for the `onlicktoact` event.</span><span class="sxs-lookup"><span data-stu-id="a099f-133">During the initialization of the function, register the handler for the `onlicktoact` event.</span></span>

```JavaScript
function initCTI() {
    Microsoft.CIFramework.setClickToAct(true);
    Microsoft.CIFramework.addHandler("onclicktoact", clickToActHandler);
    log("Added clickToActhandler to the panel");
}
```
> [!Note]
> <span data-ttu-id="a099f-134">Channel Integration Framework invokes the onclicktoact event only if you programmatically set the `setClickToAct` API to `true` or by configuring the **Enable Outbound Communication** to **Yes** in the channel provider configurations.</span><span class="sxs-lookup"><span data-stu-id="a099f-134">Channel Integration Framework invokes the onclicktoact event only if you programmatically set the `setClickToAct` API to `true` or by configuring the **Enable Outbound Communication** to **Yes** in the channel provider configurations.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="a099f-135">Add Channel Integration Framework as a dependent solution</span><span class="sxs-lookup"><span data-stu-id="a099f-135">Add Channel Integration Framework as a dependent solution</span></span>](add-cif-solution-dependent-solution.md)

## <a name="see-also"></a><span data-ttu-id="a099f-136">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a099f-136">See also</span></span>

[<span data-ttu-id="a099f-137">Tham chiếu thực thể</span><span class="sxs-lookup"><span data-stu-id="a099f-137">Entity reference</span></span>](reference/entities-attributes/msdyn-ciprovider.md)

[<span data-ttu-id="a099f-138">setClickToAct</span><span class="sxs-lookup"><span data-stu-id="a099f-138">setClickToAct</span></span>](reference/microsoft-ciframework/setClickToAct.md)

[<span data-ttu-id="a099f-139">getClickToAct</span><span class="sxs-lookup"><span data-stu-id="a099f-139">getClickToAct</span></span>](reference/microsoft-ciframework/getClickToAct.md)

[<span data-ttu-id="a099f-140">onclicktoact</span><span class="sxs-lookup"><span data-stu-id="a099f-140">onclicktoact</span></span>](reference/events/onclicktoact.md)

