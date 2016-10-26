---
title: "How to: Stream XML Fragments from an XmlReader (C#)"
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
ms.assetid: 4a8f0e45-768a-42e2-bc5f-68bdf0e0a726
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
# How to: Stream XML Fragments from an XmlReader (C#)
When you have to process large XML files, it might not be feasible to load the whole XML tree into memory. This topic shows how to stream fragments using an <xref:System.Xml.XmlReader>.  
  
 One of the most effective ways to use an <xref:System.Xml.XmlReader> to read <xref:System.Xml.Linq.XElement> objects is to write your own custom axis method. An axis method typically returns a collection such as <xref:System.Collections.Generic.IEnumerable`1> of <xref:System.Xml.Linq.XElement>, as shown in the example in this topic. In the custom axis method, after you create the XML fragment by calling the <xref:System.Xml.Linq.XNode.ReadFrom*> method, return the collection using `yield return`. This provides deferred execution semantics to your custom axis method.  
  
 When you create an XML tree from an <xref:System.Xml.XmlReader> object, the <xref:System.Xml.XmlReader> must be positioned on an element. The <xref:System.Xml.Linq.XNode.ReadFrom*> method does not return until it has read the close tag of the element.  
  
 If you want to create a partial tree, you can instantiate an <xref:System.Xml.XmlReader>, position the reader on the node that you want to convert to an <xref:System.Xml.Linq.XElement> tree, and then create the <xref:System.Xml.Linq.XElement> object.  
  
 The topic [How to: Stream XML Fragments with Access to Header Information (C#)](../../../../csharp\programming-guide\concepts\linq/how-to-stream-xml-fragments-with-access-to-header-information.md) contains information and an example on how to stream a more complex document.  
  
 The topic [How to: Perform Streaming Transform of Large XML Documents (C#)](../../../../csharp\programming-guide\concepts\linq/how-to-perform-streaming-transform-of-large-xml-documents.md) contains an example of using LINQ to XML to transform extremely large XML documents while maintaining a small memory footprint.  
  
## Example  
 This example creates a custom axis method. You can query it by using a [!INCLUDE[vbteclinq](../../../../csharp/includes/vbteclinq_md.md)] query. The custom axis method, `StreamRootChildDoc`, is a method that is designed specifically to read a document that has a repeating `Child` element.  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
 This example produces the following output:  
  
<CodeContentPlaceHolder>1</CodeContentPlaceHolder>  
 In this example, the source document is very small. However, even if there were millions of `Child` elements, this example would still have a small memory footprint.  
  
## See Also  
 [Parsing XML (C#)](../../../../csharp\programming-guide\concepts\linq/parsing-xml.md)