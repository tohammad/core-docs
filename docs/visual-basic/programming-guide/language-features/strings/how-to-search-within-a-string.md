---
title: "How to: Search Within a String (Visual Basic)"
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
  - "strings [Visual Basic], finding"
  - "strings [Visual Basic], searching"
  - "examples [Visual Basic], strings"
ms.assetid: ae4c79e0-08ea-489f-bdb2-5eb6d355f284
caps.latest.revision: 16
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
# How to: Search Within a String (Visual Basic)
This example calls the <xref:System.String.IndexOf*> method on a <xref:System.String> object to report the index of the first occurrence of a substring.  
  
## Example  
 [!code-vb[VbVbalrStrings#71](../../../../visual-basic\language-reference\functions/codesnippet/VisualBasic/how-to-search-within-a-string_1.vb)]  
  
## Compiling the Code  
 This example requires:  
  
-   An `Imports` statement specifying the <xref:System> namespace. For more information, see [Imports Statement (.NET Namespace and Type)](../../../../visual-basic\language-reference\statements/imports-statement-net-namespace-and-type.md).  
  
## Robust Programming  
 The <xref:System.String.IndexOf*> method reports the location of the first character of the first occurrence of the substring. The index is 0-based, which means the first character of a string has an index of 0.  
  
 If <xref:System.String.IndexOf*> does not find the substring, it returns -1.  
  
 The <xref:System.String.IndexOf*> method is case-sensitive and uses the current culture.  
  
 For optimal error control, you might want to enclose the string search in the `Try` block of a [Try...Catch...Finally Statement](../../../../visual-basic\language-reference\statements/try-catch-finally-statement.md) construction.  
  
## See Also  
 <xref:System.String.IndexOf*>   
 [Try...Catch...Finally Statement](../../../../visual-basic\language-reference\statements/try-catch-finally-statement.md)   
 [Introduction to Strings in Visual Basic](../../../../visual-basic\programming-guide\language-features\strings/introduction-to-strings.md)   
 [Strings](../../../../visual-basic\programming-guide\language-features\strings/index.md)