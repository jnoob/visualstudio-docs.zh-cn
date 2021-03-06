---
title: "编译器错误 CS0273 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0273"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0273"
ms.assetid: 851ad056-feee-48fd-834c-578a1a13e926
caps.latest.revision: 13
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0273
“property\_accessor”访问器的可访问性修饰符必须比属性或索引器“property”的限制性更强  
  
 Set\/get 访问器的可访问性修饰符必须比属性或索引器“property\/indexer”的限制性更强  
  
 在使用限制性比其某个访问器上访问修饰符低的访问修饰符声明属性或索引器时，将出现此错误。 若要解决此错误，请在属性或 set 访问器上使用适当的访问修饰符。 有关详细信息，请参阅[访问器可访问性](/dotnet/csharp/programming-guide/classes-and-structs/restricting-accessor-accessibility)。  
  
## 示例  
 此示例包含具有内部 set 方法的内部属性。 下面的示例生成 CS0273。  
  
```  
// CS0273.cs // compile with: /target:library public class MyClass { internal int Property { get { return 0; } internal set {}   // CS0273 // try the following line instead // private set {} } }  
```