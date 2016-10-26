---
title: "File already open"
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
  - "vbrID55"
dev_langs: 
  - "VB"
ms.assetid: d674a0fb-ef16-4cc2-9da7-709a8a07dbea
caps.latest.revision: 7
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
# File already open
Sometimes a file must be closed before another `FileOpen` or other operation can occur. Among the possible causes of this error are:  
  
-   A sequential output mode `FileOpen` operation was executed for a file that is already open  
  
-   A statement refers to an open file.  
  
### To correct this error  
  
1.  Close the file before executing the statement.  
  
## See Also  
 <xref:Microsoft.VisualBasic.FileSystem.FileOpen*>