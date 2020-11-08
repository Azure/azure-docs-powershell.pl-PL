---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054606"
---
# <span data-ttu-id="42b33-101">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="42b33-101">Get-AzureHDInsightJobOutput</span></span>

## <span data-ttu-id="42b33-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42b33-102">SYNOPSIS</span></span>
<span data-ttu-id="42b33-103">Pobiera dane wyjściowe dziennika zadania.</span><span class="sxs-lookup"><span data-stu-id="42b33-103">Gets the log output for a job.</span></span>

## <span data-ttu-id="42b33-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42b33-104">SYNTAX</span></span>

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="42b33-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42b33-105">DESCRIPTION</span></span>
<span data-ttu-id="42b33-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="42b33-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="42b33-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="42b33-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="42b33-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42b33-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="42b33-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz Tworzenie klastrów opartych na systemie Linux w [usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="42b33-109">For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in [HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="42b33-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="42b33-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="42b33-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="42b33-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="42b33-112">Polecenie cmdlet **Get-AzureHDInsightJobOutput** pobiera dane wyjściowe dziennika zadania z konta magazynu skojarzonego z klastrem.</span><span class="sxs-lookup"><span data-stu-id="42b33-112">The **Get-AzureHDInsightJobOutput** cmdlet gets the log output for a job from the storage account associated with a cluster.</span></span>
<span data-ttu-id="42b33-113">Możesz uzyskać różne typy dzienników zadań, w tym standardowe dane wyjściowe, błąd standardowy, dzienniki zadań i podsumowanie dzienników zadań.</span><span class="sxs-lookup"><span data-stu-id="42b33-113">You can get various types of job logs including standard output, standard error, task logs, and a summary of the task logs.</span></span>

## <span data-ttu-id="42b33-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42b33-114">EXAMPLES</span></span>

### <span data-ttu-id="42b33-115">Przykład 1: pobieranie wyników zlecenia</span><span class="sxs-lookup"><span data-stu-id="42b33-115">Example 1: Get job output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

<span data-ttu-id="42b33-116">Pierwsze polecenie pobiera identyfikator bieżącej subskrypcji, a następnie zapisuje go w zmiennej $SubId.</span><span class="sxs-lookup"><span data-stu-id="42b33-116">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="42b33-117">Drugie polecenie zapisuje nazwę moja Cluster w zmiennej $Clustername.</span><span class="sxs-lookup"><span data-stu-id="42b33-117">The second command stores the name MyCluster in the $Clustername variable.</span></span>

<span data-ttu-id="42b33-118">Trzecie polecenie tworzy definicję zadania MapReduce, a następnie zapisuje ją w zmiennej $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="42b33-118">The third command creates a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>
<span data-ttu-id="42b33-119">Polecenie przekazanie zadania w $WordCountJob do polecenia cmdlet **Start-AzureHDInsightJob** w celu uruchomienia zadania.</span><span class="sxs-lookup"><span data-stu-id="42b33-119">The command passes the job in $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="42b33-120">Przekazuje również $WordCountJob polecenia cmdlet **wait-AzureHDInsightJob** w celu zaczekania na zakończenie zadania, a następnie w celu pobrania danych wyjściowych zadania jest używana funkcja **Get-AzureHDInsightJobOutput** .</span><span class="sxs-lookup"><span data-stu-id="42b33-120">It also passes $WordCountJob to the **Wait-AzureHDInsightJob** cmdlet to wait for the job to finish, and then it uses **Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="42b33-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42b33-121">PARAMETERS</span></span>

### <span data-ttu-id="42b33-122">-Certificate</span><span class="sxs-lookup"><span data-stu-id="42b33-122">-Certificate</span></span>
<span data-ttu-id="42b33-123">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42b33-123">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-124">-Cluster</span><span class="sxs-lookup"><span data-stu-id="42b33-124">-Cluster</span></span>
<span data-ttu-id="42b33-125">Określa klaster.</span><span class="sxs-lookup"><span data-stu-id="42b33-125">Specifies a cluster.</span></span>
<span data-ttu-id="42b33-126">To polecenie cmdlet pobiera dzienniki zadań z klastra, którego ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="42b33-126">This cmdlet gets job logs from the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-127">-DownloadTaskLogs</span><span class="sxs-lookup"><span data-stu-id="42b33-127">-DownloadTaskLogs</span></span>
<span data-ttu-id="42b33-128">Wskazuje, że to polecenie cmdlet pobiera dzienniki zadań zadania.</span><span class="sxs-lookup"><span data-stu-id="42b33-128">Indicates that this cmdlet gets the task logs for a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-129">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="42b33-129">-Endpoint</span></span>
<span data-ttu-id="42b33-130">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42b33-130">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="42b33-131">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="42b33-131">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-132">-HostedService</span><span class="sxs-lookup"><span data-stu-id="42b33-132">-HostedService</span></span>
<span data-ttu-id="42b33-133">Określa obszar nazw usługi HDInsight, jeśli nie chcesz używać domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="42b33-133">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-134">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="42b33-134">-IgnoreSslErrors</span></span>
<span data-ttu-id="42b33-135">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="42b33-135">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-136">-JobId</span><span class="sxs-lookup"><span data-stu-id="42b33-136">-JobId</span></span>
<span data-ttu-id="42b33-137">Określa identyfikator zadania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="42b33-137">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="42b33-138">-Profile</span></span>
<span data-ttu-id="42b33-139">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42b33-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42b33-140">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="42b33-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42b33-141">-StandardError</span><span class="sxs-lookup"><span data-stu-id="42b33-141">-StandardError</span></span>
<span data-ttu-id="42b33-142">Wskazuje, że to polecenie cmdlet pobiera dane wyjściowe StdErr zadania.</span><span class="sxs-lookup"><span data-stu-id="42b33-142">Indicates that this cmdlet gets the StdErr output of a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-143">-StandardOutput</span><span class="sxs-lookup"><span data-stu-id="42b33-143">-StandardOutput</span></span>
<span data-ttu-id="42b33-144">Wskazuje, że to polecenie cmdlet pobiera dane wyjściowe zadania w SdtOut.</span><span class="sxs-lookup"><span data-stu-id="42b33-144">Indicates that this cmdlet gets the SdtOut output of a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-145">-Subscription</span><span class="sxs-lookup"><span data-stu-id="42b33-145">-Subscription</span></span>
<span data-ttu-id="42b33-146">Określa subskrypcję zawierającą klaster usługi HDInsight do pobrania.</span><span class="sxs-lookup"><span data-stu-id="42b33-146">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-147">-TaskLogsDirectory</span><span class="sxs-lookup"><span data-stu-id="42b33-147">-TaskLogsDirectory</span></span>
<span data-ttu-id="42b33-148">Określa folder lokalny, w którym mają być przechowywane dzienniki zadań.</span><span class="sxs-lookup"><span data-stu-id="42b33-148">Specifies a local folder in which to store tasks logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-149">-TaskSummary</span><span class="sxs-lookup"><span data-stu-id="42b33-149">-TaskSummary</span></span>
<span data-ttu-id="42b33-150">Wskazuje, że te polecenia cmdlet pobierają podsumowanie dziennika zadań.</span><span class="sxs-lookup"><span data-stu-id="42b33-150">Indicates that this cmdlets gets the task log summary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b33-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b33-151">CommonParameters</span></span>
<span data-ttu-id="42b33-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b33-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b33-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b33-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b33-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42b33-154">INPUTS</span></span>

## <span data-ttu-id="42b33-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42b33-155">OUTPUTS</span></span>

## <span data-ttu-id="42b33-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42b33-156">NOTES</span></span>

## <span data-ttu-id="42b33-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42b33-157">RELATED LINKS</span></span>

[<span data-ttu-id="42b33-158">Nowe — AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="42b33-158">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="42b33-159">Start — AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="42b33-159">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="42b33-160">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="42b33-160">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)
