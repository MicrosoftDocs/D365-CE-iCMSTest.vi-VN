---
title: Modify the messages for an entity (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about editing the entity messages by exporting, editing, and importing translations.
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
- entities, updating entity display strings
- modifying messages for entities, updating entity display strings
- modifying messages for entities, editing text messages by exporting; editing; and importing translations
- modifying messages for entities, manually editing entity messages
- modifying messages for entities, customizing display names of system entities or attributes
- entities, manually editing entity messages
- text messages, editing by exporting; editing; and importing translations
- entities, customizing display names of system entities or attributes
- modifying messages for entities, editing messages so that they match your custom display names
- messages, manually editing entity messages
- messages, editing to match your custom display names
ms.assetid: ab9e81bc-d218-4438-8a09-cc64db08bb40
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 950a18bf2ce36bd2077155dbc0ed697269aa97ca
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387238"
---
# <a name="modify-the-messages-for-an-entity"></a><span data-ttu-id="54586-103">Modify the messages for an entity</span><span class="sxs-lookup"><span data-stu-id="54586-103">Modify the messages for an entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="54586-104">When you customize system entity or system attribute display names, some messages displayed by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps will reference the default display names.</span><span class="sxs-lookup"><span data-stu-id="54586-104">When you customize system entity or system attribute display names, some messages displayed by [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps will reference the default display names.</span></span> <span data-ttu-id="54586-105">Edit the default messages to match your customized display names.</span><span class="sxs-lookup"><span data-stu-id="54586-105">Edit the default messages to match your customized display names.</span></span>  
  
## <a name="edit-messages-by-exporting-editing-and-importing-translations"></a><span data-ttu-id="54586-106">Edit messages by exporting, editing, and importing translations</span><span class="sxs-lookup"><span data-stu-id="54586-106">Edit messages by exporting, editing, and importing translations</span></span>

 <span data-ttu-id="54586-107">You can edit text values for the base language exported by using the feature that allows for exporting and importing translations.</span><span class="sxs-lookup"><span data-stu-id="54586-107">You can edit text values for the base language exported by using the feature that allows for exporting and importing translations.</span></span> <span data-ttu-id="54586-108">When you export translations, you will download a compressed file.</span><span class="sxs-lookup"><span data-stu-id="54586-108">When you export translations, you will download a compressed file.</span></span> <span data-ttu-id="54586-109">Extract the files and edit the CRMTranslations.xml file by using [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)].</span><span class="sxs-lookup"><span data-stu-id="54586-109">Extract the files and edit the CRMTranslations.xml file by using [!INCLUDE[pn_MS_Excel_Full](../includes/pn-ms-excel-full.md)].</span></span> <span data-ttu-id="54586-110">You can edit display strings and localized labels.</span><span class="sxs-lookup"><span data-stu-id="54586-110">You can edit display strings and localized labels.</span></span> <span data-ttu-id="54586-111">After editing the base language data in the exported file, you must compress the XRMTranslations.xml and [Content_Types].xml files and import them.</span><span class="sxs-lookup"><span data-stu-id="54586-111">After editing the base language data in the exported file, you must compress the XRMTranslations.xml and [Content_Types].xml files and import them.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="54586-112">You should evaluate each instance of the strings you want to change and look for variants that include uppercase letters or plural references.</span><span class="sxs-lookup"><span data-stu-id="54586-112">You should evaluate each instance of the strings you want to change and look for variants that include uppercase letters or plural references.</span></span> <span data-ttu-id="54586-113">Avoid using a global find/replace.</span><span class="sxs-lookup"><span data-stu-id="54586-113">Avoid using a global find/replace.</span></span>
  
## <a name="manually-edit-entity-messages"></a><span data-ttu-id="54586-114">Manually edit entity messages</span><span class="sxs-lookup"><span data-stu-id="54586-114">Manually edit entity messages</span></span>

 <span data-ttu-id="54586-115">For entity messages related to a specific entity, you can manually edit these messages in the entity customization user interface.</span><span class="sxs-lookup"><span data-stu-id="54586-115">For entity messages related to a specific entity, you can manually edit these messages in the entity customization user interface.</span></span> <span data-ttu-id="54586-116">You must save and publish each message and then publish customizations for your changes to be applied.</span><span class="sxs-lookup"><span data-stu-id="54586-116">You must save and publish each message and then publish customizations for your changes to be applied.</span></span>

> [!NOTE]
> <span data-ttu-id="54586-117">The messages displayed in the user interface for a particular entity may not include every instance of the entity name for that entity.</span><span class="sxs-lookup"><span data-stu-id="54586-117">The messages displayed in the user interface for a particular entity may not include every instance of the entity name for that entity.</span></span>  
  
 <!-- Remove the section below if Bug 700890 is not fixed -->

## <a name="programmatically-update-entity-display-strings"></a><span data-ttu-id="54586-118">Cập nhật chuỗi hiển thị thực thể theo phương thức lập trình</span><span class="sxs-lookup"><span data-stu-id="54586-118">Programmatically update entity display strings</span></span>

 <span data-ttu-id="54586-119">The display strings are stored in the `DisplayString` entity.</span><span class="sxs-lookup"><span data-stu-id="54586-119">The display strings are stored in the `DisplayString` entity.</span></span> <span data-ttu-id="54586-120">Note this entity doesn’t contain the default display strings.</span><span class="sxs-lookup"><span data-stu-id="54586-120">Note this entity doesn’t contain the default display strings.</span></span> <span data-ttu-id="54586-121">The two attributes for this entity that contain text are `CustomDisplayString` and `PublishedDisplayString`.</span><span class="sxs-lookup"><span data-stu-id="54586-121">The two attributes for this entity that contain text are `CustomDisplayString` and `PublishedDisplayString`.</span></span> <span data-ttu-id="54586-122">By default, these attribute values are `null` unless the display string has been customized.</span><span class="sxs-lookup"><span data-stu-id="54586-122">By default, these attribute values are `null` unless the display string has been customized.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="54586-123">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="54586-123">See also</span></span>

 [<span data-ttu-id="54586-124">Customize Entity Metadata</span><span class="sxs-lookup"><span data-stu-id="54586-124">Customize Entity Metadata</span></span>](customize-entity-metadata.md)   
 <!--Bug 700890 created to expose this in web api 
 [DisplayString Entity](entities/displaystring.md)   
 -->
 <span data-ttu-id="54586-125">[Sample: Create and update entity metadata](org-service/sample-create-update-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="54586-125">[Sample: Create and update entity metadata](org-service/sample-create-update-entity-metadata.md) </span></span>  
 <span data-ttu-id="54586-126">[Customize Labels to Support Multiple Languages](customize-labels-support-multiple-languages.md) </span><span class="sxs-lookup"><span data-stu-id="54586-126">[Customize Labels to Support Multiple Languages](customize-labels-support-multiple-languages.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.ExportTranslationRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.ImportTranslationRequest>
