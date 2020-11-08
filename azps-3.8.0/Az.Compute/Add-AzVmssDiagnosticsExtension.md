---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053870"
---
# <span data-ttu-id="f8b6c-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f8b6c-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="f8b6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b6c-103">Dodaje rozszerzenie diagnostyczne do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="f8b6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8b6c-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8b6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f8b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b6c-106">Polecenie cmdlet **Add-AzVmssDiagnosticsExtension** umożliwia dodanie rozszerzenia diagnostycznego do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f8b6c-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="f8b6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8b6c-107">EXAMPLES</span></span>

### <span data-ttu-id="f8b6c-108">Przykład 1: Dodawanie rozszerzenia diagnostycznego do VMSS</span><span class="sxs-lookup"><span data-stu-id="f8b6c-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="f8b6c-109">To polecenie umożliwia dodanie rozszerzenia diagnostycznego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="f8b6c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8b6c-110">PARAMETERS</span></span>

### <span data-ttu-id="f8b6c-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f8b6c-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f8b6c-112">Wskazuje, czy to polecenie cmdlet umożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8b6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b6c-113">-DefaultProfile</span></span>
<span data-ttu-id="f8b6c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8b6c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f8b6c-115">-Force</span></span>
<span data-ttu-id="f8b6c-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b6c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f8b6c-117">-Name</span></span>
<span data-ttu-id="f8b6c-118">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-118">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8b6c-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="f8b6c-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="f8b6c-120">Określa ścieżkę prywatnego pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="f8b6c-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="f8b6c-121">-SettingFilePath</span></span>
<span data-ttu-id="f8b6c-122">Określa ścieżkę pliku konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-122">Specifies the path of the public configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8b6c-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f8b6c-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="f8b6c-124">Określa wersję rozszerzenia, która ma być używana dla tego VMSS.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="f8b6c-125">Aby uzyskać wersję, uruchom polecenie cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) z wartością Microsoft. Azure. Diagnostics dla parametru *wydawcy* i IaaSDiagnostics parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="f8b6c-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8b6c-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f8b6c-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f8b6c-127">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-127">Specify the VMSS object.</span></span>
<span data-ttu-id="f8b6c-128">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="f8b6c-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="f8b6c-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f8b6c-129">-Confirm</span></span>
<span data-ttu-id="f8b6c-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b6c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8b6c-131">-WhatIf</span></span>
<span data-ttu-id="f8b6c-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8b6c-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b6c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b6c-134">CommonParameters</span></span>
<span data-ttu-id="f8b6c-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b6c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b6c-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8b6c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b6c-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8b6c-137">INPUTS</span></span>

### <span data-ttu-id="f8b6c-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f8b6c-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="f8b6c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f8b6c-139">System.String</span></span>

### <span data-ttu-id="f8b6c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8b6c-140">System.Boolean</span></span>

## <span data-ttu-id="f8b6c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8b6c-141">OUTPUTS</span></span>

### <span data-ttu-id="f8b6c-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f8b6c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f8b6c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8b6c-143">NOTES</span></span>

## <span data-ttu-id="f8b6c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8b6c-144">RELATED LINKS</span></span>

[<span data-ttu-id="f8b6c-145">Dodaj-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f8b6c-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="f8b6c-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f8b6c-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="f8b6c-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f8b6c-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
