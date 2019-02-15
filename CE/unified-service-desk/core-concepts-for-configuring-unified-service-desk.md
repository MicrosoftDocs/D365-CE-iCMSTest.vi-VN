---
title: Core concepts for configuring Unified Service Desk | MicrosoftDocs
descriptions: Unified Service Desk provides an object-oriented kind of configuration and development experience through its hosted control implementation where the hosted control is equivalent to the object in a typical object-oriented development, and is used throughout Unified Service Desk to provide its loose coupling of components.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 3c35c1e5-47eb-40e6-ac3a-8359bef9afd3
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 2198d86d623606d202570a979f881a91197f69e8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388178"
---
# <a name="core-concepts-for-configuring-unified-service-desk"></a><span data-ttu-id="761d1-102">Core concepts for configuring Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="761d1-102">Core concepts for configuring Unified Service Desk</span></span>
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="761d1-103">provides an object-oriented kind of configuration and development experience through its *hosted control implementation* where the hosted control is equivalent to the object in a typical object-oriented development, and is used throughout [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to provide its loose coupling of components.</span><span class="sxs-lookup"><span data-stu-id="761d1-103">provides an object-oriented kind of configuration and development experience through its *hosted control implementation* where the hosted control is equivalent to the object in a typical object-oriented development, and is used throughout [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to provide its loose coupling of components.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="761d1-104">[Hosted Controls](../unified-service-desk/unified-service-desk-hosted-controls.md)</span><span class="sxs-lookup"><span data-stu-id="761d1-104">[Hosted Controls](../unified-service-desk/unified-service-desk-hosted-controls.md)</span></span>  
  
 <span data-ttu-id="761d1-105">Sơ đồ dưới đây mô tả các khái niệm phát triển định hướng đối tượng và khái niệm tương đương của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="761d1-105">The following diagram depicts the object-oriented development concepts and the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] equivalents.</span></span>  
  
 <span data-ttu-id="761d1-106">![USD equivalents for object-oriented concepts](../unified-service-desk/media/crm-itpro-usd-oopsequivalent.png "USD equivalents for object-oriented concepts")</span><span class="sxs-lookup"><span data-stu-id="761d1-106">![USD equivalents for object-oriented concepts](../unified-service-desk/media/crm-itpro-usd-oopsequivalent.png "USD equivalents for object-oriented concepts")</span></span>  
  
 <span data-ttu-id="761d1-107">However, there are some important differences between [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] implementations and the typical object-oriented design:</span><span class="sxs-lookup"><span data-stu-id="761d1-107">However, there are some important differences between [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] implementations and the typical object-oriented design:</span></span>  
  
- <span data-ttu-id="761d1-108">**Tham số thay thế**, không giống như thuộc tính, được lưu trữ bên ngoài các đối tượng (kiểm soát tổ chức trong trường hợp của [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]) chính nó.</span><span class="sxs-lookup"><span data-stu-id="761d1-108">**Replacement parameters**, unlike properties, are stored external to the object (hosted control in the case of [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]) itself.</span></span> <span data-ttu-id="761d1-109">This has a distinct advantage in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] that the properties persist longer than the life of the object, thereby allowing action calls to access the properties for use in parameters or logic long after the hosted control that exposed the parameter has been closed.</span><span class="sxs-lookup"><span data-stu-id="761d1-109">This has a distinct advantage in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] that the properties persist longer than the life of the object, thereby allowing action calls to access the properties for use in parameters or logic long after the hosted control that exposed the parameter has been closed.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="761d1-110">[Replacement parameters](../unified-service-desk/replacement-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="761d1-110">[Replacement parameters](../unified-service-desk/replacement-parameters.md)</span></span>  
  
- <span data-ttu-id="761d1-111">**[!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)]hành động** tương đương với tuyên bố phương pháp.</span><span class="sxs-lookup"><span data-stu-id="761d1-111">**[!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions** are equivalent to the method declaration.</span></span> <span data-ttu-id="761d1-112">The action must first be defined by the underlying object that implements the action, and then it can be declared in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps as a usable action.</span><span class="sxs-lookup"><span data-stu-id="761d1-112">The action must first be defined by the underlying object that implements the action, and then it can be declared in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps as a usable action.</span></span> <span data-ttu-id="761d1-113">Action calls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] are essentially calls to these [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions and typically use replacement parameters as the parameters to the specific UII actions.</span><span class="sxs-lookup"><span data-stu-id="761d1-113">Action calls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] are essentially calls to these [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions and typically use replacement parameters as the parameters to the specific UII actions.</span></span> <span data-ttu-id="761d1-114">Vì vậy, trong khi hành động UII đại diện cho tuyên bố hành động có thể được thực hiện, các cuộc gọi hành động đại diện cho các cuộc gọi thực tế để hành động.</span><span class="sxs-lookup"><span data-stu-id="761d1-114">So while UII actions represent the declaration of the action that can be executed, the action calls represent the actual call to the action.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="761d1-115">[UII actions](../unified-service-desk/uii-actions.md), [Action calls](../unified-service-desk/action-calls.md)</span><span class="sxs-lookup"><span data-stu-id="761d1-115">[UII actions](../unified-service-desk/uii-actions.md), [Action calls](../unified-service-desk/action-calls.md)</span></span>  
  
- <span data-ttu-id="761d1-116">**Events** in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] make one or more action calls, which internally call UII actions on other objects.</span><span class="sxs-lookup"><span data-stu-id="761d1-116">**Events** in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] make one or more action calls, which internally call UII actions on other objects.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="761d1-117">[Events](../unified-service-desk/events.md)</span><span class="sxs-lookup"><span data-stu-id="761d1-117">[Events](../unified-service-desk/events.md)</span></span>  
  
## <a name="reference"></a><span data-ttu-id="761d1-118">Tham chiếu</span><span class="sxs-lookup"><span data-stu-id="761d1-118">Reference</span></span>  
 [<span data-ttu-id="761d1-119">Hosted control types and action/event reference</span><span class="sxs-lookup"><span data-stu-id="761d1-119">Hosted control types and action/event reference</span></span>](../unified-service-desk/hosted-control-types-action-event-reference.md)  
    
  
## <a name="related-sections"></a><span data-ttu-id="761d1-120">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="761d1-120">Related Sections</span></span>  
 [<span data-ttu-id="761d1-121">Learn to use Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="761d1-121">Learn to use Unified Service Desk</span></span>](../unified-service-desk/learn-to-use-unified-service-desk.md)  
  
 [<span data-ttu-id="761d1-122">Get started with configuring your agent application</span><span class="sxs-lookup"><span data-stu-id="761d1-122">Get started with configuring your agent application</span></span>](../unified-service-desk/get-started-configuring-agent-application.md)  
  
 [<span data-ttu-id="761d1-123">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="761d1-123">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
