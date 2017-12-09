---
title: "Метод ICorDebugRegisterSet::SetRegisters"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugRegisterSet.SetRegisters
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugRegisterSet::SetRegisters
helpviewer_keywords:
- SetRegisters method, ICorDebugRegisterSet interface [.NET Framework debugging]
- ICorDebugRegisterSet::SetRegisters method [.NET Framework debugging]
ms.assetid: ac6244b9-54ba-475f-b72a-abed6afc46ec
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 00cb6d92d23f3cb1bb4af8f24901ab5c23b8738b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugregistersetsetregisters-method"></a><span data-ttu-id="745aa-102">Метод ICorDebugRegisterSet::SetRegisters</span><span class="sxs-lookup"><span data-stu-id="745aa-102">ICorDebugRegisterSet::SetRegisters Method</span></span>
<span data-ttu-id="745aa-103">`SetRegisters`не реализован в .NET Framework версии 2.0.</span><span class="sxs-lookup"><span data-stu-id="745aa-103">`SetRegisters` is not implemented in the .NET Framework version 2.0.</span></span> <span data-ttu-id="745aa-104">Не вызывайте этот метод.</span><span class="sxs-lookup"><span data-stu-id="745aa-104">Do not call this method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="745aa-105">Использовать операции более высокого уровня, такие как [ICorDebugILFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-setip-method.md) или [ICorDebugNativeFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md).</span><span class="sxs-lookup"><span data-stu-id="745aa-105">Use the higher-level operations such as [ICorDebugILFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-setip-method.md) or [ICorDebugNativeFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="745aa-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="745aa-106">Syntax</span></span>  
  
```  
HRESULT SetRegisters (  
    [in] ULONG64   mask,  
    [in] ULONG32   regCount,  
    [in, size_is(regCount)] CORDB_REGISTER regBuffer[]  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="745aa-107">Требования</span><span class="sxs-lookup"><span data-stu-id="745aa-107">Requirements</span></span>  
 <span data-ttu-id="745aa-108">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="745aa-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="745aa-109">**Заголовок:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="745aa-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="745aa-110">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="745aa-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="745aa-111">**Версии платформы .NET framework:** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="745aa-111">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="745aa-112">См. также</span><span class="sxs-lookup"><span data-stu-id="745aa-112">See Also</span></span>  
 [<span data-ttu-id="745aa-113">ICorDebugRegisterSet-интерфейс</span><span class="sxs-lookup"><span data-stu-id="745aa-113">ICorDebugRegisterSet Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)  
 [<span data-ttu-id="745aa-114">ICorDebugRegisterSet2-интерфейс</span><span class="sxs-lookup"><span data-stu-id="745aa-114">ICorDebugRegisterSet2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)