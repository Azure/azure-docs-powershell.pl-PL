---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 8bdfa0afeb5b558faa91d82df9ccdc64a0b4433c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985293"
---
# <span data-ttu-id="9275d-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="9275d-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="9275d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9275d-102">SYNOPSIS</span></span>
<span data-ttu-id="9275d-103">Usuwa rozszerzenie szyfrowania dysku z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9275d-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="9275d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9275d-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9275d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9275d-105">DESCRIPTION</span></span>
<span data-ttu-id="9275d-106">Polecenie **cmdlet Remove-AzVMCryptionExtension** usuwa rozszerzenie szyfrowania dysku i skojarzoną konfigurację rozszerzenia z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9275d-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="9275d-107">Jeśli nie zostanie określona nazwa rozszerzenia, to polecenie cmdlet usunie rozszerzenie o nazwie domyślnej Azure JakSzyfrowanieNaszycji dla maszyn wirtualnych, na których działa system operacyjny Windows, lub polecenie AzureCryptionForLinux dla maszyn wirtualnych opartych na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="9275d-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="9275d-108">To polecenie cmdlet nie powiedzie się, jeśli szyfrowanie na maszyny wirtualnej nie zostało najpierw wyłączone.</span><span class="sxs-lookup"><span data-stu-id="9275d-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="9275d-109">Aby wyłączyć szyfrowanie na komputerze wirtualnym, [użyj opcji Disable-AzVMCryptionEncryption.](./Disable-AzVMDiskEncryption.md)</span><span class="sxs-lookup"><span data-stu-id="9275d-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="9275d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9275d-110">EXAMPLES</span></span>

### <span data-ttu-id="9275d-111">Przykład 1. Usunięcie rozszerzenia szyfrowania dysku z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9275d-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="9275d-112">To polecenie usuwa rozszerzenie o nazwie domyślnej Azure Chromecryption dla maszyny wirtualnej z systemem operacyjnym Windows lub z maszyną wirtualną o nazwie MyTestVM opartą na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="9275d-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="9275d-113">Przykład 2. Usunięcie z maszyny wirtualnej konkretnego rozszerzenia szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="9275d-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="9275d-114">To polecenie usuwa rozszerzenie szyfrowania o nazwie MyCryptEncryptionExtension z maszyny wirtualnej o nazwie MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="9275d-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="9275d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9275d-115">PARAMETERS</span></span>

### <span data-ttu-id="9275d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9275d-116">-DefaultProfile</span></span>
<span data-ttu-id="9275d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9275d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9275d-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9275d-118">-Force</span></span>
<span data-ttu-id="9275d-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9275d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9275d-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9275d-120">-Name</span></span>
<span data-ttu-id="9275d-121">Określa nazwę zasobu usługi Azure Resource Manager reprezentującą to rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="9275d-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="9275d-122">Polecenie cmdlet Set-AzVMDiskEncryptionExtension ustawia tę nazwę na AzureDriveEncryption dla maszyn wirtualnych, na których działa system operacyjny Windows, oraz polecenie AzureCryptionForLinux dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="9275d-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="9275d-123">Określ ten parametr tylko w przypadku zmiany nazwy domyślnej w cmdlet **Set-AzVMCryptionExtension** lub użycia innej nazwy zasobu w szablonie Menedżer zasobów.</span><span class="sxs-lookup"><span data-stu-id="9275d-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="9275d-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9275d-124">-NoWait</span></span>
<span data-ttu-id="9275d-125">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="9275d-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9275d-126">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="9275d-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9275d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9275d-127">-ResourceGroupName</span></span>
<span data-ttu-id="9275d-128">Określa nazwę grupy zasobów dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9275d-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="9275d-129">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="9275d-129">-VMName</span></span>
<span data-ttu-id="9275d-130">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9275d-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="9275d-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9275d-131">-Confirm</span></span>
<span data-ttu-id="9275d-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9275d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9275d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9275d-133">-WhatIf</span></span>
<span data-ttu-id="9275d-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9275d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9275d-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9275d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9275d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9275d-136">CommonParameters</span></span>
<span data-ttu-id="9275d-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9275d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9275d-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9275d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9275d-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9275d-139">INPUTS</span></span>

### <span data-ttu-id="9275d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9275d-140">System.String</span></span>

## <span data-ttu-id="9275d-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9275d-141">OUTPUTS</span></span>

### <span data-ttu-id="9275d-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9275d-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9275d-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9275d-143">NOTES</span></span>

## <span data-ttu-id="9275d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9275d-144">RELATED LINKS</span></span>

[<span data-ttu-id="9275d-145">Get-AzVM GdyszytEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="9275d-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="9275d-146">Set-AzVMCryptionExtension</span><span class="sxs-lookup"><span data-stu-id="9275d-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


