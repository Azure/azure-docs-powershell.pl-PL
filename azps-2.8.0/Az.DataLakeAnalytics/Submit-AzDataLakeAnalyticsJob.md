---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 23c8f8baa2753382ef2ee91f62199966a4fb9c2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705852"
---
# <span data-ttu-id="cb2ad-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cb2ad-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="cb2ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2ad-103">Przesyła zadanie.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-103">Submits a job.</span></span>

## <span data-ttu-id="cb2ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb2ad-104">SYNTAX</span></span>

### <span data-ttu-id="cb2ad-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="cb2ad-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2ad-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="cb2ad-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2ad-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="cb2ad-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2ad-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="cb2ad-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2ad-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="cb2ad-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb2ad-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="cb2ad-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb2ad-111">Opis</span><span class="sxs-lookup"><span data-stu-id="cb2ad-111">DESCRIPTION</span></span>
<span data-ttu-id="cb2ad-112">Polecenie cmdlet **Submit-AzDataLakeAnalyticsJob** przesyła zadanie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="cb2ad-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb2ad-113">EXAMPLES</span></span>

### <span data-ttu-id="cb2ad-114">Przykład 1: przesyłanie zadania</span><span class="sxs-lookup"><span data-stu-id="cb2ad-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="cb2ad-115">To polecenie przesyła zadanie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="cb2ad-116">Przykład 2: przesyłanie zadania za pomocą parametrów skryptu</span><span class="sxs-lookup"><span data-stu-id="cb2ad-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="cb2ad-117">Parametry skryptu U — SQL są poprzedzone powyżej treści skryptu głównego, na przykład: DECLARE @Department String = "Sales"; DECLARE @NumRecords = 1000; DECLARE @StartDateTime DateTime = New DateTime (2017; 12; 6; 0; 0; 0; 0);</span><span class="sxs-lookup"><span data-stu-id="cb2ad-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="cb2ad-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb2ad-118">PARAMETERS</span></span>

### <span data-ttu-id="cb2ad-119">— Konto</span><span class="sxs-lookup"><span data-stu-id="cb2ad-119">-Account</span></span>
<span data-ttu-id="cb2ad-120">Nazwa konta usługi Data Lake Analytics, w ramach którego zostanie przesłane zadanie.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="cb2ad-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="cb2ad-121">-AnalyticsUnits</span></span>
<span data-ttu-id="cb2ad-122">Jednostki analiz, które mają być używane dla tego zadania.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-122">The analytics units to use for this job.</span></span> <span data-ttu-id="cb2ad-123">Zwykle więcej jednostek analitycznych przeznaczonych do skryptu powoduje przyspieszenie czasu wykonywania skryptu.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

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

### <span data-ttu-id="cb2ad-124">-Compilemode</span><span class="sxs-lookup"><span data-stu-id="cb2ad-124">-CompileMode</span></span>
<span data-ttu-id="cb2ad-125">Typ kompilacji, który ma zostać wykonany dla tego zadania.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="cb2ad-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="cb2ad-126">Valid values:</span></span> 
- <span data-ttu-id="cb2ad-127">Semantyka (przeprowadzanie tylko testów semantycznych i niezbędnych testów Sanity)</span><span class="sxs-lookup"><span data-stu-id="cb2ad-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="cb2ad-128">Pełna (pełna Kompilacja)</span><span class="sxs-lookup"><span data-stu-id="cb2ad-128">Full (Full compilation)</span></span>
- <span data-ttu-id="cb2ad-129">SingleBox (pełna kompilacja prowadzona lokalnie)</span><span class="sxs-lookup"><span data-stu-id="cb2ad-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="cb2ad-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="cb2ad-130">-CompileOnly</span></span>
<span data-ttu-id="cb2ad-131">Wskazuje, że przesłanie zadania powinno być wykonane tylko w przypadku, gdy ustawiono wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="cb2ad-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2ad-132">-DefaultProfile</span></span>
<span data-ttu-id="cb2ad-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cb2ad-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb2ad-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cb2ad-134">-Name</span></span>
<span data-ttu-id="cb2ad-135">Przyjazna nazwa zadania do przesłania.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="cb2ad-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="cb2ad-136">-PipelineId</span></span>
<span data-ttu-id="cb2ad-137">Identyfikator wskazujący przesłanie tego zadania to część zestawu zadań cyklicznych, a także skojarzona z potokiem zadania.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

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

### <span data-ttu-id="cb2ad-138">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="cb2ad-138">-PipelineName</span></span>
<span data-ttu-id="cb2ad-139">Opcjonalna przyjazna nazwa dla rurociągu skojarzonego z tym zadaniem.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-139">An optional friendly name for the pipeline associated with this job.</span></span>

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

### <span data-ttu-id="cb2ad-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="cb2ad-140">-PipelineUri</span></span>
<span data-ttu-id="cb2ad-141">Opcjonalny identyfikator URI łączący z usługą inicjującą skojarzoną z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

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

### <span data-ttu-id="cb2ad-142">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="cb2ad-142">-Priority</span></span>
<span data-ttu-id="cb2ad-143">Priorytet zadania.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-143">The priority of the job.</span></span> <span data-ttu-id="cb2ad-144">Jeśli nie określono, priorytet to 1000.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="cb2ad-145">Niższy numer oznacza wyższy priorytet zadania.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="cb2ad-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="cb2ad-146">-RecurrenceId</span></span>
<span data-ttu-id="cb2ad-147">Identyfikator wskazujący, że przesłanie tego zadania jest częścią zestawu zadań cyklicznych o tym samym IDENTYFIKATORze cyklu.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

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

### <span data-ttu-id="cb2ad-148">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="cb2ad-148">-RecurrenceName</span></span>
<span data-ttu-id="cb2ad-149">Opcjonalna przyjazna nazwa korelacji cyklu między zadaniami.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

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

### <span data-ttu-id="cb2ad-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="cb2ad-150">-RunId</span></span>
<span data-ttu-id="cb2ad-151">Identyfikator identyfikujący określoną iterację uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

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

### <span data-ttu-id="cb2ad-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="cb2ad-152">-Runtime</span></span>
<span data-ttu-id="cb2ad-153">Opcjonalnie Ustaw wersję środowiska uruchomieniowego do użycia dla zadania.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="cb2ad-154">W przypadku pozostawienia tego ustawienia zostanie użyte domyślne środowisko uruchomieniowe.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="cb2ad-155">-Script</span><span class="sxs-lookup"><span data-stu-id="cb2ad-155">-Script</span></span>
<span data-ttu-id="cb2ad-156">Skrypt do wykonania (napisany w tekście).</span><span class="sxs-lookup"><span data-stu-id="cb2ad-156">Script to execute (written inline).</span></span>

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

### <span data-ttu-id="cb2ad-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="cb2ad-157">-ScriptParameter</span></span>
<span data-ttu-id="cb2ad-158">Parametry skryptu dla tego zadania, jako słownik nazw parametrów (String) do wartości (dowolna kombinacja Byte, bajty, int, uint (lub UInt32), Long, ULONG (lub UInt64), float, Double, decimal, Short (lub Int16), (lub UInt16), char, String, DateTime, bool, GUID lub Byte []).</span><span class="sxs-lookup"><span data-stu-id="cb2ad-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

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

### <span data-ttu-id="cb2ad-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="cb2ad-159">-ScriptPath</span></span>
<span data-ttu-id="cb2ad-160">Ścieżka do pliku skryptu do przesłania.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-160">Path to the script file to submit.</span></span>

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

### <span data-ttu-id="cb2ad-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2ad-161">CommonParameters</span></span>
<span data-ttu-id="cb2ad-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb2ad-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2ad-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb2ad-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2ad-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb2ad-164">INPUTS</span></span>

### <span data-ttu-id="cb2ad-165">System. String</span><span class="sxs-lookup"><span data-stu-id="cb2ad-165">System.String</span></span>

### <span data-ttu-id="cb2ad-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cb2ad-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="cb2ad-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cb2ad-167">System.Int32</span></span>

### <span data-ttu-id="cb2ad-168">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="cb2ad-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="cb2ad-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cb2ad-169">System.Guid</span></span>

### <span data-ttu-id="cb2ad-170">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cb2ad-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cb2ad-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb2ad-171">OUTPUTS</span></span>

### <span data-ttu-id="cb2ad-172">Microsoft. Azure. Management. datalake. Analytics. modele. JobInformation</span><span class="sxs-lookup"><span data-stu-id="cb2ad-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="cb2ad-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb2ad-173">NOTES</span></span>

## <span data-ttu-id="cb2ad-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb2ad-174">RELATED LINKS</span></span>

[<span data-ttu-id="cb2ad-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cb2ad-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="cb2ad-176">Zatrzymaj — AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cb2ad-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="cb2ad-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="cb2ad-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


