---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 8e6a0ec7002f211e660c3ca71d190faf719bbd6c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897697"
---
# <span data-ttu-id="9683a-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9683a-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="9683a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9683a-102">SYNOPSIS</span></span>
<span data-ttu-id="9683a-103">Dodaje rozszerzenie diagnostyczne do VMSS.</span><span class="sxs-lookup"><span data-stu-id="9683a-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9683a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9683a-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9683a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9683a-105">DESCRIPTION</span></span>
<span data-ttu-id="9683a-106">Polecenie cmdlet **Add-AzureRmVmssDiagnosticsExtension** umożliwia dodanie rozszerzenia diagnostycznego do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9683a-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="9683a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9683a-107">EXAMPLES</span></span>

### <span data-ttu-id="9683a-108">Przykład 1: Dodawanie rozszerzenia diagnostycznego do VMSS</span><span class="sxs-lookup"><span data-stu-id="9683a-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="9683a-109">To polecenie umożliwia dodanie rozszerzenia diagnostycznego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="9683a-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="9683a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9683a-110">PARAMETERS</span></span>

### <span data-ttu-id="9683a-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9683a-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="9683a-112">Wskazuje, czy to polecenie cmdlet umożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="9683a-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="9683a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9683a-113">-DefaultProfile</span></span>
<span data-ttu-id="9683a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9683a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9683a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9683a-115">-Force</span></span>
<span data-ttu-id="9683a-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9683a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9683a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9683a-117">-Name</span></span>
<span data-ttu-id="9683a-118">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="9683a-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="9683a-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="9683a-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="9683a-120">Określa ścieżkę prywatnego pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="9683a-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="9683a-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="9683a-121">-SettingFilePath</span></span>
<span data-ttu-id="9683a-122">Określa ścieżkę pliku konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="9683a-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="9683a-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9683a-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="9683a-124">Określa wersję rozszerzenia, która ma być używana dla tego VMSS.</span><span class="sxs-lookup"><span data-stu-id="9683a-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="9683a-125">Aby uzyskać wersję, uruchom polecenie cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) z wartością Microsoft. Azure. Diagnostics dla parametru *wydawcy* i IaaSDiagnostics parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="9683a-125">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="9683a-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9683a-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9683a-127">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="9683a-127">Specify the VMSS object.</span></span>
<span data-ttu-id="9683a-128">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="9683a-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="9683a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9683a-129">-Confirm</span></span>
<span data-ttu-id="9683a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9683a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9683a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9683a-131">-WhatIf</span></span>
<span data-ttu-id="9683a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9683a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9683a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9683a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9683a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9683a-134">CommonParameters</span></span>
<span data-ttu-id="9683a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9683a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9683a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9683a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9683a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9683a-137">INPUTS</span></span>

### <span data-ttu-id="9683a-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9683a-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="9683a-139">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9683a-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="9683a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9683a-140">OUTPUTS</span></span>

###  
<span data-ttu-id="9683a-141">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9683a-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="9683a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9683a-142">NOTES</span></span>

## <span data-ttu-id="9683a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9683a-143">RELATED LINKS</span></span>

[<span data-ttu-id="9683a-144">Dodaj-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="9683a-144">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="9683a-145">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9683a-145">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="9683a-146">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9683a-146">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
