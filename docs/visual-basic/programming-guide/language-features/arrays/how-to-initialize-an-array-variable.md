---
title: 如何：初始化数组变量
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], initializing
- arrays [Visual Basic], variables
- arrays [Visual Basic], initializing
- arrays [Visual Basic], declaring
ms.assetid: aadd7a60-7ca4-4608-b986-091f19e7fc10
ms.openlocfilehash: 509859cbec41ca31b3abaa1c739e2975ec93bc0e
ms.sourcegitcommit: 17ee6605e01ef32506f8fdc686954244ba6911de
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2019
ms.locfileid: "74351881"
---
# <a name="how-to-initialize-an-array-variable-in-visual-basic"></a>如何：在 Visual Basic 中初始化数组变量
通过在 `New` 子句中包含数组文本并指定数组的初始值来初始化数组变量。 可以指定类型，也可以允许从数组文本中的值推断。 有关如何推断类型的详细信息，请参阅[数组](../../../../visual-basic/programming-guide/language-features/arrays/index.md)中的 "使用初始值填充数组"。  
  
### <a name="to-initialize-an-array-variable-by-using-an-array-literal"></a>使用数组文本初始化数组变量  
  
- 在 `New` 子句中，或在分配数组值时，提供大括号（`{}`）中的元素值。 下面的示例演示多个声明、创建和初始化一个变量以包含包含类型 `Char`的元素的数组的方式。  
  
     [!code-vb[VbVbalrArrays#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#16)]  
  
     执行每个语句后，创建的数组的长度为3，索引0到索引2的元素包含初始值。 如果同时提供上限和值，则必须为从索引0到上限的每个元素包含一个值。  
  
     请注意，如果在数组文本中提供元素值，则无需指定索引上限。 如果未指定上限，则将根据数组文本中的值的数目推断数组的大小。  
  
### <a name="to-initialize-a-multidimensional-array-variable-by-using-array-literals"></a>使用数组文本初始化多维数组变量  
  
- 将值括在大括号（`{}`）中的大括号内。 确保嵌套的数组文本都推导为相同类型和长度的数组。 下面的代码示例演示了多维数组初始化的几个示例。  
  
     [!code-vb[VbVbalrArrays#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#17)]  
  
- 可以显式指定数组界限，或将其保留，让编译器根据数组文本中的值推断数组界限。 如果同时提供上限和值，则必须在每个维度的索引0到上限中包含每个元素的值。 下面的示例演示多个声明、创建和初始化一个变量，使其包含一个具有类型元素的二维数组的方法 `Short`  
  
     [!code-vb[VbVbalrArrays#18](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#18)]  
  
     执行每个语句后，创建的数组包含六个初始化的元素，这些元素具有索引 `(0,0)`、`(0,1)`、`(0,2)`、`(1,0)`、`(1,1)`和 `(1,2)`。 每个阵列位置都包含 `10`的值。  
  
- 下面的示例循环访问一个多维数组。 在 Visual Basic 编写的 Windows 控制台应用程序中，将代码粘贴到 `Sub Main()` 方法中。 最后一个注释显示输出。  
  
     [!code-vb[VbVbalrArrays#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#31)]  
  
### <a name="to-initialize-a-jagged-array-variable-by-using-array-literals"></a>使用数组文本初始化交错数组变量  
  
- 将对象值嵌套在大括号内（`{}`）。 尽管还可以嵌套指定不同长度数组的数组文本（对于交错数组），但请确保嵌套的数组文本括在括号中（`()`）。 圆括号会强制计算嵌套的数组文本，并将生成的数组用作交错数组的初始值。 下面的代码示例演示了交错数组初始化的两个示例。  
  
     [!code-vb[VbVbalrArrays#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#19)]  
  
- 下面的示例循环访问交错数组。 在 Visual Basic 编写的 Windows 控制台应用程序中，将代码粘贴到 `Sub Main()` 方法中。  代码中的最后一个注释显示输出。  
  
     [!code-vb[VbVbalrArrays#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#32)]  
  
## <a name="see-also"></a>另请参阅

- [数组](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [数组疑难解答](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)
