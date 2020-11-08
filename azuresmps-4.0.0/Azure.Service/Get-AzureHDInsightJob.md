---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3E3C9626-7AED-4B15-93D0-0B79AD17A834
online version: ''
schema: 2.0.0
ms.openlocfilehash: de4b768dbc6c97e84bccd4c8e0ef42f6f81a5b31
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055316"
---
# <span data-ttu-id="8ccb6-101">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8ccb6-101">Get-AzureHDInsightJob</span></span>

## <span data-ttu-id="8ccb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ccb6-102">SYNOPSIS</span></span>
<span data-ttu-id="8ccb6-103">Pobiera zadania usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-103">Gets HDInsight jobs.</span></span>

## <span data-ttu-id="8ccb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ccb6-104">SYNTAX</span></span>

### <span data-ttu-id="8ccb6-105">Pobieranie historii jobDetails klastra usługi HDInsight (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8ccb6-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Get-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] [-IgnoreSslErrors <Boolean>]
 [-JobId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8ccb6-106">Pobieranie historii jobDetails klastra usługi HDInsight (z określonymi poświadczeniami subskrypcji)</span><span class="sxs-lookup"><span data-stu-id="8ccb6-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Get-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] [-JobId <String>] [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8ccb6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8ccb6-107">DESCRIPTION</span></span>
<span data-ttu-id="8ccb6-108">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8ccb6-109">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8ccb6-110">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8ccb6-111">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="8ccb6-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8ccb6-112">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="8ccb6-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8ccb6-113">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8ccb6-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8ccb6-114">Polecenie cmdlet **Get-AzureHDInsightJob** pobiera ostatnie zadania usługi Azure HDInsight dla określonego klastra i wyświetla je w odwrotnej kolejności chronologicznej.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-114">The **Get-AzureHDInsightJob** cmdlet gets recent Azure HDInsight jobs for a specified cluster and displays them in reverse chronological order.</span></span>

## <span data-ttu-id="8ccb6-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ccb6-115">EXAMPLES</span></span>

## <span data-ttu-id="8ccb6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ccb6-116">PARAMETERS</span></span>

### <span data-ttu-id="8ccb6-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="8ccb6-117">-Certificate</span></span>
<span data-ttu-id="8ccb6-118">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="8ccb6-119">-Cluster</span><span class="sxs-lookup"><span data-stu-id="8ccb6-119">-Cluster</span></span>
<span data-ttu-id="8ccb6-120">Określa klaster.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-120">Specifies a cluster.</span></span>
<span data-ttu-id="8ccb6-121">To polecenie cmdlet umożliwia wykonywanie zadań usługi HDInsight uruchomionych w klastrze, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-121">This cmdlet gets HDInsight jobs that run on the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="8ccb6-122">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="8ccb6-122">-Credential</span></span>
<span data-ttu-id="8ccb6-123">Określa poświadczenia, których należy użyć, aby uzyskać bezpośredni dostęp do klastra w protokole HTTP.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="8ccb6-124">Możesz określić ten parametr zamiast parametru *abonamentu* , aby uwierzytelnić dostęp do klastra.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ccb6-125">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="8ccb6-125">-Endpoint</span></span>
<span data-ttu-id="8ccb6-126">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="8ccb6-127">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="8ccb6-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="8ccb6-128">-HostedService</span></span>
<span data-ttu-id="8ccb6-129">Określa obszar nazw usługi HDInsight, jeśli nie chcesz używać domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="8ccb6-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="8ccb6-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="8ccb6-131">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="8ccb6-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="8ccb6-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="8ccb6-132">-JobId</span></span>
<span data-ttu-id="8ccb6-133">Określa identyfikator zadania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-133">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ccb6-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="8ccb6-134">-Profile</span></span>
<span data-ttu-id="8ccb6-135">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ccb6-136">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ccb6-137">-Subscription</span><span class="sxs-lookup"><span data-stu-id="8ccb6-137">-Subscription</span></span>
<span data-ttu-id="8ccb6-138">Określa subskrypcję zawierającą zadania usługi HDInsight do pobrania.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-138">Specifies the subscription that contains the HDInsight jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ccb6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ccb6-139">CommonParameters</span></span>
<span data-ttu-id="8ccb6-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ccb6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ccb6-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ccb6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ccb6-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ccb6-142">INPUTS</span></span>

## <span data-ttu-id="8ccb6-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ccb6-143">OUTPUTS</span></span>

## <span data-ttu-id="8ccb6-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ccb6-144">NOTES</span></span>

## <span data-ttu-id="8ccb6-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ccb6-145">RELATED LINKS</span></span>

[<span data-ttu-id="8ccb6-146">Start — AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8ccb6-146">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="8ccb6-147">Zatrzymaj — AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8ccb6-147">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="8ccb6-148">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8ccb6-148">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


