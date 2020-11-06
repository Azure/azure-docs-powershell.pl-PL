---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
ms.openlocfilehash: dc147fa18d4db87b9a72aaf497f9fac59ea2a864
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525549"
---
# <span data-ttu-id="62e2f-101">Set-AzureRmVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="62e2f-101">Set-AzureRmVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="62e2f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="62e2f-103">Ustawia właściwości zasad uaktualniania stopniowego VMSS.</span><span class="sxs-lookup"><span data-stu-id="62e2f-103">Sets the VMSS rolling upgrade policy properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62e2f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62e2f-104">SYNTAX</span></span>

```
Set-AzureRmVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e2f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62e2f-105">DESCRIPTION</span></span>
<span data-ttu-id="62e2f-106">Ustawia właściwości zasad uaktualniania stopniowego VMSS.</span><span class="sxs-lookup"><span data-stu-id="62e2f-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="62e2f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62e2f-107">EXAMPLES</span></span>

### <span data-ttu-id="62e2f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62e2f-108">Example 1</span></span>
```
PS C:\> Set-AzureRmVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="62e2f-109">To polecenie ustawia 40 procent dla MaxBatchInstance, 35 procent dla MaxUnhealthyInstance, 30 procent dla MaxUnhealthyUpgradedInstance i 30 sekund czasu wstrzymania między partiami dla VMSS obiektu lokalnego $vmss.</span><span class="sxs-lookup"><span data-stu-id="62e2f-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="62e2f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62e2f-110">PARAMETERS</span></span>

### <span data-ttu-id="62e2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e2f-111">-DefaultProfile</span></span>
<span data-ttu-id="62e2f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62e2f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62e2f-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="62e2f-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="62e2f-114">Maksymalny procent wszystkich wystąpień maszyn wirtualnych, które zostaną uaktualnione jednocześnie przez uaktualnienie stopniowe w jednej partii.</span><span class="sxs-lookup"><span data-stu-id="62e2f-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="62e2f-115">Co więcej, wystąpienia niezdrowe w poprzednich lub przyszłych partiach mogą powodować zmniejszenie wartości procentowej wystąpień partii w celu zwiększenia niezawodności.</span><span class="sxs-lookup"><span data-stu-id="62e2f-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="62e2f-116">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="62e2f-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e2f-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="62e2f-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="62e2f-118">Maksymalny udział procentowy wszystkich wystąpień maszyny wirtualnej w zestawie skali, które mogą być jednocześnie niezdrowe, w wyniku uaktualnienia lub odnalezione w stanie niezdrowym przed przerwaniem uaktualnienia stopniowego przez weryfikację kondycji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="62e2f-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="62e2f-119">To ograniczenie zostanie sprawdzone przed rozpoczęciem każdej partii.</span><span class="sxs-lookup"><span data-stu-id="62e2f-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="62e2f-120">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="62e2f-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e2f-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="62e2f-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="62e2f-122">Maksymalny udział procentowy uaktualnionych wystąpień maszyny wirtualnej, które można znaleźć w nieprawidłowym stanie.</span><span class="sxs-lookup"><span data-stu-id="62e2f-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="62e2f-123">Ta kontrola będzie występować po uaktualnieniu każdej partii.</span><span class="sxs-lookup"><span data-stu-id="62e2f-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="62e2f-124">Jeśli ta wartość procentowa zostanie kiedykolwiek przekroczona, aktualizacja krocząca zostanie przerwana.</span><span class="sxs-lookup"><span data-stu-id="62e2f-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="62e2f-125">Jeśli wartość nie jest określona, jest ona ustawiona na 20.</span><span class="sxs-lookup"><span data-stu-id="62e2f-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e2f-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="62e2f-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="62e2f-127">Czas oczekiwania między ukończeniem aktualizacji dla wszystkich maszyn wirtualnych w jednej partii i rozpoczynanie następnej partii.</span><span class="sxs-lookup"><span data-stu-id="62e2f-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="62e2f-128">Czas trwania należy określić w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="62e2f-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="62e2f-129">Wartość domyślna to 0 sekund (PT0S).</span><span class="sxs-lookup"><span data-stu-id="62e2f-129">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="62e2f-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="62e2f-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="62e2f-131">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="62e2f-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="62e2f-132">Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="62e2f-132">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="62e2f-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62e2f-133">-Confirm</span></span>
<span data-ttu-id="62e2f-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62e2f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e2f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e2f-135">-WhatIf</span></span>
<span data-ttu-id="62e2f-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62e2f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62e2f-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62e2f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e2f-138">CommonParameters</span></span>
<span data-ttu-id="62e2f-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e2f-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62e2f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e2f-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62e2f-141">INPUTS</span></span>

### <span data-ttu-id="62e2f-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="62e2f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="62e2f-143">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = b77a5c561934e089]] system. String</span><span class="sxs-lookup"><span data-stu-id="62e2f-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="62e2f-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62e2f-144">OUTPUTS</span></span>

### <span data-ttu-id="62e2f-145">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="62e2f-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="62e2f-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62e2f-146">NOTES</span></span>

## <span data-ttu-id="62e2f-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62e2f-147">RELATED LINKS</span></span>

