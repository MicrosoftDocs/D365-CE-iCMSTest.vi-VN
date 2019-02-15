---
title: Configure client diagnostic logging in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn how to set client diagnostic logging.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 3c690a33-f305-4a6d-a65d-990e9504d5e5
caps.latest.revision: 25
author: kabala123
ms.author: kabala
manager: shujoshi
tags:
- MigrationHO
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 69ac2052998679f988e142515ef931684c65f681
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382588"
---
# <a name="client-diagnostic-logging-overview"></a>Client diagnostic logging overview
There are two ways you can configure [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client diagnostic logging:  

- By using an Audit & Diagnostics Settings record that is created and managed in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] area of [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.  

- By manually making changes to the UnifiedServiceDesk.exe.config file. This file must then be distributed to every desktop where you want [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client diagnostic logging.  

  Additionally, you can configure diagnostic logging specifically for exceptions that may occur in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.  

<a name="ConfigureLogging"></a>   
## <a name="configure-includepnunifiedservicedeskincludespn-unified-service-deskmd-client-diagnostic-logging"></a>Configure [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client diagnostic logging  
 This section describes how to manually configure diagnostic logging in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. Rather than use the procedure described here, we recommend you use the Audit & Diagnostics Settings feature that provides centralized administration of diagnostics and the ability to connect a custom listener. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Configure auditing and diagnostics in Unified Service Desk](../../unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk.md)  

> [!IMPORTANT]
> - The manually-configured diagnostics (as described here), will no longer work after you enable an Audit & Diagnostics Settings record that is configured for diagnostics.  
>   - [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] also provides an API that lets you configure rich diagnostic logging for custom hosted controls. More information:  [Configure enhanced diagnostic logging for custom hosted controls](../../unified-service-desk/configure-enhanced-diagnostic-logging-custom-hosted-controls.md)  

 This topic describes how to change client logging characteristics.  

 You can enable logging with the **UnifiedServiceDesk.exe.config** file, which is available in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client installation directory on your computer. Để cấu hình loại ghi nhật ký và vị trí tệp nhật ký [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]:  

1. Mở tệp **UnifiedServiceDesk.exe.config** để chỉnh sửa. Nếu bạn đã cài đặt ứng dụng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] ở vị trí mặc định, tệp này thường sẽ có sẵn tại C:\Program Files\Microsoft Dynamics 365 for Customer Engagement USD\USD.  

2. Go to the `<switches>` section in the file:  

   ```xml  
   <switches>  
   <!--   
        Possible values for switches: Off, Error, Warning, Information, Verbose  
           Verbose:      includes Error, Warning, Info, Trace levels  
           Information:  includes Error, Warning, Info levels  
           Warning:      includes Error, Warning levels  
           Error:        includes Error level  
    -->  
       <add name="EventTopicSwitch" value="Error"/>  
       <add name="Microsoft.Uii.Common.Logging" value="Error"/>  
       <add name="Microsoft.Xrm.Tooling.CrmConnectControl" value="Error"/>  
       <add name="Microsoft.Xrm.Tooling.Connector.CrmServiceClient" value="Error"/>  
       <add name="Microsoft.Xrm.Tooling.WebResourceUtility" value="Error"/>  
       <add name="Microsoft.Crm.UnifiedServiceDesk" value="Error"/>  
       <add name="Microsoft.Crm.UnifiedServiceDesk.Dynamics" value="Error"/>  
       <add name="Microsoft.Crm.UnifiedServiceDesk.CommonUtility.UserProfileManager" value="Error"/>  
       <add name="UnifiedServiceDesk.KPIControl" value="Error"/>  
   </switches>  

   ```  

3. In the `<switches>` section, specify a logging source (such as `EventTopicSwitch`), and then specify a logging level value (such as `Error`). The `<switches>` section controls logging levels for various sources. Theo mặc định, nhật ký lỗi được bật cho tất cả các lần chuyển đổi:  

   -   For information about the available logging sources, see [Available Log Sources](configure-client-diagnostic-logging-unified-service-desk.md#LogSources) later in this topic.  

   -   For information about the values you can specify for each logging source, see [Logging Levels](configure-client-diagnostic-logging-unified-service-desk.md#LoggingLevels) later in this topic.  

4. To configure the location, maximum file size, and rollover behavior of the log files, go to the `<shareListeners>` section in the file.  

   ```xml  
   <sharedListeners>  
      <add name="fileListener"  
         type="Microsoft.Xrm.Tooling.Connector.DynamicsFileLogTraceListener, Microsoft.Xrm.Tooling.Connector"  
       BaseFileName="UnifiedServiceDesk"  
       Location="LocalUserApplicationDirectory" MaxFileSize ="52428800" MaxFileCount="10"/>  
      <add name="USDDebugListener" type="Microsoft.Crm.UnifiedServiceDesk.Dynamics.UsdTraceListener, Microsoft.Crm.UnifiedServiceDesk.Dynamics" />  
      <add name="ADALListener"  
       type="Microsoft.Xrm.Tooling.Connector.DynamicsFileLogTraceListener, Microsoft.Xrm.Tooling.Connector"  
       BaseFileName="ADAL"  
        Location="LocalUserApplicationDirectory" MaxFileSize ="52428800" MaxFileCount="10"/>  
   </sharedListeners>  
   ```  

    The `<sharelisteners>` section controls the location and type of logs that are generated for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. By default, `fileListener` will create a file called **UnifiedServiceDesk.log** in c:\Users\\*\<UserName>* \AppData\Roaming\Microsoft\UnifiedServiceDesk\\*\<Version>* directory, and `USDDebugListener` will create events in the [Debug output tab](../../unified-service-desk/use-debugger-control-unified-service-desk.md) of the Debugger hosted control.  

5. Nếu bạn muốn thay đổi vị trí của tệp **UnifiedServiceDesk.log**, hãy thay đổi giá trị của tham số `Location`.  

6. By default, a new [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] log is created after the file size of the current log file exceeds 52.42 MB. By default, up to 10 log files are maintained at one time before the oldest log file is deleted.  

   - To change the maximum [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] log file size, change the value, in bytes, of the **MaxFileSize** parameter.  

   - To change the number of logs maintained before the oldest  log is deleted, change the value of the **MaxFileCount** parameter. If zero (0) is used rollover logging will be disabled and all [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client logs created will be saved.  

7. Theo mặc định, nhật ký tệp và trình sửa lỗi được bật cho tất cả các nguồn. If you want to add or remove a listener from a diagnostic source, locate the required source in the `<sources>` section, and then modify the `<listeners>` section of the source to include the listener you want.  

    For example, to add event logging for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], add the event logging listener to the `Microsoft.Crm.UnifiedServiceDesk` source.  

   ```xml  
   <source name="Microsoft.Crm.UnifiedServiceDesk" switchName="Microsoft.Crm.UnifiedServiceDesk" switchType="System.Diagnostics.SourceSwitch">  
       <listeners>  
           <add name="fileListener"/>  
           <add name="USDDebugListener" />  
           <add name="eventLogListener" type="System.Diagnostics.EventLogTraceListener" initializeData="USD"/>  
       </listeners>  
   </source>  
   ```  

    Điều này bây giờ sẽ báo cáo các sự kiện cho nhật ký sự kiện [!INCLUDE[pn_ms_Windows_short](../../includes/pn-ms-windows-short.md)] bằng thẻ "USD", bên cạnh tệp và trình gỡ lỗi. For more information about diagnostic listeners, see [Diagnostic Log Listeners](configure-client-diagnostic-logging-unified-service-desk.md#LogListeners) later in this topic.  

<a name="LogSources"></a>   
## <a name="diagnostic-log-sources"></a>Nguồn nhật ký chẩn đoán  
 Nguồn nhật ký khắc phục sự cố phổ biến được liệt kê trong trong bảng sau.  


|                            Tên nguồn thông tin                            |                                                                                                                                                        Mô tả                                                                                                                                                        |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                         EventTopicSwitch                          |                                                                          Nguồn nhật ký [!INCLUDE[pn_user_inteface_integration_uii](../../includes/pn-user-interface-integration-uii.md)] chi tiết cho giám sát lưu lượng tin nhắn bên trong UII.                                                                           |
|                   Microsoft.Uii.Common.Logging                    |                                                                                                                                   Nguồn nhật ký UII chung cho các tin nhắn được báo cáo bởi UII.                                                                                                                                    |
|              Microsoft.Xrm.Tooling.CrmConnectControl              |                                                          Nguồn nhật ký cho quy trình đăng nhập vào [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)]. Nguồn này sẽ báo cáo thông tin chẩn đoán chung hoặc chi tiết về quy trình đăng nhập.                                                           |
|         Microsoft.Xrm.Tooling.Connector.CrmServiceClient          |                                     Nguồn nhật ký cho tất cả tương tác cấp dữ liệu [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)]. Nguồn này sẽ báo cáo tất cả tương tác với [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], các trường hợp ngoại lệ và thời gian.                                      |
|             Microsoft.Xrm.Tooling.WebResourceUtility              |                                                                                           Nguồn nhật ký cho các yếu cầu về dữ liệu tài nguyên web qua liên kết giao diện [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].                                                                                            |
|                 Microsoft.Crm.UnifiedServiceDesk                  |                            Nguồn nhật ký cho chức năng [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] lõi.  Nguồn nhật ký này sẽ báo cáo các thao tác và sự kiện chính với [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].                             |
|             Microsoft.Crm.UnifiedServiceDesk.Dynamics             |     Nguồn nhật ký cho [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] tự khởi động và tải bộ vi xử lý. Nguồn này sẽ báo cáo thao tác và sự kiện là một phần của quá trình khởi tạo và bắt đầu UII và [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].     |
| Microsoft.Crm.UnifiedServiceDesk.CommonUtility.UserProfileManager | Nguồn nhật ký cho các thao tác tương tác với hệ thống UserProfile; đây là một phần của hệ thống bộ nhớ đệm. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Configure client caching for your agent application](../../unified-service-desk/admin/configure-client-caching-unified-service-desk.md) |

 Bạn có thể chuyển đổi từng nguồn nhật ký này một cách độc lập để hỗ trợ xử lý sự cố và cô lập các vấn đề hoặc thông tin bên trong [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)].  

<a name="LoggingLevels"></a>   
## <a name="diagnostic-logging-levels"></a>Cấp độ nhật ký chẩn đoán  
 Có rất nhiều cấp nhật ký khác nhau để sử dụng. Tuy nhiên, khi bạn tăng mức độ nhật ký, sẽ có nhiều dữ liệu được tạo và lưu trữ trong tệp nhật ký hơn.  

|Mức độ nhật ký|Mô tả|  
|---------------|-----------------|  
|Tắt|Tắt tất cả các sự kiện từ nguồn này.|  
|Lỗi|Chỉ báo cáo sự kiện lỗi.|  
|Cảnh báo|Báo cáo lỗi và sự kiện cảnh báo.|  
|Thông tin|Báo cáo lỗi, cảnh báo và sự kiện thông tin.|  
|Diễn giải|Báo cáo lỗi, cảnh báo, thông tin và sự kiện diễn giải.|  
|ActivityTracing|Báo cáo lỗi, cảnh báo, thông tin và sự kiện diễn giải và theo dõi hoạt động (tên phương pháp). **Note:**  ActivityTracing is available only on some of the sources.|  
|Tất cả|Báo cáo tất cả sự kiện của hệ thống.|  

<a name="LogListeners"></a>   
## <a name="diagnostic-log-listeners"></a>Người nghe nhật ký chẩn đoán  
 Người nghe nhật ký chẩn đoán được sử dụng để nhắm mục tiêu đầu ra nhật ký chẩn đoán thành tệp, nhật ký sự kiện hoặc các nguồn khác. Theo mặc định, tất cả các nguồn chẩn đoán được trang bị cho cả (Trình sửa lỗi ) mặc định và người nghe (văn bản) tệp. Bạn có thể đặt cấu hình người nghe nhật ký bổ sung cho nhật ký chẩn đoán [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]. Để biết thêm chi tiết về người nghe mặc định .NET, hãy xem:  

- [MSDN:DefaultTraceListener](https://msdn.microsoft.com/library/8fdtceh6.aspx)  

- [MSDN:EventLogTraceListener](https://msdn.microsoft.com/library/2s3yhxyf.aspx)  

- [MSDN:TextWriterTraceListener](https://msdn.microsoft.com/library/d1ckdta4.aspx)  

  You can also create custom listeners to send diagnostic logs to a location you pick. Custom listeners are created by deriving a class from the [MSDN:TraceListener](https://msdn.microsoft.com/library/hy72797k.aspx) abstract class. You can find a walkthrough of the process on [CodeGuru.com](http://www.codeguru.com/csharp/.net/article.php/c19405/Tracing-in-NET-and-Implementing-Your-Own-Trace-Listeners.htm).  

<a name="View_diagnostic_log"></a>   
## <a name="viewing-the-diagnostic-log-file"></a>Viewing the diagnostic log file  
 By default, diagnostics logging is enabled for the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application. A log file, **UnifiedServiceDesk-\<date>.log**, is available at c:\Users\\*\<UserName>* \AppData\Roaming\Microsoft\Microsoft Dynamics 365 for Customer Engagement Unified Service Desk\\*\<Version>* on the client computer to record operational errors in the client application. Tệp nhật ký được tạo ra lần đầu tiên bạn gặp bất kỳ sự lỗi đăng nhập nào vào ứng dụng khách.  

 When an error occurs in a hosted control, the  information logged in the log files provide detailed information about the exception such as the originating hosted control that caused the exception along with the exception details. Notice that the entire JavaScript code that caused the exception isn't logged. Only the faulty code along with exception description are logged.  

 Here is a sample exception detail that is logged.  

```Output  
Microsoft.Crm.UnifiedServiceDesk.Dynamics   Error   2   12/27/2016 11:54:15 AM  Origin:AppdomianUnhandledException, IsFatal:True  
Source: DemoControl  
Target: Void throwExceptionMethod()  
Exception: Exception in custom control  
StackTrace:   at DemoControl.USDControl.throwExceptionMethod()  
   at System.Threading.ExecutionContext.RunInternal(ExecutionContext executionContext, ContextCallback callback, Object state, Boolean preserveSyncCtx)  
   at System.Threading.ExecutionContext.Run(ExecutionContext executionContext, ContextCallback callback, Object state, Boolean preserveSyncCtx)  
   at System.Threading.ExecutionContext.Run(ExecutionContext executionContext, ContextCallback callback, Object state)  
   at System.Threading.ThreadHelper.ThreadStart()  

```  

<a name="usdmp"></a>   
## <a name="unified-service-desk-monitoring-process"></a>Unified Service Desk Monitoring Process  
 The [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] Monitoring Process (usdmp.exe) is a service that continuously monitors the health of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], and terminates, by default after 5 seconds, any browser process instances that are unresponsive and causing [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to become unresponsive.  If a browser process instance isn’t responding, but [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] is responsive, the browser process instance won’t be terminated. For more information about how to change the  duration of the ProcessTerminationThreshold global option for browser process termination, see [Manage Options for Unified Service Desk](../../unified-service-desk/admin/manage-options-unified-service-desk.md).  

<a name="exceptionlogging"></a>   
## <a name="error-diagnostics-reporting"></a>Error diagnostics reporting  
 Having detailed and comprehensive logging and reporting that occurs during a  component, application, or system fault can help identify when and how the fault occurred. In addition to standard diagnostics logging, error diagnostics reporting records system and application state information in the event of an exception in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client. More information about exceptions can be found in [How Unified Service Desk handles application and system errors](../../unified-service-desk/admin/how-unified-service-desk-handles-application-system-errors.md ).  

### <a name="folders-and-files-created-during-an-exception"></a>Folders and files created during an exception  
 In the event of an exception, error diagnostics reporting creates a folder on the local computer named DiagnosticsLogs_*date and time*, where date and time is in the form year-month-date_time, such as DiagnosticLogs_20170322_173643. Within the DiagnosticsLogs folder the following folder and files are created.  


|                     Diagnostics file                     |                                                                                                                                                                                                                                                                                                                                     Mô tả                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           UnifiedServiceDesk_*dateandtime*.log           |                                                                                                                                Standard diagnostics log that is created and appended when [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client is running. The file contains logging information for the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client (UnifiedServiceDesk.exe). The current files are moved into the DiagnosticsLogs folder in the event of an exception.                                                                                                                                 |
|         UnifiedServiceDeskMonitoring_*date*.log          | Standard diagnostics log that is created and appended when [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client is running. Contains logging information for the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] monitoring process (usdmp.exe), which is a process that monitors the health of the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client.   The current files are moved into the DiagnosticsLogs folder in the event of an exception. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Unified Service Desk Monitoring Process](#usdmp) |
|                    Eventlogs (folder)                    |                                                                                                                                                                                                                                                                  Folder created in the event of a fatal or non-fatal exception. Contains Windows system and application event logs and error reporting text files.                                                                                                                                                                                                                                                                  |
|                      ExitReport.txt                      |                                                                                                                                                                                                             Exit log created in the event of a fatal or non-fatal exception. Contains process state information such as machine name, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] version, process id, exit code, and time of exit.                                                                                                                                                                                                              |
|                 MachineHealthReport.txt                  |                                                                                                                                                                                                                                          Exit log created in the event of a fatal or non-fatal exception. Contains system state information such as computer processor, operating system, monitor details, language, and browser version.                                                                                                                                                                                                                                           |
|                    ProcessReport.csv                     |                                                                                                                                                                                                                                                    Exit log created in the event of a fatal or non-fatal exception. Provides a comprehensive list of all processes that were running on the system at the time of the exception.                                                                                                                                                                                                                                                    |
|                     RegistryLog.txt                      |                                                                                                                                                                                                                                     Exit log created in the event of a fatal or non-fatal exception. Includes a text-based  copy of the Windows Registry subkeys for [!INCLUDE[pn_Internet_Explorer](../../includes/pn-internet-explorer.md)].                                                                                                                                                                                                                                      |
| UnifiedServiceDesk_processId_CrashDump_*dateandtime*.dmp |                                                                                                                                                     Created only in the event of an unhandled fatal exception or when invoked manually by using the ManualDumpShortcut global option keyboard combination. Provides a full memory  dump file for UnifiedServiceDesk.exe. Notice that, to view the dump file, you need [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] or other Windows dump file viewing tool.                                                                                                                                                     |

<a name="exceptionoptions"></a>   
### <a name="configure-error-diagnostics-reporting"></a>Configure error diagnostics reporting  

1. In the web application, go to **Settings** > **Unified Service Desk** > **Auditing and Diagnostics**.  

2. Click **New**, and then select **DiagnosticsConfiguration**.  

3. Select or enter the values that you want, such as tracking, exit monitoring, and the diagnostics logs folder location. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Diagnostics](../../unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk.md#BKMK_Diagnostics)  

4. Click **Save & Close**.  

## <a name="see-also"></a>Xem thêm  
 [Configure auditing and diagnostics in Unified Service Desk](../../unified-service-desk/admin/configure-auditing-diagnostics-unified-service-desk.md)   
 [Debugging support in Unified Service Desk to troubleshoot issues](../../unified-service-desk/admin/troubleshoot-unified-service-desk.md)   
 [Khắc phục sự cố trong Unified Service Desk](../../unified-service-desk/debug-issues-unified-service-desk.md)
