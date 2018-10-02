---
title: IDebugDisassemblyStream2::GetCodeContext |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugDisassemblyStream2::GetCodeContext
helpviewer_keywords:
- IDebugDisassemblyStream2::GetCodeContext
ms.assetid: a6d0ae82-7617-4915-9713-369abe3e2e53
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c3b3b2c94a778c5684cd1eee2436a8db7dad87f2
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47470875"
---
# <a name="idebugdisassemblystream2getcodecontext"></a>IDebugDisassemblyStream2::GetCodeContext
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

本主题的最新版本，请参阅[IDebugDisassemblyStream2::GetCodeContext](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugdisassemblystream2-getcodecontext)。  
  
返回与指定的代码位置标识符相对应的代码上下文对象。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
HRESULT GetCodeContext(   
   UINT64               uCodeLocationId,  
   IDebugCodeContext2** ppCodeContext  
);  
```  
  
```csharp  
int GetCodeContext(   
   ulong                  uCodeLocationId,  
   out IDebugCodeContext2 ppCodeContext  
);  
```  
  
#### <a name="parameters"></a>参数  
 `uCodeLocationId`  
 [in]指定的代码位置标识符。 请参阅备注部分[GetCodeLocationId](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodelocationid.md)方法有关的代码位置标识符的说明。  
  
 `ppCodeContext`  
 [out]返回[IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)对象，表示关联的代码上下文。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="remarks"></a>备注  
 可以通过调用返回的代码位置标识符[GetCurrentLocation](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcurrentlocation.md)方法并且可以出现在[DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)结构。  
  
 若要将代码上下文转换的代码位置标识符，请调用[GetCodeLocationId](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodelocationid.md)方法。  
  
## <a name="see-also"></a>请参阅  
 [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [GetCodeLocationId](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodelocationid.md)   
 [GetCurrentLocation](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcurrentlocation.md)   
 [DisassemblyData](../../../extensibility/debugger/reference/disassemblydata.md)
