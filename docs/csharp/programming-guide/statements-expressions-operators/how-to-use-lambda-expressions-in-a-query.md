---
title: "How to: Use Lambda Expressions in a Query (C# Programming Guide)"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "lambda expressions [C#], in LINQ"
ms.assetid: 3cac4d25-d11f-4abd-9e7c-0f02e97ae06d
caps.latest.revision: 16
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
# How to: Use Lambda Expressions in a Query (C# Programming Guide)
You do not use lambda expressions directly in query syntax, but you do use them in method calls, and query expressions can contain method calls. In fact, some query operations can only be expressed in method syntax. For more information about the difference between query syntax and method syntax, see [Query Syntax and Method Syntax in LINQ](../../../csharp\programming-guide\concepts\linq/query-syntax-and-method-syntax-in-linq.md).  
  
## Example  
 The following example demonstrates how to use a lambda expression in a method-based query by using the <xref:System.Linq.Enumerable.Where*?displayProperty=fullName> standard query operator. Note that the <xref:System.Linq.Enumerable.Where*> method in this example has an input parameter of the delegate type <xref:System.Func`1> and that delegate takes an integer as input and returns a Boolean. The lambda expression can be converted to that delegate. If this were a [!INCLUDE[vbtecdlinq](../../../csharp/includes/vbtecdlinq_md.md)] query that used the <xref:System.Linq.Queryable.Where*?displayProperty=fullName> method, the parameter type would be an `Expression<Func\<int,bool>>` but the lambda expression would look exactly the same. For more information on the Expression type, see <xref:System.Linq.Expressions.Expression?displayProperty=fullName>.  
  
 [!code-cs[csProgGuideLINQ#1](../../../csharp\programming-guide\classes-and-structs/codesnippet/CSharp/how-to-use-lambda-expressions-in-a-query_1.cs)]  
  
## Example  
 The following example demonstrates how to use a lambda expression in a method call of a query expression. The lambda is necessary because the <xref:System.Linq.Enumerable.Sum*> standard query operator cannot be invoked by using query syntax.  
  
 The query first groups the students according to their grade level, as defined in the `GradeLevel` enum. Then for each group it adds the total scores for each student. This requires two `Sum` operations. The inner `Sum` calculates the total score for each student, and the outer `Sum` keeps a running, combined total for all students in the group.  
  
 [!code-cs[csProgGuideLINQ#2](../../../csharp\programming-guide\classes-and-structs/codesnippet/CSharp/how-to-use-lambda-expressions-in-a-query_2.cs)]  
  
## Compiling the Code  
 To run this code, copy and paste the method into the `StudentClass` that is provided in [How to: Query a Collection of Objects](../../../csharp\programming-guide\linq-query-expressions/how-to-query-a-collection-of-objects.md) and call it from the `Main` method.  
  
## See Also  
 [Lambda Expressions](../../../csharp\programming-guide\statements-expressions-operators/lambda-expressions.md)   
 [Expression Trees](../Topic/Expression%20Trees%20\(C%23%20and%20Visual%20Basic\).md)