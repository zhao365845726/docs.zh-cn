---
ms.openlocfilehash: 242a9952cb47d170aceffa1aa392071eb40cc6ab
ms.sourcegitcommit: d55e14eb63588830c0ba1ea95a24ce6c57ef8c8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/11/2019
ms.locfileid: "67857236"
---
### <a name="rsacng-and-dsacng-are-once-again-usable-in-partial-trust-scenarios"></a>RSACng 和 DSACng 在部分信任方案中再次可用

|   |   |
|---|---|
|详细信息|某些情况下 CngLightup（在多个更高级别的加密 API 中使用，例如 <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType>）和 <xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType> 依赖完全信任。 其中包括未断言 <xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType> 权限的 P/Invoke 和 <xref:System.Security.Cryptography.CngKey?displayProperty=nameWithType> 在其中有 <xref:System.Security.Permissions.SecurityPermissionFlag.UnmanagedCode?displayProperty=nameWithType> 权限要求的代码路径。 自 .NET Framework 4.6.2 起，CngLightup 尽可能用于切换到 <xref:System.Security.Cryptography.RSACng?displayProperty=nameWithType>。 结果，成功使用 <xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=nameWithType> 的部分信任应用开始失败并引发 <xref:System.Security.SecurityException> 异常。此更改添加所需断言，以便所有使用 CngLightup 的函数都有所需权限。|
|建议|如果 .NET Framework 4.6.2 中的此更改对部分信任应用有负面影响，请升级到 .NET Framework 4.7.1。|
|范围|边缘|
|版本|4.6.2|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Security.Cryptography.DSACng.%23ctor(System.Security.Cryptography.CngKey)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.Key?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.LegalKeySizes?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.CreateSignature(System.Byte[])?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.DSACng.VerifySignature(System.Byte[],System.Byte[])?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.%23ctor(System.Security.Cryptography.CngKey)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.Key?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.Decrypt(System.Byte[],System.Security.Cryptography.RSAEncryptionPadding)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.SignHash(System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

