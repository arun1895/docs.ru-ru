---
title: Вызов свойства или метода с помощью строкового имени (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- passing operators [Visual Basic]
- strings [Visual Basic], passing new operators as
- objects [Visual Basic], setting properties
- setting properties, object properties at run time
- method calls [Visual Basic], strings
- methods [Visual Basic], calling with string names
- calling methods [Visual Basic], string names
- properties [Visual Basic], setting at run time
- CallByName function
ms.assetid: 79a7b8b4-b8c7-4ad8-aca8-12a9a2b32f03
ms.openlocfilehash: 76be426049489bb58e50878822c03fa5cd5cca8e
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/24/2018
ms.locfileid: "42911650"
---
# <a name="calling-a-property-or-method-using-a-string-name-visual-basic"></a>Вызов свойства или метода с помощью строкового имени (Visual Basic)
В большинстве случаев доступ к свойствам и методам объекта во время разработки и написать код для их обработки. Однако в некоторых случаях может не известно, какие свойства и методы объекта заранее или необходима гибкость конечному пользователю для указания свойств или выполнения методов во время выполнения.  
  
## <a name="callbyname-function"></a>CallByName-функция  
 Рассмотрим, например, клиентское приложение, которое вычисляет выражения, введенные пользователем, передав оператор на COM-компонент. Предположим, что постоянно добавляются новые функции к компоненту, которым необходимы новые операторы. При использовании методов доступа к объекту standard, необходимо перекомпилировать и повторно распространить клиентское приложение, прежде чем он может использовать новые операторы. Чтобы избежать этого, можно использовать `CallByName` функцию для передачи новых операторов в виде строк без изменения приложения.  
  
 `CallByName` Функция позволяет использовать строку для указания свойства или метода во время выполнения. Сигнатура для `CallByName` выглядит следующим образом:  
  
 *Результат* = `CallByName`(*объект*, *Имя_процедуры*, *CallType*, *аргументы*())  
  
 Первый аргумент, *объект*, принимает имя объекта, будет действовать. *Имя_процедуры* аргумент принимает строку, которая содержит имя метода или свойства вызываемой процедуры. *CallType* аргумент принимает константу, представляющую тип процедуры для вызова: метод (`Microsoft.VisualBasic.CallType.Method`), свойства, считываемого (`Microsoft.VisualBasic.CallType.Get`), или свойство, которому присвоен (`Microsoft.VisualBasic.CallType.Set`). *Аргументы* аргументом, который не является обязательным, принимает массив объектов типа `Object` , содержащий все аргументы процедуры.  
  
 Можно использовать `CallByName` с классами в текущем решении, но чаще всего используется для доступа к COM-объектов или объектов из [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] сборки.  
  
 Предположим, что добавьте ссылку на сборку, содержащую класс с именем `MathClass`, который имеет новую функцию с именем `SquareRoot`, как показано в следующем коде:  
  
 [!code-vb[VbVbalrOOP#53](../../../../visual-basic/misc/codesnippet/VisualBasic/calling-a-property-or-method-using-a-string-name_1.vb)]  
  
 Ваше приложение может использовать текстовые поля для элемента управления, какой метод будет вызван и ее аргументов. Например если `TextBox1` содержит выражение для вычисления, и `TextBox2` — используется для ввода имени функции, можно использовать следующий код для вызова `SquareRoot` функцию для выражения в `TextBox1`:  
  
 [!code-vb[VbVbalrOOP#54](../../../../visual-basic/misc/codesnippet/VisualBasic/calling-a-property-or-method-using-a-string-name_2.vb)]  
  
 Если ввести «64» в `TextBox1`, «SquareRoot» в `TextBox2`, а затем вызвать `CallMath` процедуры, квадратный корень числа в `TextBox1` вычисляется. Код в примере вызывает `SquareRoot` функции (которая принимает строку, содержащую выражение для оценки в качестве обязательный аргумент) и возвращает значение «8» в `TextBox1` (квадратный корень из 64). Конечно, если пользователь вводит недопустимую строку в `TextBox2`, если строка содержит имя свойства вместо метода, или если метод имеет дополнительный аргумент, возникает ошибка времени выполнения. Необходимо добавить надежный код обработки ошибок, при использовании `CallByName` чтобы реагировать на эти или другие ошибки.  
  
> [!NOTE]
>  Хотя `CallByName` функция может быть полезна в некоторых случаях, необходимо учитывать его влияние на производительность — с помощью `CallByName` для вызова процедуры немного медленнее, чем вызов с поздним связыванием. Если вы вызываете функцию, которая вызывается повторно, например в цикле, `CallByName` может иметь существенно повлиять на производительность.  
  
## <a name="see-also"></a>См. также  
 <xref:Microsoft.VisualBasic.Interaction.CallByName%2A>  
 [Определение типа объекта](../../../../visual-basic/programming-guide/language-features/early-late-binding/determining-object-type.md)
