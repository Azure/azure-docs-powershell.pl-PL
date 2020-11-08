---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 824F6302-6285-4AEC-A63C-E2519DE4C7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2597d66e87de682bbf5702085612f7338d75deac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054975"
---
# <span data-ttu-id="44996-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="44996-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="44996-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44996-102">SYNOPSIS</span></span>
<span data-ttu-id="44996-103">Definiuje nowe zadanie MapReduce strumieniowego.</span><span class="sxs-lookup"><span data-stu-id="44996-103">Defines a new streaming MapReduce job.</span></span>

## <span data-ttu-id="44996-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44996-104">SYNTAX</span></span>

```
New-AzureHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-CmdEnv <String[]>]
 [-Combiner <String>] [-Defines <Hashtable>] [-Files <String[]>] [-InputPath <String>] [-JobName <String>]
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="44996-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44996-105">DESCRIPTION</span></span>
<span data-ttu-id="44996-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="44996-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="44996-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="44996-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="44996-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="44996-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="44996-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="44996-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="44996-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="44996-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="44996-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="44996-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="44996-112">Polecenie cmdlet **New-AzureHDInsightStreamingMapReduceJobDefinition** definiuje nowy obiekt definicji zadania reprezentujący parametry zadania strumieniowego usługi Hadoop.</span><span class="sxs-lookup"><span data-stu-id="44996-112">The **New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet defines a new job definition object that represents the parameters of a Hadoop streaming job.</span></span>

## <span data-ttu-id="44996-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44996-113">EXAMPLES</span></span>

### <span data-ttu-id="44996-114">Przykład 1: Tworzenie definicji zadania MapReduce strumieniowego</span><span class="sxs-lookup"><span data-stu-id="44996-114">Example 1: Create a streaming MapReduce job definition</span></span>
```
PS C:\>$StreamingWordCount = New-AzureHDInsightStreamingMapReduceJobDefinition -Files "/Example/Apps/WordCount.exe", "/Example/Apps/Cat.exe" -InputPath "/Example/Data/Gutenberg/Davinci.txt" -OutputPath "/Example/Data/StreamingOutput/WordCount.txt" -Mapper "Cat.exe" -Reducer "WordCount.exe"
```

<span data-ttu-id="44996-115">To polecenie tworzy określoną definicję zadania MapReduce strumieniowego, a następnie zapisuje ją w zmiennej $StreamingWordCount.</span><span class="sxs-lookup"><span data-stu-id="44996-115">This command creates the specified streaming MapReduce job definition, and then stores it in the $StreamingWordCount variable.</span></span>

## <span data-ttu-id="44996-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44996-116">PARAMETERS</span></span>

### <span data-ttu-id="44996-117">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="44996-117">-Arguments</span></span>
<span data-ttu-id="44996-118">Określa tablicę argumentów dla zadania usługi Hadoop.</span><span class="sxs-lookup"><span data-stu-id="44996-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="44996-119">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="44996-119">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44996-120">-CmdEnv</span><span class="sxs-lookup"><span data-stu-id="44996-120">-CmdEnv</span></span>
<span data-ttu-id="44996-121">Określa tablicę zmiennych środowiskowych wiersza polecenia, które można ustawić podczas uruchamiania zadania w węzłach danych.</span><span class="sxs-lookup"><span data-stu-id="44996-121">Specifies an array of command-line environment variables to set when a job runs on data nodes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44996-122">-Złączer</span><span class="sxs-lookup"><span data-stu-id="44996-122">-Combiner</span></span>
<span data-ttu-id="44996-123">Określa nazwę pliku programu do łączenia.</span><span class="sxs-lookup"><span data-stu-id="44996-123">Specifies a Combiner file name.</span></span>

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

### <span data-ttu-id="44996-124">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="44996-124">-Defines</span></span>
<span data-ttu-id="44996-125">Określa wartości konfiguracji usługi Hadoop, które mają zostać ustawione podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="44996-125">Specifies Hadoop configuration values to set when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44996-126">-Files</span><span class="sxs-lookup"><span data-stu-id="44996-126">-Files</span></span>
<span data-ttu-id="44996-127">Określa tablicę plików, które są wymagane dla zadania.</span><span class="sxs-lookup"><span data-stu-id="44996-127">Specifies an array of files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44996-128">-InputPath</span><span class="sxs-lookup"><span data-stu-id="44996-128">-InputPath</span></span>
<span data-ttu-id="44996-129">Określa ścieżkę WASB do plików wejściowych.</span><span class="sxs-lookup"><span data-stu-id="44996-129">Specifies the WASB path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Input

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44996-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="44996-130">-JobName</span></span>
<span data-ttu-id="44996-131">Określa nazwę nowej definicji zadania MapReduce.</span><span class="sxs-lookup"><span data-stu-id="44996-131">Specifies the name of the new MapReduce job definition.</span></span>
<span data-ttu-id="44996-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="44996-132">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44996-133">-Maper</span><span class="sxs-lookup"><span data-stu-id="44996-133">-Mapper</span></span>
<span data-ttu-id="44996-134">Określa nazwę pliku mapera.</span><span class="sxs-lookup"><span data-stu-id="44996-134">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="44996-135">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="44996-135">-OutputPath</span></span>
<span data-ttu-id="44996-136">Określa ścieżkę WASB dla wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="44996-136">Specifies the WASB path for the job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Output

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44996-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="44996-137">-Profile</span></span>
<span data-ttu-id="44996-138">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44996-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44996-139">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="44996-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44996-140">-Zmniejszenie</span><span class="sxs-lookup"><span data-stu-id="44996-140">-Reducer</span></span>
<span data-ttu-id="44996-141">Określa nazwę pliku z ograniczeniami.</span><span class="sxs-lookup"><span data-stu-id="44996-141">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="44996-142">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="44996-142">-StatusFolder</span></span>
<span data-ttu-id="44996-143">Określa folder zawierający wyniki standardowego wyjścia i błędów dla zadania, w tym kod wyjścia i dzienniki zadań.</span><span class="sxs-lookup"><span data-stu-id="44996-143">Specifies the folder that contains the standard outputs and error outputs for the job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="44996-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44996-144">CommonParameters</span></span>
<span data-ttu-id="44996-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44996-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44996-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44996-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44996-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44996-147">INPUTS</span></span>

## <span data-ttu-id="44996-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44996-148">OUTPUTS</span></span>

## <span data-ttu-id="44996-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44996-149">NOTES</span></span>

## <span data-ttu-id="44996-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44996-150">RELATED LINKS</span></span>

[<span data-ttu-id="44996-151">Nowe — AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="44996-151">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="44996-152">Nowe — AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="44996-152">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="44996-153">Nowe — AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="44996-153">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="44996-154">Nowe — AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="44996-154">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)


