---
title: "参数“&lt;argumentname&gt;”必须在 0 到 99 的范围内 | Microsoft Docs"
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
  - "vbrArgument_Range0to99_1"
ms.assetid: d9d9a15e-c5ee-4104-9504-b48a4a191415
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 参数“&lt;argumentname&gt;”必须在 0 到 99 的范围内
参数无效，因为它超出了 0 到 99 的范围。  
  
### 更正此错误  
  
1.  检查表达式中参数的拼写是否正确。 拼写错误的变量名可能会隐式创建一个初始化为零的数值变量。  
  
2.  检查之前对表达式中的变量进行的操作，尤其是那些从其他过程作为参数传递给该过程的操作。  
  
## 请参阅  
 [通过值和通过引用传递参数](/dotnet/visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference)