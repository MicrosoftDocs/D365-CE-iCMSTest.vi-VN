---
title: 'Best practices: Client scripting in Customer Engagement apps | MicrosoftDocs'
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 16271bd8-cfa8-4a7f-802a-60fbff7c3722
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1a30938780bd87277e7e61a34571091f18d45817
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386312"
---
# <a name="best-practices-client-scripting-in-customer-engagement"></a><span data-ttu-id="fc847-102">Best practices: Client scripting in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="fc847-102">Best practices: Client scripting in Customer Engagement</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="fc847-103">These are some of the best practice tips you could consider while writing your JavaScript code for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="fc847-103">These are some of the best practice tips you could consider while writing your JavaScript code for Customer Engagement.</span></span>

## <a name="define-unique-javascript-function-names"></a><span data-ttu-id="fc847-104">Define unique JavaScript function names</span><span class="sxs-lookup"><span data-stu-id="fc847-104">Define unique JavaScript function names</span></span>

<span data-ttu-id="fc847-105">When you write functions that will be used in JavaScript libraries, your functions may be loaded into a form with other JavaScript libraries.</span><span class="sxs-lookup"><span data-stu-id="fc847-105">When you write functions that will be used in JavaScript libraries, your functions may be loaded into a form with other JavaScript libraries.</span></span> <span data-ttu-id="fc847-106">If another library contains a function that has the same name as a function you provide, whichever function is loaded last is defined for the page.</span><span class="sxs-lookup"><span data-stu-id="fc847-106">If another library contains a function that has the same name as a function you provide, whichever function is loaded last is defined for the page.</span></span> <span data-ttu-id="fc847-107">To avoid having your functions overwritten by functions in another library, you should make sure that your functions have unique names.</span><span class="sxs-lookup"><span data-stu-id="fc847-107">To avoid having your functions overwritten by functions in another library, you should make sure that your functions have unique names.</span></span> <span data-ttu-id="fc847-108">You can use of the following strategies:</span><span class="sxs-lookup"><span data-stu-id="fc847-108">You can use of the following strategies:</span></span>

- <span data-ttu-id="fc847-109">**Unique function prefix**: Define each of your functions using the standard syntax with a consistent name that includes a unique naming convention, as shown in the following example.</span><span class="sxs-lookup"><span data-stu-id="fc847-109">**Unique function prefix**: Define each of your functions using the standard syntax with a consistent name that includes a unique naming convention, as shown in the following example.</span></span>
    ```JavaScript
    function MyUniqueName_performMyAction()
    {
        // Code to perform your action.
    }
    ```
- <span data-ttu-id="fc847-110">**Namespaced library names**: Associate each of your functions with a JavaScript object to create a kind of namespace to use when you call your functions as shown in the following example.</span><span class="sxs-lookup"><span data-stu-id="fc847-110">**Namespaced library names**: Associate each of your functions with a JavaScript object to create a kind of namespace to use when you call your functions as shown in the following example.</span></span>
    ```JavaScript
    //If the MyUniqueName namespace object isn’t defined, create it.
    if (typeof (MyUniqueName) == "undefined")
       { MyUniqueName = {}; }
       // Create Namespace container for functions in this library;
       MyUniqueName.MyFunctions = {
         performMyAction: function(){
         // Code to perform your action.
         //Call another function in your library
         this.anotherAction();
       },
       anotherAction: function(){
         // Code in another function
      }
    };
    ```

    <span data-ttu-id="fc847-111">Then when you use your function you can specify the full name.</span><span class="sxs-lookup"><span data-stu-id="fc847-111">Then when you use your function you can specify the full name.</span></span> <span data-ttu-id="fc847-112">The following example shows this.</span><span class="sxs-lookup"><span data-stu-id="fc847-112">The following example shows this.</span></span>

    ```JavaScript
    MyUniqueName.MyFunctions.performMyAction();
    ```

    <span data-ttu-id="fc847-113">If you call a function within another function you can use the this keyword as a shortcut to the object that contains both functions.</span><span class="sxs-lookup"><span data-stu-id="fc847-113">If you call a function within another function you can use the this keyword as a shortcut to the object that contains both functions.</span></span> <span data-ttu-id="fc847-114">However, if your function is being used as an event handler, the this keyword will refer to the object that the event is occurring on.</span><span class="sxs-lookup"><span data-stu-id="fc847-114">However, if your function is being used as an event handler, the this keyword will refer to the object that the event is occurring on.</span></span>

## <a name="avoid-using-unsupported-methods"></a><span data-ttu-id="fc847-115">Avoid using unsupported methods</span><span class="sxs-lookup"><span data-stu-id="fc847-115">Avoid using unsupported methods</span></span>

<span data-ttu-id="fc847-116">On the Internet, you can find many examples or suggestions that describe using unsupported methods.</span><span class="sxs-lookup"><span data-stu-id="fc847-116">On the Internet, you can find many examples or suggestions that describe using unsupported methods.</span></span> <span data-ttu-id="fc847-117">These may include leveraging undocumented internal function for page controls.</span><span class="sxs-lookup"><span data-stu-id="fc847-117">These may include leveraging undocumented internal function for page controls.</span></span> <span data-ttu-id="fc847-118">These methods may work but because they are not supported, you can’t expect that they will continue to work in future versions of Microsoft Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="fc847-118">These methods may work but because they are not supported, you can’t expect that they will continue to work in future versions of Microsoft Dynamics 365 for Customer Engagement apps.</span></span>

## <a name="avoid-using-jquery-for-form-scripts"></a><span data-ttu-id="fc847-119">Avoid using jQuery for form scripts</span><span class="sxs-lookup"><span data-stu-id="fc847-119">Avoid using jQuery for form scripts</span></span>

<span data-ttu-id="fc847-120">We do not recommend using jQuery in form scripts and ribbon commands.</span><span class="sxs-lookup"><span data-stu-id="fc847-120">We do not recommend using jQuery in form scripts and ribbon commands.</span></span> <span data-ttu-id="fc847-121">Most of the benefit provided by jQuery is that it allows for easy cross-browser manipulation of the DOM.</span><span class="sxs-lookup"><span data-stu-id="fc847-121">Most of the benefit provided by jQuery is that it allows for easy cross-browser manipulation of the DOM.</span></span> <span data-ttu-id="fc847-122">This is explicitly unsupported within form scripts and ribbon commands.</span><span class="sxs-lookup"><span data-stu-id="fc847-122">This is explicitly unsupported within form scripts and ribbon commands.</span></span> <span data-ttu-id="fc847-123">Restrict your scripts to use the objects/methods available in the [Xrm object model](understand-clientapi-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="fc847-123">Restrict your scripts to use the objects/methods available in the [Xrm object model](understand-clientapi-object-model.md).</span></span> 

<span data-ttu-id="fc847-124">If you decide to use the remaining capabilities of jQuery that are useful with Customer Engagement and include the ability to use **$.ajax**, consider the following:</span><span class="sxs-lookup"><span data-stu-id="fc847-124">If you decide to use the remaining capabilities of jQuery that are useful with Customer Engagement and include the ability to use **$.ajax**, consider the following:</span></span>

- <span data-ttu-id="fc847-125">For best performance, don’t load jQuery in the page if you do not need it.</span><span class="sxs-lookup"><span data-stu-id="fc847-125">For best performance, don’t load jQuery in the page if you do not need it.</span></span>
- <span data-ttu-id="fc847-126">Using **$.ajax** to perform requests against the Customer Engagement web services is supported, but there are alternatives.</span><span class="sxs-lookup"><span data-stu-id="fc847-126">Using **$.ajax** to perform requests against the Customer Engagement web services is supported, but there are alternatives.</span></span> <span data-ttu-id="fc847-127">The alternative to using **$.ajax** is to use the browsers **XMLHttpRequest** object directly.</span><span class="sxs-lookup"><span data-stu-id="fc847-127">The alternative to using **$.ajax** is to use the browsers **XMLHttpRequest** object directly.</span></span> <span data-ttu-id="fc847-128">The jQuery **$.ajax** method is just a wrapper for this object.</span><span class="sxs-lookup"><span data-stu-id="fc847-128">The jQuery **$.ajax** method is just a wrapper for this object.</span></span> <span data-ttu-id="fc847-129">If you use the native **XMLHttpRequest** object directly, you do not need to load jQuery.</span><span class="sxs-lookup"><span data-stu-id="fc847-129">If you use the native **XMLHttpRequest** object directly, you do not need to load jQuery.</span></span>
- <span data-ttu-id="fc847-130">Each version of jQuery that is loaded in a page can be a different version.</span><span class="sxs-lookup"><span data-stu-id="fc847-130">Each version of jQuery that is loaded in a page can be a different version.</span></span> <span data-ttu-id="fc847-131">Different versions of jQuery have different behaviors and these can cause problems when multiple versions of jQuery are loaded on the same page.</span><span class="sxs-lookup"><span data-stu-id="fc847-131">Different versions of jQuery have different behaviors and these can cause problems when multiple versions of jQuery are loaded on the same page.</span></span> <span data-ttu-id="fc847-132">There is a technique to mitigate this, but it depends on editing the jQuery library and any other libraries that depend on jQuery.</span><span class="sxs-lookup"><span data-stu-id="fc847-132">There is a technique to mitigate this, but it depends on editing the jQuery library and any other libraries that depend on jQuery.</span></span>


## <a name="write-your-code-for-multiple-browsers"></a><span data-ttu-id="fc847-133">Write your code for multiple browsers</span><span class="sxs-lookup"><span data-stu-id="fc847-133">Write your code for multiple browsers</span></span>

<span data-ttu-id="fc847-134">Dynamics 365 for Customer Engagement apps support mutiple browsers.</span><span class="sxs-lookup"><span data-stu-id="fc847-134">Dynamics 365 for Customer Engagement apps support mutiple browsers.</span></span> <span data-ttu-id="fc847-135">You should make sure that any scripts that you use will work with all supported browsers.</span><span class="sxs-lookup"><span data-stu-id="fc847-135">You should make sure that any scripts that you use will work with all supported browsers.</span></span> <span data-ttu-id="fc847-136">Most of the significant differences between Internet Explorer and other browser have to do with HTML and XML DOM manipulation.</span><span class="sxs-lookup"><span data-stu-id="fc847-136">Most of the significant differences between Internet Explorer and other browser have to do with HTML and XML DOM manipulation.</span></span> <span data-ttu-id="fc847-137">Because HTML DOM manipulation is not supported, if script logic is only performing supported actions and using the [Xrm object model](understand-clientapi-object-model.md), the changes required to support other browsers could be small.</span><span class="sxs-lookup"><span data-stu-id="fc847-137">Because HTML DOM manipulation is not supported, if script logic is only performing supported actions and using the [Xrm object model](understand-clientapi-object-model.md), the changes required to support other browsers could be small.</span></span> 
