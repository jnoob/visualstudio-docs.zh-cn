---
title: "&lt;error&gt;：“&lt;constructorname1&gt;”调用“&lt;constructorname2&gt;” | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30297"
  - "bc30297"
helpviewer_keywords: 
  - "BC30297"
ms.assetid: dfca67d7-f4d7-4451-a937-68f22b8527d5
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;error&gt;：“&lt;constructorname1&gt;”调用“&lt;constructorname2&gt;”
发生循环构造函数调用。 构造函数将调用 `Me.New()` 或 `MyClass.New()`。 一个可能的原因是尝试调用具有不同参数列表的重载构造函数。  
  
 **错误 ID：**BC30297  
  
### 更正此错误  
  
-   使用不同的参数列表调用重载构造函数。  
  
-   如果没有可访问的重载，则删除对 `Me.New()` 或 `MyClass.New()` 的调用。  
  
## 请参阅  
 [不在生成中：使用构造函数和析构函数](http://msdn.microsoft.com/zh-cn/548eebe1-86c4-4377-b2f5-447cb8be3d90)