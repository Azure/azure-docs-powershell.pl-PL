---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 087ae12961d6bd9faf844221772b92c79362d13d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545799"
---
# <span data-ttu-id="bba19-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="bba19-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="bba19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bba19-102">SYNOPSIS</span></span>
<span data-ttu-id="bba19-103">Wyłącza szyfrowanie na maszynie wirtualnej IaaS.</span><span class="sxs-lookup"><span data-stu-id="bba19-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bba19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bba19-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bba19-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bba19-105">DESCRIPTION</span></span>
<span data-ttu-id="bba19-106">Polecenie cmdlet **disable-AzureRmVMDiskEncryption** wyłącza szyfrowanie infrastruktury jako maszynę wirtualną usługi (IaaS).</span><span class="sxs-lookup"><span data-stu-id="bba19-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="bba19-107">To polecenie cmdlet jest obsługiwane tylko na maszynach wirtualnych systemu Windows, a nie na maszynach wirtualnych Linux.</span><span class="sxs-lookup"><span data-stu-id="bba19-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="bba19-108">To polecenie cmdlet powoduje zainstalowanie rozszerzenia na maszynie wirtualnej w celu wyłączenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="bba19-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="bba19-109">Jeśli parametr *name* nie jest określony, zostanie utworzona rozszerzenie z nazwą domyślną "AzureDiskEncryption for Windows VMS".</span><span class="sxs-lookup"><span data-stu-id="bba19-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="bba19-110">Uwaga: to polecenie cmdlet powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bba19-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="bba19-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bba19-111">EXAMPLES</span></span>

### <span data-ttu-id="bba19-112">Przykład 1: wyłączanie szyfrowania dla wszystkich woluminów na maszynie wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="bba19-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="bba19-113">To polecenie wyłącza szyfrowanie woluminów typu all dla maszyny wirtualnej o nazwie VM002 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="bba19-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="bba19-114">Ponieważ parametr *volumetype* nie jest określony, polecenie cmdlet ustawia wartość All (wszystko).</span><span class="sxs-lookup"><span data-stu-id="bba19-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="bba19-115">Przykład 2: wyłączanie szyfrowania dla woluminów danych na maszynie wirtualnej systemu Windows</span><span class="sxs-lookup"><span data-stu-id="bba19-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="bba19-116">To polecenie wyłącza szyfrowanie woluminów typu dane dla maszyny wirtualnej o nazwie VM004 należącej do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="bba19-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="bba19-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bba19-117">PARAMETERS</span></span>

### <span data-ttu-id="bba19-118">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bba19-118">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bba19-119">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bba19-119">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba19-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bba19-120">-Force</span></span>
<span data-ttu-id="bba19-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bba19-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba19-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bba19-122">-Name</span></span>
<span data-ttu-id="bba19-123">Specifes nazwę zasobu Menedżera zasobów platformy Azure (ARM), który reprezentuje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="bba19-123">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="bba19-124">Jeśli ten parametr nie jest określony, to polecenie cmdlet domyślnie przyjmuje wartość "AzureDiskEncryption for Windows VMs".</span><span class="sxs-lookup"><span data-stu-id="bba19-124">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba19-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba19-125">-ResourceGroupName</span></span>
<span data-ttu-id="bba19-126">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bba19-126">Specifies the resource group name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba19-127">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bba19-127">-TypeHandlerVersion</span></span>
<span data-ttu-id="bba19-128">Określa wersję rozszerzenia szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="bba19-128">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="bba19-129">Jeśli nie określisz wartości dla tego parametru, zostanie wykorzystana Najnowsza wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bba19-129">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba19-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="bba19-130">-VMName</span></span>
<span data-ttu-id="bba19-131">Określa nazwę maszyny wirtualnej, w której to polecenie cmdlet wyłącza szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="bba19-131">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba19-132">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="bba19-132">-VolumeType</span></span>
<span data-ttu-id="bba19-133">Określa typ woluminów maszyny wirtualnej, które mają wykonać operację szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="bba19-133">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="bba19-134">W przypadku maszyn wirtualnych systemu Windows prawidłowymi wartościami są:</span><span class="sxs-lookup"><span data-stu-id="bba19-134">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="bba19-135">Cały</span><span class="sxs-lookup"><span data-stu-id="bba19-135">All</span></span>
- <span data-ttu-id="bba19-136">OPERACYJNYM</span><span class="sxs-lookup"><span data-stu-id="bba19-136">OS</span></span>
- <span data-ttu-id="bba19-137">Danymi.</span><span class="sxs-lookup"><span data-stu-id="bba19-137">Data.</span></span>
<span data-ttu-id="bba19-138">Jeśli nie określisz wartości dla tego parametru, wartość domyślna to All (wszystko).</span><span class="sxs-lookup"><span data-stu-id="bba19-138">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="bba19-139">Wyłączenie szyfrowania nie jest obecnie obsługiwane w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="bba19-139">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bba19-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bba19-140">-Confirm</span></span>
<span data-ttu-id="bba19-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bba19-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba19-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba19-142">-WhatIf</span></span>
<span data-ttu-id="bba19-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bba19-143">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bba19-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bba19-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba19-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba19-145">CommonParameters</span></span>
<span data-ttu-id="bba19-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba19-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba19-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba19-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba19-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bba19-148">INPUTS</span></span>

### <span data-ttu-id="bba19-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bba19-149">None</span></span>
<span data-ttu-id="bba19-150">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="bba19-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bba19-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bba19-151">OUTPUTS</span></span>

### <span data-ttu-id="bba19-152">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bba19-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="bba19-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bba19-153">NOTES</span></span>

## <span data-ttu-id="bba19-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bba19-154">RELATED LINKS</span></span>

[<span data-ttu-id="bba19-155">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="bba19-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="bba19-156">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bba19-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="bba19-157">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="bba19-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


