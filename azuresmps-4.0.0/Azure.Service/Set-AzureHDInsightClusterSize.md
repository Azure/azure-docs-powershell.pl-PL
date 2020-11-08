---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 771B7CB2-88F6-4FC5-9DB0-E623D231E51A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdbf7778ca2d7498d7f33586f7e9e50e0955c521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054928"
---
# <span data-ttu-id="118b3-101">Set-AzureHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="118b3-101">Set-AzureHDInsightClusterSize</span></span>

## <span data-ttu-id="118b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="118b3-102">SYNOPSIS</span></span>
<span data-ttu-id="118b3-103">Ustawia liczbę węzłów danych dla klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="118b3-103">Sets the number of data nodes for an HDInsight cluster.</span></span>

## <span data-ttu-id="118b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="118b3-104">SYNTAX</span></span>

### <span data-ttu-id="118b3-105">Ustaw rozmiar klastra w węzłach o nazwie.</span><span class="sxs-lookup"><span data-stu-id="118b3-105">Set cluster size in nodes with name.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> -Name <String> [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="118b3-106">Ustaw rozmiar klastra w węzłach z rurociągiem klastra.</span><span class="sxs-lookup"><span data-stu-id="118b3-106">Set cluster size in nodes with cluster from pipeline.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> [-Force] -Cluster <AzureHDInsightCluster>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="118b3-107">Klaster według nazwy (z określonymi poświadczeniami subskrypcji)</span><span class="sxs-lookup"><span data-stu-id="118b3-107">Cluster By Name (with Specific Subscription Credential)</span></span>
```
Set-AzureHDInsightClusterSize [-Certificate <X509Certificate2>] [-Subscription <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="118b3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="118b3-108">DESCRIPTION</span></span>
<span data-ttu-id="118b3-109">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="118b3-109">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="118b3-110">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="118b3-110">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="118b3-111">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="118b3-111">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="118b3-112">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="118b3-112">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="118b3-113">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="118b3-113">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="118b3-114">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="118b3-114">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="118b3-115">Polecenie cmdlet **Set-AzureHDInsightClusterSize** ustawia liczbę węzłów danych dla klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="118b3-115">The **Set-AzureHDInsightClusterSize** cmdlet sets the number of data nodes for an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="118b3-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="118b3-116">EXAMPLES</span></span>

## <span data-ttu-id="118b3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="118b3-117">PARAMETERS</span></span>

### <span data-ttu-id="118b3-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="118b3-118">-Certificate</span></span>
<span data-ttu-id="118b3-119">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="118b3-119">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118b3-120">-Cluster</span><span class="sxs-lookup"><span data-stu-id="118b3-120">-Cluster</span></span>
<span data-ttu-id="118b3-121">Określa klaster, którego rozmiar należy zmienić.</span><span class="sxs-lookup"><span data-stu-id="118b3-121">Specifies the cluster to resize.</span></span>

```yaml
Type: AzureHDInsightCluster
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="118b3-122">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="118b3-122">-ClusterSizeInNodes</span></span>
<span data-ttu-id="118b3-123">Określa liczbę węzłów danych do utworzenia dla klastra.</span><span class="sxs-lookup"><span data-stu-id="118b3-123">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with name.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118b3-124">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="118b3-124">-Endpoint</span></span>
<span data-ttu-id="118b3-125">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="118b3-125">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="118b3-126">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="118b3-126">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118b3-127">-Force</span><span class="sxs-lookup"><span data-stu-id="118b3-127">-Force</span></span>
<span data-ttu-id="118b3-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="118b3-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Set cluster size in nodes with name., Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118b3-129">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="118b3-129">-IgnoreSslErrors</span></span>
<span data-ttu-id="118b3-130">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="118b3-130">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118b3-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="118b3-131">-Name</span></span>
<span data-ttu-id="118b3-132">Określa nazwę klastra usługi HDInsight, którego rozmiar chcesz zmienić.</span><span class="sxs-lookup"><span data-stu-id="118b3-132">Specifies the name of the HDInsight cluster to resize.</span></span>

```yaml
Type: String
Parameter Sets: Set cluster size in nodes with name.
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118b3-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="118b3-133">-Profile</span></span>
<span data-ttu-id="118b3-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="118b3-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="118b3-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="118b3-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="118b3-136">-Subscription</span><span class="sxs-lookup"><span data-stu-id="118b3-136">-Subscription</span></span>
<span data-ttu-id="118b3-137">Określa abonament.</span><span class="sxs-lookup"><span data-stu-id="118b3-137">Specifies a subscription.</span></span>
<span data-ttu-id="118b3-138">To polecenie cmdlet ustawia rozmiar klastra dla subskrypcji określanej przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="118b3-138">This cmdlet sets the cluster size for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118b3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="118b3-139">CommonParameters</span></span>
<span data-ttu-id="118b3-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="118b3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="118b3-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="118b3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="118b3-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="118b3-142">INPUTS</span></span>

## <span data-ttu-id="118b3-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="118b3-143">OUTPUTS</span></span>

## <span data-ttu-id="118b3-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="118b3-144">NOTES</span></span>

## <span data-ttu-id="118b3-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="118b3-145">RELATED LINKS</span></span>

