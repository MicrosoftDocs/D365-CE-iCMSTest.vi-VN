---
title: 'Walkthrough: Write your first client script in Customer Engagement| MicrosoftDocs'
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: conceptual
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 73dfc13c-a18c-42fc-b511-a37896c2f893
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 05e2686b2c0c251c228f934dfab91db8f2da4839
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385667"
---
# <a name="walkthrough-write-your-first-client-script"></a><span data-ttu-id="af288-102">Walkthrough: Write your first client script</span><span class="sxs-lookup"><span data-stu-id="af288-102">Walkthrough: Write your first client script</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="af288-103">Ready to write your first client script to see things in action.</span><span class="sxs-lookup"><span data-stu-id="af288-103">Ready to write your first client script to see things in action.</span></span> <span data-ttu-id="af288-104">Lets get started; we'll keep it simple.</span><span class="sxs-lookup"><span data-stu-id="af288-104">Lets get started; we'll keep it simple.</span></span>

## <a name="objective"></a><span data-ttu-id="af288-105">Mục tiêu</span><span class="sxs-lookup"><span data-stu-id="af288-105">Objective</span></span>

<span data-ttu-id="af288-106">After completing this walkthrough, you will know how to use your JavaScript code in Customer Engagement, which involves the following steps at a high level:</span><span class="sxs-lookup"><span data-stu-id="af288-106">After completing this walkthrough, you will know how to use your JavaScript code in Customer Engagement, which involves the following steps at a high level:</span></span>
- <span data-ttu-id="af288-107">Write your JavaScript code to address a business issue</span><span class="sxs-lookup"><span data-stu-id="af288-107">Write your JavaScript code to address a business issue</span></span>
- <span data-ttu-id="af288-108">Upload your JavaScript code as a web resource in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="af288-108">Upload your JavaScript code as a web resource in Customer Engagement</span></span>
- <span data-ttu-id="af288-109">Associate the JavaScript functions in the web resource to different client-side events in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="af288-109">Associate the JavaScript functions in the web resource to different client-side events in Customer Engagement.</span></span>

<span data-ttu-id="af288-110">We will draw your attention to important facts during the walkthrough, and provide references to actual methods as appropriate.</span><span class="sxs-lookup"><span data-stu-id="af288-110">We will draw your attention to important facts during the walkthrough, and provide references to actual methods as appropriate.</span></span>

## <a name="step-1-write-your-custom-javascript-code"></a><span data-ttu-id="af288-111">Step 1: Write your custom JavaScript code</span><span class="sxs-lookup"><span data-stu-id="af288-111">Step 1: Write your custom JavaScript code</span></span>

<span data-ttu-id="af288-112">The first step is to identify the business issue you are trying to address using client scripting.</span><span class="sxs-lookup"><span data-stu-id="af288-112">The first step is to identify the business issue you are trying to address using client scripting.</span></span> <span data-ttu-id="af288-113">Once you have identified it, you need to write your JavaScript code containing the custom business logic that addresses your business issue.</span><span class="sxs-lookup"><span data-stu-id="af288-113">Once you have identified it, you need to write your JavaScript code containing the custom business logic that addresses your business issue.</span></span> 

<span data-ttu-id="af288-114">Dynamics 365 for Customer Engagement does not provide a JavaScript editor.</span><span class="sxs-lookup"><span data-stu-id="af288-114">Dynamics 365 for Customer Engagement does not provide a JavaScript editor.</span></span> <span data-ttu-id="af288-115">So, you can use an external authoring tool that provides features to specifically support editing JavaScript files, such as [Notepad++](https://notepad-plus-plus.org/), [Visual Studio Code](https://code.visualstudio.com/docs/languages/javascript), or [Microsoft Visual Studio](https://docs.microsoft.com/en-us/scripting/javascript/).</span><span class="sxs-lookup"><span data-stu-id="af288-115">So, you can use an external authoring tool that provides features to specifically support editing JavaScript files, such as [Notepad++](https://notepad-plus-plus.org/), [Visual Studio Code](https://code.visualstudio.com/docs/languages/javascript), or [Microsoft Visual Studio](https://docs.microsoft.com/en-us/scripting/javascript/).</span></span>

<span data-ttu-id="af288-116">You can review the complete sample code used in the walkthrough later in this topic.</span><span class="sxs-lookup"><span data-stu-id="af288-116">You can review the complete sample code used in the walkthrough later in this topic.</span></span>

<span data-ttu-id="af288-117">Let's look at the code in detail:</span><span class="sxs-lookup"><span data-stu-id="af288-117">Let's look at the code in detail:</span></span>
 
### <a name="detailed-code-explanation"></a><span data-ttu-id="af288-118">Detailed code explanation</span><span class="sxs-lookup"><span data-stu-id="af288-118">Detailed code explanation</span></span>
- <span data-ttu-id="af288-119">**Define namespace**: The code starts by defining a namespace for your custom script.</span><span class="sxs-lookup"><span data-stu-id="af288-119">**Define namespace**: The code starts by defining a namespace for your custom script.</span></span> <span data-ttu-id="af288-120">As a best practice, you should always create namespaced JavaScript libraries to avoid having your functions overriden by functions in another library.</span><span class="sxs-lookup"><span data-stu-id="af288-120">As a best practice, you should always create namespaced JavaScript libraries to avoid having your functions overriden by functions in another library.</span></span>

    ```JavaScript
    var Sdk = window.Sdk || {};
    ``` 
    <span data-ttu-id="af288-121">In this case, all the functions defined in this library can be used as `Sdk.[functionName]`.</span><span class="sxs-lookup"><span data-stu-id="af288-121">In this case, all the functions defined in this library can be used as `Sdk.[functionName]`.</span></span>

- <span data-ttu-id="af288-122">**Define global variables**: The following section defines some global variables to be used in the script.</span><span class="sxs-lookup"><span data-stu-id="af288-122">**Define global variables**: The following section defines some global variables to be used in the script.</span></span> <span data-ttu-id="af288-123">Note that you now don't need to go through the form context to get the user name.</span><span class="sxs-lookup"><span data-stu-id="af288-123">Note that you now don't need to go through the form context to get the user name.</span></span> <span data-ttu-id="af288-124">Context information is now available globally using the **Xrm.Utility.**[getGlobalContext](reference/xrm-utility/getGlobalContext.md) method.</span><span class="sxs-lookup"><span data-stu-id="af288-124">Context information is now available globally using the **Xrm.Utility.**[getGlobalContext](reference/xrm-utility/getGlobalContext.md) method.</span></span>

    ```JavaScript
    // Define some global variables
    var myUniqueId = "_myUniqueId"; // Define an ID for the notification
    var currentUserName = Xrm.Utility.getGlobalContext().userSettings.userName; // get current user name
    var message = currentUserName + ": Your JavaScript code in action!";
    ```
- <span data-ttu-id="af288-125">**Code to execute on the OnLoad event**: This section contains the code that will be executed when the account form loads.</span><span class="sxs-lookup"><span data-stu-id="af288-125">**Code to execute on the OnLoad event**: This section contains the code that will be executed when the account form loads.</span></span> <span data-ttu-id="af288-126">For example, when you create a new account record or when you open an existing account record.</span><span class="sxs-lookup"><span data-stu-id="af288-126">For example, when you create a new account record or when you open an existing account record.</span></span>

    <span data-ttu-id="af288-127">The code uses the `executionContext` object to get the `formContext` object.</span><span class="sxs-lookup"><span data-stu-id="af288-127">The code uses the `executionContext` object to get the `formContext` object.</span></span> <span data-ttu-id="af288-128">When we attach our code with the form event later, we will remember to select the option to pass the [execution context](clientapi-execution-context.md) to this function.</span><span class="sxs-lookup"><span data-stu-id="af288-128">When we attach our code with the form event later, we will remember to select the option to pass the [execution context](clientapi-execution-context.md) to this function.</span></span> <span data-ttu-id="af288-129">Next, we display a form level notification using the [setFormNotification](reference/formContext-ui/setFormNotification.md) method.</span><span class="sxs-lookup"><span data-stu-id="af288-129">Next, we display a form level notification using the [setFormNotification](reference/formContext-ui/setFormNotification.md) method.</span></span> <span data-ttu-id="af288-130">Next, we use the **setTimeOut** method to delay the execution of the [clearFormNotification](reference/formContext-ui/clearFormNotification.md) method to clear the notification after 5 seconds.</span><span class="sxs-lookup"><span data-stu-id="af288-130">Next, we use the **setTimeOut** method to delay the execution of the [clearFormNotification](reference/formContext-ui/clearFormNotification.md) method to clear the notification after 5 seconds.</span></span>

    ```JavaScript
    // Code to run in the form OnLoad event
    this.formOnLoad = function (executionContext) {
        var formContext = executionContext.getFormContext();

        // display the form level notification as an INFO
        formContext.ui.setFormNotification(message, "INFO", myUniqueId);
        
        // Wait for 5 seconds before clearing the notification
        window.setTimeout(function () { formContext.ui.clearFormNotification(myUniqueId); }, 5000);        
    }
    ```
- <span data-ttu-id="af288-131">**Code to execute on the OnChange event**: Code in this sections will be associated with the **Account Name** field in the account form so that it gets executed **only** when you change the account name value.</span><span class="sxs-lookup"><span data-stu-id="af288-131">**Code to execute on the OnChange event**: Code in this sections will be associated with the **Account Name** field in the account form so that it gets executed **only** when you change the account name value.</span></span>

    <span data-ttu-id="af288-132">The code performs a case-insensitive search for "Contoso" in the account name, and if present, automatically sets values for some fields in the account form.</span><span class="sxs-lookup"><span data-stu-id="af288-132">The code performs a case-insensitive search for "Contoso" in the account name, and if present, automatically sets values for some fields in the account form.</span></span>

    ```JavaScript
    // Code to run in the attribute OnChange event 
    this.attributeOnChange = function (executionContext) {
        var formContext = executionContext.getFormContext();

        // Automatically set some field values if the account name contains "Contoso"
        var accountName = formContext.getAttribute("name").getValue();
        if (accountName.toLowerCase().search("contoso") != -1) {
            formContext.getAttribute("websiteurl").setValue("http://www.contoso.com");
            formContext.getAttribute("telephone1").setValue("425-555-0100");
            formContext.getAttribute("description").setValue("Website URL, Phone and Description set using custom script.");
        }
    }
    ```

- <span data-ttu-id="af288-133">**Code to execute on the OnSave event**: The code in this section displays an alert dialog box using the [openAlertDialog](reference/xrm-navigation/openalertdialog.md) method.</span><span class="sxs-lookup"><span data-stu-id="af288-133">**Code to execute on the OnSave event**: The code in this section displays an alert dialog box using the [openAlertDialog](reference/xrm-navigation/openalertdialog.md) method.</span></span> <span data-ttu-id="af288-134">This dialog box displays a message with the **OK** button; user can close the alert by clicking **OK**.</span><span class="sxs-lookup"><span data-stu-id="af288-134">This dialog box displays a message with the **OK** button; user can close the alert by clicking **OK**.</span></span>

    <span data-ttu-id="af288-135">Note that we are not passing in the execution context in this function as its not required to execute **Xrm.Utility.**\* methods.</span><span class="sxs-lookup"><span data-stu-id="af288-135">Note that we are not passing in the execution context in this function as its not required to execute **Xrm.Utility.**\* methods.</span></span> 

    ```JavaScript
    // Code to run in the form OnSave event 
    this.formOnSave = function () {
        // Display an alert dialog
        Xrm.Navigation.openAlertDialog({ text: "Record saved." });
    }
    ```

## <a name="step-2-add-your-javascript-code-in-a-script-web-resource"></a><span data-ttu-id="af288-136">Step 2: Add your JavaScript code in a Script web resource</span><span class="sxs-lookup"><span data-stu-id="af288-136">Step 2: Add your JavaScript code in a Script web resource</span></span>

<span data-ttu-id="af288-137">Now that your code is ready, you want to associate it with events in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="af288-137">Now that your code is ready, you want to associate it with events in Customer Engagement.</span></span> <span data-ttu-id="af288-138">You use [Script web resources](../script-jscript-web-resources.md) in Customer Engagement to upload the script to your Customer Engagement instance, and then associate it with events.</span><span class="sxs-lookup"><span data-stu-id="af288-138">You use [Script web resources](../script-jscript-web-resources.md) in Customer Engagement to upload the script to your Customer Engagement instance, and then associate it with events.</span></span>

1. <span data-ttu-id="af288-139">Navigate to your Customer Engagement instance in browser, and go to **Settings** > **Customizations**.</span><span class="sxs-lookup"><span data-stu-id="af288-139">Navigate to your Customer Engagement instance in browser, and go to **Settings** > **Customizations**.</span></span>
2. <span data-ttu-id="af288-140">In the Customization area, choose **Customize the System**.</span><span class="sxs-lookup"><span data-stu-id="af288-140">In the Customization area, choose **Customize the System**.</span></span>
3. <span data-ttu-id="af288-141">In the solutions explorer, under **Components**, choose **Web Resources**.</span><span class="sxs-lookup"><span data-stu-id="af288-141">In the solutions explorer, under **Components**, choose **Web Resources**.</span></span>  
4. <span data-ttu-id="af288-142">Choose **New** to create a web resource.</span><span class="sxs-lookup"><span data-stu-id="af288-142">Choose **New** to create a web resource.</span></span>
5. <span data-ttu-id="af288-143">In the new web resource dialog, specify the **Name** and **Display Name** for your web resource.</span><span class="sxs-lookup"><span data-stu-id="af288-143">In the new web resource dialog, specify the **Name** and **Display Name** for your web resource.</span></span> <span data-ttu-id="af288-144">For example: "mySampleScript.js" and "Sample: Walkthrough" Script.</span><span class="sxs-lookup"><span data-stu-id="af288-144">For example: "mySampleScript.js" and "Sample: Walkthrough" Script.</span></span> 
6. <span data-ttu-id="af288-145">Select **Script (JScript)** from the **Type** drop-down list.</span><span class="sxs-lookup"><span data-stu-id="af288-145">Select **Script (JScript)** from the **Type** drop-down list.</span></span> <span data-ttu-id="af288-146">You can either upload a file containing your JavaScript code by selecting **Choose File**, or select **Text Editor** and then paste your JavaScript code in the editor.</span><span class="sxs-lookup"><span data-stu-id="af288-146">You can either upload a file containing your JavaScript code by selecting **Choose File**, or select **Text Editor** and then paste your JavaScript code in the editor.</span></span>
    <span data-ttu-id="af288-147">![Create Web resource](../media/clientapi_walkThrough-img1.png)</span><span class="sxs-lookup"><span data-stu-id="af288-147">![Create Web resource](../media/clientapi_walkThrough-img1.png)</span></span>
1. <span data-ttu-id="af288-148">Choose **Save** to create the web resource containing your JavaScript code.</span><span class="sxs-lookup"><span data-stu-id="af288-148">Choose **Save** to create the web resource containing your JavaScript code.</span></span>
2. <span data-ttu-id="af288-149">Choose **Publish** to publish your web resource.</span><span class="sxs-lookup"><span data-stu-id="af288-149">Choose **Publish** to publish your web resource.</span></span>

## <a name="step-3-associate-script-web-resource-to-a-form"></a><span data-ttu-id="af288-150">Step 3: Associate Script web resource to a form</span><span class="sxs-lookup"><span data-stu-id="af288-150">Step 3: Associate Script web resource to a form</span></span>

<span data-ttu-id="af288-151">Associate the web resource containing your JavaScript code to Customer Engagement forms to be able to associate functions in your code with events.</span><span class="sxs-lookup"><span data-stu-id="af288-151">Associate the web resource containing your JavaScript code to Customer Engagement forms to be able to associate functions in your code with events.</span></span> <span data-ttu-id="af288-152">As the JavaScript code in this walkthrough is targeted at the account record, we will associate the web resource with the account form.</span><span class="sxs-lookup"><span data-stu-id="af288-152">As the JavaScript code in this walkthrough is targeted at the account record, we will associate the web resource with the account form.</span></span>

1. <span data-ttu-id="af288-153">Navigate to your Customer Engagement instance in browser, and go to **Sales** > **Accounts** or **Service** > **Accounts**.</span><span class="sxs-lookup"><span data-stu-id="af288-153">Navigate to your Customer Engagement instance in browser, and go to **Sales** > **Accounts** or **Service** > **Accounts**.</span></span>
2. <span data-ttu-id="af288-154">Open an account record, and select **Form** to open the form editor.</span><span class="sxs-lookup"><span data-stu-id="af288-154">Open an account record, and select **Form** to open the form editor.</span></span>

    ![Mở công cụ biên tập biểu mẫu.](../media/clientapi_walkThrough-img2.png)
1. <span data-ttu-id="af288-156">In the form editor, select **Form Properties**.</span><span class="sxs-lookup"><span data-stu-id="af288-156">In the form editor, select **Form Properties**.</span></span>
2. <span data-ttu-id="af288-157">In the **Form Properties** dialog box, under the **Events** tab, click **Add** to search and add your web resource.</span><span class="sxs-lookup"><span data-stu-id="af288-157">In the **Form Properties** dialog box, under the **Events** tab, click **Add** to search and add your web resource.</span></span>

    ![Thêm](../media/clientapi_walkThrough-img3.png)
1. <span data-ttu-id="af288-159">In the next dialog box, search for your web resource name, select it, and then click **Add** to add it as a JavaScript library for the account form.</span><span class="sxs-lookup"><span data-stu-id="af288-159">In the next dialog box, search for your web resource name, select it, and then click **Add** to add it as a JavaScript library for the account form.</span></span>

    ![Lookup record](../media/clientapi_walkThrough-img4.png)

<span data-ttu-id="af288-161">This makes the web resource available to be selected under the **Event Hadlers** section in the **Form Properties** dialog.</span><span class="sxs-lookup"><span data-stu-id="af288-161">This makes the web resource available to be selected under the **Event Hadlers** section in the **Form Properties** dialog.</span></span> <span data-ttu-id="af288-162">Remember that we have three functions in our JavaScript code to be associated with approprite events in the form.</span><span class="sxs-lookup"><span data-stu-id="af288-162">Remember that we have three functions in our JavaScript code to be associated with approprite events in the form.</span></span>

1. <span data-ttu-id="af288-163">Under the **Event Handlers** section, select **Form** as the control and **OnLoad** as the **Event**; click **Add** to add an event handler for the OnLoad event.</span><span class="sxs-lookup"><span data-stu-id="af288-163">Under the **Event Handlers** section, select **Form** as the control and **OnLoad** as the **Event**; click **Add** to add an event handler for the OnLoad event.</span></span>

   ![Form OnLoad](../media/clientapi_walkThrough-img5.png)
1. <span data-ttu-id="af288-165">In the **Handler Properties** dialog box:</span><span class="sxs-lookup"><span data-stu-id="af288-165">In the **Handler Properties** dialog box:</span></span>   

    - <span data-ttu-id="af288-166">Select the name of your web resource from the **Library** drop-down list, and specify **Sdk.formOnLoad** in the **Function** field.</span><span class="sxs-lookup"><span data-stu-id="af288-166">Select the name of your web resource from the **Library** drop-down list, and specify **Sdk.formOnLoad** in the **Function** field.</span></span> <span data-ttu-id="af288-167">The function name is [Namespace].[Function] from your JavaScript code.</span><span class="sxs-lookup"><span data-stu-id="af288-167">The function name is [Namespace].[Function] from your JavaScript code.</span></span>
    - <span data-ttu-id="af288-168">Select **Pass execution context as first parameter** to pass in the execution context as a parameter to this function.</span><span class="sxs-lookup"><span data-stu-id="af288-168">Select **Pass execution context as first parameter** to pass in the execution context as a parameter to this function.</span></span> <span data-ttu-id="af288-169">If you review the function definition in the code, we are passing an **executionContext** object to our function definition, and selecting this option wires them up.</span><span class="sxs-lookup"><span data-stu-id="af288-169">If you review the function definition in the code, we are passing an **executionContext** object to our function definition, and selecting this option wires them up.</span></span>
    
      ![Form OnLoad](../media/clientapi_walkThrough-img6.png)

1. <span data-ttu-id="af288-171">Click **OK** to return to the **Form Properties** diaog box.</span><span class="sxs-lookup"><span data-stu-id="af288-171">Click **OK** to return to the **Form Properties** diaog box.</span></span>
2. <span data-ttu-id="af288-172">Under the **Event Handlers** section, select **OnSave** as the **Event** this time, and click **Add** to add an event handler for the Form OnSave event.</span><span class="sxs-lookup"><span data-stu-id="af288-172">Under the **Event Handlers** section, select **OnSave** as the **Event** this time, and click **Add** to add an event handler for the Form OnSave event.</span></span>

    ![Form OnSave](../media/clientapi_walkThrough-img7.png)

1. <span data-ttu-id="af288-174">In the **Handler Properties** dialog box, select the name of your web resource from the **Library** drop-down list, and specify **Sdk.formOnSave** in the **Function** field.</span><span class="sxs-lookup"><span data-stu-id="af288-174">In the **Handler Properties** dialog box, select the name of your web resource from the **Library** drop-down list, and specify **Sdk.formOnSave** in the **Function** field.</span></span> <span data-ttu-id="af288-175">We won't pass the execution context to the function this time as the **Sdk.formOnSave** function code does not require it.</span><span class="sxs-lookup"><span data-stu-id="af288-175">We won't pass the execution context to the function this time as the **Sdk.formOnSave** function code does not require it.</span></span>

    ![Form OnSave](../media/clientapi_walkThrough-img8.png)

1. <span data-ttu-id="af288-177">Click **OK** to return to the **Form Properties** diaog box.</span><span class="sxs-lookup"><span data-stu-id="af288-177">Click **OK** to return to the **Form Properties** diaog box.</span></span>
2. <span data-ttu-id="af288-178">Under the **Event Handlers** section, select **Account Name** as the control and **OnChange** as the event; click **Add** to add an event handler for the OnChange event.</span><span class="sxs-lookup"><span data-stu-id="af288-178">Under the **Event Handlers** section, select **Account Name** as the control and **OnChange** as the event; click **Add** to add an event handler for the OnChange event.</span></span>

    ![Form OnSave](../media/clientapi_walkThrough-img9.png)

1. <span data-ttu-id="af288-180">In the **Handler Properties** dialog box:</span><span class="sxs-lookup"><span data-stu-id="af288-180">In the **Handler Properties** dialog box:</span></span>   

    - <span data-ttu-id="af288-181">Select the name of your web resource from the **Library** drop-down list, and specify **Sdk.attributeOnChange** in the **Function** field.</span><span class="sxs-lookup"><span data-stu-id="af288-181">Select the name of your web resource from the **Library** drop-down list, and specify **Sdk.attributeOnChange** in the **Function** field.</span></span>
    - <span data-ttu-id="af288-182">Select **Pass execution context as first parameter** to pass in the execution context as a parameter to this function.</span><span class="sxs-lookup"><span data-stu-id="af288-182">Select **Pass execution context as first parameter** to pass in the execution context as a parameter to this function.</span></span> <span data-ttu-id="af288-183">If you review the function definition in the code, we are passing an **executionContext** object to our function definition, and selecting this option wires them up.</span><span class="sxs-lookup"><span data-stu-id="af288-183">If you review the function definition in the code, we are passing an **executionContext** object to our function definition, and selecting this option wires them up.</span></span>
    
      ![Attribute OnChange](../media/clientapi_walkThrough-img10.png) 
1. <span data-ttu-id="af288-185">Click **OK** to return to the **Form Properties** diaog box.</span><span class="sxs-lookup"><span data-stu-id="af288-185">Click **OK** to return to the **Form Properties** diaog box.</span></span>
2. <span data-ttu-id="af288-186">Click **OK** in the **Form Properties** diaog box to return to the form editor.</span><span class="sxs-lookup"><span data-stu-id="af288-186">Click **OK** in the **Form Properties** diaog box to return to the form editor.</span></span>
3. <span data-ttu-id="af288-187">Click **Save** to save the changes to the form.</span><span class="sxs-lookup"><span data-stu-id="af288-187">Click **Save** to save the changes to the form.</span></span>
4. <span data-ttu-id="af288-188">Click **Publish** to publish the form changes.</span><span class="sxs-lookup"><span data-stu-id="af288-188">Click **Publish** to publish the form changes.</span></span>

<span data-ttu-id="af288-189">Thats it!</span><span class="sxs-lookup"><span data-stu-id="af288-189">Thats it!</span></span> <span data-ttu-id="af288-190">You have completed the steps to configure the account form to use custom business logic specified in your JavaScript code.</span><span class="sxs-lookup"><span data-stu-id="af288-190">You have completed the steps to configure the account form to use custom business logic specified in your JavaScript code.</span></span>

## <a name="test-your-javascript-code"></a><span data-ttu-id="af288-191">Test your JavaScript code</span><span class="sxs-lookup"><span data-stu-id="af288-191">Test your JavaScript code</span></span>

<span data-ttu-id="af288-192">Its recommended that you refresh your browser for the changes to take effect in your Customer Engagement instance.</span><span class="sxs-lookup"><span data-stu-id="af288-192">Its recommended that you refresh your browser for the changes to take effect in your Customer Engagement instance.</span></span> <span data-ttu-id="af288-193">To test custom business logic you configured in this walkthrough:</span><span class="sxs-lookup"><span data-stu-id="af288-193">To test custom business logic you configured in this walkthrough:</span></span>

1. <span data-ttu-id="af288-194">Sign in to your Customer Engagement instance.</span><span class="sxs-lookup"><span data-stu-id="af288-194">Sign in to your Customer Engagement instance.</span></span>
2. <span data-ttu-id="af288-195">Browse to **Accounts**, and try to open or create a new account.</span><span class="sxs-lookup"><span data-stu-id="af288-195">Browse to **Accounts**, and try to open or create a new account.</span></span> <span data-ttu-id="af288-196">In this case, we will open an existing account to load the account form.</span><span class="sxs-lookup"><span data-stu-id="af288-196">In this case, we will open an existing account to load the account form.</span></span> <span data-ttu-id="af288-197">You will see a notification conytaining your user name that will automatically disappear in 5 seconds.</span><span class="sxs-lookup"><span data-stu-id="af288-197">You will see a notification conytaining your user name that will automatically disappear in 5 seconds.</span></span>

      ![Form level notification](../media/clientapi_walkThrough-img11.png)

1. <span data-ttu-id="af288-199">Edit the account name to add "Contoso" in the name and move to the next field by pressing TAB.</span><span class="sxs-lookup"><span data-stu-id="af288-199">Edit the account name to add "Contoso" in the name and move to the next field by pressing TAB.</span></span> <span data-ttu-id="af288-200">This will fire the OnChange event, and will automatically update the **Phone**, **Website** and **Description** fields with the value specified in the code.</span><span class="sxs-lookup"><span data-stu-id="af288-200">This will fire the OnChange event, and will automatically update the **Phone**, **Website** and **Description** fields with the value specified in the code.</span></span>

      ![Values set automatically](../media/clientapi_walkThrough-img12.png)

1. <span data-ttu-id="af288-202">Finally clicking **Save** will fire the OnSave event, and will display the alert dialog with a message that you configured in your code.</span><span class="sxs-lookup"><span data-stu-id="af288-202">Finally clicking **Save** will fire the OnSave event, and will display the alert dialog with a message that you configured in your code.</span></span> <span data-ttu-id="af288-203">Click **OK** to close the alert.</span><span class="sxs-lookup"><span data-stu-id="af288-203">Click **OK** to close the alert.</span></span>

      ![Alert dialog](../media/clientapi_walkThrough-img13.png)

## <a name="complete-sample-code-used-in-the-walkthrough"></a><span data-ttu-id="af288-205">Complete sample code used in the walkthrough</span><span class="sxs-lookup"><span data-stu-id="af288-205">Complete sample code used in the walkthrough</span></span>

```JavaScript
// A namespace defined for the sample code
// As a best practice, you should always define 
// a unique namespace for your libraries
var Sdk = window.Sdk || {};
(function () {
    // Define some global variables
    var myUniqueId = "_myUniqueId"; // Define an ID for the notification
    var currentUserName = Xrm.Utility.getGlobalContext().userSettings.userName; // get current user name
    var message = currentUserName + ": Your JavaScript code in action!";

    // Code to run in the form OnLoad event
    this.formOnLoad = function (executionContext) {
        var formContext = executionContext.getFormContext();

        // display the form level notification as an INFO
        formContext.ui.setFormNotification(message, "INFO", myUniqueId);

        // Wait for 5 seconds before clearing the notification
        window.setTimeout(function () { formContext.ui.clearFormNotification(myUniqueId); }, 5000);
    }

    // Code to run in the attribute OnChange event 
    this.attributeOnChange = function (executionContext) {
        var formContext = executionContext.getFormContext();

        // Automatically set some field values if the account name contains "Contoso"
        var accountName = formContext.getAttribute("name").getValue();
        if (accountName.toLowerCase().search("contoso") != -1) {
            formContext.getAttribute("websiteurl").setValue("http://www.contoso.com");
            formContext.getAttribute("telephone1").setValue("425-555-0100");
            formContext.getAttribute("description").setValue("Website URL, Phone and Description set using custom script.");
        }
    }

    // Code to run in the form OnSave event 
    this.formOnSave = function () {
        // Display an alert dialog
        Xrm.Navigation.openAlertDialog({ text: "Record saved." });
    }
}).call(Sdk);
```
