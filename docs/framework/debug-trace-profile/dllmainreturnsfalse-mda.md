---
title: Помощник по отладке управляемого кода dllMainReturnsFalse
ms.date: 03/30/2017
helpviewer_keywords:
- managed debugging assistants (MDAs), DllMain returns false
- DllMainReturnsFalse MDA
- DllMain function
- MDAs (managed debugging assistants), DllMain returns false
ms.assetid: e2abdd04-f571-4b97-8c16-2221b8588429
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4987b025450f2207a01a472a0c39fc6da2de0782
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
ms.locfileid: "33386497"
---
# <a name="dllmainreturnsfalse-mda"></a>Помощник по отладке управляемого кода dllMainReturnsFalse
Помощник по отладке управляемого кода `dllMainReturnsFalse` (MDA) активируется в том случае, если управляемая функция `DllMain` в пользовательской сборке вызывается с причиной DLL_PROCESS_ATTACH и возвращает значение FALSE.  
  
## <a name="symptoms"></a>Симптомы  
 Функция `DllMain` возвращает значение FALSE, свидетельствующее о сбое при ее выполнении. Это может привести к возникновению неопределенных проблем, поскольку функции `DllMain` обычно содержат важный код инициализации.  
  
## <a name="cause"></a>Причина  
 Функция `DllMain` вызывается с причиной DLL_PROCESS_ATTACH для инициализации библиотеки DLL при загрузке. Если она возвращает значение FALSE, значит инициализация библиотеки DLL завершилась сбоем.  
  
## <a name="resolution"></a>Решение  
 Проанализируйте код функции `DllMain` для указанной библиотеки DLL и определите причину сбоя при инициализации.  
  
## <a name="effect-on-the-runtime"></a>Влияние на среду выполнения  
 Этот помощник отладки управляемого кода не оказывает никакого влияния на среду CLR. Он только выводит данные о возвращаемом значении для `DllMain`.  
  
## <a name="output"></a>Вывод  
 Сообщение, указывающее, что функция `DllMain` была вызвана с причиной DLL_PROCESS_ATTACH и вернула значение FALSE. Обратите внимание, что этот помощник по отладке кода вызывается только в том случае, если в управляемом коде реализована функция `DllMain`.  
  
## <a name="configuration"></a>Конфигурация  
  
```xml  
<mdaConfig>  
  <assistants>  
    <dllMainReturnsFalse />  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a>См. также  
 [Диагностика ошибок посредством помощников по отладке управляемого кода](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
