---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054682"
---
# <span data-ttu-id="1bea7-101">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="1bea7-101">Add-AzureHDInsightStorage</span></span>

## <span data-ttu-id="1bea7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1bea7-102">SYNOPSIS</span></span>
<span data-ttu-id="1bea7-103">Dodaje wpis konta magazynu obiektów BLOB do konfiguracji usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1bea7-103">Adds a blob storage account entry to an HDInsight configuration.</span></span>

## <span data-ttu-id="1bea7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1bea7-104">SYNTAX</span></span>

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1bea7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1bea7-105">DESCRIPTION</span></span>
<span data-ttu-id="1bea7-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="1bea7-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="1bea7-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="1bea7-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="1bea7-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1bea7-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="1bea7-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="1bea7-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="1bea7-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="1bea7-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="1bea7-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1bea7-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="1bea7-112">Polecenie cmdlet **Add-AzureHDInsightStorage** dodaje wpis konta magazynu obiektów BLOB do konfiguracji usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1bea7-112">The **Add-AzureHDInsightStorage** cmdlet adds a blob storage account entry to an Azure HDInsight configuration.</span></span>

## <span data-ttu-id="1bea7-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1bea7-113">EXAMPLES</span></span>

### <span data-ttu-id="1bea7-114">Przykład 1: Dodawanie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1bea7-114">Example 1: Add a storage account</span></span>
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

<span data-ttu-id="1bea7-115">To polecenie umożliwia dodanie konta magazynu o nazwie Moja przestrzeń do obiektu konfiguracji przechowywanego w $Config, a następnie zapisanie konfiguracji w zmiennej $StoreConfig.</span><span class="sxs-lookup"><span data-stu-id="1bea7-115">This command adds a storage account named MyStorage to the configuration object stored in $Config, and then stores the configuration in the $StoreConfig variable.</span></span>

### <span data-ttu-id="1bea7-116">Przykład 2: Konfigurowanie wielu kont magazynu</span><span class="sxs-lookup"><span data-stu-id="1bea7-116">Example 2: Configure multiple storage accounts</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="1bea7-117">W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureSubscription** w celu uzyskania bieżącego identyfikatora subskrypcji, a następnie zapisanie go w zmiennej $SubId.</span><span class="sxs-lookup"><span data-stu-id="1bea7-117">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="1bea7-118">Drugie i trzecie polecenia cmdlet **Get-AzureStorageKey** umożliwiają uzyskiwanie podstawowych kluczy magazynu dla MyBlobStorage i MySecondBlobStorage, a następnie przechowywanie kluczy odpowiednio w zmiennych $Key 1 i $Key 2.</span><span class="sxs-lookup"><span data-stu-id="1bea7-118">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="1bea7-119">Cztery, piąte i szóste polecenia uzyskują poświadczenia dotyczące bieżącej subskrypcji i Oozie oraz gałęzi, a następnie przechowują poświadczenia w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="1bea7-119">The fourth, fifth, and sixth commands get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="1bea7-120">Polecenie ostatnie wykonuje sekwencję operacji, korzystając z następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="1bea7-120">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="1bea7-121">**New-AzureHDInsightClusterConfig** , aby utworzyć konfigurację klastra usługi HDInsight</span><span class="sxs-lookup"><span data-stu-id="1bea7-121">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration</span></span>
- <span data-ttu-id="1bea7-122">**Set-AzureHDInsightDefaultStorage** w celu ustawienia domyślnego konta magazynu dla konfiguracji na MyBlobStorage.blob.Core.Windows.NET</span><span class="sxs-lookup"><span data-stu-id="1bea7-122">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net</span></span>
- <span data-ttu-id="1bea7-123">**Add-AzureHDInsightStorage** , aby dodać do konfiguracji drugie konto magazynu o nazwie MySecondBlobStorage.blob.Core.Windows.NET</span><span class="sxs-lookup"><span data-stu-id="1bea7-123">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration</span></span>
- <span data-ttu-id="1bea7-124">**Add-AzureHDInsightStorage** , aby dodać element magazynu dla Oozie i magazynu w celu odgałęzienia do konfiguracji</span><span class="sxs-lookup"><span data-stu-id="1bea7-124">**Add-AzureHDInsightStorage** to add a metastore for Oozie and a metastore for Hive to the configuration</span></span>
- <span data-ttu-id="1bea7-125">**New-AzureHDInsightCluster** , aby utworzyć klaster usługi HDInsight z nową konfiguracją</span><span class="sxs-lookup"><span data-stu-id="1bea7-125">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration</span></span>

## <span data-ttu-id="1bea7-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1bea7-126">PARAMETERS</span></span>

### <span data-ttu-id="1bea7-127">-Config</span><span class="sxs-lookup"><span data-stu-id="1bea7-127">-Config</span></span>
<span data-ttu-id="1bea7-128">Określa obiekt konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="1bea7-128">Specifies a configuration object.</span></span>
<span data-ttu-id="1bea7-129">To polecenie cmdlet umożliwia dodanie informacji o koncie magazynu do obiektu, który określi ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1bea7-129">This cmdlet adds storage account information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="1bea7-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="1bea7-130">-Profile</span></span>
<span data-ttu-id="1bea7-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bea7-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1bea7-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1bea7-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1bea7-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1bea7-133">-StorageAccountKey</span></span>
<span data-ttu-id="1bea7-134">Określa klucz konta magazynu, który służy do uzyskiwania dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1bea7-134">Specifies the storage account key that is used to access a storage account.</span></span>

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

### <span data-ttu-id="1bea7-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1bea7-135">-StorageAccountName</span></span>
<span data-ttu-id="1bea7-136">Określa nazwę konta usługi Azure Storage, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="1bea7-136">Specifies the name of the Azure storage account to add.</span></span>

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

### <span data-ttu-id="1bea7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bea7-137">CommonParameters</span></span>
<span data-ttu-id="1bea7-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bea7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bea7-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bea7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bea7-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bea7-140">INPUTS</span></span>

## <span data-ttu-id="1bea7-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1bea7-141">OUTPUTS</span></span>

## <span data-ttu-id="1bea7-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1bea7-142">NOTES</span></span>

## <span data-ttu-id="1bea7-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bea7-143">RELATED LINKS</span></span>

[<span data-ttu-id="1bea7-144">Nowe — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1bea7-144">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="1bea7-145">Nowe — AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="1bea7-145">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="1bea7-146">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="1bea7-146">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


