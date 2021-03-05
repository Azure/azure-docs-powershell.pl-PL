---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: 2816f34c8a6148d67a5bed397e573b07fa2e7004
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986917"
---
# <span data-ttu-id="edb5b-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="edb5b-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="edb5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb5b-102">SYNOPSIS</span></span>
<span data-ttu-id="edb5b-103">To polecenie cmdlet rozpoczyna uaktualnianie w celu uaktualnienia do najnowszej dostępnej wersji dla wszystkich rozszerzeń dla danego zestawu skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="edb5b-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="edb5b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="edb5b-104">SYNTAX</span></span>

### <span data-ttu-id="edb5b-105">DefaultParameters</span><span class="sxs-lookup"><span data-stu-id="edb5b-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edb5b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="edb5b-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edb5b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="edb5b-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb5b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="edb5b-108">DESCRIPTION</span></span>
<span data-ttu-id="edb5b-109">Rozpoczyna uaktualnianie, aby przenieść wszystkie rozszerzenia na tej skali maszyny wirtualnej do najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="edb5b-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="edb5b-110">Nie ma to wpływu na rozszerzenia, które już działają w najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="edb5b-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="edb5b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="edb5b-111">EXAMPLES</span></span>

### <span data-ttu-id="edb5b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="edb5b-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="edb5b-113">W tym przykładzie istniejący zestaw skali maszyny wirtualnej "MyVmssName" jest zwiększany i dodaje do niego rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="edb5b-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="edb5b-114">Ostatnie polecenie uruchamia proces uaktualniania w trakcie uaktualniania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="edb5b-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="edb5b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edb5b-115">PARAMETERS</span></span>

### <span data-ttu-id="edb5b-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="edb5b-116">-AsJob</span></span>
<span data-ttu-id="edb5b-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="edb5b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edb5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb5b-118">-DefaultProfile</span></span>
<span data-ttu-id="edb5b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="edb5b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edb5b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb5b-120">-ResourceGroupName</span></span>
<span data-ttu-id="edb5b-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="edb5b-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb5b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edb5b-122">-ResourceId</span></span>
<span data-ttu-id="edb5b-123">Identyfikator zasobu obiektu zestawu skali MASZYNY WIRTUALNEj.</span><span class="sxs-lookup"><span data-stu-id="edb5b-123">The resource Id of the VM scale set object.</span></span> 

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edb5b-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="edb5b-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="edb5b-125">Obiekt zestawu skali MASZYNY WIRTUALNEj.</span><span class="sxs-lookup"><span data-stu-id="edb5b-125">The VM scale set object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edb5b-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="edb5b-126">-VMScaleSetName</span></span>
<span data-ttu-id="edb5b-127">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="edb5b-127">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb5b-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edb5b-128">-Confirm</span></span>
<span data-ttu-id="edb5b-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="edb5b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb5b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb5b-130">-WhatIf</span></span>
<span data-ttu-id="edb5b-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb5b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edb5b-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="edb5b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb5b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb5b-133">CommonParameters</span></span>
<span data-ttu-id="edb5b-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb5b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb5b-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edb5b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb5b-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edb5b-136">INPUTS</span></span>

### <span data-ttu-id="edb5b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="edb5b-137">System.String</span></span>

### <span data-ttu-id="edb5b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="edb5b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="edb5b-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edb5b-139">OUTPUTS</span></span>

### <span data-ttu-id="edb5b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="edb5b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="edb5b-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="edb5b-141">NOTES</span></span>

## <span data-ttu-id="edb5b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edb5b-142">RELATED LINKS</span></span>
