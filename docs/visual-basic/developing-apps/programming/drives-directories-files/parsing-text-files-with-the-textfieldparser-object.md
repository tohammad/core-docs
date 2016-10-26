---
title: "Parsing Text Files with the TextFieldParser Object (Visual Basic)"
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
  - "TextFieldParser object, using"
  - "I/O [Visual Basic], parsing files"
  - "files, parsing"
ms.assetid: fc31d6e6-af0c-403f-8a00-d556b2c57567
caps.latest.revision: 20
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
# Parsing Text Files with the TextFieldParser Object (Visual Basic)
The `TextFieldParser` object allows you to parse and process very large file that are structured as delimited-width columns of text, such as log files or legacy database information. Parsing a text file with `TextFieldParser` is similar to iterating over a text file, while the parse method to extract fields of text is similar to string manipulation methods used to tokenize delimited strings.  
  
## Parsing Different Types of Text Files  
 Text files may have fields of various width, delimited by a character such as a comma or a tab space. Define `TextFieldType` and the delimiter, as in the following example, which uses the `SetDelimiters` method to define a tab-delimited text file:  
  
 [!code-vb[VbVbalrTextFieldParser#21](../../../../visual-basic\developing-apps\development-with-my/codesnippet/VisualBasic/parsing-text-files-with-the-textfieldparser-object_1.vb)]  
  
 Other text files may have field widths that are fixed. In such cases, you need to define the `TextFieldType` as `FixedWidth` and define the widths of each field, as in the following example. This example uses the `SetFieldWidths` method to define the columns of text: the first column is 5 characters wide, the second is 10, the third is 11, and the fourth is of variable width.  
  
 [!code-vb[VbVbalrTextFieldParser#22](../../../../visual-basic\developing-apps\development-with-my/codesnippet/VisualBasic/parsing-text-files-with-the-textfieldparser-object_2.vb)]  
  
 Once the format is defined, you can loop through the file, using the `ReadFields` method to process each line in turn.  
  
 If a field does not match the specified format, a <xref:Microsoft.VisualBasic.FileIO.MalformedLineException> exception is thrown. When such exceptions are thrown, the `ErrorLine` and `ErrorLineNumber` properties hold the text causing the exception and the line number of that text.  
  
## Parsing Files with Multiple Formats  
 The `PeekChars` method of the `TextFieldParser` object can be used to check each field before reading it, allowing you to define multiple formats for the fields and react accordingly. For more information, see [How to: Read From Text Files with Multiple Formats](../../../../visual-basic\developing-apps\programming\drives-directories-files/how-to-read-from-text-files-with-multiple-formats.md).  
  
## See Also  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.OpenTextFieldParser*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.PeekChars*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ReadFields*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.CommentTokens*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.Delimiters*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLine*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLineNumber*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.FieldWidths*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.HasFieldsEnclosedInQuotes*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.LineNumber*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.TextFieldType*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.TrimWhiteSpace*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.SetDelimiters*>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.SetFieldWidths*>   
 [Troubleshooting Exceptions: Microsoft.VisualBasic.FileIO.TextFieldParser.MalformedLineException](../Topic/Troubleshooting%20Exceptions:%20Microsoft.VisualBasic.FileIO.TextFieldParser.MalformedLineException.md)