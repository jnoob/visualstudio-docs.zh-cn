---
title: "编译器错误 CS0623 | Microsoft Docs"
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
  - "CS0623"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0623"
ms.assetid: c9fd6888-b9c5-48bf-b25b-2fae1446ad24
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0623
数组初始值设定项只能在变量或字段初始值设定项中使用。 请尝试改用 new 表达式。  
  
 尝试在某个上下文中使用数组初始值设定项来初始化数组，而该上下文中不允许这样做。  
  
## 示例  
 下面的示例会生成 CS0623，因为编译器会将 \\{4\\} 解释为外部数组初始值设定项中的嵌入式数组初始值设定项：  
  
```  
//cs0632.cs using System; class X { public int[] x = { 2, 3, {4}}; //CS0623 }  
```  
  
## 请参阅  
 [数组](/dotnet/csharp/programming-guide/arrays/index)