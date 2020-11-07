---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2C8C98B8-7A3B-4F24-BDF1-0B7B81049956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: bbc2661f585dacc5537583d8282c76e6fdcd7562
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718015"
---
# <span data-ttu-id="15c38-101">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="15c38-101">Set-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="15c38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15c38-102">SYNOPSIS</span></span>
<span data-ttu-id="15c38-103">Modyfikowanie zadania kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="15c38-103">Modifies a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15c38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15c38-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> [-ServiceBusQueueName <String>] -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15c38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="15c38-105">DESCRIPTION</span></span>
<span data-ttu-id="15c38-106">Polecenie cmdlet **Set-AzureRmSchedulerServiceBusQueueJob** modyfikuje zadanie kolejki usługi Service Bus w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="15c38-106">The **Set-AzureRmSchedulerServiceBusQueueJob** cmdlet modifies a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="15c38-107">To polecenie cmdlet obsługuje parametry dynamiczne na podstawie parametru *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="15c38-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="15c38-108">Parametry dynamiczne są dostępne na podstawie innych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="15c38-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="15c38-109">Aby wykryć nazwy parametrów dynamicznych po określeniu innych parametrów, wpisz łącznik (-), a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="15c38-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="15c38-110">W przypadku pominięcia wymaganego parametru polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="15c38-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="15c38-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15c38-111">EXAMPLES</span></span>

## <span data-ttu-id="15c38-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15c38-112">PARAMETERS</span></span>

### <span data-ttu-id="15c38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c38-113">-DefaultProfile</span></span>
<span data-ttu-id="15c38-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15c38-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15c38-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="15c38-115">-EndTime</span></span>
<span data-ttu-id="15c38-116">Określa godzinę zakończenia dla zadania jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="15c38-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="15c38-117">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="15c38-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="15c38-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="15c38-118">-ErrorActionType</span></span>
<span data-ttu-id="15c38-119">Określa ustawienie akcji błędu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="15c38-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="15c38-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="15c38-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15c38-121">URL</span><span class="sxs-lookup"><span data-stu-id="15c38-121">Http</span></span> 
- <span data-ttu-id="15c38-122">Https</span><span class="sxs-lookup"><span data-stu-id="15c38-122">Https</span></span> 
- <span data-ttu-id="15c38-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="15c38-123">StorageQueue</span></span> 
- <span data-ttu-id="15c38-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="15c38-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="15c38-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="15c38-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="15c38-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="15c38-126">-ExecutionCount</span></span>
<span data-ttu-id="15c38-127">Określa, ile razy zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15c38-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="15c38-128">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="15c38-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="15c38-129">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="15c38-129">-Frequency</span></span>
<span data-ttu-id="15c38-130">Określa częstotliwość zadania.</span><span class="sxs-lookup"><span data-stu-id="15c38-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="15c38-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="15c38-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15c38-132">Minutę</span><span class="sxs-lookup"><span data-stu-id="15c38-132">Minute</span></span> 
- <span data-ttu-id="15c38-133">Dobow</span><span class="sxs-lookup"><span data-stu-id="15c38-133">Hour</span></span> 
- <span data-ttu-id="15c38-134">Dniach</span><span class="sxs-lookup"><span data-stu-id="15c38-134">Day</span></span> 
- <span data-ttu-id="15c38-135">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="15c38-135">Week</span></span> 
- <span data-ttu-id="15c38-136">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="15c38-136">Month</span></span>

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

### <span data-ttu-id="15c38-137">-Interval</span><span class="sxs-lookup"><span data-stu-id="15c38-137">-Interval</span></span>
<span data-ttu-id="15c38-138">Określa interwał cyklu zadania.</span><span class="sxs-lookup"><span data-stu-id="15c38-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="15c38-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="15c38-139">-JobCollectionName</span></span>
<span data-ttu-id="15c38-140">Określa nazwę kolekcji zadań, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="15c38-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="15c38-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="15c38-141">-JobName</span></span>
<span data-ttu-id="15c38-142">Określa nazwę zadania modyfikowanego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15c38-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="15c38-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="15c38-143">-JobState</span></span>
<span data-ttu-id="15c38-144">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="15c38-144">Specifies the state of the job.</span></span>
<span data-ttu-id="15c38-145">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="15c38-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15c38-146">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="15c38-146">Enabled</span></span> 
- <span data-ttu-id="15c38-147">Łącza</span><span class="sxs-lookup"><span data-stu-id="15c38-147">Disabled</span></span>

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

### <span data-ttu-id="15c38-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c38-148">-ResourceGroupName</span></span>
<span data-ttu-id="15c38-149">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="15c38-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="15c38-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="15c38-150">-ServiceBusMessage</span></span>
<span data-ttu-id="15c38-151">Określa wiadomość kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="15c38-151">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="15c38-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="15c38-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="15c38-153">Określa obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="15c38-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="15c38-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="15c38-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="15c38-155">Określa nazwę kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="15c38-155">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="15c38-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="15c38-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="15c38-157">Określa nazwę klucza podpisu z dostępem udostępnionym.</span><span class="sxs-lookup"><span data-stu-id="15c38-157">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="15c38-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="15c38-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="15c38-159">Określa wartość klucza podpisu z dostępem udostępnionym.</span><span class="sxs-lookup"><span data-stu-id="15c38-159">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="15c38-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="15c38-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="15c38-161">Określa typ transportu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="15c38-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="15c38-162">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="15c38-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15c38-163">Wiadomości SMS</span><span class="sxs-lookup"><span data-stu-id="15c38-163">NetMessaging</span></span> 
- <span data-ttu-id="15c38-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="15c38-164">AMQP</span></span>

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

### <span data-ttu-id="15c38-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="15c38-165">-StartTime</span></span>
<span data-ttu-id="15c38-166">Określa czas rozpoczęcia, jako obiekt **DateTime** , dla zadania.</span><span class="sxs-lookup"><span data-stu-id="15c38-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="15c38-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15c38-167">-Confirm</span></span>
<span data-ttu-id="15c38-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15c38-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c38-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c38-169">-WhatIf</span></span>
<span data-ttu-id="15c38-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15c38-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15c38-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15c38-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c38-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c38-172">CommonParameters</span></span>
<span data-ttu-id="15c38-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c38-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c38-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15c38-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c38-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15c38-175">INPUTS</span></span>

### <span data-ttu-id="15c38-176">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="15c38-176">None</span></span>
<span data-ttu-id="15c38-177">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="15c38-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15c38-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15c38-178">OUTPUTS</span></span>

### <span data-ttu-id="15c38-179">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="15c38-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="15c38-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15c38-180">NOTES</span></span>

## <span data-ttu-id="15c38-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15c38-181">RELATED LINKS</span></span>

[<span data-ttu-id="15c38-182">Nowe — AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="15c38-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="15c38-183">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="15c38-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="15c38-184">Nowe — AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="15c38-184">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="15c38-185">Nowe — AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="15c38-185">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="15c38-186">Nowe — AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="15c38-186">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="15c38-187">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="15c38-187">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="15c38-188">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="15c38-188">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="15c38-189">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="15c38-189">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="15c38-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="15c38-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


