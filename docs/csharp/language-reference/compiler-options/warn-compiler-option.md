---
title: "-warn (C# Compiler Options)"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "/warn"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "warning level [C#]"
  - "/w compiler option [C#]"
  - "-w compiler option [C#]"
  - "-warn compiler option [C#]"
  - "/warn compiler option [C#]"
  - "w compiler option [C#]"
  - "warn compiler option [C#]"
ms.assetid: 5f80ff59-4991-4382-9f9a-77da18446e71
caps.latest.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
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
# /warn (C# Compiler Options)
The **/warn** option specifies the warning level for the compiler to display.  
  
## Syntax  
  
```  
/warn:option  
```  
  
## Arguments  
 `option`  
 The warning level you want displayed for the compilation: Lower numbers show only high severity warnings; higher numbers show more warnings. Valid values are 0-4:  
  
|Warning level|Meaning|  
|-------------------|-------------|  
|0|Turns off emission of all warning messages.|  
|1|Displays severe warning messages.|  
|2|Displays level 1 warnings plus certain, less-severe warnings, such as warnings about hiding class members.|  
|3|Displays level 2 warnings plus certain, less-severe warnings, such as warnings about expressions that always evaluate to `true` or `false`.|  
|4 (the default)|Displays all level 3 warnings plus informational warnings.|  
  
## Remarks  
 To get information about an error or warning, you can look up the error code in the Help Index. For other ways to get information about an error or warning, see [C# Compiler Errors](../../../csharp\language-reference\compiler-messages/index.md).  
  
 Use [/warnaserror](../../../csharp\language-reference\compiler-options/warnaserror-compiler-option.md) to treat all warnings as errors. Use [/nowarn](../../../csharp\language-reference\compiler-options/nowarn-compiler-option.md) to disable certain warnings.  
  
 **/w** is the short form of **/warn**.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Properties** page.  
  
2.  Click the **Build** property page.  
  
3.  Modify the **Warning Level** property.  
  
 For information on how to set this compiler option programmatically, see <xref:VSLangProj80.CSharpProjectConfigurationProperties3.WarningLevel*>.  
  
## Example  
 Compile `in.cs` and have the compiler only display level 1 warnings:  
  
```  
csc /warn:1 in.cs  
```  
  
## See Also  
 [C# Compiler Options](../../../csharp\language-reference\compiler-options/csharp-compiler-options.md)   
 [NIB How to: Modify Project Properties and Configuration Settings](http://msdn.microsoft.com/en-us/e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)