---
title: Format Specifiers in C# |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
- CSharp
helpviewer_keywords:
- expressions [C#], formatting values
- variables [debugger], watch variable symbols
- symbols, watch variable formatting
- QuickWatch dialog box, using format specifiers
- specifiers, watch variable format
- QuickWatch dialog box, format specifiers in C#
- specifiers
- watch variable symbols
- Watch window, format specifiers in C#
- format specifiers, debugger
- debugger, format specifiers recognized by
ms.assetid: 345c8589-5f36-4d34-a58c-e56271687dd6
caps.latest.revision: 34
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3521f39227b5abcb51a4db6b61e6bf0d853e5afe
ms.sourcegitcommit: cea6187005f8a0cdf44e866a1534a4cf5356208c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/27/2019
ms.locfileid: "59000224"
---
# <a name="format-specifiers-in-c"></a>C# 中的格式说明符 #
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

可使用格式说明符更改值在“监视”窗口中显示的格式。 还可在“即时”  窗口、“命令”  窗口甚至是源窗口中使用格式说明符。 如果将鼠标悬停在这些窗口中的表达式上，结果将在数据提示中显示。 数据提示将在数据提示的显示内容中反映格式说明符。  
  
 若要使用格式说明符，请输入变量表达式。 后跟一个逗号和相应的说明符。  
  
## <a name="using-format-specifiers"></a>设置格式说明符  
 我们使用以下示例代码：  
  
```  
{  
    int my_var1 = 0x0065;  
    int my_var2 = 0x0066;  
    int my_var3 = 0x0067;  
}  
```  
  
 将 `my_var1` 变量添加到“监视”窗口（调试时，“调试”/“窗口”/“监视”/“监视 1” ），并将显示设置为十六进制（  “监视”窗口中右键单击该变量，然后选择“十六进制显示” ）。 现在“监视”  窗口将显示它包含值 0x0065。 若要将此值显示为十进制整数而不是十六进制整数，请在“名称”****列中，于变量名称后添加一个十进制格式说明符 “, d”。 “值”列现显示“101”  
  
 ![WatchFormatCSharp](../debugger/media/watchformatcsharp.png "WatchFormatCSharp")  
  
## <a name="format-specifiers"></a>格式说明符  
 下表介绍了 Visual Studio 调试器的 C# 格式说明符。  
  
|说明符|格式|原始监视值|显示|  
|---------------|------------|--------------------------|--------------|  
|ac|表达式的强制计算。 当关闭属性的隐式计算和隐式函数调用时，这是很有用的。 请参阅 [Side Effects and Expressions](http://msdn.microsoft.com/library/e1f8a6ea-9e19-481d-b6bd-df120ad3bf4e)。|消息“用户已关闭隐式函数计算”|\<value>|  
|d|十进制整数|0x0065|101|  
|dynamic|使用“动态”视图显示指定对象|显示对象的所有成员，包括动态视图|仅显示动态视图|  
|h|十六进制整数|61541|0x0000F065|  
|nq|不带引号的字符串|"My String"|My String|  
|隐藏|显示所有公共成员和非公共成员|显示公共成员|显示所有成员|  
|raw|以项在原始项节点中的显示格式来显示项。 只对代理对象有效。|字典\<T >|字典中的原始视图\<T >|  
|results|与实现 IEnumerable 或 IEnumerable 的类型的变量一起使用\<T >，通常在查询表达式的结果。 仅显示包含查询结果的成员。|显示所有成员。|显示满足查询条件的成员。|  
  
## <a name="see-also"></a>请参阅  
 [监视窗口和快速监视窗口](../debugger/watch-and-quickwatch-windows.md)   
 [变量窗口](http://msdn.microsoft.com/library/ce0a67f6-2502-4b7a-ba45-cc32f8aeba3e)
