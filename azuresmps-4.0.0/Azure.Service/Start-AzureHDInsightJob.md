---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0308c3ff5bee358a82d74d452784f42c69bc7c32
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054390"
---
# <span data-ttu-id="82a34-101">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="82a34-101">Start-AzureHDInsightJob</span></span>

## <span data-ttu-id="82a34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82a34-102">SYNOPSIS</span></span>
<span data-ttu-id="82a34-103">Rozpoczynanie zadania usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="82a34-103">Starts an HDInsight job.</span></span>

## <span data-ttu-id="82a34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82a34-104">SYNTAX</span></span>

### <span data-ttu-id="82a34-105">Uruchamianie jobDetails w klastrze usługi HDInsight (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="82a34-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82a34-106">Uruchamianie jobDetails w klastrze usługi HDInsight (z określonymi poświadczeniami subskrypcji)</span><span class="sxs-lookup"><span data-stu-id="82a34-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82a34-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82a34-107">DESCRIPTION</span></span>
<span data-ttu-id="82a34-108">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="82a34-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="82a34-109">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="82a34-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="82a34-110">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="82a34-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="82a34-111">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="82a34-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="82a34-112">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="82a34-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="82a34-113">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="82a34-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="82a34-114">Polecenie cmdlet **Start-AzureHDInsightJob** uruchamia zdefiniowane zadanie usługi Azure HDInsight dla określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="82a34-114">The **Start-AzureHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="82a34-115">Uruchomienie zadania może być zadaniem MapReduce, zadaniem strumieniowym, zadaniem w ramach usługi Hive lub zadaniem świni.</span><span class="sxs-lookup"><span data-stu-id="82a34-115">The job to start can be a MapReduce job, a streaming job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="82a34-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82a34-116">EXAMPLES</span></span>

### <span data-ttu-id="82a34-117">Przykład 1. Uruchom zadanie usługi HDInsight</span><span class="sxs-lookup"><span data-stu-id="82a34-117">Example 1: Start an HDInsight job</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="82a34-118">Pierwsze polecenie pobiera bieżący identyfikator subskrypcji, a następnie zapisuje go w zmiennej $SubId.</span><span class="sxs-lookup"><span data-stu-id="82a34-118">The first command gets the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="82a34-119">Drugie polecenie przypisuje nazwę Cluster01 do zmiennej $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="82a34-119">The second command assigns the name Cluster01 to the $ClusterName variable.</span></span>

<span data-ttu-id="82a34-120">W trzecim poleceniu użyto polecenia cmdlet **New-AzureHDInsightMapReduceJobDefinition** w celu utworzenia MapReduce definicji zadania, a następnie zapisanie go w zmiennej $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="82a34-120">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="82a34-121">W poleceniu ostatnim jest używany operator potoku umożliwiający przekazanie $WordCountJob do polecenia cmdlet **Start-AzureHDInsightJob** w celu uruchomienia zadania.</span><span class="sxs-lookup"><span data-stu-id="82a34-121">The final command uses the pipeline operator to pass the $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="82a34-122">Po uruchomieniu zadania jest ono przekazywane do polecenia cmdlet **wait-AzureHDInsightJob** , które oczekuje na ukończenie zadania przed przekazaniem go do polecenia cmdlet **Get-AzureHDInsightJobOutput** w celu uzyskania wyników zadania.</span><span class="sxs-lookup"><span data-stu-id="82a34-122">After the job starts, it is passed to the **Wait-AzureHDInsightJob** cmdlet, which waits for the job to complete before passing it to the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="82a34-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82a34-123">PARAMETERS</span></span>

### <span data-ttu-id="82a34-124">-Certificate</span><span class="sxs-lookup"><span data-stu-id="82a34-124">-Certificate</span></span>
<span data-ttu-id="82a34-125">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="82a34-125">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a34-126">-Cluster</span><span class="sxs-lookup"><span data-stu-id="82a34-126">-Cluster</span></span>
<span data-ttu-id="82a34-127">Określa klaster.</span><span class="sxs-lookup"><span data-stu-id="82a34-127">Specifies a cluster.</span></span>
<span data-ttu-id="82a34-128">To polecenie cmdlet rozpoczyna zadanie w klastrze, którego ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="82a34-128">This cmdlet starts a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82a34-129">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="82a34-129">-Credential</span></span>
<span data-ttu-id="82a34-130">Określa poświadczenia klastra umożliwiające bezpośrednie uzyskiwanie dostępu do klastra w protokole HTTP.</span><span class="sxs-lookup"><span data-stu-id="82a34-130">Specifies cluster credentials for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="82a34-131">Możesz określić ten parametr zamiast parametru *abonamentu* , aby uwierzytelnić dostęp do klastra.</span><span class="sxs-lookup"><span data-stu-id="82a34-131">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a34-132">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="82a34-132">-Endpoint</span></span>
<span data-ttu-id="82a34-133">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82a34-133">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="82a34-134">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="82a34-134">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a34-135">-HostedService</span><span class="sxs-lookup"><span data-stu-id="82a34-135">-HostedService</span></span>
<span data-ttu-id="82a34-136">Określa obszar nazw usługi HDInsight, jeśli nie chcesz używać domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="82a34-136">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a34-137">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="82a34-137">-IgnoreSslErrors</span></span>
<span data-ttu-id="82a34-138">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="82a34-138">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a34-139">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="82a34-139">-JobDefinition</span></span>
<span data-ttu-id="82a34-140">Określa punkt końcowy, który ma być używany podczas nawiązywania połączenia z usługą Microsoft Azure, jeśli punkt końcowy jest inny niż domyślny.</span><span class="sxs-lookup"><span data-stu-id="82a34-140">Specifies the endpoint to use when connecting to Microsoft Azure if the endpoint is different from the default.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82a34-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="82a34-141">-Profile</span></span>
<span data-ttu-id="82a34-142">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82a34-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82a34-143">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="82a34-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82a34-144">-Subscription</span><span class="sxs-lookup"><span data-stu-id="82a34-144">-Subscription</span></span>
<span data-ttu-id="82a34-145">Określa abonament.</span><span class="sxs-lookup"><span data-stu-id="82a34-145">Specifies a subscription.</span></span>
<span data-ttu-id="82a34-146">To polecenie cmdlet rozpoczyna zadanie dla subskrypcji, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="82a34-146">This cmdlet starts a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a34-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a34-147">CommonParameters</span></span>
<span data-ttu-id="82a34-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a34-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a34-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a34-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a34-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82a34-150">INPUTS</span></span>

## <span data-ttu-id="82a34-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82a34-151">OUTPUTS</span></span>

## <span data-ttu-id="82a34-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82a34-152">NOTES</span></span>

## <span data-ttu-id="82a34-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82a34-153">RELATED LINKS</span></span>

[<span data-ttu-id="82a34-154">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="82a34-154">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="82a34-155">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="82a34-155">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="82a34-156">Nowe — AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="82a34-156">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="82a34-157">Zatrzymaj — AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="82a34-157">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="82a34-158">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="82a34-158">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


