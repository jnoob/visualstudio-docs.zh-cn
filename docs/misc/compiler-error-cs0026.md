---
title: "编译器错误 CS0026 | Microsoft Docs"
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
  - "CS0026"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0026"
ms.assetid: 8767fbc1-8ba7-4e88-a9f9-7e620411882b
caps.latest.revision: 12
caps.handback.revision: 12
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0026
关键字 "this" 在静态属性、静态方法或静态字段初始值设定项中无效  
  
 [this](/dotnet/csharp/language-reference/keywords/this) 关键字是指一个对象，其为某类型的实例。 由于静态方法与包含类的任何实例均无关，因此“this”关键字不含任何意义，因此不受允许。 有关详细信息，请参阅[静态类和静态类成员](/dotnet/csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members)和[对象](/dotnet/csharp/programming-guide/classes-and-structs/objects)。  
  
## 示例  
 下面的示例生成 CS0026：  
  
```  
// CS0026.cs public class A { public static int i = 0; public static void Main() { // CS0026 this.i = this.i + 1; // Try the following line instead: // i = i + 1; } }  
```