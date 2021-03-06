---
title: "属性没有 &quot;As&quot; 子句；假定为 Object 类型 | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "BC42022"
  - "vbc42022"
helpviewer_keywords: 
  - "BC42022"
ms.assetid: 3379692b-8278-4488-878a-0afb76e554b1
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 属性没有 &quot;As&quot; 子句；假定为 Object 类型
属性声明未指定 `As` 子句。  
  
 `As` 子句标识要与编程元素关联的数据类型。 在 [Property 语句](/dotnet/visual-basic/language-reference/statements/property-statement)中，它指定属性的 `Get` 过程返回到调用代码的值的数据类型。 如果在 `Property` 语句中不包含 `As` 子句，则属性的数据类型默认为 `Object`。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的详细信息，请参阅 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC42022  
  
### 更正此错误  
  
-   在 `Property` 语句中包含一个 `As` 子句以指定属性的数据类型。  
  
## 请参阅  
 [Property 过程](/dotnet/visual-basic/programming-guide/language-features/procedures/property-procedures)   
 [Property 语句](/dotnet/visual-basic/language-reference/statements/property-statement)   
 [Get 语句](/dotnet/visual-basic/language-reference/statements/get-statement)