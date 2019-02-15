---
title: 'Sample: Calculate a credit score with a custom workflow activity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates workflow activity calculates the credit score based on the Social Security Number (SSN) and name.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 9cb7eb41-1a73-44a8-ae58-14120e84243f
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1796df1cb7a8de5237db7bde6c967d42e4986cec
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387409"
---
# <a name="sample-calculate-a-credit-score-with-a-custom-workflow-activity"></a><span data-ttu-id="36a1a-103">Sample: Calculate a credit score with a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="36a1a-103">Sample: Calculate a credit score with a custom workflow activity</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="36a1a-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="36a1a-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="36a1a-105">Download the complete sample here [Custom workflow activities samples](https://code.msdn.microsoft.com/Custom-Workflow-Activities-eee57285).</span><span class="sxs-lookup"><span data-stu-id="36a1a-105">Download the complete sample here [Custom workflow activities samples](https://code.msdn.microsoft.com/Custom-Workflow-Activities-eee57285).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="36a1a-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="36a1a-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="36a1a-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="36a1a-107">Requirements</span></span>  
 <span data-ttu-id="36a1a-108">The following customizations must exist for this custom workflow activity to work:</span><span class="sxs-lookup"><span data-stu-id="36a1a-108">The following customizations must exist for this custom workflow activity to work:</span></span>  
  
- <span data-ttu-id="36a1a-109">Entity Schema Name: new_loanapplication</span><span class="sxs-lookup"><span data-stu-id="36a1a-109">Entity Schema Name: new_loanapplication</span></span>  
  
- <span data-ttu-id="36a1a-110">Attribute: new_loanapplicationid as the primary key</span><span class="sxs-lookup"><span data-stu-id="36a1a-110">Attribute: new_loanapplicationid as the primary key</span></span>  
  
- <span data-ttu-id="36a1a-111">Attribute: new_creditscore of type `int` with min of 0 and max of 1000 (if it is to be updated)</span><span class="sxs-lookup"><span data-stu-id="36a1a-111">Attribute: new_creditscore of type `int` with min of 0 and max of 1000 (if it is to be updated)</span></span>  
  
- <span data-ttu-id="36a1a-112">Attribute: new_loanamount of type money with default min/max</span><span class="sxs-lookup"><span data-stu-id="36a1a-112">Attribute: new_loanamount of type money with default min/max</span></span>  
  
- <span data-ttu-id="36a1a-113">Customize the form to include the attribute new_loanapplicantid</span><span class="sxs-lookup"><span data-stu-id="36a1a-113">Customize the form to include the attribute new_loanapplicantid</span></span>  
  
  <span data-ttu-id="36a1a-114">The contact entity must have the following customizations:</span><span class="sxs-lookup"><span data-stu-id="36a1a-114">The contact entity must have the following customizations:</span></span>  
  
- <span data-ttu-id="36a1a-115">Attribute: new_ssn as **Single Line of Text** with max length of 15</span><span class="sxs-lookup"><span data-stu-id="36a1a-115">Attribute: new_ssn as **Single Line of Text** with max length of 15</span></span>  
  
- <span data-ttu-id="36a1a-116">One-To-Many Relationship with these properties:</span><span class="sxs-lookup"><span data-stu-id="36a1a-116">One-To-Many Relationship with these properties:</span></span>  
  
  -   <span data-ttu-id="36a1a-117">Relationship Definition Schema Name: new_loanapplicant</span><span class="sxs-lookup"><span data-stu-id="36a1a-117">Relationship Definition Schema Name: new_loanapplicant</span></span>  
  
  -   <span data-ttu-id="36a1a-118">Relationship Definition Related Entity Display Name: Loan Application</span><span class="sxs-lookup"><span data-stu-id="36a1a-118">Relationship Definition Related Entity Display Name: Loan Application</span></span>  
  
  -   <span data-ttu-id="36a1a-119">Relationship Attribute Schema Name: new_loanapplicantid</span><span class="sxs-lookup"><span data-stu-id="36a1a-119">Relationship Attribute Schema Name: new_loanapplicantid</span></span>  
  
  -   <span data-ttu-id="36a1a-120">Relationship Behavior Type: Referential</span><span class="sxs-lookup"><span data-stu-id="36a1a-120">Relationship Behavior Type: Referential</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="36a1a-121">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="36a1a-121">Demonstrates</span></span>  
 <span data-ttu-id="36a1a-122">The following sample workflow activity calculates the credit score based on the Social Security Number (SSN) and name.</span><span class="sxs-lookup"><span data-stu-id="36a1a-122">The following sample workflow activity calculates the credit score based on the Social Security Number (SSN) and name.</span></span>  
  
## <a name="example"></a><span data-ttu-id="36a1a-123">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="36a1a-123">Example</span></span>  
 [!code-csharp[customworkflowactivities#ReleaseISVActivities4](../../snippets/csharp/CRMV8/customworkflowactivities/cs/releaseisvactivities4.cs#releaseisvactivities4)]  
  
### <a name="see-also"></a><span data-ttu-id="36a1a-124">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="36a1a-124">See also</span></span>  
 <span data-ttu-id="36a1a-125">[Custom Workflow Activities (Workflow Assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="36a1a-125">[Custom Workflow Activities (Workflow Assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span></span>  
 [<span data-ttu-id="36a1a-126">Add Metadata to a Custom Workflow Activity</span><span class="sxs-lookup"><span data-stu-id="36a1a-126">Add Metadata to a Custom Workflow Activity</span></span>](add-metadata-custom-workflow-activity.md)
