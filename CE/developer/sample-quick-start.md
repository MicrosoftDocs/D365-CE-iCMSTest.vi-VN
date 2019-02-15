---
title: 'Sample: Quick start for Dynamics 365 for Customer Engagement apps(Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs'
description: 'Dynamics 365 for Customer Engagement Custommer Engagement web services by using the ServerConnection helper class and perform basic create, update, retrieve, and delete operations on an entity. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0f1b28e3-0db0-4150-9c3b-d65daf0fabc5
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fe0a67a35d8b08b38039efb5925e9ca1de810ec5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386889"
---
# <a name="sample-quick-start-for-dynamics-365-for-customer-engagement"></a><span data-ttu-id="0caf7-103">Sample: Quick start for Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="0caf7-103">Sample: Quick start for Dynamics 365 for Customer Engagement</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0caf7-104">The QuickStart sample is a [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] managed code sample that shows how to connect to the Dynamics 365 for Customer Engagement web services by using the `ServerConnection` helper class and perform basic create, update, retrieve, and delete operations on an entity.</span><span class="sxs-lookup"><span data-stu-id="0caf7-104">The QuickStart sample is a [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] managed code sample that shows how to connect to the Dynamics 365 for Customer Engagement web services by using the `ServerConnection` helper class and perform basic create, update, retrieve, and delete operations on an entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0caf7-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="0caf7-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]

## <a name="requirements"></a><span data-ttu-id="0caf7-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="0caf7-106">Requirements</span></span>

<span data-ttu-id="0caf7-107">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="0caf7-107">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="0caf7-108">Download the complete sample from [Sample: Quick start for Microsoft Dynamics 365 for Customer Engagement](https://code.msdn.microsoft.com/Sample-Quick-start-for-650dbcaa).</span><span class="sxs-lookup"><span data-stu-id="0caf7-108">Download the complete sample from [Sample: Quick start for Microsoft Dynamics 365 for Customer Engagement](https://code.msdn.microsoft.com/Sample-Quick-start-for-650dbcaa).</span></span>

## <a name="demonstrates"></a><span data-ttu-id="0caf7-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="0caf7-109">Demonstrates</span></span>

<span data-ttu-id="0caf7-110">This sample authenticates the user with the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web services by using the `ServerConnection` helper class and methods.</span><span class="sxs-lookup"><span data-stu-id="0caf7-110">This sample authenticates the user with the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web services by using the `ServerConnection` helper class and methods.</span></span> <span data-ttu-id="0caf7-111">After obtaining a reference to the Organization web service, the sample performs basic create, update, retrieve, and delete operations on an account entity.</span><span class="sxs-lookup"><span data-stu-id="0caf7-111">After obtaining a reference to the Organization web service, the sample performs basic create, update, retrieve, and delete operations on an account entity.</span></span> <span data-ttu-id="0caf7-112">The sample also handles common exceptions that can be thrown.</span><span class="sxs-lookup"><span data-stu-id="0caf7-112">The sample also handles common exceptions that can be thrown.</span></span>

## <a name="example"></a><span data-ttu-id="0caf7-113">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="0caf7-113">Example</span></span>
[!code-csharp[QuickStartCS#CRUDOperations](../snippets/csharp/CRMV8/quickstartcs/cs/crudoperations.cs#crudoperations)]

### <a name="see-also"></a><span data-ttu-id="0caf7-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0caf7-114">See also</span></span>

[<span data-ttu-id="0caf7-115">Tutorials for Learning About Dynamics 365 for Customer Engagement Development apps</span><span class="sxs-lookup"><span data-stu-id="0caf7-115">Tutorials for Learning About Dynamics 365 for Customer Engagement Development apps</span></span>](tutorials-resources-sdk.md)<br />
[<span data-ttu-id="0caf7-116">Sample: Simplified Connection Quick Start using Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="0caf7-116">Sample: Simplified Connection Quick Start using Dynamics 365 for Customer Engagement apps</span></span>](xrm-tooling/sample-simplified-connection-quick-start.md)<br />
[<span data-ttu-id="0caf7-117">Helper Code: ServerConnection Class</span><span class="sxs-lookup"><span data-stu-id="0caf7-117">Helper Code: ServerConnection Class</span></span>](org-service/helper-code-serverconnection-class.md)<br />
