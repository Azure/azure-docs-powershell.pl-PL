---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549227"
---
# <span data-ttu-id="85c69-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="85c69-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="85c69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85c69-102">SYNOPSIS</span></span>
<span data-ttu-id="85c69-103">Przesyła zadanie.</span><span class="sxs-lookup"><span data-stu-id="85c69-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85c69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85c69-104">SYNTAX</span></span>

### <span data-ttu-id="85c69-105">Prześlij zadanie ze ścieżką skryptu dla p-SQL</span><span class="sxs-lookup"><span data-stu-id="85c69-105">Submit job with script path for U-SQL</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c69-106">Prześlij zadanie w usłudze c-SQL</span><span class="sxs-lookup"><span data-stu-id="85c69-106">Submit U-SQL Job</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c69-107">Prześlij zadanie ze ścieżką skryptu dla p-SQL z informacjami o reucurrence</span><span class="sxs-lookup"><span data-stu-id="85c69-107">Submit job with script path for U-SQL with reucurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c69-108">Przesyłanie zadania U-SQL z informacjami o cyklu</span><span class="sxs-lookup"><span data-stu-id="85c69-108">Submit U-SQL Job with recurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85c69-109">Prześlij zadanie ze ścieżką skryptu dla p-SQL z reucurrence i informacjami o rurociągu</span><span class="sxs-lookup"><span data-stu-id="85c69-109">Submit job with script path for U-SQL with reucurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85c69-110">Przesyłanie zadania U-SQL z informacjami o cyklu i potoku</span><span class="sxs-lookup"><span data-stu-id="85c69-110">Submit U-SQL Job with recurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85c69-111">Opis</span><span class="sxs-lookup"><span data-stu-id="85c69-111">DESCRIPTION</span></span>
<span data-ttu-id="85c69-112">Polecenie cmdlet **Submit-AzureRmDataLakeAnalyticsJob** przesyła zadanie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="85c69-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="85c69-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85c69-113">EXAMPLES</span></span>

### <span data-ttu-id="85c69-114">Przykład 1: przesyłanie zadania</span><span class="sxs-lookup"><span data-stu-id="85c69-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

<span data-ttu-id="85c69-115">To polecenie przesyła zadanie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="85c69-115">This command submits a Data Lake Analytics job.</span></span>

## <span data-ttu-id="85c69-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85c69-116">PARAMETERS</span></span>

### <span data-ttu-id="85c69-117">— Konto</span><span class="sxs-lookup"><span data-stu-id="85c69-117">-Account</span></span>
<span data-ttu-id="85c69-118">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="85c69-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="85c69-119">-Compilemode</span><span class="sxs-lookup"><span data-stu-id="85c69-119">-CompileMode</span></span>
<span data-ttu-id="85c69-120">Określa tryb kompilacji zadania.</span><span class="sxs-lookup"><span data-stu-id="85c69-120">Specifies the compilation mode of the job.</span></span>
<span data-ttu-id="85c69-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="85c69-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85c69-122">Semantyczny biznesowej</span><span class="sxs-lookup"><span data-stu-id="85c69-122">Semantic</span></span>
- <span data-ttu-id="85c69-123">Pełnotekstowej</span><span class="sxs-lookup"><span data-stu-id="85c69-123">Full</span></span>
- <span data-ttu-id="85c69-124">SingleBox</span><span class="sxs-lookup"><span data-stu-id="85c69-124">SingleBox</span></span>

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

### <span data-ttu-id="85c69-125">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="85c69-125">-CompileOnly</span></span>
<span data-ttu-id="85c69-126">Wskazuje, że to polecenie cmdlet kompiluje zadanie bez uruchamiania go.</span><span class="sxs-lookup"><span data-stu-id="85c69-126">Indicates that this cmdlet compiles the job without running it.</span></span>

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

### <span data-ttu-id="85c69-127">-DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="85c69-127">-DegreeOfParallelism</span></span>
<span data-ttu-id="85c69-128">Określa jednostki usługi Data Lake Analytics (DLAU) zadania, które wskazuje maksymalną dozwoloną Równoległość zadania.</span><span class="sxs-lookup"><span data-stu-id="85c69-128">Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c69-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85c69-129">-Name</span></span>
<span data-ttu-id="85c69-130">Określa nazwę zadania.</span><span class="sxs-lookup"><span data-stu-id="85c69-130">Specifies the job name.</span></span>

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

### <span data-ttu-id="85c69-131">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="85c69-131">-PipelineId</span></span>
<span data-ttu-id="85c69-132">Identyfikator wskazujący przesłanie tego zadania to część zestawu zadań cyklicznych, a także skojarzona z potokiem zadania.</span><span class="sxs-lookup"><span data-stu-id="85c69-132">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c69-133">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="85c69-133">-PipelineName</span></span>
<span data-ttu-id="85c69-134">Opcjonalna przyjazna nazwa dla rurociągu skojarzonego z tym zadaniem.</span><span class="sxs-lookup"><span data-stu-id="85c69-134">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c69-135">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="85c69-135">-PipelineUri</span></span>
<span data-ttu-id="85c69-136">Opcjonalny identyfikator URI łączący z usługą inicjującą skojarzoną z tym potokiem.</span><span class="sxs-lookup"><span data-stu-id="85c69-136">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c69-137">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="85c69-137">-Priority</span></span>
<span data-ttu-id="85c69-138">Określa priorytet zadania.</span><span class="sxs-lookup"><span data-stu-id="85c69-138">Specifies the priority of the job.</span></span>
<span data-ttu-id="85c69-139">Jeśli nie określono, priorytet to 1000.</span><span class="sxs-lookup"><span data-stu-id="85c69-139">If not specified, the priority is 1000.</span></span>
<span data-ttu-id="85c69-140">Mała liczba wskazuje wyższy priorytet zadania.</span><span class="sxs-lookup"><span data-stu-id="85c69-140">A low number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="85c69-141">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="85c69-141">-RecurrenceId</span></span>
<span data-ttu-id="85c69-142">Identyfikator wskazujący, że przesłanie tego zadania jest częścią zestawu zadań cyklicznych o tym samym IDENTYFIKATORze cyklu.</span><span class="sxs-lookup"><span data-stu-id="85c69-142">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c69-143">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="85c69-143">-RecurrenceName</span></span>
<span data-ttu-id="85c69-144">Opcjonalna przyjazna nazwa korelacji cyklu między zadaniami.</span><span class="sxs-lookup"><span data-stu-id="85c69-144">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c69-145">-RunId</span><span class="sxs-lookup"><span data-stu-id="85c69-145">-RunId</span></span>
<span data-ttu-id="85c69-146">Identyfikator identyfikujący określoną iterację uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="85c69-146">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c69-147">-Runtime</span><span class="sxs-lookup"><span data-stu-id="85c69-147">-Runtime</span></span>
<span data-ttu-id="85c69-148">Określa wersję zadania w czasie wykonywania.</span><span class="sxs-lookup"><span data-stu-id="85c69-148">Specifies the runtime version of the job.</span></span>

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

### <span data-ttu-id="85c69-149">-Script</span><span class="sxs-lookup"><span data-stu-id="85c69-149">-Script</span></span>
<span data-ttu-id="85c69-150">Określa zawartość skryptu, który ma zostać uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="85c69-150">Specifies the contents of the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85c69-151">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="85c69-151">-ScriptPath</span></span>
<span data-ttu-id="85c69-152">Określa ścieżkę do pliku lokalnego dla skryptu, który ma zostać uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="85c69-152">Specifies the local file path to the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c69-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c69-153">-DefaultProfile</span></span>
<span data-ttu-id="85c69-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85c69-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c69-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c69-155">CommonParameters</span></span>
<span data-ttu-id="85c69-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c69-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c69-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c69-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c69-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85c69-158">INPUTS</span></span>

### <span data-ttu-id="85c69-159">Ciąg</span><span class="sxs-lookup"><span data-stu-id="85c69-159">String</span></span>
<span data-ttu-id="85c69-160">Parametr "Script" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="85c69-160">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="85c69-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85c69-161">OUTPUTS</span></span>

### <span data-ttu-id="85c69-162">JobInformation</span><span class="sxs-lookup"><span data-stu-id="85c69-162">JobInformation</span></span>
<span data-ttu-id="85c69-163">Wstępne szczegóły zadania przesłanego zadania.</span><span class="sxs-lookup"><span data-stu-id="85c69-163">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="85c69-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85c69-164">NOTES</span></span>

## <span data-ttu-id="85c69-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85c69-165">RELATED LINKS</span></span>

[<span data-ttu-id="85c69-166">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="85c69-166">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="85c69-167">Zatrzymaj — AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="85c69-167">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="85c69-168">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="85c69-168">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


