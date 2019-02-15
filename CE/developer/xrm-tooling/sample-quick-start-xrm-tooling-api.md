---
title: 'Sample: Quick start for XRM Tooling API (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: ''
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 060d45bb-b7fd-48bd-ab8f-629c1b8bc1dc
caps.latest.revision: 20
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 18eb03b10c930cf1904e5b62637ee48e5450a1b4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386851"
---
# <a name="sample-quick-start-for-xrm-tooling-api"></a><span data-ttu-id="5315e-102">Sample: Quick start for XRM Tooling API</span><span class="sxs-lookup"><span data-stu-id="5315e-102">Sample: Quick start for XRM Tooling API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5315e-103">The QuickStart sample is a [!INCLUDE[pn_Microsoft_.Net_Framework](../../includes/pn-microsoft-net-framework.md)] managed code sample that shows how to connect to a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps instance by using the XRM Tooling APIs, and perform basic create, update, retrieve, and delete operations on an entity.</span><span class="sxs-lookup"><span data-stu-id="5315e-103">The QuickStart sample is a [!INCLUDE[pn_Microsoft_.Net_Framework](../../includes/pn-microsoft-net-framework.md)] managed code sample that shows how to connect to a [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps instance by using the XRM Tooling APIs, and perform basic create, update, retrieve, and delete operations on an entity.</span></span> <span data-ttu-id="5315e-104">For more information about XRM Tooling, see [Build windows client applications using the XRM tools](../build-windows-client-applications-xrm-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5315e-104">For more information about XRM Tooling, see [Build windows client applications using the XRM tools](../build-windows-client-applications-xrm-tools.md).</span></span>

<span data-ttu-id="5315e-105">Download the sample: [Work with XRM Tooling API](https://code.msdn.microsoft.com/XRM-Tooling-Sample-24a5c55c)</span><span class="sxs-lookup"><span data-stu-id="5315e-105">Download the sample: [Work with XRM Tooling API](https://code.msdn.microsoft.com/XRM-Tooling-Sample-24a5c55c)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5315e-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="5315e-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="5315e-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="5315e-107">Requirements</span></span>

 <span data-ttu-id="5315e-108">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="5315e-108">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span>

## <a name="demonstrates"></a><span data-ttu-id="5315e-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="5315e-109">Demonstrates</span></span>

- <span data-ttu-id="5315e-110">The sample code is built using the **WPF Application for [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)]** SDK template that provides a common login control with built-in support for authentication and credential caching and reuse.</span><span class="sxs-lookup"><span data-stu-id="5315e-110">The sample code is built using the **WPF Application for [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)]** SDK template that provides a common login control with built-in support for authentication and credential caching and reuse.</span></span> <span data-ttu-id="5315e-111">For more information about the common login control and how to use the SDK template in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)], see [Use the XRM Tooling common login control](use-xrm-tooling-common-login-control-client-applications.md).</span><span class="sxs-lookup"><span data-stu-id="5315e-111">For more information about the common login control and how to use the SDK template in [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)], see [Use the XRM Tooling common login control](use-xrm-tooling-common-login-control-client-applications.md).</span></span>  
- <span data-ttu-id="5315e-112">No helper code is used to establish a connection to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="5315e-112">No helper code is used to establish a connection to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span></span>  
- <span data-ttu-id="5315e-113">After connecting to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], the sample performs basic create, update, retrieve, and delete operations on an account entity.</span><span class="sxs-lookup"><span data-stu-id="5315e-113">After connecting to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], the sample performs basic create, update, retrieve, and delete operations on an account entity.</span></span>  
- <span data-ttu-id="5315e-114">Stores user credentials in a configuration file (Default_QuickStartXRMToolingWPFClient.exe.config) in the c:\Users\\*\<username>* \AppData\Roaming\Microsoft\QuickStartXRMToolingWPFClient folder when the sample is run for the first time, and thereafter prompts the user to either use the stored or specify new credentials at runtime to sign in to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="5315e-114">Stores user credentials in a configuration file (Default_QuickStartXRMToolingWPFClient.exe.config) in the c:\Users\\*\<username>* \AppData\Roaming\Microsoft\QuickStartXRMToolingWPFClient folder when the sample is run for the first time, and thereafter prompts the user to either use the stored or specify new credentials at runtime to sign in to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span></span>  
- <span data-ttu-id="5315e-115">Generates the following log files, if any issue occurs, to aid troubleshooting:</span><span class="sxs-lookup"><span data-stu-id="5315e-115">Generates the following log files, if any issue occurs, to aid troubleshooting:</span></span>  
- <span data-ttu-id="5315e-116">Login_ErrorLog.log: To report sign-in errors.</span><span class="sxs-lookup"><span data-stu-id="5315e-116">Login_ErrorLog.log: To report sign-in errors.</span></span> <span data-ttu-id="5315e-117">This file is available at C:\Users\\*\<username>* \AppData\Roaming\Microsoft\QuickStartXRMToolingWPFClient.</span><span class="sxs-lookup"><span data-stu-id="5315e-117">This file is available at C:\Users\\*\<username>* \AppData\Roaming\Microsoft\QuickStartXRMToolingWPFClient.</span></span>  
- <span data-ttu-id="5315e-118">QuickStartXRMToolingWPFClient.log: To report operational errors.</span><span class="sxs-lookup"><span data-stu-id="5315e-118">QuickStartXRMToolingWPFClient.log: To report operational errors.</span></span> <span data-ttu-id="5315e-119">This file is available at the same location as the executable, that is in the debug folder of your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] project.</span><span class="sxs-lookup"><span data-stu-id="5315e-119">This file is available at the same location as the executable, that is in the debug folder of your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] project.</span></span>  

## <a name="to-run-the-sample"></a><span data-ttu-id="5315e-120">To run the sample</span><span class="sxs-lookup"><span data-stu-id="5315e-120">To run the sample</span></span>

1. <span data-ttu-id="5315e-121">Locate and open the SDK\SampleCode\CS\XRMTooling folder.</span><span class="sxs-lookup"><span data-stu-id="5315e-121">Locate and open the SDK\SampleCode\CS\XRMTooling folder.</span></span>  
1. <span data-ttu-id="5315e-122">Open the QuickStartXRMToolingWPFClient.sln file in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5315e-122">Open the QuickStartXRMToolingWPFClient.sln file in Visual Studio.</span></span>  
1. <span data-ttu-id="5315e-123">Press **F5** to compile and run the program.</span><span class="sxs-lookup"><span data-stu-id="5315e-123">Press **F5** to compile and run the program.</span></span>  

## <a name="example"></a><span data-ttu-id="5315e-124">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="5315e-124">Example</span></span>

```csharp  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Text;  
using System.Threading.Tasks;  
using System.Windows;  
using System.Windows.Controls;  
using System.Windows.Data;  
using System.Windows.Documents;  
using System.Windows.Input;  
using System.Windows.Media;  
using System.Windows.Media.Imaging;  
using System.Windows.Navigation;  
using System.Windows.Shapes;  
  
// This namespace is automatically added for using   
// components in LoginWindow\CrmLogin.xaml (common login control).  
using QuickStartXRMToolingWPFClient.LoginWindow;  
  
// Add this namespace for performing   
// various operations in CRM.  
using Microsoft.Xrm.Tooling.Connector;  
  
namespace QuickStartXRMToolingWPFClient  
{  
    /// <summary>  
    /// Demonstrates how to do basic entity operations like create, retrieve,  
    /// update, and delete using the XRM Tooling APIs and the common login  
    /// control.</summary>  
    /// <remarks>  
    /// At run-time, you will be given the option to delete all the  
    /// database records created by this program.</remarks>  
    public partial class MainWindow : Window  
    {  
        public MainWindow()  
        {  
            InitializeComponent();  
            btnDelete.Visibility = Visibility.Hidden;  
        }  
  
        #region Class Level Members  
  
        private CrmLogin _ctrl = null;  
        private Guid _accountId;  
  
        #endregion Class Level Members  
  
        #region How To Sample Code  
  
        /// <summary>  
        /// Connect to Microsoft CRM, and get an instance of CRMServiceClient   
        /// </summary>  
  
        private void LoginButton_Click(object sender, RoutedEventArgs e)  
        {  
            // Create an instance of the XRM Tooling common login control  
            _ctrl = new CrmLogin();  
  
            /// Wire event to the CRM sign-in response.   
            _ctrl.ConnectionToCrmCompleted += ctrl_ConnectionToCrmCompleted;  
            UpdateStatus("Initiating connection to CRM...");  
  
            /// Show the XRM Tooling common login control.   
            _ctrl.ShowDialog();  
  
            /// Validate if you are connected to CRM   
            if (_ctrl.CrmConnectionMgr != null && _ctrl.CrmConnectionMgr.CrmSvc != null && _ctrl.CrmConnectionMgr.CrmSvc.IsReady)  
            {  
                UpdateStatus("Connected to CRM! (Version: " + _ctrl.CrmConnectionMgr.CrmSvc.ConnectedOrgVersion.ToString() +   
                    "; Org: " + _ctrl.CrmConnectionMgr.CrmSvc.ConnectedOrgUniqueName.ToString() + ")");  
                UpdateStatus("***************************************");  
                UpdateStatus("Click Start to create, retrieve, update, and delete (optional) an account record.");  
                btnSignIn.IsEnabled = false;  
                btnCRUD.IsEnabled = true;  
            }  
            // If you are not connected to CRM; display the last error and last CRM excption  
            else  
            {  
                UpdateStatus("The connection to CRM failed or was cancelled by the user.");              
            }              
        }  
  
        private void btnCRUD_Click(object sender, RoutedEventArgs e)  
        {  
            // Create an account record  
            Dictionary<string, CrmDataTypeWrapper> inData = new Dictionary<string, CrmDataTypeWrapper>();  
            inData.Add("name", new CrmDataTypeWrapper("Sample Account Name", CrmFieldType.String));  
            inData.Add("address1_city", new CrmDataTypeWrapper("Redmond", CrmFieldType.String));  
            inData.Add("telephone1", new CrmDataTypeWrapper("555-0160", CrmFieldType.String));  
            _accountId = _ctrl.CrmConnectionMgr.CrmSvc.CreateNewRecord("account", inData);  
  
            // Validate if the account is created, and then retrieve it  
            if (_accountId != Guid.Empty)  
            {  
                UpdateStatus("***************************************");  
                UpdateStatus(DateTime.Now.ToString() + ": Created an account with the following" + "\n" + "details, and retrieved it:");  
                Dictionary<string, object> data = _ctrl.CrmConnectionMgr.CrmSvc.GetEntityDataById("account", _accountId, null);  
                foreach (var pair in data)  
                {  
                    if ((pair.Key == "name") || (pair.Key == "address1_city") || (pair.Key == "telephone1"))  
                    {  
                        UpdateStatus(pair.Key.ToUpper() + ": " + pair.Value);  
                    }  
                }  
                btnCRUD.IsEnabled = false;  
            }  
            else  
            {  
                UpdateStatus("***************************************");  
                UpdateStatus("Could not create the account.");  
            }  
  
            // Update the account record  
            Dictionary<string, CrmDataTypeWrapper> updateData = new Dictionary<string, CrmDataTypeWrapper>();  
            updateData.Add("name", new CrmDataTypeWrapper("Updated Sample Account Name", CrmFieldType.String));  
            updateData.Add("address1_city", new CrmDataTypeWrapper("Boston", CrmFieldType.String));  
            updateData.Add("telephone1", new CrmDataTypeWrapper("555-0161", CrmFieldType.String));   
            bool updateAccountStatus = _ctrl.CrmConnectionMgr.CrmSvc.UpdateEntity("account","accountid",_accountId,updateData);  
  
            // Validate if the account record was updated successfully, and then display the updated information  
            if (updateAccountStatus == true)  
            {  
                UpdateStatus("***************************************");  
                UpdateStatus(DateTime.Now.ToString() + ": Updated the account details as follows:");  
                Dictionary<string, object> data = _ctrl.CrmConnectionMgr.CrmSvc.GetEntityDataById("account", _accountId, null);  
                foreach (var pair in data)  
                {  
                    if ((pair.Key == "name") || (pair.Key == "address1_city") || (pair.Key == "telephone1"))  
                    {  
                        UpdateStatus(pair.Key.ToUpper() + ": " + pair.Value);  
                    }  
                }  
            }  
            else  
            {  
                UpdateStatus("***************************************");  
                UpdateStatus("Could not update the account.");  
            }  
  
            // Prompt the user to delete the account record created in the sample  
            UpdateStatus("***************************************");  
            UpdateStatus("To delete the account record created by the sample, click Delete Record.");  
            UpdateStatus("Otherwise, click Exit to close the sample application.");  
            btnDelete.Visibility = Visibility.Visible;          
        }  
  
        // Delete the account record created in this sample.  
        private void btnDelete_Click(object sender, RoutedEventArgs e)  
        {  
            btnDelete.IsEnabled = false;  
            _ctrl.CrmConnectionMgr.CrmSvc.DeleteEntity("account", _accountId);  
            UpdateStatus("***************************************");  
            UpdateStatus(DateTime.Now.ToString() + ": Deleted the account record.");  
            UpdateStatus("Click Exit to close the sample application.");  
        }  
  
        // Exit the sample application  
        private void btnExit_Click(object sender, RoutedEventArgs e)  
        {  
            this.Close();  
        }  
  
        /// <summary>  
        /// Progressively displays the status messages about the actions  
        /// performed during the running of the sample.  
        /// <param name="updateText">Indicates the status string that needs to be   
        /// displayed to the user.</param>  
        /// </summary>  
        public void UpdateStatus(string updateText)  
        {  
            if (lblStatus.Content.ToString() != String.Empty)  
            {  
                lblStatus.Content = lblStatus.Content + "\n" + updateText;  
            }  
            else  
            {  
                lblStatus.Content = updateText;  
            }  
        }  
  
        /// <summary>  
        /// Raised when the login process is completed.  
        /// </summary>  
        private void ctrl_ConnectionToCrmCompleted(object sender, EventArgs e)  
        {  
            if (sender is CrmLogin)  
            {  
                this.Dispatcher.Invoke(() =>  
                {  
                    ((CrmLogin)sender).Close();  
                });  
            }  
        }  
    }  
    #endregion How To Sample Code  
  
}  
```

### <a name="see-also"></a><span data-ttu-id="5315e-125">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5315e-125">See also</span></span>

[<span data-ttu-id="5315e-126">Use the XRM Tooling common login control</span><span class="sxs-lookup"><span data-stu-id="5315e-126">Use the XRM Tooling common login control</span></span>](use-xrm-tooling-common-login-control-client-applications.md)<br />
[<span data-ttu-id="5315e-127">Build Windows client applications using the XRM tools</span><span class="sxs-lookup"><span data-stu-id="5315e-127">Build Windows client applications using the XRM tools</span></span>](../build-windows-client-applications-xrm-tools.md)<br />
[<span data-ttu-id="5315e-128">Tutorials for Learning About Dynamics 365 for Customer Engagement apps Development</span><span class="sxs-lookup"><span data-stu-id="5315e-128">Tutorials for Learning About Dynamics 365 for Customer Engagement apps Development</span></span>](../tutorials-resources-sdk.md)<br />
