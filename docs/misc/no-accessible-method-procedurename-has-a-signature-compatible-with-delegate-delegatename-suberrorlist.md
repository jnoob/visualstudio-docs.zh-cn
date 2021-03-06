---
title: "没有可访问的方法“&lt;procedurename&gt;”的签名与委托“&lt;delegatename&gt;”:&lt;suberrorlist&gt; 兼容 | Microsoft Docs"
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
  - "bc30950"
  - "vbc30950"
helpviewer_keywords: 
  - "BC30950"
ms.assetid: c1938099-2c03-491e-b599-d0c43bf94baf
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 没有可访问的方法“&lt;procedurename&gt;”的签名与委托“&lt;delegatename&gt;”:&lt;suberrorlist&gt; 兼容
赋值语句将过程的地址赋给一个委托变量，但编译器无法找到具有匹配签名的过程的版本。  
  
 当代码使用过程的地址时，编译器将尝试查找具有与该委托的参数列表相匹配的参数列表的过程的版本。 如果在多个重载版本中定义该过程，则编译器将尝试查找具有匹配签名的单个版本。 有关更多信息，请参见[重载决策](/dotnet/visual-basic/programming-guide/language-features/procedures/overload-resolution)。  
  
 如果编译器无法找到具有匹配签名的过程的任何版本，将生成此错误。 例如，如果该过程或委托为泛型，且向其传递一个会提供给它与其他签名不匹配的签名的类型参数，可能会发生这种情况。  
  
 **错误 ID：**BC30950  
  
### 更正此错误  
  
1.  重新定义过程或委托，以便它们具有匹配的参数列表。  
  
     \- 或 \-  
  
     定义一个具有与过程的参数列表相匹配的参数列表的新委托，或者定义一个具有与委托的参数列表相匹配的参数列表的新过程。  
  
2.  如果该过程或委托为泛型，然后向其传递一个会导致它的签名与其他签名匹配的类型参数。  
  
## 请参阅  
 [AddressOf 运算符](/dotnet/visual-basic/language-reference/operators/addressof-operator)   
 [Delegate 语句](/dotnet/visual-basic/language-reference/statements/delegate-statement)   
 [不在生成中：委托和 AddressOf 运算符](http://msdn.microsoft.com/zh-cn/7b2ed932-8598-4355-b2f7-5cedb23ee86f)   
 [重载决策](/dotnet/visual-basic/programming-guide/language-features/procedures/overload-resolution)   
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)