---
title: 'Walkthrough: Registering and configuring SimpleSPA application with adal.js (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs'
description: This walkthrough describes the process of registering and configuring the simplest Single Page Application (SPA) to access data in Dynamics 365 for Customer Engagement apps using adal.js and Cross-origin Resource Sharing (CORS)
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0346a66d-147b-40e0-a1b6-0c30815043b4
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 651f55b7667e85911527ae4ea3e8a4e4860f3015
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386154"
---
# <a name="walkthrough-registering-and-configuring-simplespa-application-with-adaljs"></a><span data-ttu-id="06964-103">Walkthrough: Registering and configuring SimpleSPA application with adal.js</span><span class="sxs-lookup"><span data-stu-id="06964-103">Walkthrough: Registering and configuring SimpleSPA application with adal.js</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="06964-104">This walkthrough describes the process of registering and configuring the simplest Single Page Application (SPA) to access data in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement using adal.js and Cross-origin Resource Sharing (CORS).</span><span class="sxs-lookup"><span data-stu-id="06964-104">This walkthrough describes the process of registering and configuring the simplest Single Page Application (SPA) to access data in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement using adal.js and Cross-origin Resource Sharing (CORS).</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="06964-105">[Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement (online)](oauth-cross-origin-resource-sharing-connect-single-page-application.md).</span><span class="sxs-lookup"><span data-stu-id="06964-105">[Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement (online)](oauth-cross-origin-resource-sharing-connect-single-page-application.md).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="06964-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="06964-106">Prerequisites</span></span>  
  
- [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]  
  
- <span data-ttu-id="06964-107">You must have a [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] system user account with administrator role for the [!INCLUDE[pn_MS_Office_365](../includes/pn-ms-office-365.md)].</span><span class="sxs-lookup"><span data-stu-id="06964-107">You must have a [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] system user account with administrator role for the [!INCLUDE[pn_MS_Office_365](../includes/pn-ms-office-365.md)].</span></span>  
  
- <span data-ttu-id="06964-108">A [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] subscription for application registration.</span><span class="sxs-lookup"><span data-stu-id="06964-108">A [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] subscription for application registration.</span></span> <span data-ttu-id="06964-109">A trial account will also work.</span><span class="sxs-lookup"><span data-stu-id="06964-109">A trial account will also work.</span></span>  
  
- [!INCLUDE[pn_microsoft_visual_studio_2015](../includes/pn-microsoft-visual-studio-2015.md)]  
  
<a name="bkmk_goal"></a>   
## <a name="goal-of-this-walkthrough"></a><span data-ttu-id="06964-110">Goal of this walkthrough</span><span class="sxs-lookup"><span data-stu-id="06964-110">Goal of this walkthrough</span></span>  
 <span data-ttu-id="06964-111">When you complete this walkthrough you will be able to run a simple SPA application in Visual Studio that will provide the ability for a user to authenticate and retrieve data from [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="06964-111">When you complete this walkthrough you will be able to run a simple SPA application in Visual Studio that will provide the ability for a user to authenticate and retrieve data from [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="06964-112">This application consists of a single HTML page.</span><span class="sxs-lookup"><span data-stu-id="06964-112">This application consists of a single HTML page.</span></span>  
  
 <span data-ttu-id="06964-113">When you debug the application initially there will only be a **Login** button.</span><span class="sxs-lookup"><span data-stu-id="06964-113">When you debug the application initially there will only be a **Login** button.</span></span>  
  
 <span data-ttu-id="06964-114">Click **Login** and you will be re-directed to a sign-in page to enter your credentials.</span><span class="sxs-lookup"><span data-stu-id="06964-114">Click **Login** and you will be re-directed to a sign-in page to enter your credentials.</span></span>  
  
 <span data-ttu-id="06964-115">After you enter your credentials you will be directed back to the HTML page where you will find the **Login** button is hidden and a **Logout** button and a **Get Accounts** button are visible.</span><span class="sxs-lookup"><span data-stu-id="06964-115">After you enter your credentials you will be directed back to the HTML page where you will find the **Login** button is hidden and a **Logout** button and a **Get Accounts** button are visible.</span></span> <span data-ttu-id="06964-116">You will also see a greeting using information from your user account.</span><span class="sxs-lookup"><span data-stu-id="06964-116">You will also see a greeting using information from your user account.</span></span>  
  
 <span data-ttu-id="06964-117">Click the **Get Accounts** button to retrieve 10 account records from your [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization.</span><span class="sxs-lookup"><span data-stu-id="06964-117">Click the **Get Accounts** button to retrieve 10 account records from your [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization.</span></span> <span data-ttu-id="06964-118">The **Get Accounts** button is disabled as shown in the following screenshot:</span><span class="sxs-lookup"><span data-stu-id="06964-118">The **Get Accounts** button is disabled as shown in the following screenshot:</span></span>  
  
 <span data-ttu-id="06964-119">![The SimpleSPA page](media/simple-spa.png "The SimpleSPA page")</span><span class="sxs-lookup"><span data-stu-id="06964-119">![The SimpleSPA page](media/simple-spa.png "The SimpleSPA page")</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="06964-120">The initial load of data from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] may be slow as the operations to support authentication take place, but subsequent operations are much faster.</span><span class="sxs-lookup"><span data-stu-id="06964-120">The initial load of data from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] may be slow as the operations to support authentication take place, but subsequent operations are much faster.</span></span>  
  
 <span data-ttu-id="06964-121">Finally, you can click the **Logout** button to logout.</span><span class="sxs-lookup"><span data-stu-id="06964-121">Finally, you can click the **Logout** button to logout.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="06964-122">This SPA application is not intended to represent a pattern for developing robust SPA applications.</span><span class="sxs-lookup"><span data-stu-id="06964-122">This SPA application is not intended to represent a pattern for developing robust SPA applications.</span></span> <span data-ttu-id="06964-123">It is simplified to focus on the process of registering and configuring the application.</span><span class="sxs-lookup"><span data-stu-id="06964-123">It is simplified to focus on the process of registering and configuring the application.</span></span>  
  
### <a name="create-a-web-application-project"></a><span data-ttu-id="06964-124">Create a web application project</span><span class="sxs-lookup"><span data-stu-id="06964-124">Create a web application project</span></span>  
  
1. <span data-ttu-id="06964-125">Using [!INCLUDE[pn_microsoft_visual_studio_2015](../includes/pn-microsoft-visual-studio-2015.md)], create a new **ASP.NET Web Application** project and use the **Empty** template.</span><span class="sxs-lookup"><span data-stu-id="06964-125">Using [!INCLUDE[pn_microsoft_visual_studio_2015](../includes/pn-microsoft-visual-studio-2015.md)], create a new **ASP.NET Web Application** project and use the **Empty** template.</span></span> <span data-ttu-id="06964-126">You can name the project whatever you like.</span><span class="sxs-lookup"><span data-stu-id="06964-126">You can name the project whatever you like.</span></span>  
  
    <span data-ttu-id="06964-127">You should be able to use earlier versions of [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] as well, but these steps will describe using [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)].</span><span class="sxs-lookup"><span data-stu-id="06964-127">You should be able to use earlier versions of [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] as well, but these steps will describe using [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)].</span></span>  
  
2. <span data-ttu-id="06964-128">Add a new HTML page named SimpleSPA.html to the project and paste in the following code:</span><span class="sxs-lookup"><span data-stu-id="06964-128">Add a new HTML page named SimpleSPA.html to the project and paste in the following code:</span></span>  
  
   ```html  
   <!DOCTYPE html>  
   <html>  
   <head>  
    <title>Simple SPA</title>  
    <meta charset="utf-8" />  
    <script src="https://secure.aadcdn.microsoftonline-p.com/lib/1.0.0/js/adal.min.js"></script>  
    <script type="text/javascript">  
     "use strict";  
  
     //Set these variables to match your environment  
     var organizationURI = "https:// [organization name].crm.dynamics.com"; //The URL to connect to CRM (online)  
     var tenant = "[xxx.onmicrosoft.com]"; //The name of the Azure AD organization you use  
     var clientId = "[client id]"; //The ClientId you got when you registered the application  
     var pageUrl = "http://localhost: [PORT #]/SimpleSPA.html"; //The URL of this page in your development environment when debugging.  
  
     var user, authContext, message, errorMessage, loginButton, logoutButton, getAccountsButton, accountsTable, accountsTableBody;  
  
     //Configuration data for AuthenticationContext  
     var endpoints = {  
      orgUri: organizationURI  
     };  
  
     window.config = {  
      tenant: tenant,  
      clientId: clientId,  
      postLogoutRedirectUri: pageUrl,  
      endpoints: endpoints,  
      cacheLocation: 'localStorage', // enable this for IE, as sessionStorage does not work for localhost.  
     };  
  
     document.onreadystatechange = function () {  
      if (document.readyState == "complete") {  
  
       //Set DOM elements referenced by scripts  
       message = document.getElementById("message");  
       errorMessage = document.getElementById("errorMessage");  
       loginButton = document.getElementById("login");  
       logoutButton = document.getElementById("logout");  
       getAccountsButton = document.getElementById("getAccounts");  
       accountsTable = document.getElementById("accountsTable");  
       accountsTableBody = document.getElementById("accountsTableBody");  
  
       //Event handlers on DOM elements  
       loginButton.addEventListener("click", login);  
       logoutButton.addEventListener("click", logout);  
       getAccountsButton.addEventListener("click", getAccounts);  
  
       //call authentication function  
       authenticate();  
  
       if (user) {  
        loginButton.style.display = "none";  
        logoutButton.style.display = "block";  
        getAccountsButton.style.display = "block";  
  
        var helloMessage = document.createElement("p");  
        helloMessage.textContent = "Hello " + user.profile.name;  
        message.appendChild(helloMessage)  
  
       }  
       else {  
        loginButton.style.display = "block";  
        logoutButton.style.display = "none";  
        getAccountsButton.style.display = "none";  
       }  
  
      }  
     }  
  
     // Function that manages authentication  
     function authenticate() {  
      //OAuth context  
      authContext = new AuthenticationContext(config);  
  
      // Check For & Handle Redirect From AAD After Login  
      var isCallback = authContext.isCallback(window.location.hash);  
      if (isCallback) {  
       authContext.handleWindowCallback();  
      }  
      var loginError = authContext.getLoginError();  
  
      if (isCallback && !loginError) {  
       window.location = authContext._getItem(authContext.CONSTANTS.STORAGE.LOGIN_REQUEST);  
      }  
      else {  
       errorMessage.textContent = loginError;  
      }  
      user = authContext.getCachedUser();  
  
     }  
  
     //function that logs in the user  
     function login() {  
      authContext.login();  
     }  
     //function that logs out the user  
     function logout() {  
      authContext.logOut();  
      accountsTable.style.display = "none";  
      accountsTableBody.innerHTML = "";  
     }  
  
   //function that initiates retrieval of accounts  
     function getAccounts() {  
  
      getAccountsButton.disabled = true;  
      var retrievingAccountsMessage = document.createElement("p");  
      retrievingAccountsMessage.textContent = "Retrieving 10 accounts from " + organizationURI + "/api/data/v8.0/accounts";  
      message.appendChild(retrievingAccountsMessage)  
  
      // Function to perform operation is passed as a parameter to the aquireToken method  
      authContext.acquireToken(organizationURI, retrieveAccounts)  
  
     }  
  
   //Function that actually retrieves the accounts  
     function retrieveAccounts(error, token) {  
      // Handle ADAL Errors.  
      if (error || !token) {  
       errorMessage.textContent = 'ADAL error occurred: ' + error;  
       return;  
      }  
  
      var req = new XMLHttpRequest()  
      req.open("GET", encodeURI(organizationURI + "/api/data/v8.0/accounts?$select=name,address1_city&$top=10"), true);  
      //Set Bearer token  
      req.setRequestHeader("Authorization", "Bearer " + token);  
      req.setRequestHeader("Accept", "application/json");  
      req.setRequestHeader("Content-Type", "application/json; charset=utf-8");  
      req.setRequestHeader("OData-MaxVersion", "4.0");  
      req.setRequestHeader("OData-Version", "4.0");  
      req.onreadystatechange = function () {  
       if (this.readyState == 4 /* complete */) {  
        req.onreadystatechange = null;  
        if (this.status == 200) {  
         var accounts = JSON.parse(this.response).value;  
         renderAccounts(accounts);  
        }  
        else {  
         var error = JSON.parse(this.response).error;  
         console.log(error.message);  
         errorMessage.textContent = error.message;  
        }  
       }  
      };  
      req.send();  
     }  
     //Function that writes account data to the accountsTable  
     function renderAccounts(accounts) {  
      accounts.forEach(function (account) {  
       var name = account.name;  
       var city = account.address1_city;  
       var nameCell = document.createElement("td");  
       nameCell.textContent = name;  
       var cityCell = document.createElement("td");  
       cityCell.textContent = city;  
       var row = document.createElement("tr");  
       row.appendChild(nameCell);  
       row.appendChild(cityCell);  
       accountsTableBody.appendChild(row);  
      });  
      accountsTable.style.display = "block";  
     }  
  
    </script>  
    <style>  
     body {  
      font-family: 'Segoe UI';  
     }  
  
     table {  
      border-collapse: collapse;  
     }  
  
     td, th {  
      border: 1px solid black;  
     }  
  
     #errorMessage {  
      color: red;  
     }  
  
     #message {  
      color: green;  
     }  
    </style>  
   </head>  
   <body>  
    <button id="login">Login</button>  
    <button id="logout" style="display:none;">Logout</button>  
    <button id="getAccounts" style="display:none;">Get Accounts</button>  
    <div id="errorMessage"></div>  
    <div id="message"></div>  
    <table id="accountsTable" style="display:none;">  
     <thead><tr><th>Name</th><th>City</th></tr></thead>  
     <tbody id="accountsTableBody"></tbody>  
    </table>  
   </body>  
   </html>  
  
   ```  
  
3. <span data-ttu-id="06964-129">Set this page as the start page for the project</span><span class="sxs-lookup"><span data-stu-id="06964-129">Set this page as the start page for the project</span></span>  
  
4. <span data-ttu-id="06964-130">In the properties of the project, select **Web** and under **Servers** note the **Project URL**.</span><span class="sxs-lookup"><span data-stu-id="06964-130">In the properties of the project, select **Web** and under **Servers** note the **Project URL**.</span></span> <span data-ttu-id="06964-131">It should be something like `http://localhost:46575/`.</span><span class="sxs-lookup"><span data-stu-id="06964-131">It should be something like `http://localhost:46575/`.</span></span> <span data-ttu-id="06964-132">Note the port number that is generated.</span><span class="sxs-lookup"><span data-stu-id="06964-132">Note the port number that is generated.</span></span> <span data-ttu-id="06964-133">You will need this in the next step.</span><span class="sxs-lookup"><span data-stu-id="06964-133">You will need this in the next step.</span></span>  
  
5. <span data-ttu-id="06964-134">Within the SimpleSPA.html page, locate the following configuration variables and set them accordingly.</span><span class="sxs-lookup"><span data-stu-id="06964-134">Within the SimpleSPA.html page, locate the following configuration variables and set them accordingly.</span></span> <span data-ttu-id="06964-135">You will be able to set the `clientId` after you complete the next part of the walkthrough.</span><span class="sxs-lookup"><span data-stu-id="06964-135">You will be able to set the `clientId` after you complete the next part of the walkthrough.</span></span>  
  
   ```javascript  
   //Set these variables to match your environment  
   var organizationURI = "https://[organization name].crm.dynamics.com"; //The URL to connect to CRM (online)  
   var tenant = "[xxx.onmicrosoft.com]"; //The name of the Azure AD organization you use  
   var clientId = "[client id]"; //The ClientId you got when you registered the application  
   var pageUrl = "http://localhost:[PORT #]/SimpleSPA.html"; //The URL of this page in your development environment when debugging.  
  
   ```  
  
### <a name="register-the-application"></a><span data-ttu-id="06964-136">Register the application</span><span class="sxs-lookup"><span data-stu-id="06964-136">Register the application</span></span>  
  
1. <span data-ttu-id="06964-137">[Sign in](http://manage.windowsazure.com) to the [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] management portal by using an account with administrator permission.</span><span class="sxs-lookup"><span data-stu-id="06964-137">[Sign in](http://manage.windowsazure.com) to the [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] management portal by using an account with administrator permission.</span></span> <span data-ttu-id="06964-138">You must use an account in the same [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] subscription (tenant) as you intend to register the app with.</span><span class="sxs-lookup"><span data-stu-id="06964-138">You must use an account in the same [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] subscription (tenant) as you intend to register the app with.</span></span> <span data-ttu-id="06964-139">You can also access the [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] portal through the [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] admin center by expanding the **ADMIN** item in the left navigation pane and selecting **Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="06964-139">You can also access the [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] portal through the [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] admin center by expanding the **ADMIN** item in the left navigation pane and selecting **Azure AD**.</span></span>  
  
    <span data-ttu-id="06964-140">If you don’t have an [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] tenant (account) or you do have one but your [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] subscription with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] is not available in your [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] subscription, following the instructions in the topic [Set up Azure Active Directory access for your Developer Site](https://msdn.microsoft.com/office/office365/HowTo/setup-development-environment) to associate the two accounts.</span><span class="sxs-lookup"><span data-stu-id="06964-140">If you don’t have an [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] tenant (account) or you do have one but your [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] subscription with [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] is not available in your [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] subscription, following the instructions in the topic [Set up Azure Active Directory access for your Developer Site](https://msdn.microsoft.com/office/office365/HowTo/setup-development-environment) to associate the two accounts.</span></span>  
  
    <span data-ttu-id="06964-141">If you don’t have an account, you can sign up for one by using a credit card.</span><span class="sxs-lookup"><span data-stu-id="06964-141">If you don’t have an account, you can sign up for one by using a credit card.</span></span> <span data-ttu-id="06964-142">However, the account is free for application registration and your credit card won’t be charged if you only follow the procedures called out in this topic to register one or more apps.</span><span class="sxs-lookup"><span data-stu-id="06964-142">However, the account is free for application registration and your credit card won’t be charged if you only follow the procedures called out in this topic to register one or more apps.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="06964-143">[Active Directory Pricing Details](http://azure.microsoft.com/pricing/details/active-directory/)</span><span class="sxs-lookup"><span data-stu-id="06964-143">[Active Directory Pricing Details](http://azure.microsoft.com/pricing/details/active-directory/)</span></span>  
  
2. <span data-ttu-id="06964-144">Click **Active Directory** in the left column of the page.</span><span class="sxs-lookup"><span data-stu-id="06964-144">Click **Active Directory** in the left column of the page.</span></span> <span data-ttu-id="06964-145">You may need to scroll the left column to see the **Active Directory** icon and label.</span><span class="sxs-lookup"><span data-stu-id="06964-145">You may need to scroll the left column to see the **Active Directory** icon and label.</span></span>  
  
3. <span data-ttu-id="06964-146">Click the desired tenant directory in the directory list.</span><span class="sxs-lookup"><span data-stu-id="06964-146">Click the desired tenant directory in the directory list.</span></span>  
  
   <span data-ttu-id="06964-147">![List of available Active Directory entries](media/azure-active-directory.PNG "List of available Active Directory entries")</span><span class="sxs-lookup"><span data-stu-id="06964-147">![List of available Active Directory entries](media/azure-active-directory.PNG "List of available Active Directory entries")</span></span>  
  
    <span data-ttu-id="06964-148">If your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] tenant directory isn’t shown in the directory list, click **Add**, and then select **Use existing directory** in the dialog box.</span><span class="sxs-lookup"><span data-stu-id="06964-148">If your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] tenant directory isn’t shown in the directory list, click **Add**, and then select **Use existing directory** in the dialog box.</span></span> <span data-ttu-id="06964-149">Follow the prompts and instructions provided, and then go back to step 1.</span><span class="sxs-lookup"><span data-stu-id="06964-149">Follow the prompts and instructions provided, and then go back to step 1.</span></span>  
  
4. <span data-ttu-id="06964-150">With the target directory selected, click **Applications** (near the top of the page), and then click **Add**.</span><span class="sxs-lookup"><span data-stu-id="06964-150">With the target directory selected, click **Applications** (near the top of the page), and then click **Add**.</span></span>  
  
5. <span data-ttu-id="06964-151">In the **What do you want to do?** dialog box, click **Add an application my organization is developing**.</span><span class="sxs-lookup"><span data-stu-id="06964-151">In the **What do you want to do?** dialog box, click **Add an application my organization is developing**.</span></span>  
  
6. <span data-ttu-id="06964-152">When prompted, enter a name for your application, for example ‘SimpleSPA’, pick the type: **Web Application and/or Web API**, and then click the right arrow to continue.</span><span class="sxs-lookup"><span data-stu-id="06964-152">When prompted, enter a name for your application, for example ‘SimpleSPA’, pick the type: **Web Application and/or Web API**, and then click the right arrow to continue.</span></span> <span data-ttu-id="06964-153">Click a question mark **?**</span><span class="sxs-lookup"><span data-stu-id="06964-153">Click a question mark **?**</span></span> <span data-ttu-id="06964-154">for more information on the appropriate values for each input field.</span><span class="sxs-lookup"><span data-stu-id="06964-154">for more information on the appropriate values for each input field.</span></span>  
  
7. <span data-ttu-id="06964-155">Enter the following information :</span><span class="sxs-lookup"><span data-stu-id="06964-155">Enter the following information :</span></span>  
  
   <span data-ttu-id="06964-156">**Sign-on URL**</span><span class="sxs-lookup"><span data-stu-id="06964-156">**Sign-on URL**</span></span>  
    <span data-ttu-id="06964-157">This is the URL which the user should be redirected to after they sign in.</span><span class="sxs-lookup"><span data-stu-id="06964-157">This is the URL which the user should be redirected to after they sign in.</span></span> <span data-ttu-id="06964-158">For debugging purposes in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] it should be  `http://localhost:####/SimpleSPA.html` where #### represents the port number you got from step 4 of the **Create a web application project** procedure.</span><span class="sxs-lookup"><span data-stu-id="06964-158">For debugging purposes in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] it should be  `http://localhost:####/SimpleSPA.html` where #### represents the port number you got from step 4 of the **Create a web application project** procedure.</span></span>  
  
   <span data-ttu-id="06964-159">**APP ID URI**</span><span class="sxs-lookup"><span data-stu-id="06964-159">**APP ID URI**</span></span>  
    <span data-ttu-id="06964-160">This must be a unique identifier for the application.</span><span class="sxs-lookup"><span data-stu-id="06964-160">This must be a unique identifier for the application.</span></span> <span data-ttu-id="06964-161">Use `https://XXXX.onmicrosoft.com/SimpleSPA` where XXXX is the Active Directory tenant.</span><span class="sxs-lookup"><span data-stu-id="06964-161">Use `https://XXXX.onmicrosoft.com/SimpleSPA` where XXXX is the Active Directory tenant.</span></span>  
  
8. <span data-ttu-id="06964-162">With the tab of the newly registered app selected, click **Configure**, locate the **Client id** and copy it.</span><span class="sxs-lookup"><span data-stu-id="06964-162">With the tab of the newly registered app selected, click **Configure**, locate the **Client id** and copy it.</span></span>  
  
    <span data-ttu-id="06964-163">Set the `clientId` variable in the SimpleSPA.html page to this value.</span><span class="sxs-lookup"><span data-stu-id="06964-163">Set the `clientId` variable in the SimpleSPA.html page to this value.</span></span> <span data-ttu-id="06964-164">Refer to step 5 of the **Create a web application project** procedure.</span><span class="sxs-lookup"><span data-stu-id="06964-164">Refer to step 5 of the **Create a web application project** procedure.</span></span>  
  
9. <span data-ttu-id="06964-165">Scroll to the bottom of the page and click **Add application**.</span><span class="sxs-lookup"><span data-stu-id="06964-165">Scroll to the bottom of the page and click **Add application**.</span></span> <span data-ttu-id="06964-166">In the dialog box select **Dynamics 365 for Customer Engagement Online** and close the dialog box.</span><span class="sxs-lookup"><span data-stu-id="06964-166">In the dialog box select **Dynamics 365 for Customer Engagement Online** and close the dialog box.</span></span>  
  
10. <span data-ttu-id="06964-167">Under permissions to other applications, you will find a row for **Dynamics 365 for Customer Engagement Online** and **Delegated Permissions: 0**.</span><span class="sxs-lookup"><span data-stu-id="06964-167">Under permissions to other applications, you will find a row for **Dynamics 365 for Customer Engagement Online** and **Delegated Permissions: 0**.</span></span> <span data-ttu-id="06964-168">Select this and add **Access Dynamics 365 for Customer Engagement (online) as organization users**.</span><span class="sxs-lookup"><span data-stu-id="06964-168">Select this and add **Access Dynamics 365 for Customer Engagement (online) as organization users**.</span></span>  
  
11. <span data-ttu-id="06964-169">Save the application registration</span><span class="sxs-lookup"><span data-stu-id="06964-169">Save the application registration</span></span>  
  
12. <span data-ttu-id="06964-170">At the bottom, select **Manage Manifest** and choose **Download Manifest**.</span><span class="sxs-lookup"><span data-stu-id="06964-170">At the bottom, select **Manage Manifest** and choose **Download Manifest**.</span></span>  
  
13. <span data-ttu-id="06964-171">Open the JSON file you downloaded and locate the line: `"oauth2AllowImplicitFlow": false,` and change `false` to `true` and save the file.</span><span class="sxs-lookup"><span data-stu-id="06964-171">Open the JSON file you downloaded and locate the line: `"oauth2AllowImplicitFlow": false,` and change `false` to `true` and save the file.</span></span>  
  
14. <span data-ttu-id="06964-172">Go back to **Manage Manifest** again.</span><span class="sxs-lookup"><span data-stu-id="06964-172">Go back to **Manage Manifest** again.</span></span> <span data-ttu-id="06964-173">Choose **Upload Manifest** and upload the JSON file you just saved.</span><span class="sxs-lookup"><span data-stu-id="06964-173">Choose **Upload Manifest** and upload the JSON file you just saved.</span></span>  
  
### <a name="debugging-the-application"></a><span data-ttu-id="06964-174">Debugging the application</span><span class="sxs-lookup"><span data-stu-id="06964-174">Debugging the application</span></span>  
  
1. <span data-ttu-id="06964-175">Set the browser to use [!INCLUDE[pn_microsoft_edge](../includes/pn-microsoft-edge.md)], [!INCLUDE[tn_Google_Chrome](../includes/tn-google-chrome.md)], or [!INCLUDE[tn_Mozilla_Firefox](../includes/tn-mozilla-firefox.md)].</span><span class="sxs-lookup"><span data-stu-id="06964-175">Set the browser to use [!INCLUDE[pn_microsoft_edge](../includes/pn-microsoft-edge.md)], [!INCLUDE[tn_Google_Chrome](../includes/tn-google-chrome.md)], or [!INCLUDE[tn_Mozilla_Firefox](../includes/tn-mozilla-firefox.md)].</span></span>  
  
   > [!NOTE]
   > [!INCLUDE[pn_Internet_Explorer](../includes/pn-internet-explorer.md)] <span data-ttu-id="06964-176">will not work for debugging in this situation.</span><span class="sxs-lookup"><span data-stu-id="06964-176">will not work for debugging in this situation.</span></span>  
  
2. <span data-ttu-id="06964-177">Press F5 to start debugging.</span><span class="sxs-lookup"><span data-stu-id="06964-177">Press F5 to start debugging.</span></span> <span data-ttu-id="06964-178">You should expect the behavior described in [Goal of this walkthrough](walkthrough-registering-configuring-simplespa-application-adal-js.md#bkmk_goal).</span><span class="sxs-lookup"><span data-stu-id="06964-178">You should expect the behavior described in [Goal of this walkthrough](walkthrough-registering-configuring-simplespa-application-adal-js.md#bkmk_goal).</span></span>  
  
    <span data-ttu-id="06964-179">If you don’t get the results you expect, double-check the values you set when registering the application and configuring the SimpleSPA.html code.</span><span class="sxs-lookup"><span data-stu-id="06964-179">If you don’t get the results you expect, double-check the values you set when registering the application and configuring the SimpleSPA.html code.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="06964-180">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="06964-180">See also</span></span>  
 [<span data-ttu-id="06964-181">Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement (online)</span><span class="sxs-lookup"><span data-stu-id="06964-181">Use OAuth with Cross-Origin Resource Sharing  to connect a Single Page Application  to Dynamics 365 for Customer Engagement (online)</span></span>](oauth-cross-origin-resource-sharing-connect-single-page-application.md)
