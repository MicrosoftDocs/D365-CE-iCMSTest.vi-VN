---
title: Download the Web Client - Unified Interface Migration Assistant | MicrosoftDocs
description: Download Web Client - Unified Interface Migration Assistant to migrate your Unified Service Desk configurations from Dynamics 365 for Customer Engagement Web Client to Unified Interface App
keywords: ''
ms.date: 07/30/2018
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
ms.assetid: AC23FCF9-5B36-4C1B-9B29-31F93ADEB3AF
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 3187ada9d51faef686a4e075a9037e12b824c42e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382602"
---
# <a name="download-migration-assistant-to-migrate-unified-service-desk-configurations-from-web-client-to-unified-interface-app"></a>Download Migration Assistant to migrate Unified Service Desk configurations from Web Client to Unified Interface App

## <a name="download-web-client---unified-interface-migration-assistant"></a>Download Web Client - Unified Interface Migration Assistant

The Web Client - Unified Interface Migration Assistant is an executable file that you can download and save on your machine. After downloading, you can run the executable file to start the migration process.

Download the [Web Client – Unified Interface Migration Assistant](https://go.microsoft.com/fwlink/?linkid=2005839).

## <a name="download-configuration-migration-tool"></a>Download Configuration Migration Tool

The migration of Unified Service Desk configurations from Dynamics 365 for Customer Engagement apps Web Client to Unified Interface App is a three step process:

- Fetch and migrate the configuration elements to a **USD_UI_Configurations** folder using the Web Client - Unified Interface Migration Assistant.
- Import the **USDWebResources** folder, which is in the **USD_UI_Configurations** folder, using the **Solutions** option in the Dynamics 365 for Customer Engagement apps.
- Import the **Data** zip folder from the **USD_UI_Configurations** folder to the Unified Interface App using the Configuration Migration Tool (DataMigrationUtility.exe).

You must download the Configuration Migration Tool (DataMigrationUtility.exe), which is available as a [NuGet package](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.ConfigurationMigration.Wpf). 

To download the tool, see [Download the tools from NuGet](/dynamics365/customer-engagement/developer/download-tools-nuget). Follow the steps on this page to extract the Configuration Migration Tool (DataMigrationUtility.exe).

> [!div class="nextstepaction"]
> [How to migrate the configurations](migration-steps-web-client-unified-interface-configuration.md)

## <a name="see-also"></a>Xem thêm

[Migration of Unified Service Desk configurations from Dynamics 365 for Customer Engagement apps Web Client to Dynamics 365 for Customer Engagement apps (Unified Interface apps)](overview-migration-assistant.md)

[Migration steps of the configurations from Dynamics 365 for Customer Engagement apps Web Client to Unified Interface App](migration-steps-web-client-unified-interface-configuration.md)
