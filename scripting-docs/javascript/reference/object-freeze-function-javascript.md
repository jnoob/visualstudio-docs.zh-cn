---
title: "Object.freeze 函数 (JavaScript) | Microsoft Docs"
ms.custom: ""
ms.date: "01/18/2017"
ms.prod: "windows-client-threshold"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-javascript"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
dev_langs: 
  - "JavaScript"
  - "TypeScript"
  - "DHTML"
helpviewer_keywords: 
  - "freeze 函数"
  - "Object.freeze 函数"
ms.assetid: 83ffe193-0a37-4e0c-9b66-44c422765fb3
caps.latest.revision: 20
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
caps.handback.revision: 20
---
# Object.freeze 函数 (JavaScript)
阻止修改现有属性的特性和值，并阻止添加新属性。  
  
## 语法  
  
```javascript  
Object.freeze(object)  
```  
  
#### 参数  
 `object`  
 必需。  在其上锁定特性的对象。  
  
## 返回值  
 传递给函数的对象。  
  
## 异常  
 如果 `object` 参数不是对象，则将引发 `TypeError` 异常。  
  
## 备注  
 `Object.freeze` 函数执行下面的操作：  
  
-   使对象不可扩展，这样便无法向其添加新属性。  
  
-   为对象的所有属性将 `configurable` 特性设置为 `false`。  在 `configurable` 为 `false` 时，无法更改属性的特性且无法删除属性。  
  
-   为对象的所有数据属性将 `writable` 特性设置为 `false`。  当 `writable` 为 false 时，无法更改数据属性值。  
  
 有关如何设置属性的特性的更多信息，请参见 [Object.defineProperty 函数](../../javascript/reference/object-defineproperty-function-javascript.md)。  若要获取属性的特性，可使用 [Object.getOwnPropertyDescriptor 函数](../../javascript/reference/object-getownpropertydescriptor-function-javascript.md)。  
  
## 相关函数  
 以下相关函数可阻止修改对象的特性。  
  
|函数|对象已设置为不可扩展的|为每个属性将 `configurable` 设置为 `false`|为每个属性将 `writable` 设置为 `false`|  
|--------|-----------------|---------------------------------------|-----------------------------------|  
|[Object.preventExtensions](../../javascript/reference/object-preventextensions-function-javascript.md)|是|否|否|  
|[Object.seal](../../javascript/reference/object-seal-function-javascript.md)|是|是|否|  
|`Object.freeze`|是|是|是|  
  
 如果满足下表中标记的所有条件，则以下函数返回 `true`。  
  
|函数|对象是否可扩展|为所有属性将 `configurable` 设置为 `false`|为所有数据属性将 `writable` 设置为 `false`|  
|--------|-------------|---------------------------------------|-------------------------------------|  
|[Object.isExtensible](../../javascript/reference/object-isextensible-function-javascript.md)|是|否|否|  
|[Object.isSealed](../../javascript/reference/object-issealed-function-javascript.md)|否|是|是|  
|[Object.isFrozen](../../javascript/reference/object-isfrozen-function-javascript.md)|否|是|是|  
  
## 示例  
 下面的示例阐释了 `Object.freeze` 函数的用法。  
  
```javascript  
// Create an object that has two properties.  
var obj = { pasta: "spaghetti", length: 10 };  
  
// Freeze the object.  
Object.freeze(obj);  
  
// Try to add a new property, and then verify that it is not added.   
    obj.newProp = 50;  
    document.write(obj.newProp);  
    document.write("<br/>");  
  
// Try to delete a property, and then verify that it is still present.   
delete obj.length;  
document.write(obj.length);  
document.write("<br/>");  
  
// Try to change a property value, and then verify that it is not changed.   
obj.pasta = "linguini";  
document.write(obj.pasta);  
  
// Output:  
// undefined  
// 10  
// spaghetti  
  
```  
  
## 要求  
 [!INCLUDE[jsv9](../../javascript/includes/jsv9-md.md)]  
  
## 请参阅  
 [Object.preventExtensions 函数](../../javascript/reference/object-preventextensions-function-javascript.md)   
 [Object.seal 函数](../../javascript/reference/object-seal-function-javascript.md)   
 [Object.isExtensible 函数](../../javascript/reference/object-isextensible-function-javascript.md)   
 [Object.isSealed 函数](../../javascript/reference/object-issealed-function-javascript.md)   
 [Object.isFrozen 函数](../../javascript/reference/object-isfrozen-function-javascript.md)