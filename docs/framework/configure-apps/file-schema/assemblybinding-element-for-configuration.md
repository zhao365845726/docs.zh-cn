---
title: <configuration> 的 <assemblyBinding> 元素
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/assemblyBinding
helpviewer_keywords:
- assemblyBinding Element
- <assemblyBinding> Element
ms.assetid: 6cc55983-b894-449b-8e26-b258e53939cd
ms.openlocfilehash: e0b83c4b3573ab6819654e72cac1bf3e4a0ba637
ms.sourcegitcommit: 68653db98c5ea7744fd438710248935f70020dfb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2019
ms.locfileid: "69921278"
---
# <a name="assemblybinding-element-for-configuration"></a>\<用于配置 > 的\<assemblyBinding > 元素

指定配置级的程序集绑定策略。

[ **\<configuration>** ](configuration-element.md)   
&nbsp;&nbsp; **\<assemblyBinding>**

## <a name="syntax"></a>语法

```xml
<assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
  <!-- Configuration files to include. -->
</assemblyBinding>
```

## <a name="attribute"></a>特性

|           | 描述 |
| --------- | ----------- |
| **xmlns** | 必需的特性。<br><br>指定程序集绑定所需的 XML 命名空间。 使用字符串“urn: 架构-microsoft-com:asm.v1”作为值。 |

## <a name="parent-element"></a>父元素

|     | 描述 |
| --- | ----------- |
| [ **\<configuration>** ](configuration-element.md) | 公共语言运行时和 .NET Framework 应用程序所使用的每个配置文件中的根元素。 |

## <a name="child-element"></a>子元素

|     | 描述 |
| --- | ----------- |
| [ **\<linkedConfiguration>** ](linkedconfiguration-element.md) | 指定要包含的配置文件。 |

## <a name="remarks"></a>备注

LinkedConfiguration > 元素通过允许应用程序配置文件在已知位置中包含程序集配置文件来简化组件程序集的管理, 而不是复制程序集[ **\<** ](linkedconfiguration-element.md)配置设置。

> [!NOTE]
> 对于具有 Windows 并行清单的应用程序, 不支持 **linkedConfiguration>元素。\<**

## <a name="example"></a>示例

下面的示例演示如何在本地硬盘上包含配置文件:

```xml
<configuration>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
    <linkedConfiguration href="file://c:\Program Files\Contoso\sharedConfig.xml" />
  </assemblyBinding>
</configuration>
```

## <a name="see-also"></a>请参阅

- [.NET Framework 的配置文件架构](index.md)
