---
title: 'Sample: Retrieve currency exchange rate (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to create a new currency, and how to retrieve and display the currency exchange rate relative to the organization’s base currency.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d071fe46-4d71-4fd1-95b8-069bd4a96f8d
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7b2932256562bab29d60728fce55ca7cdd29ead5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386609"
---
# <a name="sample-retrieve-currency-exchange-rate"></a>Sample: Retrieve currency exchange rate

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample here [Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).  

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create a new currency, and how to retrieve and display the currency exchange rate relative to the organization’s base currency.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[BusinessManagement#TransactionCurrencyExchangeRate](../snippets/csharp/CRMV8/businessmanagement/cs/transactioncurrencyexchangerate.cs#transactioncurrencyexchangerate)]  
  
### <a name="see-also"></a>Xem thêm  
 [Transaction Currency (Currency) Entity](transaction-currency-currency-entity.md)   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveExchangeRateRequest>
