---
title: "Iterator (Visual Basic)"
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
  - "vb.Iterator"
helpviewer_keywords: 
  - "Iterator keyword [Visual Basic]"
ms.assetid: 69cb0b04-ac87-49d0-bcfe-810c0d60daff
caps.latest.revision: 11
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
# Iterator (Visual Basic)
Specifies that a function or `Get` accessor is an iterator.  
  
## Remarks  
 An *iterator* performs a custom iteration over a collection. An iterator uses the [Yield](../../../visual-basic\language-reference\statements/yield-statement.md) statement to return each element in the collection one at a time. When a `Yield` statement is reached, the current location in code is retained. Execution is restarted from that location the next time that the iterator function is called.  
  
 An iterator can be implemented as a function or as a `Get` accessor of a property definition. The `Iterator` modifier appears in the declaration of the iterator function or `Get` accessor.  
  
 You call an iterator from client code by using a [For Each...Next Statement](../../../visual-basic\language-reference\statements/for-each-next-statement.md).  
  
 The return type of an iterator function or `Get` accessor can be <xref:System.Collections.IEnumerable>, <xref:System.Collections.Generic.IEnumerable`1>, <xref:System.Collections.IEnumerator>, or <xref:System.Collections.Generic.IEnumerator`1>.  
  
 An iterator cannot have any `ByRef` parameters.  
  
 An iterator cannot occur in an event, instance constructor, static constructor, or static destructor.  
  
 An iterator can be an anonymous function. For more information, see [Iterators](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md).  
  
 For more information about iterators, see [Iterators](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md).  
  
## Usage  
 The `Iterator` modifier can be used in these contexts:  
  
-   [Function Statement](../../../visual-basic\language-reference\statements/function-statement.md)  
  
-   [Property Statement](../../../visual-basic\language-reference\statements/property-statement.md)  
  
## Example  
 The following example demonstrates an iterator function. The iterator function has a `Yield` statement that is inside a [For…Next](../../../visual-basic\language-reference\statements/for-next-statement.md) loop. Each iteration of the [For Each](../../../visual-basic\language-reference\statements/for-each-next-statement.md) statement body in `Main` creates a call to the `Power` iterator function. Each call to the iterator function proceeds to the next execution of the `Yield` statement, which occurs during the next iteration of the `For…Next` loop.  
  
 [!code-vb[VbVbalrStatements#98](../../../visual-basic\language-reference\error-messages/codesnippet/VisualBasic/iterator_1.vb)]  
  
## Example  
 The following example demonstrates a `Get` accessor that is an iterator. The `Iterator` modifier is in the property declaration.  
  
 [!code-vb[VbVbalrStatements#99](../../../visual-basic\language-reference\error-messages/codesnippet/VisualBasic/iterator_2.vb)]  
  
 For additional examples, see [Iterators](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md).  
  
## See Also  
 <xref:System.Runtime.CompilerServices.IteratorStateMachineAttribute>   
 [Iterators](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md)   
 [Yield Statement](../../../visual-basic\language-reference\statements/yield-statement.md)