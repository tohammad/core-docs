---
title: "Recursive Procedures (Visual Basic)"
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
  - "Visual Basic code, procedures"
  - "procedures, that call themselves"
  - "procedures, recursive"
  - "procedures, calling"
  - "recursive procedures"
  - "functions [Visual Basic], calling recursively"
  - "recursion"
ms.assetid: ba1d3962-b4c3-48d3-875e-96fdb4198327
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
# Recursive Procedures (Visual Basic)
A *recursive* procedure is one that calls itself. In general, this is not the most effective way to write [!INCLUDE[vbprvb](../../../csharp\programming-guide\concepts\linq/includes/vbprvb_md.md)] code.  
  
 The following procedure uses recursion to calculate the factorial of its original argument.  
  
 [!code-vb[VbVbcnProcedures#51](../../../visual-basic\language-reference\procedures/codesnippet/VisualBasic/recursive-procedures_1.vb)]  
  
## Considerations with Recursive Procedures  
 **Limiting Conditions**. You must design a recursive procedure to test for at least one condition that can terminate the recursion, and you must also handle the case where no such condition is satisfied within a reasonable number of recursive calls. Without at least one condition that can be met without fail, your procedure runs a high risk of executing in an infinite loop.  
  
 **Memory Usage**. Your application has a limited amount of space for local variables. Each time a procedure calls itself, it uses more of that space for additional copies of its local variables. If this process continues indefinitely, it eventually causes a <xref:System.StackOverflowException> error.  
  
 **Efficiency**. You can almost always substitute a loop for recursion. A loop does not have the overhead of passing arguments, initializing additional storage, and returning values. Your performance can be much better without recursive calls.  
  
 **Mutual Recursion**. You might observe very poor performance, or even an infinite loop, if two procedures call each other. Such a design presents the same problems as a single recursive procedure, but can be harder to detect and debug.  
  
 **Calling with Parentheses**. When a `Function` procedure calls itself recursively, you must follow the procedure name with parentheses, even if there is no argument list. Otherwise, the function name is taken as representing the return value of the function.  
  
 **Testing**. If you write a recursive procedure, you should test it very carefully to make sure it always meets some limiting condition. You should also ensure that you cannot run out of memory due to having too many recursive calls.  
  
## See Also  
 <xref:System.StackOverflowException>   
 [Procedures](../../../visual-basic\language-reference\procedures/index.md)   
 [Sub Procedures](../../../visual-basic\language-reference\procedures/sub-procedures.md)   
 [Function Procedures](../../../visual-basic\language-reference\procedures/function-procedures.md)   
 [Property Procedures](../../../visual-basic\language-reference\procedures/property-procedures.md)   
 [Operator Procedures](../../../visual-basic\language-reference\procedures/operator-procedures.md)   
 [Procedure Parameters and Arguments](../../../visual-basic\language-reference\procedures/procedure-parameters-and-arguments.md)   
 [Procedure Overloading](../../../visual-basic\language-reference\procedures/procedure-overloading.md)   
 [Troubleshooting Procedures](../../../visual-basic\language-reference\procedures/troubleshooting-procedures.md)   
 [Loop Structures](../../../visual-basic\programming-guide\language-features\control-flow/loop-structures.md)   
 [Troubleshooting Exceptions: System.StackOverflowException](../Topic/Troubleshooting%20Exceptions:%20System.StackOverflowException.md)