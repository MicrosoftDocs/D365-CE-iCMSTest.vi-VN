---
title: Actions on dashboards (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'Learn about performing actions such as create, retrieve, update, or delete, on organization-owned and user-owned dashboards. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 586a10d6-4448-474e-9428-d13520f52213
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ef66579380d6232e922efa31d0aa8245cec4f6e5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388256"
---
# <a name="actions-on-dashboards"></a><span data-ttu-id="e50aa-103">Actions on dashboards</span><span class="sxs-lookup"><span data-stu-id="e50aa-103">Actions on dashboards</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e50aa-104">You can perform actions such as create, retrieve, update, or delete, on organization-owned and user-owned dashboards.</span><span class="sxs-lookup"><span data-stu-id="e50aa-104">You can perform actions such as create, retrieve, update, or delete, on organization-owned and user-owned dashboards.</span></span>  
  
## <a name="actions-on-an-organization-owned-dashboard"></a><span data-ttu-id="e50aa-105">Actions on an Organization-Owned Dashboard</span><span class="sxs-lookup"><span data-stu-id="e50aa-105">Actions on an Organization-Owned Dashboard</span></span>  
 <span data-ttu-id="e50aa-106">To perform the following actions on an organization-owned dashboard (`SystemForm`), you must have the System Administrator or the System Customizer role assigned to your account in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement:</span><span class="sxs-lookup"><span data-stu-id="e50aa-106">To perform the following actions on an organization-owned dashboard (`SystemForm`), you must have the System Administrator or the System Customizer role assigned to your account in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement:</span></span>  
  
- <span data-ttu-id="e50aa-107">Create, retrieve, update, and delete.</span><span class="sxs-lookup"><span data-stu-id="e50aa-107">Create, retrieve, update, and delete.</span></span> <span data-ttu-id="e50aa-108">You can create or update an organization-owned dashboard by using the [!INCLUDE[cc-dyn365-ce-web-services](../../includes/cc-dyn365-ce-web-services.md)] or by customizing the entity form.</span><span class="sxs-lookup"><span data-stu-id="e50aa-108">You can create or update an organization-owned dashboard by using the [!INCLUDE[cc-dyn365-ce-web-services](../../includes/cc-dyn365-ce-web-services.md)] or by customizing the entity form.</span></span> <span data-ttu-id="e50aa-109">For detailed information about creating a dashboard, see [Create a Dashboard](create-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="e50aa-109">For detailed information about creating a dashboard, see [Create a Dashboard](create-dashboard.md).</span></span>  
  
- <span data-ttu-id="e50aa-110">Set an organization-owned dashboard as the default dashboard for an organization by setting the `SystemForm.IsDefault` attribute value to `true` while creating or updating the dashboard.</span><span class="sxs-lookup"><span data-stu-id="e50aa-110">Set an organization-owned dashboard as the default dashboard for an organization by setting the `SystemForm.IsDefault` attribute value to `true` while creating or updating the dashboard.</span></span>  
  
  > [!IMPORTANT]
  >  <span data-ttu-id="e50aa-111">Using the methods available in the [!INCLUDE[cc-dyn365-ce-web-services](../../includes/cc-dyn365-ce-web-services.md)], it is possible to set two dashboards as the default.</span><span class="sxs-lookup"><span data-stu-id="e50aa-111">Using the methods available in the [!INCLUDE[cc-dyn365-ce-web-services](../../includes/cc-dyn365-ce-web-services.md)], it is possible to set two dashboards as the default.</span></span> <span data-ttu-id="e50aa-112">Make sure that no other dashboard is the default dashboard for the organization before updating this setting programmatically.</span><span class="sxs-lookup"><span data-stu-id="e50aa-112">Make sure that no other dashboard is the default dashboard for the organization before updating this setting programmatically.</span></span>  
  
  <span data-ttu-id="e50aa-113">After you update an organization-owned dashboard, you must publish the metadata changes to make it visible across the organization.</span><span class="sxs-lookup"><span data-stu-id="e50aa-113">After you update an organization-owned dashboard, you must publish the metadata changes to make it visible across the organization.</span></span> <span data-ttu-id="e50aa-114">You can use the <xref:Microsoft.Crm.Sdk.Messages.PublishAllXmlRequest> message or <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest> message to publish the changes made for an organization-owned dashboard.</span><span class="sxs-lookup"><span data-stu-id="e50aa-114">You can use the <xref:Microsoft.Crm.Sdk.Messages.PublishAllXmlRequest> message or <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest> message to publish the changes made for an organization-owned dashboard.</span></span> <span data-ttu-id="e50aa-115">For a sample code that demonstrates this, see [Sample: Create, Retrieve, Update and Delete (CRUD) a Dashboard](sample-create-retrieve-update-delete-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="e50aa-115">For a sample code that demonstrates this, see [Sample: Create, Retrieve, Update and Delete (CRUD) a Dashboard](sample-create-retrieve-update-delete-dashboard.md).</span></span>  
  
  <span data-ttu-id="e50aa-116">For a list of supported messages on the organization-owned dashboard entity, see [SystemForm Entity](../entities/systemform.md).</span><span class="sxs-lookup"><span data-stu-id="e50aa-116">For a list of supported messages on the organization-owned dashboard entity, see [SystemForm Entity](../entities/systemform.md).</span></span>  
  
## <a name="actions-on-a-user-owned-dashboard"></a><span data-ttu-id="e50aa-117">Actions on a User-Owned Dashboard</span><span class="sxs-lookup"><span data-stu-id="e50aa-117">Actions on a User-Owned Dashboard</span></span>  
 <span data-ttu-id="e50aa-118">You can perform the following actions on a user-owned dashboard (`UserForm`):</span><span class="sxs-lookup"><span data-stu-id="e50aa-118">You can perform the following actions on a user-owned dashboard (`UserForm`):</span></span>  
  
- <span data-ttu-id="e50aa-119">Create, retrieve, update, and delete.</span><span class="sxs-lookup"><span data-stu-id="e50aa-119">Create, retrieve, update, and delete.</span></span> <span data-ttu-id="e50aa-120">For detailed information about creating a user-owned dashboard, see [Create a Dashboard](create-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="e50aa-120">For detailed information about creating a user-owned dashboard, see [Create a Dashboard](create-dashboard.md).</span></span>  
  
- <span data-ttu-id="e50aa-121">Change the ownership of a user-owned dashboard by assigning it to another user or team using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message.</span><span class="sxs-lookup"><span data-stu-id="e50aa-121">Change the ownership of a user-owned dashboard by assigning it to another user or team using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message.</span></span>  
  
- <span data-ttu-id="e50aa-122">Retrieve the access that the specified security principal (user or team) has to a user-owned dashboard using the <xref:Microsoft.Crm.Sdk.Messages.RetrievePrincipalAccessRequest> message.</span><span class="sxs-lookup"><span data-stu-id="e50aa-122">Retrieve the access that the specified security principal (user or team) has to a user-owned dashboard using the <xref:Microsoft.Crm.Sdk.Messages.RetrievePrincipalAccessRequest> message.</span></span> <span data-ttu-id="e50aa-123">You can also retrieve all the security principals (users or teams) that have access to a user-owned dashboard, along with their access rights to the user dashboard using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveSharedPrincipalsAndAccessRequest> message.</span><span class="sxs-lookup"><span data-stu-id="e50aa-123">You can also retrieve all the security principals (users or teams) that have access to a user-owned dashboard, along with their access rights to the user dashboard using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveSharedPrincipalsAndAccessRequest> message.</span></span>  
  
- <span data-ttu-id="e50aa-124">Collaborate with other users and teams on specific areas by sharing a user-owned dashboard with them using the <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>, <xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>, and <xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest> messages.</span><span class="sxs-lookup"><span data-stu-id="e50aa-124">Collaborate with other users and teams on specific areas by sharing a user-owned dashboard with them using the <xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>, <xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>, and <xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest> messages.</span></span>  
  
  <span data-ttu-id="e50aa-125">For a list of supported messages on the user-owned dashboard entity, see [UserForm Entity](../entities/userform.md).</span><span class="sxs-lookup"><span data-stu-id="e50aa-125">For a list of supported messages on the user-owned dashboard entity, see [UserForm Entity](../entities/userform.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e50aa-126">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e50aa-126">See also</span></span>  
 <span data-ttu-id="e50aa-127">[Dashboards for Microsoft Dynamics 365 for Customer Engagement](analyze-data-with-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="e50aa-127">[Dashboards for Microsoft Dynamics 365 for Customer Engagement](analyze-data-with-dashboards.md) </span></span>  
 <span data-ttu-id="e50aa-128">[Using FormXML for Dashboards](understand-dashboards-dashboard-components-formxml.md) </span><span class="sxs-lookup"><span data-stu-id="e50aa-128">[Using FormXML for Dashboards](understand-dashboards-dashboard-components-formxml.md) </span></span>  
 <span data-ttu-id="e50aa-129">[Create a Dashboard](create-dashboard.md) </span><span class="sxs-lookup"><span data-stu-id="e50aa-129">[Create a Dashboard](create-dashboard.md) </span></span>  
 <span data-ttu-id="e50aa-130">[Sample Dashboards](sample-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="e50aa-130">[Sample Dashboards](sample-dashboards.md) </span></span>  
 <span data-ttu-id="e50aa-131">[Dashboard Entities](dashboard-entities.md) </span><span class="sxs-lookup"><span data-stu-id="e50aa-131">[Dashboard Entities](dashboard-entities.md) </span></span>  
 <span data-ttu-id="e50aa-132">[Sample: Create, Retrieve, Update and Delete (CRUD) a Dashboard](sample-create-retrieve-update-delete-dashboard.md) </span><span class="sxs-lookup"><span data-stu-id="e50aa-132">[Sample: Create, Retrieve, Update and Delete (CRUD) a Dashboard](sample-create-retrieve-update-delete-dashboard.md) </span></span>  
 [<span data-ttu-id="e50aa-133">Sample: Assign a User-Owned Dashboard to Another User</span><span class="sxs-lookup"><span data-stu-id="e50aa-133">Sample: Assign a User-Owned Dashboard to Another User</span></span>](sample-assign-user-owned-dashboard-another-user.md)
