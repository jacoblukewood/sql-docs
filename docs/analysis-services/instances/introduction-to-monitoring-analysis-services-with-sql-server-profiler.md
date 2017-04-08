---
title: "Introduction to Monitoring Analysis Services with SQL Server Profiler | Microsoft Docs"
ms.custom: ""
ms.date: "03/14/2017"
ms.prod: "sql-server-2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "analysis-services"
  - "analysis-services/multidimensional-tabular"
  - "analysis-services/data-mining"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "SQL Server Profiler, Analysis Services"
  - "monitoring Analysis Services [SQL Server]"
  - "performance [Analysis Services]"
  - "performance [Analysis Services], SQL Server Profiler"
  - "Profiler [SQL Server Profiler], Analysis Services"
ms.assetid: 568ec549-5ddc-493a-b9f8-3bdc548b562e
caps.latest.revision: 28
author: "Minewiskan"
ms.author: "owend"
manager: "erikre"
---
# Introduction to Monitoring Analysis Services with SQL Server Profiler
  You can use [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] to monitor events generated by an instance of [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)]. By using [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)], you can do the following:  
  
-   Monitor the performance of an instance of [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)].  
  
-   Debug Multidimensional Expressions (MDX) statements.  
  
-   Identify MDX statements that run slowly.  
  
-   Test MDX statements in the development phase of a project by stepping through statements to confirm that the code works as expected.  
  
-   Troubleshoot problems in [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] by capturing events on a production system and replaying them on a test system. This approach is useful for testing or debugging purposes and lets users continue to use the production system without interference.  
  
-   Audit and review activity that occurred on an instance of [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)]. A security administrator can review any one of the audited events. This includes the success or failure of a login try and the success or failure of permissions in accessing statements and objects.  
  
-   Display data about the captured events to the screen, or capture and save data about each event to a file or [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] table for future analysis or playback. When you replay data, you can rerun the saved events as they originally occurred, either in real time or step by step.  
  
## Using SQL Server Profiler  
 To use [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] to create or replay traces, you must be a member of the [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] server role. If you are a member of the [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] server role, you can start [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] from the [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] program group on the **Start** menu.  
  
 When you use [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)], note the following:  
  
-   Trace definitions are stored with the [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] database by using the CREATE statement.  
  
-   Multiple traces can be running at the same time.  
  
-   Multiple connections can receive events from the same trace.  
  
-   A trace can continue when [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] stops and restarts.  
  
    > [!NOTE]  
    >  Passwords are not revealed in trace events, but are replaced by ****** in the event.  
  
 For optimal performance, use [!INCLUDE[ssSqlProfiler](../../includes/sssqlprofiler-md.md)] to monitor only those events in which you are most interested. Monitoring too many events adds overhead and can cause the trace file or table to grow very large, especially when you monitor over a long period of time. In addition, use filtering to limit the amount of data that is collected and to prevent traces from becoming too large.  
  
## See Also  
 [Analysis Services Trace Events](../../analysis-services/trace-events/analysis-services-trace-events.md)   
 [Create Profiler Traces for Replay &#40;Analysis Services&#41;](../../analysis-services/instances/create-profiler-traces-for-replay-analysis-services.md)  
  
  