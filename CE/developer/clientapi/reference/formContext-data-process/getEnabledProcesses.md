---
title: getEnabledProcesses (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 52f79803-2ce0-4ca7-8200-aec544545d62
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b768309c73355fa3ab12447531072da90d74e1a2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386294"
---
# <a name="getenabledprocesses-client-api-reference"></a><span data-ttu-id="fddef-102">getEnabledProcesses (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="fddef-102">getEnabledProcesses (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getEnabledProcesses-description.md](./includes/getEnabledProcesses-description.md)]

## <a name="syntax"></a><span data-ttu-id="fddef-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="fddef-103">Syntax</span></span>

`formContext.data.process.getEnabledProcesses(callbackFunction(enabledProcesses));`

## <a name="parameter"></a><span data-ttu-id="fddef-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="fddef-104">Parameter</span></span>

|<span data-ttu-id="fddef-105">Tên</span><span class="sxs-lookup"><span data-stu-id="fddef-105">Name</span></span>|<span data-ttu-id="fddef-106">Loại</span><span class="sxs-lookup"><span data-stu-id="fddef-106">Type</span></span>|<span data-ttu-id="fddef-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="fddef-107">Required</span></span>|<span data-ttu-id="fddef-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="fddef-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="fddef-109">callbackFunction</span><span class="sxs-lookup"><span data-stu-id="fddef-109">callbackFunction</span></span>|<span data-ttu-id="fddef-110">Hàm</span><span class="sxs-lookup"><span data-stu-id="fddef-110">Function</span></span>|<span data-ttu-id="fddef-111">Có</span><span class="sxs-lookup"><span data-stu-id="fddef-111">Yes</span></span>|<span data-ttu-id="fddef-112">The callback function must accept a parameter that contains an object with dictionary properties where the name of the property is the Id of the business process flow and the value of the property is the name of the business process flow.</span><span class="sxs-lookup"><span data-stu-id="fddef-112">The callback function must accept a parameter that contains an object with dictionary properties where the name of the property is the Id of the business process flow and the value of the property is the name of the business process flow.</span></span><br/><br/><span data-ttu-id="fddef-113">The enabled processes are filtered according to the user’s privileges.</span><span class="sxs-lookup"><span data-stu-id="fddef-113">The enabled processes are filtered according to the user’s privileges.</span></span> <span data-ttu-id="fddef-114">The list of enabled processes is the same ones a user can see in the UI if they want to change the process manually.</span><span class="sxs-lookup"><span data-stu-id="fddef-114">The list of enabled processes is the same ones a user can see in the UI if they want to change the process manually.</span></span>|

## <a name="example"></a><span data-ttu-id="fddef-115">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="fddef-115">Example</span></span>

<span data-ttu-id="fddef-116">The **Sdk.formOnLoad** function in the example uses the **formContext.data.process.getEnabledProcesses** method to asynchronously retrieve information about business process flows that are enabled for the entity.</span><span class="sxs-lookup"><span data-stu-id="fddef-116">The **Sdk.formOnLoad** function in the example uses the **formContext.data.process.getEnabledProcesses** method to asynchronously retrieve information about business process flows that are enabled for the entity.</span></span> <span data-ttu-id="fddef-117">The sample passes an anonymous function as the first parameter.</span><span class="sxs-lookup"><span data-stu-id="fddef-117">The sample passes an anonymous function as the first parameter.</span></span> <span data-ttu-id="fddef-118">This function is executed asynchronously when the data is returned and the data is passed as the parameter to the anonymous function.</span><span class="sxs-lookup"><span data-stu-id="fddef-118">This function is executed asynchronously when the data is returned and the data is passed as the parameter to the anonymous function.</span></span>

<span data-ttu-id="fddef-119">The information about enabled business process flow is provided as a dictionary object where the Id of the process is the name of the property and the name of the business process flow is the value of the property.</span><span class="sxs-lookup"><span data-stu-id="fddef-119">The information about enabled business process flow is provided as a dictionary object where the Id of the process is the name of the property and the name of the business process flow is the value of the property.</span></span> <span data-ttu-id="fddef-120">The sample code processes this information and sets the values in a global **Sdk.enabledProcesses** array to be accessed by logic that executes later.</span><span class="sxs-lookup"><span data-stu-id="fddef-120">The sample code processes this information and sets the values in a global **Sdk.enabledProcesses** array to be accessed by logic that executes later.</span></span> <span data-ttu-id="fddef-121">The sample also loops through the values in the **Sdk.enabledProcesses** array, and uses the **Sdk.writeToConsole** function to write information about the retrieved business process flows to the console.</span><span class="sxs-lookup"><span data-stu-id="fddef-121">The sample also loops through the values in the **Sdk.enabledProcesses** array, and uses the **Sdk.writeToConsole** function to write information about the retrieved business process flows to the console.</span></span>

>[!NOTE]
><span data-ttu-id="fddef-122">The **Sdk.formOnLoad** function in the sample JavaScript library must be set as the **OnLoad** event handler for a form, and the **Pass execution context as the first parameter** check box must be selected in the **Handler Properties** dialog.</span><span class="sxs-lookup"><span data-stu-id="fddef-122">The **Sdk.formOnLoad** function in the sample JavaScript library must be set as the **OnLoad** event handler for a form, and the **Pass execution context as the first parameter** check box must be selected in the **Handler Properties** dialog.</span></span><br/><span data-ttu-id="fddef-123">Also, this sample just illustrates the use of some of the methods in the **formContext.data.process** API.</span><span class="sxs-lookup"><span data-stu-id="fddef-123">Also, this sample just illustrates the use of some of the methods in the **formContext.data.process** API.</span></span> <span data-ttu-id="fddef-124">It doesn’t represent using this API to meet a business requirement; it’s only intended to demonstrate how the key property values can be accessed in code.</span><span class="sxs-lookup"><span data-stu-id="fddef-124">It doesn’t represent using this API to meet a business requirement; it’s only intended to demonstrate how the key property values can be accessed in code.</span></span>

```JavaScript
//A namespace defined for SDK sample code
//You should define a unique namespace for your libraries
var Sdk = window.Sdk || {};
(function () {
    //A global variable to store information about enabled business processes after they are retrieved asynchronously
    this.enabledProcesses = [];

    // A function to log messages while debugging only
    this.writeToConsole = function (message) {
        if (typeof console != 'undefined')
        { console.log(message); }
    };

    // Code to run in the OnLoad event 
    this.formOnLoad = function (executionContext) {
        // Retrieve the formContext
        var formContext = executionContext.getFormContext();

        // Retrieve Enabled processes
        formContext.data.process.getEnabledProcesses(function (processes) {
            //Move processes to the global Sdk.enabledProcesses array;
            for (var processId in processes) {
                Sdk.enabledProcesses.push({ id: processId, name: processes[processId] })
            }
            Sdk.writeToConsole("Enabled business processes flows retrieved and added to Sdk.enabledProcesses array.");

            //Write the values of the Sdk.enabledProcesses array to the console
            if (Sdk.enabledProcesses.length < 0) {
                Sdk.writeToConsole("There are no enabled business process flows for this entity.");
            }
            else {
                Sdk.writeToConsole("These are the enabled business process flows for this entity:");
                for (var i = 0; i < Sdk.enabledProcesses.length; i++) {
                    var enabledProcess = Sdk.enabledProcesses[i];
                    Sdk.writeToConsole("id: " + enabledProcess.id + " name: " + enabledProcess.name)
                }
            }

            //Any code that depends on the Sdk.enabledProcesses array needs to be initiated here

        });
    };

}).call(Sdk);
```

<span data-ttu-id="fddef-125">When you run this sample with the browser developer tools open, the following is an example of the output written to the console for an entity with multiple business process flows enabled.</span><span class="sxs-lookup"><span data-stu-id="fddef-125">When you run this sample with the browser developer tools open, the following is an example of the output written to the console for an entity with multiple business process flows enabled.</span></span>

```
Enabled business processes flows retrieved and added to Sdk.enabledProcesses array.
These are the enabled business process flows for this entity:
id: 7994be68-899e-4a40-8d18-f5c3b6940188 name: Sample Lead Process
id: 919e14d1-6489-4852-abd0-a63a6ecaac5d name: Lead to Opportunity Sales Process
```

### <a name="related-topics"></a><span data-ttu-id="fddef-126">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="fddef-126">Related topics</span></span>

[<span data-ttu-id="fddef-127">setActiveProcessInstance</span><span class="sxs-lookup"><span data-stu-id="fddef-127">setActiveProcessInstance</span></span>](setActiveProcessInstance.md)

[<span data-ttu-id="fddef-128">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="fddef-128">formContext.data.process</span></span>](../formContext-data-process.md)
 


