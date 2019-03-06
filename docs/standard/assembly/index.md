---
title: .NET 中的程序集
ms.date: 07/10/2018
ms.assetid: 149f5ca5-5b34-4746-9542-1ae43b2d0256
---
# <a name="assemblies-in-net"></a><span data-ttu-id="e9559-102">.NET 中的程序集</span><span class="sxs-lookup"><span data-stu-id="e9559-102">Assemblies in .NET</span></span>

<span data-ttu-id="e9559-103">程序集构成了 .NET 应用程序的部署、版本控制、重用、激活范围和安全权限的基本单元。</span><span class="sxs-lookup"><span data-stu-id="e9559-103">Assemblies form the fundamental unit of deployment, version control, reuse, activation scoping, and security permissions for a .NET-based application.</span></span> <span data-ttu-id="e9559-104">作为 .NET 应用程序 的构建基块，程序集采用可执行文件 (.exe) 或动态链接库文件 (.dll) 的形式。</span><span class="sxs-lookup"><span data-stu-id="e9559-104">Assemblies take the form of an executable (.exe) file or dynamic link library (.dll) file, and are the building blocks of the .NET applications.</span></span> <span data-ttu-id="e9559-105">它们向公共语言运行时提供了注意类型实现代码所需的信息。</span><span class="sxs-lookup"><span data-stu-id="e9559-105">They provide the common language runtime with the information it needs to be aware of type implementations.</span></span> <span data-ttu-id="e9559-106">可以将程序集视为一组构成功能逻辑单元并旨在配合使用的类型和资源。</span><span class="sxs-lookup"><span data-stu-id="e9559-106">You can think of an assembly as a collection of types and resources that form a logical unit of functionality and are built to work together.</span></span>  
  
 <span data-ttu-id="e9559-107">在 .NET Core 和 .NET Framework 中，可以从一个或多个源代码文件生成程序集。</span><span class="sxs-lookup"><span data-stu-id="e9559-107">In .NET Core and .NET Framework, an assembly can be built from one or more source code files.</span></span> <span data-ttu-id="e9559-108">在 .NET Framework 中，程序集可以包含一个或多个模块。</span><span class="sxs-lookup"><span data-stu-id="e9559-108">In .NET Framework, assemblies can contain one or more modules.</span></span> <span data-ttu-id="e9559-109">因此，可以将大型项目规划为，由多个开发者单独开发各个源代码文件或模块，最后整合所有这些内容以创建一个程序集。</span><span class="sxs-lookup"><span data-stu-id="e9559-109">This allows larger projects to be planned in such a way that several individual developers work on separate source code files or modules, which are combined to create a single assembly.</span></span> <span data-ttu-id="e9559-110">若要详细了解模块，请参阅[操作说明：生成多文件程序集](../../framework/app-domains/how-to-build-a-multifile-assembly.md)。</span><span class="sxs-lookup"><span data-stu-id="e9559-110">For more information about modules, see [How to: Build a Multifile Assembly](../../framework/app-domains/how-to-build-a-multifile-assembly.md).</span></span>
  
 <span data-ttu-id="e9559-111">程序集具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="e9559-111">Assemblies have the following properties:</span></span>  
  
-   <span data-ttu-id="e9559-112">程序集以 .exe 或 .dll 文件的形式实现。</span><span class="sxs-lookup"><span data-stu-id="e9559-112">Assemblies are implemented as .exe or .dll files.</span></span>  
  
-   <span data-ttu-id="e9559-113">对于面向 .NET Framework 的库，可以将程序集放入[全局程序集缓存](../../framework/app-domains/gac.md)，以便在应用程序之间共享程序集。</span><span class="sxs-lookup"><span data-stu-id="e9559-113">For libraries that target the .NET Framework, you can share an assembly between applications by putting it in the [global assembly cache](../../framework/app-domains/gac.md).</span></span> <span data-ttu-id="e9559-114">必须先为程序集命名强名称，然后才能将其添加到全局程序集缓存中。</span><span class="sxs-lookup"><span data-stu-id="e9559-114">Assemblies must be strong-named before they can be included in the global assembly cache.</span></span> <span data-ttu-id="e9559-115">有关详细信息，请参阅[具有强名称的程序集](../../framework/app-domains/strong-named-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="e9559-115">For more information, see [Strong-Named Assemblies](../../framework/app-domains/strong-named-assemblies.md).</span></span>  
  
-   <span data-ttu-id="e9559-116">只有在需要使用时才会将程序集加载到内存中。</span><span class="sxs-lookup"><span data-stu-id="e9559-116">Assemblies are only loaded into memory if they are required.</span></span> <span data-ttu-id="e9559-117">如果不使用，就不会加载程序集。</span><span class="sxs-lookup"><span data-stu-id="e9559-117">If they are not used, they are not loaded.</span></span> <span data-ttu-id="e9559-118">也就是说，使用程序集，可以在大型项目中高效管理资源。</span><span class="sxs-lookup"><span data-stu-id="e9559-118">This means that assemblies can be an efficient way to manage resources in larger projects.</span></span>  
  
-   <span data-ttu-id="e9559-119">可以使用反射，以编程方式获取程序集的相关信息。</span><span class="sxs-lookup"><span data-stu-id="e9559-119">You can programmatically obtain information about an assembly by using reflection.</span></span> <span data-ttu-id="e9559-120">有关详细信息，请参阅[反射 (C#)](../../csharp/programming-guide/concepts/reflection.md) 或[反射 (Visual Basic)](../../visual-basic/programming-guide/concepts/reflection.md)。</span><span class="sxs-lookup"><span data-stu-id="e9559-120">For more information, see [Reflection (C#)](../../csharp/programming-guide/concepts/reflection.md) or [Reflection (Visual Basic)](../../visual-basic/programming-guide/concepts/reflection.md).</span></span>   
  
-   <span data-ttu-id="e9559-121">只能通过调用方法 <xref:System.Reflection.Assembly.ReflectionOnlyLoadFrom%2A?displayProperty=nameWithType> 来加载程序集以检查它。</span><span class="sxs-lookup"><span data-stu-id="e9559-121">You can load an assembly only to inspect it by calling a method <xref:System.Reflection.Assembly.ReflectionOnlyLoadFrom%2A?displayProperty=nameWithType>.</span></span>  
  
## <a name="assembly-manifest"></a><span data-ttu-id="e9559-122">程序集清单</span><span class="sxs-lookup"><span data-stu-id="e9559-122">Assembly manifest</span></span>  
 <span data-ttu-id="e9559-123">每个程序集中都有*程序集清单*。</span><span class="sxs-lookup"><span data-stu-id="e9559-123">Within every assembly is an *assembly manifest*.</span></span> <span data-ttu-id="e9559-124">与目录类似，程序集清单包含以下内容：</span><span class="sxs-lookup"><span data-stu-id="e9559-124">Similar to a table of contents, the assembly manifest contains the following:</span></span>  
  
-   <span data-ttu-id="e9559-125">程序集的标识（名称和版本）。</span><span class="sxs-lookup"><span data-stu-id="e9559-125">The assembly's identity (its name and version).</span></span>  
  
-   <span data-ttu-id="e9559-126">文件表，描述构成程序集的其他所有文件（例如，.exe 或 .dll 文件依赖的所创建的其他程序集、位图或自述文件）。</span><span class="sxs-lookup"><span data-stu-id="e9559-126">A file table describing all the other files that make up the assembly, such as other assemblies you created that your .exe or .dll file relies on, or even bitmap or Readme files.</span></span>  
  
-   <span data-ttu-id="e9559-127">程序集引用列表，列出了应用程序需要的可能由其他人创建的所有外部依赖项（.dll 或其他文件）。</span><span class="sxs-lookup"><span data-stu-id="e9559-127">An *assembly reference list*, which is a list of all external dependencies — .dlls or other files your application needs that may have been created by someone else.</span></span> <span data-ttu-id="e9559-128">程序集既可以引用全局对象，也可以引用私有对象。</span><span class="sxs-lookup"><span data-stu-id="e9559-128">Assembly references contain references to both global and private objects.</span></span> <span data-ttu-id="e9559-129">全局对象可用于所有其他应用程序。</span><span class="sxs-lookup"><span data-stu-id="e9559-129">Global objects are available to all other applications.</span></span> <span data-ttu-id="e9559-130">在 .NET Core 中，它们与特定的 .NET Core 运行时结合使用。</span><span class="sxs-lookup"><span data-stu-id="e9559-130">In .NET Core, they are coupled with a particular .NET Core runtime.</span></span> <span data-ttu-id="e9559-131">在 .NET Framework 中，它们位于全局程序集缓存中。</span><span class="sxs-lookup"><span data-stu-id="e9559-131">In .NET Framework, they reside in the global assembly cache.</span></span> <span data-ttu-id="e9559-132"><xref:System.IO?displayProperty=nameWithType> 命名空间是全局程序集缓存中的程序集示例。</span><span class="sxs-lookup"><span data-stu-id="e9559-132">The <xref:System.IO?displayProperty=nameWithType> namespace is an example of an assembly in the global assembly cache.</span></span> <span data-ttu-id="e9559-133">私有对象必须位于级别不高于应用程序安装目录的目录中。</span><span class="sxs-lookup"><span data-stu-id="e9559-133">Private objects must be in a directory at either the same level as or below the directory in which your application is installed.</span></span>  
  
 <span data-ttu-id="e9559-134">由于程序集包含内容、版本控制和依赖项的相关信息，因此，使用它们的应用程序不依赖 Windows 注册表值也能正常运行。</span><span class="sxs-lookup"><span data-stu-id="e9559-134">Because assemblies contain information about content, versioning, and dependencies, the applications that use them need not rely don Windows registry values to function properly.</span></span> <span data-ttu-id="e9559-135">程序集减少了 .dll 冲突，让应用程序变得更可靠、更易于部署。</span><span class="sxs-lookup"><span data-stu-id="e9559-135">Assemblies reduce .dll conflicts and make your applications more reliable and easier to deploy.</span></span> <span data-ttu-id="e9559-136">在许多情况下，只需将 .NET 应用程序的文件复制到目标计算机，即可进行安装。</span><span class="sxs-lookup"><span data-stu-id="e9559-136">In many cases, you can install a .NET-based application simply by copying its files to the target computer.</span></span> <span data-ttu-id="e9559-137">有关详细信息，请参阅[程序集清单](../../framework/app-domains/assembly-manifest.md)。</span><span class="sxs-lookup"><span data-stu-id="e9559-137">For more information, see [Assembly Manifest](../../framework/app-domains/assembly-manifest.md).</span></span>  
  
## <a name="adding-a-reference-to-an-assembly"></a><span data-ttu-id="e9559-138">添加对程序集的引用</span><span class="sxs-lookup"><span data-stu-id="e9559-138">Adding a reference to an assembly</span></span>  
 <span data-ttu-id="e9559-139">必须添加对程序集的引用，才能使用程序集。</span><span class="sxs-lookup"><span data-stu-id="e9559-139">To use an assembly, you must add a reference to it.</span></span> <span data-ttu-id="e9559-140">接下来，可以对 C# 使用 [using 指令](../../csharp/language-reference/keywords/using-directive.md)，或者对 Visual Basic 使用 [Imports 语句](../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)，从而选择要使用的项的命名空间。</span><span class="sxs-lookup"><span data-stu-id="e9559-140">Next, you can use the [using directive](../../csharp/language-reference/keywords/using-directive.md) for C# or [Imports statement](../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) for Visual Basic to choose the namespace of the items you want to use.</span></span> <span data-ttu-id="e9559-141">引用和导入程序集后，应用程序可以使用其名称空间的所有可访问类型、属性、方法和其他成员，就好像它们的代码是源文件的一部分一样。</span><span class="sxs-lookup"><span data-stu-id="e9559-141">Once an assembly is referenced and imported, all the accessible types, properties, methods, and other members of its namespaces are available to your application as if their code were part of your source file.</span></span>  
 
> [!NOTE]
> <span data-ttu-id="e9559-142">.NET 类库中的大多数程序集都是自动引用的。</span><span class="sxs-lookup"><span data-stu-id="e9559-142">Most assemblies from the .NET Class Library are referenced automatically.</span></span> <span data-ttu-id="e9559-143">但是，在某些情况下，系统程序集可能不会自动引用。</span><span class="sxs-lookup"><span data-stu-id="e9559-143">In some cases, though, a system assembly may not automatically be referenced.</span></span> <span data-ttu-id="e9559-144">在 .NET Core 中，可以通过在 Visual Studio 中使用 NuGet 包管理器或者通过向 \*.csproj 或 \*.vbproj 项目添加程序集的 [<PackageReference>](../../core/tools/dependencies.md#the-new-packagereference-element) 元素的方式，添加对包含该程序集的 NuGet 包的引用。</span><span class="sxs-lookup"><span data-stu-id="e9559-144">In .NET Core, you can add a reference to the NuGet package that contains the assembly either by using NuGet Package Manager in Visual Studio or by adding a [<PackageReference>](../../core/tools/dependencies.md#the-new-packagereference-element) element for the assembly to the \*.csproj or \*.vbproj project.</span></span> <span data-ttu-id="e9559-145">在 .NET Framework 中，可以通过在 Visual Studio 中使用“添加引用”对话框，或者通过使用 [C#](../../csharp/language-reference/compiler-options/reference-compiler-option.md) 或 [Visual Basic](../../visual-basic/reference/command-line-compiler/reference.md) 编译器的 `-reference` 命令行选项的方式，添加对该程序集的引用。</span><span class="sxs-lookup"><span data-stu-id="e9559-145">In .NET Framework, you can add a reference to the assembly by using the **Add Reference** dialog in Visual Studio or by using the `-reference` command line option for the [C#](../../csharp/language-reference/compiler-options/reference-compiler-option.md) or [Visual Basic](../../visual-basic/reference/command-line-compiler/reference.md) compilers.</span></span>
 
 <span data-ttu-id="e9559-146">在 C# 中，还可以在单个应用程序中使用同一程序集的两个版本。</span><span class="sxs-lookup"><span data-stu-id="e9559-146">In C#, you can also use two versions of the same assembly in a single application.</span></span> <span data-ttu-id="e9559-147">有关详细信息，请参阅[外部别名](../../csharp/language-reference/keywords/extern-alias.md)。</span><span class="sxs-lookup"><span data-stu-id="e9559-147">For more information, see [extern alias](../../csharp/language-reference/keywords/extern-alias.md).</span></span>  
  
## <a name="creating-an-assembly"></a><span data-ttu-id="e9559-148">创建程序集</span><span class="sxs-lookup"><span data-stu-id="e9559-148">Creating an assembly</span></span>  
 <span data-ttu-id="e9559-149">编译应用程序有以下几种方式：在 Visual Studio 中生成程序集，使用 .NET Core 命令行界面 (CLI) 工具从命令行生成程序集，或者使用命令行编译器生成 .NET Framework 程序集。</span><span class="sxs-lookup"><span data-stu-id="e9559-149">Compile your application by building it in Visual Studio, by building it from the command line by using .NET Core command-line interface (CLI) tools, or by building .NET Framework assemblies with a command-line compiler.</span></span> <span data-ttu-id="e9559-150">要详细了解如何使用.NET CLI 工具生成程序集，请参阅 [.NET Core 命令行接口 (CLI) 工具](../../core/tools/index.md)。</span><span class="sxs-lookup"><span data-stu-id="e9559-150">For more information about building assemblies using .NET CLI tools, see [.NET Core command-line interface (CLI) tools](../../core/tools/index.md).</span></span> <span data-ttu-id="e9559-151">要了解如何使用命令行编译器生成程序集，请参阅[使用 csc.exe 的命令行生成](../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)（适用于 C#），以及[从命令行生成](../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md)（适用于 Visual Basic）。</span><span class="sxs-lookup"><span data-stu-id="e9559-151">For building assemblies with the command-line compilers, see [Command-line build with csc.exe](../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md) for C# and [Building from the Command Line](../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) for Visual Basic.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e9559-152">若要在 Visual Studio 中生成程序集，请选择“生成”菜单上的“生成”。</span><span class="sxs-lookup"><span data-stu-id="e9559-152">To build an assembly in Visual Studio, on the **Build** menu choose **Build**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e9559-153">请参阅</span><span class="sxs-lookup"><span data-stu-id="e9559-153">See also</span></span>

 - [<span data-ttu-id="e9559-154">.NET 程序集文件格式</span><span class="sxs-lookup"><span data-stu-id="e9559-154">.NET assembly file format</span></span>](file-format.md)
 - <span data-ttu-id="e9559-155">[Assemblies in the Common Language Runtime](../../framework/app-domains/assemblies-in-the-common-language-runtime.md)（公共语言运行时中的程序集）</span><span class="sxs-lookup"><span data-stu-id="e9559-155">[Assemblies in the Common Language Runtime](../../framework/app-domains/assemblies-in-the-common-language-runtime.md)</span></span>  
 - [<span data-ttu-id="e9559-156">友元程序集 (C#)</span><span class="sxs-lookup"><span data-stu-id="e9559-156">Friend Assemblies (C#)</span></span>](../../csharp/programming-guide/concepts/assemblies-gac/friend-assemblies.md)  
 - [<span data-ttu-id="e9559-157">友元程序集 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e9559-157">Friend Assemblies (Visual Basic)</span></span>](../../visual-basic/programming-guide/concepts/assemblies-gac/friend-assemblies.md)  
 - [<span data-ttu-id="e9559-158">如何：加载和卸载程序集 (C#)</span><span class="sxs-lookup"><span data-stu-id="e9559-158">How to: Load and Unload Assemblies (C#)</span></span>](../../csharp/programming-guide/concepts/assemblies-gac/how-to-load-and-unload-assemblies.md)  
 - [<span data-ttu-id="e9559-159">如何：加载和卸载程序集 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e9559-159">How to: Load and Unload Assemblies (Visual Basic)</span></span>](../../visual-basic/programming-guide/concepts/assemblies-gac/how-to-load-and-unload-assemblies.md)  
 - [<span data-ttu-id="e9559-160">如何：在 .NET Core 中使用和调试程序集可卸载性</span><span class="sxs-lookup"><span data-stu-id="e9559-160">How to: Use and Debug Assembly Unloadability in .NET Core</span></span>](unloadability-howto.md)
 - [<span data-ttu-id="e9559-161">如何：确定文件是否为程序集 (C#)</span><span class="sxs-lookup"><span data-stu-id="e9559-161">How to: Determine If a File Is an Assembly (C#)</span></span>](../../csharp/programming-guide/concepts/assemblies-gac/how-to-determine-if-a-file-is-an-assembly.md)  
 - [<span data-ttu-id="e9559-162">如何：确定文件是否为程序集 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e9559-162">How to: Determine If a File Is an Assembly (Visual Basic)</span></span>](../../visual-basic/programming-guide/concepts/assemblies-gac/how-to-determine-if-a-file-is-an-assembly.md)  