---
title: Выполнение в массивах строковых операций, не зависящих от языка и региональных параметров
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- culture-insensitive string operations, in arrays
- arrays [.NET Framework], culture-insensitive string operations
- comparer parameter
ms.assetid: f12922e1-6234-4165-8896-63f0653ab478
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 22815b5ab993b36bc8bcb91f89f346cb6d812e19
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/17/2018
ms.locfileid: "45698251"
---
# <a name="performing-culture-insensitive-string-operations-in-arrays"></a>Выполнение в массивах строковых операций, не зависящих от языка и региональных параметров
Перегруженные версии методов <xref:System.Array.Sort%2A?displayProperty=nameWithType> и <xref:System.Array.BinarySearch%2A?displayProperty=nameWithType> выполняют сортировку с учетом языка и региональных параметров, используя свойство <xref:System.Threading.Thread.CurrentCulture%2A?displayProperty=nameWithType>. Результат, возвращаемый этими методами, зависит от порядка сортировки в параметрах языка и региональных параметров. Чтобы результат не зависел от языка и региональных параметров, используйте перегрузки этого метода, которые принимают параметр `comparer`. Параметр `comparer` указывает реализацию <xref:System.Collections.IComparer>, которую нужно использовать при сравнении элементов массива. Укажите в этом параметре пользовательский инвариантный класс сравнения, который использует <xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=nameWithType>. Пример настраиваемого инвариантного класса сравнения предлагается в подразделе "Использование класса SortedList" статьи [Выполнение в коллекциях строковых операций, не зависящих от языка и региональных параметров](../../../docs/standard/globalization-localization/performing-culture-insensitive-string-operations-in-collections.md).  
  
 **Примечание**. Если передать в метод сравнения **CultureInfo.InvariantCulture**, сравнение выполняется без учета языка и региональных параметров. Однако при этом не выполняется нелингвистическое сравнение, например для путей к файлам, разделов реестра и переменных среды. Также не поддерживается принятие решений по безопасности на основе результата сравнения. Для нелингвистического сравнения и (или) поддержки принятия решений по безопасности в приложении следует использовать метод сравнения, который принимает значение <xref:System.StringComparison>. Приложение должно передавать <xref:System.StringComparison.Ordinal>.  
  
## <a name="see-also"></a>См. также

- <xref:System.Array.Sort%2A?displayProperty=nameWithType>  
- <xref:System.Array.BinarySearch%2A?displayProperty=nameWithType>  
- <xref:System.Collections.IComparer>  
- [Выполнение строковых операций, не зависящих от языка и региональных параметров](../../../docs/standard/globalization-localization/performing-culture-insensitive-string-operations.md)
