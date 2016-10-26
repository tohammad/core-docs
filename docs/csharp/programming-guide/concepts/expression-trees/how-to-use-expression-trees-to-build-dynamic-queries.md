---
title: "How to: Use Expression Trees to Build Dynamic Queries (C#)"
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
ms.assetid: 52cd44dd-a3ec-441e-b93a-4eca388119c7
caps.latest.revision: 3
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# How to: Use Expression Trees to Build Dynamic Queries (C#)
In LINQ, expression trees are used to represent structured queries that target sources of data that implement <xref:System.Linq.IQueryable`1>. For example, the LINQ provider implements the <xref:System.Linq.IQueryable`1> interface for querying relational data stores. The C# compiler compiles queries that target such data sources into code that builds an expression tree at runtime. The query provider can then traverse the expression tree data structure and translate it into a query language appropriate for the data source.  
  
 Expression trees are also used in LINQ to represent lambda expressions that are assigned to variables of type <xref:System.Linq.Expressions.Expression`1>.  
  
 This topic describes how to use expression trees to create dynamic LINQ queries. Dynamic queries are useful when the specifics of a query are not known at compile time. For example, an application might provide a user interface that enables the end user to specify one or more predicates to filter the data. In order to use LINQ for querying, this kind of application must use expression trees to create the LINQ query at runtime.  
  
## Example  
 The following example shows you how to use expression trees to construct a query against an `IQueryable` data source and then execute it. The code builds an expression tree to represent the following query:  
  
 `companies.Where(company => (company.ToLower() == "coho winery" || company.Length > 16)).OrderBy(company => company)`  
  
 The factory methods in the <xref:System.Linq.Expressions> namespace are used to create expression trees that represent the expressions that make up the overall query. The expressions that represent calls to the standard query operator methods refer to the <xref:System.Linq.Queryable> implementations of these methods. The final expression tree is passed to the <xref:System.Linq.IQueryProvider.CreateQuery``1(System.Linq.Expressions.Expression)> implementation of the provider of the `IQueryable` data source to create an executable query of type `IQueryable`. The results are obtained by enumerating that query variable.  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
 This code uses a fixed number of expressions in the predicate that is passed to the `Queryable.Where` method. However, you can write an application that combines a variable number of predicate expressions that depends on the user input. You can also vary the standard query operators that are called in the query, depending on the input from the user.  
  
## Compiling the Code  
  
-   Create a new **Console Application** project.  
  
-   Add a reference to System.Core.dll if it is not already referenced.  
  
-   Include the System.Linq.Expressions namespace.  
  
-   Copy the code from the example and paste it into the `Main` method.  
  
## See Also  
 [Expression Trees (C#)](../../../../csharp\programming-guide\concepts\expression-trees/index.md)   
 [How to: Execute Expression Trees (C#)](../../../../csharp\programming-guide\concepts\expression-trees/how-to-execute-expression-trees.md)   
 [How to: Dynamically Specify Predicate Filters at Runtime](../../../../csharp\programming-guide\linq-query-expressions/how-to-dynamically-specify-predicate-filters-at-runtime.md)