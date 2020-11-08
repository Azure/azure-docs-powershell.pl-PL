---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054886"
---
# <span data-ttu-id="50738-101">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="50738-101">New-AzureHDInsightClusterConfig</span></span>

## <span data-ttu-id="50738-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50738-102">SYNOPSIS</span></span>
<span data-ttu-id="50738-103">Tworzy nieutrwaloną konfigurację klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="50738-103">Creates a non-persisted HDInsight cluster configuration.</span></span>

## <span data-ttu-id="50738-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50738-104">SYNTAX</span></span>

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="50738-105">Opis</span><span class="sxs-lookup"><span data-stu-id="50738-105">DESCRIPTION</span></span>
<span data-ttu-id="50738-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="50738-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="50738-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="50738-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="50738-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="50738-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="50738-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="50738-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="50738-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="50738-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="50738-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="50738-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="50738-112">Polecenie cmdlet **New-AzureHDInsightClusterConfig** tworzy nieutrwaloną konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="50738-112">The **New-AzureHDInsightClusterConfig** cmdlet creates a non-persisted Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="50738-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50738-113">EXAMPLES</span></span>

### <span data-ttu-id="50738-114">Przykład 1: Tworzenie konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="50738-114">Example 1: Create a cluster configuration</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="50738-115">W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureSubscription** w celu uzyskania bieżącego identyfikatora subskrypcji, a następnie zapisanie go w zmiennej $SubId.</span><span class="sxs-lookup"><span data-stu-id="50738-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="50738-116">Drugie i trzecie polecenia cmdlet **Get-AzureStorageKey** umożliwiają uzyskiwanie podstawowych kluczy magazynu dla MyBlobStorage i MySecondBlobStorage, a następnie przechowywanie kluczy odpowiednio w zmiennych $Key 1 i $Key 2.</span><span class="sxs-lookup"><span data-stu-id="50738-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="50738-117">W przypadku czterech, piątych i szóstych poleceń Użyj polecenia cmdlet **Get-Credential** , aby uzyskać poświadczenia dla bieżącego abonamentu oraz dla Oozie i gałąź, a następnie zapisać poświadczenia w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="50738-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="50738-118">Polecenie ostatnie wykonuje sekwencję operacji, korzystając z następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="50738-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="50738-119">**New-AzureHDInsightClusterConfig** , aby utworzyć konfigurację klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="50738-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="50738-120">**Set-AzureHDInsightDefaultStorage** , aby ustawić domyślne konto magazynu dla konfiguracji na MyBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="50738-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="50738-121">**Add-AzureHDInsightStorage** , aby dodać do konfiguracji drugie konto magazynu o nazwie MySecondBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="50738-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="50738-122">**Add-AzureHDInsightMetastore** , aby dodać do konfiguracji element magazynu dla Oozie i magazynu.</span><span class="sxs-lookup"><span data-stu-id="50738-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="50738-123">**New-AzureHDInsightCluster** , aby utworzyć klaster usługi HDInsight z nową konfiguracją.</span><span class="sxs-lookup"><span data-stu-id="50738-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="50738-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50738-124">PARAMETERS</span></span>

### <span data-ttu-id="50738-125">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="50738-125">-ClusterSizeInNodes</span></span>
<span data-ttu-id="50738-126">Określa liczbę węzłów danych do utworzenia dla klastra.</span><span class="sxs-lookup"><span data-stu-id="50738-126">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50738-127">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="50738-127">-ClusterType</span></span>
<span data-ttu-id="50738-128">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="50738-128">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50738-129">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="50738-129">-DataNodeVMSize</span></span>
<span data-ttu-id="50738-130">Określa rozmiar maszyny wirtualnej dla węzła danych.</span><span class="sxs-lookup"><span data-stu-id="50738-130">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50738-131">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="50738-131">-HeadNodeVMSize</span></span>
<span data-ttu-id="50738-132">Określa rozmiar maszyny wirtualnej węzła głównego dla klastra.</span><span class="sxs-lookup"><span data-stu-id="50738-132">Specifies the virtual machine size of the head node for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50738-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="50738-133">-Profile</span></span>
<span data-ttu-id="50738-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50738-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50738-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="50738-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50738-136">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="50738-136">-SubnetName</span></span>
<span data-ttu-id="50738-137">Określa nazwę podsieci.</span><span class="sxs-lookup"><span data-stu-id="50738-137">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50738-138">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="50738-138">-VirtualNetworkId</span></span>
<span data-ttu-id="50738-139">Określa identyfikator sieci wirtualnej, do której ma być zastrzec klaster.</span><span class="sxs-lookup"><span data-stu-id="50738-139">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50738-140">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="50738-140">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="50738-141">Określa rozmiar maszyny wirtualnej dla węzła ZooKeeper dla HBase lub klastra burzowego.</span><span class="sxs-lookup"><span data-stu-id="50738-141">Specifies the size of the virtual machine for the ZooKeeper node for an HBase or Storm cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50738-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50738-142">CommonParameters</span></span>
<span data-ttu-id="50738-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50738-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50738-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50738-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50738-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50738-145">INPUTS</span></span>

## <span data-ttu-id="50738-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50738-146">OUTPUTS</span></span>

## <span data-ttu-id="50738-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50738-147">NOTES</span></span>

## <span data-ttu-id="50738-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50738-148">RELATED LINKS</span></span>

[<span data-ttu-id="50738-149">Dodaj-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="50738-149">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="50738-150">Dodaj-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="50738-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="50738-151">Nowe — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="50738-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="50738-152">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="50738-152">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


