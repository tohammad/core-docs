---
title: "Input past end of file"
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
  - "vbrID62"
dev_langs: 
  - "VB"
ms.assetid: 65292704-6e7d-4622-9f50-eb655a59b016
caps.latest.revision: 9
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
# Input past end of file
Either an `Input` statement is reading from a file that is empty or one in which all the data is used, or you used the `EOF` function with a file opened for binary access.  
  
### To correct this error  
  
1.  Use the `EOF` function immediately before the `Input` statement to detect the end of the file.  
  
2.  If the file is opened for binary access, use `Seek` and `Loc`.  
  
## See Also  
 <xref:Microsoft.VisualBasic.FileSystem.Input*>   
 <xref:Microsoft.VisualBasic.FileSystem.EOF*>   
 <xref:Microsoft.VisualBasic.FileSystem.Seek*>   
 <xref:Microsoft.VisualBasic.FileSystem.Loc*>