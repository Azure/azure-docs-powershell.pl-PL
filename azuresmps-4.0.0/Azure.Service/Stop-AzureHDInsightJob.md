---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054730"
---
# <span data-ttu-id="d187d-101">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d187d-101">Stop-AzureHDInsightJob</span></span>

## <span data-ttu-id="d187d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d187d-102">SYNOPSIS</span></span>
<span data-ttu-id="d187d-103">Zatrzymuje zadanie usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d187d-103">Stops an HDInsight job.</span></span>

## <span data-ttu-id="d187d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d187d-104">SYNTAX</span></span>

### <span data-ttu-id="d187d-105">Uruchamianie jobDetails w klastrze usługi HDInsight (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d187d-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d187d-106">Uruchamianie jobDetails w klastrze usługi HDInsight (z określonymi poświadczeniami subskrypcji)</span><span class="sxs-lookup"><span data-stu-id="d187d-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d187d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d187d-107">DESCRIPTION</span></span>
<span data-ttu-id="d187d-108">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="d187d-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="d187d-109">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="d187d-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="d187d-110">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d187d-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="d187d-111">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="d187d-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="d187d-112">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="d187d-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="d187d-113">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d187d-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="d187d-114">Polecenie cmdlet **stop-AzureHDInsightJob** zatrzymuje zadanie usługi Azure HDInsight w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="d187d-114">The **Stop-AzureHDInsightJob** cmdlet stops an Azure HDInsight job on the specified cluster.</span></span>

## <span data-ttu-id="d187d-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d187d-115">EXAMPLES</span></span>

## <span data-ttu-id="d187d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d187d-116">PARAMETERS</span></span>

### <span data-ttu-id="d187d-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="d187d-117">-Certificate</span></span>
<span data-ttu-id="d187d-118">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d187d-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="d187d-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="d187d-119">-Cluster</span></span>
<span data-ttu-id="d187d-120">Określa klaster.</span><span class="sxs-lookup"><span data-stu-id="d187d-120">Specifies a cluster.</span></span>
<span data-ttu-id="d187d-121">To polecenie cmdlet zatrzymuje zadanie uruchomione w klastrze, którego ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d187d-121">This cmdlet stops a job that runs on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d187d-122">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="d187d-122">-Credential</span></span>
<span data-ttu-id="d187d-123">Określa poświadczenia, których należy użyć, aby uzyskać bezpośredni dostęp do klastra w protokole HTTP.</span><span class="sxs-lookup"><span data-stu-id="d187d-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="d187d-124">Możesz określić ten parametr zamiast parametru *abonamentu* , aby uwierzytelnić dostęp do klastra.</span><span class="sxs-lookup"><span data-stu-id="d187d-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

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

### <span data-ttu-id="d187d-125">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="d187d-125">-Endpoint</span></span>
<span data-ttu-id="d187d-126">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d187d-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="d187d-127">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="d187d-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="d187d-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="d187d-128">-HostedService</span></span>
<span data-ttu-id="d187d-129">Określa obszar nazw usługi HDInsight, jeśli nie chcesz używać domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="d187d-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="d187d-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="d187d-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="d187d-131">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="d187d-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="d187d-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="d187d-132">-JobId</span></span>
<span data-ttu-id="d187d-133">Określa identyfikator zadania usługi HDInsight do zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="d187d-133">Specifies the ID of the HDInsight job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d187d-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="d187d-134">-Profile</span></span>
<span data-ttu-id="d187d-135">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d187d-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d187d-136">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d187d-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d187d-137">-Subscription</span><span class="sxs-lookup"><span data-stu-id="d187d-137">-Subscription</span></span>
<span data-ttu-id="d187d-138">Określa abonament.</span><span class="sxs-lookup"><span data-stu-id="d187d-138">Specifies a subscription.</span></span>
<span data-ttu-id="d187d-139">To polecenie cmdlet zatrzymuje zadanie dla subskrypcji, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d187d-139">This cmdlet stops a job for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="d187d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d187d-140">CommonParameters</span></span>
<span data-ttu-id="d187d-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d187d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d187d-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d187d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d187d-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d187d-143">INPUTS</span></span>

## <span data-ttu-id="d187d-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d187d-144">OUTPUTS</span></span>

## <span data-ttu-id="d187d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d187d-145">NOTES</span></span>

## <span data-ttu-id="d187d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d187d-146">RELATED LINKS</span></span>

[<span data-ttu-id="d187d-147">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d187d-147">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="d187d-148">Start — AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d187d-148">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="d187d-149">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d187d-149">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


