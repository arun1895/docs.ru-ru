---
title: "Перечисление CorDebugSetContextFlag"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorDebugSetContextFlag
api_location: mscordbi.dll
api_type: COM
f1_keywords: CorDebugSetContextFlag
helpviewer_keywords: CorDebugSetContextFlag enumeration [.NET Framework debugging]
ms.assetid: b30280bb-fe75-44ed-8589-bcff081fae44
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 958ed303fab3dcb01fad2040dd06381e76fe5a00
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="cordebugsetcontextflag-enumeration"></a><span data-ttu-id="3661b-102">Перечисление CorDebugSetContextFlag</span><span class="sxs-lookup"><span data-stu-id="3661b-102">CorDebugSetContextFlag Enumeration</span></span>
<span data-ttu-id="3661b-103">Указывает происхождение контекста: взят из активного (или листового) кадра в стеке или был вычислен в результате освобождения другого кадра.</span><span class="sxs-lookup"><span data-stu-id="3661b-103">Indicates whether the context is from the active (or leaf) frame on the stack or has been computed by unwinding from another frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3661b-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3661b-104">Syntax</span></span>  
  
```  
typedef enum CorDebugSetContextFlag  
{  
   SET_CONTEXT_FLAG_ACTIVE_FRAME = 1  
   SET_CONTEXT_FLAG_UNWIND_FRAME = 2  
}  CorDebugSetContextFlag;  
```  
  
## <a name="members"></a><span data-ttu-id="3661b-105">Члены</span><span class="sxs-lookup"><span data-stu-id="3661b-105">Members</span></span>  
  
|<span data-ttu-id="3661b-106">Член</span><span class="sxs-lookup"><span data-stu-id="3661b-106">Member</span></span>|<span data-ttu-id="3661b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3661b-107">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="3661b-108">SET_CONTEXT_FLAG_ACTIVE_FRAME</span><span class="sxs-lookup"><span data-stu-id="3661b-108">SET_CONTEXT_FLAG_ACTIVE_FRAME</span></span>|<span data-ttu-id="3661b-109">Контекст, активный контекст потока.</span><span class="sxs-lookup"><span data-stu-id="3661b-109">The context is the thread’s active context.</span></span>|  
|<span data-ttu-id="3661b-110">SET_CONTEXT_FLAG_UNWIND_FRAME</span><span class="sxs-lookup"><span data-stu-id="3661b-110">SET_CONTEXT_FLAG_UNWIND_FRAME</span></span>|<span data-ttu-id="3661b-111">Контекст был вычислен в результате освобождения другого кадра.</span><span class="sxs-lookup"><span data-stu-id="3661b-111">The context has been computed by unwinding from another frame.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3661b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="3661b-112">Remarks</span></span>  
 <span data-ttu-id="3661b-113">`CorDebugSetContextFlag`Предоставляет значения, которые используются в [ICorDebugStackWalk::SetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-setcontext-method.md) метод.</span><span class="sxs-lookup"><span data-stu-id="3661b-113">`CorDebugSetContextFlag` provides values that are used by the [ICorDebugStackWalk::SetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-setcontext-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3661b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3661b-114">Requirements</span></span>  
 <span data-ttu-id="3661b-115">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3661b-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3661b-116">**Заголовок:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3661b-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3661b-117">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3661b-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3661b-118">**Версии платформы .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3661b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3661b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="3661b-119">See Also</span></span>  
 [<span data-ttu-id="3661b-120">Перечисления отладки</span><span class="sxs-lookup"><span data-stu-id="3661b-120">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
 [<span data-ttu-id="3661b-121">Отладка</span><span class="sxs-lookup"><span data-stu-id="3661b-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)