---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 7b6596d967d603a3dcecb3d20f9d2396fc00adf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547991"
---
# <span data-ttu-id="ae616-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ae616-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="ae616-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae616-102">SYNOPSIS</span></span>
<span data-ttu-id="ae616-103">Tworzy zadanie kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="ae616-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae616-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae616-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae616-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae616-105">DESCRIPTION</span></span>
<span data-ttu-id="ae616-106">Polecenie cmdlet **New-AzureRmSchedulerServiceBusQueueJob** tworzy zadanie kolejki magistrali usług w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="ae616-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="ae616-107">To polecenie cmdlet obsługuje parametry dynamiczne na podstawie parametru *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="ae616-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="ae616-108">Parametry dynamiczne są dostępne na podstawie innych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="ae616-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="ae616-109">Aby wykryć nazwy parametrów dynamicznych po określeniu innych parametrów, wpisz łącznik (-), a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="ae616-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ae616-110">W przypadku pominięcia wymaganego parametru polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="ae616-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ae616-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae616-111">EXAMPLES</span></span>

## <span data-ttu-id="ae616-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae616-112">PARAMETERS</span></span>

### <span data-ttu-id="ae616-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae616-113">-DefaultProfile</span></span>
<span data-ttu-id="ae616-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae616-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae616-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ae616-115">-EndTime</span></span>
<span data-ttu-id="ae616-116">Określa godzinę zakończenia dla zadania jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="ae616-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="ae616-117">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ae616-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="ae616-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="ae616-118">-ErrorActionType</span></span>
<span data-ttu-id="ae616-119">Określa ustawienie akcji błędu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="ae616-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="ae616-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae616-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae616-121">URL</span><span class="sxs-lookup"><span data-stu-id="ae616-121">Http</span></span> 
- <span data-ttu-id="ae616-122">Https</span><span class="sxs-lookup"><span data-stu-id="ae616-122">Https</span></span> 
- <span data-ttu-id="ae616-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="ae616-123">StorageQueue</span></span> 
- <span data-ttu-id="ae616-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ae616-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="ae616-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ae616-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="ae616-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="ae616-126">-ExecutionCount</span></span>
<span data-ttu-id="ae616-127">Określa, ile razy zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae616-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="ae616-128">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="ae616-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="ae616-129">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="ae616-129">-Frequency</span></span>
<span data-ttu-id="ae616-130">Określa częstotliwość zadania.</span><span class="sxs-lookup"><span data-stu-id="ae616-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="ae616-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae616-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae616-132">Minutę</span><span class="sxs-lookup"><span data-stu-id="ae616-132">Minute</span></span> 
- <span data-ttu-id="ae616-133">Dobow</span><span class="sxs-lookup"><span data-stu-id="ae616-133">Hour</span></span> 
- <span data-ttu-id="ae616-134">Dniach</span><span class="sxs-lookup"><span data-stu-id="ae616-134">Day</span></span> 
- <span data-ttu-id="ae616-135">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="ae616-135">Week</span></span> 
- <span data-ttu-id="ae616-136">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="ae616-136">Month</span></span>

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

### <span data-ttu-id="ae616-137">-Interval</span><span class="sxs-lookup"><span data-stu-id="ae616-137">-Interval</span></span>
<span data-ttu-id="ae616-138">Określa interwał cyklu zadania.</span><span class="sxs-lookup"><span data-stu-id="ae616-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="ae616-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ae616-139">-JobCollectionName</span></span>
<span data-ttu-id="ae616-140">Określa nazwę kolekcji zadań, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="ae616-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="ae616-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="ae616-141">-JobName</span></span>
<span data-ttu-id="ae616-142">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="ae616-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="ae616-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="ae616-143">-JobState</span></span>
<span data-ttu-id="ae616-144">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="ae616-144">Specifies the state of the job.</span></span>
<span data-ttu-id="ae616-145">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae616-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae616-146">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="ae616-146">Enabled</span></span> 
- <span data-ttu-id="ae616-147">Łącza</span><span class="sxs-lookup"><span data-stu-id="ae616-147">Disabled</span></span>

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

### <span data-ttu-id="ae616-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae616-148">-ResourceGroupName</span></span>
<span data-ttu-id="ae616-149">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="ae616-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="ae616-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="ae616-150">-ServiceBusMessage</span></span>
<span data-ttu-id="ae616-151">Określa wiadomość kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="ae616-151">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="ae616-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ae616-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="ae616-153">Określa obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="ae616-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="ae616-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="ae616-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="ae616-155">Określa nazwę kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="ae616-155">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="ae616-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="ae616-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="ae616-157">Określa nazwę klucza podpisu z dostępem udostępnionym.</span><span class="sxs-lookup"><span data-stu-id="ae616-157">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="ae616-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="ae616-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="ae616-159">Określa wartość klucza podpisu z dostępem udostępnionym.</span><span class="sxs-lookup"><span data-stu-id="ae616-159">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="ae616-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="ae616-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="ae616-161">Określa typ transportu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="ae616-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="ae616-162">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae616-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae616-163">Wiadomości SMS</span><span class="sxs-lookup"><span data-stu-id="ae616-163">NetMessaging</span></span> 
- <span data-ttu-id="ae616-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="ae616-164">AMQP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae616-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ae616-165">-StartTime</span></span>
<span data-ttu-id="ae616-166">Określa czas rozpoczęcia, jako obiekt **DateTime** , dla zadania.</span><span class="sxs-lookup"><span data-stu-id="ae616-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="ae616-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae616-167">-Confirm</span></span>
<span data-ttu-id="ae616-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae616-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae616-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae616-169">-WhatIf</span></span>
<span data-ttu-id="ae616-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae616-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae616-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae616-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae616-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae616-172">CommonParameters</span></span>
<span data-ttu-id="ae616-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae616-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae616-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae616-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae616-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae616-175">INPUTS</span></span>

### <span data-ttu-id="ae616-176">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ae616-176">None</span></span>
<span data-ttu-id="ae616-177">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ae616-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae616-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae616-178">OUTPUTS</span></span>

### <span data-ttu-id="ae616-179">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ae616-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="ae616-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae616-180">NOTES</span></span>

## <span data-ttu-id="ae616-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae616-181">RELATED LINKS</span></span>

[<span data-ttu-id="ae616-182">Nowe — AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ae616-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ae616-183">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ae616-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ae616-184">Nowe — AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ae616-184">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ae616-185">Nowe — AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ae616-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="ae616-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ae616-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ae616-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ae616-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ae616-188">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ae616-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ae616-189">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ae616-189">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ae616-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ae616-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


