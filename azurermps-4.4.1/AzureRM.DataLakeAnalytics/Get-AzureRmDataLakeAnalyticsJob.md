---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553932"
---
# <span data-ttu-id="d9657-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d9657-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="d9657-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9657-102">SYNOPSIS</span></span>
<span data-ttu-id="d9657-103">Pobiera zadanie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d9657-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9657-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9657-104">SYNTAX</span></span>

### <span data-ttu-id="d9657-105">Cała grupa zasobów i konto (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d9657-105">All In Resource Group and Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9657-106">Konkretne JobInformation</span><span class="sxs-lookup"><span data-stu-id="d9657-106">Specific JobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9657-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d9657-107">DESCRIPTION</span></span>
<span data-ttu-id="d9657-108">Polecenie cmdlet **Get-AzureRmDataLakeAnalyticsJob** pobiera zadanie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d9657-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="d9657-109">Jeśli nie podano zadania, to polecenie cmdlet umożliwia pobieranie wszystkich zadań.</span><span class="sxs-lookup"><span data-stu-id="d9657-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="d9657-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9657-110">EXAMPLES</span></span>

### <span data-ttu-id="d9657-111">Przykład 1: pobieranie określonego zadania</span><span class="sxs-lookup"><span data-stu-id="d9657-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="d9657-112">To polecenie pobiera zadanie z określonym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="d9657-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="d9657-113">Przykład 2: pobieranie zadań przesłanych w ubiegłym tygodniu</span><span class="sxs-lookup"><span data-stu-id="d9657-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="d9657-114">To polecenie pobiera zadania przesłane w ubiegłym tygodniu.</span><span class="sxs-lookup"><span data-stu-id="d9657-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="d9657-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9657-115">PARAMETERS</span></span>

### <span data-ttu-id="d9657-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="d9657-116">-Account</span></span>
<span data-ttu-id="d9657-117">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d9657-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-118">-Include</span><span class="sxs-lookup"><span data-stu-id="d9657-118">-Include</span></span>
<span data-ttu-id="d9657-119">Określa opcje wskazujące typ dodatkowych informacji do pobrania dla zadania.</span><span class="sxs-lookup"><span data-stu-id="d9657-119">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="d9657-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d9657-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9657-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d9657-121">None</span></span>
- <span data-ttu-id="d9657-122">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="d9657-122">DebugInfo</span></span>
- <span data-ttu-id="d9657-123">Celów</span><span class="sxs-lookup"><span data-stu-id="d9657-123">Statistics</span></span>
- <span data-ttu-id="d9657-124">Cały</span><span class="sxs-lookup"><span data-stu-id="d9657-124">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="d9657-125">-JobId</span></span>
<span data-ttu-id="d9657-126">Określa identyfikator zadania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="d9657-126">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9657-127">-Name</span></span>
<span data-ttu-id="d9657-128">Określa nazwę, która ma być używana do filtrowania wyników listy zadań.</span><span class="sxs-lookup"><span data-stu-id="d9657-128">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="d9657-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d9657-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9657-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d9657-130">None</span></span>
- <span data-ttu-id="d9657-131">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="d9657-131">DebugInfo</span></span>
- <span data-ttu-id="d9657-132">Celów</span><span class="sxs-lookup"><span data-stu-id="d9657-132">Statistics</span></span>
- <span data-ttu-id="d9657-133">Cały</span><span class="sxs-lookup"><span data-stu-id="d9657-133">All</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-134">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="d9657-134">-PipelineId</span></span>
<span data-ttu-id="d9657-135">Identyfikator opcjonalny, który wskazuje tylko część zadań określonego potoku, należy zwrócić.</span><span class="sxs-lookup"><span data-stu-id="d9657-135">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-136">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="d9657-136">-RecurrenceId</span></span>
<span data-ttu-id="d9657-137">Identyfikator opcjonalny, który wskazuje tylko część zadań określonego cyklu, należy zwrócić.</span><span class="sxs-lookup"><span data-stu-id="d9657-137">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-138">— Wynik</span><span class="sxs-lookup"><span data-stu-id="d9657-138">-Result</span></span>
<span data-ttu-id="d9657-139">Określa filtr wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="d9657-139">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="d9657-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d9657-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9657-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d9657-141">None</span></span>
- <span data-ttu-id="d9657-142">Anulowania</span><span class="sxs-lookup"><span data-stu-id="d9657-142">Cancelled</span></span>
- <span data-ttu-id="d9657-143">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="d9657-143">Failed</span></span>
- <span data-ttu-id="d9657-144">Doszło</span><span class="sxs-lookup"><span data-stu-id="d9657-144">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-145">-State</span><span class="sxs-lookup"><span data-stu-id="d9657-145">-State</span></span>
<span data-ttu-id="d9657-146">Określa filtr stanu dla wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="d9657-146">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="d9657-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d9657-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9657-148">Twierdzona</span><span class="sxs-lookup"><span data-stu-id="d9657-148">Accepted</span></span>
- <span data-ttu-id="d9657-149">Nowy</span><span class="sxs-lookup"><span data-stu-id="d9657-149">New</span></span>
- <span data-ttu-id="d9657-150">Kompilowania</span><span class="sxs-lookup"><span data-stu-id="d9657-150">Compiling</span></span>
- <span data-ttu-id="d9657-151">Nich</span><span class="sxs-lookup"><span data-stu-id="d9657-151">Scheduling</span></span>
- <span data-ttu-id="d9657-152">Oczekuje</span><span class="sxs-lookup"><span data-stu-id="d9657-152">Queued</span></span>
- <span data-ttu-id="d9657-153">Czynając</span><span class="sxs-lookup"><span data-stu-id="d9657-153">Starting</span></span>
- <span data-ttu-id="d9657-154">Wstrzymana</span><span class="sxs-lookup"><span data-stu-id="d9657-154">Paused</span></span>
- <span data-ttu-id="d9657-155">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="d9657-155">Running</span></span>
- <span data-ttu-id="d9657-156">Zakończona</span><span class="sxs-lookup"><span data-stu-id="d9657-156">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-157">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="d9657-157">-SubmittedAfter</span></span>
<span data-ttu-id="d9657-158">Określa filtr daty.</span><span class="sxs-lookup"><span data-stu-id="d9657-158">Specifies a date filter.</span></span>
<span data-ttu-id="d9657-159">Ten parametr służy do filtrowania wyników listy zadań na zadania przesłane po określonej dacie.</span><span class="sxs-lookup"><span data-stu-id="d9657-159">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-160">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="d9657-160">-SubmittedBefore</span></span>
<span data-ttu-id="d9657-161">Określa filtr daty.</span><span class="sxs-lookup"><span data-stu-id="d9657-161">Specifies a date filter.</span></span>
<span data-ttu-id="d9657-162">Ten parametr służy do filtrowania wyników listy zadań na zadania przesłane przed określoną datą.</span><span class="sxs-lookup"><span data-stu-id="d9657-162">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-163">-Osoba przesyłająca</span><span class="sxs-lookup"><span data-stu-id="d9657-163">-Submitter</span></span>
<span data-ttu-id="d9657-164">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d9657-164">Specifies the email address of a user.</span></span>
<span data-ttu-id="d9657-165">Ten parametr służy do filtrowania wyników listy zadań na zadania przesłane przez określonego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d9657-165">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-166">-Początek</span><span class="sxs-lookup"><span data-stu-id="d9657-166">-Top</span></span>
<span data-ttu-id="d9657-167">Wartość opcjonalna wskazująca liczbę zadań do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="d9657-167">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="d9657-168">Wartość domyślna to 500</span><span class="sxs-lookup"><span data-stu-id="d9657-168">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9657-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9657-169">-DefaultProfile</span></span>
<span data-ttu-id="d9657-170">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9657-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9657-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9657-171">CommonParameters</span></span>
<span data-ttu-id="d9657-172">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9657-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9657-173">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9657-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9657-174">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9657-174">INPUTS</span></span>

### <span data-ttu-id="d9657-175">Wiodąc</span><span class="sxs-lookup"><span data-stu-id="d9657-175">Guid</span></span>
<span data-ttu-id="d9657-176">Parametr "JobId" akceptuje wartość typu "GUID" z procesu</span><span class="sxs-lookup"><span data-stu-id="d9657-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="d9657-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9657-177">OUTPUTS</span></span>

### <span data-ttu-id="d9657-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="d9657-178">JobInformation</span></span>
<span data-ttu-id="d9657-179">Szczegółowe informacje o określonym zadaniu</span><span class="sxs-lookup"><span data-stu-id="d9657-179">The specified job information details</span></span>

### <span data-ttu-id="d9657-180">Lista<JobInformation></span><span class="sxs-lookup"><span data-stu-id="d9657-180">List<JobInformation></span></span>
<span data-ttu-id="d9657-181">Lista zadań na określonym koncie usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d9657-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="d9657-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9657-182">NOTES</span></span>

## <span data-ttu-id="d9657-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9657-183">RELATED LINKS</span></span>

[<span data-ttu-id="d9657-184">Zatrzymaj — AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d9657-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="d9657-185">Prześlij — AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d9657-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="d9657-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d9657-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


