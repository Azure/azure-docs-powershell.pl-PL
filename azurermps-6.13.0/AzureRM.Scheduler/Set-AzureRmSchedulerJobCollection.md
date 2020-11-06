---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 535455f73795d85acf05da191694f35dbeee9ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543463"
---
# <span data-ttu-id="80f4d-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80f4d-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="80f4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="80f4d-103">Modyfikuje kolekcję zadań.</span><span class="sxs-lookup"><span data-stu-id="80f4d-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80f4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80f4d-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80f4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="80f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="80f4d-106">Polecenie cmdlet **Set-AzureRmSchedulerJobCollection** modyfikuje kolekcję zadań w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="80f4d-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="80f4d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80f4d-107">EXAMPLES</span></span>

## <span data-ttu-id="80f4d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80f4d-108">PARAMETERS</span></span>

### <span data-ttu-id="80f4d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f4d-109">-DefaultProfile</span></span>
<span data-ttu-id="80f4d-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80f4d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80f4d-111">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="80f4d-111">-Frequency</span></span>
<span data-ttu-id="80f4d-112">Określa maksymalną częstotliwość, jaką można określić na dowolnym stanowisku w kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="80f4d-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="80f4d-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="80f4d-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="80f4d-114">Minutę</span><span class="sxs-lookup"><span data-stu-id="80f4d-114">Minute</span></span> 
- <span data-ttu-id="80f4d-115">Dobow</span><span class="sxs-lookup"><span data-stu-id="80f4d-115">Hour</span></span> 
- <span data-ttu-id="80f4d-116">Dniach</span><span class="sxs-lookup"><span data-stu-id="80f4d-116">Day</span></span> 
- <span data-ttu-id="80f4d-117">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="80f4d-117">Week</span></span> 
- <span data-ttu-id="80f4d-118">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="80f4d-118">Month</span></span>

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

### <span data-ttu-id="80f4d-119">-Interval</span><span class="sxs-lookup"><span data-stu-id="80f4d-119">-Interval</span></span>
<span data-ttu-id="80f4d-120">Określa interwał cyklu.</span><span class="sxs-lookup"><span data-stu-id="80f4d-120">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="80f4d-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="80f4d-121">-JobCollectionName</span></span>
<span data-ttu-id="80f4d-122">Określa nazwę kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="80f4d-122">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="80f4d-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="80f4d-123">-Location</span></span>
<span data-ttu-id="80f4d-124">Określa obszar platformy Azure, w którym istnieje kolekcja zadań.</span><span class="sxs-lookup"><span data-stu-id="80f4d-124">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="80f4d-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="80f4d-125">-MaxJobCount</span></span>
<span data-ttu-id="80f4d-126">Określa maksymalną liczbę zadań, które można utworzyć w kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="80f4d-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="80f4d-127">Wartość maksymalna zależy od planu, który określa parametr *Plan* .</span><span class="sxs-lookup"><span data-stu-id="80f4d-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="80f4d-128">-Plan</span><span class="sxs-lookup"><span data-stu-id="80f4d-128">-Plan</span></span>
<span data-ttu-id="80f4d-129">Określa plan kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="80f4d-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="80f4d-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="80f4d-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="80f4d-131">Niezależnych</span><span class="sxs-lookup"><span data-stu-id="80f4d-131">Free</span></span> 
- <span data-ttu-id="80f4d-132">Standard</span><span class="sxs-lookup"><span data-stu-id="80f4d-132">Standard</span></span> 
- <span data-ttu-id="80f4d-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="80f4d-133">P10Premium</span></span> 
- <span data-ttu-id="80f4d-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="80f4d-134">P20Premium</span></span>

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

### <span data-ttu-id="80f4d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80f4d-135">-ResourceGroupName</span></span>
<span data-ttu-id="80f4d-136">Określa grupę zasobów kolekcji zadań.</span><span class="sxs-lookup"><span data-stu-id="80f4d-136">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="80f4d-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80f4d-137">-Confirm</span></span>
<span data-ttu-id="80f4d-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80f4d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80f4d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80f4d-139">-WhatIf</span></span>
<span data-ttu-id="80f4d-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80f4d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80f4d-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80f4d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80f4d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f4d-142">CommonParameters</span></span>
<span data-ttu-id="80f4d-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80f4d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f4d-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80f4d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f4d-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80f4d-145">INPUTS</span></span>

### <span data-ttu-id="80f4d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="80f4d-146">System.String</span></span>

## <span data-ttu-id="80f4d-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80f4d-147">OUTPUTS</span></span>

### <span data-ttu-id="80f4d-148">Microsoft. Azure. Commands. Scheduler. models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="80f4d-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="80f4d-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80f4d-149">NOTES</span></span>

## <span data-ttu-id="80f4d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80f4d-150">RELATED LINKS</span></span>

[<span data-ttu-id="80f4d-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80f4d-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="80f4d-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80f4d-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="80f4d-153">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80f4d-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="80f4d-154">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80f4d-154">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="80f4d-155">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="80f4d-155">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


