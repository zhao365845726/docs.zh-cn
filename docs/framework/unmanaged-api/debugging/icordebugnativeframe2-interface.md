---
title: ICorDebugNativeFrame2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame2
helpviewer_keywords:
- ICorDebugNativeFrame2 interface [.NET Framework debugging]
ms.assetid: 52a80838-af36-4399-bc97-d8a4c6d76df2
topic_type:
- apiref
ms.openlocfilehash: 22a3f39bc1f9b4e6cad1db4fd0a6480b7c04e8fa
ms.sourcegitcommit: 13e79efdbd589cad6b1de634f5d6b1262b12ab01
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2020
ms.locfileid: "76792754"
---
# <a name="icordebugnativeframe2-interface"></a>ICorDebugNativeFrame2 接口
提供用于测试子帧与父帧关系的方法。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[IsChild 方法](icordebugnativeframe2-ischild-method.md)|确定当前帧是否为子框架。|  
|[IsMatchingParentFrame 方法](icordebugnativeframe2-ismatchingparentframe-method.md)|确定指定的帧是否为当前帧的父级。|  
|[GetStackParameterSize 方法](icordebugnativeframe2-getstackparametersize-method.md)|返回 x86 操作系统上堆栈上的参数的累积大小。|  
  
## <a name="remarks"></a>备注  
 此接口以逻辑方式扩展了 "ICorDebugNativeFrame" 接口。  
  
> [!NOTE]
> 此接口不支持跨计算机或跨进程远程调用。  
  
## <a name="requirements"></a>需求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>另请参阅

- [调试接口](debugging-interfaces.md)
- [调试](index.md)
