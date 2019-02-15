---
title: Customization XML reference | MicrosoftDocs
description: 'The customizations.xml file is one of the files included in an exported unmanaged solution. The file contains all or selected portions of the customizations and configurations for your system. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: bcdcc975-4918-4513-b04a-6a9d3d04f08c
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 165b9884e72aa6a0af71a36423501f1c4f9d359a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385587"
---
# <a name="customization-xml-reference"></a>Customization XML reference

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

The customizations.xml file is one of the files included in an exported unmanaged solution. The file contains all or selected portions of the customizations and configurations for your system. 
  
 The solutions file is exported as a compressed .zip file. The contents of the unmanaged solutions file must be extracted before the customizations file can be edited. All the files of the unmanaged solution must be added to a compressed .zip file before it can be re-imported.  

> [!NOTE]
> - Editing a managed solution file is not supported.  
> - Not all elements of the customizations.xml file can be edited. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Support for Editing the Customization File](customize-dev/when-edit-customization-file.md)

## <a name="in-this-section"></a>In This Section

 [Ribbon core schema](customize-dev/ribbon-core-schema.md)  
 [Ribbon types schema](customize-dev/ribbon-types-schema.md)  
 [Ribbon WSS schema](customize-dev/ribbon-wss-schema.md)  
 [SiteMap schema](customize-dev/sitemap-schema.md)  
 [Form XML schema](customize-dev/form-xml-schema.md)  
 [FetchXML schema](org-service/fetchxml-schema.md)  

## <a name="related-sections"></a>Các phần liên quan

 [Schemas used in Dynamics 365 for Customer Engagement apps](schemas-used-dynamics-365.md)  
 [When to Edit the Customizations File](customize-dev/when-edit-customization-file.md)  
 [Edit the Customizations file with Schema Validation](customize-dev/edit-customizations-xml-file-schema-validation.md)  
 [Customize the Ribbon for Dynamics 365 for Customer Engagement apps](customize-dev/customize-commands-ribbon.md)  
 [Change Application Navigation using the SiteMap](/developer/customize-dev/change-application-navigation-using-sitemap.md)
