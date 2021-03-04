---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: bd96a26eda14770dcc7a5592e12e64e15eac02f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969434"
---
# <span data-ttu-id="2f30c-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2f30c-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="2f30c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f30c-102">SYNOPSIS</span></span>
<span data-ttu-id="2f30c-103">Wyłącza szyfrowanie na komputerze wirtualnym IaaS.</span><span class="sxs-lookup"><span data-stu-id="2f30c-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="2f30c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2f30c-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f30c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2f30c-105">DESCRIPTION</span></span>
<span data-ttu-id="2f30c-106">Polecenie cmdlet **Disable-AzVMBlockEncryption** wyłącza szyfrowanie na maszynie wirtualnej infrastruktury jako usługi (IaaS).</span><span class="sxs-lookup"><span data-stu-id="2f30c-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="2f30c-107">To polecenie cmdlet jest obsługiwane tylko w przypadku maszyn wirtualnych systemu Windows, a nie linux.</span><span class="sxs-lookup"><span data-stu-id="2f30c-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="2f30c-108">To polecenie cmdlet instaluje na komputerze wirtualnym rozszerzenie w celu wyłączenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="2f30c-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="2f30c-109">Jeśli parametr *Name* nie zostanie określony, zostanie utworzone rozszerzenie o nazwie domyślnej "AzureCryption for Windows VMs".</span><span class="sxs-lookup"><span data-stu-id="2f30c-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="2f30c-110">Przestroga: To polecenie cmdlet ponownie uruchamia maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="2f30c-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="2f30c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2f30c-111">EXAMPLES</span></span>

### <span data-ttu-id="2f30c-112">Przykład 1. Wyłączenie szyfrowania dla wszystkich woluminów na maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="2f30c-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="2f30c-113">To polecenie wyłącza szyfrowanie woluminów typu dla maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJ002, która należy do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="2f30c-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="2f30c-114">Parametr *VolumeType* nie jest określony, dlatego polecenie cmdlet ustawia wartość All (Wszystko).</span><span class="sxs-lookup"><span data-stu-id="2f30c-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="2f30c-115">Przykład 2. Wyłączenie szyfrowania woluminów danych na maszyny wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="2f30c-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="2f30c-116">To polecenie wyłącza szyfrowanie dla woluminów danych typu dla maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJ004, która należy do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="2f30c-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="2f30c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f30c-117">PARAMETERS</span></span>

### <span data-ttu-id="2f30c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f30c-118">-DefaultProfile</span></span>
<span data-ttu-id="2f30c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f30c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f30c-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2f30c-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2f30c-121">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie wersji pomocniczej rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2f30c-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f30c-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="2f30c-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="2f30c-123">Nazwa wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2f30c-123">The extension publisher name.</span></span> <span data-ttu-id="2f30c-124">Określ ten parametr, aby zastąpić wartość domyślną "Microsoft.Azure.Security".</span><span class="sxs-lookup"><span data-stu-id="2f30c-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="2f30c-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="2f30c-125">-ExtensionType</span></span>
<span data-ttu-id="2f30c-126">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2f30c-126">The extension type.</span></span> <span data-ttu-id="2f30c-127">Określ ten parametr, aby zastąpić jego wartość domyślną "AzureUxEncryption" dla maszyn wirtualnych systemu Windows i "AzureCryptionForLinux" dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="2f30c-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="2f30c-128">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2f30c-128">-Force</span></span>
<span data-ttu-id="2f30c-129">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2f30c-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2f30c-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2f30c-130">-Name</span></span>
<span data-ttu-id="2f30c-131">Określa nazwę zasobu Azure Resource Manager (ARM) reprezentującego to rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="2f30c-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="2f30c-132">Jeśli ten parametr nie zostanie określony, to polecenie cmdlet domyślnie ma wartość "AzureCryption for Windows VMs".</span><span class="sxs-lookup"><span data-stu-id="2f30c-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f30c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f30c-133">-ResourceGroupName</span></span>
<span data-ttu-id="2f30c-134">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2f30c-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="2f30c-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2f30c-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="2f30c-136">Określa wersję rozszerzenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="2f30c-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="2f30c-137">Jeśli nie określisz wartości dla tego parametru, zostanie użyta najnowsza wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2f30c-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f30c-138">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="2f30c-138">-VMName</span></span>
<span data-ttu-id="2f30c-139">Określa nazwę maszyny wirtualnej, na podstawie których to polecenie cmdlet wyłącza szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="2f30c-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="2f30c-140">- VolumeType</span><span class="sxs-lookup"><span data-stu-id="2f30c-140">-VolumeType</span></span>
<span data-ttu-id="2f30c-141">Określa typ woluminów maszyn wirtualnych do wykonania operacji szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="2f30c-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="2f30c-142">W przypadku maszyn wirtualnych systemu Windows prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="2f30c-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="2f30c-143">Wszystkie</span><span class="sxs-lookup"><span data-stu-id="2f30c-143">All</span></span>
- <span data-ttu-id="2f30c-144">System operacyjny</span><span class="sxs-lookup"><span data-stu-id="2f30c-144">OS</span></span>
- <span data-ttu-id="2f30c-145">Dane.</span><span class="sxs-lookup"><span data-stu-id="2f30c-145">Data.</span></span>
<span data-ttu-id="2f30c-146">Jeśli nie określisz wartości dla tego parametru, wartość domyślna to Wszystko.</span><span class="sxs-lookup"><span data-stu-id="2f30c-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="2f30c-147">Wyłączenie szyfrowania nie jest obecnie obsługiwane w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="2f30c-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f30c-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f30c-148">-Confirm</span></span>
<span data-ttu-id="2f30c-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2f30c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f30c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f30c-150">-WhatIf</span></span>
<span data-ttu-id="2f30c-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f30c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f30c-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2f30c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f30c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f30c-153">CommonParameters</span></span>
<span data-ttu-id="2f30c-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f30c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f30c-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f30c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f30c-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f30c-156">INPUTS</span></span>

### <span data-ttu-id="2f30c-157">System.String</span><span class="sxs-lookup"><span data-stu-id="2f30c-157">System.String</span></span>

### <span data-ttu-id="2f30c-158">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="2f30c-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f30c-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f30c-159">OUTPUTS</span></span>

### <span data-ttu-id="2f30c-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2f30c-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2f30c-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2f30c-161">NOTES</span></span>

## <span data-ttu-id="2f30c-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f30c-162">RELATED LINKS</span></span>

[<span data-ttu-id="2f30c-163">Get-AzVM GdyszytEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="2f30c-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="2f30c-164">Remove-AzVMCryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2f30c-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="2f30c-165">Set-AzVMCryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2f30c-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


