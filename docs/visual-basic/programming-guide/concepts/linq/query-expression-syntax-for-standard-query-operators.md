---
title: "Query Expression Syntax for Standard Query Operators (Visual Basic)"
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
ms.assetid: eb978d86-d3b5-497b-95ce-a054bea8f510
caps.latest.revision: 3
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Query Expression Syntax for Standard Query Operators (Visual Basic)
Some of the more frequently used standard query operators have dedicated Visual Basic language keyword syntax that enables them to be called as part of a *query expression*. A query expression is a different, more readable form of expressing a query than its *method-based*  equivalent. Query expression clauses are translated into calls to the query methods at compile time.  
  
## Query Expression Syntax Table  
 The following table lists the standard query operators that have equivalent query expression clauses.  
  
|Method|Visual Basic Query Expression Syntax|  
|------------|------------------------------------------|  
|<xref:System.Linq.Enumerable.All*>|`Aggregate … In … Into All(…)`<br /><br /> (For more information, see [Aggregate Clause](../../../../visual-basic\language-reference\queries/aggregate-clause.md).)|  
|<xref:System.Linq.Enumerable.Any*>|`Aggregate … In … Into Any()`<br /><br /> (For more information, see [Aggregate Clause](../../../../visual-basic\language-reference\queries/aggregate-clause.md).)|  
|<xref:System.Linq.Enumerable.Average*>|`Aggregate … In … Into Average()`<br /><br /> (For more information, see [Aggregate Clause](../../../../visual-basic\language-reference\queries/aggregate-clause.md).)|  
|<xref:System.Linq.Enumerable.Cast*>|`From … As …`<br /><br /> (For more information, see [From Clause](../../../../visual-basic\language-reference\queries/from-clause.md).)|  
|<xref:System.Linq.Enumerable.Count*>|`Aggregate … In … Into Count()`<br /><br /> (For more information, see [Aggregate Clause](../../../../visual-basic\language-reference\queries/aggregate-clause.md).)|  
|<xref:System.Linq.Enumerable.Distinct``1(System.Collections.Generic.IEnumerable{``0})>|`Distinct`<br /><br /> (For more information, see [Distinct Clause](../../../../visual-basic\language-reference\queries/distinct-clause.md).)|  
|<xref:System.Linq.Enumerable.GroupBy*>|`Group … By … Into …`<br /><br /> (For more information, see [Group By Clause](../../../../visual-basic\language-reference\queries/group-by-clause.md).)|  
|<xref:System.Linq.Enumerable.GroupJoin``4(System.Collections.Generic.IEnumerable{``0},System.Collections.Generic.IEnumerable{``1},System.Func{``0,``2},System.Func{``1,``2},System.Func{``0,System.Collections.Generic.IEnumerable{``1},``3})>|`Group Join … In … On …`<br /><br /> (For more information, see [Group Join Clause](../../../../visual-basic\language-reference\queries/group-join-clause.md).)|  
|<xref:System.Linq.Enumerable.Join``4(System.Collections.Generic.IEnumerable{``0},System.Collections.Generic.IEnumerable{``1},System.Func{``0,``2},System.Func{``1,``2},System.Func{``0,``1,``3})>|`From x In …, y In … Where x.a = b.a`<br /><br /> -or-<br /><br /> `Join … [As …]In … On …`<br /><br /> (For more information, see [Join Clause](../../../../visual-basic\language-reference\queries/join-clause.md).)|  
|<xref:System.Linq.Enumerable.LongCount*>|`Aggregate … In … Into LongCount()`<br /><br /> (For more information, see [Aggregate Clause](../../../../visual-basic\language-reference\queries/aggregate-clause.md).)|  
|<xref:System.Linq.Enumerable.Max*>|`Aggregate … In … Into Max()`<br /><br /> (For more information, see [Aggregate Clause](../../../../visual-basic\language-reference\queries/aggregate-clause.md).)|  
|<xref:System.Linq.Enumerable.Min*>|`Aggregate … In … Into Min()`<br /><br /> (For more information, see [Aggregate Clause](../../../../visual-basic\language-reference\queries/aggregate-clause.md).)|  
|<xref:System.Linq.Enumerable.OrderBy``2(System.Collections.Generic.IEnumerable{``0},System.Func{``0,``1})>|`Order By`<br /><br /> (For more information, see [Order By Clause](../../../../visual-basic\language-reference\queries/order-by-clause.md).)|  
|<xref:System.Linq.Enumerable.OrderByDescending``2(System.Collections.Generic.IEnumerable{``0},System.Func{``0,``1})>|`Order By … Descending`<br /><br /> (For more information, see [Order By Clause](../../../../visual-basic\language-reference\queries/order-by-clause.md).)|  
|<xref:System.Linq.Enumerable.Select*>|`Select`<br /><br /> (For more information, see [Select Clause](../../../../visual-basic\language-reference\queries/select-clause.md).)|  
|<xref:System.Linq.Enumerable.SelectMany*>|Multiple `From` clauses<br /><br /> (For more information, see [From Clause](../../../../visual-basic\language-reference\queries/from-clause.md).)|  
|<xref:System.Linq.Enumerable.Skip*>|`Skip`<br /><br /> (For more information, see [Skip Clause](../../../../visual-basic\language-reference\queries/skip-clause.md).)|  
|<xref:System.Linq.Enumerable.SkipWhile*>|`Skip While`<br /><br /> (For more information, see [Skip While Clause](../../../../visual-basic\language-reference\queries/skip-while-clause.md).)|  
|<xref:System.Linq.Enumerable.Sum*>|`Aggregate … In … Into Sum()`<br /><br /> (For more information, see [Aggregate Clause](../../../../visual-basic\language-reference\queries/aggregate-clause.md).)|  
|<xref:System.Linq.Enumerable.Take*>|`Take`<br /><br /> (For more information, see [Take Clause](../../../../visual-basic\language-reference\queries/take-clause.md).)|  
|<xref:System.Linq.Enumerable.TakeWhile*>|`Take While`<br /><br /> (For more information, see [Take While Clause](../../../../visual-basic\language-reference\queries/take-while-clause.md).)|  
|<xref:System.Linq.Enumerable.ThenBy``2(System.Linq.IOrderedEnumerable{``0},System.Func{``0,``1})>|`Order By …, …`<br /><br /> (For more information, see [Order By Clause](../../../../visual-basic\language-reference\queries/order-by-clause.md).)|  
|<xref:System.Linq.Enumerable.ThenByDescending``2(System.Linq.IOrderedEnumerable{``0},System.Func{``0,``1})>|`Order By …, … Descending`<br /><br /> (For more information, see [Order By Clause](../../../../visual-basic\language-reference\queries/order-by-clause.md).)|  
|<xref:System.Linq.Enumerable.Where*>|`Where`<br /><br /> (For more information, see [Where Clause](../../../../visual-basic\language-reference\queries/where-clause.md).)|  
  
## See Also  
 <xref:System.Linq.Enumerable>   
 <xref:System.Linq.Queryable>   
 [Standard Query Operators Overview (Visual Basic)](../../../../visual-basic\programming-guide\concepts\linq/standard-query-operators-overview.md)   
 [Classification of Standard Query Operators by Manner of Execution (Visual Basic)](../../../../visual-basic\programming-guide\concepts\linq/classification-of-standard-query-operators-by-manner-of-execution.md)