---
title: "调用另一个构造函数时引用尚未完成的对象是无效的 | Microsoft Docs"
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
  - "bc31095"
  - "vbc31095"
helpviewer_keywords: 
  - "BC31095"
ms.assetid: 68be49f1-e662-45c7-9998-e0006324535d
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 调用另一个构造函数时引用尚未完成的对象是无效的
在对象的构造函数完成对象创建之前，已引用对象成员。  
  
 **错误 ID：**BC31095  
  
### 更正此错误  
  
-   从一个构造函数调用另一个构造函数时，请勿使用 `MyBase`、`MyClass` 或 `Me`。  
  
## 请参阅  
 [对象生存期：如何创建和销毁对象](../Topic/Object%20Lifetime:%20How%20Objects%20Are%20Created%20and%20Destroyed%20\(Visual%20Basic\).md)   
 [不在生成中：使用构造函数和析构函数](http://msdn.microsoft.com/zh-cn/548eebe1-86c4-4377-b2f5-447cb8be3d90)