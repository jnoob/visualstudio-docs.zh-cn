---
title: "&lt;type1&gt;“&lt;propertyname&gt;”与为基&lt;type2&gt;“&lt;classname&gt;”中的事件“&lt;eventname&gt;”隐式声明的成员冲突 | Microsoft Docs"
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
  - "vbc40014"
  - "bc40014"
helpviewer_keywords: 
  - "BC40014"
ms.assetid: 100534b9-d533-4e94-a2a7-0ed26426965b
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &lt;type1&gt;“&lt;propertyname&gt;”与为基&lt;type2&gt;“&lt;classname&gt;”中的事件“&lt;eventname&gt;”隐式声明的成员冲突
声明的属性与基类中某个事件生成的隐式成员具有相同的名称。 例如，如果该基类定义名为 `Event1` 的事件，编译器将生成 `add_Event1` 和 `remove_Event1` 隐式过程。 如果此类中的属性拥有其中一个名称，它应隐藏基类成员。  
  
 此消息是一个警告。 默认假定 `Shadows`。 有关隐藏警告或将警告视为错误的详细信息，请参见 [在 Visual Basic 中配置警告](../ide/configuring-warnings-in-visual-basic.md)。  
  
 **错误 ID：**BC40014  
  
### 更正此错误  
  
1.  若要隐藏基类成员，请将 `Shadows` 关键字添加到属性声明中。  
  
2.  如果不打算隐藏基类成员，请更改属性名称。  
  
## 请参阅  
 [Property 语句](/dotnet/visual-basic/language-reference/statements/property-statement)   
 [Event 语句](/dotnet/visual-basic/language-reference/statements/event-statement)   
 [Shadows](/dotnet/visual-basic/language-reference/modifiers/shadows)   
 [Visual Basic 中的隐藏](/dotnet/visual-basic/programming-guide/language-features/declared-elements/shadowing)