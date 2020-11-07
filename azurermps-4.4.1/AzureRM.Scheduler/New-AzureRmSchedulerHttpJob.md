---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 5fc591ff5d24211b8af464dab46bfb81360f83e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718095"
---
# <span data-ttu-id="70adc-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="70adc-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="70adc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70adc-102">SYNOPSIS</span></span>
<span data-ttu-id="70adc-103">Tworzy zadanie HTTP.</span><span class="sxs-lookup"><span data-stu-id="70adc-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70adc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70adc-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70adc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70adc-105">DESCRIPTION</span></span>
<span data-ttu-id="70adc-106">Polecenie cmdlet **New-AzureRmSchedulerHttpJob** tworzy zadanie http w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="70adc-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="70adc-107">To polecenie cmdlet obsługuje parametry dynamiczne na podstawie parametrów *ErrorActionType* i *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="70adc-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="70adc-108">Parametry dynamiczne są dostępne na podstawie innych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="70adc-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="70adc-109">Aby wykryć nazwy parametrów dynamicznych po określeniu innych parametrów, wpisz łącznik (-), a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="70adc-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="70adc-110">W przypadku pominięcia wymaganego parametru polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="70adc-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="70adc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70adc-111">EXAMPLES</span></span>

## <span data-ttu-id="70adc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70adc-112">PARAMETERS</span></span>

### <span data-ttu-id="70adc-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="70adc-113">-EndTime</span></span>
<span data-ttu-id="70adc-114">Określa godzinę zakończenia dla zadania jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="70adc-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="70adc-115">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="70adc-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="70adc-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="70adc-116">-ErrorActionType</span></span>
<span data-ttu-id="70adc-117">Określa ustawienie akcji błędu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="70adc-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="70adc-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="70adc-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70adc-119">URL</span><span class="sxs-lookup"><span data-stu-id="70adc-119">Http</span></span> 
- <span data-ttu-id="70adc-120">Https</span><span class="sxs-lookup"><span data-stu-id="70adc-120">Https</span></span> 
- <span data-ttu-id="70adc-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="70adc-121">StorageQueue</span></span> 
- <span data-ttu-id="70adc-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="70adc-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="70adc-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="70adc-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="70adc-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="70adc-124">-ExecutionCount</span></span>
<span data-ttu-id="70adc-125">Określa, ile razy zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70adc-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="70adc-126">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="70adc-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="70adc-127">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="70adc-127">-Frequency</span></span>
<span data-ttu-id="70adc-128">Określa maksymalną częstotliwość zadania.</span><span class="sxs-lookup"><span data-stu-id="70adc-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="70adc-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="70adc-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70adc-130">Minutę</span><span class="sxs-lookup"><span data-stu-id="70adc-130">Minute</span></span> 
- <span data-ttu-id="70adc-131">Dobow</span><span class="sxs-lookup"><span data-stu-id="70adc-131">Hour</span></span> 
- <span data-ttu-id="70adc-132">Dniach</span><span class="sxs-lookup"><span data-stu-id="70adc-132">Day</span></span> 
- <span data-ttu-id="70adc-133">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="70adc-133">Week</span></span> 
- <span data-ttu-id="70adc-134">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="70adc-134">Month</span></span>

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

### <span data-ttu-id="70adc-135">-Nagłówki</span><span class="sxs-lookup"><span data-stu-id="70adc-135">-Headers</span></span>
<span data-ttu-id="70adc-136">Określa tabelę skrótów zawierającą nagłówki.</span><span class="sxs-lookup"><span data-stu-id="70adc-136">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="70adc-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="70adc-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="70adc-138">Określa typ uwierzytelniania HTTP.</span><span class="sxs-lookup"><span data-stu-id="70adc-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="70adc-139">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="70adc-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70adc-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="70adc-140">None</span></span> 
- <span data-ttu-id="70adc-141">Kolekcja</span><span class="sxs-lookup"><span data-stu-id="70adc-141">ClientCertificate</span></span> 
- <span data-ttu-id="70adc-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="70adc-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="70adc-143">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="70adc-143">Basic</span></span>

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

### <span data-ttu-id="70adc-144">-Interval</span><span class="sxs-lookup"><span data-stu-id="70adc-144">-Interval</span></span>
<span data-ttu-id="70adc-145">Określa interwał cyklu zadania.</span><span class="sxs-lookup"><span data-stu-id="70adc-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="70adc-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="70adc-146">-JobCollectionName</span></span>
<span data-ttu-id="70adc-147">Określa nazwę kolekcji zadań, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="70adc-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="70adc-148">-JobName</span><span class="sxs-lookup"><span data-stu-id="70adc-148">-JobName</span></span>
<span data-ttu-id="70adc-149">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="70adc-149">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="70adc-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="70adc-150">-JobState</span></span>
<span data-ttu-id="70adc-151">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="70adc-151">Specifies the state of the job.</span></span>
<span data-ttu-id="70adc-152">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="70adc-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70adc-153">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="70adc-153">Enabled</span></span> 
- <span data-ttu-id="70adc-154">Łącza</span><span class="sxs-lookup"><span data-stu-id="70adc-154">Disabled</span></span>

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

### <span data-ttu-id="70adc-155">-Method</span><span class="sxs-lookup"><span data-stu-id="70adc-155">-Method</span></span>
<span data-ttu-id="70adc-156">Określa metodę dla typów akcji dla zadania.</span><span class="sxs-lookup"><span data-stu-id="70adc-156">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="70adc-157">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="70adc-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70adc-158">Pobierz</span><span class="sxs-lookup"><span data-stu-id="70adc-158">GET</span></span> 
- <span data-ttu-id="70adc-159">WPROWADZENIA</span><span class="sxs-lookup"><span data-stu-id="70adc-159">PUT</span></span> 
- <span data-ttu-id="70adc-160">WYSYŁK</span><span class="sxs-lookup"><span data-stu-id="70adc-160">POST</span></span> 
- <span data-ttu-id="70adc-161">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="70adc-161">DELETE</span></span>

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

### <span data-ttu-id="70adc-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="70adc-162">-RequestBody</span></span>
<span data-ttu-id="70adc-163">Określa wartość treści dla akcji PUT i KSIĘGUJ zadania.</span><span class="sxs-lookup"><span data-stu-id="70adc-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="70adc-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70adc-164">-ResourceGroupName</span></span>
<span data-ttu-id="70adc-165">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="70adc-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="70adc-166">-StartTime</span><span class="sxs-lookup"><span data-stu-id="70adc-166">-StartTime</span></span>
<span data-ttu-id="70adc-167">Określa czas rozpoczęcia, jako obiekt **DateTime** , dla zadania.</span><span class="sxs-lookup"><span data-stu-id="70adc-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="70adc-168">-URI</span><span class="sxs-lookup"><span data-stu-id="70adc-168">-Uri</span></span>
<span data-ttu-id="70adc-169">Określa identyfikator URI dla akcji zadania.</span><span class="sxs-lookup"><span data-stu-id="70adc-169">Specifies a URI for the job action.</span></span>

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

### <span data-ttu-id="70adc-170">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70adc-170">-Confirm</span></span>
<span data-ttu-id="70adc-171">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70adc-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70adc-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70adc-172">-WhatIf</span></span>
<span data-ttu-id="70adc-173">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70adc-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70adc-174">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70adc-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70adc-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70adc-175">-DefaultProfile</span></span>
<span data-ttu-id="70adc-176">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70adc-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70adc-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70adc-177">CommonParameters</span></span>
<span data-ttu-id="70adc-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70adc-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70adc-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70adc-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70adc-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70adc-180">INPUTS</span></span>

## <span data-ttu-id="70adc-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70adc-181">OUTPUTS</span></span>

### <span data-ttu-id="70adc-182">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="70adc-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="70adc-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70adc-183">NOTES</span></span>

## <span data-ttu-id="70adc-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70adc-184">RELATED LINKS</span></span>

[<span data-ttu-id="70adc-185">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="70adc-185">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="70adc-186">Nowe — AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="70adc-186">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="70adc-187">Nowe — AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="70adc-187">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="70adc-188">Nowe — AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="70adc-188">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="70adc-189">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="70adc-189">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="70adc-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="70adc-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="70adc-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="70adc-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="70adc-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="70adc-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="70adc-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="70adc-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


