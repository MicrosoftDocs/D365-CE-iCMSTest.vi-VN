---
title: 'Sample: Install or remove sample data (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: Sample code to install standard sample data for Customer Engagement (online).
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ab035539-7158-4efb-ad4c-86cb87eb2e0f
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 20
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: eef29edc81404ae34bb1f96ad9a660afbd847a32
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387097"
---
# <a name="sample-install-or-remove-sample-data"></a>Sample: Install or remove sample data

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the sample: [Work with installing or removing sample data](https://code.msdn.microsoft.com/Sample-Install-or-remove-df7cf89f).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to install or uninstall the sample data for an organization by using the <xref:Microsoft.Crm.Sdk.Messages.InstallSampleDataRequest> message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Other#ImportOrRemoveSampleData](../snippets/csharp/CRMV8/other/cs/importorremovesampledata.cs#importorremovesampledata)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Data for Dynamics 365 for Customer Engagement apps](sample-data.md)   
 <xref:Microsoft.Crm.Sdk.Messages.InstallSampleDataRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.UninstallSampleDataRequest>
