---
title: "“AddressOf”表达式无法转换为“&lt;typename&gt;”，因为“&lt;typename&gt;”不是委托类型 | Microsoft Docs"
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
  - "vbc30581"
  - "bc30581"
helpviewer_keywords: 
  - "BC30581"
ms.assetid: 5db7589a-5456-4b3a-9d6b-93d9157f0484
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “AddressOf”表达式无法转换为“&lt;typename&gt;”，因为“&lt;typename&gt;”不是委托类型
语句试图将 `AddressOf` 表达式转换为不是委托类型的类型。  
  
 `AddressOf` 运算符创建引用特定过程的过程委托实例。`AddressOf` 可用作委托构造函数的操作数，或可用于可由编译器确定委托类型的上下文中。  
  
 **错误 ID：**BC30581  
  
### 更正此错误  
  
-   将目标类型更改为委托类型。  
  
## 请参阅  
 [AddressOf 运算符](/dotnet/visual-basic/language-reference/operators/addressof-operator)   
 [不在生成中：委托和 AddressOf 运算符](http://msdn.microsoft.com/zh-cn/7b2ed932-8598-4355-b2f7-5cedb23ee86f)