---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: ad87e4e556263889de23640abad391ee28d7b397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549395"
---
# <span data-ttu-id="4debe-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4debe-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="4debe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4debe-102">SYNOPSIS</span></span>
<span data-ttu-id="4debe-103">Dodaje rozszerzenie do VMSS.</span><span class="sxs-lookup"><span data-stu-id="4debe-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4debe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4debe-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4debe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4debe-105">DESCRIPTION</span></span>
<span data-ttu-id="4debe-106">Polecenie cmdlet **Add-AzureRmVmssExtension** dodaje rozszerzenie do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4debe-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4debe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4debe-107">EXAMPLES</span></span>

### <span data-ttu-id="4debe-108">Przykład 1: Dodawanie rozszerzenia do VMSS</span><span class="sxs-lookup"><span data-stu-id="4debe-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="4debe-109">To polecenie dodaje rozszerzenie do VMSS.</span><span class="sxs-lookup"><span data-stu-id="4debe-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="4debe-110">Przykład 2: Dodawanie rozszerzenia do VMSS za pomocą ustawień i ustawień chronionych</span><span class="sxs-lookup"><span data-stu-id="4debe-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="4debe-111">To polecenie dodaje rozszerzenie do VMSS przy użyciu przykładowego skryptu bash w magazynie obiektów blob, określa adres URL magazynu obiektów blob i polecenia wykonywalnego w obszarze Ustawienia i zabezpieczenia dostęp w ustawieniach chronionych.</span><span class="sxs-lookup"><span data-stu-id="4debe-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="4debe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4debe-112">PARAMETERS</span></span>

### <span data-ttu-id="4debe-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="4debe-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="4debe-114">Wskazuje, czy wersja rozszerzenia ma być automatycznie aktualizowana do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="4debe-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="4debe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4debe-115">-DefaultProfile</span></span>
<span data-ttu-id="4debe-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4debe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4debe-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="4debe-117">-ForceUpdateTag</span></span>
<span data-ttu-id="4debe-118">Jeśli wartość jest podana i jest różna od poprzedniej wartości, program obsługi rozszerzeń zostanie zmuszony do zaktualizowania, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.</span><span class="sxs-lookup"><span data-stu-id="4debe-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="4debe-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4debe-119">-Name</span></span>
<span data-ttu-id="4debe-120">Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4debe-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4debe-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="4debe-121">-ProtectedSetting</span></span>
<span data-ttu-id="4debe-122">Określa prywatną konfigurację rozszerzenia w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="4debe-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="4debe-123">To polecenie cmdlet szyfruje konfigurację prywatną.</span><span class="sxs-lookup"><span data-stu-id="4debe-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="4debe-124">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="4debe-124">-Publisher</span></span>
<span data-ttu-id="4debe-125">Określa nazwę wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="4debe-125">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="4debe-126">Gdy program Publisher zarejestruje rozszerzenie, program Publisher podaje nazwę.</span><span class="sxs-lookup"><span data-stu-id="4debe-126">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="4debe-127">Może to zrobić za pomocą polecenia cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) w celu uzyskania wydawcy.</span><span class="sxs-lookup"><span data-stu-id="4debe-127">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="4debe-128">-Setting</span><span class="sxs-lookup"><span data-stu-id="4debe-128">-Setting</span></span>
<span data-ttu-id="4debe-129">Określa konfigurację publiczną w postaci ciągu dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="4debe-129">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="4debe-130">To polecenie cmdlet nie szyfruje konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="4debe-130">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="4debe-131">-Type</span><span class="sxs-lookup"><span data-stu-id="4debe-131">-Type</span></span>
<span data-ttu-id="4debe-132">Określa typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="4debe-132">Specifies the extension type.</span></span>
<span data-ttu-id="4debe-133">Aby uzyskać typ rozszerzenia, można użyć polecenia cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) .</span><span class="sxs-lookup"><span data-stu-id="4debe-133">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="4debe-134">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="4debe-134">-TypeHandlerVersion</span></span>
<span data-ttu-id="4debe-135">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4debe-135">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="4debe-136">Aby uzyskać wersję rozszerzenia, możesz użyć polecenia cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) .</span><span class="sxs-lookup"><span data-stu-id="4debe-136">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="4debe-137">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4debe-137">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4debe-138">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="4debe-138">Specify the VMSS object.</span></span>
<span data-ttu-id="4debe-139">Aby utworzyć obiekt, możesz użyć [nowego-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="4debe-139">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="4debe-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4debe-140">-Confirm</span></span>
<span data-ttu-id="4debe-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4debe-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4debe-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4debe-142">-WhatIf</span></span>
<span data-ttu-id="4debe-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4debe-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4debe-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4debe-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4debe-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4debe-145">CommonParameters</span></span>
<span data-ttu-id="4debe-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4debe-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4debe-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4debe-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4debe-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4debe-148">INPUTS</span></span>

### <span data-ttu-id="4debe-149">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4debe-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4debe-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4debe-150">System.String</span></span>

### <span data-ttu-id="4debe-151">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4debe-151">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4debe-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="4debe-152">System.Object</span></span>

## <span data-ttu-id="4debe-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4debe-153">OUTPUTS</span></span>

### <span data-ttu-id="4debe-154">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4debe-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4debe-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4debe-155">NOTES</span></span>

## <span data-ttu-id="4debe-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4debe-156">RELATED LINKS</span></span>

[<span data-ttu-id="4debe-157">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4debe-157">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="4debe-158">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="4debe-158">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4debe-159">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="4debe-159">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="4debe-160">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="4debe-160">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="4debe-161">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4debe-161">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
