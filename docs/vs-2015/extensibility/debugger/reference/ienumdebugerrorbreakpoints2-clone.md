---
title: IEnumDebugErrorBreakpoints2::Clone |Microsoft Docs
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
- IEnumDebugErrorBreakpoints2::Clone
helpviewer_keywords:
- IEnumDebugErrorBreakpoints2::Clone
ms.assetid: f6fb4985-8dd6-4a9b-98e0-15dbc64cc9ec
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 754813545f774aa87bb72538782f654d1f090a43
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47482049"
---
# <a name="ienumdebugerrorbreakpoints2clone"></a>IEnumDebugErrorBreakpoints2::Clone
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

本主题的最新版本，请参阅[IEnumDebugErrorBreakpoints2::Clone](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/ienumdebugerrorbreakpoints2-clone)。  
  
返回当前枚举作为一个单独的对象的副本。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
HRESULT Clone(  
   IEnumDebugErrorBreakpoints2** ppEnum  
);  
```  
  
```csharp  
int Clone(  
   out IEnumDebugErrorBreakpoints2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>参数  
 `ppEnum`  
 [out]返回此枚举作为一个单独的对象的副本。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="remarks"></a>备注  
 枚举的副本在调用此方法时都具有与原始相同的状态。 但是，该副本的和原始的状态是独立的并且可以单独更改。  
  
## <a name="see-also"></a>请参阅  
 [IEnumDebugErrorBreakpoints2](../../../extensibility/debugger/reference/ienumdebugerrorbreakpoints2.md)
