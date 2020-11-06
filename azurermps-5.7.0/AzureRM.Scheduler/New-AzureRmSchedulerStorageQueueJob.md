---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5563B6E8-805B-463B-AF78-4F5750F5CDEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: eb72b64576524d85730e89f6eece094591a12158
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551595"
---
# <span data-ttu-id="29bc7-101">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="29bc7-101">New-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="29bc7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="29bc7-103">Tworzy zadanie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="29bc7-103">Creates a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29bc7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29bc7-104">SYNTAX</span></span>

```
New-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -StorageSASToken <String>
 -StorageQueueMessage <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29bc7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="29bc7-106">Polecenie cmdlet **New-AzureRmSchedulerStorageQueueJob** tworzy zadanie kolejki magazynu w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="29bc7-106">The **New-AzureRmSchedulerStorageQueueJob** cmdlet creates a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="29bc7-107">To polecenie cmdlet obsługuje parametry dynamiczne na podstawie parametru *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="29bc7-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="29bc7-108">Parametry dynamiczne są dostępne na podstawie innych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="29bc7-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="29bc7-109">Aby wykryć nazwy parametrów dynamicznych po określeniu innych parametrów, wpisz łącznik (-), a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="29bc7-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="29bc7-110">W przypadku pominięcia wymaganego parametru polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="29bc7-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="29bc7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29bc7-111">EXAMPLES</span></span>

## <span data-ttu-id="29bc7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29bc7-112">PARAMETERS</span></span>

### <span data-ttu-id="29bc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bc7-113">-DefaultProfile</span></span>
<span data-ttu-id="29bc7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29bc7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="29bc7-115">-EndTime</span></span>
<span data-ttu-id="29bc7-116">Określa godzinę zakończenia dla zadania jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="29bc7-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="29bc7-117">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="29bc7-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="29bc7-118">-ErrorActionType</span></span>
<span data-ttu-id="29bc7-119">Określa ustawienie akcji błędu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="29bc7-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="29bc7-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="29bc7-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29bc7-121">URL</span><span class="sxs-lookup"><span data-stu-id="29bc7-121">Http</span></span> 
- <span data-ttu-id="29bc7-122">Https</span><span class="sxs-lookup"><span data-stu-id="29bc7-122">Https</span></span> 
- <span data-ttu-id="29bc7-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="29bc7-123">StorageQueue</span></span> 
- <span data-ttu-id="29bc7-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="29bc7-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="29bc7-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="29bc7-125">ServiceBusTopic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="29bc7-126">-ExecutionCount</span></span>
<span data-ttu-id="29bc7-127">Określa, ile razy zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29bc7-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="29bc7-128">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="29bc7-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-129">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="29bc7-129">-Frequency</span></span>
<span data-ttu-id="29bc7-130">Określa częstotliwość zadania.</span><span class="sxs-lookup"><span data-stu-id="29bc7-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="29bc7-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="29bc7-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29bc7-132">Minutę</span><span class="sxs-lookup"><span data-stu-id="29bc7-132">Minute</span></span> 
- <span data-ttu-id="29bc7-133">Dobow</span><span class="sxs-lookup"><span data-stu-id="29bc7-133">Hour</span></span> 
- <span data-ttu-id="29bc7-134">Dniach</span><span class="sxs-lookup"><span data-stu-id="29bc7-134">Day</span></span> 
- <span data-ttu-id="29bc7-135">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="29bc7-135">Week</span></span> 
- <span data-ttu-id="29bc7-136">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="29bc7-136">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-137">-Interval</span><span class="sxs-lookup"><span data-stu-id="29bc7-137">-Interval</span></span>
<span data-ttu-id="29bc7-138">Określa interwał cyklu zadania.</span><span class="sxs-lookup"><span data-stu-id="29bc7-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="29bc7-139">-JobCollectionName</span></span>
<span data-ttu-id="29bc7-140">Określa nazwę kolekcji zadań, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="29bc7-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="29bc7-141">-JobName</span></span>
<span data-ttu-id="29bc7-142">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="29bc7-142">Specifies a name for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="29bc7-143">-JobState</span></span>
<span data-ttu-id="29bc7-144">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="29bc7-144">Specifies the state of the job.</span></span>
<span data-ttu-id="29bc7-145">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="29bc7-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29bc7-146">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="29bc7-146">Enabled</span></span> 
- <span data-ttu-id="29bc7-147">Łącza</span><span class="sxs-lookup"><span data-stu-id="29bc7-147">Disabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29bc7-148">-ResourceGroupName</span></span>
<span data-ttu-id="29bc7-149">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="29bc7-149">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="29bc7-150">-StartTime</span></span>
<span data-ttu-id="29bc7-151">Określa czas rozpoczęcia, jako obiekt **DateTime** , dla zadania.</span><span class="sxs-lookup"><span data-stu-id="29bc7-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="29bc7-152">-StorageQueueAccount</span></span>
<span data-ttu-id="29bc7-153">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="29bc7-153">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="29bc7-154">-StorageQueueMessage</span></span>
<span data-ttu-id="29bc7-155">Określa komunikat kolejki dla zadania magazynowania.</span><span class="sxs-lookup"><span data-stu-id="29bc7-155">Specifies a queue message for the storage job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="29bc7-156">-StorageQueueName</span></span>
<span data-ttu-id="29bc7-157">Określa nazwę kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="29bc7-157">Specifies a storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="29bc7-158">-StorageSASToken</span></span>
<span data-ttu-id="29bc7-159">Określa token podpisu dostępu współdzielonego dla kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="29bc7-159">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29bc7-160">-Confirm</span></span>
<span data-ttu-id="29bc7-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29bc7-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29bc7-162">-WhatIf</span></span>
<span data-ttu-id="29bc7-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29bc7-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29bc7-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29bc7-164">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29bc7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bc7-165">CommonParameters</span></span>
<span data-ttu-id="29bc7-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29bc7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bc7-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29bc7-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bc7-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29bc7-168">INPUTS</span></span>

### <span data-ttu-id="29bc7-169">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="29bc7-169">None</span></span>
<span data-ttu-id="29bc7-170">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="29bc7-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29bc7-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29bc7-171">OUTPUTS</span></span>

### <span data-ttu-id="29bc7-172">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="29bc7-172">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="29bc7-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29bc7-173">NOTES</span></span>

## <span data-ttu-id="29bc7-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29bc7-174">RELATED LINKS</span></span>

[<span data-ttu-id="29bc7-175">Nowe — AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="29bc7-175">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="29bc7-176">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="29bc7-176">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="29bc7-177">Nowe — AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="29bc7-177">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="29bc7-178">Nowe — AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="29bc7-178">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="29bc7-179">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="29bc7-179">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="29bc7-180">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="29bc7-180">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="29bc7-181">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="29bc7-181">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="29bc7-182">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="29bc7-182">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="29bc7-183">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="29bc7-183">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


