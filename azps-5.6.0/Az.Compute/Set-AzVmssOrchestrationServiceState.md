---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: 84f208a18061d7a682fc1662c97811a19590ca65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983745"
---
# <span data-ttu-id="f4ebd-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="f4ebd-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="f4ebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ebd-103">Ustawia stan usługi tworzenia maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="f4ebd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f4ebd-104">SYNTAX</span></span>

### <span data-ttu-id="f4ebd-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4ebd-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ebd-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="f4ebd-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ebd-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="f4ebd-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ebd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f4ebd-108">DESCRIPTION</span></span>
<span data-ttu-id="f4ebd-109">Ustawia stan usługi tworzenia maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="f4ebd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f4ebd-110">EXAMPLES</span></span>

### <span data-ttu-id="f4ebd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f4ebd-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="f4ebd-112">To polecenie zawiesza usługę Naprawy automatyczne na maszyny wirtualnej "maszyny wirtualne 1" w grupie zasobów "rg".</span><span class="sxs-lookup"><span data-stu-id="f4ebd-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="f4ebd-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f4ebd-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="f4ebd-114">To polecenie wznawia usługę Naprawy automatyczne na maszyny wirtualnej "maszyny wirtualne 1" w grupie zasobów "rg".</span><span class="sxs-lookup"><span data-stu-id="f4ebd-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="f4ebd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4ebd-115">PARAMETERS</span></span>

### <span data-ttu-id="f4ebd-116">— Akcja</span><span class="sxs-lookup"><span data-stu-id="f4ebd-116">-Action</span></span>
<span data-ttu-id="f4ebd-117">Czynność do wykonania.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-117">The action to be performed.</span></span>  <span data-ttu-id="f4ebd-118">Dopuszczalne wartości to: Wznów, Wstrzymaj.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ebd-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f4ebd-119">-AsJob</span></span>
<span data-ttu-id="f4ebd-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f4ebd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4ebd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ebd-121">-DefaultProfile</span></span>
<span data-ttu-id="f4ebd-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4ebd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4ebd-123">-InputObject</span></span>
<span data-ttu-id="f4ebd-124">Obiekt lokalny zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-124">The local object of the virtual machine scale set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ebd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ebd-125">-ResourceGroupName</span></span>
<span data-ttu-id="f4ebd-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4ebd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4ebd-127">-ResourceId</span></span>
<span data-ttu-id="f4ebd-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="f4ebd-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f4ebd-129">-ServiceName</span></span>
<span data-ttu-id="f4ebd-130">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ebd-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f4ebd-131">-VMScaleSetName</span></span>
<span data-ttu-id="f4ebd-132">Nazwa zestawu skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="f4ebd-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4ebd-133">-Confirm</span></span>
<span data-ttu-id="f4ebd-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ebd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ebd-135">-WhatIf</span></span>
<span data-ttu-id="f4ebd-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4ebd-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ebd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ebd-138">CommonParameters</span></span>
<span data-ttu-id="f4ebd-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ebd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ebd-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4ebd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ebd-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4ebd-141">INPUTS</span></span>

### <span data-ttu-id="f4ebd-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f4ebd-142">System.String</span></span>

### <span data-ttu-id="f4ebd-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f4ebd-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f4ebd-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4ebd-144">OUTPUTS</span></span>

### <span data-ttu-id="f4ebd-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f4ebd-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f4ebd-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f4ebd-146">NOTES</span></span>

## <span data-ttu-id="f4ebd-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4ebd-147">RELATED LINKS</span></span>
