---
title: "类型约束“&lt;expression&gt;”不是类或接口 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc32048"
  - "vbc32048"
helpviewer_keywords: 
  - "BC32048"
ms.assetid: 68811886-44ac-43e1-9315-b39857310033
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 类型约束“&lt;expression&gt;”不是类或接口
约束列表包含的表达式不表示对类型形参的有效约束。  
  
 约束列表对传递给类型形参的类型实参有一定要求。 你可以采用任意组合指定以下要求：  
  
-   该类型实参必须实现一个或多个接口  
  
-   该类型实参最多从一个类继承  
  
-   类型实参必须公开一个创建代码可以访问的无形参构造函数  
  
-   类型实参必须是引用类型或值类型  
  
 **错误 ID：**BC32048  
  
### 更正此错误  
  
-   验证表达式及其元素是否拼写正确。  
  
-   如果表达式不符合前面列出的要求，请从约束列表中将其删除。  
  
-   如果表达式引用接口或类，请验证编译器是否有权访问该接口或类。 可能需要限定其名称，并可能需要添加一个项目引用。 有关详细信息，请参见 [NOTINBUILD：当多个变量具有相同名称时解析引用](http://msdn.microsoft.com/zh-cn/9601e39f-1911-44e1-ace5-3f6e090408b9)中的“项目引用”。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [值类型和引用类型](/dotnet/visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types)   
 [NOTINBUILD 如何：限定已声明的元素名称](http://msdn.microsoft.com/zh-cn/6bd112f5-df6f-42b8-9427-a9225bfcbaab)   
 [How to: Add and Remove Project References](http://msdn.microsoft.com/zh-cn/f51b784d-0bc8-4c19-a898-e560d5ed696b)