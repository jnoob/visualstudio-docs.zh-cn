---
title: "ParamArray 参数必须声明为“ByVal” | Microsoft Docs"
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
  - "vbc30667"
  - "bc30667"
helpviewer_keywords: 
  - "BC30667"
ms.assetid: 583e231f-a4c9-47aa-ae37-7bac43b0b318
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# ParamArray 参数必须声明为“ByVal”
`ParamArray` 参数不能使用 `ByRef` 修饰符。  
  
 **错误 ID：**BC30667  
  
### 更正此错误  
  
-   使用 `ByVal` 修饰符声明 `ParamArray` 参数。  
  
## 请参阅  
 [ParamArray](/dotnet/visual-basic/language-reference/modifiers/paramarray)   
 [ByRef](/dotnet/visual-basic/language-reference/modifiers/byref)   
 [ByVal](/dotnet/visual-basic/language-reference/modifiers/byval)