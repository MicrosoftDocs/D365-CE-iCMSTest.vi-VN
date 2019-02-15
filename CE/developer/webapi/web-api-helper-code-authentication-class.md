---
title: 'Web API Helper code: Authentication class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: Authentication class assists in establishing a validated connection to a Dynamics 365 for Customer Engagement Web service
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a7b5931c-3142-4616-a331-1e07b4d8845d
caps.latest.revision: 11
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fb43203dfc60b7aa2e20214d138925aa94cedf71
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387239"
---
# <a name="web-api-helper-code-authentication-class"></a><span data-ttu-id="6b75c-103">Web API Helper code: Authentication class</span><span class="sxs-lookup"><span data-stu-id="6b75c-103">Web API Helper code: Authentication class</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6b75c-104">Use the `Authentication` class to assist in establishing a validated connection to a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Web service.</span><span class="sxs-lookup"><span data-stu-id="6b75c-104">Use the `Authentication` class to assist in establishing a validated connection to a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Web service.</span></span> <span data-ttu-id="6b75c-105">This class supports two authentication protocols: [Windows Authentication](https://docs.microsoft.com/en-us/windows-server/security/windows-authentication/windows-authentication-overview) for Dynamics 365 for Customer Engagement apps on-premises or [OAuth 2.0](http://oauth.net/2/) for Dynamics 365 for Customer Engagement apps (online) or internet-facing deployments (IFDs).</span><span class="sxs-lookup"><span data-stu-id="6b75c-105">This class supports two authentication protocols: [Windows Authentication](https://docs.microsoft.com/en-us/windows-server/security/windows-authentication/windows-authentication-overview) for Dynamics 365 for Customer Engagement apps on-premises or [OAuth 2.0](http://oauth.net/2/) for Dynamics 365 for Customer Engagement apps (online) or internet-facing deployments (IFDs).</span></span> <span data-ttu-id="6b75c-106">This class relies upon the Microsoft Azure Active Directory Authentication Library ([ADAL](https://docs.microsoft.com/en-us/dotnet/api/microsoft.identitymodel.clients.activedirectory?view=azure-dotnet)) to handle the OAuth protocol.</span><span class="sxs-lookup"><span data-stu-id="6b75c-106">This class relies upon the Microsoft Azure Active Directory Authentication Library ([ADAL](https://docs.microsoft.com/en-us/dotnet/api/microsoft.identitymodel.clients.activedirectory?view=azure-dotnet)) to handle the OAuth protocol.</span></span>  
  
 <span data-ttu-id="6b75c-107">The `Authentication` class is located in the file Authentication.cs in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode/).</span><span class="sxs-lookup"><span data-stu-id="6b75c-107">The `Authentication` class is located in the file Authentication.cs in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode/).</span></span> <span data-ttu-id="6b75c-108">It is designed to work in conjunction with the `Configuration` helper class  hierarchy to enable you to establish a secure connection to your Dynamics 365 for Customer Engagement service through an object of type System.Net.Http.[HttpMessageHandler](https://msdn.microsoft.com/library/hh138091\(v=vs.110\).aspx).</span><span class="sxs-lookup"><span data-stu-id="6b75c-108">It is designed to work in conjunction with the `Configuration` helper class  hierarchy to enable you to establish a secure connection to your Dynamics 365 for Customer Engagement service through an object of type System.Net.Http.[HttpMessageHandler](https://msdn.microsoft.com/library/hh138091\(v=vs.110\).aspx).</span></span> <span data-ttu-id="6b75c-109">For more information, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span><span class="sxs-lookup"><span data-stu-id="6b75c-109">For more information, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span></span>  
  
## <a name="authentication-processing"></a><span data-ttu-id="6b75c-110">Authentication processing</span><span class="sxs-lookup"><span data-stu-id="6b75c-110">Authentication processing</span></span>  
 <span data-ttu-id="6b75c-111">The mechanism that the `Authentication` class uses to authenticate with a  Dynamics 365 for Customer Engagement service depends upon the information you pass into the constructor with the `Configuration` parameter.</span><span class="sxs-lookup"><span data-stu-id="6b75c-111">The mechanism that the `Authentication` class uses to authenticate with a  Dynamics 365 for Customer Engagement service depends upon the information you pass into the constructor with the `Configuration` parameter.</span></span> <span data-ttu-id="6b75c-112">It attempts to build a HttpMessageHandler-derived object that you can then use to instantiate a System.Net.Http.[HttpClient](https://msdn.microsoft.com/library/system.net.http.httpclient\(v=vs.110\).aspx) instance to provide a secure, persistent communication session with the Dynamics 365 for Customer Engagement Service.</span><span class="sxs-lookup"><span data-stu-id="6b75c-112">It attempts to build a HttpMessageHandler-derived object that you can then use to instantiate a System.Net.Http.[HttpClient](https://msdn.microsoft.com/library/system.net.http.httpclient\(v=vs.110\).aspx) instance to provide a secure, persistent communication session with the Dynamics 365 for Customer Engagement Service.</span></span>  
  
 <span data-ttu-id="6b75c-113">First a brief discovery handshake is performed with the specified Dynamics 365 for Customer Engagement service to determine whether OAuth or Windows native authentication is being used.</span><span class="sxs-lookup"><span data-stu-id="6b75c-113">First a brief discovery handshake is performed with the specified Dynamics 365 for Customer Engagement service to determine whether OAuth or Windows native authentication is being used.</span></span>  
  
-   <span data-ttu-id="6b75c-114">If OAuth is used, then an `OAuthMessageHandler` object is created using the authentication authority that was discovered in the handshake.</span><span class="sxs-lookup"><span data-stu-id="6b75c-114">If OAuth is used, then an `OAuthMessageHandler` object is created using the authentication authority that was discovered in the handshake.</span></span> <span data-ttu-id="6b75c-115">This class, derived from System.Net.Http.[DelegatingHandler](https://msdn.microsoft.com/library/hh193679\(v=vs.110\).aspx), refreshes the OAuth access token on every request, so you don’t have to explicitly manage token expiration.</span><span class="sxs-lookup"><span data-stu-id="6b75c-115">This class, derived from System.Net.Http.[DelegatingHandler](https://msdn.microsoft.com/library/hh193679\(v=vs.110\).aspx), refreshes the OAuth access token on every request, so you don’t have to explicitly manage token expiration.</span></span>  
  
-   <span data-ttu-id="6b75c-116">If Windows authentication is used, and user credentials are supplied, then those credentials are used to construct a [HttpClientHandler](https://msdn.microsoft.com/library/system.net.http.httpclienthandler\(v=vs.110\).aspx).</span><span class="sxs-lookup"><span data-stu-id="6b75c-116">If Windows authentication is used, and user credentials are supplied, then those credentials are used to construct a [HttpClientHandler](https://msdn.microsoft.com/library/system.net.http.httpclienthandler\(v=vs.110\).aspx).</span></span>  
  
-   <span data-ttu-id="6b75c-117">If Windows authentication is used, but user credentials are not supplied, then a HttpClientHandler is constructed using default network credentials.</span><span class="sxs-lookup"><span data-stu-id="6b75c-117">If Windows authentication is used, but user credentials are not supplied, then a HttpClientHandler is constructed using default network credentials.</span></span>  
  
## <a name="class-hierarchy-and-members"></a><span data-ttu-id="6b75c-118">Class hierarchy and members</span><span class="sxs-lookup"><span data-stu-id="6b75c-118">Class hierarchy and members</span></span>  
 <span data-ttu-id="6b75c-119">The following table shows the public members of the `Authentication` class.</span><span class="sxs-lookup"><span data-stu-id="6b75c-119">The following table shows the public members of the `Authentication` class.</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="6b75c-120">![Dynamics 365 for Customer Engagement Web API Helper Library-Authentication Class Diagram](../media/web-api-helper-library-authentication-class-diagram.png "Dynamics 365 for Customer Engagement Web API Helper Library-Authentication Class Diagram")</span><span class="sxs-lookup"><span data-stu-id="6b75c-120">![Dynamics 365 for Customer Engagement Web API Helper Library-Authentication Class Diagram](../media/web-api-helper-library-authentication-class-diagram.png "Dynamics 365 for Customer Engagement Web API Helper Library-Authentication Class Diagram")</span></span>|<span data-ttu-id="6b75c-121">**Authentication class**</span><span class="sxs-lookup"><span data-stu-id="6b75c-121">**Authentication class**</span></span><br /><br /> <span data-ttu-id="6b75c-122">*Properties:*</span><span class="sxs-lookup"><span data-stu-id="6b75c-122">*Properties:*</span></span><br /><br /> <span data-ttu-id="6b75c-123">`Authority` – the URL of the server that manages OAuth authentication.</span><span class="sxs-lookup"><span data-stu-id="6b75c-123">`Authority` – the URL of the server that manages OAuth authentication.</span></span><br /><br /> <span data-ttu-id="6b75c-124">`ClientHandler` – the [HttpMessageHandler](https://msdn.microsoft.com/library/hh138091\(v=vs.110\).aspx)-derived object that provides the network credentials or authorization access token for message requests.</span><span class="sxs-lookup"><span data-stu-id="6b75c-124">`ClientHandler` – the [HttpMessageHandler](https://msdn.microsoft.com/library/hh138091\(v=vs.110\).aspx)-derived object that provides the network credentials or authorization access token for message requests.</span></span><br /><br /> <span data-ttu-id="6b75c-125">`Context` – the [AuthenticationContext](https://msdn.microsoft.com/library/microsoft.identitymodel.clients.activedirectory.authenticationcontext.aspx) for an authentication event.</span><span class="sxs-lookup"><span data-stu-id="6b75c-125">`Context` – the [AuthenticationContext](https://msdn.microsoft.com/library/microsoft.identitymodel.clients.activedirectory.authenticationcontext.aspx) for an authentication event.</span></span><br /><br /> <span data-ttu-id="6b75c-126">*Methods:*</span><span class="sxs-lookup"><span data-stu-id="6b75c-126">*Methods:*</span></span><br /><br /> <span data-ttu-id="6b75c-127">`AquireToken` – For OAuth, returns an [AuthenticationResult](https://msdn.microsoft.com/library/microsoft.identitymodel.clients.activedirectory.authenticationresult.aspx),  containing the refresh and access tokens, for the current authentication context.</span><span class="sxs-lookup"><span data-stu-id="6b75c-127">`AquireToken` – For OAuth, returns an [AuthenticationResult](https://msdn.microsoft.com/library/microsoft.identitymodel.clients.activedirectory.authenticationresult.aspx),  containing the refresh and access tokens, for the current authentication context.</span></span><br /><br /> <span data-ttu-id="6b75c-128">`Authentication` – Initializes an instance of this class using the `Configuration` parameter.</span><span class="sxs-lookup"><span data-stu-id="6b75c-128">`Authentication` – Initializes an instance of this class using the `Configuration` parameter.</span></span><br /><br /> <span data-ttu-id="6b75c-129">`DiscoverAuthority` – Discovers the authentication authority of the Dynamics 365 for Customer Engagement web service.</span><span class="sxs-lookup"><span data-stu-id="6b75c-129">`DiscoverAuthority` – Discovers the authentication authority of the Dynamics 365 for Customer Engagement web service.</span></span><br /><br /> <br /><br /> <span data-ttu-id="6b75c-130">**OAuthMessageHandler class**</span><span class="sxs-lookup"><span data-stu-id="6b75c-130">**OAuthMessageHandler class**</span></span><br /><br /> <span data-ttu-id="6b75c-131">This nested class sets the authorization header for each sent message for Dynamics 365 for Customer Engagement apps (online) and IFD deployments.</span><span class="sxs-lookup"><span data-stu-id="6b75c-131">This nested class sets the authorization header for each sent message for Dynamics 365 for Customer Engagement apps (online) and IFD deployments.</span></span>|  
  
## <a name="usage"></a><span data-ttu-id="6b75c-132">Sử dụng</span><span class="sxs-lookup"><span data-stu-id="6b75c-132">Usage</span></span>  
 <span data-ttu-id="6b75c-133">The `Configuration` and `Authentication` classes are designed to be used in tandem to establish a secure connection to the target Dynamics 365 for Customer Engagement service.</span><span class="sxs-lookup"><span data-stu-id="6b75c-133">The `Configuration` and `Authentication` classes are designed to be used in tandem to establish a secure connection to the target Dynamics 365 for Customer Engagement service.</span></span>  <span data-ttu-id="6b75c-134">First you create an object of type `Configuration`, then pass it as the single parameter to the `Authentication` constructor.</span><span class="sxs-lookup"><span data-stu-id="6b75c-134">First you create an object of type `Configuration`, then pass it as the single parameter to the `Authentication` constructor.</span></span>  <span data-ttu-id="6b75c-135">After successful creation, you can use the `ClientHandler` property to construct a secure, authenticated, persistent HTTP client connection to the Dynamics 365 for Customer Engagement service.</span><span class="sxs-lookup"><span data-stu-id="6b75c-135">After successful creation, you can use the `ClientHandler` property to construct a secure, authenticated, persistent HTTP client connection to the Dynamics 365 for Customer Engagement service.</span></span>  
  
 <span data-ttu-id="6b75c-136">One common way to accomplish this operation, which is used by most of the Web API C# samples, is to use the derived class `FileConfiguration` to read connection information from properly authored application configuration files, as demonstrated in the following lines.</span><span class="sxs-lookup"><span data-stu-id="6b75c-136">One common way to accomplish this operation, which is used by most of the Web API C# samples, is to use the derived class `FileConfiguration` to read connection information from properly authored application configuration files, as demonstrated in the following lines.</span></span>  
  
```csharp  
  
FileConfiguration config = new FileConfiguration(null);  
Authentication auth = new Authentication(config);  
httpClient = new HttpClient(auth.ClientHandler, true);  
  
```  
  
 <span data-ttu-id="6b75c-137">For more information on this manner of use, see the section [FileConfiguration connection settings](web-api-helper-code-configuration-classes.md#bkmk_FileConfigconnectionsettings).</span><span class="sxs-lookup"><span data-stu-id="6b75c-137">For more information on this manner of use, see the section [FileConfiguration connection settings](web-api-helper-code-configuration-classes.md#bkmk_FileConfigconnectionsettings).</span></span> <span data-ttu-id="6b75c-138">Although the `Authentication` class contains several other public properties and methods, these are primarily provided to support the creation of the `ClientHandler` property, and would rarely be directly accessed by most client applications.</span><span class="sxs-lookup"><span data-stu-id="6b75c-138">Although the `Authentication` class contains several other public properties and methods, these are primarily provided to support the creation of the `ClientHandler` property, and would rarely be directly accessed by most client applications.</span></span>  
  
## <a name="class-listing"></a><span data-ttu-id="6b75c-139">Class listing</span><span class="sxs-lookup"><span data-stu-id="6b75c-139">Class listing</span></span>  
 <span data-ttu-id="6b75c-140">The most current source for this class is found in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode) NuGet package.</span><span class="sxs-lookup"><span data-stu-id="6b75c-140">The most current source for this class is found in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode) NuGet package.</span></span>  
  
```csharp
using Microsoft.IdentityModel.Clients.ActiveDirectory;  
using System;  
using System.Net;  
using System.Net.Http;  
using System.Net.Http.Headers;  
using System.Security;  
using System.Threading.Tasks;  
  
namespace Microsoft.Crm.Sdk.Samples.HelperCode  
{  
    /// <summary>  
    /// Manages user authentication with the Dynamics CRM Web API (OData v4) services. This class uses Microsoft Azure  
    /// Active Directory Authentication Library (ADAL) to handle the OAuth 2.0 protocol.   
    /// </summary>  
    public class Authentication  
    {  
        private Configuration _config = null;  
        private HttpMessageHandler _clientHandler = null;  
        private AuthenticationContext _context = null;  
        private string _authority = null;  
  
        #region Constructors  
        /// <summary>  
        /// Base constructor.  
        /// </summary>  
        public Authentication() { }  
  
        /// <summary>  
        /// Establishes an authentication session for the service.  
        /// </summary>  
        /// <param name="config">A populated configuration object.</param>  
        public Authentication(Configuration config)  
            : base()  
        {  
            if (config == null)  
                throw new Exception("Configuration cannot be null.");  
  
            _config = config;  
  
            SetClientHandler();  
        }  
  
        /// <summary>  
        /// Custom constructor that allows adding an authority determined asynchronously before   
        /// instantiating the Authentication class.  
        /// </summary>  
        /// <remarks>For a WPF application, first call DiscoverAuthorityAsync(), and then call this  
        /// constructor passing in the authority value.</remarks>  
        /// <param name="config">A populated configuration object.</param>  
        /// <param name="authority">The URL of the authority.</param>  
        public Authentication(Configuration config, string authority)  
            : base()  
        {  
            if (config == null)  
                throw new Exception("Configuration cannot be null.");  
  
            _config = config;  
            Authority = authority;  
  
            SetClientHandler();  
        }  
        #endregion Constructors  
  
        #region Properties  
        /// <summary>  
        /// The authentication context.  
        /// </summary>  
        public AuthenticationContext Context  
        {  
            get  
            { return _context; }  
  
            set  
            { _context = value; }  
        }  
  
        /// <summary>  
        /// The HTTP client message handler.  
        /// </summary>  
        public HttpMessageHandler ClientHandler  
        {  
            get  
            { return _clientHandler; }  
  
            set  
            { _clientHandler = value; }  
        }  
  
        /// <summary>  
        /// The URL of the authority to be used for authentication.  
        /// </summary>  
        public string Authority  
        {  
            get  
            {  
                if (_authority == null)  
                    _authority = DiscoverAuthority(_config.ServiceUrl);  
  
                return _authority;  
            }  
  
            set { _authority = value; }  
        }  
        #endregion Properties  
  
        #region Methods  
        /// <summary>  
        /// Returns the authentication result for the configured authentication context.  
        /// </summary>  
        /// <returns>The refreshed access token.</returns>  
        /// <remarks>Refresh the access token before every service call to avoid having to manage token expiration.</remarks>  
        public AuthenticationResult AcquireToken()  
        {  
            if (_config != null && (!string.IsNullOrEmpty(_config.Username) && _config.Password != null))  
            {  
                UserCredential cred = new UserCredential(_config.Username, _config.Password);  
                return _context.AcquireToken(_config.ServiceUrl, _config.ClientId, cred);  
            }  
            return _context.AcquireToken(_config.ServiceUrl, _config.ClientId, new Uri(_config.RedirectUrl),  
                PromptBehavior.Auto);  
        }  
  
        /// <summary>  
        /// Returns the authentication result for the configured authentication context.  
        /// </summary>  
        /// <param name="username">The username of a CRM system user in the target organization. </param>  
        /// <param name="password">The password of a CRM system user in the target organization.</param>  
        /// <returns>The authentication result.</returns>  
        /// <remarks>Setting the username or password parameters to null results in the user being prompted to  
        /// enter log-on credentials. Refresh the access token before every service call to avoid having to manage  
        /// token expiration.</remarks>  
        public AuthenticationResult AcquireToken(string username, SecureString password)  
        {  
  
            try  
            {  
                if (!string.IsNullOrEmpty(username) && password != null)  
                {  
                    UserCredential cred = new UserCredential(username, password);  
                    return _context.AcquireToken(_config.ServiceUrl, _config.ClientId, cred);  
                }  
            }  
            catch (Exception e)  
            {  
                throw new Exception("Authentication failed. Verify the configuration values are correct.", e);  
            }  
            return null;  
        }  
  
        /// <summary>  
        /// Discover the authentication authority.  
        /// </summary>  
        /// <returns>The URL of the authentication authority on the specified endpoint address, or an empty string  
        /// if the authority cannot be discovered.</returns>  
         public static string DiscoverAuthority(string serviceUrl)  
        {  
            try  
            {  
                AuthenticationParameters ap = AuthenticationParameters.CreateFromResourceUrlAsync(  
                    new Uri(serviceUrl + "api/data/")).Result;  
  
                return ap.Authority;  
            }  
            catch (HttpRequestException e)  
            {  
                throw new Exception("An HTTP request exception occurred during authority discovery.", e);  
            }  
            catch (System.Exception e )  
            {  
                // This exception ocurrs when the service is not configured for OAuth.  
                if( e.HResult == -2146233088 )  
                {  
                    return String.Empty;  
                }  
                else  
                {  
                    throw e;  
                }  
            }  
        }  
  
        /// <summary>  
        /// Discover the authentication authority asynchronously.  
        /// </summary>  
        /// <param name="serviceUrl">The specified endpoint address</param>  
        /// <returns>The URL of the authentication authority on the specified endpoint address, or an empty string  
        /// if the authority cannot be discovered.</returns>  
        public static async Task<string> DiscoverAuthorityAsync(string serviceUrl)  
        {  
            try  
            {  
                AuthenticationParameters ap = await AuthenticationParameters.CreateFromResourceUrlAsync(  
                    new Uri(serviceUrl + "api/data/"));  
  
                return ap.Authority;  
            }  
            catch (HttpRequestException e)  
            {  
                throw new Exception("An HTTP request exception occurred during authority discovery.", e);  
            }  
            catch (Exception e)  
            {  
                // These exceptions ocurr when the service is not configured for OAuth.  
  
                // -2147024809 message: Invalid authenticate header format Parameter name: authenticateHeader  
                if (e.HResult == -2146233088 || e.HResult == -2147024809)  
                {  
                    return String.Empty;  
                }  
                else  
                {  
                    throw e;  
                }  
            }  
        }  
  
        /// <summary>  
        /// Sets the client message handler as appropriate for the type of authentication  
        /// in use on the web service endpoint.  
        /// </summary>  
        private void SetClientHandler()  
        {  
            // Check the Authority to determine if OAuth authentication is used.  
            if (String.IsNullOrEmpty(Authority))  
            {  
                if (_config.Username != String.Empty)  
                {  
                    _clientHandler = new HttpClientHandler()  
                    { Credentials = new NetworkCredential(_config.Username, _config.Password, _config.Domain) };  
                }  
                else  
                // No username is provided, so try to use the default domain credentials.  
                {  
                    _clientHandler = new HttpClientHandler()  
                    { UseDefaultCredentials = true };  
                }  
            }  
            else  
            {  
                _clientHandler = new OAuthMessageHandler(this, new HttpClientHandler());  
                _context = new AuthenticationContext(Authority, false);  
            }  
        }  
        #endregion Methods  
  
        /// <summary>  
        /// Custom HTTP client handler that adds the Authorization header to message requests. This  
        /// is required for IFD and Online deployments.  
        /// </summary>  
        class OAuthMessageHandler : DelegatingHandler  
        {  
            Authentication _auth = null;  
  
            public OAuthMessageHandler( Authentication auth, HttpMessageHandler innerHandler )  
                : base(innerHandler)  
            {  
                _auth = auth;  
            }  
  
            protected override Task<HttpResponseMessage> SendAsync(  
                HttpRequestMessage request, System.Threading.CancellationToken cancellationToken)  
            {  
                // It is a best practice to refresh the access token before every message request is sent. Doing so  
                // avoids having to check the expiration date/time of the token. This operation is quick.  
                request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", _auth.AcquireToken().AccessToken);  
  
                return base.SendAsync(request, cancellationToken);  
            }  
        }  
    }  
}  
```  
  
### <a name="see-also"></a><span data-ttu-id="6b75c-141">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6b75c-141">See also</span></span>  
 <span data-ttu-id="6b75c-142">[Get Started with the Web API (C#)](get-started-dynamics-365-web-api-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="6b75c-142">[Get Started with the Web API (C#)](get-started-dynamics-365-web-api-csharp.md) </span></span>  
 <span data-ttu-id="6b75c-143">[Start a Web API project in Visual Studio (C#)](start-web-api-project-visual-studio-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="6b75c-143">[Start a Web API project in Visual Studio (C#)](start-web-api-project-visual-studio-csharp.md) </span></span>  
 <span data-ttu-id="6b75c-144">[Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="6b75c-144">[Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md) </span></span>  
 <span data-ttu-id="6b75c-145">[Helper code: Configuration class](web-api-helper-code-configuration-classes.md) </span><span class="sxs-lookup"><span data-stu-id="6b75c-145">[Helper code: Configuration class](web-api-helper-code-configuration-classes.md) </span></span>  
 [<span data-ttu-id="6b75c-146">Helper code: CrmHttpResponseException class</span><span class="sxs-lookup"><span data-stu-id="6b75c-146">Helper code: CrmHttpResponseException class</span></span>](web-api-helper-code-crmhttpresponseexception-class.md)
