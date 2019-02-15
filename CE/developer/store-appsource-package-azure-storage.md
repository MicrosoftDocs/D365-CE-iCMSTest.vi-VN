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
# <a name="step-5-store-your-appsource-package-on-azure-storage-and-generate-a-url-with-sas-key"></a>Step 5: Store your AppSource Package on Azure Storage and generate a URL with SAS key

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Microsoft Azure Storage is a Microsoft-managed cloud service that provides storage that is highly available, secure, durable, scalable, and redundant. More information: [Introduction to Microsoft Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-introduction).

To maintain security of your files, all app developers must store their AppSource package file in a Microsoft Azure Blob storage account, and use a Shared Access Signature (SAS) key to share the package file. Your package file is retrieved from your Azure Storage location for certification, and then for AppSource trials.

## <a name="before-you-upload-your-package"></a>Before you upload your package

Download and install the Microsoft Azure Storage Explorer from [http://storageexplorer.com](http://storageexplorer.com).

Azure Storage Explorer lets you easily manage the contents of your storage account.

## <a name="upload-your-package-and-generate-a-url-with-sas-key"></a>Upload your package and generate a URL with SAS key

To upload your package to Azure Blob storage:

1. Create a free trial or pay as you go Azure account at [https://azure.microsoft.com](https://azure.microsoft.com).
2. Sign in to Azure Management portal at [https://portal.azure.com](https://portal.azure.com).
3. Create a new Storage account by clicking  > **Storage** > **Storage account - blob, file, table, queue**.
    
   ![](media/appsource-storageaccount-pic1.png)

4. On the **Create storage account** page, specify **Name**, **Resource group**, and **Location** for your storage account. Leave the rest of the fields with the default options. Bấm **Tạo**. 

   ![](media/appsource-storageaccount-pic2.png)
 
  
5. After your storage account is created, navigate to the newly created resource group, and create a new Blob container. Under **Blob Service**, select **Containers**, and then **+ Container**.

   ![](media/appsource-storageaccount-pic3.png)

6. Specify a name for your container, and select the **Public access level** as **Blob**. Bấm **OK**.

   ![](media/appsource-storageaccount-pic4.png)

7. Start Azure Storage Explorer on your computer, and connect to your Azure Storage account by signing in using the same account with which you created your Azure Storage account.

8. In Azure Storage Explorer, select the newly created container, and then select **Upload** > **Upload Files** to upload the app source package that you created in [Step 4: Create an AppSource package for your app](create-package-app-appsource.md). 

   ![](media/appsource-storageaccount-pic5.png)

9. Browse to the AppSource package file on your computer, and select to upload it.

10. Right-click on the uploaded AppSource package file, and select **Get Shared Access Signature**.

    ![](media/appsource-storageaccount-pic6.png)

11. On the **Shared Access Signature** page, modify the **Expiry time** value to make the Shared Access Signature (SAS) active for a month from the **Start time**. Bấm **Tạo**.

    ![](media/appsource-storageaccount-pic7.png)

12. The next page displays information about the generated SAS information. Copy the **URL** value and save it for later. You will need to specify this URL while creating an offer in the Cloud Partner Portal.

    ![](media/appsource-storageaccount-pic8.png)


> [!div class="nextstepaction"]
> [Next steps: Submit your app on Cloud Partner Portal](next-steps-submit-app-cloud-partner-portal.md)
