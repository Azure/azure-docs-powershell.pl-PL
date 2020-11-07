---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: f84d9f823d97872d8ad2491a2ab45ef3bb5a22a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893869"
---
# <span data-ttu-id="05cb4-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="05cb4-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="05cb4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="05cb4-103">Dodaje rozszerzenie diagnostyczne do VMSS.</span><span class="sxs-lookup"><span data-stu-id="05cb4-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="05cb4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05cb4-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05cb4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="05cb4-105">DESCRIPTION</span></span>
<span data-ttu-id="05cb4-106">Polecenie cmdlet **Add-AzVmssDiagnosticsExtension** umożliwia dodanie rozszerzenia diagnostycznego do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="05cb4-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="05cb4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05cb4-107">EXAMPLES</span></span>

### <span data-ttu-id="05cb4-108">Przykład 1: Dodawanie rozszerzenia diagnostycznego do VMSS</span><span class="sxs-lookup"><span data-stu-id="05cb4-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="05cb4-109">To polecenie umożliwia dodanie rozszerzenia diagnostycznego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="05cb4-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="05cb4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05cb4-110">PARAMETERS</span></span>

### <span data-ttu-id="05cb4-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="05cb4-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="05cb4-112">Wskazuje, czy to polecenie cmdlet umożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="05cb4-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="05cb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05cb4-113">-DefaultProfile</span></span>
<span data-ttu-id="05cb4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05cb4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05cb4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="05cb4-115">-Force</span></span>
<span data-ttu-id="05cb4-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="05cb4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="05cb4-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05cb4-117">-Name</span></span>
<span data-ttu-id="05cb4-118">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="05cb4-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="05cb4-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="05cb4-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="05cb4-120">Określa ścieżkę prywatnego pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="05cb4-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="05cb4-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="05cb4-121">-SettingFilePath</span></span>
<span data-ttu-id="05cb4-122">Określa ścieżkę pliku konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="05cb4-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="05cb4-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="05cb4-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="05cb4-124">Określa wersję rozszerzenia, która ma być używana dla tego VMSS.</span><span class="sxs-lookup"><span data-stu-id="05cb4-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="05cb4-125">Aby uzyskać wersję, uruchom polecenie cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) z wartością Microsoft. Azure. Diagnostics dla parametru *wydawcy* i IaaSDiagnostics parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="05cb4-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="05cb4-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="05cb4-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="05cb4-127">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="05cb4-127">Specify the VMSS object.</span></span>
<span data-ttu-id="05cb4-128">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="05cb4-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="05cb4-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05cb4-129">-Confirm</span></span>
<span data-ttu-id="05cb4-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05cb4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05cb4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05cb4-131">-WhatIf</span></span>
<span data-ttu-id="05cb4-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05cb4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05cb4-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05cb4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05cb4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05cb4-134">CommonParameters</span></span>
<span data-ttu-id="05cb4-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05cb4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05cb4-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05cb4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05cb4-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05cb4-137">INPUTS</span></span>

### <span data-ttu-id="05cb4-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="05cb4-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="05cb4-139">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="05cb4-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="05cb4-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05cb4-140">OUTPUTS</span></span>

###  
<span data-ttu-id="05cb4-141">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="05cb4-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="05cb4-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05cb4-142">NOTES</span></span>

## <span data-ttu-id="05cb4-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05cb4-143">RELATED LINKS</span></span>

[<span data-ttu-id="05cb4-144">Dodaj-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="05cb4-144">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="05cb4-145">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="05cb4-145">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="05cb4-146">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="05cb4-146">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
