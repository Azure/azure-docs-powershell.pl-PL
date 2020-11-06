---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: a3fdbb3732def98bbf885cb58bf6f00dcb61eb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526605"
---
# <span data-ttu-id="3a99b-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="3a99b-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="3a99b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a99b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a99b-103">Tworzy zadanie HTTP.</span><span class="sxs-lookup"><span data-stu-id="3a99b-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a99b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a99b-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a99b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a99b-105">DESCRIPTION</span></span>
<span data-ttu-id="3a99b-106">Polecenie cmdlet **New-AzureRmSchedulerHttpJob** tworzy zadanie http w usłudze Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="3a99b-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="3a99b-107">To polecenie cmdlet obsługuje parametry dynamiczne na podstawie parametrów *ErrorActionType* i *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="3a99b-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="3a99b-108">Parametry dynamiczne są dostępne na podstawie innych wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="3a99b-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="3a99b-109">Aby wykryć nazwy parametrów dynamicznych po określeniu innych parametrów, wpisz łącznik (-), a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="3a99b-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3a99b-110">W przypadku pominięcia wymaganego parametru polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="3a99b-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3a99b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a99b-111">EXAMPLES</span></span>

## <span data-ttu-id="3a99b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a99b-112">PARAMETERS</span></span>

### <span data-ttu-id="3a99b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a99b-113">-DefaultProfile</span></span>
<span data-ttu-id="3a99b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a99b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a99b-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3a99b-115">-EndTime</span></span>
<span data-ttu-id="3a99b-116">Określa godzinę zakończenia dla zadania jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="3a99b-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="3a99b-117">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="3a99b-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="3a99b-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="3a99b-118">-ErrorActionType</span></span>
<span data-ttu-id="3a99b-119">Określa ustawienie akcji błędu dla zadania.</span><span class="sxs-lookup"><span data-stu-id="3a99b-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="3a99b-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3a99b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a99b-121">URL</span><span class="sxs-lookup"><span data-stu-id="3a99b-121">Http</span></span> 
- <span data-ttu-id="3a99b-122">Https</span><span class="sxs-lookup"><span data-stu-id="3a99b-122">Https</span></span> 
- <span data-ttu-id="3a99b-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="3a99b-123">StorageQueue</span></span> 
- <span data-ttu-id="3a99b-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="3a99b-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="3a99b-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="3a99b-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="3a99b-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="3a99b-126">-ExecutionCount</span></span>
<span data-ttu-id="3a99b-127">Określa, ile razy zadanie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a99b-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="3a99b-128">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="3a99b-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="3a99b-129">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="3a99b-129">-Frequency</span></span>
<span data-ttu-id="3a99b-130">Określa maksymalną częstotliwość zadania.</span><span class="sxs-lookup"><span data-stu-id="3a99b-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="3a99b-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3a99b-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a99b-132">Minutę</span><span class="sxs-lookup"><span data-stu-id="3a99b-132">Minute</span></span> 
- <span data-ttu-id="3a99b-133">Dobow</span><span class="sxs-lookup"><span data-stu-id="3a99b-133">Hour</span></span> 
- <span data-ttu-id="3a99b-134">Dniach</span><span class="sxs-lookup"><span data-stu-id="3a99b-134">Day</span></span> 
- <span data-ttu-id="3a99b-135">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="3a99b-135">Week</span></span> 
- <span data-ttu-id="3a99b-136">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="3a99b-136">Month</span></span>

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

### <span data-ttu-id="3a99b-137">-Nagłówki</span><span class="sxs-lookup"><span data-stu-id="3a99b-137">-Headers</span></span>
<span data-ttu-id="3a99b-138">Określa tabelę skrótów zawierającą nagłówki.</span><span class="sxs-lookup"><span data-stu-id="3a99b-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a99b-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="3a99b-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="3a99b-140">Określa typ uwierzytelniania HTTP.</span><span class="sxs-lookup"><span data-stu-id="3a99b-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="3a99b-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3a99b-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a99b-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3a99b-142">None</span></span> 
- <span data-ttu-id="3a99b-143">Kolekcja</span><span class="sxs-lookup"><span data-stu-id="3a99b-143">ClientCertificate</span></span> 
- <span data-ttu-id="3a99b-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="3a99b-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="3a99b-145">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="3a99b-145">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a99b-146">-Interval</span><span class="sxs-lookup"><span data-stu-id="3a99b-146">-Interval</span></span>
<span data-ttu-id="3a99b-147">Określa interwał cyklu zadania.</span><span class="sxs-lookup"><span data-stu-id="3a99b-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="3a99b-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3a99b-148">-JobCollectionName</span></span>
<span data-ttu-id="3a99b-149">Określa nazwę kolekcji zadań, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="3a99b-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="3a99b-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="3a99b-150">-JobName</span></span>
<span data-ttu-id="3a99b-151">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="3a99b-151">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="3a99b-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="3a99b-152">-JobState</span></span>
<span data-ttu-id="3a99b-153">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="3a99b-153">Specifies the state of the job.</span></span>
<span data-ttu-id="3a99b-154">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3a99b-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a99b-155">Wyłączona</span><span class="sxs-lookup"><span data-stu-id="3a99b-155">Enabled</span></span> 
- <span data-ttu-id="3a99b-156">Łącza</span><span class="sxs-lookup"><span data-stu-id="3a99b-156">Disabled</span></span>

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

### <span data-ttu-id="3a99b-157">-Method</span><span class="sxs-lookup"><span data-stu-id="3a99b-157">-Method</span></span>
<span data-ttu-id="3a99b-158">Określa metodę dla typów akcji dla zadania.</span><span class="sxs-lookup"><span data-stu-id="3a99b-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="3a99b-159">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3a99b-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a99b-160">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3a99b-160">GET</span></span> 
- <span data-ttu-id="3a99b-161">WPROWADZENIA</span><span class="sxs-lookup"><span data-stu-id="3a99b-161">PUT</span></span> 
- <span data-ttu-id="3a99b-162">WYSYŁK</span><span class="sxs-lookup"><span data-stu-id="3a99b-162">POST</span></span> 
- <span data-ttu-id="3a99b-163">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="3a99b-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a99b-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="3a99b-164">-RequestBody</span></span>
<span data-ttu-id="3a99b-165">Określa wartość treści dla akcji PUT i KSIĘGUJ zadania.</span><span class="sxs-lookup"><span data-stu-id="3a99b-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="3a99b-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a99b-166">-ResourceGroupName</span></span>
<span data-ttu-id="3a99b-167">Określa grupę zasobów, do której należy zadanie.</span><span class="sxs-lookup"><span data-stu-id="3a99b-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="3a99b-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3a99b-168">-StartTime</span></span>
<span data-ttu-id="3a99b-169">Określa czas rozpoczęcia, jako obiekt **DateTime** , dla zadania.</span><span class="sxs-lookup"><span data-stu-id="3a99b-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="3a99b-170">-URI</span><span class="sxs-lookup"><span data-stu-id="3a99b-170">-Uri</span></span>
<span data-ttu-id="3a99b-171">Określa identyfikator URI dla akcji zadania.</span><span class="sxs-lookup"><span data-stu-id="3a99b-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a99b-172">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a99b-172">-Confirm</span></span>
<span data-ttu-id="3a99b-173">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a99b-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a99b-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a99b-174">-WhatIf</span></span>
<span data-ttu-id="3a99b-175">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a99b-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a99b-176">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a99b-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a99b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a99b-177">CommonParameters</span></span>
<span data-ttu-id="3a99b-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a99b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a99b-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a99b-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a99b-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a99b-180">INPUTS</span></span>

### <span data-ttu-id="3a99b-181">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3a99b-181">None</span></span>
<span data-ttu-id="3a99b-182">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3a99b-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a99b-183">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a99b-183">OUTPUTS</span></span>

### <span data-ttu-id="3a99b-184">Microsoft. Azure. Commands. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3a99b-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="3a99b-185">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a99b-185">NOTES</span></span>

## <span data-ttu-id="3a99b-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a99b-186">RELATED LINKS</span></span>

[<span data-ttu-id="3a99b-187">Nowe — AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3a99b-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="3a99b-188">Nowe — AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="3a99b-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="3a99b-189">Nowe — AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="3a99b-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="3a99b-190">Nowe — AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="3a99b-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="3a99b-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="3a99b-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="3a99b-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3a99b-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="3a99b-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="3a99b-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="3a99b-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="3a99b-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="3a99b-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="3a99b-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


