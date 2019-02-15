---
title: Actions on dialogs (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'This topic describes the actions you can perform on dialogs using the Dynamics 365 for Customer Engagement web services (SDK). '
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
- dialogs, dialogs, actions
ms.assetid: dec79d11-75fc-4a1c-ae50-3b5d3d237fd7
caps.latest.revision: 29
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ab3b389c51a6361d3ff8dce8baeec2a99e521a7c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387977"
---
# <a name="actions-on-dialogs"></a><span data-ttu-id="df996-103">Actions on dialogs</span><span class="sxs-lookup"><span data-stu-id="df996-103">Actions on dialogs</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="df996-104">This topic describes the actions you can perform on dialogs.</span><span class="sxs-lookup"><span data-stu-id="df996-104">This topic describes the actions you can perform on dialogs.</span></span>  

<a name="DialogRelated"></a>   

## <a name="dialog-related-activities"></a><span data-ttu-id="df996-105">Dialog-related activities</span><span class="sxs-lookup"><span data-stu-id="df996-105">Dialog-related activities</span></span>

 <span data-ttu-id="df996-106">These activities are available as steps in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Process Designer.</span><span class="sxs-lookup"><span data-stu-id="df996-106">These activities are available as steps in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Process Designer.</span></span>  

### <a name="query-includepndynamicscrmincludespn-dynamics-crmmd-apps-data"></a><span data-ttu-id="df996-107">Query [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Data</span><span class="sxs-lookup"><span data-stu-id="df996-107">Query [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Data</span></span>

 <span data-ttu-id="df996-108">Enables you to define query variables that can be used to query [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data.</span><span class="sxs-lookup"><span data-stu-id="df996-108">Enables you to define query variables that can be used to query [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps data.</span></span> <span data-ttu-id="df996-109">These query variables can either have pre-defined values or can be parameterized so that they accept values at the runtime, and fetch records accordingly.</span><span class="sxs-lookup"><span data-stu-id="df996-109">These query variables can either have pre-defined values or can be parameterized so that they accept values at the runtime, and fetch records accordingly.</span></span>  

 <span data-ttu-id="df996-110">You can parameterize a query variable by using the **Modify Query Variables** tab on the **Define Query** page, and then use the dynamic values section on the query form to associate the prompt and response variables with the query variables.</span><span class="sxs-lookup"><span data-stu-id="df996-110">You can parameterize a query variable by using the **Modify Query Variables** tab on the **Define Query** page, and then use the dynamic values section on the query form to associate the prompt and response variables with the query variables.</span></span>  

 <span data-ttu-id="df996-111">The query variable defined using the **Query Dynamics 365 for Customer Engagement apps Data** step is available for all the prompts and responses from the point where they have been defined in the dialog definition.</span><span class="sxs-lookup"><span data-stu-id="df996-111">The query variable defined using the **Query Dynamics 365 for Customer Engagement apps Data** step is available for all the prompts and responses from the point where they have been defined in the dialog definition.</span></span>  

### <a name="assign-value"></a><span data-ttu-id="df996-112">Gán giá trị</span><span class="sxs-lookup"><span data-stu-id="df996-112">Assign Value</span></span>

 <span data-ttu-id="df996-113">Enables you to perform simple arithmetic (increment, decrement, and multiply) and string (append) operations on the variables and input arguments in dialogs.</span><span class="sxs-lookup"><span data-stu-id="df996-113">Enables you to perform simple arithmetic (increment, decrement, and multiply) and string (append) operations on the variables and input arguments in dialogs.</span></span> <span data-ttu-id="df996-114">You can also use the **Assign Value** step to clear any value that is stored in the variables or input parameters.</span><span class="sxs-lookup"><span data-stu-id="df996-114">You can also use the **Assign Value** step to clear any value that is stored in the variables or input parameters.</span></span>  

### <a name="link-child-dialog"></a><span data-ttu-id="df996-115">Liên kết hộp thoại con</span><span class="sxs-lookup"><span data-stu-id="df996-115">Link Child Dialog</span></span>

 <span data-ttu-id="df996-116">You can specify a dialog as a child dialog, and invoke it from within another dialog (parent) by using the **Link Child Dialog** step in the parent dialog.</span><span class="sxs-lookup"><span data-stu-id="df996-116">You can specify a dialog as a child dialog, and invoke it from within another dialog (parent) by using the **Link Child Dialog** step in the parent dialog.</span></span>  

### <a name="stop-dialog"></a><span data-ttu-id="df996-117">Stop Dialog</span><span class="sxs-lookup"><span data-stu-id="df996-117">Stop Dialog</span></span>

 <span data-ttu-id="df996-118">Enables you to end a dialog at a particular stage in the dialog flow.</span><span class="sxs-lookup"><span data-stu-id="df996-118">Enables you to end a dialog at a particular stage in the dialog flow.</span></span> <span data-ttu-id="df996-119">This step can be used in any conditional statement where you want a dialog to end at that point based on the response from the user.</span><span class="sxs-lookup"><span data-stu-id="df996-119">This step can be used in any conditional statement where you want a dialog to end at that point based on the response from the user.</span></span>  

<a name="WorkflowRelated"></a>   

## <a name="workflow-related-activities"></a><span data-ttu-id="df996-120">Workflow-related activities</span><span class="sxs-lookup"><span data-stu-id="df996-120">Workflow-related activities</span></span>

 <span data-ttu-id="df996-121">The following workflow-related activities can be used for dialogs: **Create Record**, **Update Record**, **Assign Record**, **Update Record**, **Send E-mail**, **Start Child Workflow**, and **Change Status**.</span><span class="sxs-lookup"><span data-stu-id="df996-121">The following workflow-related activities can be used for dialogs: **Create Record**, **Update Record**, **Assign Record**, **Update Record**, **Send E-mail**, **Start Child Workflow**, and **Change Status**.</span></span>  

<a name="CustomActivities"></a>   

## <a name="custom-workflow-activities"></a><span data-ttu-id="df996-122">Custom workflow activities</span><span class="sxs-lookup"><span data-stu-id="df996-122">Custom workflow activities</span></span>

 <span data-ttu-id="df996-123">You can create custom workflow activities to extend the dialogs in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="df996-123">You can create custom workflow activities to extend the dialogs in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="df996-124">For detailed information about custom workflow activities, see [Custom Workflow Activities](custom-workflow-activities-workflow-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="df996-124">For detailed information about custom workflow activities, see [Custom Workflow Activities](custom-workflow-activities-workflow-assemblies.md).</span></span>  

<a name="StartDialog"></a>   

## <a name="start-a-dialog-by-using-a-url"></a><span data-ttu-id="df996-125">Start a dialog by using a URL</span><span class="sxs-lookup"><span data-stu-id="df996-125">Start a dialog by using a URL</span></span>

 <span data-ttu-id="df996-126">You can start an activated dialog by specifying the URL of the dialog.</span><span class="sxs-lookup"><span data-stu-id="df996-126">You can start an activated dialog by specifying the URL of the dialog.</span></span> <span data-ttu-id="df996-127">To do so, you must specify the URL in the following format:</span><span class="sxs-lookup"><span data-stu-id="df996-127">To do so, you must specify the URL in the following format:</span></span>  

```
http://CRMServer_Name/Org_Name/cs/dialog/rundialog.aspx?DialogId=DialogID&EntityName=EntityLogicalName&ObjectId=EntityObjectId  
```

 <span data-ttu-id="df996-128">Where,</span><span class="sxs-lookup"><span data-stu-id="df996-128">Where,</span></span>  

- <span data-ttu-id="df996-129">*CRMServer_Name* is the name of your [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server.</span><span class="sxs-lookup"><span data-stu-id="df996-129">*CRMServer_Name* is the name of your [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server.</span></span>  

- <span data-ttu-id="df996-130">_Org_Name_ is the organization name.</span><span class="sxs-lookup"><span data-stu-id="df996-130">_Org_Name_ is the organization name.</span></span>  

- <span data-ttu-id="df996-131">_DialogID_ is GUID of the dialog that you want to run.</span><span class="sxs-lookup"><span data-stu-id="df996-131">_DialogID_ is GUID of the dialog that you want to run.</span></span>  

- <span data-ttu-id="df996-132">_EntityLogicalName_ is the entity logical name of the primary entity of the dialog that you want to run.</span><span class="sxs-lookup"><span data-stu-id="df996-132">_EntityLogicalName_ is the entity logical name of the primary entity of the dialog that you want to run.</span></span>  

- <span data-ttu-id="df996-133">_EntityObjectId_ is the GUID of the primary entity record.</span><span class="sxs-lookup"><span data-stu-id="df996-133">_EntityObjectId_ is the GUID of the primary entity record.</span></span>  
  <span data-ttu-id="df996-134">A sample URL to start a dialog:</span><span class="sxs-lookup"><span data-stu-id="df996-134">A sample URL to start a dialog:</span></span>  
  `http://crmserver/AdventureWorksCycle/cs/dialog/rundialog.aspx?DialogId=9F53D2D8-AC54-46A6-A190-F23DE6677C65&EntityName=contact&ObjectId=41D1884E-B4B6-DF11-BF5E-00155DB05986`  
     

### <a name="see-also"></a><span data-ttu-id="df996-135">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="df996-135">See also</span></span>

 [<span data-ttu-id="df996-136">Work with Dialogs</span><span class="sxs-lookup"><span data-stu-id="df996-136">Work with Dialogs</span></span>](use-dialogs-guided-processes.md)  
 [<span data-ttu-id="df996-137">Understanding Dialogs</span><span class="sxs-lookup"><span data-stu-id="df996-137">Understanding Dialogs</span></span>](understand-dialogs.md)  
 [<span data-ttu-id="df996-138">Sample: Create, Retrieve, Update, and Delete (CRUD) a Dialog</span><span class="sxs-lookup"><span data-stu-id="df996-138">Sample: Create, Retrieve, Update, and Delete (CRUD) a Dialog</span></span>](sample-create-retrieve-update-delete-dialog.md)
