---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E3D22B03-2997-4F2C-895E-AE0993FD7C92
online version: ''
schema: 2.0.0
ms.openlocfilehash: bfd3e1f2bb5d057dec8a7bee5929ba5c67c8d53d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055464"
---
# <span data-ttu-id="333fb-101">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="333fb-101">Grant-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="333fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="333fb-102">SYNOPSIS</span></span>
<span data-ttu-id="333fb-103">Przyznaje dostęp HTTP do klastra.</span><span class="sxs-lookup"><span data-stu-id="333fb-103">Grants HTTP access to a cluster.</span></span>

## <span data-ttu-id="333fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="333fb-104">SYNTAX</span></span>

```
Grant-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Credential <PSCredential> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="333fb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="333fb-105">DESCRIPTION</span></span>
<span data-ttu-id="333fb-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="333fb-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="333fb-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="333fb-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="333fb-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="333fb-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="333fb-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="333fb-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="333fb-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="333fb-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="333fb-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="333fb-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="333fb-112">Polecenie cmdlet **Grant-AzureHDInsightHttpServicesAccess** udziela dostępu HTTP do klastra usługi Azure HDInsight przy użyciu ODBC, Ambari, Oozie i usług sieci Web.</span><span class="sxs-lookup"><span data-stu-id="333fb-112">The **Grant-AzureHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie, and web services.</span></span>

## <span data-ttu-id="333fb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="333fb-113">EXAMPLES</span></span>

## <span data-ttu-id="333fb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="333fb-114">PARAMETERS</span></span>

### <span data-ttu-id="333fb-115">-Certificate</span><span class="sxs-lookup"><span data-stu-id="333fb-115">-Certificate</span></span>
<span data-ttu-id="333fb-116">Określa certyfikat zarządzania dla subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="333fb-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="333fb-117">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="333fb-117">-Credential</span></span>
<span data-ttu-id="333fb-118">Określa nazwę użytkownika i hasło dostępu HTTP.</span><span class="sxs-lookup"><span data-stu-id="333fb-118">Specifies a user name and password for HTTP access.</span></span>

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

### <span data-ttu-id="333fb-119">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="333fb-119">-Endpoint</span></span>
<span data-ttu-id="333fb-120">Określa punkt końcowy, którego należy użyć w celu nawiązania połączenia z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="333fb-120">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="333fb-121">Jeśli nie podano tego parametru, to polecenie cmdlet używa domyślnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="333fb-121">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="333fb-122">-HostedService</span><span class="sxs-lookup"><span data-stu-id="333fb-122">-HostedService</span></span>
<span data-ttu-id="333fb-123">Określa obszar nazw usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="333fb-123">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="333fb-124">Jeśli nie podano tego parametru, to polecenie cmdlet użyje domyślnego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="333fb-124">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="333fb-125">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="333fb-125">-IgnoreSslErrors</span></span>
<span data-ttu-id="333fb-126">Wskazuje, czy są ignorowane błędy protokołu SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="333fb-126">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="333fb-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="333fb-127">-Location</span></span>
<span data-ttu-id="333fb-128">Określa obszar platformy Azure, w którym znajduje się klaster.</span><span class="sxs-lookup"><span data-stu-id="333fb-128">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="333fb-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="333fb-129">-Name</span></span>
<span data-ttu-id="333fb-130">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="333fb-130">Specifies the name of a cluster.</span></span>
<span data-ttu-id="333fb-131">To polecenie cmdlet udziela dostępu HTTP do klastra, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="333fb-131">This cmdlet grants HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="333fb-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="333fb-132">-Profile</span></span>
<span data-ttu-id="333fb-133">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="333fb-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="333fb-134">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="333fb-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="333fb-135">-Subscription</span><span class="sxs-lookup"><span data-stu-id="333fb-135">-Subscription</span></span>
<span data-ttu-id="333fb-136">Określa subskrypcję zawierającą klaster usługi HDInsight, do którego ma zostać udzielony dostęp.</span><span class="sxs-lookup"><span data-stu-id="333fb-136">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="333fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333fb-137">CommonParameters</span></span>
<span data-ttu-id="333fb-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333fb-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="333fb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333fb-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="333fb-140">INPUTS</span></span>

## <span data-ttu-id="333fb-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="333fb-141">OUTPUTS</span></span>

## <span data-ttu-id="333fb-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="333fb-142">NOTES</span></span>

## <span data-ttu-id="333fb-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="333fb-143">RELATED LINKS</span></span>

[<span data-ttu-id="333fb-144">REVOKE-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="333fb-144">Revoke-AzureHDInsightHttpServicesAccess</span></span>](./Revoke-AzureHDInsightHttpServicesAccess.md)


