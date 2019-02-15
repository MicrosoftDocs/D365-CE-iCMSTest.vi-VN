---
title: 'Sample: Export ribbon definitions (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample shows how to export Ribbon definitions. It uses the RetrieveApplicationRibbonRequest and RetrieveEntityRibbonRequest messages. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a657c8bb-dbeb-461f-8271-d07a97c3ea0e
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1a87fc57d33ef0bfd23a7b279280c81a28fd474c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388721"
---
# <a name="sample-export-ribbon-definitions"></a>Sample: Export ribbon definitions

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. [Download the Export ribbon definitions sample](https://code.msdn.microsoft.com/Export-ribbon-definitions-df97a4cb).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to export Ribbon definitions. It uses the <xref:Microsoft.Crm.Sdk.Messages.RetrieveApplicationRibbonRequest> and <xref:Microsoft.Crm.Sdk.Messages.RetrieveEntityRibbonRequest> messages.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[ExportRibbonXml#ExportRibbonXml](../../snippets/csharp/CRMV8/exportribbonxml/cs/exportribbonxml.cs#exportribbonxml)]  
  
### <a name="see-also"></a>Xem thêm  
 [Customize commands and the ribbon](customize-commands-ribbon.md)   
 [Pass Parameters to a URL By Using the Ribbon](pass-parameters-url-by-using-ribbon.md)   
 [Ribbon core schema](ribbon-core-schema.md) [Ribbon types schema](ribbon-types-schema.md) [Ribbon WSS schema](ribbon-wss-schema.md) <xref:Microsoft.Crm.Sdk.Messages.RetrieveApplicationRibbonRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveEntityRibbonRequest>
