---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062593"
---
# <span data-ttu-id="92c08-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="92c08-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="92c08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92c08-102">SYNOPSIS</span></span>
<span data-ttu-id="92c08-103">Polecenie Uruchom na maszynie wirtualnej zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="92c08-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="92c08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92c08-104">SYNTAX</span></span>

### <span data-ttu-id="92c08-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92c08-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92c08-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="92c08-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92c08-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="92c08-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92c08-108">Opis</span><span class="sxs-lookup"><span data-stu-id="92c08-108">DESCRIPTION</span></span>
<span data-ttu-id="92c08-109">Wywoływanie polecenia Uruchom na maszynie wirtualnej zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="92c08-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="92c08-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92c08-110">EXAMPLES</span></span>

### <span data-ttu-id="92c08-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92c08-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="92c08-112">Wywołać polecenie Uruchom dla RunPowerShellScript, zastępując skrypt "sample.ps1" i parametry na maszynie wirtualnej o IDENTYFIKATORze "0" w zestawie skali maszyny wirtualnej "vmssname" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="92c08-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="92c08-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="92c08-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="92c08-114">Wywołać polecenie Uruchom dla RunPowerShellScript, zastępując skrypt "sample.ps1" i parametry na maszynie wirtualnej o IDENTYFIKATORze "0" w zestawie skali maszyny wirtualnej "vmssname" w grupie zasobów "rgName".</span><span class="sxs-lookup"><span data-stu-id="92c08-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="92c08-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92c08-115">PARAMETERS</span></span>

### <span data-ttu-id="92c08-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92c08-116">-AsJob</span></span>
<span data-ttu-id="92c08-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="92c08-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92c08-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="92c08-118">-CommandId</span></span>
<span data-ttu-id="92c08-119">Identyfikator polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="92c08-119">The run command id.</span></span>

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

### <span data-ttu-id="92c08-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92c08-120">-DefaultProfile</span></span>
<span data-ttu-id="92c08-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92c08-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92c08-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="92c08-122">-InstanceId</span></span>
<span data-ttu-id="92c08-123">Identyfikator wystąpienia ustawienia maszyny wirtualnej w skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="92c08-123">The instance ID of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="92c08-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="92c08-124">-Parameter</span></span>
<span data-ttu-id="92c08-125">Parametry polecenia Uruchom.</span><span class="sxs-lookup"><span data-stu-id="92c08-125">The run command parameters.</span></span>

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

### <span data-ttu-id="92c08-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92c08-126">-ResourceGroupName</span></span>
<span data-ttu-id="92c08-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92c08-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="92c08-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92c08-128">-ResourceId</span></span>
<span data-ttu-id="92c08-129">Identyfikator zasobu zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="92c08-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="92c08-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="92c08-130">-ScriptPath</span></span>
<span data-ttu-id="92c08-131">Ścieżka skryptu, który ma zostać wykonany.</span><span class="sxs-lookup"><span data-stu-id="92c08-131">Path of the script to be executed.</span></span>  <span data-ttu-id="92c08-132">Gdy ta wartość zostanie podana, dany skrypt zastąpi domyślny skrypt polecenia.</span><span class="sxs-lookup"><span data-stu-id="92c08-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="92c08-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="92c08-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="92c08-134">Zestaw skali maszyny wirtualnej PS, ustaw obiekt VM.</span><span class="sxs-lookup"><span data-stu-id="92c08-134">The PS Virtual Machine Scale Set VM Object.</span></span>

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

### <span data-ttu-id="92c08-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="92c08-135">-VMScaleSetName</span></span>
<span data-ttu-id="92c08-136">Nazwa maszyny wirtualnej zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="92c08-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="92c08-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92c08-137">-Confirm</span></span>
<span data-ttu-id="92c08-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92c08-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92c08-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92c08-139">-WhatIf</span></span>
<span data-ttu-id="92c08-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92c08-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92c08-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92c08-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92c08-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c08-142">CommonParameters</span></span>
<span data-ttu-id="92c08-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92c08-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c08-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92c08-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c08-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92c08-145">INPUTS</span></span>

### <span data-ttu-id="92c08-146">System. String</span><span class="sxs-lookup"><span data-stu-id="92c08-146">System.String</span></span>

### <span data-ttu-id="92c08-147">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="92c08-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="92c08-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92c08-148">OUTPUTS</span></span>

### <span data-ttu-id="92c08-149">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="92c08-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="92c08-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92c08-150">NOTES</span></span>

## <span data-ttu-id="92c08-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92c08-151">RELATED LINKS</span></span>
