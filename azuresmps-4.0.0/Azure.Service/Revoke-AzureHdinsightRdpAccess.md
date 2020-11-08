---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6818F49E-0A51-4D99-BC3D-5A90F1F30C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78caed4ac43f21a1afe21a8901bdcd77ba29e482
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054442"
---
# <span data-ttu-id="2379d-101">Revoke-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="2379d-101">Revoke-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="2379d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2379d-102">SYNOPSIS</span></span>
<span data-ttu-id="2379d-103">Wyłącza dostęp RDP do klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2379d-103">Disables RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="2379d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2379d-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2379d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2379d-105">DESCRIPTION</span></span>
<span data-ttu-id="2379d-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="2379d-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="2379d-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="2379d-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="2379d-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2379d-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="2379d-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="2379d-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="2379d-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="2379d-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="2379d-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2379d-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="2379d-112">Polecenie cmdlet **REVOKE-AzureHDInsightRdpAccess** wyłącza dostęp do protokołu RDP (Remote Desktop Protocol) do klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2379d-112">The **Revoke-AzureHDInsightRdpAccess** cmdlet disables Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2379d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2379d-113">EXAMPLES</span></span>

## <span data-ttu-id="2379d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2379d-114">PARAMETERS</span></span>

### <span data-ttu-id="2379d-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="2379d-115">-Certificate</span></span>
<span data-ttu-id="2379d-116">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2379d-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="2379d-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="2379d-117">-Endpoint</span></span>
<span data-ttu-id="2379d-118">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2379d-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="2379d-119">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="2379d-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="2379d-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="2379d-120">-HostedService</span></span>
<span data-ttu-id="2379d-121">Określa obszar nazw usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2379d-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="2379d-122">Jeśli nie podano tego parametru, to polecenie cmdlet użyje domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="2379d-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="2379d-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="2379d-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="2379d-124">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="2379d-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="2379d-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2379d-125">-Location</span></span>
<span data-ttu-id="2379d-126">Określa obszar platformy Azure, w którym znajduje się klaster.</span><span class="sxs-lookup"><span data-stu-id="2379d-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="2379d-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2379d-127">-Name</span></span>
<span data-ttu-id="2379d-128">Określa nazwę klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2379d-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="2379d-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="2379d-129">-Profile</span></span>
<span data-ttu-id="2379d-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2379d-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2379d-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2379d-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2379d-132">-Subscription</span><span class="sxs-lookup"><span data-stu-id="2379d-132">-Subscription</span></span>
<span data-ttu-id="2379d-133">Określa abonament.</span><span class="sxs-lookup"><span data-stu-id="2379d-133">Specifies a subscription.</span></span>
<span data-ttu-id="2379d-134">Ten aplet polecenia odwołuje dostęp do protokołu RDP (Remote Desktop Protocol) dla subskrypcji, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="2379d-134">This cmdlet revokes Remote Desktop Protocol (RDP) access for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="2379d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2379d-135">CommonParameters</span></span>
<span data-ttu-id="2379d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2379d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2379d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2379d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2379d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2379d-138">INPUTS</span></span>

## <span data-ttu-id="2379d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2379d-139">OUTPUTS</span></span>

## <span data-ttu-id="2379d-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2379d-140">NOTES</span></span>

## <span data-ttu-id="2379d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2379d-141">RELATED LINKS</span></span>

[<span data-ttu-id="2379d-142">Grant-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="2379d-142">Grant-AzureHdinsightRdpAccess</span></span>](./Grant-AzureHdinsightRdpAccess.md)


