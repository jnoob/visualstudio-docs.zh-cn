---
title: "编译器错误 CS0198 | Microsoft Docs"
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
  - "CS0198"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0198"
ms.assetid: 222c20f6-3f7f-4750-9f99-b5e6ae6c1271
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0198
无法给静态只读字段“name”的字段赋值（静态构造函数或变量初始值设定项中除外）  
  
 [readonly](/dotnet/csharp/language-reference/keywords/readonly) 变量必须与构造函数具有相同的[静态](/dotnet/csharp/language-reference/keywords/static)用法，在此构造函数中你要对其进行初始化。 有关详细信息，请参阅[静态构造函数](/dotnet/csharp/programming-guide/classes-and-structs/static-constructors)。  
  
 下面的示例生成 CS0198：  
  
```  
// CS0198.cs class MyClass { public static readonly int TestInt = 6; MyClass() { TestInt = 11;   // CS0198, constructor is not static and readonly field is } public static void Main() { } }  
```