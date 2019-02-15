---
title: Handle exceptions in your code (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This article discusses the exceptions that are returned from a Dynamics 365 for Customer Engagement web service method call. The sample in this article highlights the common faults and exceptions that your application design should handle.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 02d0ad6c-eb76-4ea9-972f-c7647eef6c09
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f02b4a609b0a66bdbb37926e25aedf76137570e5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385494"
---
# <a name="handle-exceptions-in-your-code"></a><span data-ttu-id="8b968-104">Handle exceptions in your code</span><span class="sxs-lookup"><span data-stu-id="8b968-104">Handle exceptions in your code</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8b968-105">There are a number of exceptions that can be returned from a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web service method call.</span><span class="sxs-lookup"><span data-stu-id="8b968-105">There are a number of exceptions that can be returned from a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web service method call.</span></span> <span data-ttu-id="8b968-106">Your application design must catch and appropriately handle these exceptions.</span><span class="sxs-lookup"><span data-stu-id="8b968-106">Your application design must catch and appropriately handle these exceptions.</span></span> <span data-ttu-id="8b968-107">In the SDK .NET assemblies, all web service method calls use a communication channel to the server based on the [!INCLUDE[pn_WCF_long](../../includes/pn-wcf-long.md)] technology.</span><span class="sxs-lookup"><span data-stu-id="8b968-107">In the SDK .NET assemblies, all web service method calls use a communication channel to the server based on the [!INCLUDE[pn_WCF_long](../../includes/pn-wcf-long.md)] technology.</span></span> <span data-ttu-id="8b968-108">In WCF terms, exceptions returned from the channel are called *faults*.</span><span class="sxs-lookup"><span data-stu-id="8b968-108">In WCF terms, exceptions returned from the channel are called *faults*.</span></span>  

<a name="BKMK_Common"></a>   

## <a name="common-exceptions-and-faults"></a><span data-ttu-id="8b968-109">Common exceptions and faults</span><span class="sxs-lookup"><span data-stu-id="8b968-109">Common exceptions and faults</span></span>  

 <span data-ttu-id="8b968-110">The following code is used in most [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)] samples.</span><span class="sxs-lookup"><span data-stu-id="8b968-110">The following code is used in most [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)] samples.</span></span> <span data-ttu-id="8b968-111">It highlights the common faults and exceptions that your application design should handle.</span><span class="sxs-lookup"><span data-stu-id="8b968-111">It highlights the common faults and exceptions that your application design should handle.</span></span>  
  
 [!code-csharp[StrongTypes#CRUDOperations2](../../snippets/csharp/CRMV8/strongtypes/cs/crudoperations2.cs#crudoperations2)]  
  
> [!NOTE]
>  <span data-ttu-id="8b968-112">If you’re accessing the Discovery web service, your code should catch <xref:Microsoft.Xrm.Sdk.DiscoveryServiceFault> instead of the <xref:Microsoft.Xrm.Sdk.OrganizationServiceFault> fault shown previously.</span><span class="sxs-lookup"><span data-stu-id="8b968-112">If you’re accessing the Discovery web service, your code should catch <xref:Microsoft.Xrm.Sdk.DiscoveryServiceFault> instead of the <xref:Microsoft.Xrm.Sdk.OrganizationServiceFault> fault shown previously.</span></span>  
  
 <span data-ttu-id="8b968-113">In addition to these exceptions and faults, your code must handle the following exceptions:</span><span class="sxs-lookup"><span data-stu-id="8b968-113">In addition to these exceptions and faults, your code must handle the following exceptions:</span></span>  
  
- [<span data-ttu-id="8b968-114">SecurityTokenValidationException</span><span class="sxs-lookup"><span data-stu-id="8b968-114">SecurityTokenValidationException</span></span>](https://msdn.microsoft.com/library/system.identitymodel.tokens.securitytokenvalidationexception.aspx)  
  
- [<span data-ttu-id="8b968-115">ExpiredSecurityTokenException</span><span class="sxs-lookup"><span data-stu-id="8b968-115">ExpiredSecurityTokenException</span></span>](https://msdn.microsoft.com/library/system.servicemodel.security.expiredsecuritytokenexception.aspx)  
  
- [<span data-ttu-id="8b968-116">SecurityAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="8b968-116">SecurityAccessDeniedException</span></span>](https://msdn.microsoft.com/library/system.servicemodel.security.securityaccessdeniedexception.aspx)  
  
- [<span data-ttu-id="8b968-117">MessageSecurityException</span><span class="sxs-lookup"><span data-stu-id="8b968-117">MessageSecurityException</span></span>](https://msdn.microsoft.com/library/system.servicemodel.security.messagesecurityexception.aspx)  
  
- [<span data-ttu-id="8b968-118">SecurityNegotiationException</span><span class="sxs-lookup"><span data-stu-id="8b968-118">SecurityNegotiationException</span></span>](https://msdn.microsoft.com/library/system.servicemodel.security.securitynegotiationexception.aspx)  
  
  <span data-ttu-id="8b968-119">When connecting to [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps, a `SecurityAccessDeniedException` exception can be thrown if you use a valid [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] and your account is not associated with any [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] appsorganization.</span><span class="sxs-lookup"><span data-stu-id="8b968-119">When connecting to [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps, a `SecurityAccessDeniedException` exception can be thrown if you use a valid [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] and your account is not associated with any [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] appsorganization.</span></span> <span data-ttu-id="8b968-120">A `MessageSecurityException` can be thrown if your [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] isn’t valid or there was an authentication failure.</span><span class="sxs-lookup"><span data-stu-id="8b968-120">A `MessageSecurityException` can be thrown if your [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] isn’t valid or there was an authentication failure.</span></span>  
  
<a name="BKMK_BusinessRuleErrors"></a>

## <a name="custom-errors-from-business-rules"></a><span data-ttu-id="8b968-121">Custom errors from business rules</span><span class="sxs-lookup"><span data-stu-id="8b968-121">Custom errors from business rules</span></span>
 
 <span data-ttu-id="8b968-122">With [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] and [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)], customizers can create business rules that are evaluated on the server.</span><span class="sxs-lookup"><span data-stu-id="8b968-122">With [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] and [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)], customizers can create business rules that are evaluated on the server.</span></span> <span data-ttu-id="8b968-123">Customizers can throw error messages based on conditions set in the business rule.</span><span class="sxs-lookup"><span data-stu-id="8b968-123">Customizers can throw error messages based on conditions set in the business rule.</span></span> <span data-ttu-id="8b968-124">Developers should be sure to include robust error handling in their code to catch and handle these exceptions.</span><span class="sxs-lookup"><span data-stu-id="8b968-124">Developers should be sure to include robust error handling in their code to catch and handle these exceptions.</span></span>  
  
 <span data-ttu-id="8b968-125">The following is an example of the trace log produced when one of these errors is returned from a business rule named **Name of Entity Scope Business Rule returning Error** and the error message is **custom error message**.</span><span class="sxs-lookup"><span data-stu-id="8b968-125">The following is an example of the trace log produced when one of these errors is returned from a business rule named **Name of Entity Scope Business Rule returning Error** and the error message is **custom error message**.</span></span>  
  
```csharp
Unhandled Exception: System.ServiceModel.FaultException`1[[Microsoft.Xrm.Sdk.OrganizationServiceFault, Microsoft.Xrm.Sdk, Version=7.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]: custom error messageDetail:   
<OrganizationServiceFault xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://schemas.microsoft.com/xrm/2011/Contracts">  
  <ErrorCode>-2147220891</ErrorCode>  
  <ErrorDetails xmlns:d2p1="http://schemas.datacontract.org/2004/07/System.Collections.Generic">  
    <KeyValuePairOfstringanyType>  
      <d2p1:key>OperationStatus</d2p1:key>  
      <d2p1:value xmlns:d4p1="http://www.w3.org/2001/XMLSchema" i:type="d4p1:string">0</d2p1:value>  
    </KeyValuePairOfstringanyType>  
    <KeyValuePairOfstringanyType>  
      <d2p1:key>SubErrorCode</d2p1:key>  
      <d2p1:value xmlns:d4p1="http://www.w3.org/2001/XMLSchema" i:type="d4p1:string">-2146233088</d2p1:value>  
    </KeyValuePairOfstringanyType>  
  </ErrorDetails>  
  <Message>custom error message</Message>  
  <Timestamp>2014-09-04T17:43:16.8197965Z</Timestamp>  
  <InnerFault i:nil="true" />  
  <TraceText>  
  
[Microsoft.Crm.ObjectModel: Microsoft.Crm.ObjectModel.SyncWorkflowExecutionPlugin]  
[cf6a25a9-5a34-e411-80b9-00155dd8c20f: ]  
Starting sync workflow 'Name of Entity Scope Business Rule returning Error', Id: c76a25a9-5a34-e411-80b9-00155dd8c20f  
Entering ConditionStep1_step:   
Entering SetMessage_step:   
Sync workflow 'Name of Entity Scope Business Rule returning Error' terminated with error 'custom error message'  
  
</TraceText>  
</OrganizationServiceFault>  
```  
  
 [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="8b968-126">[Create and edit Business Rules](https://technet.microsoft.com/library/dn531086.aspx).</span><span class="sxs-lookup"><span data-stu-id="8b968-126">[Create and edit Business Rules](https://technet.microsoft.com/library/dn531086.aspx).</span></span>  
  
<a name="BKMK_AdditionalInfo"></a>   
## <a name="additional-information-about-exceptions"></a><span data-ttu-id="8b968-127">Additional information about exceptions</span><span class="sxs-lookup"><span data-stu-id="8b968-127">Additional information about exceptions</span></span>  
 <span data-ttu-id="8b968-128">When an uncaught exception is thrown that contains sensitive information that the user doesn’t have permission to see, the sensitive information in the exception is hidden from the user and a reference number is provided.</span><span class="sxs-lookup"><span data-stu-id="8b968-128">When an uncaught exception is thrown that contains sensitive information that the user doesn’t have permission to see, the sensitive information in the exception is hidden from the user and a reference number is provided.</span></span> <span data-ttu-id="8b968-129">This reference number refers to the related server event log entry and server trace entry.</span><span class="sxs-lookup"><span data-stu-id="8b968-129">This reference number refers to the related server event log entry and server trace entry.</span></span> <span data-ttu-id="8b968-130">A system administrator can look up those entries and find more information about the exception.</span><span class="sxs-lookup"><span data-stu-id="8b968-130">A system administrator can look up those entries and find more information about the exception.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="8b968-131">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8b968-131">See also</span></span>  
 <span data-ttu-id="8b968-132">[Troubleshooting and error handling](troubleshooting-error-handling.md) </span><span class="sxs-lookup"><span data-stu-id="8b968-132">[Troubleshooting and error handling](troubleshooting-error-handling.md) </span></span>  
 <span data-ttu-id="8b968-133">[Troubleshooting tips](troubleshooting-tips.md) </span><span class="sxs-lookup"><span data-stu-id="8b968-133">[Troubleshooting tips](troubleshooting-tips.md) </span></span>  
 <span data-ttu-id="8b968-134">[Web service error codes](web-service-error-codes.md) </span><span class="sxs-lookup"><span data-stu-id="8b968-134">[Web service error codes](web-service-error-codes.md) </span></span>  
 <span data-ttu-id="8b968-135">[Handle exceptions in plug-ins](../handle-exceptions-plugins.md) </span><span class="sxs-lookup"><span data-stu-id="8b968-135">[Handle exceptions in plug-ins](../handle-exceptions-plugins.md) </span></span>  
 [<span data-ttu-id="8b968-136">.NET Framework Developer Center</span><span class="sxs-lookup"><span data-stu-id="8b968-136">.NET Framework Developer Center</span></span>](https://msdn.microsoft.com/netframework/aa663324.aspx)
