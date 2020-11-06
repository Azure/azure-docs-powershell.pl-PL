---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: fbf9d8c38c10465c565e40a284171b3232ba2949
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551080"
---
# <span data-ttu-id="aec10-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="aec10-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="aec10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aec10-102">SYNOPSIS</span></span>
<span data-ttu-id="aec10-103">Dodaje rozszerzenie do VMSS.</span><span class="sxs-lookup"><span data-stu-id="aec10-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aec10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aec10-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aec10-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aec10-105">DESCRIPTION</span></span>
<span data-ttu-id="aec10-106">Polecenie cmdlet **Add-AzureRmVmssExtension** dodaje rozszerzenie do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="aec10-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="aec10-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aec10-107">EXAMPLES</span></span>

### <span data-ttu-id="aec10-108">Przykład 1: Dodawanie rozszerzenia do VMSS</span><span class="sxs-lookup"><span data-stu-id="aec10-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="aec10-109">To polecenie powoduje dodanie rozszerzenia do usługi zarządzania maszyną.</span><span class="sxs-lookup"><span data-stu-id="aec10-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="aec10-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aec10-110">PARAMETERS</span></span>

### <span data-ttu-id="aec10-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="aec10-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="aec10-112">Wskazuje, czy wersja rozszerzenia ma być automatycznie aktualizowana do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="aec10-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="aec10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec10-113">-DefaultProfile</span></span>
<span data-ttu-id="aec10-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aec10-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec10-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="aec10-115">-ForceUpdateTag</span></span>
<span data-ttu-id="aec10-116">Jeśli wartość jest podana i jest różna od poprzedniej wartości, program obsługi rozszerzeń zostanie zmuszony do zaktualizowania, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="aec10-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="aec10-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aec10-117">-Name</span></span>
<span data-ttu-id="aec10-118">Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec10-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="aec10-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="aec10-119">-ProtectedSetting</span></span>
<span data-ttu-id="aec10-120">Określa prywatną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="aec10-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="aec10-121">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="aec10-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="aec10-122">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="aec10-122">-Publisher</span></span>
<span data-ttu-id="aec10-123">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="aec10-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="aec10-124">Gdy program Publisher zarejestruje rozszerzenie, program Publisher podaje nazwę.</span><span class="sxs-lookup"><span data-stu-id="aec10-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="aec10-125">Może to zrobić za pomocą polecenia cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) w celu uzyskania wydawcy.</span><span class="sxs-lookup"><span data-stu-id="aec10-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="aec10-126">-Setting</span><span class="sxs-lookup"><span data-stu-id="aec10-126">-Setting</span></span>
<span data-ttu-id="aec10-127">Określa konfigurację publiczną w postaci ciągu dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="aec10-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="aec10-128">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="aec10-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="aec10-129">-Type</span><span class="sxs-lookup"><span data-stu-id="aec10-129">-Type</span></span>
<span data-ttu-id="aec10-130">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="aec10-130">Specifies the extension type.</span></span>
<span data-ttu-id="aec10-131">Aby uzyskać typ rozszerzenia, można użyć polecenia cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) .</span><span class="sxs-lookup"><span data-stu-id="aec10-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="aec10-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="aec10-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="aec10-133">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aec10-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="aec10-134">Aby uzyskać wersję rozszerzenia, możesz użyć polecenia cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) .</span><span class="sxs-lookup"><span data-stu-id="aec10-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="aec10-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aec10-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="aec10-136">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="aec10-136">Specify the VMSS object.</span></span>
<span data-ttu-id="aec10-137">Aby utworzyć obiekt, możesz użyć [nowego-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="aec10-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="aec10-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aec10-138">-Confirm</span></span>
<span data-ttu-id="aec10-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec10-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec10-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec10-140">-WhatIf</span></span>
<span data-ttu-id="aec10-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec10-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aec10-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aec10-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec10-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec10-143">CommonParameters</span></span>
<span data-ttu-id="aec10-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec10-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec10-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec10-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec10-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aec10-146">INPUTS</span></span>

## <span data-ttu-id="aec10-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aec10-147">OUTPUTS</span></span>

###  
<span data-ttu-id="aec10-148">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="aec10-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="aec10-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aec10-149">NOTES</span></span>

## <span data-ttu-id="aec10-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aec10-150">RELATED LINKS</span></span>

[<span data-ttu-id="aec10-151">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="aec10-151">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="aec10-152">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="aec10-152">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="aec10-153">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="aec10-153">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="aec10-154">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="aec10-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="aec10-155">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="aec10-155">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
