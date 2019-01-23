---
title: IXCLRDataProcess::GetAppDomainByUniqueId 方法
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
helpviewer.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 83e7d4e1a4ff3c2e6f573d6c097c7cdb9c5f3c54
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416369"
---
# <a name="ixclrdataprocessgetappdomainbyuniqueid-method"></a><span data-ttu-id="814c9-102">IXCLRDataProcess::GetAppDomainByUniqueId 方法</span><span class="sxs-lookup"><span data-stu-id="814c9-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span></span>

<span data-ttu-id="814c9-103">获取`AppDomain`基于它的唯一标识符的进程中。</span><span class="sxs-lookup"><span data-stu-id="814c9-103">Gets an `AppDomain` in a process based on its unique identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="814c9-104">语法</span><span class="sxs-lookup"><span data-stu-id="814c9-104">Syntax</span></span>
```
HRESULT GetAppDomainByUniqueID(
    [in] ULONG64               id,
    [out] IXCLRDataAppDomain **appDomain
);
```

### <a name="parameters"></a><span data-ttu-id="814c9-105">参数</span><span class="sxs-lookup"><span data-stu-id="814c9-105">Parameters</span></span>
<span data-ttu-id="814c9-106">`id` [in]AppDomain 的唯一标识符</span><span class="sxs-lookup"><span data-stu-id="814c9-106">`id` [in] The unique identifier of the AppDomain</span></span>

<span data-ttu-id="814c9-107">`appDomain` [out]AppDomain</span><span class="sxs-lookup"><span data-stu-id="814c9-107">`appDomain` [out] The AppDomain</span></span>

## <a name="remarks"></a><span data-ttu-id="814c9-108">备注</span><span class="sxs-lookup"><span data-stu-id="814c9-108">Remarks</span></span>

<span data-ttu-id="814c9-109">提供的方法属于`IXCLRDataProcess`接口，并对应于虚拟方法表的 20 槽。</span><span class="sxs-lookup"><span data-stu-id="814c9-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="814c9-110">`IXCLRDataAppDomain*`返回用于与其他 Api 的交互。</span><span class="sxs-lookup"><span data-stu-id="814c9-110">The `IXCLRDataAppDomain*` returned is used for interaction with other APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="814c9-111">要求</span><span class="sxs-lookup"><span data-stu-id="814c9-111">Requirements</span></span>
<span data-ttu-id="814c9-112">**平台：** 请参阅[系统需求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="814c9-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="814c9-113">**标头：** 无</span><span class="sxs-lookup"><span data-stu-id="814c9-113">**Header:** None</span></span>  
<span data-ttu-id="814c9-114">**库：** 无</span><span class="sxs-lookup"><span data-stu-id="814c9-114">**Library:** None</span></span>  
<span data-ttu-id="814c9-115">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="814c9-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="814c9-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="814c9-116">See Also</span></span>
- [<span data-ttu-id="814c9-117">调试</span><span class="sxs-lookup"><span data-stu-id="814c9-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="814c9-118">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="814c9-118">IXCLRDataProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)