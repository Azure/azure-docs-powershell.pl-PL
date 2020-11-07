---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 084775812a887e0cc6fe497a0e0cef46ec464956
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706258"
---
# <span data-ttu-id="aa798-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="aa798-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="aa798-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa798-102">SYNOPSIS</span></span>
<span data-ttu-id="aa798-103">Usuwa rozszerzenie szyfrowania dysku z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aa798-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="aa798-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa798-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa798-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa798-105">DESCRIPTION</span></span>
<span data-ttu-id="aa798-106">Polecenie cmdlet **Remove-AzVMDiskEncryptionExtension** usuwa rozszerzenie szyfrowanie dysku i skojarzoną konfigurację rozszerzenia z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aa798-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="aa798-107">Jeśli nie podano nazwy rozszerzenia, to polecenie cmdlet usunie rozszerzenie o nazwie domyślnej AzureDiskEncryption dla maszyn wirtualnych z uruchomionym systemem operacyjnym Windows lub AzureDiskEncryptionForLinux dla maszyn wirtualnych opartych na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="aa798-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="aa798-108">To polecenie cmdlet nie powiedzie się, jeśli szyfrowanie na maszynie wirtualnej nie zostanie najpierw wyłączone.</span><span class="sxs-lookup"><span data-stu-id="aa798-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="aa798-109">Aby wyłączyć szyfrowanie na maszynie wirtualnej, użyj [łącza Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span><span class="sxs-lookup"><span data-stu-id="aa798-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="aa798-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa798-110">EXAMPLES</span></span>

### <span data-ttu-id="aa798-111">Przykład 1: usunięcie rozszerzenia szyfrowanie dysku z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aa798-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="aa798-112">To polecenie usuwa rozszerzenie o nazwie domyślnej AzureDiskEncryption dla maszyny wirtualnej z uruchomionym systemem operacyjnym Windows lub AzureDiskEncryptionForLinux dla maszyny wirtualnej opartej na usłudze Linux o nazwie MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="aa798-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="aa798-113">Przykład 2: usunięcie określonego rozszerzenia szyfrowania dysku z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aa798-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="aa798-114">To polecenie usuwa rozszerzenie szyfrowania o nazwie MyDiskEncryptionExtension z maszyny wirtualnej o nazwie MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="aa798-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="aa798-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa798-115">PARAMETERS</span></span>

### <span data-ttu-id="aa798-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa798-116">-DefaultProfile</span></span>
<span data-ttu-id="aa798-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa798-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa798-118">-Force</span><span class="sxs-lookup"><span data-stu-id="aa798-118">-Force</span></span>
<span data-ttu-id="aa798-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="aa798-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa798-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa798-120">-Name</span></span>
<span data-ttu-id="aa798-121">Określa nazwę zasobu Menedżera zasobów Azure, który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="aa798-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="aa798-122">Polecenie cmdlet Set-AzVMDiskEncryptionExtension ustawia tę nazwę na AzureDiskEncryption dla maszyn wirtualnych z uruchomionym systemem operacyjnym Windows i AzureDiskEncryptionForLinux dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="aa798-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="aa798-123">Ten parametr należy określić tylko w przypadku zmiany nazwy domyślnej w poleceniu cmdlet **Set-AzVMDiskEncryptionExtension** lub użycia innej nazwy zasobu w szablonie Menedżera zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa798-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="aa798-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="aa798-124">-NoWait</span></span>
<span data-ttu-id="aa798-125">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="aa798-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="aa798-126">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="aa798-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa798-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa798-127">-ResourceGroupName</span></span>
<span data-ttu-id="aa798-128">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aa798-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="aa798-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="aa798-129">-VMName</span></span>
<span data-ttu-id="aa798-130">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aa798-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="aa798-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa798-131">-Confirm</span></span>
<span data-ttu-id="aa798-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa798-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa798-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa798-133">-WhatIf</span></span>
<span data-ttu-id="aa798-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa798-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa798-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa798-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa798-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa798-136">CommonParameters</span></span>
<span data-ttu-id="aa798-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa798-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa798-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa798-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa798-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa798-139">INPUTS</span></span>

### <span data-ttu-id="aa798-140">System. String</span><span class="sxs-lookup"><span data-stu-id="aa798-140">System.String</span></span>

## <span data-ttu-id="aa798-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa798-141">OUTPUTS</span></span>

### <span data-ttu-id="aa798-142">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="aa798-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="aa798-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa798-143">NOTES</span></span>

## <span data-ttu-id="aa798-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa798-144">RELATED LINKS</span></span>

[<span data-ttu-id="aa798-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="aa798-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="aa798-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="aa798-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


