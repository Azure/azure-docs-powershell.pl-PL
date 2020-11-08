---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234218"
---
# <span data-ttu-id="e4adc-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="e4adc-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="e4adc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4adc-102">SYNOPSIS</span></span>
<span data-ttu-id="e4adc-103">Przesyła zadanie Synapse analiza Spark.</span><span class="sxs-lookup"><span data-stu-id="e4adc-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="e4adc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4adc-104">SYNTAX</span></span>

### <span data-ttu-id="e4adc-105">RunSparkJobParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e4adc-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4adc-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4adc-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4adc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e4adc-107">DESCRIPTION</span></span>
<span data-ttu-id="e4adc-108">Polecenie cmdlet **Submit-AzSynapseSparkJob** przesyła zadanie Synapse analiz Spark.</span><span class="sxs-lookup"><span data-stu-id="e4adc-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="e4adc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4adc-109">EXAMPLES</span></span>

### <span data-ttu-id="e4adc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e4adc-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="e4adc-111">To polecenie przesyła zadanie Synapse analiza Spark.</span><span class="sxs-lookup"><span data-stu-id="e4adc-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="e4adc-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e4adc-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="e4adc-113">To polecenie przesyła zadanie programu Synapse Analytics Spark .NET.</span><span class="sxs-lookup"><span data-stu-id="e4adc-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="e4adc-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e4adc-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="e4adc-115">To polecenie przesyła zadanie PySpark analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="e4adc-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="e4adc-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4adc-116">PARAMETERS</span></span>

### <span data-ttu-id="e4adc-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="e4adc-117">-CommandLineArgument</span></span>
<span data-ttu-id="e4adc-118">Opcjonalne argumenty zadania.</span><span class="sxs-lookup"><span data-stu-id="e4adc-118">Optional arguments to the job.</span></span> <span data-ttu-id="e4adc-119">na przykład "--iteracja 10000--timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="e4adc-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="e4adc-120">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="e4adc-120">-Configuration</span></span>
<span data-ttu-id="e4adc-121">Właściwości konfiguracji platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="e4adc-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="e4adc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4adc-122">-DefaultProfile</span></span>
<span data-ttu-id="e4adc-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4adc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4adc-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="e4adc-124">-ExecutorCount</span></span>
<span data-ttu-id="e4adc-125">Liczba wykonawców, które mają zostać przydzielone w określonej puli platformy Spark dla zadania.</span><span class="sxs-lookup"><span data-stu-id="e4adc-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="e4adc-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="e4adc-126">-ExecutorSize</span></span>
<span data-ttu-id="e4adc-127">Liczba podstawowych i pamięci, które mają być używane w przypadku modułów wykonujących zadania, przydzielonych w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="e4adc-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="e4adc-128">-Language</span><span class="sxs-lookup"><span data-stu-id="e4adc-128">-Language</span></span>
<span data-ttu-id="e4adc-129">Język zadania do przesłania.</span><span class="sxs-lookup"><span data-stu-id="e4adc-129">Language of the job to submit.</span></span>

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

### <span data-ttu-id="e4adc-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="e4adc-130">-MainClassName</span></span>
<span data-ttu-id="e4adc-131">W pełni kwalifikowany identyfikator lub główna Klasa, która znajduje się w głównym pliku definicji.</span><span class="sxs-lookup"><span data-stu-id="e4adc-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="e4adc-132">Wymagane dla zadania usługi Spark i .NET Spark.</span><span class="sxs-lookup"><span data-stu-id="e4adc-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="e4adc-133">na przykład "org. Apache. Spark. przykłady. SparkPi"</span><span class="sxs-lookup"><span data-stu-id="e4adc-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

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

### <span data-ttu-id="e4adc-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e4adc-134">-MainDefinitionFile</span></span>
<span data-ttu-id="e4adc-135">Główny plik służący do zadania.</span><span class="sxs-lookup"><span data-stu-id="e4adc-135">The main file used for the job.</span></span>
<span data-ttu-id="e4adc-136">na przykład " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="e4adc-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="e4adc-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4adc-137">-Name</span></span>
<span data-ttu-id="e4adc-138">Nazwa zadania usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="e4adc-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="e4adc-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="e4adc-139">-ReferenceFile</span></span>
<span data-ttu-id="e4adc-140">Dodatkowe pliki używane w celu odwołania w pliku definicji głównej.</span><span class="sxs-lookup"><span data-stu-id="e4adc-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="e4adc-141">Lista identyfikatorów URI magazynu rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="e4adc-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="e4adc-142">na przykład " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="e4adc-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="e4adc-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="e4adc-143">-SparkPoolName</span></span>
<span data-ttu-id="e4adc-144">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="e4adc-144">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="e4adc-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="e4adc-145">-SparkPoolObject</span></span>
<span data-ttu-id="e4adc-146">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="e4adc-146">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e4adc-147">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="e4adc-147">-WorkspaceName</span></span>
<span data-ttu-id="e4adc-148">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="e4adc-148">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e4adc-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4adc-149">-Confirm</span></span>
<span data-ttu-id="e4adc-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4adc-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4adc-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4adc-151">-WhatIf</span></span>
<span data-ttu-id="e4adc-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4adc-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4adc-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4adc-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4adc-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4adc-154">CommonParameters</span></span>
<span data-ttu-id="e4adc-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4adc-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4adc-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4adc-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4adc-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4adc-157">INPUTS</span></span>

### <span data-ttu-id="e4adc-158">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="e4adc-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="e4adc-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4adc-159">OUTPUTS</span></span>

### <span data-ttu-id="e4adc-160">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="e4adc-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="e4adc-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4adc-161">NOTES</span></span>

## <span data-ttu-id="e4adc-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4adc-162">RELATED LINKS</span></span>
