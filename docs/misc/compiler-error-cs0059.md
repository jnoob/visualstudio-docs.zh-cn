---
title: "编译器错误 CS0059 | Microsoft Docs"
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
  - "CS0059"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0059"
ms.assetid: 25a8624b-7f7b-4487-ba80-413d57f9132b
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0059
可访问性不一致：参数类型“type”的可访问性低于委托“delegate”  
  
 方法的返回类型和形参表中引用的每个类型都必须至少具有和方法自身相同的可访问性。 有关详细信息，请参阅[访问修饰符](/dotnet/csharp/programming-guide/classes-and-structs/access-modifiers)。  
  
## 示例  
 下面的示例生成 CS0059：  
  
```  
// CS0059.cs class MyClass //defaults to private accessibility // try the following line instead // public class MyClass { } public delegate void MyClassDel( MyClass myClass);   // CS0059 public class Program { public static void Main() { } }  
```