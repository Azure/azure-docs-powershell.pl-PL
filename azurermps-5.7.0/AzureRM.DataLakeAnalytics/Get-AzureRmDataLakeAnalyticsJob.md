---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525137"
---
# <span data-ttu-id="90b8b-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="90b8b-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="90b8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="90b8b-103">Pobiera zadanie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="90b8b-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90b8b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90b8b-104">SYNTAX</span></span>

### <span data-ttu-id="90b8b-105">GetAllInResourceGroupAndAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="90b8b-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90b8b-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="90b8b-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90b8b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="90b8b-107">DESCRIPTION</span></span>
<span data-ttu-id="90b8b-108">Polecenie cmdlet **Get-AzureRmDataLakeAnalyticsJob** pobiera zadanie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="90b8b-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="90b8b-109">Jeśli nie podano zadania, to polecenie cmdlet umożliwia pobieranie wszystkich zadań.</span><span class="sxs-lookup"><span data-stu-id="90b8b-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="90b8b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90b8b-110">EXAMPLES</span></span>

### <span data-ttu-id="90b8b-111">Przykład 1: pobieranie określonego zadania</span><span class="sxs-lookup"><span data-stu-id="90b8b-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="90b8b-112">To polecenie pobiera zadanie z określonym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="90b8b-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="90b8b-113">Przykład 2: pobieranie zadań przesłanych w ubiegłym tygodniu</span><span class="sxs-lookup"><span data-stu-id="90b8b-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="90b8b-114">To polecenie pobiera zadania przesłane w ubiegłym tygodniu.</span><span class="sxs-lookup"><span data-stu-id="90b8b-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="90b8b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90b8b-115">PARAMETERS</span></span>

### <span data-ttu-id="90b8b-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="90b8b-116">-Account</span></span>
<span data-ttu-id="90b8b-117">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="90b8b-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b8b-118">-DefaultProfile</span></span>
<span data-ttu-id="90b8b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="90b8b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90b8b-120">-Include</span><span class="sxs-lookup"><span data-stu-id="90b8b-120">-Include</span></span>
<span data-ttu-id="90b8b-121">Określa opcje wskazujące typ dodatkowych informacji do pobrania dla zadania.</span><span class="sxs-lookup"><span data-stu-id="90b8b-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="90b8b-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="90b8b-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90b8b-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="90b8b-123">None</span></span>
- <span data-ttu-id="90b8b-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="90b8b-124">DebugInfo</span></span>
- <span data-ttu-id="90b8b-125">Celów</span><span class="sxs-lookup"><span data-stu-id="90b8b-125">Statistics</span></span>
- <span data-ttu-id="90b8b-126">Cały</span><span class="sxs-lookup"><span data-stu-id="90b8b-126">All</span></span>

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="90b8b-127">-JobId</span></span>
<span data-ttu-id="90b8b-128">Określa identyfikator zadania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="90b8b-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90b8b-129">-Name</span></span>
<span data-ttu-id="90b8b-130">Określa nazwę, która ma być używana do filtrowania wyników listy zadań.</span><span class="sxs-lookup"><span data-stu-id="90b8b-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="90b8b-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="90b8b-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90b8b-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="90b8b-132">None</span></span>
- <span data-ttu-id="90b8b-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="90b8b-133">DebugInfo</span></span>
- <span data-ttu-id="90b8b-134">Celów</span><span class="sxs-lookup"><span data-stu-id="90b8b-134">Statistics</span></span>
- <span data-ttu-id="90b8b-135">Cały</span><span class="sxs-lookup"><span data-stu-id="90b8b-135">All</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="90b8b-136">-PipelineId</span></span>
<span data-ttu-id="90b8b-137">Identyfikator opcjonalny, który wskazuje tylko część zadań określonego potoku, należy zwrócić.</span><span class="sxs-lookup"><span data-stu-id="90b8b-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="90b8b-138">-RecurrenceId</span></span>
<span data-ttu-id="90b8b-139">Identyfikator opcjonalny, który wskazuje tylko część zadań określonego cyklu, należy zwrócić.</span><span class="sxs-lookup"><span data-stu-id="90b8b-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-140">— Wynik</span><span class="sxs-lookup"><span data-stu-id="90b8b-140">-Result</span></span>
<span data-ttu-id="90b8b-141">Określa filtr wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="90b8b-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="90b8b-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="90b8b-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90b8b-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="90b8b-143">None</span></span>
- <span data-ttu-id="90b8b-144">Anulowania</span><span class="sxs-lookup"><span data-stu-id="90b8b-144">Cancelled</span></span>
- <span data-ttu-id="90b8b-145">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="90b8b-145">Failed</span></span>
- <span data-ttu-id="90b8b-146">Doszło</span><span class="sxs-lookup"><span data-stu-id="90b8b-146">Succeeded</span></span>

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-147">-State</span><span class="sxs-lookup"><span data-stu-id="90b8b-147">-State</span></span>
<span data-ttu-id="90b8b-148">Określa filtr stanu dla wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="90b8b-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="90b8b-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="90b8b-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90b8b-150">Twierdzona</span><span class="sxs-lookup"><span data-stu-id="90b8b-150">Accepted</span></span>
- <span data-ttu-id="90b8b-151">Nowy</span><span class="sxs-lookup"><span data-stu-id="90b8b-151">New</span></span>
- <span data-ttu-id="90b8b-152">Kompilowania</span><span class="sxs-lookup"><span data-stu-id="90b8b-152">Compiling</span></span>
- <span data-ttu-id="90b8b-153">Nich</span><span class="sxs-lookup"><span data-stu-id="90b8b-153">Scheduling</span></span>
- <span data-ttu-id="90b8b-154">Oczekuje</span><span class="sxs-lookup"><span data-stu-id="90b8b-154">Queued</span></span>
- <span data-ttu-id="90b8b-155">Czynając</span><span class="sxs-lookup"><span data-stu-id="90b8b-155">Starting</span></span>
- <span data-ttu-id="90b8b-156">Wstrzymana</span><span class="sxs-lookup"><span data-stu-id="90b8b-156">Paused</span></span>
- <span data-ttu-id="90b8b-157">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="90b8b-157">Running</span></span>
- <span data-ttu-id="90b8b-158">Zakończona</span><span class="sxs-lookup"><span data-stu-id="90b8b-158">Ended</span></span>

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="90b8b-159">-SubmittedAfter</span></span>
<span data-ttu-id="90b8b-160">Określa filtr daty.</span><span class="sxs-lookup"><span data-stu-id="90b8b-160">Specifies a date filter.</span></span>
<span data-ttu-id="90b8b-161">Ten parametr służy do filtrowania wyników listy zadań na zadania przesłane po określonej dacie.</span><span class="sxs-lookup"><span data-stu-id="90b8b-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="90b8b-162">-SubmittedBefore</span></span>
<span data-ttu-id="90b8b-163">Określa filtr daty.</span><span class="sxs-lookup"><span data-stu-id="90b8b-163">Specifies a date filter.</span></span>
<span data-ttu-id="90b8b-164">Ten parametr służy do filtrowania wyników listy zadań na zadania przesłane przed określoną datą.</span><span class="sxs-lookup"><span data-stu-id="90b8b-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-165">-Osoba przesyłająca</span><span class="sxs-lookup"><span data-stu-id="90b8b-165">-Submitter</span></span>
<span data-ttu-id="90b8b-166">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="90b8b-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="90b8b-167">Ten parametr służy do filtrowania wyników listy zadań na zadania przesłane przez określonego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="90b8b-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-168">-Początek</span><span class="sxs-lookup"><span data-stu-id="90b8b-168">-Top</span></span>
<span data-ttu-id="90b8b-169">Wartość opcjonalna wskazująca liczbę zadań do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="90b8b-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="90b8b-170">Wartość domyślna to 500</span><span class="sxs-lookup"><span data-stu-id="90b8b-170">Default value is 500</span></span>

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b8b-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b8b-171">CommonParameters</span></span>
<span data-ttu-id="90b8b-172">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b8b-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b8b-173">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b8b-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b8b-174">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90b8b-174">INPUTS</span></span>

### <span data-ttu-id="90b8b-175">Wiodąc</span><span class="sxs-lookup"><span data-stu-id="90b8b-175">Guid</span></span>
<span data-ttu-id="90b8b-176">Parametr "JobId" akceptuje wartość typu "GUID" z procesu</span><span class="sxs-lookup"><span data-stu-id="90b8b-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="90b8b-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90b8b-177">OUTPUTS</span></span>

### <span data-ttu-id="90b8b-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="90b8b-178">JobInformation</span></span>
<span data-ttu-id="90b8b-179">Szczegółowe informacje o określonym zadaniu</span><span class="sxs-lookup"><span data-stu-id="90b8b-179">The specified job information details</span></span>

### <span data-ttu-id="90b8b-180">Lista<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="90b8b-180">List<PSJobInformationBasic></span></span>
<span data-ttu-id="90b8b-181">Lista zadań na określonym koncie usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="90b8b-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="90b8b-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90b8b-182">NOTES</span></span>

## <span data-ttu-id="90b8b-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90b8b-183">RELATED LINKS</span></span>

[<span data-ttu-id="90b8b-184">Zatrzymaj — AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="90b8b-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="90b8b-185">Prześlij — AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="90b8b-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="90b8b-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="90b8b-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


