---
title: "“ReDim”保留操作数不能为 Nothing | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b857f313-3fc2-4262-a577-88df1718b811
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “ReDim”保留操作数不能为 Nothing
`ReDim` 语句尝试使用 `Preserve` 关键字来更改不是最后一个维度的数组的维度，但未为其操作数提供有效的值。  
  
### 更正此错误  
  
-   将 `Preserve` 操作数更改为有效的值。  
  
## 请参阅  
 [NOTINBUILD Visual Basic 中的数组概述](http://msdn.microsoft.com/zh-cn/ca50e2f2-b4d2-4c57-9169-9abbcc3392d8)   
 [NOTINBUILD Visual Basic 中的多维数组](http://msdn.microsoft.com/zh-cn/d92cad25-07e2-4d79-8ea4-ab269700f5de)   
 [ReDim 语句](/dotnet/visual-basic/language-reference/statements/redim-statement)   
 [Dim 语句](/dotnet/visual-basic/language-reference/statements/dim-statement)   
 [保留 \- 删除](http://msdn.microsoft.com/zh-cn/91badeab-b4e0-48b6-92c9-9f0c8f995d81)