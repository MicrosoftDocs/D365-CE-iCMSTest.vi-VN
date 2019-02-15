---
title: 'Sample: Query metadata and detect changes (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample demonstrates how to use the classes and methods in the Query and Metadata namespaces to query for specific items of metadata and then track changes to the organization metadata. '
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1df1931b-51a2-4992-9985-cb6da7605ed5
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 21
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 90b2213ee7be88263e13a77026242ac7d1450091
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388493"
---
# <a name="sample-query-metadata-and-detect-changes"></a><span data-ttu-id="b4972-103">Sample: Query metadata and detect changes</span><span class="sxs-lookup"><span data-stu-id="b4972-103">Sample: Query metadata and detect changes</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b4972-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="b4972-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="b4972-105">Download the sample: [Query metadata and detect changes](https://code.msdn.microsoft.com/Sample-for-query-metadata-98848365).</span><span class="sxs-lookup"><span data-stu-id="b4972-105">Download the sample: [Query metadata and detect changes](https://code.msdn.microsoft.com/Sample-for-query-metadata-98848365).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b4972-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="b4972-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="b4972-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="b4972-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="b4972-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="b4972-108">Demonstrates</span></span>  
 <span data-ttu-id="b4972-109">This sample shows how to use the classes and methods in the <xref:Microsoft.Xrm.Sdk.Metadata.Query> and <xref:Microsoft.Xrm.Sdk.Metadata> namespaces to query for specific items of metadata and then track changes to the organization metadata.</span><span class="sxs-lookup"><span data-stu-id="b4972-109">This sample shows how to use the classes and methods in the <xref:Microsoft.Xrm.Sdk.Metadata.Query> and <xref:Microsoft.Xrm.Sdk.Metadata> namespaces to query for specific items of metadata and then track changes to the organization metadata.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b4972-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="b4972-110">Example</span></span>  
 <span data-ttu-id="b4972-111">This sample creates an in-memory cache of all option-set option labels for certain entities.</span><span class="sxs-lookup"><span data-stu-id="b4972-111">This sample creates an in-memory cache of all option-set option labels for certain entities.</span></span> <span data-ttu-id="b4972-112">Then, a custom entity that contains OptionSet attributes is added and the cache of option-set option labels is updated.</span><span class="sxs-lookup"><span data-stu-id="b4972-112">Then, a custom entity that contains OptionSet attributes is added and the cache of option-set option labels is updated.</span></span> <span data-ttu-id="b4972-113">Then a single option is added to one of the custom OptionSet attributes and the cache is updated to add it.</span><span class="sxs-lookup"><span data-stu-id="b4972-113">Then a single option is added to one of the custom OptionSet attributes and the cache is updated to add it.</span></span> <span data-ttu-id="b4972-114">Finally, the custom entity is deleted and the cache of option-set option labels is again updated to reflect this change.</span><span class="sxs-lookup"><span data-stu-id="b4972-114">Finally, the custom entity is deleted and the cache of option-set option labels is again updated to reflect this change.</span></span>  
  
 <span data-ttu-id="b4972-115">The sample will display output similar to the following when it is complete.</span><span class="sxs-lookup"><span data-stu-id="b4972-115">The sample will display output similar to the following when it is complete.</span></span>  
  
- <span data-ttu-id="b4972-116">463 option labels for 5 entities added to the cache.</span><span class="sxs-lookup"><span data-stu-id="b4972-116">463 option labels for 5 entities added to the cache.</span></span>  
  
- <span data-ttu-id="b4972-117">ClientVersionStamp: 296297!10/22/2012 21:41:57</span><span class="sxs-lookup"><span data-stu-id="b4972-117">ClientVersionStamp: 296297!10/22/2012 21:41:57</span></span>  
  
- <span data-ttu-id="b4972-118">Adding a custom entity named sample_SampleEntityForMetadataQuery with a custom optionset attribute named : sample_ExampleOptionSet</span><span class="sxs-lookup"><span data-stu-id="b4972-118">Adding a custom entity named sample_SampleEntityForMetadataQuery with a custom optionset attribute named : sample_ExampleOptionSet</span></span>  
  
- <span data-ttu-id="b4972-119">8 option labels for 1 entities were added to the cache.</span><span class="sxs-lookup"><span data-stu-id="b4972-119">8 option labels for 1 entities were added to the cache.</span></span>  
  
- <span data-ttu-id="b4972-120">471 Option Labels cached</span><span class="sxs-lookup"><span data-stu-id="b4972-120">471 Option Labels cached</span></span>  
  
- <span data-ttu-id="b4972-121">No Option Labels removed.</span><span class="sxs-lookup"><span data-stu-id="b4972-121">No Option Labels removed.</span></span>  
  
- <span data-ttu-id="b4972-122">ClientVersionStamp: 296646!10/22/2012 21:42:06</span><span class="sxs-lookup"><span data-stu-id="b4972-122">ClientVersionStamp: 296646!10/22/2012 21:42:06</span></span>  
  
- <span data-ttu-id="b4972-123">Adding an additional option to the sample_ExampleOptionSet attribute options.</span><span class="sxs-lookup"><span data-stu-id="b4972-123">Adding an additional option to the sample_ExampleOptionSet attribute options.</span></span>  
  
- <span data-ttu-id="b4972-124">1 option labels for 1 entities were added to the cache.</span><span class="sxs-lookup"><span data-stu-id="b4972-124">1 option labels for 1 entities were added to the cache.</span></span>  
  
- <span data-ttu-id="b4972-125">472 Option Labels cached</span><span class="sxs-lookup"><span data-stu-id="b4972-125">472 Option Labels cached</span></span>  
  
- <span data-ttu-id="b4972-126">No Option Labels removed.</span><span class="sxs-lookup"><span data-stu-id="b4972-126">No Option Labels removed.</span></span>  
  
- <span data-ttu-id="b4972-127">ClientVersionStamp: 296649!10/22/2012 21:42:16</span><span class="sxs-lookup"><span data-stu-id="b4972-127">ClientVersionStamp: 296649!10/22/2012 21:42:16</span></span>  
  
- <span data-ttu-id="b4972-128">Current Options: 472</span><span class="sxs-lookup"><span data-stu-id="b4972-128">Current Options: 472</span></span>  
  
- <span data-ttu-id="b4972-129">Deleting the sample_SampleEntityForMetadataQuery custom entity</span><span class="sxs-lookup"><span data-stu-id="b4972-129">Deleting the sample_SampleEntityForMetadataQuery custom entity</span></span>  
  
- <span data-ttu-id="b4972-130">No option labels were added to the cache.</span><span class="sxs-lookup"><span data-stu-id="b4972-130">No option labels were added to the cache.</span></span>  
  
- <span data-ttu-id="b4972-131">9 Option Labels removed</span><span class="sxs-lookup"><span data-stu-id="b4972-131">9 Option Labels removed</span></span>  
  
- <span data-ttu-id="b4972-132">463 Total Option Labels currently cached</span><span class="sxs-lookup"><span data-stu-id="b4972-132">463 Total Option Labels currently cached</span></span>  
  
- <span data-ttu-id="b4972-133">ClientVersionStamp: 297079!10/22/2012 21:42:34</span><span class="sxs-lookup"><span data-stu-id="b4972-133">ClientVersionStamp: 297079!10/22/2012 21:42:34</span></span>  
  
  [!code-csharp[MetadataQuery#MetadataQuery](../../snippets/csharp/CRMV8/metadataquery/cs/metadataquery.cs#metadataquery)]  
  
### <a name="see-also"></a><span data-ttu-id="b4972-134">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b4972-134">See also</span></span>  
 [<span data-ttu-id="b4972-135">Retrieve and detect changes to metadata</span><span class="sxs-lookup"><span data-stu-id="b4972-135">Retrieve and detect changes to metadata</span></span>](../retrieve-detect-changes-metadata.md)
