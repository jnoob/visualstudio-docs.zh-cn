---
title: "Idiaenumframedata:: Framebyrva |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaEnumFrameData::frameByRVA method
ms.assetid: 4b8dec05-e76c-4cc4-9644-2369d583849f
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: fbfadc19b1da36ce7e1fc261e48d0fe5d5ecf200
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="idiaenumframedataframebyrva"></a>IDiaEnumFrameData::frameByRVA
按相对虚拟地址 (RVA) 返回帧。  
  
## <a name="syntax"></a>语法  
  
```C++  
HRESULT frameByRVA(   
   DWORD           relativeVirtualAddress,  
   IDiaFrameData** frame  
);  
```  
  
#### <a name="parameters"></a>参数  
 relativeVirtualAddress  
 [in]感兴趣的帧的 RVA。  
  
 框架  
 [out]返回[IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)对象表示包含提供的地址的帧。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`。 返回`S_FALSE`如果任何帧数据与指定的地址不匹配。 否则，返回错误代码。  
  
## <a name="see-also"></a>请参阅  
 [IDiaEnumFrameData](../../debugger/debug-interface-access/idiaenumframedata.md)   
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)