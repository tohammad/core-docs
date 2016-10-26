---
title: "How to: Filter on Element Names (LINQ to XML) (Visual Basic)"
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
ms.assetid: b1437b4a-48aa-4546-834a-d6d3ab015fe1
caps.latest.revision: 3
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Filter on Element Names (LINQ to XML) (Visual Basic)
When you call one of the methods that return <xref:System.Collections.Generic.IEnumerable`1> of <xref:System.Xml.Linq.XElement>, you can filter on the element name.  
  
## Example  
 This example retrieves a collection of descendants that is filtered to contain only descendants with the specified name.  
  
 This example uses the following XML document: [Sample XML File: Typical Purchase Order (LINQ to XML)](../../../../visual-basic\programming-guide\concepts\linq/sample-xml-file-typical-purchase-order-linq-to-xml.md).  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
 This code produces the following output:  
  
<CodeContentPlaceHolder>1</CodeContentPlaceHolder>  
 The other methods that return <xref:System.Collections.Generic.IEnumerable`1> of <xref:System.Xml.Linq.XElement> collections follow the same pattern. Their signatures are similar to <xref:System.Xml.Linq.XContainer.Elements*> and <xref:System.Xml.Linq.XContainer.Descendants*>. The following is the complete list of methods that have similar method signatures:  
  
-   <xref:System.Xml.Linq.XNode.Ancestors*>  
  
-   <xref:System.Xml.Linq.XContainer.Descendants*>  
  
-   <xref:System.Xml.Linq.XContainer.Elements*>  
  
-   <xref:System.Xml.Linq.XNode.ElementsAfterSelf*>  
  
-   <xref:System.Xml.Linq.XNode.ElementsBeforeSelf*>  
  
-   <xref:System.Xml.Linq.XElement.AncestorsAndSelf*>  
  
-   <xref:System.Xml.Linq.XElement.DescendantsAndSelf*>  
  
## Example  
 The following example shows the same query for XML that is in a namespace. For more information, see [Working with XML Namespaces (Visual Basic)](../../../../visual-basic\programming-guide\concepts\linq/working-with-xml-namespaces.md).  
  
 This example uses the following XML document: [Sample XML File: Typical Purchase Order in a Namespace](../../../../visual-basic\programming-guide\concepts\linq/sample-xml-file-typical-purchase-order-in-a-namespace.md).  
  
```vb  
Imports <xmlns:aw="http://www.adventure-works.com">  
  
Module Module1  
    Sub Main()  
        Dim po As XElement = XElement.Load("PurchaseOrderInNamespace.xml")  
        Dim items As IEnumerable(Of XElement) = _  
            From el In po...<aw:ProductName> _  
            Select el  
        For Each prdName As XElement In items  
            Console.WriteLine(prdName.Name.ToString & ":" & prdName.Value)  
        Next  
    End Sub  
End Module  
```  
  
 This code produces the following output:  
  
```  
{http://www.adventure-works.com}ProductName:Lawnmower  
{http://www.adventure-works.com}ProductName:Baby Monitor  
```  
  
## See Also  
 [LINQ to XML Axes (Visual Basic)](../../../../visual-basic\programming-guide\concepts\linq/linq-to-xml-axes.md)