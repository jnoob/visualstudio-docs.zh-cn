---
title: "编译器警告（等级 1）CS0688 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0688"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0688"
ms.assetid: 8ce5af36-663e-46e8-87e9-bb32555796ae
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器警告（等级 1）CS0688
“method1”具有链接要求，但会重写或实现不具有链接要求“method2”。 可能存在安全漏洞。  
  
 可通过调用基类方法轻松绕过对派生类方法设置的此链接要求。 要填补此安全漏洞，基类方法需要同样使用此链接要求。 有关详细信息，请参阅[要求与LinkDemand](http://msdn.microsoft.com/zh-cn/1ab877f2-70f4-4e0d-8116-943999dfe8f5)。  
  
## 示例  
 以下示例生成 CS0688。 若要解决此警告而不修改基类，请从重写方法中删除安全特性。 这不会解决安全问题。  
  
```  
// CS0688.cs // compile with: /W:1 using System; using System.Security.Permissions; class Base { //Uncomment the following line to close the security hole //[FileIOPermission(SecurityAction.LinkDemand, All=@"C:\\")] public virtual void DoScaryFileStuff() { } } class Derived: Base { [FileIOPermission(SecurityAction.LinkDemand, All=@"C:\\")] // CS0688 public override void DoScaryFileStuff() { } static void Main() { } }  
```