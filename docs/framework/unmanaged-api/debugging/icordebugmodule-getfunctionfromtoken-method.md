---
title: Método ICorDebugModule::GetFunctionFromToken
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetFunctionFromToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetFunctionFromToken
helpviewer_keywords:
- GetFunctionFromToken method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetFunctionFromToken method [.NET Framework debugging]
ms.assetid: 6fe12194-4ef7-43c1-9570-ade35ccf127a
topic_type:
- apiref
ms.openlocfilehash: a33b6ff308f3444496e5a1cb2e04f28e80305db5
ms.sourcegitcommit: 488aced39b5f374bc0a139a4993616a54d15baf0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2020
ms.locfileid: "83212571"
---
# <a name="icordebugmodulegetfunctionfromtoken-method"></a>Método ICorDebugModule::GetFunctionFromToken
Obtém a função que é especificada pelo token de metadados.  
  
## <a name="syntax"></a>Sintaxe  
  
```cpp  
HRESULT GetFunctionFromToken(  
    [in] mdMethodDef methodDef,  
    [out] ICorDebugFunction **ppFunction  
);  
```  
  
## <a name="parameters"></a>Parâmetros  
 `methodDef`  
 no Um `mdMethodDef` token de metadados que faz referência aos metadados da função.  
  
 `ppFunction`  
 fora Um ponteiro para o endereço de um objeto de interface ICorDebugFunction que representa a função.  
  
## <a name="remarks"></a>Comentários  
 O `GetFunctionFromToken` método retornará um CORDBG_E_FUNCTION_NOT_IL HRESULT se o valor passado `methodDef` não se referir a um método MSIL (Microsoft Intermediate Language).  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** confira [Requisitos do sistema](../../get-started/system-requirements.md).  
  
 **Cabeçalho:** CorDebug.idl, CorDebug.h  
  
 **Biblioteca:** CorGuids.lib  
  
 **.NET Framework versões:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
