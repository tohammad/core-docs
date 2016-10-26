---
title: "LINQ to XML Annotations2"
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
ms.assetid: c3e8b3ff-fceb-4428-b0ca-1ed6f128aac8
caps.latest.revision: 3
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# LINQ to XML Annotations
Annotations in [!INCLUDE[sqltecxlinq](../../../../csharp\programming-guide\concepts\linq/includes/sqltecxlinq_md.md)] enable you to associate any arbitrary object of any arbitrary type with any XML component in an XML tree.  
  
 To add an annotation to an XML component, such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XAttribute>, you call the <xref:System.Xml.Linq.XObject.AddAnnotation*> method. You retrieve annotations by type.  
  
 Note that annotations are not part of the XML infoset; they are not serialized or deserialized.  
  
## Methods  
 You can use the following methods when working with annotations:  
  
|Method|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XObject.AddAnnotation*>|Adds an object to the annotation list of an <xref:System.Xml.Linq.XObject>.|  
|<xref:System.Xml.Linq.XObject.Annotation*>|Gets the first annotation object of the specified type from an <xref:System.Xml.Linq.XObject>.|  
|<xref:System.Xml.Linq.XObject.Annotations*>|Gets a collection of annotations of the specified type for an <xref:System.Xml.Linq.XObject>.|  
|<xref:System.Xml.Linq.XObject.RemoveAnnotations*>|Removes the annotations of the specified type from an <xref:System.Xml.Linq.XObject>.|  
  
## See Also  
 [Advanced LINQ to XML Programming (Visual Basic)](../../../../visual-basic\programming-guide\concepts\linq/advanced-linq-to-xml-programming.md)