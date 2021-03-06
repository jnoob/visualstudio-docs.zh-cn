---
title: "XML 元素不能从类型“type”中选择 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc36807"
  - "bc36807"
helpviewer_keywords: 
  - "BC36807"
ms.assetid: 01c19899-2b44-41e9-a99c-35edfa0deaf1
caps.latest.revision: 5
caps.handback.revision: 5
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# XML 元素不能从类型“type”中选择
针对不属于类型 <xref:System.Xml.Linq.XElement>、<xref:System.Xml.Linq.XDocument> 或 `IEnumerable(Of XElement)` 的对象引用了一个 XML 子元素。 有关详细信息，请参阅[XML 子轴属性](/dotnet/visual-basic/language-reference/xml-axis/xml-child-axis-property)。  
  
```vb#  
' Generates an error. Dim var = "sample text".<child>  
```  
  
 **错误 ID:** BC36807  
  
### 更正此错误  
  
-   确保正在引用特性的对象被强类型化为 <xref:System.Xml.Linq.XElement><xref:System.Xml.Linq.XDocument> 或 `IEnumerable(Of XElement)`。 下面是一个示例：  
  
    ```vb#  
    Dim elem As XElement = <root> <child /> </root> Dim var = elem.<child>  
    ```  
  
## 请参阅  
 [XML 子轴属性](/dotnet/visual-basic/language-reference/xml-axis/xml-child-axis-property)   
 [XML 轴属性](/dotnet/visual-basic/language-reference/xml-axis/xml-axis-properties)   
 [XML](/dotnet/visual-basic/programming-guide/language-features/xml/index)