---
title: IDebugSourceServerModule::GetSourceServerData | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugSourceServerModule::GetSourceServerData
ms.assetid: f15d86aa-1bd9-4b16-a64a-21b01c27db2e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fc99d014c1e31616ebd2a6cc16608a1d1bc741ce
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/22/2019
ms.locfileid: "56683865"
---
# <a name="idebugsourceservermodulegetsourceserverdata"></a>IDebugSourceServerModule::GetSourceServerData
检索源服务器信息的数组。

## <a name="syntax"></a>语法

```cpp
HRESULT GetSourceServerData(
    ULONG* pDataByteCount,
    BYTE** ppData
);
```

```csharp
public int GetSourceServerData(
    out uint  pDataByteCount,
    out int[] ppData
);
```

#### <a name="parameters"></a>参数
`pDataByteCount`

 [out]数据数组中的字节数。

`ppData`

 [out]对数据数组的引用。

## <a name="return-value"></a>返回值
如果成功，则返回`S_OK`; 否则为返回错误代码。

## <a name="example"></a>示例
下面的示例演示如何实现此方法对于**CModule**对象，它公开[IDebugSourceServerModule](../../../extensibility/debugger/reference/idebugsourceservermodule.md)接口。

```cpp
HRESULT CModule::GetSourceServerData(ULONG* pDataByteCount, BYTE** ppData)
{
    HRESULT hr = S_OK;
    CComPtr<ISymUnmanagedReader> pSymReader;
    CComPtr<ISymUnmanagedSourceServerModule> pSourceServerModule;

    IfFalseGo( pDataByteCount && ppData, E_INVALIDARG );
    *pDataByteCount = 0;
    *ppData = NULL;

    IfFailGo( this->GetUnmanagedSymReader( &pSymReader ) );
    IfFailGo( pSymReader->QueryInterface( &pSourceServerModule ) );

    IfFailGo( pSourceServerModule->GetSourceServerData( pDataByteCount, ppData ) );

Error:

    return hr;
}
```

## <a name="see-also"></a>请参阅
- [IDebugSourceServerModule](../../../extensibility/debugger/reference/idebugsourceservermodule.md)
