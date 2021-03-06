---
title: "没有为类型“&lt;typename1&gt;”和“&lt;typename2&gt;”定义运算符“&lt;operatorname&gt;” | Microsoft Docs"
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
  - "vbc31080"
  - "bc31080"
helpviewer_keywords: 
  - "BC31080"
ms.assetid: d2f77450-2bf2-4b1e-b95f-dbc7878f2777
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 没有为类型“&lt;typename1&gt;”和“&lt;typename2&gt;”定义运算符“&lt;operatorname&gt;”
没有为类型“\<typename1\>”和“\<typename2\>”定义运算符“\<operatorname\>”。 使用“Is”运算符比较两个引用类型。  
  
 试图以对指定类型不适合的方式使用运算符。 在使用“\=”运算符而不是 `Is` 运算符比较两个对象时，可能会导致此错误。  
  
 **错误 ID：**BC31080  
  
### 更正此错误  
  
1.  使用 `Is` 运算符比较两个引用类型。  
  
2.  将 `Not` 运算符与 `Is` 运算符一起使用以表示不相等。 例如:  
  
     [!code-vb[VbVbalrOOP#89](../misc/codesnippet/VisualBasic/operator-operatorname-is-not-defined-for-types-typename1-and-typename2_1.vb)]  
  
## 请参阅  
 [Is 运算符](/dotnet/visual-basic/language-reference/operators/is-operator)   
 [\= 运算符](/dotnet/visual-basic/language-reference/operators/assignment-operator)   
 [Not 运算符](/dotnet/visual-basic/language-reference/operators/not-operator)