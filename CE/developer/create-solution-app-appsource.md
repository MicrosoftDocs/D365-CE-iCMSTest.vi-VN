---
title: 'Step 3: Create a managed solution for your app (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs'
description: Learn about how to create a managed solution for your app to include all the components. This is required for publishing an app to Appsource.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: bbb1ecdb-4938-4ff6-a2d5-f100851fc287
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1916df59ee97b746cf185736ad3ab251cf539100
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387264"
---
# <a name="step-3-create-a-managed-solution-for-your-app"></a><span data-ttu-id="2d553-104">Step 3: Create a managed solution for your app</span><span class="sxs-lookup"><span data-stu-id="2d553-104">Step 3: Create a managed solution for your app</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2d553-105">Create a managed solution to include all the components for your app.</span><span class="sxs-lookup"><span data-stu-id="2d553-105">Create a managed solution to include all the components for your app.</span></span> <span data-ttu-id="2d553-106">You might find these topics helpful as you plan and create a managed solution to package your app components:</span><span class="sxs-lookup"><span data-stu-id="2d553-106">You might find these topics helpful as you plan and create a managed solution to package your app components:</span></span>
- [<span data-ttu-id="2d553-107">Giới thiệu về các giải pháp</span><span class="sxs-lookup"><span data-stu-id="2d553-107">Introduction to solutions</span></span>](introduction-solutions.md)
- [<span data-ttu-id="2d553-108">Plan for solution development</span><span class="sxs-lookup"><span data-stu-id="2d553-108">Plan for solution development</span></span>](plan-solution-development.md) 
- [<span data-ttu-id="2d553-109">Create, install, and update a managed solution</span><span class="sxs-lookup"><span data-stu-id="2d553-109">Create, install, and update a managed solution</span></span>](create-install-update-managed-solution.md)

## <a name="display-name-and-description-of-your-solution"></a><span data-ttu-id="2d553-110">Display name and description of your solution</span><span class="sxs-lookup"><span data-stu-id="2d553-110">Display name and description of your solution</span></span>

<span data-ttu-id="2d553-111">While creating a solution to package your app components, make sure you provide appropriate values in the **Display Name** and **Description** fields for your new solution that you want to be displayed to your customers.</span><span class="sxs-lookup"><span data-stu-id="2d553-111">While creating a solution to package your app components, make sure you provide appropriate values in the **Display Name** and **Description** fields for your new solution that you want to be displayed to your customers.</span></span>

![Create a solution](media/appsource-new-solution.png)

<span data-ttu-id="2d553-113">The **Display Name** and **Description** values for a solution are displayed to the customers in the **Dynamics 365 for Customer Engagement apps Administration Center** portal.</span><span class="sxs-lookup"><span data-stu-id="2d553-113">The **Display Name** and **Description** values for a solution are displayed to the customers in the **Dynamics 365 for Customer Engagement apps Administration Center** portal.</span></span>

![Giải pháp](media/appsource-solution-names.png)

## <a name="supporting-data-for-your-solution"></a><span data-ttu-id="2d553-115">Supporting data for your solution</span><span class="sxs-lookup"><span data-stu-id="2d553-115">Supporting data for your solution</span></span>

<span data-ttu-id="2d553-116">If your solution requires supporting or demo data:</span><span class="sxs-lookup"><span data-stu-id="2d553-116">If your solution requires supporting or demo data:</span></span>
1. <span data-ttu-id="2d553-117">Create supporting/demo data in your test environment.</span><span class="sxs-lookup"><span data-stu-id="2d553-117">Create supporting/demo data in your test environment.</span></span>
2. <span data-ttu-id="2d553-118">Use the [Configuration Migration tool](../admin/manage-configuration-data.md) to create a schema to include your supporting/demo data.</span><span class="sxs-lookup"><span data-stu-id="2d553-118">Use the [Configuration Migration tool](../admin/manage-configuration-data.md) to create a schema to include your supporting/demo data.</span></span> 
3. <span data-ttu-id="2d553-119">Save the schema file so that you can reuse it later to update the data in case your demo data changes.</span><span class="sxs-lookup"><span data-stu-id="2d553-119">Save the schema file so that you can reuse it later to update the data in case your demo data changes.</span></span>
4. <span data-ttu-id="2d553-120">Use the schema to export the data.</span><span class="sxs-lookup"><span data-stu-id="2d553-120">Use the schema to export the data.</span></span> <span data-ttu-id="2d553-121">Ensure that you provide a meaningful name to your export file.</span><span class="sxs-lookup"><span data-stu-id="2d553-121">Ensure that you provide a meaningful name to your export file.</span></span> <span data-ttu-id="2d553-122">The data is exported and as a .zip file.</span><span class="sxs-lookup"><span data-stu-id="2d553-122">The data is exported and as a .zip file.</span></span>

<span data-ttu-id="2d553-123">For detailed information about using the Configuration Migration tool to create a schema and export your data, see [Create a schema to export configuration data](../admin/create-schema-export-configuration-data.md)</span><span class="sxs-lookup"><span data-stu-id="2d553-123">For detailed information about using the Configuration Migration tool to create a schema and export your data, see [Create a schema to export configuration data](../admin/create-schema-export-configuration-data.md)</span></span>

## <a name="at-the-end-of-this-step"></a><span data-ttu-id="2d553-124">At the end of this step</span><span class="sxs-lookup"><span data-stu-id="2d553-124">At the end of this step</span></span>

<span data-ttu-id="2d553-125">You will have a solution file (example: *SampleSolution.zip*) and optionally a demo data file (example: *SampleData.zip*) for your app.</span><span class="sxs-lookup"><span data-stu-id="2d553-125">You will have a solution file (example: *SampleSolution.zip*) and optionally a demo data file (example: *SampleData.zip*) for your app.</span></span>


> [!div class="nextstepaction"]
> [<span data-ttu-id="2d553-126">Step 4: Create an AppSource package for your app</span><span class="sxs-lookup"><span data-stu-id="2d553-126">Step 4: Create an AppSource package for your app</span></span>](create-package-app-appsource.md) 