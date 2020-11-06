---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2B9FEEDB-09AA-40B6-B42C-F9090F54EB3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 3a4c0cfb2e9ec3b41921e42b793a06163b9a8303
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550775"
---
# <span data-ttu-id="c212e-101">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c212e-101">New-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="c212e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c212e-102">SYNOPSIS</span></span>
<span data-ttu-id="c212e-103">Umożliwia utworzenie zadania dotyczącego tematu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="c212e-103">Creates a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c212e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c212e-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c212e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c212e-105">DESCRIPTION</span></span>
<span data-ttu-id="c212e-106">Polecenie cmdlet **New-AzureRmSchedulerServiceBusTopicJob** tworzy zadanie tematu magistrali usług w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="c212e-106">The **New-AzureRmSchedulerServiceBusTopicJob** cmdlet creates a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="c212e-107">To polecenie cmdlet obsługuje parametry dynamiczne na podstawie parametru *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="c212e-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="c212e-108">Parametry dynamiczne są dostępne na podstawie innych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="c212e-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="c212e-109">Aby wykryć nazwy parametrów dynamicznych po określeniu innych parametrów, wpisz łącznik (-), a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="c212e-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c212e-110">W przypadku pominięcia wymaganego parametru polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="c212e-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c212e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c212e-111">EXAMPLES</span></span>

## <span data-ttu-id="c212e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c212e-112">PARAMETERS</span></span>

### <span data-ttu-id="c212e-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c212e-113">-EndTime</span></span>
<span data-ttu-id="c212e-114">Określa godzinę zakończenia dla zadania jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="c212e-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="c212e-115">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="c212e-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="c212e-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="c212e-116">-ErrorActionType</span></span>
<span data-ttu-id="c212e-117">Określa ustawienie akcji błędu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="c212e-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="c212e-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c212e-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c212e-119">URL</span><span class="sxs-lookup"><span data-stu-id="c212e-119">Http</span></span> 
- <span data-ttu-id="c212e-120">Https</span><span class="sxs-lookup"><span data-stu-id="c212e-120">Https</span></span> 
- <span data-ttu-id="c212e-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="c212e-121">StorageQueue</span></span> 
- <span data-ttu-id="c212e-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="c212e-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="c212e-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="c212e-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="c212e-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="c212e-124">-ExecutionCount</span></span>
<span data-ttu-id="c212e-125">Określa, ile razy zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c212e-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="c212e-126">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="c212e-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="c212e-127">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="c212e-127">-Frequency</span></span>
<span data-ttu-id="c212e-128">Określa maksymalną częstotliwość zadania.</span><span class="sxs-lookup"><span data-stu-id="c212e-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="c212e-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c212e-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c212e-130">Minutę</span><span class="sxs-lookup"><span data-stu-id="c212e-130">Minute</span></span> 
- <span data-ttu-id="c212e-131">Dobow</span><span class="sxs-lookup"><span data-stu-id="c212e-131">Hour</span></span> 
- <span data-ttu-id="c212e-132">Dniach</span><span class="sxs-lookup"><span data-stu-id="c212e-132">Day</span></span> 
- <span data-ttu-id="c212e-133">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="c212e-133">Week</span></span> 
- <span data-ttu-id="c212e-134">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="c212e-134">Month</span></span>

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

### <span data-ttu-id="c212e-135">-Interval</span><span class="sxs-lookup"><span data-stu-id="c212e-135">-Interval</span></span>
<span data-ttu-id="c212e-136">Określa interwał cyklu zadania.</span><span class="sxs-lookup"><span data-stu-id="c212e-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="c212e-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c212e-137">-JobCollectionName</span></span>
<span data-ttu-id="c212e-138">Określa nazwę kolekcji zadań, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="c212e-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="c212e-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="c212e-139">-JobName</span></span>
<span data-ttu-id="c212e-140">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="c212e-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="c212e-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="c212e-141">-JobState</span></span>
<span data-ttu-id="c212e-142">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="c212e-142">Specifies the state of the job.</span></span>
<span data-ttu-id="c212e-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c212e-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c212e-144">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="c212e-144">Enabled</span></span> 
- <span data-ttu-id="c212e-145">Łącza</span><span class="sxs-lookup"><span data-stu-id="c212e-145">Disabled</span></span>

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

### <span data-ttu-id="c212e-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c212e-146">-ResourceGroupName</span></span>
<span data-ttu-id="c212e-147">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="c212e-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="c212e-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="c212e-148">-ServiceBusMessage</span></span>
<span data-ttu-id="c212e-149">Określa komunikat tematu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="c212e-149">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="c212e-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="c212e-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="c212e-151">Określa obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="c212e-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="c212e-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="c212e-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="c212e-153">Określa nazwę klucza podpisu z dostępem udostępnionym.</span><span class="sxs-lookup"><span data-stu-id="c212e-153">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="c212e-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="c212e-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="c212e-155">Określa wartość klucza podpisu z dostępem udostępnionym.</span><span class="sxs-lookup"><span data-stu-id="c212e-155">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="c212e-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="c212e-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="c212e-157">Określa ścieżkę tematu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="c212e-157">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="c212e-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="c212e-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="c212e-159">Określa typ transportu usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="c212e-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="c212e-160">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c212e-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c212e-161">Wiadomości SMS</span><span class="sxs-lookup"><span data-stu-id="c212e-161">NetMessaging</span></span>
- <span data-ttu-id="c212e-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="c212e-162">AMQP</span></span>

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

### <span data-ttu-id="c212e-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c212e-163">-StartTime</span></span>
<span data-ttu-id="c212e-164">Określa czas rozpoczęcia, jako obiekt **DateTime** , dla zadania.</span><span class="sxs-lookup"><span data-stu-id="c212e-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="c212e-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c212e-165">-Confirm</span></span>
<span data-ttu-id="c212e-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c212e-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c212e-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c212e-167">-WhatIf</span></span>
<span data-ttu-id="c212e-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c212e-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c212e-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c212e-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c212e-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c212e-170">-DefaultProfile</span></span>
<span data-ttu-id="c212e-171">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c212e-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c212e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c212e-172">CommonParameters</span></span>
<span data-ttu-id="c212e-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c212e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c212e-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c212e-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c212e-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c212e-175">INPUTS</span></span>

## <span data-ttu-id="c212e-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c212e-176">OUTPUTS</span></span>

### <span data-ttu-id="c212e-177">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c212e-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="c212e-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c212e-178">NOTES</span></span>

## <span data-ttu-id="c212e-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c212e-179">RELATED LINKS</span></span>

[<span data-ttu-id="c212e-180">Nowe — AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c212e-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c212e-181">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c212e-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c212e-182">Nowe — AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c212e-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c212e-183">Nowe — AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c212e-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="c212e-184">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c212e-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c212e-185">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c212e-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c212e-186">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c212e-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c212e-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c212e-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c212e-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c212e-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


