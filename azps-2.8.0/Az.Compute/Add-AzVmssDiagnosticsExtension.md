---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 55abb45cb689f05f721ed42afadb855638f90256
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706477"
---
# <span data-ttu-id="cdd76-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cdd76-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="cdd76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdd76-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd76-103">Dodaje rozszerzenie diagnostyczne do VMSS.</span><span class="sxs-lookup"><span data-stu-id="cdd76-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="cdd76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdd76-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd76-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cdd76-105">DESCRIPTION</span></span>
<span data-ttu-id="cdd76-106">Polecenie cmdlet **Add-AzVmssDiagnosticsExtension** umożliwia dodanie rozszerzenia diagnostycznego do wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="cdd76-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="cdd76-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdd76-107">EXAMPLES</span></span>

### <span data-ttu-id="cdd76-108">Przykład 1: Dodawanie rozszerzenia diagnostycznego do VMSS</span><span class="sxs-lookup"><span data-stu-id="cdd76-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="cdd76-109">To polecenie umożliwia dodanie rozszerzenia diagnostycznego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="cdd76-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="cdd76-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdd76-110">PARAMETERS</span></span>

### <span data-ttu-id="cdd76-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cdd76-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="cdd76-112">Wskazuje, czy to polecenie cmdlet umożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="cdd76-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="cdd76-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd76-113">-DefaultProfile</span></span>
<span data-ttu-id="cdd76-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd76-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdd76-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cdd76-115">-Force</span></span>
<span data-ttu-id="cdd76-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cdd76-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cdd76-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cdd76-117">-Name</span></span>
<span data-ttu-id="cdd76-118">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="cdd76-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="cdd76-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="cdd76-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="cdd76-120">Określa ścieżkę prywatnego pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="cdd76-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="cdd76-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="cdd76-121">-SettingFilePath</span></span>
<span data-ttu-id="cdd76-122">Określa ścieżkę pliku konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="cdd76-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="cdd76-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cdd76-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="cdd76-124">Określa wersję rozszerzenia, która ma być używana dla tego VMSS.</span><span class="sxs-lookup"><span data-stu-id="cdd76-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="cdd76-125">Aby uzyskać wersję, uruchom polecenie cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) z wartością Microsoft. Azure. Diagnostics dla parametru *wydawcy* i IaaSDiagnostics parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="cdd76-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="cdd76-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cdd76-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cdd76-127">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="cdd76-127">Specify the VMSS object.</span></span>
<span data-ttu-id="cdd76-128">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="cdd76-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="cdd76-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cdd76-129">-Confirm</span></span>
<span data-ttu-id="cdd76-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd76-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd76-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd76-131">-WhatIf</span></span>
<span data-ttu-id="cdd76-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd76-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd76-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cdd76-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd76-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd76-134">CommonParameters</span></span>
<span data-ttu-id="cdd76-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd76-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd76-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdd76-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd76-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdd76-137">INPUTS</span></span>

### <span data-ttu-id="cdd76-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cdd76-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="cdd76-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cdd76-139">System.String</span></span>

### <span data-ttu-id="cdd76-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdd76-140">System.Boolean</span></span>

## <span data-ttu-id="cdd76-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdd76-141">OUTPUTS</span></span>

### <span data-ttu-id="cdd76-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cdd76-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cdd76-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdd76-143">NOTES</span></span>

## <span data-ttu-id="cdd76-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdd76-144">RELATED LINKS</span></span>

[<span data-ttu-id="cdd76-145">Dodaj-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cdd76-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="cdd76-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cdd76-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="cdd76-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cdd76-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
