---
title: "编译器错误 CS0314 | Microsoft Docs"
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
  - "CS0314"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0314"
ms.assetid: 12f68f51-0568-4e80-b0fd-15899807477d
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0314
不能将类型“type1”用作泛型类型或方法“name”中的类型参数“name”。 没有从“type1”到“type2”的装箱转换或类型参数转换。  
  
 当泛型类型使用受约束的类型参数时，新类也必须满足这些相同的约束。  
  
### 更正此错误  
  
1.  在下面的示例中，将 `where T : ClassConstraint` 添加到类 `B` 中。  
  
## 示例  
 下面的代码生成 CS0314：  
  
```  
// cs0314.cs // Compile with: /target:library public class ClassConstraint { } public class A<T> where T : ClassConstraint { } public class B<T> : A<T> //CS0314 { } // Try using this instead. public class C<T> : A<T> where T : ClassConstraint { }  
```  
  
## 请参阅  
 [类型参数的约束](/dotnet/csharp/programming-guide/generics/constraints-on-type-parameters)