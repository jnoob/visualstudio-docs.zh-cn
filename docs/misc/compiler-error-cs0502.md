---
title: "编译器错误 CS0502 | Microsoft Docs"
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
  - "CS0502"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0502"
ms.assetid: 6cd6deda-73a1-42d8-893b-45a685e63380
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0502
“member”不能既是抽象的又是密封的  
  
 类成员不能既是[抽象的](/dotnet/csharp/language-reference/keywords/abstract)又是[密封的](/dotnet/csharp/language-reference/keywords/sealed)。  
  
 下面的示例生成 CS0502：  
  
```  
// CS0502.cs public class B { abstract public void F(); } public class C : B { abstract sealed override public void F()   // CS0502 { } } public class CMain { public static void Main() { } }  
```