---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525345"
---
# <span data-ttu-id="5c053-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5c053-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="5c053-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c053-102">SYNOPSIS</span></span>
<span data-ttu-id="5c053-103">Dodaje rozszerzenie do VMSS.</span><span class="sxs-lookup"><span data-stu-id="5c053-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c053-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c053-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c053-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c053-105">DESCRIPTION</span></span>
<span data-ttu-id="5c053-106">Polecenie cmdlet **Add-AzureRmVmssExtension** dodaje rozszerzenie do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5c053-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5c053-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c053-107">EXAMPLES</span></span>

### <span data-ttu-id="5c053-108">Przykład 1: Dodawanie rozszerzenia do VMSS</span><span class="sxs-lookup"><span data-stu-id="5c053-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="5c053-109">To polecenie powoduje dodanie rozszerzenia do usługi zarządzania maszyną.</span><span class="sxs-lookup"><span data-stu-id="5c053-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="5c053-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c053-110">PARAMETERS</span></span>

### <span data-ttu-id="5c053-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5c053-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5c053-112">Wskazuje, czy wersja rozszerzenia ma być automatycznie aktualizowana do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="5c053-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="5c053-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c053-113">-Name</span></span>
<span data-ttu-id="5c053-114">Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c053-114">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="5c053-115">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="5c053-115">-ProtectedSetting</span></span>
<span data-ttu-id="5c053-116">Określa prywatną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="5c053-116">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="5c053-117">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="5c053-117">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="5c053-118">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="5c053-118">-Publisher</span></span>
<span data-ttu-id="5c053-119">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5c053-119">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="5c053-120">Gdy program Publisher zarejestruje rozszerzenie, program Publisher podaje nazwę.</span><span class="sxs-lookup"><span data-stu-id="5c053-120">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="5c053-121">Może to zrobić za pomocą polecenia cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) w celu uzyskania wydawcy.</span><span class="sxs-lookup"><span data-stu-id="5c053-121">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="5c053-122">-Setting</span><span class="sxs-lookup"><span data-stu-id="5c053-122">-Setting</span></span>
<span data-ttu-id="5c053-123">Określa konfigurację publiczną w postaci ciągu dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5c053-123">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="5c053-124">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="5c053-124">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="5c053-125">-Type</span><span class="sxs-lookup"><span data-stu-id="5c053-125">-Type</span></span>
<span data-ttu-id="5c053-126">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="5c053-126">Specifies the extension type.</span></span>
<span data-ttu-id="5c053-127">Aby uzyskać typ rozszerzenia, można użyć polecenia cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) .</span><span class="sxs-lookup"><span data-stu-id="5c053-127">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="5c053-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5c053-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="5c053-129">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c053-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="5c053-130">Aby uzyskać wersję rozszerzenia, możesz użyć polecenia cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) .</span><span class="sxs-lookup"><span data-stu-id="5c053-130">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="5c053-131">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5c053-131">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5c053-132">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="5c053-132">Specify the VMSS object.</span></span>
<span data-ttu-id="5c053-133">Aby utworzyć obiekt, możesz użyć [nowego-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="5c053-133">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c053-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c053-134">-Confirm</span></span>
<span data-ttu-id="5c053-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c053-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c053-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c053-136">-WhatIf</span></span>
<span data-ttu-id="5c053-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c053-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c053-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5c053-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c053-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c053-139">CommonParameters</span></span>
<span data-ttu-id="5c053-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c053-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c053-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c053-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c053-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c053-142">INPUTS</span></span>

### <span data-ttu-id="5c053-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5c053-143">None</span></span>
<span data-ttu-id="5c053-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5c053-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c053-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c053-145">OUTPUTS</span></span>

###  
<span data-ttu-id="5c053-146">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5c053-146">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5c053-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c053-147">NOTES</span></span>

## <span data-ttu-id="5c053-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c053-148">RELATED LINKS</span></span>

[<span data-ttu-id="5c053-149">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5c053-149">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="5c053-150">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="5c053-150">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="5c053-151">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="5c053-151">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="5c053-152">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5c053-152">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="5c053-153">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5c053-153">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
