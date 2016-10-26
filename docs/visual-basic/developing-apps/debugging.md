---
title: "Debugging Your Visual Basic Application"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "debugging [Visual Basic], common tasks"
ms.assetid: 904760b8-9fe9-42a7-9d65-d93774253219
caps.latest.revision: 28
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Debugging Your Visual Basic Application
This page provides links to documentation for the debugging features that are built into [!INCLUDE[vsprvs](../../csharp/includes/vsprvs_md.md)]. For example, you can find semantic errors in your application by observing its run-time behavior in the debugger itself.  
  
 By using the debugger, you can examine the content of variables in your application without inserting additional calls to output the values. Similarly, you can insert a breakpoint in your code to halt execution at the point that you specify.  
  
## Controlling Execution  
 The following table lists debugging tasks involving execution control and provides links to their associated Help pages.  
  
|||  
|-|-|  
|To|See|  
|Start to debug a Visual Studio project, attach to a process, break into code, step through code, run to the cursor, run to a function on the call stack, set the next statement, step through Just My Code, stop debugging, restart debugging, or detach from a debugged process.|[Navigating through Code with the Debugger](../Topic/Navigating%20through%20Code%20with%20the%20Debugger.md)|  
|Specify the configurations for the debug and release versions of a program.|[Debug and Release Project Configurations](http://msdn.microsoft.com/en-us/0440b300-0614-4511-901a-105b771b236e)|  
|Set start options (command-line arguments, working directory, remote machine)|[NIB: How to: Set Start Options for Application Debugging](http://msdn.microsoft.com/en-us/ce792058-7bac-4dd6-858b-466e872687b8)|  
|Debug at design time.|[Walkthrough: Debugging at Design Time](../Topic/Walkthrough:%20Debugging%20at%20Design%20Time.md)|  
|Enable just-in-time debugging, which launches the Visual Studio debugger when a program running outside Visual Studio encounters a fatal error.|[Just-In-Time Debugging](../Topic/Just-In-Time%20Debugging%20in%20Visual%20Studio.md)|  
|Set breakpoints for source lines, assembly instructions, and call stack function. Specify conditions, hit counts, and execution location.|[Using Breakpoints](../Topic/Using%20Breakpoints.md)|  
  
## Handling Exceptions  
 The following table lists debugging tasks involving exception handling and points to their associated Help pages.  
  
|||  
|-|-|  
|To|See|  
|Break on unhandled exceptions.|[How to: Break on User-Unhandled Exceptions](../Topic/How%20to:%20Break%20on%20User-Unhandled%20Exceptions.md)|  
|Break when an exception is thrown.|[How to: Break When an Exception is Thrown](../Topic/How%20to:%20Break%20When%20an%20Exception%20is%20Thrown.md)|  
|Break on first-chance exceptions.|[How to: Break When an Exception is Thrown](../Topic/How%20to:%20Break%20When%20an%20Exception%20is%20Thrown.md)|  
|Use the exception assistant.|[How to: Correct Run-Time Errors with the Exception Assistant](../Topic/How%20to:%20Correct%20Run-Time%20Errors%20with%20the%20Exception%20Assistant.md)|  
|Add a new exception.|[How to: Add New Exceptions](../Topic/How%20to:%20Add%20New%20Exceptions.md)|  
|Continue execution after an exception has been thrown.|[Continuing Execution After an Exception](../Topic/Continuing%20Execution%20After%20an%20Exception.md)|  
  
## Edit and Continue  
 The following table lists debugging tasks involving Edit and Continue and points to their associated Help pages.  
  
|||  
|-|-|  
|To|See|  
|Turn Edit and Continue off and on.|[How to: Enable and Disable Edit and Continue](../Topic/How%20to:%20Enable%20and%20Disable%20Edit%20and%20Continue.md)|  
|Stop Edit and Continue from applying code changes.|[How to: Stop Code Changes](../Topic/How%20to:%20Stop%20Code%20Changes.md)|  
|Apply edits in break mode.|[How to: Apply Edits in Break Mode with Edit and Continue](../Topic/How%20to:%20Apply%20Edits%20in%20Break%20Mode%20with%20Edit%20and%20Continue.md)|  
  
## Examining Debugging Data  
 The following table lists debugging tasks involving viewing debugging data and points to their associated Help pages.  
  
|||  
|-|-|  
|To|See|  
|Use the **Registers** window to display register contents.|[How to: Use the Registers Window](../Topic/How%20to:%20Use%20the%20Registers%20Window.md)|  
|Use the **Call Stack** window to view function or procedure calls that are currently on the stack.|[How to: Use the Call Stack Window](../Topic/How%20to:%20Use%20the%20Call%20Stack%20Window.md)|  
|Use the **Disassembly** window to view assembly code corresponding to the instructions created by the compiler.|[How to: Use the Disassembly Window](../Topic/How%20to:%20Use%20the%20Disassembly%20Window.md)|  
|Use the **Modules** window to list and describe modules used by your program.|[How to: Use the Modules Window](../Topic/How%20to:%20Use%20the%20Modules%20Window.md)|  
|Use the **Script Explorer** window to list script files that are currently loaded into the program.|[How to: View Script Documents](../Topic/How%20to:%20View%20Script%20Documents.md)|  
|Use the **Threads** window to examine and control threads in the program.|[How to: Use the Threads Window](../Topic/How%20to:%20Use%20the%20Threads%20Window.md)|  
  
## See Also  
 [Walkthrough: Debugging a Windows Form](../Topic/Walkthrough:%20Debugging%20a%20Windows%20Form.md)   
 [Debugging Managed Code](../Topic/Debugging%20Managed%20Code.md)   
 [Debugging Native Code](../Topic/Debugging%20Native%20Code.md)   
 [Debugging Web Applications and Script](../Topic/Debugging%20Web%20Applications%20and%20Script.md)   
 [Debugging User Interface Reference](../Topic/Debugging%20User%20Interface%20Reference.md)   
 [Debugger Settings and Preparation](../Topic/Debugger%20Settings%20and%20Preparation.md)   
 [Debugger Basics](../Topic/Debugger%20Basics.md)   
 [Navigating through Code with the Debugger](../Topic/Navigating%20through%20Code%20with%20the%20Debugger.md)   
 [IntelliTrace](../Topic/IntelliTrace.md)   
 [C#, F#, and Visual Basic Project Types](../Topic/Debugging%20Preparation:%20C%23,%20F%23,%20and%20Visual%20Basic%20Project%20Types.md)   
 [How to: Apply Edits in Break Mode with Edit and Continue](../Topic/How%20to:%20Apply%20Edits%20in%20Break%20Mode%20with%20Edit%20and%20Continue.md)