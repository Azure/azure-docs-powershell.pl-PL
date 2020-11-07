---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVmssVMRunCommand.md
ms.openlocfilehash: 1c1cdeff1e1a73de6947855922a4fed45fe387e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719159"
---
# <span data-ttu-id="e05b7-101">Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="e05b7-101">Invoke-AzureRmVmssVMRunCommand</span></span>

## <span data-ttu-id="e05b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e05b7-102">SYNOPSIS</span></span>
<span data-ttu-id="e05b7-103">Polecenie Uruchom na maszynie wirtualnej zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e05b7-103">Run command on the Virtual Machine Scale Set VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e05b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e05b7-104">SYNTAX</span></span>

### <span data-ttu-id="e05b7-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e05b7-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05b7-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e05b7-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e05b7-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e05b7-107">ObjectParameter</span></span>
```
Invoke-AzureRmVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e05b7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e05b7-108">DESCRIPTION</span></span>
<span data-ttu-id="e05b7-109">Wywoływanie polecenia Uruchom na maszynie wirtualnej zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e05b7-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="e05b7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e05b7-110">EXAMPLES</span></span>

### <span data-ttu-id="e05b7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e05b7-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="e05b7-112">Wywołać polecenie Uruchom dla RunPowerShellScript, zastępując skrypt "sample.ps1" i parametry na maszynie wirtualnej o IDENTYFIKATORze "0" w zestawie skali maszyny wirtualnej "vmssname" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="e05b7-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="e05b7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e05b7-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzureRmVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="e05b7-114">Wywołać polecenie Uruchom dla RunPowerShellScript, zastępując skrypt "sample.ps1" i parametry na maszynie wirtualnej o IDENTYFIKATORze "0" w zestawie skali maszyny wirtualnej "vmssname" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="e05b7-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="e05b7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e05b7-115">PARAMETERS</span></span>

### <span data-ttu-id="e05b7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e05b7-116">-AsJob</span></span>
<span data-ttu-id="e05b7-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e05b7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e05b7-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="e05b7-118">-CommandId</span></span>
<span data-ttu-id="e05b7-119">Identyfikator polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="e05b7-119">The run command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05b7-120">-DefaultProfile</span></span>
<span data-ttu-id="e05b7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e05b7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e05b7-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e05b7-122">-InstanceId</span></span>
<span data-ttu-id="e05b7-123">Identyfikator wystąpienia ustawienia maszyny wirtualnej w skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e05b7-123">The instance ID of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05b7-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e05b7-124">-Parameter</span></span>
<span data-ttu-id="e05b7-125">Parametry polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="e05b7-125">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="e05b7-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e05b7-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05b7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e05b7-128">-ResourceId</span></span>
<span data-ttu-id="e05b7-129">Identyfikator zasobu zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e05b7-129">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05b7-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="e05b7-130">-ScriptPath</span></span>
<span data-ttu-id="e05b7-131">Ścieżka skryptu, który ma zostać wykonany.</span><span class="sxs-lookup"><span data-stu-id="e05b7-131">Path of the script to be executed.</span></span>  <span data-ttu-id="e05b7-132">Gdy ta wartość zostanie podana, dany skrypt zastąpi domyślny skrypt polecenia.</span><span class="sxs-lookup"><span data-stu-id="e05b7-132">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e05b7-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e05b7-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="e05b7-134">Zestaw skali maszyny wirtualnej PS, ustaw obiekt VM.</span><span class="sxs-lookup"><span data-stu-id="e05b7-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e05b7-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e05b7-135">-VMScaleSetName</span></span>
<span data-ttu-id="e05b7-136">Nazwa maszyny wirtualnej zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e05b7-136">The name of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e05b7-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e05b7-137">-Confirm</span></span>
<span data-ttu-id="e05b7-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e05b7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e05b7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e05b7-139">-WhatIf</span></span>
<span data-ttu-id="e05b7-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e05b7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e05b7-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e05b7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e05b7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05b7-142">CommonParameters</span></span>
<span data-ttu-id="e05b7-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05b7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05b7-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05b7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05b7-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e05b7-145">INPUTS</span></span>

### <span data-ttu-id="e05b7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e05b7-146">System.String</span></span>

### <span data-ttu-id="e05b7-147">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e05b7-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="e05b7-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e05b7-148">OUTPUTS</span></span>

### <span data-ttu-id="e05b7-149">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="e05b7-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="e05b7-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e05b7-150">NOTES</span></span>

## <span data-ttu-id="e05b7-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e05b7-151">RELATED LINKS</span></span>
