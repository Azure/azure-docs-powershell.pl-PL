---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 5563B6E8-805B-463B-AF78-4F5750F5CDEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: ba8d917c33f2ab7ac6c82db303df08c01c648bf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550771"
---
# <span data-ttu-id="fd29c-101">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="fd29c-101">New-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="fd29c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd29c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd29c-103">Tworzy zadanie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="fd29c-103">Creates a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd29c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd29c-104">SYNTAX</span></span>

```
New-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -StorageSASToken <String>
 -StorageQueueMessage <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd29c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd29c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd29c-106">Polecenie cmdlet **New-AzureRmSchedulerStorageQueueJob** tworzy zadanie kolejki magazynu w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="fd29c-106">The **New-AzureRmSchedulerStorageQueueJob** cmdlet creates a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="fd29c-107">To polecenie cmdlet obsługuje parametry dynamiczne na podstawie parametru *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="fd29c-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="fd29c-108">Parametry dynamiczne są dostępne na podstawie innych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="fd29c-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="fd29c-109">Aby wykryć nazwy parametrów dynamicznych po określeniu innych parametrów, wpisz łącznik (-), a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="fd29c-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fd29c-110">W przypadku pominięcia wymaganego parametru polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="fd29c-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fd29c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd29c-111">EXAMPLES</span></span>

## <span data-ttu-id="fd29c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd29c-112">PARAMETERS</span></span>

### <span data-ttu-id="fd29c-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="fd29c-113">-EndTime</span></span>
<span data-ttu-id="fd29c-114">Określa godzinę zakończenia dla zadania jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="fd29c-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="fd29c-115">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="fd29c-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd29c-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="fd29c-116">-ErrorActionType</span></span>
<span data-ttu-id="fd29c-117">Określa ustawienie akcji błędu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="fd29c-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="fd29c-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fd29c-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd29c-119">URL</span><span class="sxs-lookup"><span data-stu-id="fd29c-119">Http</span></span> 
- <span data-ttu-id="fd29c-120">Https</span><span class="sxs-lookup"><span data-stu-id="fd29c-120">Https</span></span> 
- <span data-ttu-id="fd29c-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="fd29c-121">StorageQueue</span></span> 
- <span data-ttu-id="fd29c-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="fd29c-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="fd29c-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="fd29c-123">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd29c-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="fd29c-124">-ExecutionCount</span></span>
<span data-ttu-id="fd29c-125">Określa, ile razy zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd29c-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="fd29c-126">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="fd29c-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="fd29c-127">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="fd29c-127">-Frequency</span></span>
<span data-ttu-id="fd29c-128">Określa częstotliwość zadania.</span><span class="sxs-lookup"><span data-stu-id="fd29c-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="fd29c-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fd29c-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd29c-130">Minutę</span><span class="sxs-lookup"><span data-stu-id="fd29c-130">Minute</span></span> 
- <span data-ttu-id="fd29c-131">Dobow</span><span class="sxs-lookup"><span data-stu-id="fd29c-131">Hour</span></span> 
- <span data-ttu-id="fd29c-132">Dniach</span><span class="sxs-lookup"><span data-stu-id="fd29c-132">Day</span></span> 
- <span data-ttu-id="fd29c-133">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="fd29c-133">Week</span></span> 
- <span data-ttu-id="fd29c-134">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="fd29c-134">Month</span></span>

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

### <span data-ttu-id="fd29c-135">-Interval</span><span class="sxs-lookup"><span data-stu-id="fd29c-135">-Interval</span></span>
<span data-ttu-id="fd29c-136">Określa interwał cyklu zadania.</span><span class="sxs-lookup"><span data-stu-id="fd29c-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="fd29c-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="fd29c-137">-JobCollectionName</span></span>
<span data-ttu-id="fd29c-138">Określa nazwę kolekcji zadań, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="fd29c-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="fd29c-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="fd29c-139">-JobName</span></span>
<span data-ttu-id="fd29c-140">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="fd29c-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="fd29c-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="fd29c-141">-JobState</span></span>
<span data-ttu-id="fd29c-142">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="fd29c-142">Specifies the state of the job.</span></span>
<span data-ttu-id="fd29c-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fd29c-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd29c-144">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="fd29c-144">Enabled</span></span> 
- <span data-ttu-id="fd29c-145">Łącza</span><span class="sxs-lookup"><span data-stu-id="fd29c-145">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd29c-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd29c-146">-ResourceGroupName</span></span>
<span data-ttu-id="fd29c-147">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="fd29c-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="fd29c-148">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fd29c-148">-StartTime</span></span>
<span data-ttu-id="fd29c-149">Określa czas rozpoczęcia, jako obiekt **DateTime** , dla zadania.</span><span class="sxs-lookup"><span data-stu-id="fd29c-149">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd29c-150">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="fd29c-150">-StorageQueueAccount</span></span>
<span data-ttu-id="fd29c-151">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="fd29c-151">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="fd29c-152">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="fd29c-152">-StorageQueueMessage</span></span>
<span data-ttu-id="fd29c-153">Określa komunikat kolejki dla zadania magazynowania.</span><span class="sxs-lookup"><span data-stu-id="fd29c-153">Specifies a queue message for the storage job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd29c-154">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="fd29c-154">-StorageQueueName</span></span>
<span data-ttu-id="fd29c-155">Określa nazwę kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="fd29c-155">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="fd29c-156">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="fd29c-156">-StorageSASToken</span></span>
<span data-ttu-id="fd29c-157">Określa token podpisu dostępu współdzielonego dla kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="fd29c-157">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="fd29c-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd29c-158">-Confirm</span></span>
<span data-ttu-id="fd29c-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd29c-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd29c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd29c-160">-WhatIf</span></span>
<span data-ttu-id="fd29c-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd29c-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd29c-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd29c-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd29c-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd29c-163">-DefaultProfile</span></span>
<span data-ttu-id="fd29c-164">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd29c-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd29c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd29c-165">CommonParameters</span></span>
<span data-ttu-id="fd29c-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd29c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd29c-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd29c-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd29c-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd29c-168">INPUTS</span></span>

## <span data-ttu-id="fd29c-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd29c-169">OUTPUTS</span></span>

### <span data-ttu-id="fd29c-170">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fd29c-170">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="fd29c-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd29c-171">NOTES</span></span>

## <span data-ttu-id="fd29c-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd29c-172">RELATED LINKS</span></span>

[<span data-ttu-id="fd29c-173">Nowe — AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="fd29c-173">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="fd29c-174">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fd29c-174">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="fd29c-175">Nowe — AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="fd29c-175">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="fd29c-176">Nowe — AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="fd29c-176">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="fd29c-177">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="fd29c-177">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="fd29c-178">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="fd29c-178">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="fd29c-179">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="fd29c-179">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="fd29c-180">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="fd29c-180">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="fd29c-181">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="fd29c-181">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


