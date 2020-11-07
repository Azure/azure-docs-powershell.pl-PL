---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 6720f4eb323d0050cacd9656fc14559da24ecf81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710333"
---
# <span data-ttu-id="1bba6-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="1bba6-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="1bba6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1bba6-102">SYNOPSIS</span></span>
<span data-ttu-id="1bba6-103">Wyłącza szyfrowanie na maszynie wirtualnej IaaS.</span><span class="sxs-lookup"><span data-stu-id="1bba6-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="1bba6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1bba6-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bba6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1bba6-105">DESCRIPTION</span></span>
<span data-ttu-id="1bba6-106">Polecenie cmdlet **disable-AzVMDiskEncryption** wyłącza szyfrowanie infrastruktury jako maszynę wirtualną usługi (IaaS).</span><span class="sxs-lookup"><span data-stu-id="1bba6-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="1bba6-107">To polecenie cmdlet jest obsługiwane tylko na maszynach wirtualnych systemu Windows, a nie na maszynach wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="1bba6-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="1bba6-108">To polecenie cmdlet powoduje zainstalowanie rozszerzenia na maszynie wirtualnej w celu wyłączenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="1bba6-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="1bba6-109">Jeśli parametr *name* nie jest określony, zostanie utworzona rozszerzenie z nazwą domyślną "AzureDiskEncryption for Windows VMS".</span><span class="sxs-lookup"><span data-stu-id="1bba6-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="1bba6-110">Uwaga: to polecenie cmdlet powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1bba6-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="1bba6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1bba6-111">EXAMPLES</span></span>

### <span data-ttu-id="1bba6-112">Przykład 1: wyłączanie szyfrowania dla wszystkich woluminów na maszynie wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="1bba6-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="1bba6-113">To polecenie wyłącza szyfrowanie woluminów typu all dla maszyny wirtualnej o nazwie VM002 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="1bba6-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="1bba6-114">Ponieważ parametr *volumetype* nie jest określony, polecenie cmdlet ustawia wartość All (wszystko).</span><span class="sxs-lookup"><span data-stu-id="1bba6-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="1bba6-115">Przykład 2: wyłączanie szyfrowania dla woluminów danych na maszynie wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="1bba6-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="1bba6-116">To polecenie wyłącza szyfrowanie woluminów typu dane dla maszyny wirtualnej o nazwie VM004 należącej do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="1bba6-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="1bba6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1bba6-117">PARAMETERS</span></span>

### <span data-ttu-id="1bba6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bba6-118">-DefaultProfile</span></span>
<span data-ttu-id="1bba6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1bba6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bba6-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1bba6-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1bba6-121">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1bba6-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="1bba6-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="1bba6-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="1bba6-123">Nazwa wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1bba6-123">The extension publisher name.</span></span> <span data-ttu-id="1bba6-124">Ten parametr można określić tylko w celu zastąpienia wartości domyślnej "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="1bba6-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="1bba6-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="1bba6-125">-ExtensionType</span></span>
<span data-ttu-id="1bba6-126">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1bba6-126">The extension type.</span></span> <span data-ttu-id="1bba6-127">Określ ten parametr, aby zastąpić swoją domyślną wartość "AzureDiskEncryption" dla maszyn wirtualnych systemu Windows i "AzureDiskEncryptionForLinux" dla maszyn wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="1bba6-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="1bba6-128">-Force</span><span class="sxs-lookup"><span data-stu-id="1bba6-128">-Force</span></span>
<span data-ttu-id="1bba6-129">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1bba6-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1bba6-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1bba6-130">-Name</span></span>
<span data-ttu-id="1bba6-131">Specifes nazwę zasobu Menedżera zasobów platformy Azure (ARM), który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="1bba6-131">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="1bba6-132">Jeśli ten parametr nie jest określony, to polecenie cmdlet domyślnie przyjmuje wartość "AzureDiskEncryption for Windows VMs".</span><span class="sxs-lookup"><span data-stu-id="1bba6-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="1bba6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bba6-133">-ResourceGroupName</span></span>
<span data-ttu-id="1bba6-134">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1bba6-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="1bba6-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1bba6-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="1bba6-136">Określa wersję rozszerzenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="1bba6-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="1bba6-137">Jeśli nie określisz wartości dla tego parametru, zostanie wykorzystana Najnowsza wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1bba6-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="1bba6-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="1bba6-138">-VMName</span></span>
<span data-ttu-id="1bba6-139">Określa nazwę maszyny wirtualnej, w której to polecenie cmdlet wyłącza szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="1bba6-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="1bba6-140">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="1bba6-140">-VolumeType</span></span>
<span data-ttu-id="1bba6-141">Określa typ woluminów maszyny wirtualnej, które mają wykonać operację szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="1bba6-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="1bba6-142">W przypadku maszyn wirtualnych systemu Windows prawidłowymi wartościami są:</span><span class="sxs-lookup"><span data-stu-id="1bba6-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="1bba6-143">Cały</span><span class="sxs-lookup"><span data-stu-id="1bba6-143">All</span></span>
- <span data-ttu-id="1bba6-144">OPERACYJNYM</span><span class="sxs-lookup"><span data-stu-id="1bba6-144">OS</span></span>
- <span data-ttu-id="1bba6-145">Danymi.</span><span class="sxs-lookup"><span data-stu-id="1bba6-145">Data.</span></span>
<span data-ttu-id="1bba6-146">Jeśli nie określisz wartości dla tego parametru, wartość domyślna to All (wszystko).</span><span class="sxs-lookup"><span data-stu-id="1bba6-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="1bba6-147">Wyłączenie szyfrowania nie jest obecnie obsługiwane w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="1bba6-147">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="1bba6-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1bba6-148">-Confirm</span></span>
<span data-ttu-id="1bba6-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bba6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bba6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bba6-150">-WhatIf</span></span>
<span data-ttu-id="1bba6-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bba6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bba6-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1bba6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bba6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bba6-153">CommonParameters</span></span>
<span data-ttu-id="1bba6-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bba6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bba6-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bba6-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bba6-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bba6-156">INPUTS</span></span>

### <span data-ttu-id="1bba6-157">System. String</span><span class="sxs-lookup"><span data-stu-id="1bba6-157">System.String</span></span>

### <span data-ttu-id="1bba6-158">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1bba6-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1bba6-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1bba6-159">OUTPUTS</span></span>

### <span data-ttu-id="1bba6-160">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1bba6-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1bba6-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1bba6-161">NOTES</span></span>

## <span data-ttu-id="1bba6-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bba6-162">RELATED LINKS</span></span>

[<span data-ttu-id="1bba6-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="1bba6-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="1bba6-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1bba6-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="1bba6-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1bba6-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)

