---
title: 'Sample: Dump global option set information to a file | MicrosoftDocs'
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2016
- Dynamics CRM Online
ms.assetid: b9437469-70b5-4a3c-ae49-115522fb5cee
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: aeeeafdc96064d7d6e7467bc8c2b11f8d8cbf443
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387337"
---
# <a name="sample-dump-global-option-set-information-to-a-file"></a><span data-ttu-id="2a54d-102">Sample: Dump global option set information to a file</span><span class="sxs-lookup"><span data-stu-id="2a54d-102">Sample: Dump global option set information to a file</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2a54d-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2a54d-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="2a54d-104">Download the sample: [Work with global option sets](https://code.msdn.microsoft.com/Samples-of-option-set-37c4b418).</span><span class="sxs-lookup"><span data-stu-id="2a54d-104">Download the sample: [Work with global option sets](https://code.msdn.microsoft.com/Samples-of-option-set-37c4b418).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="2a54d-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="2a54d-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="2a54d-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="2a54d-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="2a54d-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="2a54d-107">Demonstrates</span></span>  
 <span data-ttu-id="2a54d-108">This sample shows how to write out all the global OptionSet metadata to an XML file.</span><span class="sxs-lookup"><span data-stu-id="2a54d-108">This sample shows how to write out all the global OptionSet metadata to an XML file.</span></span> <span data-ttu-id="2a54d-109">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllOptionSetsRequest> message.</span><span class="sxs-lookup"><span data-stu-id="2a54d-109">It uses the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllOptionSetsRequest> message.</span></span>  
  
 <span data-ttu-id="2a54d-110">The following sample creates a new file at `\OptionSets\bin\Debug\AllOptionSetValues.xml`.</span><span class="sxs-lookup"><span data-stu-id="2a54d-110">The following sample creates a new file at `\OptionSets\bin\Debug\AllOptionSetValues.xml`.</span></span> <span data-ttu-id="2a54d-111">You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report.</span><span class="sxs-lookup"><span data-stu-id="2a54d-111">You can open this file in [!INCLUDE[pn_MS_Excel_Full](../../includes/pn-ms-excel-full.md)] to see a tabular report.</span></span> <span data-ttu-id="2a54d-112">You may need this information to discover the entity type code for a custom entity for use in reports.</span><span class="sxs-lookup"><span data-stu-id="2a54d-112">You may need this information to discover the entity type code for a custom entity for use in reports.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2a54d-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="2a54d-113">Example</span></span>  
 [!code-csharp[optionsets#DumpOptionSetInfo](../../snippets/csharp/CRMV8/optionsets/cs/dumpoptionsetinfo.cs#dumpoptionsetinfo)]  
  
### <a name="see-also"></a><span data-ttu-id="2a54d-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2a54d-114">See also</span></span>  
 <span data-ttu-id="2a54d-115">[Use the Organization service with Dynamics 365 for Customer Engagement apps metadata](use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="2a54d-115">[Use the Organization service with Dynamics 365 for Customer Engagement apps metadata](use-organization-service-metadata.md) </span></span>  
 <span data-ttu-id="2a54d-116">[Customize Global Option Sets in Dynamics 365 for Customer Engagement apps](../org-service/customize-global-option-sets.md) </span><span class="sxs-lookup"><span data-stu-id="2a54d-116">[Customize Global Option Sets in Dynamics 365 for Customer Engagement apps](../org-service/customize-global-option-sets.md) </span></span>  
 [<span data-ttu-id="2a54d-117">Global Option Set Messages</span><span class="sxs-lookup"><span data-stu-id="2a54d-117">Global Option Set Messages</span></span>](customize-global-option-sets.md#messages)   
