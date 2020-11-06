---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/submit-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: fc09560bca0d825cc65d8a4f964119cd50898190
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526861"
---
# <span data-ttu-id="0599e-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0599e-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="0599e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0599e-102">SYNOPSIS</span></span>
<span data-ttu-id="0599e-103">Przesyła zadanie.</span><span class="sxs-lookup"><span data-stu-id="0599e-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0599e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0599e-104">SYNTAX</span></span>

### <span data-ttu-id="0599e-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="0599e-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0599e-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="0599e-106">SubmitUSqlJob</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0599e-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="0599e-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0599e-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="0599e-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0599e-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="0599e-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0599e-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="0599e-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0599e-111">Opis</span><span class="sxs-lookup"><span data-stu-id="0599e-111">DESCRIPTION</span></span>
<span data-ttu-id="0599e-112">Polecenie cmdlet **Submit-AzureRmDataLakeAnalyticsJob** przesyła zadanie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0599e-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="0599e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0599e-113">EXAMPLES</span></span>

### <span data-ttu-id="0599e-114">Przykład 1: przesyłanie zadania</span><span class="sxs-lookup"><span data-stu-id="0599e-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="0599e-115">To polecenie przesyła zadanie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0599e-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="0599e-116">Przykład 2: przesyłanie zadania za pomocą parametrów skryptu</span><span class="sxs-lookup"><span data-stu-id="0599e-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="0599e-117">Parametry skryptu U — SQL są poprzedzone powyżej treści skryptu głównego, na przykład:</span><span class="sxs-lookup"><span data-stu-id="0599e-117">U-SQL script parameters are prepended above the main script contents, e.g.:</span></span>

<span data-ttu-id="0599e-118">DECLARE @Department String = "Sales"; DECLARE @NumRecords = 1000; DECLARE @StartDateTime DateTime = New DateTime (2017; 12; 6; 0; 0; 0; 0);</span><span class="sxs-lookup"><span data-stu-id="0599e-118">DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="0599e-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0599e-119">PARAMETERS</span></span>

### <span data-ttu-id="0599e-120">— Konto</span><span class="sxs-lookup"><span data-stu-id="0599e-120">-Account</span></span>
<span data-ttu-id="0599e-121">Nazwa konta usługi Data Lake Analytics, w ramach którego zostanie przesłane zadanie.</span><span class="sxs-lookup"><span data-stu-id="0599e-121">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="0599e-122">-Compilemode</span><span class="sxs-lookup"><span data-stu-id="0599e-122">-CompileMode</span></span>
<span data-ttu-id="0599e-123">Typ kompilacji, który ma zostać wykonany dla tego zadania.</span><span class="sxs-lookup"><span data-stu-id="0599e-123">The type of compilation to be done on this job.</span></span> <span data-ttu-id="0599e-124">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="0599e-124">Valid values:</span></span> 

- <span data-ttu-id="0599e-125">Semantyka (przeprowadzanie tylko testów semantycznych i niezbędnych testów Sanity)</span><span class="sxs-lookup"><span data-stu-id="0599e-125">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="0599e-126">Pełna (pełna Kompilacja)</span><span class="sxs-lookup"><span data-stu-id="0599e-126">Full (Full compilation)</span></span>
- <span data-ttu-id="0599e-127">SingleBox (pełna kompilacja prowadzona lokalnie)</span><span class="sxs-lookup"><span data-stu-id="0599e-127">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-128">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="0599e-128">-CompileOnly</span></span>
<span data-ttu-id="0599e-129">Wskazuje, że przesłanie zadania powinno być wykonane tylko w przypadku, gdy ustawiono wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="0599e-129">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0599e-130">-DefaultProfile</span></span>
<span data-ttu-id="0599e-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0599e-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0599e-132">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="0599e-132">-AnalyticsUnits</span></span>
<span data-ttu-id="0599e-133">Jednostki analiz, które mają być używane dla tego zadania.</span><span class="sxs-lookup"><span data-stu-id="0599e-133">The analytics units to use for this job.</span></span> <span data-ttu-id="0599e-134">Zwykle więcej jednostek analitycznych przeznaczonych do skryptu powoduje przyspieszenie czasu wykonywania skryptu.</span><span class="sxs-lookup"><span data-stu-id="0599e-134">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0599e-135">-Name</span></span>
<span data-ttu-id="0599e-136">Przyjazna nazwa zadania do przesłania.</span><span class="sxs-lookup"><span data-stu-id="0599e-136">The friendly name of the job to submit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-137">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="0599e-137">-PipelineId</span></span>
<span data-ttu-id="0599e-138">Identyfikator wskazujący przesłanie tego zadania to część zestawu zadań cyklicznych, a także skojarzona z potokiem zadania.</span><span class="sxs-lookup"><span data-stu-id="0599e-138">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-139">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="0599e-139">-PipelineName</span></span>
<span data-ttu-id="0599e-140">Opcjonalna przyjazna nazwa dla rurociągu skojarzonego z tym zadaniem.</span><span class="sxs-lookup"><span data-stu-id="0599e-140">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-141">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="0599e-141">-PipelineUri</span></span>
<span data-ttu-id="0599e-142">Opcjonalny identyfikator URI łączący z usługą inicjującą skojarzoną z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="0599e-142">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-143">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="0599e-143">-Priority</span></span>
<span data-ttu-id="0599e-144">Priorytet zadania.</span><span class="sxs-lookup"><span data-stu-id="0599e-144">The priority of the job.</span></span> <span data-ttu-id="0599e-145">Jeśli nie określono, priorytet to 1000.</span><span class="sxs-lookup"><span data-stu-id="0599e-145">If not specified, the priority is 1000.</span></span> <span data-ttu-id="0599e-146">Niższy numer oznacza wyższy priorytet zadania.</span><span class="sxs-lookup"><span data-stu-id="0599e-146">A lower number indicates a higher job priority.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-147">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="0599e-147">-RecurrenceId</span></span>
<span data-ttu-id="0599e-148">Identyfikator wskazujący, że przesłanie tego zadania jest częścią zestawu zadań cyklicznych o tym samym IDENTYFIKATORze cyklu.</span><span class="sxs-lookup"><span data-stu-id="0599e-148">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-149">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="0599e-149">-RecurrenceName</span></span>
<span data-ttu-id="0599e-150">Opcjonalna przyjazna nazwa korelacji cyklu między zadaniami.</span><span class="sxs-lookup"><span data-stu-id="0599e-150">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-151">-RunId</span><span class="sxs-lookup"><span data-stu-id="0599e-151">-RunId</span></span>
<span data-ttu-id="0599e-152">Identyfikator identyfikujący określoną iterację uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="0599e-152">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-153">-Runtime</span><span class="sxs-lookup"><span data-stu-id="0599e-153">-Runtime</span></span>
<span data-ttu-id="0599e-154">Opcjonalnie Ustaw wersję środowiska uruchomieniowego do użycia dla zadania.</span><span class="sxs-lookup"><span data-stu-id="0599e-154">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="0599e-155">W przypadku pozostawienia tego ustawienia zostanie użyte domyślne środowisko uruchomieniowe.</span><span class="sxs-lookup"><span data-stu-id="0599e-155">If left unset, the default runtime is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-156">-Script</span><span class="sxs-lookup"><span data-stu-id="0599e-156">-Script</span></span>
<span data-ttu-id="0599e-157">Skrypt do wykonania (napisany w tekście).</span><span class="sxs-lookup"><span data-stu-id="0599e-157">Script to execute (written inline).</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-158">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="0599e-158">-ScriptParameter</span></span>
<span data-ttu-id="0599e-159">Parametry skryptu dla tego zadania, jako słownik nazw parametrów (String) do wartości (dowolna kombinacja Byte, bajty, int, uint (lub UInt32), Long, ULONG (lub UInt64), float, Double, decimal, Short (lub Int16), (lub UInt16), char, String, DateTime, bool, GUID lub Byte []).</span><span class="sxs-lookup"><span data-stu-id="0599e-159">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-160">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="0599e-160">-ScriptPath</span></span>
<span data-ttu-id="0599e-161">Ścieżka do pliku skryptu do przesłania.</span><span class="sxs-lookup"><span data-stu-id="0599e-161">Path to the script file to submit.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0599e-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0599e-162">CommonParameters</span></span>
<span data-ttu-id="0599e-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0599e-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0599e-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0599e-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0599e-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0599e-165">INPUTS</span></span>

### <span data-ttu-id="0599e-166">Ciąg</span><span class="sxs-lookup"><span data-stu-id="0599e-166">String</span></span>
<span data-ttu-id="0599e-167">Parametr "Script" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="0599e-167">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="0599e-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0599e-168">OUTPUTS</span></span>

### <span data-ttu-id="0599e-169">JobInformation</span><span class="sxs-lookup"><span data-stu-id="0599e-169">JobInformation</span></span>
<span data-ttu-id="0599e-170">Wstępne szczegóły zadania przesłanego zadania.</span><span class="sxs-lookup"><span data-stu-id="0599e-170">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="0599e-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0599e-171">NOTES</span></span>

## <span data-ttu-id="0599e-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0599e-172">RELATED LINKS</span></span>

[<span data-ttu-id="0599e-173">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0599e-173">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="0599e-174">Zatrzymaj — AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0599e-174">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="0599e-175">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0599e-175">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


