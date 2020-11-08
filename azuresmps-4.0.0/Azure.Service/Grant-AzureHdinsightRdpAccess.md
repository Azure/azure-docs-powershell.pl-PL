---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 95CCEB79-EAC4-4F56-B289-5401F976E5F5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92b2c005f855ccf99e8bae4d8db8445ba7e63dad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055228"
---
# <span data-ttu-id="ae608-101">Grant-AzureHDInsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="ae608-101">Grant-AzureHDInsightRdpAccess</span></span>

## <span data-ttu-id="ae608-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae608-102">SYNOPSIS</span></span>
<span data-ttu-id="ae608-103">Udziela dostępu RDP do klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ae608-103">Grants RDP access to an HDInsight cluster.</span></span>

## <span data-ttu-id="ae608-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae608-104">SYNTAX</span></span>

```
Grant-AzureHDInsightRdpAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -RdpCredential <PSCredential> -RdpAccessExpiry <DateTime> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae608-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae608-105">DESCRIPTION</span></span>
<span data-ttu-id="ae608-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="ae608-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ae608-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="ae608-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ae608-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae608-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ae608-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ae608-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ae608-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ae608-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ae608-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ae608-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ae608-112">Polecenie cmdlet **Grant-AzureHDInsightRdpAccess** przyznaje dostęp do klastra usługi Remote Desktop Protocol (RDP) do klastra Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ae608-112">The **Grant-AzureHDInsightRdpAccess** cmdlet grants Remote Desktop Protocol (RDP) access to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ae608-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae608-113">EXAMPLES</span></span>

## <span data-ttu-id="ae608-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae608-114">PARAMETERS</span></span>

### <span data-ttu-id="ae608-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="ae608-115">-Certificate</span></span>
<span data-ttu-id="ae608-116">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ae608-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="ae608-117">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="ae608-117">-Endpoint</span></span>
<span data-ttu-id="ae608-118">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae608-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="ae608-119">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ae608-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="ae608-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="ae608-120">-HostedService</span></span>
<span data-ttu-id="ae608-121">Określa obszar nazw usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ae608-121">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="ae608-122">Jeśli nie podano tego parametru, to polecenie cmdlet użyje domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="ae608-122">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="ae608-123">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="ae608-123">-IgnoreSslErrors</span></span>
<span data-ttu-id="ae608-124">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="ae608-124">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="ae608-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ae608-125">-Location</span></span>
<span data-ttu-id="ae608-126">Określa obszar platformy Azure, w którym znajduje się klaster.</span><span class="sxs-lookup"><span data-stu-id="ae608-126">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="ae608-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae608-127">-Name</span></span>
<span data-ttu-id="ae608-128">Określa nazwę klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ae608-128">Specifies the name of an Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="ae608-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="ae608-129">-Profile</span></span>
<span data-ttu-id="ae608-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae608-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae608-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ae608-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae608-132">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="ae608-132">-RdpAccessExpiry</span></span>
<span data-ttu-id="ae608-133">Określa wygaśnięcie jako obiekt **DateTime** , aby uzyskać dostęp do klastra za pomocą protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ae608-133">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae608-134">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="ae608-134">-RdpCredential</span></span>
<span data-ttu-id="ae608-135">Określa poświadczenia dostępu RDP do klastra.</span><span class="sxs-lookup"><span data-stu-id="ae608-135">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae608-136">-Subscription</span><span class="sxs-lookup"><span data-stu-id="ae608-136">-Subscription</span></span>
<span data-ttu-id="ae608-137">Określa subskrypcję zawierającą klaster usługi HDInsight, do którego ma zostać udzielony dostęp.</span><span class="sxs-lookup"><span data-stu-id="ae608-137">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="ae608-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae608-138">CommonParameters</span></span>
<span data-ttu-id="ae608-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae608-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae608-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae608-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae608-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae608-141">INPUTS</span></span>

## <span data-ttu-id="ae608-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae608-142">OUTPUTS</span></span>

## <span data-ttu-id="ae608-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae608-143">NOTES</span></span>

## <span data-ttu-id="ae608-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae608-144">RELATED LINKS</span></span>

[<span data-ttu-id="ae608-145">REVOKE-AzureHdinsightRdpAccess</span><span class="sxs-lookup"><span data-stu-id="ae608-145">Revoke-AzureHdinsightRdpAccess</span></span>](./Revoke-AzureHdinsightRdpAccess.md)


