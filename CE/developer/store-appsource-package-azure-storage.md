---
title: 'Step 5: Store your AppSource Package on Azure storage and generate a URL with SAS key (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: To maintain security of your files, all app developers must store their AppSource package file in a Microsoft Azure Blob storage account, and use a Shared Access Signature (SAS) key to share the package file. Your package file is retrieved from your Azure Storage location for certification, and then for AppSource trials.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 270d7049-b933-4214-a088-79ed23c4323b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b709f1fefe94dd1083fddec72d8a5f4c1db6a849
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386453"
---
# <a name="step-5-store-your-appsource-package-on-azure-storage-and-generate-a-url-with-sas-key"></a><span data-ttu-id="da343-104">Step 5: Store your AppSource Package on Azure Storage and generate a URL with SAS key</span><span class="sxs-lookup"><span data-stu-id="da343-104">Step 5: Store your AppSource Package on Azure Storage and generate a URL with SAS key</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="da343-105">Microsoft Azure Storage is a Microsoft-managed cloud service that provides storage that is highly available, secure, durable, scalable, and redundant.</span><span class="sxs-lookup"><span data-stu-id="da343-105">Microsoft Azure Storage is a Microsoft-managed cloud service that provides storage that is highly available, secure, durable, scalable, and redundant.</span></span> <span data-ttu-id="da343-106">More information: [Introduction to Microsoft Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-introduction).</span><span class="sxs-lookup"><span data-stu-id="da343-106">More information: [Introduction to Microsoft Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-introduction).</span></span>

<span data-ttu-id="da343-107">To maintain security of your files, all app developers must store their AppSource package file in a Microsoft Azure Blob storage account, and use a Shared Access Signature (SAS) key to share the package file.</span><span class="sxs-lookup"><span data-stu-id="da343-107">To maintain security of your files, all app developers must store their AppSource package file in a Microsoft Azure Blob storage account, and use a Shared Access Signature (SAS) key to share the package file.</span></span> <span data-ttu-id="da343-108">Your package file is retrieved from your Azure Storage location for certification, and then for AppSource trials.</span><span class="sxs-lookup"><span data-stu-id="da343-108">Your package file is retrieved from your Azure Storage location for certification, and then for AppSource trials.</span></span>

## <a name="before-you-upload-your-package"></a><span data-ttu-id="da343-109">Before you upload your package</span><span class="sxs-lookup"><span data-stu-id="da343-109">Before you upload your package</span></span>

<span data-ttu-id="da343-110">Download and install the Microsoft Azure Storage Explorer from [http://storageexplorer.com](http://storageexplorer.com).</span><span class="sxs-lookup"><span data-stu-id="da343-110">Download and install the Microsoft Azure Storage Explorer from [http://storageexplorer.com](http://storageexplorer.com).</span></span>

<span data-ttu-id="da343-111">Azure Storage Explorer lets you easily manage the contents of your storage account.</span><span class="sxs-lookup"><span data-stu-id="da343-111">Azure Storage Explorer lets you easily manage the contents of your storage account.</span></span>

## <a name="upload-your-package-and-generate-a-url-with-sas-key"></a><span data-ttu-id="da343-112">Upload your package and generate a URL with SAS key</span><span class="sxs-lookup"><span data-stu-id="da343-112">Upload your package and generate a URL with SAS key</span></span>

<span data-ttu-id="da343-113">To upload your package to Azure Blob storage:</span><span class="sxs-lookup"><span data-stu-id="da343-113">To upload your package to Azure Blob storage:</span></span>

1. <span data-ttu-id="da343-114">Create a free trial or pay as you go Azure account at [https://azure.microsoft.com](https://azure.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="da343-114">Create a free trial or pay as you go Azure account at [https://azure.microsoft.com](https://azure.microsoft.com).</span></span>
2. <span data-ttu-id="da343-115">Sign in to Azure Management portal at [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="da343-115">Sign in to Azure Management portal at [https://portal.azure.com](https://portal.azure.com).</span></span>
3. <span data-ttu-id="da343-116">Create a new Storage account by clicking  > **Storage** > **Storage account - blob, file, table, queue**.</span><span class="sxs-lookup"><span data-stu-id="da343-116">Create a new Storage account by clicking  > **Storage** > **Storage account - blob, file, table, queue**.</span></span>
    
   ![](media/appsource-storageaccount-pic1.png)

4. <span data-ttu-id="da343-117">On the **Create storage account** page, specify **Name**, **Resource group**, and **Location** for your storage account.</span><span class="sxs-lookup"><span data-stu-id="da343-117">On the **Create storage account** page, specify **Name**, **Resource group**, and **Location** for your storage account.</span></span> <span data-ttu-id="da343-118">Leave the rest of the fields with the default options.</span><span class="sxs-lookup"><span data-stu-id="da343-118">Leave the rest of the fields with the default options.</span></span> <span data-ttu-id="da343-119">Bấm **Tạo**.</span><span class="sxs-lookup"><span data-stu-id="da343-119">Click **Create**.</span></span> 

   ![](media/appsource-storageaccount-pic2.png)
 
  
5. <span data-ttu-id="da343-120">After your storage account is created, navigate to the newly created resource group, and create a new Blob container.</span><span class="sxs-lookup"><span data-stu-id="da343-120">After your storage account is created, navigate to the newly created resource group, and create a new Blob container.</span></span> <span data-ttu-id="da343-121">Under **Blob Service**, select **Containers**, and then **+ Container**.</span><span class="sxs-lookup"><span data-stu-id="da343-121">Under **Blob Service**, select **Containers**, and then **+ Container**.</span></span>

   ![](media/appsource-storageaccount-pic3.png)

6. <span data-ttu-id="da343-122">Specify a name for your container, and select the **Public access level** as **Blob**.</span><span class="sxs-lookup"><span data-stu-id="da343-122">Specify a name for your container, and select the **Public access level** as **Blob**.</span></span> <span data-ttu-id="da343-123">Bấm **OK**.</span><span class="sxs-lookup"><span data-stu-id="da343-123">Click **OK**.</span></span>

   ![](media/appsource-storageaccount-pic4.png)

7. <span data-ttu-id="da343-124">Start Azure Storage Explorer on your computer, and connect to your Azure Storage account by signing in using the same account with which you created your Azure Storage account.</span><span class="sxs-lookup"><span data-stu-id="da343-124">Start Azure Storage Explorer on your computer, and connect to your Azure Storage account by signing in using the same account with which you created your Azure Storage account.</span></span>

8. <span data-ttu-id="da343-125">In Azure Storage Explorer, select the newly created container, and then select **Upload** > **Upload Files** to upload the app source package that you created in [Step 4: Create an AppSource package for your app](create-package-app-appsource.md).</span><span class="sxs-lookup"><span data-stu-id="da343-125">In Azure Storage Explorer, select the newly created container, and then select **Upload** > **Upload Files** to upload the app source package that you created in [Step 4: Create an AppSource package for your app](create-package-app-appsource.md).</span></span> 

   ![](media/appsource-storageaccount-pic5.png)

9. <span data-ttu-id="da343-126">Browse to the AppSource package file on your computer, and select to upload it.</span><span class="sxs-lookup"><span data-stu-id="da343-126">Browse to the AppSource package file on your computer, and select to upload it.</span></span>

10. <span data-ttu-id="da343-127">Right-click on the uploaded AppSource package file, and select **Get Shared Access Signature**.</span><span class="sxs-lookup"><span data-stu-id="da343-127">Right-click on the uploaded AppSource package file, and select **Get Shared Access Signature**.</span></span>

    ![](media/appsource-storageaccount-pic6.png)

11. <span data-ttu-id="da343-128">On the **Shared Access Signature** page, modify the **Expiry time** value to make the Shared Access Signature (SAS) active for a month from the **Start time**.</span><span class="sxs-lookup"><span data-stu-id="da343-128">On the **Shared Access Signature** page, modify the **Expiry time** value to make the Shared Access Signature (SAS) active for a month from the **Start time**.</span></span> <span data-ttu-id="da343-129">Bấm **Tạo**.</span><span class="sxs-lookup"><span data-stu-id="da343-129">Click **Create**.</span></span>

    ![](media/appsource-storageaccount-pic7.png)

12. <span data-ttu-id="da343-130">The next page displays information about the generated SAS information.</span><span class="sxs-lookup"><span data-stu-id="da343-130">The next page displays information about the generated SAS information.</span></span> <span data-ttu-id="da343-131">Copy the **URL** value and save it for later.</span><span class="sxs-lookup"><span data-stu-id="da343-131">Copy the **URL** value and save it for later.</span></span> <span data-ttu-id="da343-132">You will need to specify this URL while creating an offer in the Cloud Partner Portal.</span><span class="sxs-lookup"><span data-stu-id="da343-132">You will need to specify this URL while creating an offer in the Cloud Partner Portal.</span></span>

    ![](media/appsource-storageaccount-pic8.png)


> [!div class="nextstepaction"]
> [<span data-ttu-id="da343-133">Next steps: Submit your app on Cloud Partner Portal</span><span class="sxs-lookup"><span data-stu-id="da343-133">Next steps: Submit your app on Cloud Partner Portal</span></span>](next-steps-submit-app-cloud-partner-portal.md)
