---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: a61d745cb748d27baf7b07b6b4389077e50aaa24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550776"
---
# <span data-ttu-id="f1a55-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="f1a55-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="f1a55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1a55-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a55-103">Tworzy zadanie kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f1a55-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1a55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1a55-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a55-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f1a55-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a55-106">Polecenie cmdlet **New-AzureRmSchedulerServiceBusQueueJob** tworzy zadanie kolejki magistrali usług w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="f1a55-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="f1a55-107">To polecenie cmdlet obsługuje parametry dynamiczne na podstawie parametru *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="f1a55-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="f1a55-108">Parametry dynamiczne są dostępne na podstawie innych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="f1a55-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="f1a55-109">Aby wykryć nazwy parametrów dynamicznych po określeniu innych parametrów, wpisz łącznik (-), a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="f1a55-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f1a55-110">W przypadku pominięcia wymaganego parametru polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="f1a55-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f1a55-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1a55-111">EXAMPLES</span></span>

## <span data-ttu-id="f1a55-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1a55-112">PARAMETERS</span></span>

### <span data-ttu-id="f1a55-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f1a55-113">-EndTime</span></span>
<span data-ttu-id="f1a55-114">Określa godzinę zakończenia dla zadania jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="f1a55-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="f1a55-115">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="f1a55-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="f1a55-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="f1a55-116">-ErrorActionType</span></span>
<span data-ttu-id="f1a55-117">Określa ustawienie akcji błędu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="f1a55-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="f1a55-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f1a55-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1a55-119">URL</span><span class="sxs-lookup"><span data-stu-id="f1a55-119">Http</span></span> 
- <span data-ttu-id="f1a55-120">Https</span><span class="sxs-lookup"><span data-stu-id="f1a55-120">Https</span></span> 
- <span data-ttu-id="f1a55-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="f1a55-121">StorageQueue</span></span> 
- <span data-ttu-id="f1a55-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="f1a55-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="f1a55-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f1a55-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="f1a55-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="f1a55-124">-ExecutionCount</span></span>
<span data-ttu-id="f1a55-125">Określa, ile razy zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f1a55-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="f1a55-126">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="f1a55-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="f1a55-127">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="f1a55-127">-Frequency</span></span>
<span data-ttu-id="f1a55-128">Określa częstotliwość zadania.</span><span class="sxs-lookup"><span data-stu-id="f1a55-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="f1a55-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f1a55-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1a55-130">Minutę</span><span class="sxs-lookup"><span data-stu-id="f1a55-130">Minute</span></span> 
- <span data-ttu-id="f1a55-131">Dobow</span><span class="sxs-lookup"><span data-stu-id="f1a55-131">Hour</span></span> 
- <span data-ttu-id="f1a55-132">Dniach</span><span class="sxs-lookup"><span data-stu-id="f1a55-132">Day</span></span> 
- <span data-ttu-id="f1a55-133">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="f1a55-133">Week</span></span> 
- <span data-ttu-id="f1a55-134">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="f1a55-134">Month</span></span>

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

### <span data-ttu-id="f1a55-135">-Interval</span><span class="sxs-lookup"><span data-stu-id="f1a55-135">-Interval</span></span>
<span data-ttu-id="f1a55-136">Określa interwał cyklu zadania.</span><span class="sxs-lookup"><span data-stu-id="f1a55-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="f1a55-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f1a55-137">-JobCollectionName</span></span>
<span data-ttu-id="f1a55-138">Określa nazwę kolekcji zadań, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="f1a55-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="f1a55-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="f1a55-139">-JobName</span></span>
<span data-ttu-id="f1a55-140">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="f1a55-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="f1a55-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="f1a55-141">-JobState</span></span>
<span data-ttu-id="f1a55-142">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="f1a55-142">Specifies the state of the job.</span></span>
<span data-ttu-id="f1a55-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f1a55-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1a55-144">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="f1a55-144">Enabled</span></span> 
- <span data-ttu-id="f1a55-145">Łącza</span><span class="sxs-lookup"><span data-stu-id="f1a55-145">Disabled</span></span>

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

### <span data-ttu-id="f1a55-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a55-146">-ResourceGroupName</span></span>
<span data-ttu-id="f1a55-147">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="f1a55-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="f1a55-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="f1a55-148">-ServiceBusMessage</span></span>
<span data-ttu-id="f1a55-149">Określa wiadomość kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f1a55-149">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="f1a55-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="f1a55-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="f1a55-151">Określa obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f1a55-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="f1a55-152">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="f1a55-152">-ServiceBusQueueName</span></span>
<span data-ttu-id="f1a55-153">Określa nazwę kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f1a55-153">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="f1a55-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="f1a55-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="f1a55-155">Określa nazwę klucza podpisu z dostępem udostępnionym.</span><span class="sxs-lookup"><span data-stu-id="f1a55-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="f1a55-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="f1a55-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="f1a55-157">Określa wartość klucza podpisu z dostępem udostępnionym.</span><span class="sxs-lookup"><span data-stu-id="f1a55-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="f1a55-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="f1a55-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="f1a55-159">Określa typ transportu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f1a55-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="f1a55-160">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f1a55-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1a55-161">Wiadomości SMS</span><span class="sxs-lookup"><span data-stu-id="f1a55-161">NetMessaging</span></span> 
- <span data-ttu-id="f1a55-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="f1a55-162">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1a55-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f1a55-163">-StartTime</span></span>
<span data-ttu-id="f1a55-164">Określa czas rozpoczęcia, jako obiekt **DateTime** , dla zadania.</span><span class="sxs-lookup"><span data-stu-id="f1a55-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="f1a55-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1a55-165">-Confirm</span></span>
<span data-ttu-id="f1a55-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1a55-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a55-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a55-167">-WhatIf</span></span>
<span data-ttu-id="f1a55-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1a55-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a55-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f1a55-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a55-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a55-170">-DefaultProfile</span></span>
<span data-ttu-id="f1a55-171">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1a55-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1a55-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a55-172">CommonParameters</span></span>
<span data-ttu-id="f1a55-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a55-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a55-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a55-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a55-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1a55-175">INPUTS</span></span>

## <span data-ttu-id="f1a55-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1a55-176">OUTPUTS</span></span>

### <span data-ttu-id="f1a55-177">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f1a55-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="f1a55-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1a55-178">NOTES</span></span>

## <span data-ttu-id="f1a55-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1a55-179">RELATED LINKS</span></span>

[<span data-ttu-id="f1a55-180">Nowe — AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f1a55-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="f1a55-181">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f1a55-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f1a55-182">Nowe — AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="f1a55-182">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="f1a55-183">Nowe — AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="f1a55-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="f1a55-184">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f1a55-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="f1a55-185">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f1a55-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f1a55-186">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="f1a55-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="f1a55-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="f1a55-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="f1a55-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="f1a55-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


