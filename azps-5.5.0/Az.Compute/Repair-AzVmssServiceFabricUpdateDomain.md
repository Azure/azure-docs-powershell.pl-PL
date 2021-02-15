---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177483"
---
# <span data-ttu-id="f5c1e-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="f5c1e-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="f5c1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c1e-103">Podręcznik ręcznej aktualizacji platformy w domenie w celu zaktualizowania maszyn wirtualnych w zestawie skal maszyn wirtualnych w sieci szkielet usługi.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="f5c1e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5c1e-104">SYNTAX</span></span>

### <span data-ttu-id="f5c1e-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f5c1e-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5c1e-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="f5c1e-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5c1e-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="f5c1e-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5c1e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5c1e-108">DESCRIPTION</span></span>
<span data-ttu-id="f5c1e-109">Wymusz ręczną aktualizację domeny platformy w celu zaktualizowania maszyn wirtualnych w zestawie skalowania maszyny wirtualnej w materiału usługi.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="f5c1e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5c1e-110">EXAMPLES</span></span>

### <span data-ttu-id="f5c1e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5c1e-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="f5c1e-112">To polecenie wymusza aktualizację szkieletów usług w usłudze UD 0 dla skali maszyny wirtualnej określonej przez nazwę grupy zasobów i nazwę zestawu skalowania.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="f5c1e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f5c1e-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="f5c1e-114">To polecenie wymusza aktualizację szkieletów usług w usłudze UD 1 dla skali maszyny wirtualnej określonej przez obiekt zestawu skali MASZYNY WIRTUALNEj.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="f5c1e-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f5c1e-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="f5c1e-116">To polecenie wymusza aktualizację szkieletów usług w usłudze UD 2 dla skali maszyny wirtualnej określonej przez identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="f5c1e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5c1e-117">PARAMETERS</span></span>

### <span data-ttu-id="f5c1e-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f5c1e-118">-AsJob</span></span>
<span data-ttu-id="f5c1e-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f5c1e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5c1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c1e-120">-DefaultProfile</span></span>
<span data-ttu-id="f5c1e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5c1e-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="f5c1e-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="f5c1e-123">Domena aktualizacji platformy, dla której jest wymagane ręczne odzyskiwanie.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c1e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c1e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f5c1e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f5c1e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5c1e-126">-ResourceId</span></span>
<span data-ttu-id="f5c1e-127">Identyfikator zasobu dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-127">The resource id for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="f5c1e-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f5c1e-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f5c1e-129">Lokalny obiekt zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f5c1e-129">Local virtual machine scale set object</span></span>

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

### <span data-ttu-id="f5c1e-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f5c1e-130">-VMScaleSetName</span></span>
<span data-ttu-id="f5c1e-131">Nazwa zestawu skal maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f5c1e-131">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="f5c1e-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5c1e-132">-Confirm</span></span>
<span data-ttu-id="f5c1e-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5c1e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5c1e-134">-WhatIf</span></span>
<span data-ttu-id="f5c1e-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5c1e-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5c1e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c1e-137">CommonParameters</span></span>
<span data-ttu-id="f5c1e-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5c1e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c1e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5c1e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c1e-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5c1e-140">INPUTS</span></span>

### <span data-ttu-id="f5c1e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f5c1e-141">System.String</span></span>

### <span data-ttu-id="f5c1e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f5c1e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f5c1e-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5c1e-143">OUTPUTS</span></span>

### <span data-ttu-id="f5c1e-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryGrafiiResponse</span><span class="sxs-lookup"><span data-stu-id="f5c1e-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="f5c1e-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5c1e-145">NOTES</span></span>

## <span data-ttu-id="f5c1e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5c1e-146">RELATED LINKS</span></span>
