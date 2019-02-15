---
title: Delete data in bulk (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Helps maintain data quality and manage the consumption of system storage by deleting data that is no longer needed.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- bulk delete
- deleting data in bulk in Microsoft Dynamics CRM, about the bulk deletion feature
- deleting data in bulk in Microsoft Dynamics CRM, how the bulk deletion feature helps you delete multiple topics
- bulk deletion feature, about
- deleting data in bulk in Microsoft Dynamics CRM, data cleanup (periodic and scheduled)
- deleting data in bulk in Microsoft Dynamics CRM, tasks for using bulk deletion
- deleting data in bulk in Microsoft Dynamics CRM, failure log
- bulk deletion
- deleting data in bulk in Microsoft Dynamics CRM, email notifications
ms.assetid: 67a3a031-4edf-49de-983b-ba9902223278
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ed981b3778447984bea2400a1bc67c7553f58415
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388438"
---
# <a name="delete-data-in-bulk"></a><span data-ttu-id="93577-103">Delete data in bulk</span><span class="sxs-lookup"><span data-stu-id="93577-103">Delete data in bulk</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="93577-104">Tính năng *xóa hàng loạt* giúp bạn duy trì chất lượng dữ liệu và quản lý việc tiêu thụ lưu trữ hệ thống trong [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] bằng cách xoá dữ liệu mà bạn không còn cần.</span><span class="sxs-lookup"><span data-stu-id="93577-104">The *bulk deletion* feature helps you to maintain data quality and manage the consumption of system storage in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] by deleting data that you no longer need.</span></span>  
  
 <span data-ttu-id="93577-105">Ví dụ, bạn có thể xoá dữ liệu sau với số lượng lớn:</span><span class="sxs-lookup"><span data-stu-id="93577-105">For example, you can delete the following data in bulk:</span></span>  
  
- <span data-ttu-id="93577-106">Dữ liệu cũ.</span><span class="sxs-lookup"><span data-stu-id="93577-106">Stale data.</span></span>  
  
- <span data-ttu-id="93577-107">Dữ liệu mà không liên quan đến kinh doanh.</span><span class="sxs-lookup"><span data-stu-id="93577-107">Data that is irrelevant to the business.</span></span>  
  
- <span data-ttu-id="93577-108">Thử nghiệm không cần thiết hoặc dữ liệu mẫu.</span><span class="sxs-lookup"><span data-stu-id="93577-108">Unneeded test or sample data.</span></span>  
  
- <span data-ttu-id="93577-109">Dữ liệu không được nhập chính xác từ các hệ thống khác.</span><span class="sxs-lookup"><span data-stu-id="93577-109">Data that is incorrectly imported from other systems.</span></span>  
  
  <span data-ttu-id="93577-110">Với xóa hàng loạt, bạn có thể thực hiện thao tác sau:</span><span class="sxs-lookup"><span data-stu-id="93577-110">With bulk deletion you can perform the following operations:</span></span>  
  
- <span data-ttu-id="93577-111">Xóa dữ liệu trên nhiều thực thể.</span><span class="sxs-lookup"><span data-stu-id="93577-111">Delete data across multiple entities.</span></span>  
  
- <span data-ttu-id="93577-112">Xoá hồ sơ cho một thực thể được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="93577-112">Delete records for a specified entity.</span></span>  
  
- <span data-ttu-id="93577-113">Nhận thông báo email khi xóa hàng loạt kết thúc.</span><span class="sxs-lookup"><span data-stu-id="93577-113">Receive email notifications when a bulk deletion finishes.</span></span>  
  
- <span data-ttu-id="93577-114">Xoá dữ liệu định kỳ.</span><span class="sxs-lookup"><span data-stu-id="93577-114">Delete data periodically.</span></span>  
  
- <span data-ttu-id="93577-115">Lên lịch thời gian bắt đầu cho xóa hàng loạt định kỳ.</span><span class="sxs-lookup"><span data-stu-id="93577-115">Schedule the start time of a recurring bulk delete.</span></span>  
  
- <span data-ttu-id="93577-116">Truy xuất thông tin về những thất bại xảy ra trong xóa hàng loạt.</span><span class="sxs-lookup"><span data-stu-id="93577-116">Retrieve the information about the failures that occurred during a bulk deletion.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="93577-117">In This Section</span><span class="sxs-lookup"><span data-stu-id="93577-117">In This Section</span></span>  
 [<span data-ttu-id="93577-118">Running Bulk Delete</span><span class="sxs-lookup"><span data-stu-id="93577-118">Running Bulk Delete</span></span>](run-bulk-delete.md)  
  
 [<span data-ttu-id="93577-119">BulkDeleteOperation Entity</span><span class="sxs-lookup"><span data-stu-id="93577-119">BulkDeleteOperation Entity</span></span>](entities/bulkdeleteoperation.md)  
  
 [<span data-ttu-id="93577-120">BulkDeleteFailure Entity</span><span class="sxs-lookup"><span data-stu-id="93577-120">BulkDeleteFailure Entity</span></span>](entities/bulkdeletefailure.md)  
  
## <a name="related-sections"></a><span data-ttu-id="93577-121">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="93577-121">Related Sections</span></span>  

 [<span data-ttu-id="93577-122">Data Management</span><span class="sxs-lookup"><span data-stu-id="93577-122">Data Management</span></span>](manage-data.md)  
  
 [<span data-ttu-id="93577-123">Nhập dữ liệu</span><span class="sxs-lookup"><span data-stu-id="93577-123">Import data</span></span>](import-data.md)
