---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 429b0a6cec9c7a3f27019e950e5497eac961c81f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986133"
---
# <span data-ttu-id="4046a-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4046a-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="4046a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4046a-102">SYNOPSIS</span></span>
<span data-ttu-id="4046a-103">Przesyła zadanie.</span><span class="sxs-lookup"><span data-stu-id="4046a-103">Submits a job.</span></span>

## <span data-ttu-id="4046a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4046a-104">SYNTAX</span></span>

### <span data-ttu-id="4046a-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="4046a-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4046a-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="4046a-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4046a-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="4046a-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4046a-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="4046a-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4046a-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="4046a-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4046a-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="4046a-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4046a-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="4046a-111">DESCRIPTION</span></span>
<span data-ttu-id="4046a-112">Polecenie **cmdlet Submit-AzDataLakeAnalyticsJob** przesyła zadanie Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4046a-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="4046a-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4046a-113">EXAMPLES</span></span>

### <span data-ttu-id="4046a-114">Przykład 1. Przesyłanie zadania</span><span class="sxs-lookup"><span data-stu-id="4046a-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="4046a-115">To polecenie przesyła zadanie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4046a-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="4046a-116">Przykład 2. Przesyłanie zadania z parametrami skryptu</span><span class="sxs-lookup"><span data-stu-id="4046a-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="4046a-117">Parametry skryptu języka U-SQL są przed zawartością głównego skryptu, na przykład: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017; 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="4046a-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="4046a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4046a-118">PARAMETERS</span></span>

### <span data-ttu-id="4046a-119">— Konto</span><span class="sxs-lookup"><span data-stu-id="4046a-119">-Account</span></span>
<span data-ttu-id="4046a-120">Nazwa konta Data Lake Analytics, pod którym zostanie przesłane zadanie.</span><span class="sxs-lookup"><span data-stu-id="4046a-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="4046a-121">- AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="4046a-121">-AnalyticsUnits</span></span>
<span data-ttu-id="4046a-122">Jednostki analizy, których należy użyć dla tego zadania.</span><span class="sxs-lookup"><span data-stu-id="4046a-122">The analytics units to use for this job.</span></span> <span data-ttu-id="4046a-123">Zazwyczaj więcej jednostek analizy przeznaczonych do skryptów przyspiesza wykonywanie skryptów.</span><span class="sxs-lookup"><span data-stu-id="4046a-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="4046a-124">-CompileMode</span></span>
<span data-ttu-id="4046a-125">Typ kompilacji, która ma zostać wykonana w tym zadaniu.</span><span class="sxs-lookup"><span data-stu-id="4046a-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="4046a-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="4046a-126">Valid values:</span></span> 
- <span data-ttu-id="4046a-127">Semantyczne (wykonuje tylko testy semantyczne i konieczne testy sanności)</span><span class="sxs-lookup"><span data-stu-id="4046a-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="4046a-128">Pełne (pełna kompilacja)</span><span class="sxs-lookup"><span data-stu-id="4046a-128">Full (Full compilation)</span></span>
- <span data-ttu-id="4046a-129">SingleBox (pełna kompilacja wykonywana lokalnie)</span><span class="sxs-lookup"><span data-stu-id="4046a-129">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="4046a-130">-CompileOnly</span></span>
<span data-ttu-id="4046a-131">Wskazuje, że zadanie powinno zostać skompilowane i nie powinno zostać wykonane tylko w przypadku, gdy ma ustawioną wartość True (Prawda).</span><span class="sxs-lookup"><span data-stu-id="4046a-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4046a-132">-DefaultProfile</span></span>
<span data-ttu-id="4046a-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4046a-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4046a-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4046a-134">-Name</span></span>
<span data-ttu-id="4046a-135">Przyjazna nazwa zadania do zgłoszenia.</span><span class="sxs-lookup"><span data-stu-id="4046a-135">The friendly name of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="4046a-136">-PipelineId</span></span>
<span data-ttu-id="4046a-137">Identyfikator wskazujący, że przesyłanie tego zadania jest częścią zestawu zadań cyklicznych, a także skojarzonych z potokiem zadania.</span><span class="sxs-lookup"><span data-stu-id="4046a-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="4046a-138">-PipelineName</span></span>
<span data-ttu-id="4046a-139">Opcjonalna przyjazna nazwa potoku skojarzonego z tym zadaniem.</span><span class="sxs-lookup"><span data-stu-id="4046a-139">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="4046a-140">-PipelineUri</span></span>
<span data-ttu-id="4046a-141">Opcjonalny uri, który łączy się z usługą pochodzącą skojarzoną z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="4046a-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-142">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="4046a-142">-Priority</span></span>
<span data-ttu-id="4046a-143">Priorytet zadania.</span><span class="sxs-lookup"><span data-stu-id="4046a-143">The priority of the job.</span></span> <span data-ttu-id="4046a-144">Jeśli nie zostanie określony, priorytet wynosi 1000.</span><span class="sxs-lookup"><span data-stu-id="4046a-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="4046a-145">Mniejsza liczba oznacza wyższy priorytet zadania.</span><span class="sxs-lookup"><span data-stu-id="4046a-145">A lower number indicates a higher job priority.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="4046a-146">-RecurrenceId</span></span>
<span data-ttu-id="4046a-147">Identyfikator wskazujący, że przesyłanie tego zadania jest częścią zestawu zadań cyklicznych o tym samym identyfikatorze cyklu.</span><span class="sxs-lookup"><span data-stu-id="4046a-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="4046a-148">-RecurrenceName</span></span>
<span data-ttu-id="4046a-149">Opcjonalna przyjazna nazwa korelacji cyklu między zadaniami.</span><span class="sxs-lookup"><span data-stu-id="4046a-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-150">- RunId</span><span class="sxs-lookup"><span data-stu-id="4046a-150">-RunId</span></span>
<span data-ttu-id="4046a-151">Identyfikator identyfikujący tę określoną iterację uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="4046a-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-152">— Środowisko uruchomieniowe</span><span class="sxs-lookup"><span data-stu-id="4046a-152">-Runtime</span></span>
<span data-ttu-id="4046a-153">Opcjonalnie ustaw wersję środowiska uruchomieniowego do użycia w zadaniu.</span><span class="sxs-lookup"><span data-stu-id="4046a-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="4046a-154">Jeśli pozostawisz ustawienie bez ustawienia, zostanie użyte domyślne środowisko uruchomieniowe.</span><span class="sxs-lookup"><span data-stu-id="4046a-154">If left unset, the default runtime is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-155">— Skrypt</span><span class="sxs-lookup"><span data-stu-id="4046a-155">-Script</span></span>
<span data-ttu-id="4046a-156">Skrypt do wykonania (napisany w tekście).</span><span class="sxs-lookup"><span data-stu-id="4046a-156">Script to execute (written inline).</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-157">-ScriptParameters</span><span class="sxs-lookup"><span data-stu-id="4046a-157">-ScriptParameter</span></span>
<span data-ttu-id="4046a-158">Parametry skryptu dla tego zadania, jako słownik nazw parametrów (ciąg) na wartości (dowolna kombinacja bajtów, sbyte, int, uint (lub uint32), long, ulong (lub uint64), float, double, decimal, short (lub int16), ortort (lub uint16), char, string, DateTime, bool, Guid lub byte[]).</span><span class="sxs-lookup"><span data-stu-id="4046a-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-159">- ScriptPath</span><span class="sxs-lookup"><span data-stu-id="4046a-159">-ScriptPath</span></span>
<span data-ttu-id="4046a-160">Ścieżka do pliku skryptu do przesyłania.</span><span class="sxs-lookup"><span data-stu-id="4046a-160">Path to the script file to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4046a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4046a-161">CommonParameters</span></span>
<span data-ttu-id="4046a-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4046a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4046a-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4046a-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4046a-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4046a-164">INPUTS</span></span>

### <span data-ttu-id="4046a-165">System.String</span><span class="sxs-lookup"><span data-stu-id="4046a-165">System.String</span></span>

### <span data-ttu-id="4046a-166">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="4046a-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4046a-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4046a-167">System.Int32</span></span>

### <span data-ttu-id="4046a-168">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="4046a-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="4046a-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4046a-169">System.Guid</span></span>

### <span data-ttu-id="4046a-170">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4046a-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4046a-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4046a-171">OUTPUTS</span></span>

### <span data-ttu-id="4046a-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="4046a-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="4046a-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4046a-173">NOTES</span></span>

## <span data-ttu-id="4046a-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4046a-174">RELATED LINKS</span></span>

[<span data-ttu-id="4046a-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4046a-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="4046a-176">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4046a-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="4046a-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4046a-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


