---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 97c8824bca395ddd8fb23ebb4750ab35931c5d51
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893865"
---
# <span data-ttu-id="31bbd-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="31bbd-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="31bbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="31bbd-103">Dodaje rozszerzenie do VMSS.</span><span class="sxs-lookup"><span data-stu-id="31bbd-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="31bbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31bbd-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31bbd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31bbd-105">DESCRIPTION</span></span>
<span data-ttu-id="31bbd-106">Polecenie cmdlet **Add-AzVmssExtension** dodaje rozszerzenie do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="31bbd-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="31bbd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31bbd-107">EXAMPLES</span></span>

### <span data-ttu-id="31bbd-108">Przykład 1: Dodawanie rozszerzenia do VMSS</span><span class="sxs-lookup"><span data-stu-id="31bbd-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="31bbd-109">To polecenie powoduje dodanie rozszerzenia do usługi zarządzania maszyną.</span><span class="sxs-lookup"><span data-stu-id="31bbd-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="31bbd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31bbd-110">PARAMETERS</span></span>

### <span data-ttu-id="31bbd-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="31bbd-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="31bbd-112">Wskazuje, czy wersja rozszerzenia ma być automatycznie aktualizowana do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="31bbd-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31bbd-113">-DefaultProfile</span></span>
<span data-ttu-id="31bbd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31bbd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="31bbd-115">-ForceUpdateTag</span></span>
<span data-ttu-id="31bbd-116">Jeśli wartość jest podana i jest różna od poprzedniej wartości, program obsługi rozszerzeń zostanie zmuszony do zaktualizowania, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="31bbd-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31bbd-117">-Name</span></span>
<span data-ttu-id="31bbd-118">Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31bbd-118">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="31bbd-119">-ProtectedSetting</span></span>
<span data-ttu-id="31bbd-120">Określa prywatną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="31bbd-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="31bbd-121">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="31bbd-121">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-122">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="31bbd-122">-Publisher</span></span>
<span data-ttu-id="31bbd-123">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="31bbd-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="31bbd-124">Gdy program Publisher zarejestruje rozszerzenie, program Publisher podaje nazwę.</span><span class="sxs-lookup"><span data-stu-id="31bbd-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="31bbd-125">Może to zrobić za pomocą polecenia cmdlet [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) w celu uzyskania wydawcy.</span><span class="sxs-lookup"><span data-stu-id="31bbd-125">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-126">-Setting</span><span class="sxs-lookup"><span data-stu-id="31bbd-126">-Setting</span></span>
<span data-ttu-id="31bbd-127">Określa konfigurację publiczną w postaci ciągu dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="31bbd-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="31bbd-128">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="31bbd-128">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-129">-Type</span><span class="sxs-lookup"><span data-stu-id="31bbd-129">-Type</span></span>
<span data-ttu-id="31bbd-130">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="31bbd-130">Specifies the extension type.</span></span>
<span data-ttu-id="31bbd-131">Aby uzyskać typ rozszerzenia, można użyć polecenia cmdlet [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) .</span><span class="sxs-lookup"><span data-stu-id="31bbd-131">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="31bbd-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="31bbd-133">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="31bbd-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="31bbd-134">Aby uzyskać wersję rozszerzenia, możesz użyć polecenia cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) .</span><span class="sxs-lookup"><span data-stu-id="31bbd-134">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="31bbd-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="31bbd-136">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="31bbd-136">Specify the VMSS object.</span></span>
<span data-ttu-id="31bbd-137">Aby utworzyć obiekt, możesz użyć [nowego-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="31bbd-137">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31bbd-138">-Confirm</span></span>
<span data-ttu-id="31bbd-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31bbd-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31bbd-140">-WhatIf</span></span>
<span data-ttu-id="31bbd-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31bbd-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31bbd-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31bbd-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bbd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31bbd-143">CommonParameters</span></span>
<span data-ttu-id="31bbd-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31bbd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31bbd-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31bbd-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31bbd-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31bbd-146">INPUTS</span></span>

### <span data-ttu-id="31bbd-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="31bbd-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="31bbd-148">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="31bbd-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="31bbd-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31bbd-149">OUTPUTS</span></span>

###  
<span data-ttu-id="31bbd-150">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="31bbd-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="31bbd-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31bbd-151">NOTES</span></span>

## <span data-ttu-id="31bbd-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31bbd-152">RELATED LINKS</span></span>

[<span data-ttu-id="31bbd-153">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="31bbd-153">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="31bbd-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="31bbd-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="31bbd-155">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="31bbd-155">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="31bbd-156">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="31bbd-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="31bbd-157">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="31bbd-157">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
