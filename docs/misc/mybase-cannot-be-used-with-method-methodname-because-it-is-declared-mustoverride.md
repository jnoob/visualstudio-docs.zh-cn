---
title: "&quot;MyBase&quot; 不能和方法“&lt;methodname&gt;”一起使用，因为后者被声明为 &quot;MustOverride&quot; | Microsoft Docs"
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
  - "vbc30399"
  - "bc30399"
helpviewer_keywords: 
  - "BC30399"
ms.assetid: 09a30219-a07c-425f-be03-36fc38c04cb0
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &quot;MyBase&quot; 不能和方法“&lt;methodname&gt;”一起使用，因为后者被声明为 &quot;MustOverride&quot;
试图在声明为 `MustOverride` 的方法中使用 `MyBase`。  
  
 **错误 ID：**BC30399  
  
### 更正此错误  
  
-   删除 `MustOverride` 声明。  
  
## 请参阅  
 [MyBase \- delete](http://msdn.microsoft.com/zh-cn/52491d06-6451-4f6f-9aa6-8fab59bbc2b9)   
 [MustOverride](/dotnet/visual-basic/language-reference/modifiers/mustoverride)