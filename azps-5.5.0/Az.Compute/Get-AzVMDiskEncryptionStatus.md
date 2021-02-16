---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199331"
---
# <span data-ttu-id="88ea1-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="88ea1-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="88ea1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="88ea1-103">Pobiera stan szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88ea1-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="88ea1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88ea1-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88ea1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="88ea1-105">DESCRIPTION</span></span>
<span data-ttu-id="88ea1-106">Polecenie **cmdlet Get-AzVMCryptionStatus** pobiera stan szyfrowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88ea1-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="88ea1-107">Wyświetla on stan szyfrowania systemu operacyjnego i ilości danych.</span><span class="sxs-lookup"><span data-stu-id="88ea1-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="88ea1-108">Oprócz stanu szyfrowania jest na nim również wyświetlany tajny adres URL szyfrowania, adres URL klucza szyfrowania, identyfikatory zasobów usługi **KeyVaults,** w których znajduje się klucz szyfrowania i klucz szyfrowania dla woluminu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="88ea1-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="88ea1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88ea1-109">EXAMPLES</span></span>

### <span data-ttu-id="88ea1-110">Przykład 1. Uzyskiwanie stanu szyfrowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="88ea1-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="88ea1-111">To polecenie otrzymuje stan szyfrowania maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJ 0001.</span><span class="sxs-lookup"><span data-stu-id="88ea1-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="88ea1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88ea1-112">PARAMETERS</span></span>

### <span data-ttu-id="88ea1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ea1-113">-DefaultProfile</span></span>
<span data-ttu-id="88ea1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="88ea1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88ea1-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="88ea1-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="88ea1-116">Nazwa wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="88ea1-116">The extension publisher name.</span></span> <span data-ttu-id="88ea1-117">Określ ten parametr, aby zastąpić wartość domyślną "Microsoft.Azure.Security".</span><span class="sxs-lookup"><span data-stu-id="88ea1-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="88ea1-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="88ea1-118">-ExtensionType</span></span>
<span data-ttu-id="88ea1-119">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="88ea1-119">The extension type.</span></span> <span data-ttu-id="88ea1-120">Określ ten parametr, aby zastąpić jego wartość domyślną "AzureUxEncryption" dla maszyn wirtualnych systemu Windows i "AzureCryptionForLinux" dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="88ea1-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="88ea1-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="88ea1-121">-Name</span></span>
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

### <span data-ttu-id="88ea1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ea1-122">-ResourceGroupName</span></span>
<span data-ttu-id="88ea1-123">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88ea1-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="88ea1-124">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="88ea1-124">-VMName</span></span>
<span data-ttu-id="88ea1-125">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="88ea1-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="88ea1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ea1-126">CommonParameters</span></span>
<span data-ttu-id="88ea1-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ea1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ea1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88ea1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ea1-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88ea1-129">INPUTS</span></span>

### <span data-ttu-id="88ea1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="88ea1-130">System.String</span></span>

## <span data-ttu-id="88ea1-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88ea1-131">OUTPUTS</span></span>

### <span data-ttu-id="88ea1-132">Microsoft.Azure.Commands.Compute.Extension.AzureCryption.AzureCryptionEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="88ea1-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="88ea1-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88ea1-133">NOTES</span></span>

## <span data-ttu-id="88ea1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88ea1-134">RELATED LINKS</span></span>

[<span data-ttu-id="88ea1-135">Remove-AzVMCryptionExtension</span><span class="sxs-lookup"><span data-stu-id="88ea1-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="88ea1-136">Set-AzVMCryptionExtension</span><span class="sxs-lookup"><span data-stu-id="88ea1-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


