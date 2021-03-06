---
title: Download and Install Best Practices Analyzer | MicrosoftDocs
description: Learn about downloading and installing the Best Practices Analyzer.
keywords: ''
ms.date: 08/17/2018
ms.service:
- usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: B96D2870-9475-475B-B37B-221C3EC55D45
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 321786cca04d3344cff093cd413d329d212091ff
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382378"
---
# <a name="download-and-install-best-practices-analyzer"></a>Download and Install Best Practices Analyzer

## <a name="includepn-best-practices-analyzerincludespn-best-practices-analyzermd-support-matrix-and-download-location"></a>[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] support matrix and download location

The table provides where you can download [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] for various versions of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].


|Kịch bản | Mô tả |[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]| Download Location|
|---------|-------------|------------------------------------------------------------------------------|------------------|
|Available through sample application package | [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] is part of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] – Microsoft Dynamics 365 for Customer Engagement apps Web client sample application | [!INCLUDE[pn-unified-service-desk-4-0](../../includes/pn-unified-service-desk-4-0.md)] | [Download](https://go.microsoft.com/fwlink/?linkid=2007340) |
| Available through [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] package |                          [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] is available as a download package |[!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)]  <br>  [!INCLUDE[pn-unified-service-desk-3-2](../../includes/pn-unified-service-desk-3-2.md)] <br> [!INCLUDE[pn-unified-service-desk-3-1](../../includes/pn-unified-service-desk-3-1.md)] <br> [!INCLUDE[pn-unified-service-desk-3-0](../../includes/pn-unified-service-desk-3-0.md)] <br> [!INCLUDE[pn-unified-service-desk-2-2](../../includes/pn-unified-service-desk-2-2.md)] | [Download](https://go.microsoft.com/fwlink/p/?linkid=872089) |

## <a name="install-includepn-best-practices-analyzerincludespn-best-practices-analyzermd"></a>Cài đặt [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)]

Before you can install and deploy [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)], you must download [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] package specific to your [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] version. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Download Best Practices Analyzer](#download-best-practices-analyzer)

### <a name="best-practices-analyzer-for-unified-service-desk-40"></a>Best Practices Analyzer for Unified Service Desk 4.0

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] for [!INCLUDE[pn-unified-service-desk-4-0](../../includes/pn-unified-service-desk-4-0.md)] is available in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Web Client sample package.

You can deploy a [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] sample package using Package Deployer. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Deploy sample Unified Service Desk applications using Package Deployer](../admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md)

> [!Note]
> After you upgrade to [!INCLUDE[pn-unified-service-desk-4-0](../../includes/pn-unified-service-desk-4-0.md)], you can also download the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] package and follow the procedure mentioned in section [Best Practices Analyzer for Unified Service Desk 3.3 or lower version](#best-practices-analyzer-for-unified-service-desk-3.3-or-lower-version) to install [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)].

### <a name="best-practices-analyzer-for-unified-service-desk-33-or-lower-version"></a>Best Practices Analyzer for Unified Service Desk 3.3 or lower version

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] for [!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)] or lower versions is available as a separate download package.

Download the sample zip package for [!INCLUDE[pn-unified-service-desk-3-3](../../includes/pn-unified-service-desk-3-3.md)] or lower versions and extract the package. After extracting the zip package, you can see the following:

-  **BestPracticesAnalyzerPackage** folder
- `Microsoft.Crm.UnifiedServiceDesk.Packages.BestPracticesAnalyzerPackage.dll` file

Copy the folder and .dll file, and paste in your **PkgConfig** folder. After copying the folder and .dll file, deploy the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] sample package using Package Deployer.

After deploying the sample package using Package Deployer, perform the walkthrough to configure the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] in your agent application. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Walkthrough: Configure Best Practices Analyzer](../admin/walkthrough-configure-best-practices-analyzer.md)

> [!Note]
> The [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] support is available until [!INCLUDE[pn-unified-service-desk-2-2](../../includes/pn-unified-service-desk-2-2.md)]

## <a name="see-also"></a>Xem thêm

[Analyze best practices in Unified Service Desk](../admin/analyze-best-practices-unified-service-desk.md)

[Walkthrough: Configure Best Practices Analyzer](../admin/walkthrough-configure-best-practices-analyzer.md)

[Read Best Practices Analyzer report](../admin/read-best-practices-analyzer-report.md)

[Best practice rule categories and parameters](../admin/compliance-categories-parameters-bpa.md)

[System configurations](../admin/system-configurations-bpa.md)

[Internet Explorer settings](../admin/internet-explorer-settings-bpa.md)

[Unified Service Desk configurations](../admin/unified-service-desk-configurations-bpa.md)
