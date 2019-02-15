---
title: Asynchronous operation states (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the asynchronous operation states, which can be waiting to run, it can be running, or it can be completed.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 78340765-afb7-47eb-a024-6c2dfd41cd6f
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 081261d30ec6f1395474fafd3603889ae429748d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387949"
---
# <a name="asynchronous-operation-states"></a>Asynchronous operation states

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

After asynchronous operations are added to the asynchronous queue, they exist in a well-defined state. An asynchronous operation can be waiting to run, it can be running, or it can be completed. There are also other possible states before the operation is eventually deleted from the queue. The states define the life cycle of the asynchronous operation.  
  
<a name="bkmk_states"></a>   
## <a name="states-for-asynchronous-operations"></a>States for asynchronous operations  
 The state of the asynchronous operation can be altered through three means: by the platform as part of regular queue processing, by the user interacting with the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps web application, or by a web service call that alters the asynchronous operation. As a developer you can retrieve the current state of any asynchronous operation that you have access to and also change the state.  
  
 The following table lists the states, and the statuses for each state, of an `AsyncOperation`.  
  
|Tiểu bang|Trạng thái|Numeric status value|  
|-----------|------------|--------------------------|  
|Sẵn sàng|WaitingForResources|0|  
|Đã treo|Đang chờ|10|  
|Đã khóa|InProgress|20|  
|Đã khóa|Đang tạm dừng|21|  
|Đã khóa|Đang hủy|22|  
|Đã hoàn thành|Đã thành công|30|  
|Đã hoàn thành|Không thành công|31|  
|Đã hoàn thành|Đã hủy|32|  
  
 The supported states are defined in the `AsyncOperationState` enumeration. In the early bound `AsyncOperation` class, the state is available in the `AsyncOperation.StateCode` attribute while the status is available in the `AsyncOperation.StatusCode` attribute. For more information, see the AsyncOperation entity metadata. [!INCLUDE[metadata_browser](../includes/metadata-browser.md)]. The statuses are shown in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Web application in the **Status Reason** field in **System Jobs** grid. By selecting any of the menu items in the **More Actions** menu in **System Jobs**, you can interactively alter the state of an asynchronous operation. Allowed actions include the following: Cancel, Resume, Postpone, and Pause.  
  
 The following diagram shows the asynchronous operation state transitions that are supported.  
  
 ![AsyncOperation state diagram](media/crm-v5s-as-statediagram.png "AsyncOperation state diagram")  
  
 Notice that an asynchronous operation can only transition from one state to another along specific paths as shown in the diagram. Some paths are initiated by the user interacting with the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application while other paths are initiated by the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps platform as part of regular asynchronous queue processing or because of a Web service call. For example, an asynchronous operation cannot transition directly from a Suspended state to a Locked state.  
  
 A locked state indicates that the `AsyncOperation` instance is being used by the asynchronous service. While it is locked it cannot be used by another instance of the service. This ensures that the instance is not executed more than once, for example by two different asynchronous services.  
  
<a name="bkmk_retrieve"></a>   
## <a name="retrieve-and-update-asyncoperation-states"></a>Retrieve and update AsyncOperation states  
 Monitoring and updating the state of an asynchronous operation is typically done interactively through the **System Jobs** grid in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Web application. However, you can also use the SDK to write code that performs those same tasks.  
  
#### <a name="read-the-state-of-an-asynchronous-operation"></a>Read the state of an asynchronous operation  
  
1.  Retrieve an `AsyncOperation` by name using the <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method or by ID using the <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*> method.  
  
2.  Read the `AsyncOperation.StateCode` attribute.  
  
#### <a name="change-the-state-code"></a>Change the state code  
  
1. Modify the retrieved state code attribute to a new value according to the allowed operation states. You could also change the `AsyncOperation.PostponeUntil` attribute.  
  
2. Call <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*> to change the value of those attributes in the database.  
  
   The previous operations can also be performed by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*> method with the appropriate request messages. Attributes of `AsyncOperation` other than `AsyncOperation.StateCode` and `AsyncOperation.PostponeUntil` should be considered read-only.  
  
## <a name="recurring-system-jobs"></a>Recurring system jobs  
 You cannot cancel, pause, or resume most system jobs. Refer to the following list that identifies some of these restricted system jobs. The value in the first column is the value of the `OperationType` attribute of the `AsyncOperation` entity.  
  
|Async Operation Type (Option Value)|Operation Description|  
|-------------------------------------------|---------------------------|  
|22|Calculate Organization Maximum Storage Size|  
|18|Calculate Organization Storage Size|  
|19|Collect Organization Database Statistics|  
|20|Collection Organization Size Statistics|  
|16|Collect Organization Statistics|  
|9|SQM Data Collection|  
|25|Organization Full Text Catalog Index|  
|31|Storage Limit Notification|  
|24|Update Statistic Intervals|  
|27|Update Contract States|  
  
 For the complete list of supported asynchronous operation types, see the `AsyncOperation` entity metadata. [!INCLUDE[metadata_browser](../includes/metadata-browser.md)]  
  
### <a name="see-also"></a>Xem thêm  
 [Dịch vụ Không đồng thời](asynchronous-service.md)   
 [Asynchronous Operation (system job) Entity](asyncoperation-system-job-entity.md)   
 [Dependency and execution order in asynchronous operations](dependency-execution-order-asynchronous-operations.md)
