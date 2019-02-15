---
title: Publish customizations | MicrosoftDocs
description: Publishing customizations makes the Web application aware of changes to the data that affects the user interface.
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
- publish customizations
ms.assetid: 649ec32a-1ae1-4966-96fa-3543f4a05509
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fee26e9bf1ce8d5736ee4b7445173f95bcb782c6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388751"
---
# <a name="publish-customizations"></a><span data-ttu-id="b3d33-103">Đăng tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="b3d33-103">Publish customizations</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b3d33-104">Publishing customizations makes the Web application aware of changes to the data that affects the user interface.</span><span class="sxs-lookup"><span data-stu-id="b3d33-104">Publishing customizations makes the Web application aware of changes to the data that affects the user interface.</span></span>  
  
<a name="BKMK_WhenToPublishCustomizations"></a>   
## <a name="when-to-publish-customizations"></a><span data-ttu-id="b3d33-105">When to publish customizations</span><span class="sxs-lookup"><span data-stu-id="b3d33-105">When to publish customizations</span></span>  
 <span data-ttu-id="b3d33-106">Customizations are automatically published when new items are created or existing items are deleted.</span><span class="sxs-lookup"><span data-stu-id="b3d33-106">Customizations are automatically published when new items are created or existing items are deleted.</span></span>  
  
 <span data-ttu-id="b3d33-107">You must publish changes after updating schema metadata or entities that affect the user interface.</span><span class="sxs-lookup"><span data-stu-id="b3d33-107">You must publish changes after updating schema metadata or entities that affect the user interface.</span></span> <span data-ttu-id="b3d33-108">You can decide to wait and publish a set of related changes together.</span><span class="sxs-lookup"><span data-stu-id="b3d33-108">You can decide to wait and publish a set of related changes together.</span></span>  
  
 <span data-ttu-id="b3d33-109">Only published customizations are exported with a solution.</span><span class="sxs-lookup"><span data-stu-id="b3d33-109">Only published customizations are exported with a solution.</span></span> <span data-ttu-id="b3d33-110">You should always publish customizations before exporting a solution.</span><span class="sxs-lookup"><span data-stu-id="b3d33-110">You should always publish customizations before exporting a solution.</span></span>  
  
 <span data-ttu-id="b3d33-111">Khi bạn thực hiện tuỳ chỉnh mà sẽ xuất hiện trong [!INCLUDE[pn_moca_full](../../includes/pn-moca-full.md)], bạn nên luôn xuất bản tuỳ chỉnh của bạn rõ ràng để đảm bảo rằng mỗi mục được đồng bộ hoá với các ứng dụng [!INCLUDE[pn_moca_short](../../includes/pn-moca-short.md)].</span><span class="sxs-lookup"><span data-stu-id="b3d33-111">When you perform customizations that will appear in [!INCLUDE[pn_moca_full](../../includes/pn-moca-full.md)], you should always explicitly publish your customizations to make sure that every item is synchronized with the [!INCLUDE[pn_moca_short](../../includes/pn-moca-short.md)] application.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b3d33-112">Xuất bản tùy chỉnh có thể can thiệp đến hoạt động bình thường hệ thống.</span><span class="sxs-lookup"><span data-stu-id="b3d33-112">Publishing customizations can interfere with normal system operation.</span></span> <span data-ttu-id="b3d33-113">In a production environment, we recommend that you schedule publishing customizations when it’s least disruptive to users.</span><span class="sxs-lookup"><span data-stu-id="b3d33-113">In a production environment, we recommend that you schedule publishing customizations when it’s least disruptive to users.</span></span>  
  
## <a name="publishing-programmatically"></a><span data-ttu-id="b3d33-114">Publishing programmatically</span><span class="sxs-lookup"><span data-stu-id="b3d33-114">Publishing programmatically</span></span>  
 <span data-ttu-id="b3d33-115">The following table lists the two messages that you can use to publish customizations.</span><span class="sxs-lookup"><span data-stu-id="b3d33-115">The following table lists the two messages that you can use to publish customizations.</span></span>  
  
|<span data-ttu-id="b3d33-116">Thông báo</span><span class="sxs-lookup"><span data-stu-id="b3d33-116">Message</span></span>|<span data-ttu-id="b3d33-117">Mô tả</span><span class="sxs-lookup"><span data-stu-id="b3d33-117">Description</span></span>|  
|-------------|-----------------|  
|<xref:Microsoft.Crm.Sdk.Messages.PublishAllXmlRequest>|<span data-ttu-id="b3d33-118">Publishes all customizations.</span><span class="sxs-lookup"><span data-stu-id="b3d33-118">Publishes all customizations.</span></span>|  
|<xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest>|<span data-ttu-id="b3d33-119">Publishes the specified customizations.</span><span class="sxs-lookup"><span data-stu-id="b3d33-119">Publishes the specified customizations.</span></span>|  
  
 <span data-ttu-id="b3d33-120">When you use the `PublishXmlRequest` message, you specify which items you want to publish by using the <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest.ParameterXml> parameter.</span><span class="sxs-lookup"><span data-stu-id="b3d33-120">When you use the `PublishXmlRequest` message, you specify which items you want to publish by using the <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest.ParameterXml> parameter.</span></span> <span data-ttu-id="b3d33-121">`ParameterXML` must comply with the [Publish Request Schema](publish-request-schema.md).</span><span class="sxs-lookup"><span data-stu-id="b3d33-121">`ParameterXML` must comply with the [Publish Request Schema](publish-request-schema.md).</span></span>  
  
<a name="BKMK_RetrieveUnpublishedMetadata"></a>   
## <a name="retrieving-unpublished-metadata"></a><span data-ttu-id="b3d33-122">Retrieving unpublished metadata</span><span class="sxs-lookup"><span data-stu-id="b3d33-122">Retrieving unpublished metadata</span></span>  
 <span data-ttu-id="b3d33-123">If you want to create an application to edit customizable items in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, you must retrieve any unpublished definitions of those items.</span><span class="sxs-lookup"><span data-stu-id="b3d33-123">If you want to create an application to edit customizable items in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, you must retrieve any unpublished definitions of those items.</span></span> <span data-ttu-id="b3d33-124">If a developer defines some changes but does not publish them, your application must be able to retrieve them to display them in the user interface.</span><span class="sxs-lookup"><span data-stu-id="b3d33-124">If a developer defines some changes but does not publish them, your application must be able to retrieve them to display them in the user interface.</span></span>  
  
 <span data-ttu-id="b3d33-125">Use the following two methods to retrieve unpublished metadata:</span><span class="sxs-lookup"><span data-stu-id="b3d33-125">Use the following two methods to retrieve unpublished metadata:</span></span>  
  
 <span data-ttu-id="b3d33-126">**RetrieveAsIfPublished parameter**</span><span class="sxs-lookup"><span data-stu-id="b3d33-126">**RetrieveAsIfPublished parameter**</span></span>  
 <span data-ttu-id="b3d33-127">Retrieves entity, attribute, entity relationship, and option set data by using the following messages:</span><span class="sxs-lookup"><span data-stu-id="b3d33-127">Retrieves entity, attribute, entity relationship, and option set data by using the following messages:</span></span>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllOptionSetsRequest>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAttributeRequest>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityRequest>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveOptionSetRequest>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveRelationshipRequest>  
  
  <span data-ttu-id="b3d33-128">**RetrieveUnpublished Request**</span><span class="sxs-lookup"><span data-stu-id="b3d33-128">**RetrieveUnpublished Request**</span></span>  
  <span data-ttu-id="b3d33-129">Retrieves user interface items, such as form, template, visualization and Web resource definitions, by using the following messages:</span><span class="sxs-lookup"><span data-stu-id="b3d33-129">Retrieves user interface items, such as form, template, visualization and Web resource definitions, by using the following messages:</span></span>  
  
- <xref:Microsoft.Crm.Sdk.Messages.RetrieveUnpublishedRequest>  
  
- <xref:Microsoft.Crm.Sdk.Messages.RetrieveUnpublishedMultipleRequest>  
  
### <a name="see-also"></a><span data-ttu-id="b3d33-130">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b3d33-130">See also</span></span>  
 <span data-ttu-id="b3d33-131">[Customize Dynamics 365 for Customer Engagement](customize-applications.md) </span><span class="sxs-lookup"><span data-stu-id="b3d33-131">[Customize Dynamics 365 for Customer Engagement](customize-applications.md) </span></span>  
 <span data-ttu-id="b3d33-132">[Extend the Metadata Model for Microsoft Dynamics 365 for Customer Engagement](../org-service/use-organization-service-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="b3d33-132">[Extend the Metadata Model for Microsoft Dynamics 365 for Customer Engagement](../org-service/use-organization-service-metadata.md) </span></span>  
 <span data-ttu-id="b3d33-133">[Publish request schema](publish-request-schema.md) </span><span class="sxs-lookup"><span data-stu-id="b3d33-133">[Publish request schema](publish-request-schema.md) </span></span>  
 <span data-ttu-id="b3d33-134">[Customize Entity Forms in Microsoft Dynamics 365 for Customer Engagement](customize-entity-forms.md) </span><span class="sxs-lookup"><span data-stu-id="b3d33-134">[Customize Entity Forms in Microsoft Dynamics 365 for Customer Engagement](customize-entity-forms.md) </span></span>  
 <span data-ttu-id="b3d33-135">[Customize Entity Views in Microsoft Dynamics 365 for Customer Engagement](customize-entity-views.md) </span><span class="sxs-lookup"><span data-stu-id="b3d33-135">[Customize Entity Views in Microsoft Dynamics 365 for Customer Engagement](customize-entity-views.md) </span></span>  
 <span data-ttu-id="b3d33-136">[Customize Global Option Sets in Microsoft Dynamics 365 for Customer Engagement](../org-service/customize-global-option-sets.md) </span><span class="sxs-lookup"><span data-stu-id="b3d33-136">[Customize Global Option Sets in Microsoft Dynamics 365 for Customer Engagement](../org-service/customize-global-option-sets.md) </span></span>  
 <span data-ttu-id="b3d33-137">[Change Application Navigation using the SiteMap](/developer/customize-dev/change-application-navigation-using-sitemap.md) </span><span class="sxs-lookup"><span data-stu-id="b3d33-137">[Change Application Navigation using the SiteMap](/developer/customize-dev/change-application-navigation-using-sitemap.md) </span></span>  
 <span data-ttu-id="b3d33-138">[Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="b3d33-138">[Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="b3d33-139">[Open Forms, Views, and Dialogs with a URL](../open-forms-views-dialogs-reports-url.md) </span><span class="sxs-lookup"><span data-stu-id="b3d33-139">[Open Forms, Views, and Dialogs with a URL](../open-forms-views-dialogs-reports-url.md) </span></span>  
 <span data-ttu-id="b3d33-140">[Client scripting in Customer Engagement using JavaScript](../clientapi/client-scripting.md) </span><span class="sxs-lookup"><span data-stu-id="b3d33-140">[Client scripting in Customer Engagement using JavaScript](../clientapi/client-scripting.md) </span></span>  
 [<span data-ttu-id="b3d33-141">Web Resources for Microsoft Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="b3d33-141">Web Resources for Microsoft Dynamics 365 for Customer Engagement</span></span>](../web-resources.md)   
