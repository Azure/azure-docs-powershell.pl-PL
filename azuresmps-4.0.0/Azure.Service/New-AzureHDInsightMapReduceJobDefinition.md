---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054882"
---
# <span data-ttu-id="860b0-101">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="860b0-101">New-AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="860b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="860b0-102">SYNOPSIS</span></span>
<span data-ttu-id="860b0-103">Definiuje nowe zadanie MapReduce.</span><span class="sxs-lookup"><span data-stu-id="860b0-103">Defines a new MapReduce job.</span></span>

## <span data-ttu-id="860b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="860b0-104">SYNTAX</span></span>

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="860b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="860b0-105">DESCRIPTION</span></span>
<span data-ttu-id="860b0-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="860b0-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="860b0-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="860b0-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="860b0-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="860b0-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="860b0-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="860b0-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="860b0-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="860b0-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="860b0-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="860b0-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="860b0-112">Polecenie cmdlet **New-AzureHDInsightMapReduceJobDefinition** definiuje nowe zadanie MapReduce, które ma być uruchamiane w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="860b0-112">The **New-AzureHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job to run on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="860b0-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="860b0-113">EXAMPLES</span></span>

### <span data-ttu-id="860b0-114">Przykład 1: Definiowanie zadania programu MapReduce, uruchamianie zadania i uzyskiwanie danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="860b0-114">Example 1: Define a MapReduce job, run the job, and get the output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="860b0-115">Pierwsze polecenie pobiera identyfikator bieżącej subskrypcji, a następnie zapisuje go w zmiennej $SubId.</span><span class="sxs-lookup"><span data-stu-id="860b0-115">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="860b0-116">Drugie polecenie przypisuje nazwę webcluster do zmiennej $Clustername.</span><span class="sxs-lookup"><span data-stu-id="860b0-116">The second command assigns the name MyCluster to the $Clustername variable.</span></span>

<span data-ttu-id="860b0-117">W trzecim poleceniu użyto polecenia cmdlet **New-AzureHDInsightMapReduceJobDefinition** w celu utworzenia MapReduce definicji zadania, a następnie zapisania jej w zmiennej $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="860b0-117">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then store it in the $WordCountJob variable.</span></span>

<span data-ttu-id="860b0-118">W czwartym poleceniu są wykonywane sekwencje operacji za pomocą następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="860b0-118">The fourth command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="860b0-119">**Start-AzureHDInsightJob** , aby uruchomić zadanie na $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="860b0-119">**Start-AzureHDInsightJob** to start the job on $ClusterName.</span></span> 
- <span data-ttu-id="860b0-120">**Poczekaj — AzureHDInsightJob** , aby poczekać na zakończenie zadania i wyświetlić postęp w kierunku ukończenia.</span><span class="sxs-lookup"><span data-stu-id="860b0-120">**Wait-AzureHDInsightJob** to wait for the job to finish and to display the progress toward completion.</span></span>
- <span data-ttu-id="860b0-121">**Get-AzureHDInsightJobOutput** , aby uzyskać dane wyjściowe zlecenia.</span><span class="sxs-lookup"><span data-stu-id="860b0-121">**Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="860b0-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="860b0-122">PARAMETERS</span></span>

### <span data-ttu-id="860b0-123">-Argumenty</span><span class="sxs-lookup"><span data-stu-id="860b0-123">-Arguments</span></span>
<span data-ttu-id="860b0-124">Określa tablicę argumentów dla zadania usługi Hadoop.</span><span class="sxs-lookup"><span data-stu-id="860b0-124">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="860b0-125">Argumenty są przekazywane jako argumenty wiersza polecenia dla każdego zadania.</span><span class="sxs-lookup"><span data-stu-id="860b0-125">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="860b0-126">-ClassName</span><span class="sxs-lookup"><span data-stu-id="860b0-126">-ClassName</span></span>
<span data-ttu-id="860b0-127">Określa nazwę klasy zadania w pliku archiwum Java (w formacie JAR).</span><span class="sxs-lookup"><span data-stu-id="860b0-127">Specifies the name of the job class in the Java Archive (JAR) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860b0-128">-Definiuje</span><span class="sxs-lookup"><span data-stu-id="860b0-128">-Defines</span></span>
<span data-ttu-id="860b0-129">Określa wartości konfiguracji usługi Hadoop, które mają zostać ustawione podczas uruchamiania zadania.</span><span class="sxs-lookup"><span data-stu-id="860b0-129">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="860b0-130">-Files</span><span class="sxs-lookup"><span data-stu-id="860b0-130">-Files</span></span>
<span data-ttu-id="860b0-131">Określa tablicę plików WASB, które są wymagane dla zadania.</span><span class="sxs-lookup"><span data-stu-id="860b0-131">Specifies an array of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="860b0-132">-JarFile</span><span class="sxs-lookup"><span data-stu-id="860b0-132">-JarFile</span></span>
<span data-ttu-id="860b0-133">Określa w pełni kwalifikowaną nazwę pliku JAR, który zawiera kod i zależności zadania MapReduce.</span><span class="sxs-lookup"><span data-stu-id="860b0-133">Specifies the fully qualified name of a JAR file that contains the code and dependencies of a MapReduce job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860b0-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="860b0-134">-JobName</span></span>
<span data-ttu-id="860b0-135">Określa nazwę zadania programu MapReduce.</span><span class="sxs-lookup"><span data-stu-id="860b0-135">Specifies the name of a MapReduce job.</span></span>
<span data-ttu-id="860b0-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="860b0-136">This parameter is optional.</span></span>
<span data-ttu-id="860b0-137">Jeśli ten parametr nie jest określony, zostanie wykorzystana wartość parametru *ClassName* .</span><span class="sxs-lookup"><span data-stu-id="860b0-137">If you do not specify this parameter, the value of the *ClassName* parameter is used.</span></span>

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

### <span data-ttu-id="860b0-138">-LibJars</span><span class="sxs-lookup"><span data-stu-id="860b0-138">-LibJars</span></span>
<span data-ttu-id="860b0-139">Określa tablicę LibJar odwołań do zadania.</span><span class="sxs-lookup"><span data-stu-id="860b0-139">Specifies an array of LibJar references of the job.</span></span>

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

### <span data-ttu-id="860b0-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="860b0-140">-Profile</span></span>
<span data-ttu-id="860b0-141">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="860b0-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="860b0-142">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="860b0-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="860b0-143">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="860b0-143">-StatusFolder</span></span>
<span data-ttu-id="860b0-144">Określa lokalizację folderu zawierającego wyniki standardowego wyjścia i błędów dla zadania, w tym kod wyjścia i dzienniki zadań.</span><span class="sxs-lookup"><span data-stu-id="860b0-144">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="860b0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860b0-145">CommonParameters</span></span>
<span data-ttu-id="860b0-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="860b0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860b0-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="860b0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860b0-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="860b0-148">INPUTS</span></span>

## <span data-ttu-id="860b0-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="860b0-149">OUTPUTS</span></span>

## <span data-ttu-id="860b0-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="860b0-150">NOTES</span></span>

## <span data-ttu-id="860b0-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="860b0-151">RELATED LINKS</span></span>

[<span data-ttu-id="860b0-152">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="860b0-152">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="860b0-153">Nowe — AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="860b0-153">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="860b0-154">Nowe — AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="860b0-154">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="860b0-155">Nowe — AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="860b0-155">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="860b0-156">Start — AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="860b0-156">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="860b0-157">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="860b0-157">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


