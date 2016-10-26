---
title: "&#39;&lt;eventname&gt;&#39; is an event, and cannot be called directly"
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
  - "bc32022"
  - "vbc32022"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC32022"
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
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
# &#39;&lt;eventname&gt;&#39; is an event, and cannot be called directly
'<`eventname`>' is an event, and so cannot be called directly. Use a `RaiseEvent` statement to raise an event.  
  
 A procedure call specifies an event for the procedure name. An event handler is a procedure, but the event itself is a signaling device, which must be raised and handled.  
  
 **Error ID:** BC32022  
  
### To correct this error  
  
1.  Use a `RaiseEvent` statement to signal an event and invoke the procedure or procedures that handle it.  
  
## See Also  
 [RaiseEvent Statement](../../../visual-basic\language-reference\statements/raiseevent-statement.md)