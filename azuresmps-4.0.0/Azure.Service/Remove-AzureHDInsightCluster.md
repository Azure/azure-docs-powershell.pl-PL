---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 7D73D37B-17EE-4FF8-9A21-D2014D5417D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa779907648ca8e8e1288394d562c86b6102d9ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055442"
---
# <span data-ttu-id="ae5c3-101">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ae5c3-101">Remove-AzureHDInsightCluster</span></span>

## <span data-ttu-id="ae5c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5c3-103">Usuwa klaster usługi HDInsight z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-103">Deletes an HDInsight cluster from a subscription.</span></span>

## <span data-ttu-id="ae5c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae5c3-104">SYNTAX</span></span>

```
Remove-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae5c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae5c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ae5c3-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ae5c3-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ae5c3-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ae5c3-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ae5c3-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ae5c3-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ae5c3-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ae5c3-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ae5c3-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ae5c3-112">Polecenie cmdlet **Remove-AzureHDInsightCluster** umożliwia usunięcie określonego klastra usługi HDInsight z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-112">The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="ae5c3-113">Ta operacja usuwa również wszystkie dane przechowywane w systemie plików HDFS (Distributed File System) usługi Hadoop w klastrze.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-113">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="ae5c3-114">Dane przechowywane na skojarzonym koncie usługi Azure Storage nie są usuwane.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-114">Data stored in the associated Azure Storage account is not deleted.</span></span>

## <span data-ttu-id="ae5c3-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae5c3-115">EXAMPLES</span></span>

### <span data-ttu-id="ae5c3-116">Przykład 1: usuwanie klastra</span><span class="sxs-lookup"><span data-stu-id="ae5c3-116">Example 1: Remove a cluster</span></span>
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

<span data-ttu-id="ae5c3-117">To polecenie usuwa klaster usługi HDInsight o nazwie HDICluster.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-117">This command deletes the HDInsight cluster named HDICluster.</span></span>

## <span data-ttu-id="ae5c3-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae5c3-118">PARAMETERS</span></span>

### <span data-ttu-id="ae5c3-119">-Certificate</span><span class="sxs-lookup"><span data-stu-id="ae5c3-119">-Certificate</span></span>
<span data-ttu-id="ae5c3-120">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-120">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="ae5c3-121">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="ae5c3-121">-Endpoint</span></span>
<span data-ttu-id="ae5c3-122">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-122">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="ae5c3-123">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-123">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="ae5c3-124">-HostedService</span><span class="sxs-lookup"><span data-stu-id="ae5c3-124">-HostedService</span></span>
<span data-ttu-id="ae5c3-125">Określa obszar nazw usługi HDInsight, jeśli nie chcesz używać domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-125">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="ae5c3-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="ae5c3-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="ae5c3-127">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="ae5c3-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="ae5c3-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae5c3-128">-Name</span></span>
<span data-ttu-id="ae5c3-129">Określa nazwę klastra usługi HDInsight do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-129">Specifies the name of the HDInsight cluster to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5c3-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="ae5c3-130">-Profile</span></span>
<span data-ttu-id="ae5c3-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae5c3-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae5c3-133">-Subscription</span><span class="sxs-lookup"><span data-stu-id="ae5c3-133">-Subscription</span></span>
<span data-ttu-id="ae5c3-134">Określa konto abonamentu zawierające klaster usługi HDInsight do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-134">Specifies the subscription account that contains the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="ae5c3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5c3-135">CommonParameters</span></span>
<span data-ttu-id="ae5c3-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae5c3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5c3-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5c3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5c3-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae5c3-138">INPUTS</span></span>

## <span data-ttu-id="ae5c3-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae5c3-139">OUTPUTS</span></span>

## <span data-ttu-id="ae5c3-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae5c3-140">NOTES</span></span>

## <span data-ttu-id="ae5c3-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae5c3-141">RELATED LINKS</span></span>

[<span data-ttu-id="ae5c3-142">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ae5c3-142">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="ae5c3-143">Nowe — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ae5c3-143">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="ae5c3-144">Użyj — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ae5c3-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


