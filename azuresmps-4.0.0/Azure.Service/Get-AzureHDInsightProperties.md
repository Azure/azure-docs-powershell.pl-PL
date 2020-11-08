---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055317"
---
# <span data-ttu-id="6a226-101">Get-AzureHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="6a226-101">Get-AzureHDInsightProperties</span></span>

## <span data-ttu-id="6a226-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a226-102">SYNOPSIS</span></span>
<span data-ttu-id="6a226-103">Pobiera właściwości specyficzne dla usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6a226-103">Gets properties specific to an HDInsight service.</span></span>

## <span data-ttu-id="6a226-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a226-104">SYNTAX</span></span>

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a226-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a226-105">DESCRIPTION</span></span>
<span data-ttu-id="6a226-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="6a226-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="6a226-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="6a226-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="6a226-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a226-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="6a226-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="6a226-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="6a226-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="6a226-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="6a226-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6a226-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="6a226-112">Polecenie cmdlet **Get-AzureHDInsightProperties** pobiera właściwości specyficzne dla usługi Azure HDInsight, takiej jak lista dostępnych regionów platformy Azure, wersje klastra usługi HDInsight i dostępna pojemność obliczeniowa.</span><span class="sxs-lookup"><span data-stu-id="6a226-112">The **Get-AzureHDInsightProperties** cmdlet gets properties specific to an Azure HDInsight service, such as a list of available Azure regions, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="6a226-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a226-113">EXAMPLES</span></span>

### <span data-ttu-id="6a226-114">Przykład 1: uzyskiwanie właściwości usługi HDInsight dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6a226-114">Example 1: Get HDInsight properties for a subscription</span></span>
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

<span data-ttu-id="6a226-115">Pierwsze polecenie uzyskuje nazwę bieżącej subskrypcji platformy Azure, a następnie zapisuje ją w zmiennej $SubName.</span><span class="sxs-lookup"><span data-stu-id="6a226-115">The first command gets the name of the current Azure subscription, and then stores it in the $SubName variable.</span></span>

<span data-ttu-id="6a226-116">Drugie polecenie pobiera właściwości usługi HDInsight dla subskrypcji w $SubName.</span><span class="sxs-lookup"><span data-stu-id="6a226-116">The second command gets the HDInsight properties for the subscription in $SubName.</span></span>

## <span data-ttu-id="6a226-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a226-117">PARAMETERS</span></span>

### <span data-ttu-id="6a226-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="6a226-118">-Certificate</span></span>
<span data-ttu-id="6a226-119">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6a226-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="6a226-120">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="6a226-120">-Endpoint</span></span>
<span data-ttu-id="6a226-121">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a226-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="6a226-122">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6a226-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="6a226-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="6a226-123">-HostedService</span></span>
<span data-ttu-id="6a226-124">Określa obszar nazw usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6a226-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="6a226-125">Jeśli nie podano tego parametru, to polecenie cmdlet użyje domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6a226-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="6a226-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="6a226-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="6a226-127">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="6a226-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="6a226-128">— Lokalizacje</span><span class="sxs-lookup"><span data-stu-id="6a226-128">-Locations</span></span>
<span data-ttu-id="6a226-129">Wskazuje, że ten aplet polecenia pobiera listę regionów platformy Azure, w których jest dostępna Usługa HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6a226-129">Indicates that this cmdlet gets the list of Azure regions where the HDInsight service is available.</span></span>

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

### <span data-ttu-id="6a226-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="6a226-130">-Profile</span></span>
<span data-ttu-id="6a226-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a226-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6a226-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6a226-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a226-133">-Subscription</span><span class="sxs-lookup"><span data-stu-id="6a226-133">-Subscription</span></span>
<span data-ttu-id="6a226-134">Określa subskrypcję zawierającą właściwości usługi HDInsight do pobrania.</span><span class="sxs-lookup"><span data-stu-id="6a226-134">Specifies the subscription that contains the HDInsight properties to get.</span></span>

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

### <span data-ttu-id="6a226-135">-Wersje</span><span class="sxs-lookup"><span data-stu-id="6a226-135">-Versions</span></span>
<span data-ttu-id="6a226-136">Wskazuje, że ten aplet polecenia pobiera listę wersji klastra usługi HDInsight, które są dostępne w usłudze dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6a226-136">Indicates that this cmdlet gets the list of HDInsight cluster versions that are available in the service for a subscription.</span></span>

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

### <span data-ttu-id="6a226-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a226-137">CommonParameters</span></span>
<span data-ttu-id="6a226-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a226-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a226-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a226-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a226-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a226-140">INPUTS</span></span>

## <span data-ttu-id="6a226-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a226-141">OUTPUTS</span></span>

## <span data-ttu-id="6a226-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a226-142">NOTES</span></span>

## <span data-ttu-id="6a226-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a226-143">RELATED LINKS</span></span>

