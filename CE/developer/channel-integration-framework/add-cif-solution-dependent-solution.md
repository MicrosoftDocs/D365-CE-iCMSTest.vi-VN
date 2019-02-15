---
title: Add a Dynamics 365 Channel Integration Framework (CIF) solution as a dependent solution| Microsoft Docs
description: Read how you can add a CIF solution as a dependent solution and use CIF solution's capabilities in your own solution.
keywords: ''
ms.date: 12/10/2018
ms.service:
- dynamics-365-cross-app
ms.custom:
- dyn365-a11y
- dyn365-developer
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement Version 9.x
ms.assetid: 7B9466F3-CFF6-447B-8570-AB3A51F4096C
author: susikka
ms.author: susikka
manager: shujoshi
ms.openlocfilehash: d7499811e0bcba396f2f5f82bf9576fff3c8095c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388323"
---
# <a name="add-a-dynamics-365-channel-integration-framework-cif-solution-as-a-dependent-solution"></a><span data-ttu-id="42f81-103">Add a Dynamics 365 Channel Integration Framework (CIF) solution as a dependent solution</span><span class="sxs-lookup"><span data-stu-id="42f81-103">Add a Dynamics 365 Channel Integration Framework (CIF) solution as a dependent solution</span></span>

<span data-ttu-id="42f81-104">Third-party channel providers can add a Channel Integration Framework (CIF) solution as a dependent solution to use CIF's capabilites in the solutions they develop for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="42f81-104">Third-party channel providers can add a Channel Integration Framework (CIF) solution as a dependent solution to use CIF's capabilites in the solutions they develop for Dynamics 365.</span></span> <span data-ttu-id="42f81-105">This topic describes how users can install, update, and delete a CIF solution as a dependent solution.</span><span class="sxs-lookup"><span data-stu-id="42f81-105">This topic describes how users can install, update, and delete a CIF solution as a dependent solution.</span></span>

## <a name="add-a-channel-integration-framework-solution-as-a-dependent-solution"></a><span data-ttu-id="42f81-106">Add a Channel Integration Framework solution as a dependent solution</span><span class="sxs-lookup"><span data-stu-id="42f81-106">Add a Channel Integration Framework solution as a dependent solution</span></span>  

1. <span data-ttu-id="42f81-107">Add the Channel Integration Framework application to your Dynamics 365 instance that has an unmanaged dependent solution installed (for example, solution "X").</span><span class="sxs-lookup"><span data-stu-id="42f81-107">Add the Channel Integration Framework application to your Dynamics 365 instance that has an unmanaged dependent solution installed (for example, solution "X").</span></span> <span data-ttu-id="42f81-108">More information: [Get Channel Integration Framework](get-channel-integration-framework.md)</span><span class="sxs-lookup"><span data-stu-id="42f81-108">More information: [Get Channel Integration Framework](get-channel-integration-framework.md)</span></span>

2. <span data-ttu-id="42f81-109">Sign in to your Dynamics 365 instance and go to **Settings** > **Solutions**.</span><span class="sxs-lookup"><span data-stu-id="42f81-109">Sign in to your Dynamics 365 instance and go to **Settings** > **Solutions**.</span></span>

3. <span data-ttu-id="42f81-110">From the list of solutions, select the "X" solution to open it.</span><span class="sxs-lookup"><span data-stu-id="42f81-110">From the list of solutions, select the "X" solution to open it.</span></span>

4. <span data-ttu-id="42f81-111">In the window that opens, select **Model Driven App** from the left panel.</span><span class="sxs-lookup"><span data-stu-id="42f81-111">In the window that opens, select **Model Driven App** from the left panel.</span></span>

5. <span data-ttu-id="42f81-112">Select **Channel Integration Framework** and then select **OK**.</span><span class="sxs-lookup"><span data-stu-id="42f81-112">Select **Channel Integration Framework** and then select **OK**.</span></span>

6. <span data-ttu-id="42f81-113">Select **Publish all customizations**.</span><span class="sxs-lookup"><span data-stu-id="42f81-113">Select **Publish all customizations**.</span></span>

7. <span data-ttu-id="42f81-114">Close the solution window.</span><span class="sxs-lookup"><span data-stu-id="42f81-114">Close the solution window.</span></span>

8. <span data-ttu-id="42f81-115">Export the solution.</span><span class="sxs-lookup"><span data-stu-id="42f81-115">Export the solution.</span></span>

## <a name="remove-a-channel-integration-framework-solution-as-a-dependent-solution"></a><span data-ttu-id="42f81-116">Remove a Channel Integration Framework solution as a dependent solution</span><span class="sxs-lookup"><span data-stu-id="42f81-116">Remove a Channel Integration Framework solution as a dependent solution</span></span>
  
1. [!INCLUDE[proc_permissions_system_admin_and_customizer](../../includes/proc-permissions-system-admin-and-customizer.md)]  
  
2. <span data-ttu-id="42f81-117">Đăng nhập vào [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="42f81-117">Sign in to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span></span>  
  
3. <span data-ttu-id="42f81-118">Chọn **Thiết đặt** > **Giải pháp**.</span><span class="sxs-lookup"><span data-stu-id="42f81-118">Select **Settings** > **Solutions**.</span></span>  
  
4. <span data-ttu-id="42f81-119">Select solution "X".</span><span class="sxs-lookup"><span data-stu-id="42f81-119">Select solution "X".</span></span>

5. <span data-ttu-id="42f81-120">In the window that opens, select the **Channel Integration Framework** solution.</span><span class="sxs-lookup"><span data-stu-id="42f81-120">In the window that opens, select the **Channel Integration Framework** solution.</span></span>

6. <span data-ttu-id="42f81-121">Select **Delete** and then select the **Delete** button in the dialog box that opens to confirm that you want to remove CIF as a dependent solution.</span><span class="sxs-lookup"><span data-stu-id="42f81-121">Select **Delete** and then select the **Delete** button in the dialog box that opens to confirm that you want to remove CIF as a dependent solution.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="42f81-122">Authenticate channel users to the channel (widget)</span><span class="sxs-lookup"><span data-stu-id="42f81-122">Authenticate channel users to the channel (widget)</span></span>](authenticate-channel-users.md)

## <a name="see-also"></a><span data-ttu-id="42f81-123">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="42f81-123">See also</span></span>

[<span data-ttu-id="42f81-124">Get Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="42f81-124">Get Channel Integration Framework</span></span>](get-channel-integration-framework.md)<br />
[<span data-ttu-id="42f81-125">Configure a channel provider for your Dynamics 365 organization</span><span class="sxs-lookup"><span data-stu-id="42f81-125">Configure a channel provider for your Dynamics 365 organization</span></span>](configure-channel-provider-channel-integration-framework.md)<br />
[<span data-ttu-id="42f81-126">Enable outbound communication (ClickToAct)</span><span class="sxs-lookup"><span data-stu-id="42f81-126">Enable outbound communication (ClickToAct)</span></span>](enable-outbound-communication-clicktoact.md)<br />
[<span data-ttu-id="42f81-127">Authenticate channel users to the channel (widget)</span><span class="sxs-lookup"><span data-stu-id="42f81-127">Authenticate channel users to the channel (widget)</span></span>](authenticate-channel-users.md)<br />
[<span data-ttu-id="42f81-128">Pass a Dynamics 365 URL to a widget library</span><span class="sxs-lookup"><span data-stu-id="42f81-128">Pass a Dynamics 365 URL to a widget library</span></span>](pass-url-widget-library.md)
