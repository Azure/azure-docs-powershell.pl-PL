---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224695"
---
# <span data-ttu-id="2a0be-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="2a0be-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="2a0be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a0be-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0be-103">Dodaje rozszerzenie do VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a0be-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="2a0be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a0be-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a0be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a0be-105">DESCRIPTION</span></span>
<span data-ttu-id="2a0be-106">Polecenie cmdlet **Add-AzVmssExtension** dodaje rozszerzenie do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="2a0be-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="2a0be-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a0be-107">EXAMPLES</span></span>

### <span data-ttu-id="2a0be-108">Przykład 1: Dodawanie rozszerzenia do VMSS</span><span class="sxs-lookup"><span data-stu-id="2a0be-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="2a0be-109">To polecenie dodaje rozszerzenie do VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a0be-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="2a0be-110">Przykład 2: Dodawanie rozszerzenia do VMSS za pomocą ustawień i ustawień chronionych</span><span class="sxs-lookup"><span data-stu-id="2a0be-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="2a0be-111">To polecenie dodaje rozszerzenie do VMSS przy użyciu przykładowego skryptu bash w magazynie obiektów blob, określa adres URL magazynu obiektów blob i polecenia wykonywalnego w obszarze Ustawienia i zabezpieczenia dostęp w ustawieniach chronionych.</span><span class="sxs-lookup"><span data-stu-id="2a0be-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="2a0be-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a0be-112">PARAMETERS</span></span>

### <span data-ttu-id="2a0be-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2a0be-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2a0be-114">Wskazuje, czy wersja rozszerzenia ma być automatycznie aktualizowana do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="2a0be-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a0be-115">-DefaultProfile</span></span>
<span data-ttu-id="2a0be-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0be-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a0be-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="2a0be-117">-ForceUpdateTag</span></span>
<span data-ttu-id="2a0be-118">Jeśli wartość jest podana i jest różna od poprzedniej wartości, program obsługi rozszerzeń zostanie zmuszony do zaktualizowania, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="2a0be-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="2a0be-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a0be-119">-Name</span></span>
<span data-ttu-id="2a0be-120">Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0be-120">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="2a0be-121">-ProtectedSetting</span></span>
<span data-ttu-id="2a0be-122">Określa prywatną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="2a0be-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="2a0be-123">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="2a0be-123">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="2a0be-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="2a0be-125">Kolekcja nazw rozszerzeń, po których to rozszerzenie musi zostać zainicjowane.</span><span class="sxs-lookup"><span data-stu-id="2a0be-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-126">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="2a0be-126">-Publisher</span></span>
<span data-ttu-id="2a0be-127">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2a0be-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="2a0be-128">Gdy program Publisher zarejestruje rozszerzenie, program Publisher podaje nazwę.</span><span class="sxs-lookup"><span data-stu-id="2a0be-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="2a0be-129">Może to zrobić za pomocą polecenia cmdlet [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) w celu uzyskania wydawcy.</span><span class="sxs-lookup"><span data-stu-id="2a0be-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-130">-Setting</span><span class="sxs-lookup"><span data-stu-id="2a0be-130">-Setting</span></span>
<span data-ttu-id="2a0be-131">Określa konfigurację publiczną w postaci ciągu dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2a0be-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="2a0be-132">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="2a0be-132">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-133">-Type</span><span class="sxs-lookup"><span data-stu-id="2a0be-133">-Type</span></span>
<span data-ttu-id="2a0be-134">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2a0be-134">Specifies the extension type.</span></span>
<span data-ttu-id="2a0be-135">Aby uzyskać typ rozszerzenia, można użyć polecenia cmdlet [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) .</span><span class="sxs-lookup"><span data-stu-id="2a0be-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2a0be-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="2a0be-137">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2a0be-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="2a0be-138">Aby uzyskać wersję rozszerzenia, możesz użyć polecenia cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) .</span><span class="sxs-lookup"><span data-stu-id="2a0be-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2a0be-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2a0be-140">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="2a0be-140">Specify the VMSS object.</span></span>
<span data-ttu-id="2a0be-141">Aby utworzyć obiekt, możesz użyć [nowego-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="2a0be-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a0be-142">-Confirm</span></span>
<span data-ttu-id="2a0be-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0be-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a0be-144">-WhatIf</span></span>
<span data-ttu-id="2a0be-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0be-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a0be-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a0be-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a0be-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0be-147">CommonParameters</span></span>
<span data-ttu-id="2a0be-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a0be-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0be-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a0be-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0be-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a0be-150">INPUTS</span></span>

### <span data-ttu-id="2a0be-151">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2a0be-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2a0be-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2a0be-152">System.String</span></span>

### <span data-ttu-id="2a0be-153">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2a0be-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2a0be-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="2a0be-154">System.Object</span></span>

## <span data-ttu-id="2a0be-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a0be-155">OUTPUTS</span></span>

### <span data-ttu-id="2a0be-156">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2a0be-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2a0be-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a0be-157">NOTES</span></span>

## <span data-ttu-id="2a0be-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a0be-158">RELATED LINKS</span></span>

[<span data-ttu-id="2a0be-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="2a0be-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="2a0be-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2a0be-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="2a0be-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="2a0be-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="2a0be-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="2a0be-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="2a0be-163">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2a0be-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
