---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 16ea3a8754ef08e933412582f100296d07fcb430
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958881"
---
# <span data-ttu-id="2d14d-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="2d14d-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="2d14d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d14d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d14d-103">Ustawia właściwości zasad wycofywania aktualizacji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2d14d-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="2d14d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d14d-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d14d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d14d-105">DESCRIPTION</span></span>
<span data-ttu-id="2d14d-106">Ustawia właściwości zasad wycofywania aktualizacji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2d14d-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="2d14d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d14d-107">EXAMPLES</span></span>

### <span data-ttu-id="2d14d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d14d-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="2d14d-109">To polecenie ustawia wartość 40 procent dla wartości MaxBatchInstance, 35 procent dla wartości MaxUnhealthyInstance, 30 procent dla wartości MaxUnhealthyUpgradedInstance i 30-sekundowy czas wstrzymania między partiami dla obiektu lokalnego VMSS $vmss.</span><span class="sxs-lookup"><span data-stu-id="2d14d-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="2d14d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d14d-110">PARAMETERS</span></span>

### <span data-ttu-id="2d14d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d14d-111">-DefaultProfile</span></span>
<span data-ttu-id="2d14d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d14d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d14d-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2d14d-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="2d14d-114">Maksymalny procent całkowitej liczby wystąpień maszyn wirtualnych, które zostaną uaktualnione jednocześnie przez uaktualnianie w jednej partii.</span><span class="sxs-lookup"><span data-stu-id="2d14d-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="2d14d-115">Ponieważ jest to maksymalna liczba wystąpień w poprzednich lub przyszłych partiach o złej kondycji, może spowodować zmniejszenie procentu wystąpień w partii w celu zapewnienia większej niezawodności.</span><span class="sxs-lookup"><span data-stu-id="2d14d-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="2d14d-116">Jeśli wartość nie zostanie określona, zostanie ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="2d14d-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d14d-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2d14d-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="2d14d-118">Maksymalna wartość procentowa całkowitej liczby wystąpień maszyn wirtualnych w zestawie skali, które mogą być jednocześnie w złej kondycji w wyniku uaktualnienia lub w wyniku wystąpienia w stanie złej kondycji przez testy kondycji maszyn wirtualnych przed kropkami uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="2d14d-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="2d14d-119">To ograniczenie będzie sprawdzane przed uruchomieniem dowolnej partii.</span><span class="sxs-lookup"><span data-stu-id="2d14d-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="2d14d-120">Jeśli wartość nie zostanie określona, zostanie ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="2d14d-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d14d-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2d14d-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="2d14d-122">Maksymalna wartość procentowa uaktualnionych wystąpień maszyn wirtualnych, które mogą być w stanie o złej kondycji.</span><span class="sxs-lookup"><span data-stu-id="2d14d-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="2d14d-123">Ten sprawdzanie będzie się odbywać po uaktualnieniu każdej partii.</span><span class="sxs-lookup"><span data-stu-id="2d14d-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="2d14d-124">Jeśli wartość procentowa będzie kiedykolwiek przekroczona, czas aktualizacji jest przerywany.</span><span class="sxs-lookup"><span data-stu-id="2d14d-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="2d14d-125">Jeśli wartość nie zostanie określona, zostanie ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="2d14d-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d14d-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="2d14d-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="2d14d-127">Czas oczekiwania między ukończeniem aktualizacji dla wszystkich maszyn wirtualnych w jednej partii a rozpoczęciem następnej partii.</span><span class="sxs-lookup"><span data-stu-id="2d14d-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="2d14d-128">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="2d14d-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="2d14d-129">Wartość domyślna to 0 sekund (PT0S).</span><span class="sxs-lookup"><span data-stu-id="2d14d-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d14d-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2d14d-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2d14d-131">Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="2d14d-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="2d14d-132">Obiekt można New-AzVmssConfig za pomocą polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d14d-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="2d14d-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d14d-133">-Confirm</span></span>
<span data-ttu-id="2d14d-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2d14d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d14d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d14d-135">-WhatIf</span></span>
<span data-ttu-id="2d14d-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d14d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d14d-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2d14d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d14d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d14d-138">CommonParameters</span></span>
<span data-ttu-id="2d14d-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d14d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d14d-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d14d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d14d-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d14d-141">INPUTS</span></span>

### <span data-ttu-id="2d14d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2d14d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2d14d-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2d14d-143">System.Int32</span></span>

### <span data-ttu-id="2d14d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2d14d-144">System.String</span></span>

## <span data-ttu-id="2d14d-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d14d-145">OUTPUTS</span></span>

### <span data-ttu-id="2d14d-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2d14d-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2d14d-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d14d-147">NOTES</span></span>

## <span data-ttu-id="2d14d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d14d-148">RELATED LINKS</span></span>
