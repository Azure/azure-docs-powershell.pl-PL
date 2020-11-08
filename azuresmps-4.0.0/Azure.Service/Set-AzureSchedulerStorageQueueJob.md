---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055016"
---
# <span data-ttu-id="ce31c-101">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ce31c-101">Set-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="ce31c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce31c-102">SYNOPSIS</span></span>
<span data-ttu-id="ce31c-103">Umożliwia zaktualizowanie zadania harmonogramu, które zawiera akcję magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-103">Updates a scheduler job that has a storage action.</span></span>

## <span data-ttu-id="ce31c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce31c-104">SYNTAX</span></span>

### <span data-ttu-id="ce31c-105">Wymagane</span><span class="sxs-lookup"><span data-stu-id="ce31c-105">Required</span></span>
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ce31c-106">Cykliczne</span><span class="sxs-lookup"><span data-stu-id="ce31c-106">Recurring</span></span>
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ce31c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ce31c-107">DESCRIPTION</span></span>
<span data-ttu-id="ce31c-108">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce31c-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ce31c-109">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ce31c-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ce31c-110">Polecenie cmdlet **Set-AzureSchedulerStorageQueueJob** aktualizuje zadanie harmonogramu z akcją magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ce31c-110">The **Set-AzureSchedulerStorageQueueJob** cmdlet updates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="ce31c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce31c-111">EXAMPLES</span></span>

### <span data-ttu-id="ce31c-112">Przykład 1: aktualizowanie wiadomości w kolejce magazynu</span><span class="sxs-lookup"><span data-stu-id="ce31c-112">Example 1: Update a Storage queue message</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

<span data-ttu-id="ce31c-113">To polecenie aktualizuje komunikat kolejki dla zadania przechowywania o nazwie Job12.</span><span class="sxs-lookup"><span data-stu-id="ce31c-113">This command updates the queue message for the Storage job named Job12.</span></span>
<span data-ttu-id="ce31c-114">Polecenie określa nazwę kolekcji zadań i lokalizację.</span><span class="sxs-lookup"><span data-stu-id="ce31c-114">The command specifies the job collection name and the location.</span></span>

### <span data-ttu-id="ce31c-115">Przykład 2: Włączanie zadania w kolejce magazynu</span><span class="sxs-lookup"><span data-stu-id="ce31c-115">Example 2: Enable a Storage queue job</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

<span data-ttu-id="ce31c-116">To polecenie włącza zadanie o nazwie Job16.</span><span class="sxs-lookup"><span data-stu-id="ce31c-116">This command enables the job named Job16.</span></span>
<span data-ttu-id="ce31c-117">Polecenie zmieni stan zadania na włączone przez określenie wartości parametru *JobState* .</span><span class="sxs-lookup"><span data-stu-id="ce31c-117">The command changes the state of the job to Enabled by specifying that value for the *JobState* parameter.</span></span>

## <span data-ttu-id="ce31c-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce31c-118">PARAMETERS</span></span>

### <span data-ttu-id="ce31c-119">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ce31c-119">-EndTime</span></span>
<span data-ttu-id="ce31c-120">Określa godzinę jako obiekt **DateTime** , aby harmonogram przestał zainicjowania zadania.</span><span class="sxs-lookup"><span data-stu-id="ce31c-120">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="ce31c-121">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="ce31c-121">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="ce31c-122">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ce31c-122">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="ce31c-123">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="ce31c-123">-ErrorActionHeaders</span></span>
<span data-ttu-id="ce31c-124">Określa nagłówki jako tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="ce31c-124">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="ce31c-125">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="ce31c-125">-ErrorActionMethod</span></span>
<span data-ttu-id="ce31c-126">Określa metodę dla typów akcji HTTP i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ce31c-126">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="ce31c-127">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ce31c-127">Valid values are:</span></span> 

- <span data-ttu-id="ce31c-128">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ce31c-128">GET</span></span>
- <span data-ttu-id="ce31c-129">WPROWADZENIA</span><span class="sxs-lookup"><span data-stu-id="ce31c-129">PUT</span></span>
- <span data-ttu-id="ce31c-130">WYSYŁK</span><span class="sxs-lookup"><span data-stu-id="ce31c-130">POST</span></span>
- <span data-ttu-id="ce31c-131">OZNACZENIA</span><span class="sxs-lookup"><span data-stu-id="ce31c-131">HEAD</span></span>
- <span data-ttu-id="ce31c-132">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="ce31c-132">DELETE</span></span>

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

### <span data-ttu-id="ce31c-133">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="ce31c-133">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="ce31c-134">Określa treść akcji zadania magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-134">Specifies the body for Storage job actions.</span></span>

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

### <span data-ttu-id="ce31c-135">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="ce31c-135">-ErrorActionRequestBody</span></span>
<span data-ttu-id="ce31c-136">Określa treść dla akcji PUT i KSIĘGUJ zadania.</span><span class="sxs-lookup"><span data-stu-id="ce31c-136">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="ce31c-137">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="ce31c-137">-ErrorActionSASToken</span></span>
<span data-ttu-id="ce31c-138">Określa token (SAS) (Shared Access Signature) dla kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-138">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

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

### <span data-ttu-id="ce31c-139">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce31c-139">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="ce31c-140">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-140">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="ce31c-141">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ce31c-141">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="ce31c-142">Określa nazwę kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-142">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="ce31c-143">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="ce31c-143">-ErrorActionURI</span></span>
<span data-ttu-id="ce31c-144">Określa identyfikator URI dla akcji zadania błędu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-144">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="ce31c-145">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="ce31c-145">-ExecutionCount</span></span>
<span data-ttu-id="ce31c-146">Określa liczbę wystąpień uruchomionego zadania.</span><span class="sxs-lookup"><span data-stu-id="ce31c-146">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="ce31c-147">Domyślnie zadanie powtarza się cyklicznie.</span><span class="sxs-lookup"><span data-stu-id="ce31c-147">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="ce31c-148">-Częstotliwość</span><span class="sxs-lookup"><span data-stu-id="ce31c-148">-Frequency</span></span>
<span data-ttu-id="ce31c-149">Określa maksymalną częstotliwość dla tego zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-149">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="ce31c-150">-Interval</span><span class="sxs-lookup"><span data-stu-id="ce31c-150">-Interval</span></span>
<span data-ttu-id="ce31c-151">Określa interwał cyklu z częstotliwością określoną przy użyciu parametru *częstotliwości* .</span><span class="sxs-lookup"><span data-stu-id="ce31c-151">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="ce31c-152">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ce31c-152">-JobCollectionName</span></span>
<span data-ttu-id="ce31c-153">Określa nazwę kolekcji, która ma zawierać zadanie harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-153">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="ce31c-154">-JobName</span><span class="sxs-lookup"><span data-stu-id="ce31c-154">-JobName</span></span>
<span data-ttu-id="ce31c-155">Określa nazwę zadania harmonogramu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="ce31c-155">Specifies the name of the scheduler job to update.</span></span>

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

### <span data-ttu-id="ce31c-156">-JobState</span><span class="sxs-lookup"><span data-stu-id="ce31c-156">-JobState</span></span>
<span data-ttu-id="ce31c-157">Określa stan zadania harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-157">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="ce31c-158">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ce31c-158">-Location</span></span>
<span data-ttu-id="ce31c-159">Określa nazwę lokalizacji, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="ce31c-159">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="ce31c-160">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ce31c-160">Valid values are:</span></span> 

- <span data-ttu-id="ce31c-161">W dowolnym miejscu w Azji</span><span class="sxs-lookup"><span data-stu-id="ce31c-161">Anywhere Asia</span></span>
- <span data-ttu-id="ce31c-162">Dowolne miejsce w Europie</span><span class="sxs-lookup"><span data-stu-id="ce31c-162">Anywhere Europe</span></span>
- <span data-ttu-id="ce31c-163">Dowolne miejsce w USA</span><span class="sxs-lookup"><span data-stu-id="ce31c-163">Anywhere US</span></span>
- <span data-ttu-id="ce31c-164">Azja Wschodnia</span><span class="sxs-lookup"><span data-stu-id="ce31c-164">East Asia</span></span>
- <span data-ttu-id="ce31c-165">Wschodnie USA</span><span class="sxs-lookup"><span data-stu-id="ce31c-165">East US</span></span>
- <span data-ttu-id="ce31c-166">Północno-środkowe USA</span><span class="sxs-lookup"><span data-stu-id="ce31c-166">North Central US</span></span>
- <span data-ttu-id="ce31c-167">Europa Północna</span><span class="sxs-lookup"><span data-stu-id="ce31c-167">North Europe</span></span>
- <span data-ttu-id="ce31c-168">Południowa Centrala amerykańska</span><span class="sxs-lookup"><span data-stu-id="ce31c-168">South Central US</span></span>
- <span data-ttu-id="ce31c-169">Azja Południowo-Wschodnia</span><span class="sxs-lookup"><span data-stu-id="ce31c-169">Southeast Asia</span></span>
- <span data-ttu-id="ce31c-170">Europa Zachodnia</span><span class="sxs-lookup"><span data-stu-id="ce31c-170">West Europe</span></span>
- <span data-ttu-id="ce31c-171">Zachodnie USA</span><span class="sxs-lookup"><span data-stu-id="ce31c-171">West US</span></span>

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

### <span data-ttu-id="ce31c-172">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce31c-172">-PassThru</span></span>
<span data-ttu-id="ce31c-173">Wskazuje, że to polecenie cmdlet zwraca obiekt reprezentujący element, na którym działa.</span><span class="sxs-lookup"><span data-stu-id="ce31c-173">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="ce31c-174">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ce31c-174">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce31c-175">-Profile</span><span class="sxs-lookup"><span data-stu-id="ce31c-175">-Profile</span></span>
<span data-ttu-id="ce31c-176">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce31c-176">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce31c-177">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ce31c-177">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce31c-178">-SASToken</span><span class="sxs-lookup"><span data-stu-id="ce31c-178">-SASToken</span></span>
<span data-ttu-id="ce31c-179">Określa token SAS dla kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-179">Specifies the SAS token for the Storage queue.</span></span>

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

### <span data-ttu-id="ce31c-180">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ce31c-180">-StartTime</span></span>
<span data-ttu-id="ce31c-181">Określa godzinę, jako obiekt **DateTime** , w celu rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="ce31c-181">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="ce31c-182">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="ce31c-182">-StorageQueueAccount</span></span>
<span data-ttu-id="ce31c-183">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-183">Specifies the Storage account name.</span></span>

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

### <span data-ttu-id="ce31c-184">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="ce31c-184">-StorageQueueMessage</span></span>
<span data-ttu-id="ce31c-185">Określa komunikat kolejki dla zadania magazynowania.</span><span class="sxs-lookup"><span data-stu-id="ce31c-185">Specifies the queue message for the Storage job.</span></span>

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

### <span data-ttu-id="ce31c-186">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="ce31c-186">-StorageQueueName</span></span>
<span data-ttu-id="ce31c-187">Określa nazwę kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="ce31c-187">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="ce31c-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce31c-188">CommonParameters</span></span>
<span data-ttu-id="ce31c-189">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce31c-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce31c-190">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce31c-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce31c-191">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce31c-191">INPUTS</span></span>

## <span data-ttu-id="ce31c-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce31c-192">OUTPUTS</span></span>

## <span data-ttu-id="ce31c-193">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce31c-193">NOTES</span></span>

## <span data-ttu-id="ce31c-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce31c-194">RELATED LINKS</span></span>

[<span data-ttu-id="ce31c-195">Nowe — AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ce31c-195">New-AzureSchedulerStorageQueueJob</span></span>](./New-AzureSchedulerStorageQueueJob.md)


