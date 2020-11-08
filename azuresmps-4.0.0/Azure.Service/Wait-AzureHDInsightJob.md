---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054798"
---
# <span data-ttu-id="18815-101">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="18815-101">Wait-AzureHDInsightJob</span></span>

## <span data-ttu-id="18815-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18815-102">SYNOPSIS</span></span>
<span data-ttu-id="18815-103">Oczekuje na ukończenie lub niepowodzenie zadania usługi HDInsight i wyświetla postęp zadania.</span><span class="sxs-lookup"><span data-stu-id="18815-103">Awaits the completion or failure of an HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="18815-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18815-104">SYNTAX</span></span>

### <span data-ttu-id="18815-105">Pobieranie historii jobDetails klastra usługi HDInsight (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="18815-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="18815-106">Pobieranie historii jobDetails klastra usługi HDInsight (z określonymi poświadczeniami subskrypcji)</span><span class="sxs-lookup"><span data-stu-id="18815-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="18815-107">Zadanie oczekiwania z identyfikatorem JobId w klastrze usługi HDInsight</span><span class="sxs-lookup"><span data-stu-id="18815-107">Wait Job with JobId on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="18815-108">Zadanie oczekiwania zadania w klastrze usługi HDInsight</span><span class="sxs-lookup"><span data-stu-id="18815-108">Wait Job with Job on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="18815-109">Opis</span><span class="sxs-lookup"><span data-stu-id="18815-109">DESCRIPTION</span></span>
<span data-ttu-id="18815-110">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="18815-110">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="18815-111">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="18815-111">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="18815-112">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="18815-112">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="18815-113">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="18815-113">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="18815-114">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="18815-114">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="18815-115">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="18815-115">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="18815-116">Polecenie cmdlet **wait-AzureHDInsightJob** oczekuje na zakończenie lub niepowodzenie zadania usługi Azure HDInsight i wyświetla postęp zadania.</span><span class="sxs-lookup"><span data-stu-id="18815-116">The **Wait-AzureHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="18815-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18815-117">EXAMPLES</span></span>

### <span data-ttu-id="18815-118">Przykład 1. Uruchom zadanie i poczekaj na jego ukończenie</span><span class="sxs-lookup"><span data-stu-id="18815-118">Example 1: Run a job and wait for it to complete</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="18815-119">Pierwsze polecenie pobiera bieżący identyfikator subskrypcji platformy Azure, a następnie zapisuje go w zmiennej $SubId.</span><span class="sxs-lookup"><span data-stu-id="18815-119">The first command gets the current Azure subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="18815-120">Drugie polecenie pobiera określony klaster, a następnie zapisuje go w zmiennej $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="18815-120">The second command gets the specified cluster, and then stores it in the $ClusterName variable.</span></span>

<span data-ttu-id="18815-121">W trzecim poleceniu użyto polecenia cmdlet **New-AzureHDInsightMapReduceJobDefinition** w celu utworzenia MapReduce definicji zadania, a następnie zapisanie go w zmiennej $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="18815-121">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="18815-122">W czwartym poleceniu użyto kilku poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="18815-122">The fourth command uses several cmdlets in sequence:</span></span> 

- <span data-ttu-id="18815-123">Używa operatora potoku w celu przekazania $WordCountJob do polecenia cmdlet **Start-AzureHDInsightJob** w celu uruchomienia zadania.</span><span class="sxs-lookup"><span data-stu-id="18815-123">It uses the pipeline operator to pass $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span> 
- <span data-ttu-id="18815-124">Zadanie jest przekazywane do polecenia cmdlet **wait-AzureHDInsightJob** w celu poczekania na wykonanie zadania w ciągu 3600 sekund.</span><span class="sxs-lookup"><span data-stu-id="18815-124">The job is passed to the **Wait-AzureHDInsightJob** cmdlet to wait 3600 seconds for the job to complete.</span></span> 
- <span data-ttu-id="18815-125">Jeśli zadanie zostanie zakończone, polecenie Użyj polecenia cmdlet **Get-AzureHDInsightJobOutput** w celu uzyskania danych wyjściowych zadania.</span><span class="sxs-lookup"><span data-stu-id="18815-125">If the job completes, the command uses the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="18815-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18815-126">PARAMETERS</span></span>

### <span data-ttu-id="18815-127">-Certificate</span><span class="sxs-lookup"><span data-stu-id="18815-127">-Certificate</span></span>
<span data-ttu-id="18815-128">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="18815-128">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18815-129">-Cluster</span><span class="sxs-lookup"><span data-stu-id="18815-129">-Cluster</span></span>
<span data-ttu-id="18815-130">Określa klaster.</span><span class="sxs-lookup"><span data-stu-id="18815-130">Specifies a cluster.</span></span>
<span data-ttu-id="18815-131">To polecenie cmdlet oczekuje na zadanie w klastrze, którego ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="18815-131">This cmdlet waits for a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18815-132">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="18815-132">-Credential</span></span>
<span data-ttu-id="18815-133">Określa poświadczenia, których należy użyć, aby uzyskać bezpośredni dostęp do klastra w protokole HTTP.</span><span class="sxs-lookup"><span data-stu-id="18815-133">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="18815-134">Możesz określić ten parametr zamiast parametru *abonamentu* , aby uwierzytelnić dostęp do klastra.</span><span class="sxs-lookup"><span data-stu-id="18815-134">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18815-135">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="18815-135">-Endpoint</span></span>
<span data-ttu-id="18815-136">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18815-136">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="18815-137">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="18815-137">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18815-138">-HostedService</span><span class="sxs-lookup"><span data-stu-id="18815-138">-HostedService</span></span>
<span data-ttu-id="18815-139">Określa obszar nazw usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18815-139">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="18815-140">Jeśli ten parametr nie zostanie określony, zostanie wykorzystana domyślna przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="18815-140">If you do not specify this parameter, the default namespace is used.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18815-141">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="18815-141">-IgnoreSslErrors</span></span>
<span data-ttu-id="18815-142">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="18815-142">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18815-143">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="18815-143">-Job</span></span>
<span data-ttu-id="18815-144">Określa zadanie usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18815-144">Specifies an Azure HDInsight job.</span></span>

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18815-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="18815-145">-JobId</span></span>
<span data-ttu-id="18815-146">Określa identyfikator zadania, na który należy czekać.</span><span class="sxs-lookup"><span data-stu-id="18815-146">Specifies the ID of the job to wait for.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18815-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="18815-147">-Profile</span></span>
<span data-ttu-id="18815-148">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18815-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="18815-149">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="18815-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="18815-150">-Subscription</span><span class="sxs-lookup"><span data-stu-id="18815-150">-Subscription</span></span>
<span data-ttu-id="18815-151">Określa abonament.</span><span class="sxs-lookup"><span data-stu-id="18815-151">Specifies a subscription.</span></span>
<span data-ttu-id="18815-152">To polecenie cmdlet oczekuje na zadanie subskrypcji, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="18815-152">This cmdlet waits for a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18815-153">-WaitTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="18815-153">-WaitTimeoutInSeconds</span></span>
<span data-ttu-id="18815-154">Określa limit czasu (w sekundach) dla operacji oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="18815-154">Specifies the time-out, in seconds, for the wait operation.</span></span>
<span data-ttu-id="18815-155">Jeśli limit czasu upływa przed zakończeniem zadania, polecenie cmdlet przestanie działać.</span><span class="sxs-lookup"><span data-stu-id="18815-155">If the time-out expires before the job completes, the cmdlet ceases to run.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18815-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18815-156">CommonParameters</span></span>
<span data-ttu-id="18815-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18815-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18815-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18815-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18815-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18815-159">INPUTS</span></span>

## <span data-ttu-id="18815-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18815-160">OUTPUTS</span></span>

## <span data-ttu-id="18815-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18815-161">NOTES</span></span>

## <span data-ttu-id="18815-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18815-162">RELATED LINKS</span></span>

[<span data-ttu-id="18815-163">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="18815-163">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="18815-164">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="18815-164">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="18815-165">Start — AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="18815-165">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="18815-166">Zatrzymaj — AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="18815-166">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)


