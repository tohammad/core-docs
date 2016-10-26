---
title: "How to: Convert Strings into an Array of Bytes in Visual Basic"
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
  - "string conversion, arrays"
  - "arrays [Visual Basic], converting strings to"
  - "byte arrays"
  - "examples [Visual Basic], string conversion"
  - "arrays [Visual Basic], byte arrays"
ms.assetid: f477d35c-a3fc-4a30-b1d4-cd0d353aae1d
caps.latest.revision: 8
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
# How to: Convert Strings into an Array of Bytes in Visual Basic
This topic shows how to convert a string into an array of bytes.  
  
## Example  
 This example uses the <xref:System.Text.Encoding.GetBytes*> method of the <xref:System.Text.Encoding.Unicode*?displayProperty=fullName> encoding class to convert a string into an array of bytes.  
  
 [!code-vb[VbVbalrStrings#74](../../../../visual-basic\language-reference\functions/codesnippet/VisualBasic/how-to-convert-strings-into-an-array-of-bytes_1.vb)]  
  
 You can choose from several encoding options to convert a string into a byte array:  
  
-   <xref:System.Text.Encoding.ASCII*?displayProperty=fullName>: Gets an encoding for the ASCII (7-bit) character set.  
  
-   <xref:System.Text.Encoding.BigEndianUnicode*?displayProperty=fullName>: Gets an encoding for the UTF-16 format using the big-endian byte order.  
  
-   <xref:System.Text.Encoding.Default*?displayProperty=fullName>: Gets an encoding for the system's current ANSI code page.  
  
-   <xref:System.Text.Encoding.Unicode*?displayProperty=fullName>: Gets an encoding for the UTF-16 format using the little-endian byte order.  
  
-   <xref:System.Text.Encoding.UTF32*?displayProperty=fullName>: Gets an encoding for the UTF-32 format using the little-endian byte order.  
  
-   <xref:System.Text.Encoding.UTF7*?displayProperty=fullName>: Gets an encoding for the UTF-7 format.  
  
-   <xref:System.Text.Encoding.UTF8*?displayProperty=fullName>: Gets an encoding for the UTF-8 format.  
  
## See Also  
 <xref:System.Text.Encoding?displayProperty=fullName>   
 <xref:System.Text.Encoding.GetBytes*>   
 [How to: Convert an Array of Bytes into a String in Visual Basic](../../../../visual-basic\programming-guide\language-features\strings/how-to-convert-an-array-of-bytes-into-a-string.md)