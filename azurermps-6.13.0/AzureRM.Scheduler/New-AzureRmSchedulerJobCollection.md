---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 479b91f222852ebfc356d320cf880eb2ae99db6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541479"
---
# <span data-ttu-id="8001e-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8001e-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="8001e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8001e-102">SYNOPSIS</span></span>
<span data-ttu-id="8001e-103">Tworzy kolekcję zadań.</span><span class="sxs-lookup"><span data-stu-id="8001e-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8001e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8001e-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8001e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8001e-105">DESCRIPTION</span></span>
<span data-ttu-id="8001e-106">Polecenie cmdlet **New-AzureRmSchedulerJobCollection** tworzy kolekcję zadań w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="8001e-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="8001e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8001e-107">EXAMPLES</span></span>

## <span data-ttu-id="8001e-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8001e-108">PARAMETERS</span></span>

### <span data-ttu-id="8001e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8001e-109">-DefaultProfile</span></span>
<span data-ttu-id="8001e-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8001e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8001e-111">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="8001e-111">-Frequency</span></span>
<span data-ttu-id="8001e-112">Określa maksymalną częstotliwość, jaką można określić na dowolnym stanowisku w kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="8001e-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="8001e-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8001e-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8001e-114">Minutę</span><span class="sxs-lookup"><span data-stu-id="8001e-114">Minute</span></span> 
- <span data-ttu-id="8001e-115">Dobow</span><span class="sxs-lookup"><span data-stu-id="8001e-115">Hour</span></span> 
- <span data-ttu-id="8001e-116">Dniach</span><span class="sxs-lookup"><span data-stu-id="8001e-116">Day</span></span> 
- <span data-ttu-id="8001e-117">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="8001e-117">Week</span></span> 
- <span data-ttu-id="8001e-118">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="8001e-118">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8001e-119">-Interval</span><span class="sxs-lookup"><span data-stu-id="8001e-119">-Interval</span></span>
<span data-ttu-id="8001e-120">Określa interwał cyklu.</span><span class="sxs-lookup"><span data-stu-id="8001e-120">Specifies an interval of recurrence.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8001e-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8001e-121">-JobCollectionName</span></span>
<span data-ttu-id="8001e-122">Określa nazwę kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="8001e-122">Specifies a name for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8001e-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8001e-123">-Location</span></span>
<span data-ttu-id="8001e-124">Określa obszar Azure, w którym to polecenie cmdlet tworzy kolekcję zadań.</span><span class="sxs-lookup"><span data-stu-id="8001e-124">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8001e-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="8001e-125">-MaxJobCount</span></span>
<span data-ttu-id="8001e-126">Określa maksymalną liczbę zadań, które można utworzyć w kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="8001e-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="8001e-127">Wartość maksymalna zależy od planu, który określa parametr *Plan* .</span><span class="sxs-lookup"><span data-stu-id="8001e-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8001e-128">-Plan</span><span class="sxs-lookup"><span data-stu-id="8001e-128">-Plan</span></span>
<span data-ttu-id="8001e-129">Określa plan kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="8001e-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="8001e-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8001e-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8001e-131">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="8001e-131">Free</span></span> 
- <span data-ttu-id="8001e-132">Standard</span><span class="sxs-lookup"><span data-stu-id="8001e-132">Standard</span></span> 
- <span data-ttu-id="8001e-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="8001e-133">P10Premium</span></span> 
- <span data-ttu-id="8001e-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="8001e-134">P20Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8001e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8001e-135">-ResourceGroupName</span></span>
<span data-ttu-id="8001e-136">Określa grupę zasobów dla kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="8001e-136">Specifies the resource group for the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8001e-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8001e-137">-Confirm</span></span>
<span data-ttu-id="8001e-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8001e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8001e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8001e-139">-WhatIf</span></span>
<span data-ttu-id="8001e-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8001e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8001e-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8001e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8001e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8001e-142">CommonParameters</span></span>
<span data-ttu-id="8001e-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8001e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8001e-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8001e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8001e-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8001e-145">INPUTS</span></span>

### <span data-ttu-id="8001e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8001e-146">System.String</span></span>

## <span data-ttu-id="8001e-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8001e-147">OUTPUTS</span></span>

### <span data-ttu-id="8001e-148">Microsoft. Azure. Commands. Scheduler. models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="8001e-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="8001e-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8001e-149">NOTES</span></span>

## <span data-ttu-id="8001e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8001e-150">RELATED LINKS</span></span>

[<span data-ttu-id="8001e-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8001e-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8001e-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8001e-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8001e-153">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8001e-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8001e-154">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8001e-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8001e-155">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8001e-155">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


