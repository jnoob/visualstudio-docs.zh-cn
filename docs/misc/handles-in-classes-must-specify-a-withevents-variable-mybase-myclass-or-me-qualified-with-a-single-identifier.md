---
title: "类中的“Handles”必须指定用单个标识符限定的“WithEvents”变量、“MyBase”、“MyClass”或“Me” | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc31412"
  - "vbc31412"
helpviewer_keywords: 
  - "BC31412"
ms.assetid: acbefc38-448a-4afa-90c2-77389415d618
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 类中的“Handles”必须指定用单个标识符限定的“WithEvents”变量、“MyBase”、“MyClass”或“Me”
若要指定事件处理程序，`Handles` 语句必须指定用 `WithEvents` 关键字声明的对象变量，或通过 `MyBase` 关键字限定的成员。  
  
 **错误 ID：**BC31412  
  
### 更正此错误  
  
1.  使用 `WithEvents` 修饰符来声明要用于 `Handles` 语句的变量。  
  
2.  为基类中的当前类指定事件名称。  
  
## 请参阅  
 [Handles](/dotnet/visual-basic/language-reference/statements/handles-clause)   
 [WithEvents](/dotnet/visual-basic/language-reference/modifiers/withevents)   
 [事件](/dotnet/visual-basic/programming-guide/language-features/events/events)