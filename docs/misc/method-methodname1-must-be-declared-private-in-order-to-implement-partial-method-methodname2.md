---
title: "方法“&lt;methodname1&gt;”必须声明为“Private”才能实现分部方法“&lt;methodname2&gt;” | Microsoft Docs"
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
  - "vbc31441"
  - "bc31441"
helpviewer_keywords: 
  - "BC31441"
ms.assetid: 4d8d19ad-0c3b-4eba-ada8-2cfa6ae795c4
caps.latest.revision: 5
caps.handback.revision: 5
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 方法“&lt;methodname1&gt;”必须声明为“Private”才能实现分部方法“&lt;methodname2&gt;”
分部方法的实现必须声明为 `Private`。 例如，下面的代码会导致此错误。  
  
```vb#  
Partial Class Product ' Declaration of the partial method. Partial Private Sub valueChanged() End Sub End Class  
```  
  
```vb#  
Partial Class Product ' Implementation of the partial method, with Private missing, ' causes this error. 'Sub valueChanged() '    MsgBox(Value was changed to " & Me.Quantity) 'End Sub End Class  
```  
  
 **错误 ID：**BC31441  
  
### 更正此错误  
  
1.  在分部方法的实现中使用访问修饰符 `Private`，如以下示例中所示。  
  
    ```vb#  
    Private Sub valueChanged() MsgBox(Value was changed to " & Me.Quantity) End Sub  
    ```  
  
## 请参阅  
 [分部方法](/dotnet/visual-basic/programming-guide/language-features/procedures/partial-methods)   
 [Visual Basic 中的访问级别](/dotnet/visual-basic/programming-guide/language-features/declared-elements/access-levels)