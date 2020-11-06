---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 1d0c66d3442d6db03897140849f5713d3107f8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552516"
---
# <span data-ttu-id="6705a-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="6705a-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="6705a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6705a-102">SYNOPSIS</span></span>
<span data-ttu-id="6705a-103">Tworzy zadanie HTTP.</span><span class="sxs-lookup"><span data-stu-id="6705a-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6705a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6705a-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6705a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6705a-105">DESCRIPTION</span></span>
<span data-ttu-id="6705a-106">Polecenie cmdlet **New-AzureRmSchedulerHttpJob** tworzy zadanie http w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="6705a-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="6705a-107">To polecenie cmdlet obsługuje parametry dynamiczne na podstawie parametrów *ErrorActionType* i *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="6705a-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="6705a-108">Parametry dynamiczne są dostępne na podstawie innych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="6705a-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="6705a-109">Aby wykryć nazwy parametrów dynamicznych po określeniu innych parametrów, wpisz łącznik (-), a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="6705a-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6705a-110">W przypadku pominięcia wymaganego parametru polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="6705a-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6705a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6705a-111">EXAMPLES</span></span>

## <span data-ttu-id="6705a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6705a-112">PARAMETERS</span></span>

### <span data-ttu-id="6705a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6705a-113">-DefaultProfile</span></span>
<span data-ttu-id="6705a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6705a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6705a-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6705a-115">-EndTime</span></span>
<span data-ttu-id="6705a-116">Określa godzinę zakończenia dla zadania jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="6705a-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="6705a-117">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="6705a-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="6705a-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="6705a-118">-ErrorActionType</span></span>
<span data-ttu-id="6705a-119">Określa ustawienie akcji błędu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="6705a-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="6705a-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6705a-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6705a-121">URL</span><span class="sxs-lookup"><span data-stu-id="6705a-121">Http</span></span> 
- <span data-ttu-id="6705a-122">Https</span><span class="sxs-lookup"><span data-stu-id="6705a-122">Https</span></span> 
- <span data-ttu-id="6705a-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="6705a-123">StorageQueue</span></span> 
- <span data-ttu-id="6705a-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="6705a-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="6705a-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="6705a-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="6705a-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="6705a-126">-ExecutionCount</span></span>
<span data-ttu-id="6705a-127">Określa, ile razy zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6705a-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="6705a-128">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="6705a-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="6705a-129">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="6705a-129">-Frequency</span></span>
<span data-ttu-id="6705a-130">Określa maksymalną częstotliwość zadania.</span><span class="sxs-lookup"><span data-stu-id="6705a-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="6705a-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6705a-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6705a-132">Minutę</span><span class="sxs-lookup"><span data-stu-id="6705a-132">Minute</span></span> 
- <span data-ttu-id="6705a-133">Dobow</span><span class="sxs-lookup"><span data-stu-id="6705a-133">Hour</span></span> 
- <span data-ttu-id="6705a-134">Dniach</span><span class="sxs-lookup"><span data-stu-id="6705a-134">Day</span></span> 
- <span data-ttu-id="6705a-135">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="6705a-135">Week</span></span> 
- <span data-ttu-id="6705a-136">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="6705a-136">Month</span></span>

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

### <span data-ttu-id="6705a-137">-Nagłówki</span><span class="sxs-lookup"><span data-stu-id="6705a-137">-Headers</span></span>
<span data-ttu-id="6705a-138">Określa tabelę skrótów zawierającą nagłówki.</span><span class="sxs-lookup"><span data-stu-id="6705a-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6705a-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="6705a-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="6705a-140">Określa typ uwierzytelniania HTTP.</span><span class="sxs-lookup"><span data-stu-id="6705a-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="6705a-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6705a-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6705a-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6705a-142">None</span></span> 
- <span data-ttu-id="6705a-143">Kolekcja</span><span class="sxs-lookup"><span data-stu-id="6705a-143">ClientCertificate</span></span> 
- <span data-ttu-id="6705a-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="6705a-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="6705a-145">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="6705a-145">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6705a-146">-Interval</span><span class="sxs-lookup"><span data-stu-id="6705a-146">-Interval</span></span>
<span data-ttu-id="6705a-147">Określa interwał cyklu zadania.</span><span class="sxs-lookup"><span data-stu-id="6705a-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="6705a-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="6705a-148">-JobCollectionName</span></span>
<span data-ttu-id="6705a-149">Określa nazwę kolekcji zadań, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="6705a-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="6705a-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="6705a-150">-JobName</span></span>
<span data-ttu-id="6705a-151">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="6705a-151">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="6705a-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="6705a-152">-JobState</span></span>
<span data-ttu-id="6705a-153">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="6705a-153">Specifies the state of the job.</span></span>
<span data-ttu-id="6705a-154">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6705a-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6705a-155">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="6705a-155">Enabled</span></span> 
- <span data-ttu-id="6705a-156">Łącza</span><span class="sxs-lookup"><span data-stu-id="6705a-156">Disabled</span></span>

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

### <span data-ttu-id="6705a-157">-Method</span><span class="sxs-lookup"><span data-stu-id="6705a-157">-Method</span></span>
<span data-ttu-id="6705a-158">Określa metodę dla typów akcji dla zadania.</span><span class="sxs-lookup"><span data-stu-id="6705a-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="6705a-159">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6705a-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6705a-160">Pobierz</span><span class="sxs-lookup"><span data-stu-id="6705a-160">GET</span></span> 
- <span data-ttu-id="6705a-161">WPROWADZENIA</span><span class="sxs-lookup"><span data-stu-id="6705a-161">PUT</span></span> 
- <span data-ttu-id="6705a-162">WYSYŁK</span><span class="sxs-lookup"><span data-stu-id="6705a-162">POST</span></span> 
- <span data-ttu-id="6705a-163">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="6705a-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6705a-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="6705a-164">-RequestBody</span></span>
<span data-ttu-id="6705a-165">Określa wartość treści dla akcji PUT i KSIĘGUJ zadania.</span><span class="sxs-lookup"><span data-stu-id="6705a-165">Specifies the value of the body for PUT and POST job actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6705a-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6705a-166">-ResourceGroupName</span></span>
<span data-ttu-id="6705a-167">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="6705a-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="6705a-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6705a-168">-StartTime</span></span>
<span data-ttu-id="6705a-169">Określa czas rozpoczęcia, jako obiekt **DateTime** , dla zadania.</span><span class="sxs-lookup"><span data-stu-id="6705a-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="6705a-170">-URI</span><span class="sxs-lookup"><span data-stu-id="6705a-170">-Uri</span></span>
<span data-ttu-id="6705a-171">Określa identyfikator URI dla akcji zadania.</span><span class="sxs-lookup"><span data-stu-id="6705a-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6705a-172">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6705a-172">-Confirm</span></span>
<span data-ttu-id="6705a-173">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6705a-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6705a-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6705a-174">-WhatIf</span></span>
<span data-ttu-id="6705a-175">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6705a-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6705a-176">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6705a-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6705a-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6705a-177">CommonParameters</span></span>
<span data-ttu-id="6705a-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6705a-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6705a-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6705a-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6705a-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6705a-180">INPUTS</span></span>

### <span data-ttu-id="6705a-181">System. String</span><span class="sxs-lookup"><span data-stu-id="6705a-181">System.String</span></span>

### <span data-ttu-id="6705a-182">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6705a-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6705a-183">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6705a-183">OUTPUTS</span></span>

### <span data-ttu-id="6705a-184">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6705a-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="6705a-185">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6705a-185">NOTES</span></span>

## <span data-ttu-id="6705a-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6705a-186">RELATED LINKS</span></span>

[<span data-ttu-id="6705a-187">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6705a-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6705a-188">Nowe — AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="6705a-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="6705a-189">Nowe — AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="6705a-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="6705a-190">Nowe — AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="6705a-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="6705a-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="6705a-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="6705a-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6705a-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6705a-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="6705a-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="6705a-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="6705a-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="6705a-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="6705a-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


