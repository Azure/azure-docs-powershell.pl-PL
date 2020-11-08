---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3B39F43D-E74A-441D-91BC-26C324C1EDF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d0ea12e873604360114b02bb89d9bde12c9e70e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054610"
---
# <span data-ttu-id="ca82a-101">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ca82a-101">Get-AzureHDInsightCluster</span></span>

## <span data-ttu-id="ca82a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca82a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca82a-103">Pobiera klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ca82a-103">Gets an HDInsight cluster.</span></span>

## <span data-ttu-id="ca82a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca82a-104">SYNTAX</span></span>

```
Get-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca82a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca82a-105">DESCRIPTION</span></span>
<span data-ttu-id="ca82a-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="ca82a-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ca82a-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="ca82a-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ca82a-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca82a-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ca82a-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ca82a-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ca82a-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ca82a-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ca82a-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ca82a-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ca82a-112">Polecenie cmdlet **Get-AzureHDInsightCluster** pobiera klastry usługi Azure HDInsight dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ca82a-112">The **Get-AzureHDInsightCluster** cmdlet gets the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="ca82a-113">W celu uzyskania określonego klastra można użyć parametru *name* .</span><span class="sxs-lookup"><span data-stu-id="ca82a-113">You can use the *Name* parameter to get a specific cluster.</span></span>

## <span data-ttu-id="ca82a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca82a-114">EXAMPLES</span></span>

### <span data-ttu-id="ca82a-115">Przykład 1: uzyskiwanie klastrów w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ca82a-115">Example 1: Get the clusters in a subscription</span></span>
```
PS C:\> Get-AzureHDInsightCluster
```

<span data-ttu-id="ca82a-116">To polecenie pobiera informacje o klastrach usługi HDInsight w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ca82a-116">This command gets information about the HDInsight clusters in the current subscription.</span></span>

## <span data-ttu-id="ca82a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca82a-117">PARAMETERS</span></span>

### <span data-ttu-id="ca82a-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="ca82a-118">-Certificate</span></span>
<span data-ttu-id="ca82a-119">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ca82a-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="ca82a-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="ca82a-120">-Endpoint</span></span>
<span data-ttu-id="ca82a-121">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca82a-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="ca82a-122">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ca82a-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="ca82a-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="ca82a-123">-HostedService</span></span>
<span data-ttu-id="ca82a-124">Określa obszar nazw usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ca82a-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="ca82a-125">Jeśli nie podano tego parametru, to polecenie cmdlet użyje domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="ca82a-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="ca82a-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="ca82a-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="ca82a-127">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="ca82a-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="ca82a-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca82a-128">-Name</span></span>
<span data-ttu-id="ca82a-129">Określa nazwę klastra usługi HDInsight do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ca82a-129">Specifies the name of an HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca82a-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="ca82a-130">-Profile</span></span>
<span data-ttu-id="ca82a-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca82a-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ca82a-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ca82a-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ca82a-133">-Subscription</span><span class="sxs-lookup"><span data-stu-id="ca82a-133">-Subscription</span></span>
<span data-ttu-id="ca82a-134">Określa subskrypcję zawierającą klaster usługi HDInsight do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ca82a-134">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

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

### <span data-ttu-id="ca82a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca82a-135">CommonParameters</span></span>
<span data-ttu-id="ca82a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca82a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca82a-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca82a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca82a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca82a-138">INPUTS</span></span>

## <span data-ttu-id="ca82a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca82a-139">OUTPUTS</span></span>

## <span data-ttu-id="ca82a-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca82a-140">NOTES</span></span>

## <span data-ttu-id="ca82a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca82a-141">RELATED LINKS</span></span>

[<span data-ttu-id="ca82a-142">Nowe — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ca82a-142">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="ca82a-143">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ca82a-143">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="ca82a-144">Użyj — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ca82a-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


