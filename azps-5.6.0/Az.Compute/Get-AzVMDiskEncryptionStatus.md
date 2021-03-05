---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 7d0a7537594bb41fbcc41a7ddf457820c9b29dd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981009"
---
# <span data-ttu-id="c447b-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="c447b-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="c447b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c447b-102">SYNOPSIS</span></span>
<span data-ttu-id="c447b-103">Pobiera stan szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c447b-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="c447b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c447b-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c447b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c447b-105">DESCRIPTION</span></span>
<span data-ttu-id="c447b-106">Polecenie **cmdlet Get-AzVMCryptionStatus** pobiera stan szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c447b-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="c447b-107">Wyświetla on stan szyfrowania systemu operacyjnego i ilości danych.</span><span class="sxs-lookup"><span data-stu-id="c447b-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="c447b-108">Oprócz stanu szyfrowania jest na nim również wyświetlany tajny adres URL szyfrowania, adres URL klucza szyfrowania, identyfikatory zasobów usługi **KeyVaults,** w których znajduje się klucz szyfrowania i klucz szyfrowania dla woluminu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="c447b-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="c447b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c447b-109">EXAMPLES</span></span>

### <span data-ttu-id="c447b-110">Przykład 1. Uzyskiwanie stanu szyfrowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c447b-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="c447b-111">To polecenie otrzymuje stan szyfrowania maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJ 0001.</span><span class="sxs-lookup"><span data-stu-id="c447b-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="c447b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c447b-112">PARAMETERS</span></span>

### <span data-ttu-id="c447b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c447b-113">-DefaultProfile</span></span>
<span data-ttu-id="c447b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c447b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c447b-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="c447b-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="c447b-116">Nazwa wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="c447b-116">The extension publisher name.</span></span> <span data-ttu-id="c447b-117">Określ ten parametr, aby zastąpić wartość domyślną "Microsoft.Azure.Security".</span><span class="sxs-lookup"><span data-stu-id="c447b-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c447b-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="c447b-118">-ExtensionType</span></span>
<span data-ttu-id="c447b-119">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="c447b-119">The extension type.</span></span> <span data-ttu-id="c447b-120">Określ ten parametr, aby zastąpić jego wartość domyślną "AzureUxEncryption" dla maszyn wirtualnych systemu Windows i "AzureCryptionForLinux" dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="c447b-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c447b-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c447b-121">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c447b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c447b-122">-ResourceGroupName</span></span>
<span data-ttu-id="c447b-123">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c447b-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c447b-124">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="c447b-124">-VMName</span></span>
<span data-ttu-id="c447b-125">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c447b-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c447b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c447b-126">CommonParameters</span></span>
<span data-ttu-id="c447b-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c447b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c447b-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c447b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c447b-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c447b-129">INPUTS</span></span>

### <span data-ttu-id="c447b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c447b-130">System.String</span></span>

## <span data-ttu-id="c447b-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c447b-131">OUTPUTS</span></span>

### <span data-ttu-id="c447b-132">Microsoft.Azure.Commands.Compute.Extension.AzureCryption.AzureCryptionEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="c447b-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="c447b-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c447b-133">NOTES</span></span>

## <span data-ttu-id="c447b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c447b-134">RELATED LINKS</span></span>

[<span data-ttu-id="c447b-135">Remove-AzVMCryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c447b-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="c447b-136">Set-AzVMCryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c447b-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


