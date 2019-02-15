---
title: 'Helper code: SystemUserProvider class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: The SystemUserProvider class demonstrates how to programmatically create additional users in Active Directory andDynamics 365 for Customer Engagement (online) Customer Engagement
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- creating additional users by using Active Directory in CRM
- SystemUserProvider class, helper code samples
- sample for creating additional users by using Active Directory in CRM, SystemUserProvider class
- adding more users by using Active Directory in CRM sample, SystemUserProvider class
- SystemUserProvider class, creating additional users by using Active Directory in CRM
- helper code samples, SystemUserProvider class
ms.assetid: 4a4da7b8-ca42-4f03-9a27-83d487d38ace
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8bc2aa7b3e2cf2955bddfe392c8fc6766f152b15
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386713"
---
# <a name="helper-code-systemuserprovider-class"></a><span data-ttu-id="5ed8c-103">Helper code: SystemUserProvider class</span><span class="sxs-lookup"><span data-stu-id="5ed8c-103">Helper code: SystemUserProvider class</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5ed8c-104">The file is present in code samples' folder that you download.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-104">The file is present in code samples' folder that you download.</span></span>
 
 <span data-ttu-id="5ed8c-105">Path: `download-directory>\<sample name>\C#\SystemUserProvider.cs`.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-105">Path: `download-directory>\<sample name>\C#\SystemUserProvider.cs`.</span></span>
 
 <span data-ttu-id="5ed8c-106">For example, if you download the **Work with visualizations and dashboards** sample to D drive, you can find the sample in the following folder path.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-106">For example, if you download the **Work with visualizations and dashboards** sample to D drive, you can find the sample in the following folder path.</span></span>

 <span data-ttu-id="5ed8c-107">Path: `D:\Work with visualizations and dashboards\SystemUserProvider.cs`</span><span class="sxs-lookup"><span data-stu-id="5ed8c-107">Path: `D:\Work with visualizations and dashboards\SystemUserProvider.cs`</span></span>
  
## <a name="requirements"></a><span data-ttu-id="5ed8c-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="5ed8c-108">Requirements</span></span>  
 <span data-ttu-id="5ed8c-109">The logged on system user must have system administration privileges for this sample code to create the new user accounts.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-109">The logged on system user must have system administration privileges for this sample code to create the new user accounts.</span></span> [!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]  
  
## <a name="demonstrates"></a><span data-ttu-id="5ed8c-110">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="5ed8c-110">Demonstrates</span></span>  
 <span data-ttu-id="5ed8c-111">The **SystemUserProvider** class demonstrates how to programmatically create additional users in [!INCLUDE[pn_Active_Directory](../../includes/pn-active-directory.md)] and[!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-111">The **SystemUserProvider** class demonstrates how to programmatically create additional users in [!INCLUDE[pn_Active_Directory](../../includes/pn-active-directory.md)] and[!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span>  
  
 <span data-ttu-id="5ed8c-112">Several SDK samples require additional (fictitious) system users to exist in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)], other than the logged on user, for the sample to perform its intended task.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-112">Several SDK samples require additional (fictitious) system users to exist in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)], other than the logged on user, for the sample to perform its intended task.</span></span> <span data-ttu-id="5ed8c-113">These samples use the **SystemUserProvider** class methods to create these additional required users.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-113">These samples use the **SystemUserProvider** class methods to create these additional required users.</span></span> <span data-ttu-id="5ed8c-114">Since it currently is not possible to programmatically create a new [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] user, when running against a [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] server, the code just prints the required user information to the console.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-114">Since it currently is not possible to programmatically create a new [!INCLUDE[pn_Windows_Live_ID](../../includes/pn-windows-live-id.md)] user, when running against a [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] server, the code just prints the required user information to the console.</span></span> <span data-ttu-id="5ed8c-115">You can then manually add and invite those users if desired.</span><span class="sxs-lookup"><span data-stu-id="5ed8c-115">You can then manually add and invite those users if desired.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5ed8c-116">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="5ed8c-116">Example</span></span>  
 [!code-csharp[HelperCode#SystemUserProvider](../../snippets/csharp/CRMV8/helpercode/cs/systemuserprovider.cs#systemuserprovider)]
  
### <a name="see-also"></a><span data-ttu-id="5ed8c-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5ed8c-117">See also</span></span>  
 <span data-ttu-id="5ed8c-118">[Use the Sample and Helper Code](use-sample-helper-code.md) </span><span class="sxs-lookup"><span data-stu-id="5ed8c-118">[Use the Sample and Helper Code](use-sample-helper-code.md) </span></span>  
 <span data-ttu-id="5ed8c-119">[Helper Code: Enumerations for Option Sets](helper-code-enumerations-option-sets.md) </span><span class="sxs-lookup"><span data-stu-id="5ed8c-119">[Helper Code: Enumerations for Option Sets](helper-code-enumerations-option-sets.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.AssociateEntitiesRequest>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest>
