---
title: <typeparamref> - C# 编程指南
ms.date: 07/20/2015
f1_keywords:
- typeparamref
helpviewer_keywords:
- typeparamref C# XML tag
- <typeparamref> C# XML tag
ms.assetid: 6d8ffc58-12c5-4688-8db6-833a7ded5886
ms.openlocfilehash: 266eadad322fd3c4167c7a911cb57ef1e1333012
ms.sourcegitcommit: 13e79efdbd589cad6b1de634f5d6b1262b12ab01
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2020
ms.locfileid: "76789661"
---
# <a name="typeparamref-c-programming-guide"></a>\<typeparamref>（C# 编程指南）

## <a name="syntax"></a>语法

```xml
<typeparamref name="name"/>
```

## <a name="parameters"></a>参数

- `name`

  类型参数的名称。 用双引号 (" ") 将名称引起来。

## <a name="remarks"></a>备注

有关泛型类型中的类型参数及方法的详细信息，请参阅[泛型](../generics/index.md)。

通过此标记，文档文件的使用者可显著设置字体格式，例如采用斜体。

使用 [-doc](../../language-reference/compiler-options/doc-compiler-option.md) 进行编译以便将文档注释处理到文件中。

## <a name="example"></a>示例

[!code-csharp[csProgGuideDocComments#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#13)]

## <a name="see-also"></a>请参阅

- [C# 编程指南](../index.md)
- [建议的文档注释标记](./recommended-tags-for-documentation-comments.md)
