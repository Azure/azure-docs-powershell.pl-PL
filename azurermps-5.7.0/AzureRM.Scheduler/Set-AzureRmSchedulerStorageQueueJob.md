---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: d93ceb91ded5161dc962f902434cefe0f2070ae5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716611"
---
# <span data-ttu-id="1875e-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="1875e-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="1875e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1875e-102">SYNOPSIS</span></span>
<span data-ttu-id="1875e-103">Modyfikuje zadanie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="1875e-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1875e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1875e-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1875e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1875e-105">DESCRIPTION</span></span>
<span data-ttu-id="1875e-106">Polecenie cmdlet **Set-AzureRmSchedulerStorageQueueJob** modyfikuje zadanie kolejki magazynowania w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="1875e-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="1875e-107">To polecenie cmdlet obsługuje parametry dynamiczne na podstawie parametru *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="1875e-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="1875e-108">Parametry dynamiczne są dostępne na podstawie innych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="1875e-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="1875e-109">Aby wykryć nazwy parametrów dynamicznych po określeniu innych parametrów, wpisz łącznik (-), a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="1875e-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1875e-110">W przypadku pominięcia wymaganego parametru polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="1875e-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1875e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1875e-111">EXAMPLES</span></span>

## <span data-ttu-id="1875e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1875e-112">PARAMETERS</span></span>

### <span data-ttu-id="1875e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1875e-113">-DefaultProfile</span></span>
<span data-ttu-id="1875e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1875e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1875e-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1875e-115">-EndTime</span></span>
<span data-ttu-id="1875e-116">Określa godzinę zakończenia dla zadania jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="1875e-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="1875e-117">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="1875e-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="1875e-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="1875e-118">-ErrorActionType</span></span>
<span data-ttu-id="1875e-119">Określa ustawienie akcji błędu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="1875e-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="1875e-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1875e-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1875e-121">URL</span><span class="sxs-lookup"><span data-stu-id="1875e-121">Http</span></span> 
- <span data-ttu-id="1875e-122">Https</span><span class="sxs-lookup"><span data-stu-id="1875e-122">Https</span></span> 
- <span data-ttu-id="1875e-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="1875e-123">StorageQueue</span></span> 
- <span data-ttu-id="1875e-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="1875e-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="1875e-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="1875e-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="1875e-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="1875e-126">-ExecutionCount</span></span>
<span data-ttu-id="1875e-127">Określa, ile razy zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1875e-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="1875e-128">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="1875e-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="1875e-129">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="1875e-129">-Frequency</span></span>
<span data-ttu-id="1875e-130">Określa częstotliwość zadania.</span><span class="sxs-lookup"><span data-stu-id="1875e-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="1875e-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1875e-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1875e-132">Minutę</span><span class="sxs-lookup"><span data-stu-id="1875e-132">Minute</span></span> 
- <span data-ttu-id="1875e-133">Dobow</span><span class="sxs-lookup"><span data-stu-id="1875e-133">Hour</span></span> 
- <span data-ttu-id="1875e-134">Dniach</span><span class="sxs-lookup"><span data-stu-id="1875e-134">Day</span></span> 
- <span data-ttu-id="1875e-135">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="1875e-135">Week</span></span> 
- <span data-ttu-id="1875e-136">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="1875e-136">Month</span></span>

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

### <span data-ttu-id="1875e-137">-Interval</span><span class="sxs-lookup"><span data-stu-id="1875e-137">-Interval</span></span>
<span data-ttu-id="1875e-138">Określa interwał cyklu zadania.</span><span class="sxs-lookup"><span data-stu-id="1875e-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="1875e-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="1875e-139">-JobCollectionName</span></span>
<span data-ttu-id="1875e-140">Określa nazwę kolekcji zadań, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="1875e-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="1875e-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="1875e-141">-JobName</span></span>
<span data-ttu-id="1875e-142">Określa nazwę zadania modyfikowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1875e-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1875e-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="1875e-143">-JobState</span></span>
<span data-ttu-id="1875e-144">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="1875e-144">Specifies the state of the job.</span></span>
<span data-ttu-id="1875e-145">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1875e-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1875e-146">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="1875e-146">Enabled</span></span> 
- <span data-ttu-id="1875e-147">Łącza</span><span class="sxs-lookup"><span data-stu-id="1875e-147">Disabled</span></span>

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

### <span data-ttu-id="1875e-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1875e-148">-ResourceGroupName</span></span>
<span data-ttu-id="1875e-149">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="1875e-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="1875e-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1875e-150">-StartTime</span></span>
<span data-ttu-id="1875e-151">Określa czas rozpoczęcia, jako obiekt **DateTime** , dla zadania.</span><span class="sxs-lookup"><span data-stu-id="1875e-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="1875e-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="1875e-152">-StorageQueueAccount</span></span>
<span data-ttu-id="1875e-153">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1875e-153">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1875e-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="1875e-154">-StorageQueueMessage</span></span>
<span data-ttu-id="1875e-155">Określa komunikat kolejki dla zadania magazynowania.</span><span class="sxs-lookup"><span data-stu-id="1875e-155">Specifies a queue message for storage job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1875e-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="1875e-156">-StorageQueueName</span></span>
<span data-ttu-id="1875e-157">Określa nazwę kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="1875e-157">Specifies a storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1875e-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="1875e-158">-StorageSASToken</span></span>
<span data-ttu-id="1875e-159">Określa token podpisu dostępu współdzielonego dla kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="1875e-159">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1875e-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1875e-160">-Confirm</span></span>
<span data-ttu-id="1875e-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1875e-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1875e-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1875e-162">-WhatIf</span></span>
<span data-ttu-id="1875e-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1875e-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1875e-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1875e-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1875e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1875e-165">CommonParameters</span></span>
<span data-ttu-id="1875e-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1875e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1875e-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1875e-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1875e-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1875e-168">INPUTS</span></span>

### <span data-ttu-id="1875e-169">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1875e-169">None</span></span>
<span data-ttu-id="1875e-170">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1875e-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1875e-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1875e-171">OUTPUTS</span></span>

### <span data-ttu-id="1875e-172">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1875e-172">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="1875e-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1875e-173">NOTES</span></span>

## <span data-ttu-id="1875e-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1875e-174">RELATED LINKS</span></span>

[<span data-ttu-id="1875e-175">Nowe — AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="1875e-175">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="1875e-176">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1875e-176">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1875e-177">Nowe — AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="1875e-177">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="1875e-178">Nowe — AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="1875e-178">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="1875e-179">Nowe — AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="1875e-179">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="1875e-180">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="1875e-180">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="1875e-181">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="1875e-181">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="1875e-182">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="1875e-182">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="1875e-183">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="1875e-183">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


