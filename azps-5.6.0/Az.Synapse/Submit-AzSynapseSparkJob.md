---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: 0555d9ba860d9a8c4c036fa9171d1fadc7a167eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011290"
---
# <span data-ttu-id="49ca8-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="49ca8-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="49ca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="49ca8-103">Przesyła zadanie analizy Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="49ca8-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="49ca8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49ca8-104">SYNTAX</span></span>

### <span data-ttu-id="49ca8-105">RunSparkJobParameterSetName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="49ca8-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ca8-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ca8-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ca8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="49ca8-107">DESCRIPTION</span></span>
<span data-ttu-id="49ca8-108">Polecenie cmdlet **Submit-AzSynapseSparkJob** przesyła zadanie analizy Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="49ca8-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="49ca8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49ca8-109">EXAMPLES</span></span>

### <span data-ttu-id="49ca8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49ca8-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="49ca8-111">To polecenie przesyła zadanie analizy Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="49ca8-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="49ca8-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="49ca8-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="49ca8-113">To polecenie przesyła zadanie .NET analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="49ca8-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="49ca8-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="49ca8-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="49ca8-115">To polecenie przesyła zadanie aplikacji Synapse Analytics PySpark.</span><span class="sxs-lookup"><span data-stu-id="49ca8-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="49ca8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49ca8-116">PARAMETERS</span></span>

### <span data-ttu-id="49ca8-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="49ca8-117">-CommandLineArgument</span></span>
<span data-ttu-id="49ca8-118">Argumenty opcjonalne dla zadania.</span><span class="sxs-lookup"><span data-stu-id="49ca8-118">Optional arguments to the job.</span></span> <span data-ttu-id="49ca8-119">np. "-iteracja 10000 --limit czasu 20s"</span><span class="sxs-lookup"><span data-stu-id="49ca8-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-120">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="49ca8-120">-Configuration</span></span>
<span data-ttu-id="49ca8-121">Właściwości konfiguracji przebiegu w przebiegu w sieci.</span><span class="sxs-lookup"><span data-stu-id="49ca8-121">Spark configuration properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ca8-122">-DefaultProfile</span></span>
<span data-ttu-id="49ca8-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49ca8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49ca8-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="49ca8-124">-ExecutorCount</span></span>
<span data-ttu-id="49ca8-125">Liczba executorów, którzy mają zostać przydzieleni w określonej puli przebiegu w czasie dla zadania.</span><span class="sxs-lookup"><span data-stu-id="49ca8-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="49ca8-126">-ExecutorSize</span></span>
<span data-ttu-id="49ca8-127">Liczba rdzeni i pamięci, które mają być używane dla executorów przydzielonych do określonej puli przebiegu w czasie dla zadania.</span><span class="sxs-lookup"><span data-stu-id="49ca8-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-128">— język</span><span class="sxs-lookup"><span data-stu-id="49ca8-128">-Language</span></span>
<span data-ttu-id="49ca8-129">Język zadania do przesyłania.</span><span class="sxs-lookup"><span data-stu-id="49ca8-129">Language of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="49ca8-130">-MainClassName</span></span>
<span data-ttu-id="49ca8-131">W pełni kwalifikowany identyfikator lub główna klasa, która znajduje się w pliku definicji głównej.</span><span class="sxs-lookup"><span data-stu-id="49ca8-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="49ca8-132">Wymagane dla zadania spark i .NET Spark.</span><span class="sxs-lookup"><span data-stu-id="49ca8-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="49ca8-133">np. "org.org.spark.examples.SparkPi"</span><span class="sxs-lookup"><span data-stu-id="49ca8-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MainExecutableFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="49ca8-134">-MainDefinitionFile</span></span>
<span data-ttu-id="49ca8-135">Główny plik używany w zadaniu.</span><span class="sxs-lookup"><span data-stu-id="49ca8-135">The main file used for the job.</span></span>
<span data-ttu-id="49ca8-136">np. " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="49ca8-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49ca8-137">-Name</span></span>
<span data-ttu-id="49ca8-138">Nazwa zadania przebiegu w przebiegu w imieniu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="49ca8-138">Name of Spark job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="49ca8-139">-ReferenceFile</span></span>
<span data-ttu-id="49ca8-140">Dodatkowe pliki używane w celach referencyjnych w głównym pliku definicji.</span><span class="sxs-lookup"><span data-stu-id="49ca8-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="49ca8-141">Lista URI magazynu rozdzielana przecinkami.</span><span class="sxs-lookup"><span data-stu-id="49ca8-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="49ca8-142">np. " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="49ca8-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="49ca8-143">-SparkPoolName</span></span>
<span data-ttu-id="49ca8-144">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="49ca8-144">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-145">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="49ca8-145">-SparkPoolObject</span></span>
<span data-ttu-id="49ca8-146">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="49ca8-146">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: RunSparkJobByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="49ca8-147">-WorkspaceName</span></span>
<span data-ttu-id="49ca8-148">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="49ca8-148">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49ca8-149">-Confirm</span></span>
<span data-ttu-id="49ca8-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49ca8-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ca8-151">-WhatIf</span></span>
<span data-ttu-id="49ca8-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ca8-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49ca8-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49ca8-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ca8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ca8-154">CommonParameters</span></span>
<span data-ttu-id="49ca8-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ca8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ca8-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49ca8-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ca8-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49ca8-157">INPUTS</span></span>

### <span data-ttu-id="49ca8-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="49ca8-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="49ca8-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49ca8-159">OUTPUTS</span></span>

### <span data-ttu-id="49ca8-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="49ca8-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="49ca8-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49ca8-161">NOTES</span></span>

## <span data-ttu-id="49ca8-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49ca8-162">RELATED LINKS</span></span>
