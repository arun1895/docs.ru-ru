---
title: Практическое руководство. Анимация объекта с помощью ключевых кадров
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], objects with key frames
- key frames [WPF], animating objects with
ms.assetid: b1f15ba9-cac7-4cea-8699-5c6b55c05c5e
ms.openlocfilehash: 5e948b574e1b4a1c431b9495583e9579502576a8
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2018
ms.locfileid: "43416338"
---
# <a name="how-to-animate-an-object-by-using-key-frames"></a>Практическое руководство. Анимация объекта с помощью ключевых кадров
В этом примере показано, как анимировать объект, который в этом примере является <xref:System.Windows.Controls.Page.Background%2A> свойство <xref:System.Windows.Controls.Page> элемента управления, с помощью ключевых кадров.  
  
## <a name="example"></a>Пример  
 В следующем примере используется <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames> изменения в класс анимация цвета <xref:System.Windows.Controls.Page.Background%2A> свойство <xref:System.Windows.Controls.Page> элемента управления. Пример изменяется цвет кисти фона с регулярными интервалами. Эта анимация использует <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> класс, чтобы создать три различных ключевых кадров. Анимация использует ключевых кадра следующим образом:  
  
1.  В конце первой секунды, анимирует экземпляр <xref:System.Windows.Media.LinearGradientBrush> класса. В этом разделе примере применяется линейный градиент к цвету фона, таким образом, чтобы переход цвета с желтого на оранжевый, красный.  
  
2.  В конце следующей секунды, анимирует экземпляр <xref:System.Windows.Media.RadialGradientBrush> класса. Этот раздел примера относится радиального градиента к цвет фона, определяющий цвет переход от белого к синему на черный.  
  
3.  В конце третьей секунды, анимирует экземпляр <xref:System.Windows.Media.DrawingBrush> класса. В этом разделе примере применяется шахматной в фоновом режиме.  
  
4.  Анимация начинается снова и повторяется бесконечно.  
  
> [!NOTE]
>  <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> Это единственный тип ключевого кадра, который можно использовать с <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames> класса. Опорные кадры, например <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> , создают резкие изменения значений, то есть, изменения цвета в этом примере происходит внезапное.  
  
 [!code-xaml[keyframes_snip#ObjectAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ObjectAnimationUsingKeyFramesExample.xaml#objectanimationusingkeyframeswholepage)]  
  
 Описание полного примера см. в разделе [Пример анимации по ключевым кадрам](https://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>См. также  
 <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames>  
 <xref:System.Windows.Controls.Page.Background%2A>  
 <xref:System.Windows.Controls.Page>  
 <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame>  
 <xref:System.Windows.Media.LinearGradientBrush>  
 <xref:System.Windows.Media.RadialGradientBrush>  
 <xref:System.Windows.Media.DrawingBrush>  
 [Общие сведения об анимации по ключевым кадрам](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)  
 [Практические руководства, посвященные анимации по ключевым кадрам](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)
