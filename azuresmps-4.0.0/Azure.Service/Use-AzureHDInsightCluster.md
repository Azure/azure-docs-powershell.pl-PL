---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0BF58D9C-814E-4276-823F-D566DC99391C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 773af58d0ae9b4ca940240875b5cf9a8d3a0ffe7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054803"
---
# <span data-ttu-id="ce0ab-101">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ce0ab-101">Use-AzureHDInsightCluster</span></span>

## <span data-ttu-id="ce0ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce0ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0ab-103">Wybiera klaster usługi HDInsight dla Invoke-AzureHDInsightHiveJob polecenia cmdlet służącego do przesyłania zadań.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-103">Selects an HDInsight cluster for the Invoke-AzureHDInsightHiveJob cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="ce0ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce0ab-104">SYNTAX</span></span>

```
Use-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce0ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ce0ab-105">DESCRIPTION</span></span>
<span data-ttu-id="ce0ab-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ce0ab-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ce0ab-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ce0ab-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ce0ab-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ce0ab-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ce0ab-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ce0ab-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ce0ab-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ce0ab-112">Polecenie cmdlet **use-AzureHDInsightCluster** umożliwia wybranie klastra usługi Azure HDInsight dla polecenia cmdlet **Invoke-AzureHDInsightHiveJob** w celu użycia go do przesyłania zadań.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-112">The **Use-AzureHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the **Invoke-AzureHDInsightHiveJob** cmdlet to use to submit jobs.</span></span>

## <span data-ttu-id="ce0ab-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce0ab-113">EXAMPLES</span></span>

## <span data-ttu-id="ce0ab-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce0ab-114">PARAMETERS</span></span>

### <span data-ttu-id="ce0ab-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="ce0ab-115">-Certificate</span></span>
<span data-ttu-id="ce0ab-116">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="ce0ab-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="ce0ab-117">-Endpoint</span></span>
<span data-ttu-id="ce0ab-118">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="ce0ab-119">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="ce0ab-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="ce0ab-120">-HostedService</span></span>
<span data-ttu-id="ce0ab-121">Określa obszar nazw usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="ce0ab-122">Jeśli ten parametr nie zostanie określony, zostanie wykorzystana domyślna przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-122">If you do not specify this parameter, the default namespace is used.</span></span>

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

### <span data-ttu-id="ce0ab-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="ce0ab-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="ce0ab-124">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="ce0ab-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="ce0ab-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce0ab-125">-Name</span></span>
<span data-ttu-id="ce0ab-126">Określa nazwę klastra używanego przez polecenie cmdlet **Invoke-AzureHDInsightHiveJob** .</span><span class="sxs-lookup"><span data-stu-id="ce0ab-126">Specifies the name of the cluster that is used by the **Invoke-AzureHDInsightHiveJob** cmdlet.</span></span>

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

### <span data-ttu-id="ce0ab-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="ce0ab-127">-Profile</span></span>
<span data-ttu-id="ce0ab-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce0ab-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce0ab-130">-Subscription</span><span class="sxs-lookup"><span data-stu-id="ce0ab-130">-Subscription</span></span>
<span data-ttu-id="ce0ab-131">Określa subskrypcję zawierającą klastry usługi HDInsight do użycia.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-131">Specifies the subscription that contains the HDInsight clusters to use.</span></span>

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

### <span data-ttu-id="ce0ab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0ab-132">CommonParameters</span></span>
<span data-ttu-id="ce0ab-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce0ab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0ab-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce0ab-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0ab-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce0ab-135">INPUTS</span></span>

## <span data-ttu-id="ce0ab-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce0ab-136">OUTPUTS</span></span>

## <span data-ttu-id="ce0ab-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce0ab-137">NOTES</span></span>

## <span data-ttu-id="ce0ab-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce0ab-138">RELATED LINKS</span></span>

[<span data-ttu-id="ce0ab-139">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ce0ab-139">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="ce0ab-140">Nowe — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ce0ab-140">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="ce0ab-141">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ce0ab-141">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)


