---
title: 调试本机代码中的线程的提示 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- threading [Visual Studio], debugging
- debugging [Visual Studio], threads
ms.assetid: 0374c8c6-57a3-4cfe-8047-2effef5ff5dc
caps.latest.revision: 25
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4a0a72f9846add13f2f57581a0b836a9f57f8150
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2019
ms.locfileid: "58931009"
---
# <a name="tips-for-debugging-threads-in-native-code"></a>调试本机代码中的线程时的提示
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

下面是在调试本机代码中的线程时可以使用的一些提示：  
  
-   可以通过在“监视”窗口或“快速监视”对话框中键入 `@TIB` 来查看“线程信息块”的内容。  
  
-   可以通过在“监视”窗口或“快速监视”对话框中输入 `@Err` 来查看当前线程的上一个错误代码。  
  
-   可以使用 C 运行库 (CRT) 函数来调试多线程应用程序。 有关详细信息，请参阅 [_malloc_dbg](http://msdn.microsoft.com/library/c97eca51-140b-4461-8bd2-28965b49ecdb)。  
  
## <a name="see-also"></a>请参阅  
 [调试多线程应用程序](../debugger/debug-multithreaded-applications-in-visual-studio.md)   
 [调试本机代码](../debugger/debugging-native-code.md)
