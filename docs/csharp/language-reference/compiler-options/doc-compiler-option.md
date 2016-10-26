---
title: "-doc (C# Compiler Options)"
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
  - "FileProperties.BuildAction"
  - "/doc"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "comments, C# code"
  - "XML documentation [C#], comments in source files"
  - "doc compiler option [C#]"
  - "Visual C#, XML documentation for"
  - "-doc compiler option [C#]"
  - "/doc compiler option [C#]"
ms.assetid: 849eea59-c936-4311-bad8-d07404480f2a
caps.latest.revision: 19
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
# /doc (C# Compiler Options)
The **/doc** option allows you to place documentation comments in an XML file.  
  
## Syntax  
  
```  
/doc:file  
```  
  
## Arguments  
 `file`  
 The output file for XML, which is populated with the comments in the source code files of the compilation.  
  
## Remarks  
 In source code files, documentation comments that precede the following can be processed and added to the XML file:  
  
-   Such user-defined types as a [class](../../../csharp\language-reference\keywords/class.md), [delegate](../../../csharp\language-reference\keywords/delegate.md), or [interface](../../../csharp\language-reference\keywords/interface.md)  
  
-   Such members as a field, [event](../../../csharp\language-reference\keywords/event.md), [property](../../../csharp\programming-guide\classes-and-structs/using-properties.md), or method  
  
 The source code file that contains Main is output first into the XML.  
  
 To use the generated .xml file for use with the [IntelliSense](../Topic/Using%20IntelliSense.md) feature, let the file name of the .xml file be the same as the assembly you want to support and then make sure the .xml file is in the same directory as the assembly. Thus, when the assembly is referenced in the Visual Studio project, the .xml file is found as well. See [Supplying Code Comments](../Topic/Supplying%20XML%20Code%20Comments.md) and for more information.  
  
 Unless you compile with [/target:module](../../../csharp\language-reference\compiler-options/target-module-compiler-option.md), `file` will contain \<assembly>\</assembly> tags specifying the name of the file containing the assembly manifest for the output file of the compilation.  
  
> [!NOTE]
>  The /doc option applies to all input files; or, if set in the Project Settings, all files in the project. To disable warnings related to documentation comments for a specific file or section of code, use [#pragma warning](../../../csharp\language-reference\preprocessor-directives/preprocessor-pragma-warning.md).  
  
 See [Recommended Tags for Documentation Comments](../../../csharp\programming-guide\xmldoc/recommended-tags-for-documentation-comments.md) for ways to generate documentation from comments in your code.  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Properties** page.  
  
2.  Click the **Build** tab.  
  
3.  Modify the **XML documentation file** property.  
  
 For information on how to set this compiler option programmatically, see <xref:VSLangProj80.CSharpProjectConfigurationProperties3.DocumentationFile*>.  
  
## See Also  
 [C# Compiler Options](../../../csharp\language-reference\compiler-options/csharp-compiler-options.md)   
 [NIB How to: Modify Project Properties and Configuration Settings](http://msdn.microsoft.com/en-us/e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)