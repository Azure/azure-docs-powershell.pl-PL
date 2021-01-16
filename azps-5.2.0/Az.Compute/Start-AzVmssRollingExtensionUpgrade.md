---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347242"
---
# <span data-ttu-id="16218-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="16218-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="16218-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16218-102">SYNOPSIS</span></span>
<span data-ttu-id="16218-103">To polecenie cmdlet rozpoczyna uaktualnianie stopniowe wszystkich rozszerzeń na danej skali maszyny wirtualnej do najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="16218-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="16218-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16218-104">SYNTAX</span></span>

### <span data-ttu-id="16218-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="16218-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16218-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="16218-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16218-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16218-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16218-108">Opis</span><span class="sxs-lookup"><span data-stu-id="16218-108">DESCRIPTION</span></span>
<span data-ttu-id="16218-109">Rozpoczyna uaktualnienie stopniowe, aby przenieść wszystkie rozszerzenia tej skali maszyny wirtualnej na najnowszą dostępną wersję.</span><span class="sxs-lookup"><span data-stu-id="16218-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="16218-110">Rozszerzenia, na których jest już uruchomiona najnowsza dostępna wersja, nie ulegają zmianie.</span><span class="sxs-lookup"><span data-stu-id="16218-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="16218-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16218-111">EXAMPLES</span></span>

### <span data-ttu-id="16218-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="16218-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="16218-113">W tym przykładzie jest pobierany istniejący zestaw skali maszyny wirtualnej "MyVmssName" i dodano do niego rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="16218-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="16218-114">Polecenie ostatnie uruchamia proces uaktualniania stopniowego.</span><span class="sxs-lookup"><span data-stu-id="16218-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="16218-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16218-115">PARAMETERS</span></span>

### <span data-ttu-id="16218-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16218-116">-AsJob</span></span>
<span data-ttu-id="16218-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="16218-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16218-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16218-118">-DefaultProfile</span></span>
<span data-ttu-id="16218-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16218-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16218-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16218-120">-ResourceGroupName</span></span>
<span data-ttu-id="16218-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="16218-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="16218-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16218-122">-ResourceId</span></span>
<span data-ttu-id="16218-123">Identyfikator zasobu obiektu zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="16218-123">The resource Id of the VM scale set object.</span></span> 

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

### <span data-ttu-id="16218-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="16218-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="16218-125">Obiekt zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="16218-125">The VM scale set object.</span></span>

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

### <span data-ttu-id="16218-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="16218-126">-VMScaleSetName</span></span>
<span data-ttu-id="16218-127">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="16218-127">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="16218-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16218-128">-Confirm</span></span>
<span data-ttu-id="16218-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16218-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16218-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16218-130">-WhatIf</span></span>
<span data-ttu-id="16218-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16218-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16218-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="16218-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16218-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16218-133">CommonParameters</span></span>
<span data-ttu-id="16218-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16218-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16218-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16218-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16218-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16218-136">INPUTS</span></span>

### <span data-ttu-id="16218-137">System. String</span><span class="sxs-lookup"><span data-stu-id="16218-137">System.String</span></span>

### <span data-ttu-id="16218-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="16218-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="16218-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16218-139">OUTPUTS</span></span>

### <span data-ttu-id="16218-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="16218-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="16218-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16218-141">NOTES</span></span>

## <span data-ttu-id="16218-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16218-142">RELATED LINKS</span></span>
