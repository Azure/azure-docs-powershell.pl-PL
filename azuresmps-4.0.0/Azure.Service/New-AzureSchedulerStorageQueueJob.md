---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054868"
---
# <span data-ttu-id="c5886-101">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c5886-101">New-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="c5886-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5886-102">SYNOPSIS</span></span>
<span data-ttu-id="c5886-103">Tworzy zadanie harmonogramu zawierające akcję magazynu.</span><span class="sxs-lookup"><span data-stu-id="c5886-103">Creates a scheduler job that has a Storage action.</span></span>

## <span data-ttu-id="c5886-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5886-104">SYNTAX</span></span>

### <span data-ttu-id="c5886-105">Wymagane</span><span class="sxs-lookup"><span data-stu-id="c5886-105">Required</span></span>
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c5886-106">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="c5886-106">Recurring</span></span>
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c5886-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c5886-107">DESCRIPTION</span></span>
<span data-ttu-id="c5886-108">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c5886-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c5886-109">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c5886-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c5886-110">Polecenie cmdlet **New-AzureSchedulerStorageQueueJob** tworzy zadanie harmonogramu z akcją usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c5886-110">The **New-AzureSchedulerStorageQueueJob** cmdlet creates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="c5886-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5886-111">EXAMPLES</span></span>

### <span data-ttu-id="c5886-112">Przykład 1. Tworzenie zadania przechowywania, które jest uruchamiane raz</span><span class="sxs-lookup"><span data-stu-id="c5886-112">Example 1: Create a Storage job that runs once</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

<span data-ttu-id="c5886-113">To polecenie tworzy zadanie przechowywania harmonogramu jako część kolekcji o nazwie JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="c5886-113">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="c5886-114">To polecenie Określa konto magazynu, nazwę kolejki i token SAS.</span><span class="sxs-lookup"><span data-stu-id="c5886-114">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="c5886-115">Zadanie jest uruchamiane raz natychmiast.</span><span class="sxs-lookup"><span data-stu-id="c5886-115">The job runs once, immediately.</span></span>

### <span data-ttu-id="c5886-116">Przykład 2: Tworzenie zadania magazynowania, które jest uruchamiane określoną liczbą razy</span><span class="sxs-lookup"><span data-stu-id="c5886-116">Example 2: Create a Storage job that runs a specified number of times</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

<span data-ttu-id="c5886-117">To polecenie tworzy zadanie przechowywania harmonogramu jako część kolekcji o nazwie JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="c5886-117">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="c5886-118">To polecenie Określa konto magazynu, nazwę kolejki i token SAS.</span><span class="sxs-lookup"><span data-stu-id="c5886-118">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="c5886-119">Zadanie jest wykonywane w sumie 20 razy, dwa razy w ciągu godziny.</span><span class="sxs-lookup"><span data-stu-id="c5886-119">The job runs 20 times in total, twice every hour.</span></span>

## <span data-ttu-id="c5886-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5886-120">PARAMETERS</span></span>

### <span data-ttu-id="c5886-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c5886-121">-EndTime</span></span>
<span data-ttu-id="c5886-122">Określa godzinę jako obiekt **DateTime** , aby harmonogram przestał zainicjowania zadania.</span><span class="sxs-lookup"><span data-stu-id="c5886-122">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="c5886-123">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="c5886-123">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="c5886-124">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c5886-124">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="c5886-125">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="c5886-125">-ErrorActionHeaders</span></span>
<span data-ttu-id="c5886-126">Określa nagłówki jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="c5886-126">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="c5886-127">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="c5886-127">-ErrorActionMethod</span></span>
<span data-ttu-id="c5886-128">Określa metodę dla typów akcji HTTP i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c5886-128">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="c5886-129">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="c5886-129">Valid values are:</span></span> 

- <span data-ttu-id="c5886-130">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c5886-130">GET</span></span>
- <span data-ttu-id="c5886-131">WPROWADZENIA</span><span class="sxs-lookup"><span data-stu-id="c5886-131">PUT</span></span>
- <span data-ttu-id="c5886-132">WYSYŁK</span><span class="sxs-lookup"><span data-stu-id="c5886-132">POST</span></span>
- <span data-ttu-id="c5886-133">OZNACZENIA</span><span class="sxs-lookup"><span data-stu-id="c5886-133">HEAD</span></span>
- <span data-ttu-id="c5886-134">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="c5886-134">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-135">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="c5886-135">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="c5886-136">Określa treść akcji zadania magazynu.</span><span class="sxs-lookup"><span data-stu-id="c5886-136">Specifies the body for Storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-137">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="c5886-137">-ErrorActionRequestBody</span></span>
<span data-ttu-id="c5886-138">Określa treść dla akcji PUT i KSIĘGUJ zadania.</span><span class="sxs-lookup"><span data-stu-id="c5886-138">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-139">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="c5886-139">-ErrorActionSASToken</span></span>
<span data-ttu-id="c5886-140">Określa token (SAS) (Shared Access Signature) dla kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="c5886-140">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-141">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c5886-141">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="c5886-142">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c5886-142">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-143">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c5886-143">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="c5886-144">Określa nazwę kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="c5886-144">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-145">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="c5886-145">-ErrorActionURI</span></span>
<span data-ttu-id="c5886-146">Określa identyfikator URI dla akcji zadania błędu.</span><span class="sxs-lookup"><span data-stu-id="c5886-146">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-147">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="c5886-147">-ExecutionCount</span></span>
<span data-ttu-id="c5886-148">Określa liczbę wystąpień uruchomionego zadania.</span><span class="sxs-lookup"><span data-stu-id="c5886-148">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="c5886-149">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="c5886-149">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="c5886-150">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="c5886-150">-Frequency</span></span>
<span data-ttu-id="c5886-151">Określa maksymalną częstotliwość dla tego zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="c5886-151">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="c5886-152">-Interval</span><span class="sxs-lookup"><span data-stu-id="c5886-152">-Interval</span></span>
<span data-ttu-id="c5886-153">Określa interwał cyklu z częstotliwością określoną przy użyciu parametru *częstotliwości* .</span><span class="sxs-lookup"><span data-stu-id="c5886-153">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="c5886-154">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c5886-154">-JobCollectionName</span></span>
<span data-ttu-id="c5886-155">Określa nazwę kolekcji, która ma zawierać zadanie harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="c5886-155">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-156">-JobName</span><span class="sxs-lookup"><span data-stu-id="c5886-156">-JobName</span></span>
<span data-ttu-id="c5886-157">Określa nazwę zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="c5886-157">Specifies the name for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-158">-JobState</span><span class="sxs-lookup"><span data-stu-id="c5886-158">-JobState</span></span>
<span data-ttu-id="c5886-159">Określa stan zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="c5886-159">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="c5886-160">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c5886-160">-Location</span></span>
<span data-ttu-id="c5886-161">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="c5886-161">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="c5886-162">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="c5886-162">Valid values are:</span></span> 

- <span data-ttu-id="c5886-163">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="c5886-163">Anywhere Asia</span></span>
- <span data-ttu-id="c5886-164">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="c5886-164">Anywhere Europe</span></span>
- <span data-ttu-id="c5886-165">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="c5886-165">Anywhere US</span></span>
- <span data-ttu-id="c5886-166">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="c5886-166">East Asia</span></span>
- <span data-ttu-id="c5886-167">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="c5886-167">East US</span></span>
- <span data-ttu-id="c5886-168">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="c5886-168">North Central US</span></span>
- <span data-ttu-id="c5886-169">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="c5886-169">North Europe</span></span>
- <span data-ttu-id="c5886-170">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="c5886-170">South Central US</span></span>
- <span data-ttu-id="c5886-171">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="c5886-171">Southeast Asia</span></span>
- <span data-ttu-id="c5886-172">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="c5886-172">West Europe</span></span>
- <span data-ttu-id="c5886-173">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="c5886-173">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-174">-Profile</span><span class="sxs-lookup"><span data-stu-id="c5886-174">-Profile</span></span>
<span data-ttu-id="c5886-175">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5886-175">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5886-176">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c5886-176">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-177">-SASToken</span><span class="sxs-lookup"><span data-stu-id="c5886-177">-SASToken</span></span>
<span data-ttu-id="c5886-178">Określa token SAS dla kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="c5886-178">Specifies the SAS token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-179">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c5886-179">-StartTime</span></span>
<span data-ttu-id="c5886-180">Określa godzinę, jako obiekt **DateTime** , w celu rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="c5886-180">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-181">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="c5886-181">-StorageQueueAccount</span></span>
<span data-ttu-id="c5886-182">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c5886-182">Specifies the Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-183">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="c5886-183">-StorageQueueMessage</span></span>
<span data-ttu-id="c5886-184">Określa komunikat kolejki dla zadania magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c5886-184">Specifies the queue message for Storage job.</span></span>

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

### <span data-ttu-id="c5886-185">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="c5886-185">-StorageQueueName</span></span>
<span data-ttu-id="c5886-186">Określa nazwę kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="c5886-186">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5886-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5886-187">CommonParameters</span></span>
<span data-ttu-id="c5886-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5886-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5886-189">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5886-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5886-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5886-190">INPUTS</span></span>

## <span data-ttu-id="c5886-191">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5886-191">OUTPUTS</span></span>

## <span data-ttu-id="c5886-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5886-192">NOTES</span></span>

## <span data-ttu-id="c5886-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5886-193">RELATED LINKS</span></span>

[<span data-ttu-id="c5886-194">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c5886-194">Set-AzureSchedulerStorageQueueJob</span></span>](./Set-AzureSchedulerStorageQueueJob.md)


