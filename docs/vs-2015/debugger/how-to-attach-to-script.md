---
title: 如何： 附加到脚本 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- script debugging, attaching to script
- script, attaching to
- processes, attaching to script
- remote debugging, attaching to script
ms.assetid: 82013e9a-ef53-4fd2-b451-a6891cdc6307
caps.latest.revision: 26
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 18f9ec77b990113cc039142f6bfe51058d532408
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47481487"
---
# <a name="how-to-attach-to-script"></a>如何：附加到脚本
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[如何： 附加到脚本](https://docs.microsoft.com/visualstudio/debugger/how-to-attach-to-script)。  
  
本主题介绍如何手动将 Visual Studio 调试器附加到脚本文件进行调试。  
  
### <a name="to-attach-to-a-running-process"></a>附加到正在运行的进程  
  
1.  在 **“调试”** 菜单上选择 **“附加到进程”**。 (如果不没有打开任何项目，选择**附加到进程**上**工具**菜单。)  
  
2.  在中**附加到进程**对话框中，看**可用进程**需要将附加到列表并找到的脚本进程。 您可以通过查看来识别脚本进程**类型**列。  
  
    1.  如果要调试的进程运行在另一台计算器上，必须首先选择该远程计算机。 有关详细信息，请参阅[如何： 选择远程计算机](http://msdn.microsoft.com/en-us/4332ba8e-2f0b-4f62-b96a-e762b9f3c3ba)。  
  
    2.  如果进程在其他用户帐户下运行，请选中 **“显示所有用户的进程”** 复选框。  
  
    3.  如果通过连接**远程桌面连接**，选择**显示所有会话中的进程**复选框。  
  
3.  单击要附加到的进程。  
  
4.  在中**将附加到**框中，你应看到**脚本代码**或**自动： 脚本代码**。 如果显示其他内容，请按照下列步骤操作：  
  
    1.  单击 **“选择”**。  
  
    2.  在中**选择代码类型**对话框中，单击**调试这些代码类型**，然后选择**脚本**。  
  
    3.  单击 **“确定”**。  
  
5.  单击 **“附加”**。  
  
     此时您可能会看到一个警告，通知您 Internet Explorer 中已禁用脚本调试。 如果发生这种情况，请参阅[警告： 脚本调试被禁用](../debugger/warning-script-debugging-disabled.md)。  
  
 打开 **“进程”** 对话框时，会自动显示 **“可用进程”** 列表。 在该对话框打开时进程可以在后台启动和停止。 因此，内容可能并非总是最新的。 可以随时通过按查看当前进程列表刷新列表**刷新**按钮。  
  
 调试时可以附加到多个程序，但在任何时间，调试器中都只有一个程序处于活动状态。 可以在“调试位置”工具栏中设置活动程序。 有关详细信息，请参阅[如何： 设置当前进程](http://msdn.microsoft.com/en-us/7e1d7fa5-0e40-44cf-8c41-d3dba31c969e)。  
  
 所有**调试**菜单执行命令都会影响活动程序。 您可以从进程对话框中断任何已调试的程序。请参阅[使用断点](../debugger/using-breakpoints.md)。  
  
> [!NOTE]
>  如果尝试附加到不受信任的用户帐户拥有的进程，则会出现安全警告对话框确认。 有关详细信息，请参阅[安全警告： 附加到不受信任的用户所拥有的进程可能很危险。以下信息看上去可疑或者你不确定，如果未附加到此进程](../debugger/security-warning-attaching-to-a-process-owned-by-an-untrusted-user-can-be-dangerous-if-the-following-information-looks-suspicious-or-you-are-unsure-do-not-attach-to-this-process.md)。  
  
 在某些情况下，在“终端服务”（“远程桌面”）会话中进行调试时，“可用进程”列表不会显示所有可用进程。 在 [!INCLUDE[WinXPSvr](../includes/winxpsvr-md.md)] 或更高版本中，如果以受限用户的身份运行 Visual Studio，“可用进程”列表将不显示在会话 0 中运行的进程，该会话用于运行服务与其他服务器进程（包括 w3wp.exe）。 您可以通过以下方法解决该问题：使用管理员帐户运行 Visual Studio 或从服务器控制台而不是“终端服务”会话运行 Visual Studio。 如果可能都不奏效，第三个选项是附加到进程通过键入 vsjitdebugger.exe-p ProcessId 在 Windows 命令行。 您可以使用 tlist.exe 来确定进程 ID。 若要获取 tlist.exe，请下载并安装调试工具的 Windows，网址[Windows 硬件开发人员中心](http://go.microsoft.com/fwlink/?linkid=1651)。  
  
## <a name="see-also"></a>请参阅  
 [客户端脚本调试](../debugger/client-side-script-debugging.md)   
 [将附加到正在运行的进程](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md)   
 [安全警告：附加到不受信任的用户所拥有的进程可能很危险。以下信息看上去可疑或者你不确定，如果未附加到此进程](../debugger/security-warning-attaching-to-a-process-owned-by-an-untrusted-user-can-be-dangerous-if-the-following-information-looks-suspicious-or-you-are-unsure-do-not-attach-to-this-process.md)   
 [调试器安全](../debugger/debugger-security.md)


