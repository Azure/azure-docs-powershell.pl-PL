---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 0e28b5df77734645380316af6396f745469637df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548188"
---
# <span data-ttu-id="1557f-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1557f-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="1557f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1557f-102">SYNOPSIS</span></span>
<span data-ttu-id="1557f-103">Dodaje rozszerzenie diagnostyczne do VMSS.</span><span class="sxs-lookup"><span data-stu-id="1557f-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1557f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1557f-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1557f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1557f-105">DESCRIPTION</span></span>
<span data-ttu-id="1557f-106">Polecenie cmdlet **Add-AzureRmVmssDiagnosticsExtension** umożliwia dodanie rozszerzenia diagnostycznego do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1557f-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="1557f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1557f-107">EXAMPLES</span></span>

### <span data-ttu-id="1557f-108">Przykład 1: Dodawanie rozszerzenia diagnostycznego do VMSS</span><span class="sxs-lookup"><span data-stu-id="1557f-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="1557f-109">To polecenie umożliwia dodanie rozszerzenia diagnostycznego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="1557f-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="1557f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1557f-110">PARAMETERS</span></span>

### <span data-ttu-id="1557f-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1557f-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1557f-112">Wskazuje, czy to polecenie cmdlet umożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="1557f-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="1557f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1557f-113">-Force</span></span>
<span data-ttu-id="1557f-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1557f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1557f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1557f-115">-Name</span></span>
<span data-ttu-id="1557f-116">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1557f-116">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="1557f-117">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="1557f-117">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="1557f-118">Określa ścieżkę prywatnego pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="1557f-118">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="1557f-119">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="1557f-119">-SettingFilePath</span></span>
<span data-ttu-id="1557f-120">Określa ścieżkę pliku konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="1557f-120">Specifies the path of the public configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1557f-121">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1557f-121">-TypeHandlerVersion</span></span>
<span data-ttu-id="1557f-122">Określa wersję rozszerzenia, która ma być używana dla tego VMSS.</span><span class="sxs-lookup"><span data-stu-id="1557f-122">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="1557f-123">Aby uzyskać wersję, uruchom polecenie cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) z wartością Microsoft. Azure. Diagnostics dla parametru *wydawcy* i IaaSDiagnostics parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="1557f-123">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="1557f-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1557f-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1557f-125">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="1557f-125">Specify the VMSS object.</span></span>
<span data-ttu-id="1557f-126">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="1557f-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="1557f-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1557f-127">-Confirm</span></span>
<span data-ttu-id="1557f-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1557f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1557f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1557f-129">-WhatIf</span></span>
<span data-ttu-id="1557f-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1557f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1557f-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1557f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1557f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1557f-132">CommonParameters</span></span>
<span data-ttu-id="1557f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1557f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1557f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1557f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1557f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1557f-135">INPUTS</span></span>

### <span data-ttu-id="1557f-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1557f-136">None</span></span>
<span data-ttu-id="1557f-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1557f-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1557f-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1557f-138">OUTPUTS</span></span>

###  
<span data-ttu-id="1557f-139">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1557f-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1557f-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1557f-140">NOTES</span></span>

## <span data-ttu-id="1557f-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1557f-141">RELATED LINKS</span></span>

[<span data-ttu-id="1557f-142">Dodaj-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="1557f-142">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="1557f-143">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1557f-143">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="1557f-144">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1557f-144">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
