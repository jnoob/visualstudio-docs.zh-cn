---
title: "“&lt;membername&gt;”无法实现“&lt;interfacename&gt;.&lt;interfacemembername&gt;”，因为它们在类型参数约束上存在差异 | Microsoft Docs"
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
  - "vbc32078"
  - "BC32078"
helpviewer_keywords: 
  - "BC32078"
ms.assetid: 2c971345-edb4-491e-9202-8eb8286b66f8
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;membername&gt;”无法实现“&lt;interfacename&gt;.&lt;interfacemembername&gt;”，因为它们在类型参数约束上存在差异
泛型事件、属性或过程试图实现接口中定义的类似成员，但它们在类型参数上有不同的约束列表。  
  
 要实现接口成员，实现成员不仅必须与该接口成员的完整签名匹配，还必须与每个参数的传递机制匹配。  
  
 要实现泛型接口成员，实现成员还必须与类型参数的数目以及每个参数的约束列表匹配。  
  
 有关接口的实现的详细信息，请参阅[不在生成中：Implements 关键字和 Implements 语句](http://msdn.microsoft.com/zh-cn/b96560f7-6413-480f-a1e2-f80253bab5be)。  
  
 **错误 ID：**BC32078  
  
### 更正此错误  
  
-   如果打算实现接口成员，可将类型参数约束修改为与该接口成员的类型参数约束完全匹配。  
  
-   如果该类型参数约束必须保持为原有状态，则无法实现此声明中的接口成员。 从声明中删除 [Implements](/dotnet/visual-basic/language-reference/statements/implements-clause) 关键字。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [不在生成中：Visual Basic 中的接口实现示例](http://msdn.microsoft.com/zh-cn/50bf2a30-73b6-4126-a921-075fd6eec278)