---
title: Практическое руководство. Использование атрибутов разделения столбцов FlowDocument
ms.date: 03/30/2017
helpviewer_keywords:
- FlowDocument column-separating attributes
- column-separating attributes
- documents [WPF], FlowDocument column-separating attributes
ms.assetid: c7a822f8-aeca-45bd-a258-2852ff28005c
ms.openlocfilehash: 678e01a35c286ea03f0385291d64f2f900f068c5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2018
ms.locfileid: "33543775"
---
# <a name="how-to-use-flowdocument-column-separating-attributes"></a>Практическое руководство. Использование атрибутов разделения столбцов FlowDocument
В этом примере показано, как использовать возможности разделения столбцов <xref:System.Windows.Documents.FlowDocument>.  
  
## <a name="example"></a>Пример  
 В следующем примере определяется <xref:System.Windows.Documents.FlowDocument>и задает <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, и <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> атрибуты.  <xref:System.Windows.Documents.FlowDocument> Содержит один абзац содержимого образца.  
  
 [!code-xaml[FlowDocumentSnippets#_FlowDocumentColumnStuffXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml#_flowdocumentcolumnstuffxaml)]  
  
 На следующем рисунке показано влияние <xref:System.Windows.Documents.FlowDocument.ColumnGap%2A>, <xref:System.Windows.Documents.FlowDocument.ColumnRuleBrush%2A>, и <xref:System.Windows.Documents.FlowDocument.ColumnRuleWidth%2A> атрибуты в готовом для просмотра <xref:System.Windows.Documents.FlowDocument>.  
  
 ![Снимок экрана: Документ нефиксированного формата внутренний столбец](../../../../docs/framework/wpf/advanced/media/flowdocumentintracolumn.png "FlowDocumentIntraColumn")
