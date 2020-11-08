---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF41DDBA-6D4B-47A5-BCFF-3D0BB1D375C5
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2b6aaf5e8564b3eea675a57176b8f7118d2c7a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054926"
---
# <span data-ttu-id="edfa1-101">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="edfa1-101">Set-AzureHDInsightDefaultStorage</span></span>

## <span data-ttu-id="edfa1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="edfa1-102">SYNOPSIS</span></span>
<span data-ttu-id="edfa1-103">Ustawia domyślne konto magazynu dla klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="edfa1-103">Sets the default storage account for an HDInsight cluster.</span></span>

## <span data-ttu-id="edfa1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="edfa1-104">SYNTAX</span></span>

```
Set-AzureHDInsightDefaultStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> -StorageContainerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="edfa1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="edfa1-105">DESCRIPTION</span></span>
<span data-ttu-id="edfa1-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="edfa1-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="edfa1-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="edfa1-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="edfa1-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="edfa1-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="edfa1-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="edfa1-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="edfa1-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="edfa1-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="edfa1-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="edfa1-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="edfa1-112">Polecenie cmdlet **Set-AzureHDInsightDefaultStorage** ustawia domyślne konto magazynu dla konfiguracji klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="edfa1-112">The **Set-AzureHDInsightDefaultStorage** cmdlet sets the default storage account for an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="edfa1-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="edfa1-113">EXAMPLES</span></span>

### <span data-ttu-id="edfa1-114">Przykład 1: Ustawianie domyślnego konta magazynu</span><span class="sxs-lookup"><span data-stu-id="edfa1-114">Example 1: Set the default storage account</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer"
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="edfa1-115">W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureSubscription** w celu uzyskania bieżącego identyfikatora subskrypcji, a następnie zapisanie go w zmiennej $SubId.</span><span class="sxs-lookup"><span data-stu-id="edfa1-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="edfa1-116">Drugie i trzecie polecenia cmdlet **Get-AzureStorageKey** umożliwiają uzyskiwanie podstawowych kluczy magazynu dla MyBlobStorage i MySecondBlobStorage, a następnie przechowywanie kluczy odpowiednio w zmiennych $Key 1 i $Key 2.</span><span class="sxs-lookup"><span data-stu-id="edfa1-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="edfa1-117">W przypadku czterech, piątych i szóstych poleceń Użyj polecenia cmdlet **Get-Credential** , aby uzyskać poświadczenia dla bieżącej subskrypcji, a następnie Zapisz poświadczenia w $Creds, $OozieCreds i $HiveCreds zmiennych.</span><span class="sxs-lookup"><span data-stu-id="edfa1-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription, and then stores the credentials in the $Creds, $OozieCreds, and $HiveCreds variables.</span></span>

<span data-ttu-id="edfa1-118">Polecenie ostatnie wykonuje sekwencję operacji, korzystając z następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="edfa1-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="edfa1-119">**New-AzureHDInsightClusterConfig** , aby utworzyć konfigurację klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="edfa1-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="edfa1-120">**Set-AzureHDInsightDefaultStorage** , aby ustawić domyślne konto magazynu dla konfiguracji na MyBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="edfa1-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="edfa1-121">**Add-AzureHDInsightStorage** , aby dodać do konfiguracji drugie konto magazynu o nazwie MySecondBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="edfa1-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="edfa1-122">**Add-AzureHDInsightMetastore** , aby dodać do konfiguracji element magazynu dla Oozie i magazynu.</span><span class="sxs-lookup"><span data-stu-id="edfa1-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="edfa1-123">**New-AzureHDInsightCluster** , aby utworzyć klaster usługi HDInsight z nową konfiguracją.</span><span class="sxs-lookup"><span data-stu-id="edfa1-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="edfa1-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edfa1-124">PARAMETERS</span></span>

### <span data-ttu-id="edfa1-125">-Config</span><span class="sxs-lookup"><span data-stu-id="edfa1-125">-Config</span></span>
<span data-ttu-id="edfa1-126">Określa obiekt konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="edfa1-126">Specifies a configuration object.</span></span>
<span data-ttu-id="edfa1-127">To polecenie cmdlet ustawia domyślne konto magazynu dla obiektu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="edfa1-127">This cmdlet sets the default storage account for the object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edfa1-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="edfa1-128">-Profile</span></span>
<span data-ttu-id="edfa1-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edfa1-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="edfa1-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="edfa1-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="edfa1-131">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="edfa1-131">-StorageAccountKey</span></span>
<span data-ttu-id="edfa1-132">Określa klucz konta magazynu, w którym można uzyskać dostęp do domyślnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="edfa1-132">Specifies the storage account key that is used to access the default storage account.</span></span>

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

### <span data-ttu-id="edfa1-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="edfa1-133">-StorageAccountName</span></span>
<span data-ttu-id="edfa1-134">Określa nazwę domyślnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="edfa1-134">Specifies the name of a default storage account.</span></span>

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

### <span data-ttu-id="edfa1-135">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="edfa1-135">-StorageContainerName</span></span>
<span data-ttu-id="edfa1-136">Określa nazwę domyślnego kontenera magazynu dla klastra.</span><span class="sxs-lookup"><span data-stu-id="edfa1-136">Specifies the name of the default storage container for a cluster.</span></span>

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

### <span data-ttu-id="edfa1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfa1-137">CommonParameters</span></span>
<span data-ttu-id="edfa1-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edfa1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfa1-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edfa1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfa1-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edfa1-140">INPUTS</span></span>

## <span data-ttu-id="edfa1-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="edfa1-141">OUTPUTS</span></span>

## <span data-ttu-id="edfa1-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="edfa1-142">NOTES</span></span>

## <span data-ttu-id="edfa1-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edfa1-143">RELATED LINKS</span></span>

[<span data-ttu-id="edfa1-144">Dodaj-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="edfa1-144">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="edfa1-145">Dodaj-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="edfa1-145">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="edfa1-146">Nowe — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="edfa1-146">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="edfa1-147">Nowe — AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="edfa1-147">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


