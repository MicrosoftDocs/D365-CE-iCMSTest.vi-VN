---
title: Analyze best practices in Unified Service Desk (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the best practices analyzer, which performs analysis on the Internet Explorer settings, Unified Service Desk configurations in Dynamics 365 for Customer Engagement apps, and system configurations on which you install Unified Service Desk, and displays a report to review and mitigate the issues.
ms.custom: ''
ms.date: 04/24/2018
ms.service: usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 8ED5D0F6-4A3E-49FA-A399-0AEDFF2236AA
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 975589c8cbc9b8e41d646a5db72432e7424e3bf8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382479"
---
# <a name="analyze-best-practices-in-includepnunifiedservicedeskincludespn-unified-service-deskmd"></a>Analyze best practices in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]

Best practices are the guidelines about System Configurations, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], Internet Explorer settings, and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations in Dynamics 365 for Customer Engagement apps. Consider these guidelines as our recommended way to use [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and serve your customers.

Although deviating from best practices may not necessarily lead to a breakdown, they indicate crucial parameters that can result in poor performance, poor reliability, unexpected conflicts, increased security risks, or other potential problems. 

## <a name="what-is-includepn-best-practices-analyzerincludespn-best-practices-analyzermd-for-includepnunifiedservicedeskincludespn-unified-service-deskmd"></a>What is [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] analyzes the compliance of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] with best practice rules in certain categories. The [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] displays the results of analysis in the form of a report with severity levels, description of the parameter, and mitigation for the non-compliant / problematic areas.

The following table lists the categories against which [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] analyzes the compliance of best practice rules.


|                                         Category name                                         |                                                                                                                                        Mô tả                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Configurations | [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Configurations are the configurations (hosted controls, actions, events, and so on) that you configure for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] in Dynamics 365 for Customer Engagement apps. |
|                                     System configurations                                     |                                          System configurations are the information about local computer hardware (RAM, operating system, and so on), and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] version.                                          |
|                                  Internet Explorer settings                                   |                                                                              Internet Explorer settings are the settings (General, Security, Advanced, and so on) that you configure for Internet Explorer.                                                                               |

The following table lists the results of Severity level analysis.


| Severity category |                                                                                                                                                                                      Mô tả                                                                                                                                                                                       |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|       Pass        |                                                                                                                                                 The report displays a pass result when a parameter satisfies the recommended criteria.                                                                                                                                                 |
|      Cảnh báo      | The report displays a warning result when a parameter doesn't satisfy the recommended criteria and due to which [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can encounter potential issues. Using recommended value settings for parameters helps [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to perform better. |
|       Lỗi       |                                                                                                                                             The report displays an error result when a parameter doesn't satisfy the recommended criteria.                                                                                                                                             |

## <a name="see-also"></a>Xem thêm

[Download and install Best Practices Analyzer](../admin/download-install-best-practices-analyzer.md)

[Walkthrough: Configure Best Practices Analyzer](../admin/walkthrough-configure-best-practices-analyzer.md)

[Read Best Practices Analyzer report](../admin/read-best-practices-analyzer-report.md)

[Best practice rule categories and parameters](../admin/compliance-categories-parameters-bpa.md)

[System configurations](../admin/system-configurations-bpa.md)

[Internet Explorer settings](../admin/internet-explorer-settings-bpa.md)

[Unified Service Desk configurations](../admin/unified-service-desk-configurations-bpa.md)
