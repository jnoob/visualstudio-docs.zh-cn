---
title: "编译器错误 CS1940 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1940"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1940"
ms.assetid: 546e9bba-725d-4ea9-826f-37ec9d832add
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1940
找到源类型“type”的多个查询模式实现。 对“method”的调用不明确。  
  
 当定义了查询方法的多个实现，而编译器无法确定最适合的查询时，则会生成此错误。 在下面的示例中，`Select` 的两个版本具有相同的签名，因为它们都接受同一 `int` 作为输入参数，并且返回值均为 `int`。  
  
### 更正此错误  
  
1.  仅为每个方法提供一个实现。  
  
## 示例  
 以下代码生成 CS1940：  
  
```  
// cs1940.cs using System; //must include explicitly for types defined in 3.5 class Test { public delegate int Dele(int x); int num = 0; public int Select(Func<int, int> d) { return d(this.num); } public int Select(Dele d) // CS1940 { return d(this.num) + 1; } public static void Main() { var q = from x in new Test() select x; } }  
```  
  
## 请参阅  
 [Standard Query Operators Overview](../Topic/Standard%20Query%20Operators%20Overview.md)