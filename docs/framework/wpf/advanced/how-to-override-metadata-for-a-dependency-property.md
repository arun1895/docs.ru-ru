---
title: Практическое руководство. Переопределение метаданных для свойств зависимости
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- metadata [WPF], overriding for dependency properties
- dependency properties [WPF], overriding metadata for
- overriding metadata for dependency properties [WPF]
ms.assetid: f90f026e-60d8-428a-933d-edf0dba4441f
ms.openlocfilehash: 8b207ca931d2202f7a35ae3cd16e325ec295ef5a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
ms.locfileid: "33543723"
---
# <a name="how-to-override-metadata-for-a-dependency-property"></a>Практическое руководство. Переопределение метаданных для свойств зависимости
В этом примере показан способ переопределения метаданных свойства зависимостей по умолчанию, поступающие из наследованного класса путем вызова <xref:System.Windows.DependencyProperty.OverrideMetadata%2A> метод и предоставление метаданных определенного типа.  
  
## <a name="example"></a>Пример  
 Определив его <xref:System.Windows.PropertyMetadata>, класс может определить поведения свойства зависимостей, такие как его по умолчанию значение свойства обратные вызовы и системы. Многие классы свойств зависимостей уже имеют метаданные по умолчанию, заданные во время процесса их регистрации. К ним относятся свойства зависимостей, которые являются частью [!INCLUDE[TLA2#tla_api](../../../../includes/tla2sharptla-api-md.md)] [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]. Класс, который наследует свойство зависимости при наследовании класса, может переопределить исходные метаданные, так что характеристики свойства, которые могут изменяться посредством метаданных, будут соответствовать любым особым требованиям подкласса.  
  
 Переопределение метаданных в свойстве зависимости должно быть выполнено до того, как свойство начнет использоваться системой свойств (то есть до того момента, когда будут созданы определенные экземпляры объектов, регистрирующие свойство). Вызовы <xref:System.Windows.DependencyProperty.OverrideMetadata%2A> должны быть выполнены в статическом конструкторе типа, предоставляющего себя в качестве `forType` параметр <xref:System.Windows.DependencyProperty.OverrideMetadata%2A>. При попытке изменить метаданные существующих экземпляров типа-владельца не возникнет исключения, но это приведет к несогласованному поведению системы свойств. Кроме того, метаданные могут переопределяться один раз для каждого типа. Последующие попытки переопределить метаданные для того же типа вызовут исключение.  
  
 В приведенном ниже примере пользовательский класс `MyAdvancedStateControl` переопределяет метаданные, предоставленные свойству `StateProperty` классом `MyAdvancedStateControl`, новыми метаданными свойства. Например, значение `StateProperty` по умолчанию теперь является `true`, если это свойство запрашивается для нового экземпляра `MyAdvancedStateControl`.  
  
 [!code-csharp[PropertySystemEsoterics#MyStateControl](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PropertySystemEsoterics/CSharp/SDKSampleLibrary/class1.cs#mystatecontrol)]
 [!code-vb[PropertySystemEsoterics#MyStateControl](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PropertySystemEsoterics/visualbasic/sdksamplelibrary/class1.vb#mystatecontrol)]  
[!code-csharp[PropertySystemEsoterics#MyAdvancedStateControl](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PropertySystemEsoterics/CSharp/SDKSampleLibrary/class1.cs#myadvancedstatecontrol)]
[!code-vb[PropertySystemEsoterics#MyAdvancedStateControl](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PropertySystemEsoterics/visualbasic/sdksamplelibrary/class1.vb#myadvancedstatecontrol)]  
  
## <a name="see-also"></a>См. также  
 <xref:System.Windows.DependencyProperty>  
 [Общие сведения о свойствах зависимости](../../../../docs/framework/wpf/advanced/dependency-properties-overview.md)  
 [Пользовательские свойства зависимостей](../../../../docs/framework/wpf/advanced/custom-dependency-properties.md)  
 [Разделы практического руководства](../../../../docs/framework/wpf/advanced/properties-how-to-topics.md)
