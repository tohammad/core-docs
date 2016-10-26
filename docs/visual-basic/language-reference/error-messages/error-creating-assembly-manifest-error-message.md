---
title: "Error creating assembly manifest: &lt;error message&gt;"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30140"
  - "vbc30140"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30140"
ms.assetid: 1beb5aa0-7b79-4c85-946b-5c2d0a41d1d2
caps.latest.revision: 13
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
# Error creating assembly manifest: &lt;error message&gt;
The [!INCLUDE[vbprvb](../../../csharp\programming-guide\concepts\linq/includes/vbprvb_md.md)] compiler calls the Assembly Linker (Al.exe, also known as Alink) to generate an assembly with a manifest. The linker has reported an error in the pre-emission stage of creating the assembly.  
  
 This can occur if there are problems with the key file or the key container specified. To fully sign an assembly, you must provide a valid key file that contains information about the public and private keys. To delay sign an assembly, you must select the **Delay sign only** check box and provide a valid key file that contains information about the public key information. The private key is not necessary when an assembly is delay-signed. For more information, see [How to: Sign an Assembly (Visual Studio)](http://msdn.microsoft.com/en-us/f468a7d3-234c-4353-924d-8e0ae5896564).  
  
 **Error ID:** BC30140  
  
### To correct this error  
  
1.  Examine the quoted error message and consult the topic [Al.exe Tool Errors and Warnings](http://msdn.microsoft.com/en-us/7f125d49-0a03-47a6-9ba9-d61a679a7d4b) for error AL1019 further explanation and advice  
  
2.  If the error persists, gather information about the circumstances and notify Microsoft Product Support Services.  
  
## See Also  
 [How to: Sign an Assembly (Visual Studio)](http://msdn.microsoft.com/en-us/f468a7d3-234c-4353-924d-8e0ae5896564)   
 [Signing Page, Project Designer](../Topic/Signing%20Page,%20Project%20Designer.md)   
 [Al.exe (Assembly Linker)](../Topic/Al.exe%20\(Assembly%20Linker\).md)   
 [Al.exe Tool Errors and Warnings](http://msdn.microsoft.com/en-us/7f125d49-0a03-47a6-9ba9-d61a679a7d4b)   
 [Talk to Us](../Topic/Talk%20to%20Us.md)