---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: d3577b906134a940a9339441f305d98c32b8fe74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550779"
---
# <span data-ttu-id="318ce-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="318ce-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="318ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="318ce-102">SYNOPSIS</span></span>
<span data-ttu-id="318ce-103">Tworzy kolekcję zadań.</span><span class="sxs-lookup"><span data-stu-id="318ce-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="318ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="318ce-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="318ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="318ce-105">DESCRIPTION</span></span>
<span data-ttu-id="318ce-106">Polecenie cmdlet **New-AzureRmSchedulerJobCollection** tworzy kolekcję zadań w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="318ce-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="318ce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="318ce-107">EXAMPLES</span></span>

## <span data-ttu-id="318ce-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="318ce-108">PARAMETERS</span></span>

### <span data-ttu-id="318ce-109">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="318ce-109">-Frequency</span></span>
<span data-ttu-id="318ce-110">Określa maksymalną częstotliwość, jaką można określić na dowolnym stanowisku w kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="318ce-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="318ce-111">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="318ce-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="318ce-112">Minutę</span><span class="sxs-lookup"><span data-stu-id="318ce-112">Minute</span></span> 
- <span data-ttu-id="318ce-113">Dobow</span><span class="sxs-lookup"><span data-stu-id="318ce-113">Hour</span></span> 
- <span data-ttu-id="318ce-114">Dniach</span><span class="sxs-lookup"><span data-stu-id="318ce-114">Day</span></span> 
- <span data-ttu-id="318ce-115">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="318ce-115">Week</span></span> 
- <span data-ttu-id="318ce-116">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="318ce-116">Month</span></span>

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

### <span data-ttu-id="318ce-117">-Interval</span><span class="sxs-lookup"><span data-stu-id="318ce-117">-Interval</span></span>
<span data-ttu-id="318ce-118">Określa interwał cyklu.</span><span class="sxs-lookup"><span data-stu-id="318ce-118">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="318ce-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="318ce-119">-JobCollectionName</span></span>
<span data-ttu-id="318ce-120">Określa nazwę kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="318ce-120">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="318ce-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="318ce-121">-Location</span></span>
<span data-ttu-id="318ce-122">Określa obszar Azure, w którym to polecenie cmdlet tworzy kolekcję zadań.</span><span class="sxs-lookup"><span data-stu-id="318ce-122">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="318ce-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="318ce-123">-MaxJobCount</span></span>
<span data-ttu-id="318ce-124">Określa maksymalną liczbę zadań, które można utworzyć w kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="318ce-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="318ce-125">Wartość maksymalna zależy od planu, który określa parametr *Plan* .</span><span class="sxs-lookup"><span data-stu-id="318ce-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="318ce-126">-Plan</span><span class="sxs-lookup"><span data-stu-id="318ce-126">-Plan</span></span>
<span data-ttu-id="318ce-127">Określa plan kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="318ce-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="318ce-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="318ce-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="318ce-129">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="318ce-129">Free</span></span> 
- <span data-ttu-id="318ce-130">Standard</span><span class="sxs-lookup"><span data-stu-id="318ce-130">Standard</span></span> 
- <span data-ttu-id="318ce-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="318ce-131">P10Premium</span></span> 
- <span data-ttu-id="318ce-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="318ce-132">P20Premium</span></span>

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

### <span data-ttu-id="318ce-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="318ce-133">-ResourceGroupName</span></span>
<span data-ttu-id="318ce-134">Określa grupę zasobów dla kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="318ce-134">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="318ce-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="318ce-135">-Confirm</span></span>
<span data-ttu-id="318ce-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="318ce-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="318ce-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="318ce-137">-WhatIf</span></span>
<span data-ttu-id="318ce-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="318ce-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="318ce-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="318ce-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="318ce-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318ce-140">-DefaultProfile</span></span>
<span data-ttu-id="318ce-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="318ce-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="318ce-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318ce-142">CommonParameters</span></span>
<span data-ttu-id="318ce-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318ce-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318ce-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="318ce-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318ce-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="318ce-145">INPUTS</span></span>

## <span data-ttu-id="318ce-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="318ce-146">OUTPUTS</span></span>

### <span data-ttu-id="318ce-147">Microsoft. Azure. Commands. Scheduler. models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="318ce-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="318ce-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="318ce-148">NOTES</span></span>

## <span data-ttu-id="318ce-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="318ce-149">RELATED LINKS</span></span>

[<span data-ttu-id="318ce-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="318ce-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="318ce-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="318ce-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="318ce-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="318ce-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="318ce-153">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="318ce-153">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="318ce-154">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="318ce-154">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


