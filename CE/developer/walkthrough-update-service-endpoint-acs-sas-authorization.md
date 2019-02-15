---
title: 'Walkthrough: Update a service endpoint from ACS to SAS authorization (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The walkthrough demonstrates updating a service endpoint from Access Control Service (ACS) to Shared Access Signature (SAS) authorization.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a1a4fe6f-be17-4a75-af6c-cd1ee901b868
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4c8905d673d5cac646cc34c75693be673edb1fbd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385621"
---
# <a name="walkthrough-update-a-service-endpoint-from-acs-to-sas-authorization"></a><span data-ttu-id="64d3f-103">Walkthrough: Update a service endpoint from ACS to SAS authorization</span><span class="sxs-lookup"><span data-stu-id="64d3f-103">Walkthrough: Update a service endpoint from ACS to SAS authorization</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="64d3f-104">Shared Access Signature (SAS) is the recommended authorization method for the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement and [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] integration as its use results in improved authorization performance compared to Access Control Service (ACS), and SAS is supported on all [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] deployments without any special server configuration.</span><span class="sxs-lookup"><span data-stu-id="64d3f-104">Shared Access Signature (SAS) is the recommended authorization method for the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement and [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] integration as its use results in improved authorization performance compared to Access Control Service (ACS), and SAS is supported on all [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] deployments without any special server configuration.</span></span> <span data-ttu-id="64d3f-105">You can update existing service endpoint entity records in a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization from ACS to SAS authorization by using the Plug-in Registration Tool and following these steps.</span><span class="sxs-lookup"><span data-stu-id="64d3f-105">You can update existing service endpoint entity records in a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization from ACS to SAS authorization by using the Plug-in Registration Tool and following these steps.</span></span>  
  
> [!NOTE]
> [!INCLUDE[cc_feature_included_with_update_8_1_0_admins](../includes/cc-feature-included-with-update-8-1-0-admins.md)] <span data-ttu-id="64d3f-106">The Plug-in Registration Tool from the v8.1 or later [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] SDK includes SAS support.</span><span class="sxs-lookup"><span data-stu-id="64d3f-106">The Plug-in Registration Tool from the v8.1 or later [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] SDK includes SAS support.</span></span>  
  
## <a name="step-1-update-the-messaging-entity"></a><span data-ttu-id="64d3f-107">Step 1: Update the messaging entity</span><span class="sxs-lookup"><span data-stu-id="64d3f-107">Step 1: Update the messaging entity</span></span>  
 <span data-ttu-id="64d3f-108">You'll need to update your [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] messaging entity that was configured for ACS authorization, for example a queue or topic, to be properly configured for SAS.</span><span class="sxs-lookup"><span data-stu-id="64d3f-108">You'll need to update your [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] messaging entity that was configured for ACS authorization, for example a queue or topic, to be properly configured for SAS.</span></span> <span data-ttu-id="64d3f-109">This is simple to do as you just need to add a SAS shared access policy.</span><span class="sxs-lookup"><span data-stu-id="64d3f-109">This is simple to do as you just need to add a SAS shared access policy.</span></span>  
  
### <a name="perform-the-update"></a><span data-ttu-id="64d3f-110">Perform the update</span><span class="sxs-lookup"><span data-stu-id="64d3f-110">Perform the update</span></span>  
  
1. <span data-ttu-id="64d3f-111">Sign in to the [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)][Classic portal](https://manage.windowsazure.com).</span><span class="sxs-lookup"><span data-stu-id="64d3f-111">Sign in to the [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)][Classic portal](https://manage.windowsazure.com).</span></span>  
  
2. <span data-ttu-id="64d3f-112">Navigate to the messaging entity that you plan to update.</span><span class="sxs-lookup"><span data-stu-id="64d3f-112">Navigate to the messaging entity that you plan to update.</span></span>  
  
3. <span data-ttu-id="64d3f-113">Select the entity and then select **CONFIGURE**.</span><span class="sxs-lookup"><span data-stu-id="64d3f-113">Select the entity and then select **CONFIGURE**.</span></span>  
  
4. <span data-ttu-id="64d3f-114">Create a shared access policy and specify **Send** permission at a minimum.</span><span class="sxs-lookup"><span data-stu-id="64d3f-114">Create a shared access policy and specify **Send** permission at a minimum.</span></span> <span data-ttu-id="64d3f-115">**Listen** permission is required for a two-way endpoint contract.</span><span class="sxs-lookup"><span data-stu-id="64d3f-115">**Listen** permission is required for a two-way endpoint contract.</span></span>  
  
5. <span data-ttu-id="64d3f-116">Verify the messaging entity's SAS connection information.</span><span class="sxs-lookup"><span data-stu-id="64d3f-116">Verify the messaging entity's SAS connection information.</span></span> <span data-ttu-id="64d3f-117">It should have a connection string.</span><span class="sxs-lookup"><span data-stu-id="64d3f-117">It should have a connection string.</span></span>  
  
## <a name="step-2-update-the-service-endpoint"></a><span data-ttu-id="64d3f-118">Step 2: Update the service endpoint</span><span class="sxs-lookup"><span data-stu-id="64d3f-118">Step 2: Update the service endpoint</span></span>  
 <span data-ttu-id="64d3f-119">Now go ahead an update the service endpoint entity record in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organization with the SAS information of your messaging entity.</span><span class="sxs-lookup"><span data-stu-id="64d3f-119">Now go ahead an update the service endpoint entity record in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organization with the SAS information of your messaging entity.</span></span>  
  
### <a name="perform-the-update"></a><span data-ttu-id="64d3f-120">Perform the update</span><span class="sxs-lookup"><span data-stu-id="64d3f-120">Perform the update</span></span>  
  
1. <span data-ttu-id="64d3f-121">Run the Plug-in Registration Tool and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organization containing the service endpoint.</span><span class="sxs-lookup"><span data-stu-id="64d3f-121">Run the Plug-in Registration Tool and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organization containing the service endpoint.</span></span>  
  
2. <span data-ttu-id="64d3f-122">Select the service endpoint and then select **Update**.</span><span class="sxs-lookup"><span data-stu-id="64d3f-122">Select the service endpoint and then select **Update**.</span></span>  
  
3. <span data-ttu-id="64d3f-123">Enter a value for the **SAS Key Name** and the **SAS Key**.</span><span class="sxs-lookup"><span data-stu-id="64d3f-123">Enter a value for the **SAS Key Name** and the **SAS Key**.</span></span> <span data-ttu-id="64d3f-124">These are obtained from the messaging entity's connection string that is available in the [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] management portal.</span><span class="sxs-lookup"><span data-stu-id="64d3f-124">These are obtained from the messaging entity's connection string that is available in the [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] management portal.</span></span> <span data-ttu-id="64d3f-125">Look for SharedAccessKeyName and `SharedAccessKey` values in the connection string.</span><span class="sxs-lookup"><span data-stu-id="64d3f-125">Look for SharedAccessKeyName and `SharedAccessKey` values in the connection string.</span></span>  
  
4. <span data-ttu-id="64d3f-126">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="64d3f-126">Select **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="64d3f-127">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="64d3f-127">See also</span></span>  
 <span data-ttu-id="64d3f-128">[Azure extensions for Dynamics 365 for Customer Engagement](azure-extensions.md) </span><span class="sxs-lookup"><span data-stu-id="64d3f-128">[Azure extensions for Dynamics 365 for Customer Engagement](azure-extensions.md) </span></span>  
 [<span data-ttu-id="64d3f-129">Azure integration with Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="64d3f-129">Azure integration with Dynamics 365 for Customer Engagement</span></span>](azure-integration.md)
