---
title: "编译器错误 CS1912 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1912"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1912"
ms.assetid: 6205420e-01b9-4470-89f9-5924f1e49108
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1912
成员“name”的初始化重复。  
  
 一个对象初始值设定项仅能对每个成员进行一次初始化。  
  
### 更正此错误  
  
1.  删除对象初始值设定项中对该成员的第二次初始化。  
  
## 示例  
 下面的代码生成 CS1912，因为 `memberA` 被初始化了两次：  
  
```  
// cs1912.cs using System.Linq; public class TestClass { public int memberA { get; set; } public int memberB { get; set; } } public class Test { static void Main() { TestClass tc = new TestClass() { memberA = 5, memberA = 6, memberB = 2}; // CS1912 } }  
```  
  
## 请参阅  
 [对象和集合初始值设定项](/dotnet/csharp/programming-guide/classes-and-structs/object-and-collection-initializers)