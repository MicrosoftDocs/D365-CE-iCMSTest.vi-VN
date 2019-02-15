---
title: 'Walkthrough: Update a service endpoint imported from a solution (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The walkthrough demonstrates updating a service endpoint imported from a solution.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8c860992-d3c6-4bfa-86c4-98018af6f22c
caps.latest.revision: 8
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 89d75425cd8d129ba1845270ff368f3290921845
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385553"
---
# <a name="walkthrough-update-a-service-endpoint-imported-from-a-solution"></a><span data-ttu-id="b50cb-103">Walkthrough: Update a service endpoint imported from a solution</span><span class="sxs-lookup"><span data-stu-id="b50cb-103">Walkthrough: Update a service endpoint imported from a solution</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b50cb-104">An extra step is required after importing into an organization a solution containing one or more service endpoints configured for SAS authorization.</span><span class="sxs-lookup"><span data-stu-id="b50cb-104">An extra step is required after importing into an organization a solution containing one or more service endpoints configured for SAS authorization.</span></span> <span data-ttu-id="b50cb-105">When the solution containing the service endpoints is exported, the exported solution does not contain the SAS Key for each service endpoint.</span><span class="sxs-lookup"><span data-stu-id="b50cb-105">When the solution containing the service endpoints is exported, the exported solution does not contain the SAS Key for each service endpoint.</span></span> <span data-ttu-id="b50cb-106">After importing the solution into an organization, you must perform an additional step to provide the SAS Key for each service endpoint.</span><span class="sxs-lookup"><span data-stu-id="b50cb-106">After importing the solution into an organization, you must perform an additional step to provide the SAS Key for each service endpoint.</span></span>  
  
 <span data-ttu-id="b50cb-107">Follow these steps to set the SAS Key for each service endpoint after solution import.</span><span class="sxs-lookup"><span data-stu-id="b50cb-107">Follow these steps to set the SAS Key for each service endpoint after solution import.</span></span>  
  
### <a name="update-the-sas-key"></a><span data-ttu-id="b50cb-108">Update the SAS Key</span><span class="sxs-lookup"><span data-stu-id="b50cb-108">Update the SAS Key</span></span>  
  
1. <span data-ttu-id="b50cb-109">Run the Plug-in Registration Tool, which can be found in the Tools folder of the [!INCLUDE[pn_crm_8_1_0_op](../includes/pn-crm-8-1-0-op.md)] (or later) SDK download.</span><span class="sxs-lookup"><span data-stu-id="b50cb-109">Run the Plug-in Registration Tool, which can be found in the Tools folder of the [!INCLUDE[pn_crm_8_1_0_op](../includes/pn-crm-8-1-0-op.md)] (or later) SDK download.</span></span> <span data-ttu-id="b50cb-110">Previous releases of the tool do not support SAS authorization.</span><span class="sxs-lookup"><span data-stu-id="b50cb-110">Previous releases of the tool do not support SAS authorization.</span></span>  
  
2. <span data-ttu-id="b50cb-111">Using the tool, sign in to the organization that contains the imported solution.</span><span class="sxs-lookup"><span data-stu-id="b50cb-111">Using the tool, sign in to the organization that contains the imported solution.</span></span>  
  
3. <span data-ttu-id="b50cb-112">Select the target service endpoint in the tab view of the organization.</span><span class="sxs-lookup"><span data-stu-id="b50cb-112">Select the target service endpoint in the tab view of the organization.</span></span>  
  
4. <span data-ttu-id="b50cb-113">Chọn **Cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="b50cb-113">Select **Update**.</span></span> <span data-ttu-id="b50cb-114">You should see the following form with the fields already filled in.</span><span class="sxs-lookup"><span data-stu-id="b50cb-114">You should see the following form with the fields already filled in.</span></span>  
  
   <span data-ttu-id="b50cb-115">![Update service endpoint SAS key value](media/sas-key.PNG "Update service endpoint SAS key value")</span><span class="sxs-lookup"><span data-stu-id="b50cb-115">![Update service endpoint SAS key value](media/sas-key.PNG "Update service endpoint SAS key value")</span></span>  
  
5. <span data-ttu-id="b50cb-116">The **SAS Key** field is displayed with a value of "\*\*\*\*\*\*\*".</span><span class="sxs-lookup"><span data-stu-id="b50cb-116">The **SAS Key** field is displayed with a value of "\*\*\*\*\*\*\*".</span></span>  <span data-ttu-id="b50cb-117">Replace that value with the correct SAS key value.</span><span class="sxs-lookup"><span data-stu-id="b50cb-117">Replace that value with the correct SAS key value.</span></span> <span data-ttu-id="b50cb-118">You can obtain the SAS Key for your [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] messaging entity (queue, topic, etc.) from the [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)][classic portal](http://manage.windowsazure.com).</span><span class="sxs-lookup"><span data-stu-id="b50cb-118">You can obtain the SAS Key for your [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] messaging entity (queue, topic, etc.) from the [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)][classic portal](http://manage.windowsazure.com).</span></span>  
  
6. <span data-ttu-id="b50cb-119">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="b50cb-119">Select **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b50cb-120">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b50cb-120">See also</span></span>  
 <span data-ttu-id="b50cb-121">[Azure extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md) </span><span class="sxs-lookup"><span data-stu-id="b50cb-121">[Azure extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md) </span></span>  
 [<span data-ttu-id="b50cb-122">Service Bus authentication and authorization</span><span class="sxs-lookup"><span data-stu-id="b50cb-122">Service Bus authentication and authorization</span></span>](https://azure.microsoft.com/en-us/documentation/articles/service-bus-authentication-and-authorization/)
