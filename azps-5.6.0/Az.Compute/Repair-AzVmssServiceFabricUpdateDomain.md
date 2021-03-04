---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: e0edd9ad095f6f7887e0e3f4951828844d2521c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955985"
---
# <span data-ttu-id="a1d56-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="a1d56-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="a1d56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1d56-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d56-103">Podręcznik ręcznej aktualizacji platformy w domenie w celu zaktualizowania maszyn wirtualnych w zestawie skal maszyn wirtualnych w usłudze fabric.</span><span class="sxs-lookup"><span data-stu-id="a1d56-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="a1d56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1d56-104">SYNTAX</span></span>

### <span data-ttu-id="a1d56-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1d56-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1d56-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="a1d56-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d56-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="a1d56-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d56-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1d56-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d56-109">Wymusz ręczną aktualizację domeny platformy w celu zaktualizowania maszyn wirtualnych w zestawie skalowania maszyny wirtualnej w sieci szkielet usługi.</span><span class="sxs-lookup"><span data-stu-id="a1d56-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="a1d56-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1d56-110">EXAMPLES</span></span>

### <span data-ttu-id="a1d56-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1d56-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="a1d56-112">To polecenie wymusza aktualizację szkieletów usług w środowisku UD 0 dla skali maszyny wirtualnej określonej przez nazwę grupy zasobów i nazwę zestawu skalowania.</span><span class="sxs-lookup"><span data-stu-id="a1d56-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="a1d56-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a1d56-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="a1d56-114">To polecenie wymusza aktualizację szkieletów usług w usłudze UD 1 dla skali maszyny wirtualnej określonej przez obiekt zestawu skali MASZYNY WIRTUALNEj.</span><span class="sxs-lookup"><span data-stu-id="a1d56-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="a1d56-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a1d56-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="a1d56-116">To polecenie wymusza aktualizację szkieletów usług w usłudze UD 2 dla skali maszyny wirtualnej określonej przez identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a1d56-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="a1d56-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1d56-117">PARAMETERS</span></span>

### <span data-ttu-id="a1d56-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a1d56-118">-AsJob</span></span>
<span data-ttu-id="a1d56-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a1d56-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1d56-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d56-120">-DefaultProfile</span></span>
<span data-ttu-id="a1d56-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d56-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d56-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="a1d56-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="a1d56-123">Domena aktualizacji platformy, dla której jest wymagane ręczne odzyskiwanie.</span><span class="sxs-lookup"><span data-stu-id="a1d56-123">The platform update domain for which a manual recovery walk is requested.</span></span>

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

### <span data-ttu-id="a1d56-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d56-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1d56-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1d56-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1d56-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d56-126">-ResourceId</span></span>
<span data-ttu-id="a1d56-127">Identyfikator zasobu dla zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a1d56-127">The resource id for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="a1d56-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a1d56-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a1d56-129">Lokalny obiekt zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="a1d56-129">Local virtual machine scale set object</span></span>

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

### <span data-ttu-id="a1d56-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a1d56-130">-VMScaleSetName</span></span>
<span data-ttu-id="a1d56-131">Nazwa zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a1d56-131">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="a1d56-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1d56-132">-Confirm</span></span>
<span data-ttu-id="a1d56-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a1d56-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d56-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d56-134">-WhatIf</span></span>
<span data-ttu-id="a1d56-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1d56-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d56-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a1d56-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d56-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d56-137">CommonParameters</span></span>
<span data-ttu-id="a1d56-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d56-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d56-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1d56-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d56-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1d56-140">INPUTS</span></span>

### <span data-ttu-id="a1d56-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a1d56-141">System.String</span></span>

### <span data-ttu-id="a1d56-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a1d56-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a1d56-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1d56-143">OUTPUTS</span></span>

### <span data-ttu-id="a1d56-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryGrafiiResponse</span><span class="sxs-lookup"><span data-stu-id="a1d56-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="a1d56-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1d56-145">NOTES</span></span>

## <span data-ttu-id="a1d56-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1d56-146">RELATED LINKS</span></span>
