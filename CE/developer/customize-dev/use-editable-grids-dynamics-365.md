---
title: Use editable grids in Customer Engagement (Dynamics 365 for Customer Engagement Developer Guide) | MicrosoftDocs
description: Editable grid is a new custom control in Dynamics 365 for Customer Engagement that provides rich inline editing capabilities on web and mobile clients (Dynamics 365 for Customer Engagement for phones and Dynamics 365 for Customer Engagement for tablets) including the ability to group, sort, and filter data within the same grid so that you do not have to switch records or views.
ms.custom: ''
ms.date: 10/18/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ffc75be6-cf2b-4707-9cdc-871e17544056
caps.latest.revision: 16
author: KumarVivek
ms.author: kvivek
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 55c0e3f50e023e27b171d0e038164ad89800f83f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387959"
---
# <a name="use-editable-grids-in-customer-engagement"></a><span data-ttu-id="1f168-103">Use editable grids in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="1f168-103">Use editable grids in Customer Engagement</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1f168-104">Editable grid is a custom control in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement that provides rich inline editing capabilities on web and mobile clients ([!INCLUDE[pn_Mobile_Express_short](../../includes/pn-mobile-express-short.md)] and [!INCLUDE[pn_moca_short](../../includes/pn-moca-short.md)]) including the ability to group, sort, and filter data within the same grid so that you do not have to switch records or views.</span><span class="sxs-lookup"><span data-stu-id="1f168-104">Editable grid is a custom control in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement that provides rich inline editing capabilities on web and mobile clients ([!INCLUDE[pn_Mobile_Express_short](../../includes/pn-mobile-express-short.md)] and [!INCLUDE[pn_moca_short](../../includes/pn-moca-short.md)]) including the ability to group, sort, and filter data within the same grid so that you do not have to switch records or views.</span></span> <span data-ttu-id="1f168-105">The editable grid control is supported in the main grid and subgrids on a form in the web client and in dashboards and on form grids on the mobile clients.</span><span class="sxs-lookup"><span data-stu-id="1f168-105">The editable grid control is supported in the main grid and subgrids on a form in the web client and in dashboards and on form grids on the mobile clients.</span></span> <span data-ttu-id="1f168-106">Although the editable grid control provides editing capability, it honors the read-only grid metadata and field-level security settings.</span><span class="sxs-lookup"><span data-stu-id="1f168-106">Although the editable grid control provides editing capability, it honors the read-only grid metadata and field-level security settings.</span></span> <span data-ttu-id="1f168-107">Editable grids also support business rules and form scripting so you can apply custom business logic according to your organization's requirements.</span><span class="sxs-lookup"><span data-stu-id="1f168-107">Editable grids also support business rules and form scripting so you can apply custom business logic according to your organization's requirements.</span></span>  

> [!NOTE] 
> <span data-ttu-id="1f168-108">If you are using legacy forms (versions prior to Dynamics CRM 2016) and enable an editable grid on a subgrid, the editable subgrid will not be rendered.</span><span class="sxs-lookup"><span data-stu-id="1f168-108">If you are using legacy forms (versions prior to Dynamics CRM 2016) and enable an editable grid on a subgrid, the editable subgrid will not be rendered.</span></span> <span data-ttu-id="1f168-109">Quản trị viên hệ thống có thể tắt các biểu mẫu cũ trong thiết đặt hệ thống nếu cần thiết.</span><span class="sxs-lookup"><span data-stu-id="1f168-109">System administrators can turn off legacy forms in system settings, if needed.</span></span> 

<span data-ttu-id="1f168-110">For more information about using editable grids using the UI, see [Make grids (lists) editable using the Editable Grid custom control](../../customize/make-grids-lists-editable-custom-control.md)</span><span class="sxs-lookup"><span data-stu-id="1f168-110">For more information about using editable grids using the UI, see [Make grids (lists) editable using the Editable Grid custom control](../../customize/make-grids-lists-editable-custom-control.md)</span></span> 
  
  
<a name="FormScripting"></a>   
## <a name="form-scripting-support"></a><span data-ttu-id="1f168-111">Form scripting support</span><span class="sxs-lookup"><span data-stu-id="1f168-111">Form scripting support</span></span>  
 <span data-ttu-id="1f168-112">The editable grids support client-side events and methods that can be used to write custom client extensions according to your business need.</span><span class="sxs-lookup"><span data-stu-id="1f168-112">The editable grids support client-side events and methods that can be used to write custom client extensions according to your business need.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="1f168-113">[Grids and subgrids in Customer Engagement (Client API reference)](../clientapi/reference/grids.md)</span><span class="sxs-lookup"><span data-stu-id="1f168-113">[Grids and subgrids in Customer Engagement (Client API reference)](../clientapi/reference/grids.md)</span></span> 
  
<a name="EntitiesSupported"></a>   
## <a name="entities-and-views-supported-by-editable-grid"></a><span data-ttu-id="1f168-114">Entities and views supported by editable grid</span><span class="sxs-lookup"><span data-stu-id="1f168-114">Entities and views supported by editable grid</span></span>  
 <span data-ttu-id="1f168-115">Not all entities and views support the use of editable grid.</span><span class="sxs-lookup"><span data-stu-id="1f168-115">Not all entities and views support the use of editable grid.</span></span>  
  
 <span data-ttu-id="1f168-116">On the web client, an entity will support editable grid if all of the following conditions are true:</span><span class="sxs-lookup"><span data-stu-id="1f168-116">On the web client, an entity will support editable grid if all of the following conditions are true:</span></span>  
  
- <span data-ttu-id="1f168-117">The entity is customizable (IsCustomizable = true)</span><span class="sxs-lookup"><span data-stu-id="1f168-117">The entity is customizable (IsCustomizable = true)</span></span>  
  
- <span data-ttu-id="1f168-118">The entity is either refreshed (IsAIRUpdated = true) or a custom entity (IsCustomEntity = true)</span><span class="sxs-lookup"><span data-stu-id="1f168-118">The entity is either refreshed (IsAIRUpdated = true) or a custom entity (IsCustomEntity = true)</span></span>  
  
- <span data-ttu-id="1f168-119">The entity is not a child entity (IsChildEntity = false)</span><span class="sxs-lookup"><span data-stu-id="1f168-119">The entity is not a child entity (IsChildEntity = false)</span></span>  
  
  <span data-ttu-id="1f168-120">On the [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] mobile client, an entity will support editable grid if the entity can be displayed in the mobile client's site map.</span><span class="sxs-lookup"><span data-stu-id="1f168-120">On the [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] mobile client, an entity will support editable grid if the entity can be displayed in the mobile client's site map.</span></span>  
  
  <span data-ttu-id="1f168-121">For information about the entities that support editable grids, see **Supported out-of-the-box entities** section in [Make grids (lists) editable in Dynamics 365 for Customer Engagement using the Editable Grid custom control](../../customize/make-grids-lists-editable-custom-control.md)</span><span class="sxs-lookup"><span data-stu-id="1f168-121">For information about the entities that support editable grids, see **Supported out-of-the-box entities** section in [Make grids (lists) editable in Dynamics 365 for Customer Engagement using the Editable Grid custom control](../../customize/make-grids-lists-editable-custom-control.md)</span></span>  
  
  <span data-ttu-id="1f168-122">Editable grids do not support roll up associated views (**Rollup type** = `Related`).</span><span class="sxs-lookup"><span data-stu-id="1f168-122">Editable grids do not support roll up associated views (**Rollup type** = `Related`).</span></span>  
  
  <span data-ttu-id="1f168-123">Use the following sample code to generate an XML file that you can open in [!INCLUDE[pn_microsoft_excel](../../includes/pn-microsoft-excel.md)] as an XML table to view the entity-support information for editable controls.</span><span class="sxs-lookup"><span data-stu-id="1f168-123">Use the following sample code to generate an XML file that you can open in [!INCLUDE[pn_microsoft_excel](../../includes/pn-microsoft-excel.md)] as an XML table to view the entity-support information for editable controls.</span></span> [!INCLUDE[pn_Excel_short](../../includes/pn-excel-short.md)] <span data-ttu-id="1f168-124">will figure out the schema automatically, and display the information under the following columns:</span><span class="sxs-lookup"><span data-stu-id="1f168-124">will figure out the schema automatically, and display the information under the following columns:</span></span>  
  
- <span data-ttu-id="1f168-125">`LogicalName`: Logical name of entity.</span><span class="sxs-lookup"><span data-stu-id="1f168-125">`LogicalName`: Logical name of entity.</span></span>  
  
- <span data-ttu-id="1f168-126">`DisplayName`: Display name of entity.</span><span class="sxs-lookup"><span data-stu-id="1f168-126">`DisplayName`: Display name of entity.</span></span>  
  
- <span data-ttu-id="1f168-127">`CanEnableEditableGridWeb`: Displays status  (True or False) whether editable grid is supported for the entity  on the web client.</span><span class="sxs-lookup"><span data-stu-id="1f168-127">`CanEnableEditableGridWeb`: Displays status  (True or False) whether editable grid is supported for the entity  on the web client.</span></span>  
  
- <span data-ttu-id="1f168-128">`CanEnableEditableGridMobile`: Displays status (True or False) whether editable grid is supported for the entity on mobile clients.</span><span class="sxs-lookup"><span data-stu-id="1f168-128">`CanEnableEditableGridMobile`: Displays status (True or False) whether editable grid is supported for the entity on mobile clients.</span></span> <span data-ttu-id="1f168-129">([!INCLUDE[pn_Mobile_Express_short](../../includes/pn-mobile-express-short.md)] and [!INCLUDE[pn_moca_short](../../includes/pn-moca-short.md)]).</span><span class="sxs-lookup"><span data-stu-id="1f168-129">([!INCLUDE[pn_Mobile_Express_short](../../includes/pn-mobile-express-short.md)] and [!INCLUDE[pn_moca_short](../../includes/pn-moca-short.md)]).</span></span>  
  
```csharp  
using System;  
using System.Linq;  
using System.Xml.Linq;  
using System.ServiceModel;  
using System.ServiceModel.Description;  
using System.Collections.Generic;  
using System.Xml.Serialization;  
using System.Xml;  
using System.IO;  
  
// These namespaces are found in the Microsoft.Xrm.Sdk.dll assembly  
// found in the SDK\bin folder.  
using Microsoft.Xrm.Sdk;  
using Microsoft.Xrm.Sdk.Query;  
using Microsoft.Xrm.Sdk.Metadata;  
using Microsoft.Xrm.Sdk.Client;  
using Microsoft.Xrm.Sdk.Messages;  
  
// This namespace is found in Microsoft.Crm.Sdk.Proxy.dll assembly  
// found in the SDK\bin folder.  
using Microsoft.Crm.Sdk.Messages;  
  
namespace Microsoft.Crm.Sdk.Samples  
{  
    /// <summary>  
    /// This sample generates an XML table to display the entity-support information for   
    ///  editable controls.  
    /// </summary>  
    public class DumpEditableGridEntityInfo  
    {  
        #region Class Level Members  
  
        /// <summary>  
        /// Stores the organization service proxy.  
        /// </summary>  
        OrganizationServiceProxy _serviceProxy;  
  
        // Create storage for new attributes being created  
        public List<AttributeMetadata> addedAttributes;  
  
        // Specify which language code to use in the sample. If you are using a language  
        // other than US English, you will need to modify this value accordingly.  
        // See http://msdn.microsoft.com/en-us/library/0h88fahh.aspx  
        public const int _languageCode = 1033;  
  
        // Define the IDs/variables needed for this sample.  
        public int _insertedStatusValue;  
  
        #endregion Class Level Members  
  
        #region How To Sample Code  
        /// <summary>  
        /// </summary>  
        /// <param name="serverConfig">Contains server connection information.</param>  
        /// <param name="promptForDelete">When True, the user will be prompted to delete all  
        /// created entities.</param>  
        public void Run(ServerConnection.Configuration serverConfig, bool promptForDelete)  
        {  
            try  
            {  
  
                // Connect to the Organization service.   
                // The using statement assures that the service proxy will be properly disposed.  
                using (_serviceProxy = new OrganizationServiceProxy(serverConfig.OrganizationUri, serverConfig.HomeRealmUri, serverConfig.Credentials, serverConfig.DeviceCredentials))  
                {  
                    // This statement is required to enable early-bound type support.  
                    _serviceProxy.EnableProxyTypes();  
  
                    //<snippetDumpEditableGridEntityInfo1>  
                    RetrieveAllEntitiesRequest request = new RetrieveAllEntitiesRequest()  
                    {  
                        EntityFilters = EntityFilters.Entity,  
                        RetrieveAsIfPublished = true  
                    };  
  
                    // Retrieve the MetaData.  
                    RetrieveAllEntitiesResponse response = (RetrieveAllEntitiesResponse)_serviceProxy.Execute(request);  
  
                    // Create an instance of StreamWriter to write text to a file.  
                    // The using statement also closes the StreamWriter.  
                    // To view this file, right click the file and choose open with Excel.   
                    // Excel will figure out the schema and display the information in columns.  
  
                    String filename = String.Concat("EditableGridEntityInfo.xml");  
                    using (StreamWriter sw = new StreamWriter(filename))  
                    {  
                        // Create Xml Writer.  
                        XmlTextWriter metadataWriter = new XmlTextWriter(sw);  
  
                        // Start Xml File.  
                        metadataWriter.WriteStartDocument();  
  
                        // Metadata Xml Node.  
                        metadataWriter.WriteStartElement("Metadata");  
  
                        foreach (EntityMetadata currentEntity in response.EntityMetadata)  
                        {  
                            // Start Entity Node  
                            metadataWriter.WriteStartElement("Entity");  
  
                            bool canBeDisplayedInSitemap = currentEntity.IsCustomizable.Value;  
  
                            if (canBeDisplayedInSitemap)  
                            {  
                                metadataWriter.WriteElementString("LogicalName", currentEntity.LogicalName);  
                                metadataWriter.WriteElementString("DisplayName", currentEntity.DisplayName.UserLocalizedLabel?.Label);  
                                metadataWriter.WriteElementString("CanEnableEditableGridWeb", (!(bool)currentEntity.IsChildEntity && ((bool)currentEntity.IsAIRUpdated || (bool)currentEntity.IsCustomEntity)).ToString());  
                                metadataWriter.WriteElementString("CanEnableEditableGridMobile", (currentEntity.IsVisibleInMobileClient.Value || currentEntity.IsVisibleInMobileClient.CanBeChanged).ToString());  
                            }  
  
                            // Write the Entity's Information.  
  
                            //End Entity Node  
                            metadataWriter.WriteEndElement();  
                        }  
  
                        // End Metadata Xml Node  
                        metadataWriter.WriteEndElement();  
                        metadataWriter.WriteEndDocument();  
  
                        // Close xml writer.  
                        metadataWriter.Close();  
                        Console.WriteLine("Dumped information in the EditableGridEntityInfo.xml file");  
                    }  
                }  
            }  
  
            // Catch any service fault exceptions that Microsoft Dynamics CRM throws.  
            catch (FaultException<Microsoft.Xrm.Sdk.OrganizationServiceFault>)  
            {  
                // You can handle an exception here or pass it back to the calling method.  
                throw;  
            }  
        }  
        #endregion How To Sample Code  
  
        #region Main  
        /// <summary>  
        /// Standard Main() method used by most SDK samples.  
        /// </summary>  
        /// <param name="args"></param>  
        static public void Main(string[] args)  
        {  
            try  
            {  
                // Obtain the target organization's Web address and client logon   
                // credentials from the user.  
                ServerConnection serverConnect = new ServerConnection();  
                ServerConnection.Configuration config = serverConnect.GetServerConfiguration();  
                DumpEditableGridEntityInfo app = new DumpEditableGridEntityInfo();  
                app.Run(config, false);                  
            }  
            catch (FaultException<Microsoft.Xrm.Sdk.OrganizationServiceFault> ex)  
            {  
                Console.WriteLine("The application terminated with an error.");  
                Console.WriteLine("Timestamp: {0}", ex.Detail.Timestamp);  
                Console.WriteLine("Code: {0}", ex.Detail.ErrorCode);  
                Console.WriteLine("Message: {0}", ex.Detail.Message);  
                Console.WriteLine("Plugin Trace: {0}", ex.Detail.TraceText);  
                Console.WriteLine("Inner Fault: {0}",  
                    null == ex.Detail.InnerFault ? "No Inner Fault" : "Has Inner Fault");  
            }  
            catch (System.TimeoutException ex)  
            {  
                Console.WriteLine("The application terminated with an error.");  
                Console.WriteLine("Message: {0}", ex.Message);  
                Console.WriteLine("Stack Trace: {0}", ex.StackTrace);  
                Console.WriteLine("Inner Fault: {0}",  
                    null == ex.InnerException.Message ? "No Inner Fault" : ex.InnerException.Message);  
            }  
            catch (System.Exception ex)  
            {  
                Console.WriteLine("The application terminated with an error.");  
                Console.WriteLine(ex.Message);  
  
                // Display the details of the inner exception.  
                if (ex.InnerException != null)  
                {  
                    Console.WriteLine(ex.InnerException.Message);  
  
                    FaultException<Microsoft.Xrm.Sdk.OrganizationServiceFault> fe  
                        = ex.InnerException  
                        as FaultException<Microsoft.Xrm.Sdk.OrganizationServiceFault>;  
                    if (fe != null)  
                    {  
                        Console.WriteLine("Timestamp: {0}", fe.Detail.Timestamp);  
                        Console.WriteLine("Code: {0}", fe.Detail.ErrorCode);  
                        Console.WriteLine("Message: {0}", fe.Detail.Message);  
                        Console.WriteLine("Plugin Trace: {0}", fe.Detail.TraceText);  
                        Console.WriteLine("Inner Fault: {0}",  
                            null == fe.Detail.InnerFault ? "No Inner Fault" : "Has Inner Fault");  
                    }  
                }  
            }  
            // Additional exceptions to catch: SecurityTokenValidationException, ExpiredSecurityTokenException,  
            // SecurityAccessDeniedException, MessageSecurityException, and SecurityNegotiationException.  
  
            finally  
            {  
  
                Console.WriteLine("Press <Enter> to exit.");  
                Console.ReadLine();  
            }  
  
        }  
        #endregion Main  
  
    }  
}  
```  

## <a name="frequently-asked-questions-faqs"></a><span data-ttu-id="1f168-130">Câu hỏi thường gặp (FAQ)</span><span class="sxs-lookup"><span data-stu-id="1f168-130">Frequently asked questions (FAQs)</span></span>

<span data-ttu-id="1f168-131">For a list of FAQs related to editable grids, see [Editable grids FAQs](../../customize/make-grids-lists-editable-custom-control.md#frequently-asked-questions-faqs)</span><span class="sxs-lookup"><span data-stu-id="1f168-131">For a list of FAQs related to editable grids, see [Editable grids FAQs](../../customize/make-grids-lists-editable-custom-control.md#frequently-asked-questions-faqs)</span></span>

### <a name="see-also"></a><span data-ttu-id="1f168-132">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1f168-132">See also</span></span>  
 [<span data-ttu-id="1f168-133">Grids and subgrids in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="1f168-133">Grids and subgrids in Customer Engagement</span></span>](../clientapi/reference/grids.md) <br/> 
 [<span data-ttu-id="1f168-134">Để lưới (danh sách) có thể chỉnh sửa được, hãy sử dụng kiểm soát tùy chỉnh Lưới có thể chỉnh sửa</span><span class="sxs-lookup"><span data-stu-id="1f168-134">Make grids (lists) editable using the Editable Grid custom control</span></span>](../../customize/make-grids-lists-editable-custom-control.md)<br/>
 [<span data-ttu-id="1f168-135">Sử dụng phím tắt trong lưới có thể chỉnh sửa</span><span class="sxs-lookup"><span data-stu-id="1f168-135">Use keyboard shortcuts in editable grids</span></span>](../../basics/keyboard-shortcuts.md#editable-grids-views)
