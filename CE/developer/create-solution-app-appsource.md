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
# <a name="step-3-create-a-managed-solution-for-your-app"></a>Step 3: Create a managed solution for your app

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Create a managed solution to include all the components for your app. You might find these topics helpful as you plan and create a managed solution to package your app components:
- [Giới thiệu về các giải pháp](introduction-solutions.md)
- [Plan for solution development](plan-solution-development.md) 
- [Create, install, and update a managed solution](create-install-update-managed-solution.md)

## <a name="display-name-and-description-of-your-solution"></a>Display name and description of your solution

While creating a solution to package your app components, make sure you provide appropriate values in the **Display Name** and **Description** fields for your new solution that you want to be displayed to your customers.

![Create a solution](media/appsource-new-solution.png)

The **Display Name** and **Description** values for a solution are displayed to the customers in the **Dynamics 365 for Customer Engagement apps Administration Center** portal.

![Giải pháp](media/appsource-solution-names.png)

## <a name="supporting-data-for-your-solution"></a>Supporting data for your solution

If your solution requires supporting or demo data:
1. Create supporting/demo data in your test environment.
2. Use the [Configuration Migration tool](../admin/manage-configuration-data.md) to create a schema to include your supporting/demo data. 
3. Save the schema file so that you can reuse it later to update the data in case your demo data changes.
4. Use the schema to export the data. Ensure that you provide a meaningful name to your export file. The data is exported and as a .zip file.

For detailed information about using the Configuration Migration tool to create a schema and export your data, see [Create a schema to export configuration data](../admin/create-schema-export-configuration-data.md)

## <a name="at-the-end-of-this-step"></a>At the end of this step

You will have a solution file (example: *SampleSolution.zip*) and optionally a demo data file (example: *SampleData.zip*) for your app.


> [!div class="nextstepaction"]
> [Step 4: Create an AppSource package for your app](create-package-app-appsource.md) 