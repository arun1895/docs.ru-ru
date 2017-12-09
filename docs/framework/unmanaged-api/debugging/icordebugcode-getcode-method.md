---
title: "Метод ICorDebugCode::GetCode"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugCode.GetCode
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugCode::GetCode
helpviewer_keywords:
- ICorDebugCode::GetCode method [.NET Framework debugging]
- GetCode method, ICorDebugCode interface [.NET Framework debugging]
ms.assetid: 7137e3d1-1dad-48d8-8c37-16ac816534d3
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 12820d0be725c92754640aaa4eebca56bbc33ab6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugcodegetcode-method"></a><span data-ttu-id="63c55-102">Метод ICorDebugCode::GetCode</span><span class="sxs-lookup"><span data-stu-id="63c55-102">ICorDebugCode::GetCode Method</span></span>
<span data-ttu-id="63c55-103">Возвращает весь код для заданной функции, отформатированной для дизассемблирования.</span><span class="sxs-lookup"><span data-stu-id="63c55-103">Gets all the code for the specified function, formatted for disassembly.</span></span> <span data-ttu-id="63c55-104">Этот метод является устаревшим в .NET Framework версии 2.0.</span><span class="sxs-lookup"><span data-stu-id="63c55-104">This method has been deprecated in the .NET Framework version 2.0.</span></span> <span data-ttu-id="63c55-105">Используйте [ICorDebugCode2::GetCodeChunks](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md) вместо него.</span><span class="sxs-lookup"><span data-stu-id="63c55-105">Use [ICorDebugCode2::GetCodeChunks](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63c55-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63c55-106">Syntax</span></span>  
  
```  
HRESULT GetCode (  
    [in] ULONG32     startOffset,   
    [in] ULONG32     endOffset,  
    [in] ULONG32     cBufferAlloc,  
    [out, size_is(cBufferAlloc),  
        length_is(*pcBufferSize)] BYTE buffer[],  
    [out] ULONG32    *pcBufferSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="63c55-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="63c55-107">Parameters</span></span>  
 `startOffset`  
 <span data-ttu-id="63c55-108">[in] Смещение начала функции.</span><span class="sxs-lookup"><span data-stu-id="63c55-108">[in] The offset of the beginning of the function.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="63c55-109">[in] Смещение конца функции.</span><span class="sxs-lookup"><span data-stu-id="63c55-109">[in] The offset of the end of the function.</span></span>  
  
 `cBufferAlloc`  
 <span data-ttu-id="63c55-110">[in] Размер `buffer` массива, в которой будет возвращаться код.</span><span class="sxs-lookup"><span data-stu-id="63c55-110">[in] The size of the `buffer` array into which the code will be returned.</span></span>  
  
 `buffer`  
 <span data-ttu-id="63c55-111">[out] Массив, в который будет возвращаться код.</span><span class="sxs-lookup"><span data-stu-id="63c55-111">[out] The array into which the code will be returned.</span></span>  
  
 `pcBufferSize`  
 <span data-ttu-id="63c55-112">[out] Число байтов, возвращенных.</span><span class="sxs-lookup"><span data-stu-id="63c55-112">[out] The number of bytes returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="63c55-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="63c55-113">Remarks</span></span>  
 <span data-ttu-id="63c55-114">Если код функции поделен на несколько блоков, они объединяются в порядке возрастания смещения машинного кода.</span><span class="sxs-lookup"><span data-stu-id="63c55-114">If the function's code has been divided into multiple chunks, they are concatenated in order of increasing native offset.</span></span> <span data-ttu-id="63c55-115">Границы инструкций не проверяются.</span><span class="sxs-lookup"><span data-stu-id="63c55-115">Instruction boundaries are not checked.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="63c55-116">Требования</span><span class="sxs-lookup"><span data-stu-id="63c55-116">Requirements</span></span>  
 <span data-ttu-id="63c55-117">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="63c55-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="63c55-118">**Заголовок:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="63c55-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="63c55-119">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="63c55-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="63c55-120">**Версии платформы .NET framework:** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="63c55-120">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63c55-121">См. также</span><span class="sxs-lookup"><span data-stu-id="63c55-121">See Also</span></span>  
 [<span data-ttu-id="63c55-122">Метод GetCodeChunks</span><span class="sxs-lookup"><span data-stu-id="63c55-122">GetCodeChunks Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md)  
 