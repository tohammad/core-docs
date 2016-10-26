---
title: "How to: Find the Immediate Preceding Sibling (XPath-LINQ to XML) (C#)"
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
ms.assetid: 74c06201-0b1b-4b5e-b3ac-0092980614e6
caps.latest.revision: 3
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# How to: Find the Immediate Preceding Sibling (XPath-LINQ to XML) (C#)
Sometimes you want to find the immediate preceding sibling to a node. Due to the difference in the semantics of positional predicates for the preceding sibling axes in XPath as opposed to [!INCLUDE[sqltecxlinq](../../../../csharp\programming-guide\concepts\linq/includes/sqltecxlinq_md.md)], this is one of the more interesting comparisons.  
  
## Example  
 In this example, the [!INCLUDE[sqltecxlinq](../../../../csharp\programming-guide\concepts\linq/includes/sqltecxlinq_md.md)] query uses the <xref:System.Linq.Enumerable.Last*> operator to find the last node in the collection returned by <xref:System.Xml.Linq.XNode.ElementsBeforeSelf*>. By contrast, the XPath expression uses a predicate with a value of 1 to find the immediately preceding element.  
  
```c#  
XElement root = XElement.Parse(  
    @"<Root>  
    <Child1/>  
    <Child2/>  
    <Child3/>  
    <Child4/>  
</Root>");  
XElement child4 = root.Element("Child4");  
  
// LINQ to XML query  
XElement el1 =  
    child4  
    .ElementsBeforeSelf()  
    .Last();  
  
// XPath expression  
XElement el2 =  
    ((IEnumerable)child4  
                 .XPathEvaluate("preceding-sibling::*[1]"))  
                 .Cast<XElement>()  
                 .First();  
  
if (el1 == el2)  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
Console.WriteLine(el1);  
```  
  
 This example produces the following output:  
  
```  
Results are identical  
<Child3 />  
```  
  
## See Also  
 [LINQ to XML for XPath Users (C#)](../../../../csharp\programming-guide\concepts\linq/linq-to-xml-for-xpath-users.md)