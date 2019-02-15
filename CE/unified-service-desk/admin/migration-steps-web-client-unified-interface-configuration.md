---
title: Migrate Unified Service Desk configurations from Web Client to Unified Interface app | MicrosoftDocs
description: The three-step process for migrating Web Client configurations to Unified Interface
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
ms.assetid: 7B923254-C1B1-4345-84B7-69FA641A18A9
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 14abd3b7853ad95bfc13943ede14e2d4d7af20d7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382607"
---
# <a name="how-to-migrate-unified-service-desk-configurations-from-dynamics-365-for-customer-engagement-apps-web-client-to-unified-interface"></a><span data-ttu-id="e2225-103">How to migrate Unified Service Desk configurations from Dynamics 365 for Customer Engagement apps Web Client to Unified Interface</span><span class="sxs-lookup"><span data-stu-id="e2225-103">How to migrate Unified Service Desk configurations from Dynamics 365 for Customer Engagement apps Web Client to Unified Interface</span></span>

<span data-ttu-id="e2225-104">The migration of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations from [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web Client to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Unified Interface is a three-step process.</span><span class="sxs-lookup"><span data-stu-id="e2225-104">The migration of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations from [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web Client to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Unified Interface is a three-step process.</span></span>

- <span data-ttu-id="e2225-105">**Step 1:** Fetch and migrate the configuration elements to a **USD_UI_Configurations** folder using the Web Client - Unified Interface Migration Assistant.</span><span class="sxs-lookup"><span data-stu-id="e2225-105">**Step 1:** Fetch and migrate the configuration elements to a **USD_UI_Configurations** folder using the Web Client - Unified Interface Migration Assistant.</span></span>

- <span data-ttu-id="e2225-106">**Step 2:** Import the **USDWebResources** folder, which is in the **USD_UI_Configurations** folder, using the **Solutions** option in the Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="e2225-106">**Step 2:** Import the **USDWebResources** folder, which is in the **USD_UI_Configurations** folder, using the **Solutions** option in the Dynamics 365 for Customer Engagement apps.</span></span>

- <span data-ttu-id="e2225-107">**Step 3:** Import the **Data** zip folder from the **USD_UI_Configurations** folder to the Unified Interface App using the Configuration Migration Tool (DataMigrationUtility.exe).</span><span class="sxs-lookup"><span data-stu-id="e2225-107">**Step 3:** Import the **Data** zip folder from the **USD_UI_Configurations** folder to the Unified Interface App using the Configuration Migration Tool (DataMigrationUtility.exe).</span></span>

<span data-ttu-id="e2225-108">This diagram illustrates the flow of the migration:</span><span class="sxs-lookup"><span data-stu-id="e2225-108">This diagram illustrates the flow of the migration:</span></span>
> [!div class="mx-imgBorder"]
> <span data-ttu-id="e2225-109">![Migration Steps](../media/migration-steps-web-client-unified-interface-migration-assistant.PNG "Migration Steps")</span><span class="sxs-lookup"><span data-stu-id="e2225-109">![Migration Steps](../media/migration-steps-web-client-unified-interface-migration-assistant.PNG "Migration Steps")</span></span> 

1. <span data-ttu-id="e2225-110">**Dynamics 365 for Customer Engagement apps Web Client**</span><span class="sxs-lookup"><span data-stu-id="e2225-110">**Dynamics 365 for Customer Engagement apps Web Client**</span></span> </br></br> <span data-ttu-id="e2225-111">The [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web Client is the instance from where you want to migrate your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations.</span><span class="sxs-lookup"><span data-stu-id="e2225-111">The [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web Client is the instance from where you want to migrate your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations.</span></span>

2. <span data-ttu-id="e2225-112">**Máy khách web - Trợ lý Di chuyển Giao diện Hợp nhất**</span><span class="sxs-lookup"><span data-stu-id="e2225-112">**Web Client - Unified Interface Migration Assistant**</span></span> </br></br> <span data-ttu-id="e2225-113">The tool to fetch and migrate the Web Client configurations to **USD_UI_Configurations** folder, which contains the **Data** and **WebResources** zip folders.</span><span class="sxs-lookup"><span data-stu-id="e2225-113">The tool to fetch and migrate the Web Client configurations to **USD_UI_Configurations** folder, which contains the **Data** and **WebResources** zip folders.</span></span> <span data-ttu-id="e2225-114">If you have **RunXrmCommand** actions in Web Client configurations, the migration assistant migrates the **RunXRMCommand** actions as a web resource and you can find them in the **USDWebResources** folder under the **USD_UI_Configurations** folder.</span><span class="sxs-lookup"><span data-stu-id="e2225-114">If you have **RunXrmCommand** actions in Web Client configurations, the migration assistant migrates the **RunXRMCommand** actions as a web resource and you can find them in the **USDWebResources** folder under the **USD_UI_Configurations** folder.</span></span>

3. <span data-ttu-id="e2225-115">**USD_UI_Configurations**</span><span class="sxs-lookup"><span data-stu-id="e2225-115">**USD_UI_Configurations**</span></span> </br></br> <span data-ttu-id="e2225-116">The configurations are migrated to the **USD_UI_Configurations** zip folder that contains the **Data** and/or **WebResources** zip folder.</span><span class="sxs-lookup"><span data-stu-id="e2225-116">The configurations are migrated to the **USD_UI_Configurations** zip folder that contains the **Data** and/or **WebResources** zip folder.</span></span>

4. <span data-ttu-id="e2225-117">**Configuration Migration Tool**</span><span class="sxs-lookup"><span data-stu-id="e2225-117">**Configuration Migration Tool**</span></span> </br></br> <span data-ttu-id="e2225-118">The Configuration Migration Tool lets you to import the **Data** zip folder and deploy it to the target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="e2225-118">The Configuration Migration Tool lets you to import the **Data** zip folder and deploy it to the target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Unified Interface App.</span></span>

5. <span data-ttu-id="e2225-119">**Dynamics 365 for Customer Engagement apps (Unified Interface apps)** The target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance to which you want to deploy the configurations.</span><span class="sxs-lookup"><span data-stu-id="e2225-119">**Dynamics 365 for Customer Engagement apps (Unified Interface apps)** The target [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance to which you want to deploy the configurations.</span></span>

## <a name="step-1-use-migration-assistant-to-fetch-and-migrate-the-web-client-configurations"></a><span data-ttu-id="e2225-120">Step 1: Use migration assistant to fetch and migrate the Web Client configurations</span><span class="sxs-lookup"><span data-stu-id="e2225-120">Step 1: Use migration assistant to fetch and migrate the Web Client configurations</span></span>

1. <span data-ttu-id="e2225-121">Run **UCMigrationTool.exe**.</span><span class="sxs-lookup"><span data-stu-id="e2225-121">Run **UCMigrationTool.exe**.</span></span>

2. <span data-ttu-id="e2225-122">In the introduction screen, select **Continue**.</span><span class="sxs-lookup"><span data-stu-id="e2225-122">In the introduction screen, select **Continue**.</span></span>

3. <span data-ttu-id="e2225-123">In the **Login** screen, provide authentication details to connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance from where you want to fetch and migrate the configurations.</span><span class="sxs-lookup"><span data-stu-id="e2225-123">In the **Login** screen, provide authentication details to connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance from where you want to fetch and migrate the configurations.</span></span> <span data-ttu-id="e2225-124">If you have multiple organizations, and want to select the organization where you want to fetch and migrate the configurations, select the **Display list of available organizations** check box, and select **Login**.</span><span class="sxs-lookup"><span data-stu-id="e2225-124">If you have multiple organizations, and want to select the organization where you want to fetch and migrate the configurations, select the **Display list of available organizations** check box, and select **Login**.</span></span></br>
<span data-ttu-id="e2225-125">![Migration Assistant Login screen](../media/usd-migration-assistant-login.PNG "Migration Assistant Login Screen")</span><span class="sxs-lookup"><span data-stu-id="e2225-125">![Migration Assistant Login screen](../media/usd-migration-assistant-login.PNG "Migration Assistant Login Screen")</span></span>

4. <span data-ttu-id="e2225-126">In the **Export Configurations** screen, select **Export**.</span><span class="sxs-lookup"><span data-stu-id="e2225-126">In the **Export Configurations** screen, select **Export**.</span></span></br>
<span data-ttu-id="e2225-127">**Data file location** is the location where the migration assistant stores the **Data.zip** folder, which contains the configurations that you export from the Web Client.</span><span class="sxs-lookup"><span data-stu-id="e2225-127">**Data file location** is the location where the migration assistant stores the **Data.zip** folder, which contains the configurations that you export from the Web Client.</span></span></br>
<span data-ttu-id="e2225-128">When the export is successfully completed, select **Next**.</span><span class="sxs-lookup"><span data-stu-id="e2225-128">When the export is successfully completed, select **Next**.</span></span></br>
<span data-ttu-id="e2225-129">![Export configurations screen](../media/usd-migration-assistant-export-configurations.PNG "Export configurations screen")</span><span class="sxs-lookup"><span data-stu-id="e2225-129">![Export configurations screen](../media/usd-migration-assistant-export-configurations.PNG "Export configurations screen")</span></span>

5. <span data-ttu-id="e2225-130">In the **Select Configurations** screen, select the configuration elements (hosted controls) you want to migrate, and select **Next**.</span><span class="sxs-lookup"><span data-stu-id="e2225-130">In the **Select Configurations** screen, select the configuration elements (hosted controls) you want to migrate, and select **Next**.</span></span></br><span data-ttu-id="e2225-131">This is a multi-select list, and you can select several configuration elements to migrate.</span><span class="sxs-lookup"><span data-stu-id="e2225-131">This is a multi-select list, and you can select several configuration elements to migrate.</span></span>
</br><span data-ttu-id="e2225-132">The migration assistant displays only the hosted controls to select.</span><span class="sxs-lookup"><span data-stu-id="e2225-132">The migration assistant displays only the hosted controls to select.</span></span> <span data-ttu-id="e2225-133">If you select a hosted control, the migration assistant exports all the actions, action calls, events, and other elements associated with the particular hosted control.</span><span class="sxs-lookup"><span data-stu-id="e2225-133">If you select a hosted control, the migration assistant exports all the actions, action calls, events, and other elements associated with the particular hosted control.</span></span></br>
<span data-ttu-id="e2225-134">![Select configurations screen](../media/usd-migration-assistant-select-configurations.PNG "Select configurations screen")</span><span class="sxs-lookup"><span data-stu-id="e2225-134">![Select configurations screen](../media/usd-migration-assistant-select-configurations.PNG "Select configurations screen")</span></span>

6. <span data-ttu-id="e2225-135">In the **Confirm Selection** screen, review the configurations you selected for migration, and select **Next**.</span><span class="sxs-lookup"><span data-stu-id="e2225-135">In the **Confirm Selection** screen, review the configurations you selected for migration, and select **Next**.</span></span> <span data-ttu-id="e2225-136">If you want to change the selection, select **Previous** and repeat step 5.</span><span class="sxs-lookup"><span data-stu-id="e2225-136">If you want to change the selection, select **Previous** and repeat step 5.</span></span>

7. <span data-ttu-id="e2225-137">In the **Migrate Configurations** screen, choose **Migrate**.</span><span class="sxs-lookup"><span data-stu-id="e2225-137">In the **Migrate Configurations** screen, choose **Migrate**.</span></span> <span data-ttu-id="e2225-138">After the migration is completed, select **Next**.</span><span class="sxs-lookup"><span data-stu-id="e2225-138">After the migration is completed, select **Next**.</span></span></br>
<span data-ttu-id="e2225-139">![Migrate configurations screen](../media/usd-migration-assistant-migrate.PNG "Migrate configurations screen")</span><span class="sxs-lookup"><span data-stu-id="e2225-139">![Migrate configurations screen](../media/usd-migration-assistant-migrate.PNG "Migrate configurations screen")</span></span>

8. <span data-ttu-id="e2225-140">In the **File Download** screen, the migration assistant provides a default location to download the **USD_UI_Configurations.zip** folder.</span><span class="sxs-lookup"><span data-stu-id="e2225-140">In the **File Download** screen, the migration assistant provides a default location to download the **USD_UI_Configurations.zip** folder.</span></span> <span data-ttu-id="e2225-141">To change the default download location, select **Browse** and choose a location, and select **Download File**.</span><span class="sxs-lookup"><span data-stu-id="e2225-141">To change the default download location, select **Browse** and choose a location, and select **Download File**.</span></span></br>
<span data-ttu-id="e2225-142">The migration assistant displays the **Download Completed**.</span><span class="sxs-lookup"><span data-stu-id="e2225-142">The migration assistant displays the **Download Completed**.</span></span></br>
<span data-ttu-id="e2225-143">![File Download screen](../media/usd-migration-assistant-download-file.PNG "File Download screen")</span><span class="sxs-lookup"><span data-stu-id="e2225-143">![File Download screen](../media/usd-migration-assistant-download-file.PNG "File Download screen")</span></span>

9. <span data-ttu-id="e2225-144">Select **Exit** to close and exit the tool.</span><span class="sxs-lookup"><span data-stu-id="e2225-144">Select **Exit** to close and exit the tool.</span></span>

## <a name="step-2-import-the-usdwebresources-folder"></a><span data-ttu-id="e2225-145">Step 2: Import the USDWebResources folder</span><span class="sxs-lookup"><span data-stu-id="e2225-145">Step 2: Import the USDWebResources folder</span></span>

<span data-ttu-id="e2225-146">The **USDWebResources** folder contains the migrated **RunXrmCommand** actions that were present in Web Client.</span><span class="sxs-lookup"><span data-stu-id="e2225-146">The **USDWebResources** folder contains the migrated **RunXrmCommand** actions that were present in Web Client.</span></span> <span data-ttu-id="e2225-147">To deploy the **USDWebResources** on the target Unified Intrface App, import the web resources as a solution in the Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="e2225-147">To deploy the **USDWebResources** on the target Unified Intrface App, import the web resources as a solution in the Dynamics 365 for Customer Engagement apps.</span></span>

<span data-ttu-id="e2225-148">To import the **USDWebResources** zip folder, follow these steps:</span><span class="sxs-lookup"><span data-stu-id="e2225-148">To import the **USDWebResources** zip folder, follow these steps:</span></span>

1. <span data-ttu-id="e2225-149">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e2225-149">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>

2. <span data-ttu-id="e2225-150">Go to **Settings** > **Solutions**.</span><span class="sxs-lookup"><span data-stu-id="e2225-150">Go to **Settings** > **Solutions**.</span></span>

3. <span data-ttu-id="e2225-151">Select **Import** to import the web resource.</span><span class="sxs-lookup"><span data-stu-id="e2225-151">Select **Import** to import the web resource.</span></span>

4. <span data-ttu-id="e2225-152">In the **Select Solution Package** window, browse and select the **USDWebResources** zip folder, and select **Next**.</span><span class="sxs-lookup"><span data-stu-id="e2225-152">In the **Select Solution Package** window, browse and select the **USDWebResources** zip folder, and select **Next**.</span></span>

5. <span data-ttu-id="e2225-153">In the **Solution Information** screen, review the solution information and select **Import**.</span><span class="sxs-lookup"><span data-stu-id="e2225-153">In the **Solution Information** screen, review the solution information and select **Import**.</span></span></br>
<span data-ttu-id="e2225-154">You can see the success message after the solution is imported successfully.</span><span class="sxs-lookup"><span data-stu-id="e2225-154">You can see the success message after the solution is imported successfully.</span></span>

6. <span data-ttu-id="e2225-155">In the **Importing Solution** screen, select **Close**.</span><span class="sxs-lookup"><span data-stu-id="e2225-155">In the **Importing Solution** screen, select **Close**.</span></span>

<span data-ttu-id="e2225-156">You can see the **USDWebResources** in the solutions list.</span><span class="sxs-lookup"><span data-stu-id="e2225-156">You can see the **USDWebResources** in the solutions list.</span></span></br>

<span data-ttu-id="e2225-157">![USDWebResource imported to Dynamics 365 for Customer Engagement apps](../media/usd-configuration-migration-webresources-import.PNG "USDWebResource imported to Dynamics 365 for Customer Engagement apps")</span><span class="sxs-lookup"><span data-stu-id="e2225-157">![USDWebResource imported to Dynamics 365 for Customer Engagement apps](../media/usd-configuration-migration-webresources-import.PNG "USDWebResource imported to Dynamics 365 for Customer Engagement apps")</span></span>

<span data-ttu-id="e2225-158">For more information, see [Import, update, and export solutions](/dynamics365/customer-engagement/customize/import-update-export-solutions)</span><span class="sxs-lookup"><span data-stu-id="e2225-158">For more information, see [Import, update, and export solutions](/dynamics365/customer-engagement/customize/import-update-export-solutions)</span></span>

## <a name="step-3-use-configuration-migration-tool-to-import-and-deploy-the-configurations-on-unified-interface-app"></a><span data-ttu-id="e2225-159">Step 3: Use Configuration Migration Tool to import and deploy the configurations on Unified Interface App</span><span class="sxs-lookup"><span data-stu-id="e2225-159">Step 3: Use Configuration Migration Tool to import and deploy the configurations on Unified Interface App</span></span>

<span data-ttu-id="e2225-160">**Prerequesites:** Download the Configuration Migration tool (DataMigrationUtility.exe).</span><span class="sxs-lookup"><span data-stu-id="e2225-160">**Prerequesites:** Download the Configuration Migration tool (DataMigrationUtility.exe).</span></span> <span data-ttu-id="e2225-161">To download the tool, see [Download the tools from NuGet](/dynamics365/customer-engagement/developer/download-tools-nuget).</span><span class="sxs-lookup"><span data-stu-id="e2225-161">To download the tool, see [Download the tools from NuGet](/dynamics365/customer-engagement/developer/download-tools-nuget).</span></span>

1. <span data-ttu-id="e2225-162">Go to the location where you downloaded the Configuration Migration Tool (DataMigrationUtility.exe).</span><span class="sxs-lookup"><span data-stu-id="e2225-162">Go to the location where you downloaded the Configuration Migration Tool (DataMigrationUtility.exe).</span></span>

2. <span data-ttu-id="e2225-163">Open **ConfigurationMigration** and execute **DataMigrationUtility.exe**.</span><span class="sxs-lookup"><span data-stu-id="e2225-163">Open **ConfigurationMigration** and execute **DataMigrationUtility.exe**.</span></span> 

3. <span data-ttu-id="e2225-164">In the next screen, select **Import data**, and select **Continue**.</span><span class="sxs-lookup"><span data-stu-id="e2225-164">In the next screen, select **Import data**, and select **Continue**.</span></span></br>
<span data-ttu-id="e2225-165">![Configuration Migration Tool options screen](../media/usd-configuration-migration-tool-options.PNG "Configuration Migration Tool options data screen")</span><span class="sxs-lookup"><span data-stu-id="e2225-165">![Configuration Migration Tool options screen](../media/usd-configuration-migration-tool-options.PNG "Configuration Migration Tool options data screen")</span></span>

4. <span data-ttu-id="e2225-166">In the **Login** screen, provide authentication details to connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance to which you want to deploy the migrated configurations.</span><span class="sxs-lookup"><span data-stu-id="e2225-166">In the **Login** screen, provide authentication details to connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance to which you want to deploy the migrated configurations.</span></span> <span data-ttu-id="e2225-167">If you have multiple organizations, and want to select the organization to which you want to deploy the migrated configurations, select the **Display list of available organizations** check box, and select **Login**.</span><span class="sxs-lookup"><span data-stu-id="e2225-167">If you have multiple organizations, and want to select the organization to which you want to deploy the migrated configurations, select the **Display list of available organizations** check box, and select **Login**.</span></span></br>
<span data-ttu-id="e2225-168">![Configuration Migration Tool login screen](../media/usd-configuration-migration-tool-login.PNG "Configuration Migration Tool login screen")</span><span class="sxs-lookup"><span data-stu-id="e2225-168">![Configuration Migration Tool login screen](../media/usd-configuration-migration-tool-login.PNG "Configuration Migration Tool login screen")</span></span>

5. <span data-ttu-id="e2225-169">In the next screen, browse the **USD_UI_Configurations** folder and select the **Data.zip** folder, and then select **Import Data**.</span><span class="sxs-lookup"><span data-stu-id="e2225-169">In the next screen, browse the **USD_UI_Configurations** folder and select the **Data.zip** folder, and then select **Import Data**.</span></span></br>
<span data-ttu-id="e2225-170">![Browse and select data.zip folder](../media/usd-configuration-migration-tool-import-data.PNG "Browse and select data.zip folder")</span><span class="sxs-lookup"><span data-stu-id="e2225-170">![Browse and select data.zip folder](../media/usd-configuration-migration-tool-import-data.PNG "Browse and select data.zip folder")</span></span>

6. <span data-ttu-id="e2225-171">After the import is complete, select **Exit**.</span><span class="sxs-lookup"><span data-stu-id="e2225-171">After the import is complete, select **Exit**.</span></span></br>
<span data-ttu-id="e2225-172">![Importing is completed. Select Exit](../media/usd-configuration-migration-tool-import-complete.PNG "Importing is completed. Select Exit")</span><span class="sxs-lookup"><span data-stu-id="e2225-172">![Importing is completed. Select Exit](../media/usd-configuration-migration-tool-import-complete.PNG "Importing is completed. Select Exit")</span></span>

## <a name="test-the-deployment-of-the-configurations-on-the-target-unified-interface-app"></a><span data-ttu-id="e2225-173">Test the deployment of the configurations on the target Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="e2225-173">Test the deployment of the configurations on the target Unified Interface App.</span></span>

1. <span data-ttu-id="e2225-174">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="e2225-174">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>

2. [!INCLUDE[proc_settings_usd](../../includes/proc-settings-usd.md)]

3. <span data-ttu-id="e2225-175">Select configurations that you migrated from the Web Client.</span><span class="sxs-lookup"><span data-stu-id="e2225-175">Select configurations that you migrated from the Web Client.</span></span></br>
<span data-ttu-id="e2225-176">For example, the selected configuration elements are as follows:</span><span class="sxs-lookup"><span data-stu-id="e2225-176">For example, the selected configuration elements are as follows:</span></span>

  |<span data-ttu-id="e2225-177">Configuration Name</span><span class="sxs-lookup"><span data-stu-id="e2225-177">Configuration Name</span></span>|<span data-ttu-id="e2225-178">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e2225-178">Description</span></span>|
  |-------|-------|
  |<span data-ttu-id="e2225-179">KB Article</span><span class="sxs-lookup"><span data-stu-id="e2225-179">KB Article</span></span>| <span data-ttu-id="e2225-180">Trang CRM</span><span class="sxs-lookup"><span data-stu-id="e2225-180">CRM Page</span></span>|
  |<span data-ttu-id="e2225-181">KB Search</span><span class="sxs-lookup"><span data-stu-id="e2225-181">KB Search</span></span>| <span data-ttu-id="e2225-182">Kiểm soát KM</span><span class="sxs-lookup"><span data-stu-id="e2225-182">KM Control</span></span>|

  </br><span data-ttu-id="e2225-183">![Select configurations](../media/usd-migration-assistant-selected-configurations.PNG "Selected configurations")</span><span class="sxs-lookup"><span data-stu-id="e2225-183">![Select configurations](../media/usd-migration-assistant-selected-configurations.PNG "Selected configurations")</span></span></br>
 <span data-ttu-id="e2225-184">You must select **Hosted Controls** to verify.</span><span class="sxs-lookup"><span data-stu-id="e2225-184">You must select **Hosted Controls** to verify.</span></span></br></br>
<span data-ttu-id="e2225-185">You can see configurations are migrated to Unified Interface specific elements.</span><span class="sxs-lookup"><span data-stu-id="e2225-185">You can see configurations are migrated to Unified Interface specific elements.</span></span>

  |<span data-ttu-id="e2225-186">Configuration Name</span><span class="sxs-lookup"><span data-stu-id="e2225-186">Configuration Name</span></span>|<span data-ttu-id="e2225-187">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e2225-187">Description</span></span>|
  |-------|-------|
  |<span data-ttu-id="e2225-188">KB Article</span><span class="sxs-lookup"><span data-stu-id="e2225-188">KB Article</span></span>| <span data-ttu-id="e2225-189">Unified Interface Page</span><span class="sxs-lookup"><span data-stu-id="e2225-189">Unified Interface Page</span></span>|
  |<span data-ttu-id="e2225-190">KB Search</span><span class="sxs-lookup"><span data-stu-id="e2225-190">KB Search</span></span>| <span data-ttu-id="e2225-191">Unified Interface KM Control</span><span class="sxs-lookup"><span data-stu-id="e2225-191">Unified Interface KM Control</span></span>|
  
  </br><span data-ttu-id="e2225-192">![Verifying the configuration migration](../media/usd-configuration-migration-verification.PNG "Verifying the configuration migration")</span><span class="sxs-lookup"><span data-stu-id="e2225-192">![Verifying the configuration migration](../media/usd-configuration-migration-verification.PNG "Verifying the configuration migration")</span></span>

## <a name="see-also"></a><span data-ttu-id="e2225-193">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e2225-193">See also</span></span>

[<span data-ttu-id="e2225-194">Migration of Unified Service Desk configurations from Dynamics 365 for Customer Engagement Web Client to Dynamics 365 for Customer Engagement apps (Unified Interface apps)</span><span class="sxs-lookup"><span data-stu-id="e2225-194">Migration of Unified Service Desk configurations from Dynamics 365 for Customer Engagement Web Client to Dynamics 365 for Customer Engagement apps (Unified Interface apps)</span></span>](overview-migration-assistant.md)

[<span data-ttu-id="e2225-195">Download the Web Client - Unified Interface Migration Assistant</span><span class="sxs-lookup"><span data-stu-id="e2225-195">Download the Web Client - Unified Interface Migration Assistant</span></span>](download-migration-assistant.md)

[<span data-ttu-id="e2225-196">Download the tools from NuGet</span><span class="sxs-lookup"><span data-stu-id="e2225-196">Download the tools from NuGet</span></span>](/dynamics365/customer-engagement/developer/download-tools-nuget)

[<span data-ttu-id="e2225-197">Import configuration data</span><span class="sxs-lookup"><span data-stu-id="e2225-197">Import configuration data</span></span>](/dynamics365/customer-engagement/admin/import-configuration-data)
