---
title: /debug (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- debug compiler switches
- /debug compiler option [Visual Basic]
- -debug compiler option [Visual Basic]
- debug compiler option [Visual Basic]
ms.assetid: c2b0bea5-1d5e-499f-9bd5-4f6c6b715ea2
ms.openlocfilehash: 92ff9c5ea7352506c1949a77b4fb6291d63758d7
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2018
ms.locfileid: "50193803"
---
# <a name="-debug-visual-basic"></a>-debug (Visual Basic)
Компилятор создает отладочную информацию и помещает ее в файлах вывода.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
-debug[+ | -]  
' -or-  
-debug:[full | pdbonly]  
```  
  
## <a name="arguments"></a>Аргументы  
  
|Термин|Определение|  
|---|---|  
|`+` &#124; `-`|Необязательный. Указание `+` или `/debug` компилятор создает отладочную информацию и помещает ее в PDB-файл. Указание `-` действует так же как и при указании не `/debug`.|  
|`full` &#124; `pdbonly`|Необязательный. Определяет тип отладочной информации, создаваемой компилятором. Если вы не укажете `/debug:pdbonly`, по умолчанию используется `full`, что позволяет подключить отладчик к выполняющейся программе. `pdbonly` Аргумент разрешает отладку исходного кода при запуске программы в отладчике, но ассемблерный код отображается только в том случае, когда исполняемой программы к отладчику.|  
  
## <a name="remarks"></a>Примечания  
 Используйте этот параметр для создания отладочных сборок. Если вы не укажете `/debug`, `/debug+`, или `/debug:full`, вы не сможете отладка выходного файла программы.  
  
 По умолчанию отладочная информация не создается (`/debug-`). Для получения отладочной информации, укажите `/debug` или `/debug+`.  
  
 Сведения о настройке производительности отладки для приложения см. в разделе [Упрощение отладки образов](../../../framework/debug-trace-profile/making-an-image-easier-to-debug.md).  
  
|Чтобы задать - Отладка в среде разработки Visual Studio|  
|---|  
|1.  Выберите проект в **обозревателе решений**, а затем в меню **Проект** щелкните **Свойства**. <br />2.  Откройте вкладку **Компиляция**.<br />3.  Щелкните **Дополнительные параметры компиляции**.<br />4.  Измените значение в **создать отладочную информацию** поле.|  
  
## <a name="example"></a>Пример  
 Следующий пример помещает отладочную информацию в выходном файле `App.exe`.  
  
```  
vbc -debug -out:app.exe test.vb  
```  
  
## <a name="see-also"></a>См. также  
 [Компилятор Visual Basic с интерфейсом командной строки](../../../visual-basic/reference/command-line-compiler/index.md)  
 [/bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md)  
 [Примеры командных строк компиляции](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
