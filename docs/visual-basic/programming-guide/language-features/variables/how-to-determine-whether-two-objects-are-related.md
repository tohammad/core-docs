---
title: "How to: Determine Whether Two Objects Are Related (Visual Basic)"
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
  - "inheritance, Visual Basic objects"
  - "objects [Visual Basic], inheritance"
  - "object variables, determining relation"
ms.assetid: da002e3f-6616-4bad-a229-f842d06652bb
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
# How to: Determine Whether Two Objects Are Related (Visual Basic)
You can compare two objects to determine the relationship, if any, between the classes from which they are created. The <xref:System.Type.IsInstanceOfType*> method of the <xref:System.Type?displayProperty=fullName> class returns `True` if the specified class inherits from the current class, or if the current type is an interface supported by the specified class.  
  
### To determine if one object inherits from another object's class or interface  
  
1.  On the object you think might be of the base type, invoke the <xref:System.Object.GetType*> method.  
  
2.  On the <xref:System.Type?displayProperty=fullName> object returned by <xref:System.Object.GetType*>, invoke the <xref:System.Type.IsInstanceOfType*> method.  
  
3.  In the argument list for <xref:System.Type.IsInstanceOfType*>, specify the object you think might be of the derived type.  
  
     <xref:System.Type.IsInstanceOfType*> returns `True` if its argument type inherits from the <xref:System.Type?displayProperty=fullName> object type.  
  
## Example  
 The following example determines whether one object represents a class derived from another object's class.  
  
```  
Public Class baseClass  
End Class  
Public Class derivedClass : Inherits baseClass  
End Class  
Public Class testTheseClasses  
    Public Sub seeIfRelated()  
        Dim baseObj As Object = New baseClass()  
        Dim derivedObj As Object = New derivedClass()  
        Dim related As Boolean  
        related = baseObj.GetType().IsInstanceOfType(derivedObj)  
        MsgBox(CStr(related))  
    End Sub  
End Class  
```  
  
 Note the unexpected placement of the two object variables in the call to <xref:System.Type.IsInstanceOfType*>. The supposed base type is used to generate the <xref:System.Type?displayProperty=fullName> class, and the supposed derived type is passed as an argument to the <xref:System.Type.IsInstanceOfType*> method.  
  
## See Also  
 <xref:System.Object.GetType*>   
 <xref:System.Type?displayProperty=fullName>   
 <xref:System.Type.IsInstanceOfType*>   
 [Object Data Type](../../../../visual-basic\language-reference\data-types/object-data-type.md)   
 [Object Variables](../../../../visual-basic\programming-guide\language-features\variables/object-variables.md)   
 [Object Variable Values](../../../../visual-basic\programming-guide\language-features\variables/object-variable-values.md)   
 [How to: Determine Whether Two Objects Are Identical](../../../../visual-basic\programming-guide\language-features\variables/how-to-determine-whether-two-objects-are-identical.md)