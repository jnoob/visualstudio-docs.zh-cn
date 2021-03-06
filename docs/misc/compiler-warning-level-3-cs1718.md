---
title: "编译器警告（等级 3）CS1718 | Microsoft Docs"
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
  - "CS1718"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1718"
ms.assetid: 7c1c11fd-4f91-482d-b8f7-efe2a361634e
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器警告（等级 3）CS1718
对同一变量进行比较；是否希望比较其他变量?  
  
 如果要与其他变量进行比较，则只需更正语句。  
  
 但另一种可能是你要测试 True 或 False，并通过如 `if (a == a) (true)` 或 `if (a < a) (false)` 这样的语句来完成此操作。 最好仅表示 `if (true)` 或 `if (false)`。 主要有两个原因：  
  
-   它更简单：总是更清楚地表达你的意思。  
  
-   它有助于避免混淆：C\# 2.0 的一个新功能是可以为 Null 的值类型，这类似于 T\-SQL（SQL Server 使用的编程语言）中的值 `null`。 由于 T\-SQL 中使用了三元逻辑，熟悉 T\-SQL 的开发人员可能会关心可以为 Null 值的类型在类似于 `if (a == a)` 的表达式上的效果。 如果你使用 `true` 或 `false`，就可以避免这类可能出现的混。  
  
## 示例  
 下面的代码生成警告 CS1718。  
  
```  
// CS1718.cs using System; public class Tester { public static void Main() { int i = 0; if (i == i) { // CS1718.cs //if (true) { i++; } } }  
```