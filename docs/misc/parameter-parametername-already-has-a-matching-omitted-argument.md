---
title: "形参“&lt;parametername&gt;”已有匹配的已省略实参 | Microsoft Docs"
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
  - "vbc36566"
  - "bc36566"
helpviewer_keywords: 
  - "BC36566"
ms.assetid: b37af6bc-abd0-4436-bf8a-a467e3603342
caps.latest.revision: 6
caps.handback.revision: 6
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 形参“&lt;parametername&gt;”已有匹配的已省略实参
按位置省略了一个参数后，过程调用又按名称提供了同一个参数。 下面是一个示例：  
  
```vb#  
Public Sub ABC(ByVal X As Byte, Optional ByVal Y As Byte = 0, _ Optional ByVal Z As Byte = 0) ' ... ' Argument Y is omitted by position, but supplied by name. Call ABC(6, , Y:=3)     
```  
  
 **错误 ID：**BC36566  
  
### 更正此错误  
  
-   按位置提供参数，或删除省略它的逗号。  
  
## 请参阅  
 [按位置和按名称传递参数](/dotnet/visual-basic/programming-guide/language-features/procedures/passing-arguments-by-position-and-by-name)