---
title: IMetaDataEmit::GetSaveSize 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.GetSaveSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::GetSaveSize
helpviewer_keywords:
- IMetaDataEmit::GetSaveSize method [.NET Framework metadata]
- GetSaveSize method [.NET Framework metadata]
ms.assetid: 8aea2e2c-23a3-4cda-9a06-e19f97383830
topic_type:
- apiref
ms.openlocfilehash: 125a63638a41707b8eed918253cb1f93abb907eb
ms.sourcegitcommit: 9a39f2a06f110c9c7ca54ba216900d038aa14ef3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/23/2019
ms.locfileid: "74434336"
---
# <a name="imetadataemitgetsavesize-method"></a>IMetaDataEmit::GetSaveSize 方法
获取当前范围内的程序集和它的元数据的预计二进制大小。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetSaveSize (  
    [in]  CorSaveSize fSave,  
    [out] DWORD       *pdwSaveSize  
);  
```  
  
## <a name="parameters"></a>参数  
 `fSave`  
 中[CorSaveSize](../../../../docs/framework/unmanaged-api/metadata/corsavesize-enumeration.md)枚举的一个值，该值指定是获取准确大小还是近似大小。 只有三个值有效： cssAccurate、cssQuick 和 cssDiscardTransientCAs：  
  
- cssAccurate 返回准确的保存大小，但需要更长的时间来计算。  
  
- cssQuick 返回大小，为安全起见，但计算时间较少。  
  
- cssDiscardTransientCAs 告知 `GetSaveSize` 它可以丢弃可放弃的自定义属性。  
  
 `pdwSaveSize`  
 弄一个指针，指向保存该文件所需的大小。  
  
## <a name="remarks"></a>备注  
 `GetSaveSize` 计算在当前作用域中保存程序集及其所有元数据所需的空间（以字节为单位）。 （对[IMetaDataEmit：： SaveToStream](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-savetostream-method.md)方法的调用将发出此数目的字节。）  
  
 如果调用方实现了[IMapToken](../../../../docs/framework/unmanaged-api/metadata/imaptoken-interface.md)接口（通过[IMetaDataEmit：： SetHandler](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-sethandler-method.md)或[IMetaDataEmit：： Merge](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-merge-method.md)），`GetSaveSize` 将对元数据执行两次传递以对其进行优化和压缩。 否则，不执行任何优化。  
  
 如果执行了优化，则第一个传递将只对元数据结构进行排序，以优化导入时间搜索的性能。 此步骤通常会导致四处移动记录，并产生副作用，由工具保留的标记将会失效。 但是，在第二次传递后，元数据不会将这些令牌更改通知给调用方。 在第二次传递中，将执行各种优化，以减少元数据的总大小，例如，在引用到在当前元数据范围内声明的类型或成员时，`mdTypeRef` 和 `mdMemberRef` 令牌进行优化。 在此阶段中，会发生另一轮标记映射。 此次传递后，元数据引擎通过其 `IMapToken` 接口通知调用方所有已更改的令牌值。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 Mscoree.dll 中的资源  
  
 **.NET Framework 版本：** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a>另请参阅

- [IMetaDataEmit Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataEmit2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
