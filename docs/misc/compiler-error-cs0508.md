---
title: "编译器错误 CS0508 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0508"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0508"
ms.assetid: 28403573-6e64-4496-918d-fb50c8851e51
caps.latest.revision: 10
caps.handback.revision: 10
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0508
“Type1”：返回类型必须为“Type2”才能匹配重写的成员“MemberName”  
  
 试图更改方法重写中的返回类型。 若要解决此错误，请确保这两种方法声明相同的返回类型。  
  
## 示例  
 下面的示例生成 CS0508。  
  
```  
// CS0508.cs // compile with: /target:library abstract public class Clx { public int i = 0; // Return type is int. abstract public int F(); } public class Cly : Clx { public override double F() { return 0.0;   // CS0508 } }  
```