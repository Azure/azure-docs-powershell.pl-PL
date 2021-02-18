---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180947"
---
# <span data-ttu-id="9de09-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9de09-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="9de09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9de09-102">SYNOPSIS</span></span>
<span data-ttu-id="9de09-103">Otrzymuje zadanie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9de09-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="9de09-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9de09-104">SYNTAX</span></span>

### <span data-ttu-id="9de09-105">GetAllInResourceGroupAndAccount (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9de09-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9de09-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="9de09-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9de09-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9de09-107">DESCRIPTION</span></span>
<span data-ttu-id="9de09-108">Polecenie **cmdlet Get-AzDataLakeAnalyticsJob** otrzymuje zadanie Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9de09-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="9de09-109">Jeśli nie określisz zadania, to polecenie cmdlet będzie pobierać wszystkie zadania.</span><span class="sxs-lookup"><span data-stu-id="9de09-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="9de09-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9de09-110">EXAMPLES</span></span>

### <span data-ttu-id="9de09-111">Przykład 1. Uzyskiwanie określonego zadania</span><span class="sxs-lookup"><span data-stu-id="9de09-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="9de09-112">To polecenie pobiera zadanie z określonym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="9de09-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="9de09-113">Przykład 2. Uzyskiwanie zadań przesłanych w ubiegłym tygodniu</span><span class="sxs-lookup"><span data-stu-id="9de09-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="9de09-114">To polecenie pobiera zadania przesłane w ubiegłym tygodniu.</span><span class="sxs-lookup"><span data-stu-id="9de09-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="9de09-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9de09-115">PARAMETERS</span></span>

### <span data-ttu-id="9de09-116">— Konto</span><span class="sxs-lookup"><span data-stu-id="9de09-116">-Account</span></span>
<span data-ttu-id="9de09-117">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9de09-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="9de09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de09-118">-DefaultProfile</span></span>
<span data-ttu-id="9de09-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9de09-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-120">— Uwzględnij</span><span class="sxs-lookup"><span data-stu-id="9de09-120">-Include</span></span>
<span data-ttu-id="9de09-121">Określa opcje wskazujące typ dodatkowych informacji o zadaniu.</span><span class="sxs-lookup"><span data-stu-id="9de09-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="9de09-122">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9de09-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9de09-123">Brak</span><span class="sxs-lookup"><span data-stu-id="9de09-123">None</span></span>
- <span data-ttu-id="9de09-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="9de09-124">DebugInfo</span></span>
- <span data-ttu-id="9de09-125">Statystyka</span><span class="sxs-lookup"><span data-stu-id="9de09-125">Statistics</span></span>
- <span data-ttu-id="9de09-126">Wszystko</span><span class="sxs-lookup"><span data-stu-id="9de09-126">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-127">- JobId</span><span class="sxs-lookup"><span data-stu-id="9de09-127">-JobId</span></span>
<span data-ttu-id="9de09-128">Określa identyfikator zadania do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="9de09-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9de09-129">-Name</span></span>
<span data-ttu-id="9de09-130">Określa nazwę, która ma być filtrowana w wynikach listy zadań.</span><span class="sxs-lookup"><span data-stu-id="9de09-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="9de09-131">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9de09-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9de09-132">Brak</span><span class="sxs-lookup"><span data-stu-id="9de09-132">None</span></span>
- <span data-ttu-id="9de09-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="9de09-133">DebugInfo</span></span>
- <span data-ttu-id="9de09-134">Statystyka</span><span class="sxs-lookup"><span data-stu-id="9de09-134">Statistics</span></span>
- <span data-ttu-id="9de09-135">Wszystko</span><span class="sxs-lookup"><span data-stu-id="9de09-135">All</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="9de09-136">-PipelineId</span></span>
<span data-ttu-id="9de09-137">Powinien zostać zwrócony identyfikator opcjonalny, który wskazuje, że mają być zwracane tylko zadania w części określonego potoku.</span><span class="sxs-lookup"><span data-stu-id="9de09-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="9de09-138">-RecurrenceId</span></span>
<span data-ttu-id="9de09-139">Powinien zostać zwrócony identyfikator opcjonalny, który wskazuje, że mają być zwracane tylko zadania w ramach określonego cyklu.</span><span class="sxs-lookup"><span data-stu-id="9de09-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-140">— wynik</span><span class="sxs-lookup"><span data-stu-id="9de09-140">-Result</span></span>
<span data-ttu-id="9de09-141">Określa filtr wyników dla wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="9de09-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="9de09-142">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9de09-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9de09-143">Brak</span><span class="sxs-lookup"><span data-stu-id="9de09-143">None</span></span>
- <span data-ttu-id="9de09-144">Anulowano</span><span class="sxs-lookup"><span data-stu-id="9de09-144">Cancelled</span></span>
- <span data-ttu-id="9de09-145">Niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="9de09-145">Failed</span></span>
- <span data-ttu-id="9de09-146">Udało się</span><span class="sxs-lookup"><span data-stu-id="9de09-146">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-147">— województwo</span><span class="sxs-lookup"><span data-stu-id="9de09-147">-State</span></span>
<span data-ttu-id="9de09-148">Określa filtr stanu dla wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="9de09-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="9de09-149">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9de09-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9de09-150">Zaakceptowane</span><span class="sxs-lookup"><span data-stu-id="9de09-150">Accepted</span></span>
- <span data-ttu-id="9de09-151">Nowy</span><span class="sxs-lookup"><span data-stu-id="9de09-151">New</span></span>
- <span data-ttu-id="9de09-152">Kompilowanie</span><span class="sxs-lookup"><span data-stu-id="9de09-152">Compiling</span></span>
- <span data-ttu-id="9de09-153">Planowanie</span><span class="sxs-lookup"><span data-stu-id="9de09-153">Scheduling</span></span>
- <span data-ttu-id="9de09-154">W kolejce</span><span class="sxs-lookup"><span data-stu-id="9de09-154">Queued</span></span>
- <span data-ttu-id="9de09-155">Rozpoczynanie</span><span class="sxs-lookup"><span data-stu-id="9de09-155">Starting</span></span>
- <span data-ttu-id="9de09-156">Wstrzymano</span><span class="sxs-lookup"><span data-stu-id="9de09-156">Paused</span></span>
- <span data-ttu-id="9de09-157">Uruchomione</span><span class="sxs-lookup"><span data-stu-id="9de09-157">Running</span></span>
- <span data-ttu-id="9de09-158">Zakończone</span><span class="sxs-lookup"><span data-stu-id="9de09-158">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="9de09-159">-SubmittedAfter</span></span>
<span data-ttu-id="9de09-160">Określa filtr daty.</span><span class="sxs-lookup"><span data-stu-id="9de09-160">Specifies a date filter.</span></span>
<span data-ttu-id="9de09-161">Ten parametr umożliwia filtrowanie wyników listy zadań do zadań przesłanych po określonej dacie.</span><span class="sxs-lookup"><span data-stu-id="9de09-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="9de09-162">-SubmittedBefore</span></span>
<span data-ttu-id="9de09-163">Określa filtr daty.</span><span class="sxs-lookup"><span data-stu-id="9de09-163">Specifies a date filter.</span></span>
<span data-ttu-id="9de09-164">Ten parametr umożliwia filtrowanie wyników listy zadań do zadań przesłanych przed określoną datą.</span><span class="sxs-lookup"><span data-stu-id="9de09-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-165">— Przesyłanie</span><span class="sxs-lookup"><span data-stu-id="9de09-165">-Submitter</span></span>
<span data-ttu-id="9de09-166">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9de09-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="9de09-167">Ten parametr umożliwia filtrowanie wyników listy zadań do zadań przesłanych przez określonego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9de09-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-168">— Na górze</span><span class="sxs-lookup"><span data-stu-id="9de09-168">-Top</span></span>
<span data-ttu-id="9de09-169">Opcjonalna wartość wskazująca liczbę zadań do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="9de09-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="9de09-170">Wartość domyślna to 500</span><span class="sxs-lookup"><span data-stu-id="9de09-170">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de09-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de09-171">CommonParameters</span></span>
<span data-ttu-id="9de09-172">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de09-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de09-173">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de09-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de09-174">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9de09-174">INPUTS</span></span>

### <span data-ttu-id="9de09-175">System.String</span><span class="sxs-lookup"><span data-stu-id="9de09-175">System.String</span></span>

### <span data-ttu-id="9de09-176">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9de09-176">System.Guid</span></span>

### <span data-ttu-id="9de09-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="9de09-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="9de09-178">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9de09-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9de09-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span><span class="sxs-lookup"><span data-stu-id="9de09-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="9de09-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span><span class="sxs-lookup"><span data-stu-id="9de09-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="9de09-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9de09-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9de09-182">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9de09-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9de09-183">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9de09-183">OUTPUTS</span></span>

### <span data-ttu-id="9de09-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="9de09-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="9de09-185">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9de09-185">NOTES</span></span>

## <span data-ttu-id="9de09-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9de09-186">RELATED LINKS</span></span>

[<span data-ttu-id="9de09-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9de09-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="9de09-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9de09-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="9de09-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9de09-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


