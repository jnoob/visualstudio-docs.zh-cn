---
title: "此继承将导致在 &lt;type1&gt;“&lt;typename1&gt;”及其嵌套 &lt;type2&gt;“&lt;typename2&gt;”之间产生循环依赖项。 | Microsoft Docs"
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
  - "vbc30907"
  - "bc30907"
helpviewer_keywords: 
  - "BC30907"
ms.assetid: 17d4f938-5895-4d33-943e-8abf0ceacdc9
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 此继承将导致在 &lt;type1&gt;“&lt;typename1&gt;”及其嵌套 &lt;type2&gt;“&lt;typename2&gt;”之间产生循环依赖项。
继承结构会导致嵌套类之间的循环依赖关系，即两个相互继承的类。  
  
 以下代码可生成此错误消息。  
  
```  
Public Class c1 Inherits c3.c4 Public Class c2 End Class End Class Public Class c3 Inherits c1.c2 Public Class c4 End Class End Class  
```  
  
 在前面的代码中，类 `c1` 继承自类 `c4`，但 `c4` 嵌套在 `c3` 中，其继承自嵌套在 `c1` 内的 `c2`。  
  
 **错误 ID：**BC30907  
  
### 更正此错误  
  
-   更改继承结构，以便不存在循环依赖。  
  
## 请参阅  
 [继承的基础知识](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)