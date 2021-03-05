---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 774fb61f2394c5634c8415a7a18ce63f4e696a3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991551"
---
# <span data-ttu-id="fcf3a-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fcf3a-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="fcf3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcf3a-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf3a-103">Dodaje rozszerzenie do programu VMSS.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="fcf3a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fcf3a-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcf3a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fcf3a-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf3a-106">Polecenie **cmdlet AzVmssExtension dodatku Add-AzVmssExtension** dodaje rozszerzenie do zestawu skal maszyny wirtualnej (VIRTUAL Machine Scale Set, VIRTUALSS).</span><span class="sxs-lookup"><span data-stu-id="fcf3a-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="fcf3a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fcf3a-107">EXAMPLES</span></span>

### <span data-ttu-id="fcf3a-108">Przykład 1. Dodawanie rozszerzenia do maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="fcf3a-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="fcf3a-109">To polecenie powoduje dodanie rozszerzenia do usługi maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="fcf3a-110">Przykład 2. Dodawanie rozszerzenia do maszyn wirtualnych o ustawieniach i ustawieniach chronionych</span><span class="sxs-lookup"><span data-stu-id="fcf3a-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="fcf3a-111">To polecenie powoduje dodanie rozszerzenia do usług VMSS z przykładowym skryptem bash w magazynie obiektów blob, określenie adresu URL magazynu obiektów blob i wykonywalnego polecenia w ustawieniach oraz dostępu zabezpieczeń w ustawieniach chronionych.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="fcf3a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcf3a-112">PARAMETERS</span></span>

### <span data-ttu-id="fcf3a-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fcf3a-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fcf3a-114">Wskazuje, czy wersja rozszerzenia powinna zostać automatycznie zaktualizowana do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="fcf3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf3a-115">-DefaultProfile</span></span>
<span data-ttu-id="fcf3a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcf3a-117">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="fcf3a-117">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="fcf3a-118">Wskazuje, czy rozszerzenie powinno zostać automatycznie uaktualnione przez platformę, jeśli jest dostępna nowsza wersja rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-118">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf3a-119">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="fcf3a-119">-ForceUpdateTag</span></span>
<span data-ttu-id="fcf3a-120">Jeśli podano wartość inną niż poprzednia, program obsługi rozszerzenia będzie musiał zaktualizować plik nawet wtedy, gdy konfiguracja rozszerzenia się nie zmieniła.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-120">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="fcf3a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fcf3a-121">-Name</span></span>
<span data-ttu-id="fcf3a-122">Określa nazwę rozszerzenia, które dodaje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-122">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="fcf3a-123">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="fcf3a-123">-ProtectedSetting</span></span>
<span data-ttu-id="fcf3a-124">Określa prywatną konfigurację rozszerzenia jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-124">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="fcf3a-125">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-125">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="fcf3a-126">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="fcf3a-126">-ProvisionAfterExtension</span></span>
<span data-ttu-id="fcf3a-127">Zbiór nazw rozszerzeń, po których to rozszerzenie wymaga obsługi administracyjnej.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-127">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="fcf3a-128">— Publisher</span><span class="sxs-lookup"><span data-stu-id="fcf3a-128">-Publisher</span></span>
<span data-ttu-id="fcf3a-129">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-129">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="fcf3a-130">Po zarejestrowaniu rozszerzenia wydawca podaje jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-130">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="fcf3a-131">Aby pobrać wydawcę, możesz użyć polecenia cmdlet [Get-AzVMImagePublisher.](./Get-AzVMImagePublisher.md)</span><span class="sxs-lookup"><span data-stu-id="fcf3a-131">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="fcf3a-132">— Ustawienie</span><span class="sxs-lookup"><span data-stu-id="fcf3a-132">-Setting</span></span>
<span data-ttu-id="fcf3a-133">Określa konfigurację publiczną jako ciąg rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-133">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="fcf3a-134">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-134">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="fcf3a-135">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="fcf3a-135">-Type</span></span>
<span data-ttu-id="fcf3a-136">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-136">Specifies the extension type.</span></span>
<span data-ttu-id="fcf3a-137">Aby pobrać typ rozszerzenia, możesz użyć polecenia cmdlet [Get-AzVMExtensionImageType.](./Get-AzVMExtensionImageType.md)</span><span class="sxs-lookup"><span data-stu-id="fcf3a-137">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="fcf3a-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fcf3a-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="fcf3a-139">Określa wersję rozszerzenia do użycia dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="fcf3a-140">Aby pobrać wersję rozszerzenia, możesz użyć polecenia cmdlet [Get-AzVMExtensionImage.](./Get-AzVMExtensionImage.md)</span><span class="sxs-lookup"><span data-stu-id="fcf3a-140">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="fcf3a-141">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fcf3a-141">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fcf3a-142">Określanie obiektu MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-142">Specify the VMSS object.</span></span>
<span data-ttu-id="fcf3a-143">Aby utworzyć obiekt, możesz użyć konfiguracji [New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="fcf3a-143">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="fcf3a-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fcf3a-144">-Confirm</span></span>
<span data-ttu-id="fcf3a-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf3a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf3a-146">-WhatIf</span></span>
<span data-ttu-id="fcf3a-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcf3a-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf3a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf3a-149">CommonParameters</span></span>
<span data-ttu-id="fcf3a-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf3a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf3a-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcf3a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf3a-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcf3a-152">INPUTS</span></span>

### <span data-ttu-id="fcf3a-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fcf3a-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fcf3a-154">System.String</span><span class="sxs-lookup"><span data-stu-id="fcf3a-154">System.String</span></span>

### <span data-ttu-id="fcf3a-155">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fcf3a-155">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fcf3a-156">System.Object</span><span class="sxs-lookup"><span data-stu-id="fcf3a-156">System.Object</span></span>

## <span data-ttu-id="fcf3a-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcf3a-157">OUTPUTS</span></span>

### <span data-ttu-id="fcf3a-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fcf3a-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fcf3a-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fcf3a-159">NOTES</span></span>

## <span data-ttu-id="fcf3a-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcf3a-160">RELATED LINKS</span></span>

[<span data-ttu-id="fcf3a-161">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fcf3a-161">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="fcf3a-162">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fcf3a-162">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="fcf3a-163">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="fcf3a-163">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="fcf3a-164">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="fcf3a-164">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="fcf3a-165">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fcf3a-165">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
