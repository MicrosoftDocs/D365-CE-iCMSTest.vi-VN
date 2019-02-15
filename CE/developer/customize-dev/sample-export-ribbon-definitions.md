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
# <a name="sample-export-ribbon-definitions"></a><span data-ttu-id="d3532-104">Sample: Export ribbon definitions</span><span class="sxs-lookup"><span data-stu-id="d3532-104">Sample: Export ribbon definitions</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d3532-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="d3532-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="d3532-106">[Download the Export ribbon definitions sample](https://code.msdn.microsoft.com/Export-ribbon-definitions-df97a4cb).</span><span class="sxs-lookup"><span data-stu-id="d3532-106">[Download the Export ribbon definitions sample](https://code.msdn.microsoft.com/Export-ribbon-definitions-df97a4cb).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d3532-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="d3532-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="d3532-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="d3532-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="d3532-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="d3532-109">Demonstrates</span></span>  
 <span data-ttu-id="d3532-110">This sample shows how to export Ribbon definitions.</span><span class="sxs-lookup"><span data-stu-id="d3532-110">This sample shows how to export Ribbon definitions.</span></span> <span data-ttu-id="d3532-111">It uses the <xref:Microsoft.Crm.Sdk.Messages.RetrieveApplicationRibbonRequest> and <xref:Microsoft.Crm.Sdk.Messages.RetrieveEntityRibbonRequest> messages.</span><span class="sxs-lookup"><span data-stu-id="d3532-111">It uses the <xref:Microsoft.Crm.Sdk.Messages.RetrieveApplicationRibbonRequest> and <xref:Microsoft.Crm.Sdk.Messages.RetrieveEntityRibbonRequest> messages.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d3532-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d3532-112">Example</span></span>  
 [!code-csharp[ExportRibbonXml#ExportRibbonXml](../../snippets/csharp/CRMV8/exportribbonxml/cs/exportribbonxml.cs#exportribbonxml)]  
  
### <a name="see-also"></a><span data-ttu-id="d3532-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d3532-113">See also</span></span>  
 <span data-ttu-id="d3532-114">[Customize commands and the ribbon](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="d3532-114">[Customize commands and the ribbon](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="d3532-115">[Pass Parameters to a URL By Using the Ribbon](pass-parameters-url-by-using-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="d3532-115">[Pass Parameters to a URL By Using the Ribbon](pass-parameters-url-by-using-ribbon.md) </span></span>  
 <span data-ttu-id="d3532-116">[Ribbon core schema](ribbon-core-schema.md) [Ribbon types schema](ribbon-types-schema.md) [Ribbon WSS schema](ribbon-wss-schema.md) <xref:Microsoft.Crm.Sdk.Messages.RetrieveApplicationRibbonRequest> </span><span class="sxs-lookup"><span data-stu-id="d3532-116">[Ribbon core schema](ribbon-core-schema.md) [Ribbon types schema](ribbon-types-schema.md) [Ribbon WSS schema](ribbon-wss-schema.md) <xref:Microsoft.Crm.Sdk.Messages.RetrieveApplicationRibbonRequest> </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveEntityRibbonRequest>
