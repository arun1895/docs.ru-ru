---
title: Метод ISymUnmanagedWriter::DefineSequencePoints
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineSequencePoints
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineSequencePoints
helpviewer_keywords:
- DefineSequencePoints method [.NET Framework debugging]
- ISymUnmanagedWriter::DefineSequencePoints method [.NET Framework debugging]
ms.assetid: 64202baf-be6b-40ba-8162-8cc6c0c9b8e1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5825f0425947f109ed834879684357fef7b70959
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123778"
---
# <a name="isymunmanagedwriterdefinesequencepoints-method"></a>Метод ISymUnmanagedWriter::DefineSequencePoints
Определяет группу точек следования в текущем методе. Каждая Начальная строка и начальный столбец определяют начало оператора в методе. Каждая конечная строка и конечный столбец определяет конец оператора в методе. Массивы должны быть упорядочены по возрастанию смещений. Смещение всегда измеряется от начала метода, в байтах.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
HRESULT DefineSequencePoints(  
    [in] ISymUnmanagedDocumentWriter*  document,  
    [in] ULONG32 spCount,  
    [in, size_is(spCount)] ULONG32     offsets[],  
    [in, size_is(spCount)] ULONG32     lines[],  
    [in, size_is(spCount)] ULONG32     columns[],  
    [in, size_is(spCount)] ULONG32     endLines[],  
    [in, size_is(spCount)] ULONG32     endColumns[]);  
```  
  
#### <a name="parameters"></a>Параметры  
 `document`  
 [in] Объект документа, для которого определяются точки следования.  
  
 `spCount`  
 [in] Объект `ULONG32` указывает размер каждого из `offsets`, `lines`, `columns`, `endLines`, и `endColumns` буферов.  
  
 `offsets`  
 [in] Смещение точек следования определяются от начала метода.  
  
 `lines`  
 [in] Начальная строка числа точек следования.  
  
 `columns`  
 [in] Начальный номера столбцов точек следования.  
  
 `endLines`  
 [in] Конечный номера строк точек следования. Этот параметр является необязательным.  
  
 `endColumns`  
 [in] Номера конечных столбцов точек следования. Этот параметр является необязательным.  
  
## <a name="return-value"></a>Возвращаемое значение  
 Значение S_OK, если метод выполнен успешно; в противном случае — значение E_FAIL или другим кодом ошибки.  
  
## <a name="requirements"></a>Требования  
 **Заголовок:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>См. также  
 [Интерфейс ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
