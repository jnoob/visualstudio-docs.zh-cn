---
title: "编译器错误 CS0185 | Microsoft Docs"
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
  - "CS0185"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0185"
ms.assetid: d6546e10-0af3-4860-8e6f-2da7dbeb3d28
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0185
“type”不是 lock 语句要求的引用类型  
  
 [lock](/dotnet/csharp/language-reference/keywords/lock-statement) 语句只能评估引用类型。 有关详细信息，请参阅[线程同步](../Topic/Thread%20Synchronization%20\(C%23%20and%20Visual%20Basic\).md)和[引用类型](/dotnet/csharp/language-reference/keywords/reference-types)。  
  
## 示例  
 以下示例生成 CS0185：  
  
```  
// CS0185.cs public class MainClass { public static void Main () { lock (1)   // CS0185 // try the following lines instead // MainClass x = new MainClass(); // lock(x) { } } }  
```