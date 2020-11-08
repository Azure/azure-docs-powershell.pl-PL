---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A1DFA523-B532-4902-838D-74C8CA97A335
online version: ''
schema: 2.0.0
ms.openlocfilehash: f85d12100eb5b2b093eea252ac308e8a45cf1c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055400"
---
# <span data-ttu-id="bd2c2-101">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bd2c2-101">Revoke-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="bd2c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="bd2c2-103">Wyłącza dostęp HTTP do klastra.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-103">Disables HTTP access to a cluster.</span></span>

## <span data-ttu-id="bd2c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd2c2-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 [-IgnoreSslErrors <Boolean>] [-Endpoint <Uri>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bd2c2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd2c2-105">DESCRIPTION</span></span>
<span data-ttu-id="bd2c2-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="bd2c2-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="bd2c2-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="bd2c2-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="bd2c2-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="bd2c2-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="bd2c2-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="bd2c2-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bd2c2-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="bd2c2-112">Polecenie cmdlet **REVOKE-AzureHDInsightHttpServicesAccess** wyłącza dostęp HTTP do klastra dla usług ODBC, Ambari, Oozie i WebHCatalog sieci Web.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-112">The **Revoke-AzureHDInsightHttpServicesAccess** cmdlet disables HTTP access to a cluster for ODBC, Ambari, Oozie and WebHCatalog web services.</span></span>

## <span data-ttu-id="bd2c2-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd2c2-113">EXAMPLES</span></span>

## <span data-ttu-id="bd2c2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd2c2-114">PARAMETERS</span></span>

### <span data-ttu-id="bd2c2-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="bd2c2-115">-Certificate</span></span>
<span data-ttu-id="bd2c2-116">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="bd2c2-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="bd2c2-117">-Endpoint</span></span>
<span data-ttu-id="bd2c2-118">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="bd2c2-119">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="bd2c2-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="bd2c2-120">-HostedService</span></span>
<span data-ttu-id="bd2c2-121">Określa obszar nazw usługi HDInsight, jeśli nie chcesz używać domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-121">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="bd2c2-122">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="bd2c2-122">-IgnoreSslErrors</span></span>
<span data-ttu-id="bd2c2-123">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="bd2c2-123">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="bd2c2-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bd2c2-124">-Location</span></span>
<span data-ttu-id="bd2c2-125">Określa region, w którym znajduje się klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-125">Specifies the region in which an HDInsight cluster is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd2c2-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd2c2-126">-Name</span></span>
<span data-ttu-id="bd2c2-127">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-127">Specifies the name of a cluster.</span></span>
<span data-ttu-id="bd2c2-128">To polecenie cmdlet wyłącza dostęp HTTP do klastra, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-128">This cmdlet disables HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="bd2c2-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="bd2c2-129">-Profile</span></span>
<span data-ttu-id="bd2c2-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bd2c2-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bd2c2-132">-Subscription</span><span class="sxs-lookup"><span data-stu-id="bd2c2-132">-Subscription</span></span>
<span data-ttu-id="bd2c2-133">Określa konto abonamentu zawierające klaster usługi HDInsight, który ma zostać odwołany.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-133">Specifies the subscription account that contains the HDInsight cluster to revoke.</span></span>

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

### <span data-ttu-id="bd2c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd2c2-134">CommonParameters</span></span>
<span data-ttu-id="bd2c2-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd2c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd2c2-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd2c2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd2c2-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd2c2-137">INPUTS</span></span>

## <span data-ttu-id="bd2c2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd2c2-138">OUTPUTS</span></span>

## <span data-ttu-id="bd2c2-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd2c2-139">NOTES</span></span>

## <span data-ttu-id="bd2c2-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd2c2-140">RELATED LINKS</span></span>

[<span data-ttu-id="bd2c2-141">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bd2c2-141">Grant-AzureHDInsightHttpServicesAccess</span></span>](./Grant-AzureHDInsightHttpServicesAccess.md)


