---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054689"
---
# <span data-ttu-id="53a42-101">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="53a42-101">Add-AzureHDInsightMetastore</span></span>

## <span data-ttu-id="53a42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53a42-102">SYNOPSIS</span></span>
<span data-ttu-id="53a42-103">Dodaje konto bazy danych programu SQL Server do konfiguracji klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="53a42-103">Adds a SQL Server database account to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="53a42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53a42-104">SYNTAX</span></span>

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="53a42-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53a42-105">DESCRIPTION</span></span>
<span data-ttu-id="53a42-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="53a42-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="53a42-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="53a42-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="53a42-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="53a42-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="53a42-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="53a42-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="53a42-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="53a42-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="53a42-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="53a42-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="53a42-112">Polecenie cmdlet **Add-AzureHDInsightMetastore** umożliwia dodanie bazy danych programu Microsoft SQL Server do konfiguracji usługi Azure HDInsight utworzonej za pomocą polecenia cmdlet **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="53a42-112">The **Add-AzureHDInsightMetastore** cmdlet adds a Microsoft SQL Server database to an Azure HDInsight configuration that is created by the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>
<span data-ttu-id="53a42-113">Baza danych służy do przechowywania metadanych gałęzi lub Oozie.</span><span class="sxs-lookup"><span data-stu-id="53a42-113">The database is used to store metadata for Hive or Oozie, or both.</span></span>

## <span data-ttu-id="53a42-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53a42-114">EXAMPLES</span></span>

### <span data-ttu-id="53a42-115">Przykład 1: Dodawanie magazynu</span><span class="sxs-lookup"><span data-stu-id="53a42-115">Example 1: Add a metastore</span></span>
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

<span data-ttu-id="53a42-116">To polecenie dodaje bazę danych programu SQL Server o nazwie ContosoSQLServer, która służy jako magazyn dla klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="53a42-116">This command adds a SQL Server database named ContosoSQLServer to serve as a Hive metastore for an HDInsight cluster.</span></span>

### <span data-ttu-id="53a42-117">Przykład 2: Konfigurowanie miejsca do magazynowania i Dodawanie magazynu</span><span class="sxs-lookup"><span data-stu-id="53a42-117">Example 2: Configure storage and add metastores</span></span>
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

<span data-ttu-id="53a42-118">W pierwszym poleceniu jest używany polecenie cmdlet **Get-AzureSubscription** w celu uzyskania bieżącego identyfikatora subskrypcji, a następnie zapisanie go w zmiennej $SubId.</span><span class="sxs-lookup"><span data-stu-id="53a42-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="53a42-119">Drugie i trzecie polecenia cmdlet **Get-AzureStorageKey** umożliwiają uzyskiwanie podstawowych kluczy magazynu dla MyBlobStorage i MySecondBlobStorage, a następnie przechowywanie kluczy odpowiednio w zmiennych $Key 1 i $Key 2.</span><span class="sxs-lookup"><span data-stu-id="53a42-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="53a42-120">W przypadku czterech, piątych i szóstych poleceń Użyj polecenia cmdlet **Get-Credential** , aby uzyskać poświadczenia dla bieżącego abonamentu oraz dla Oozie i gałąź, a następnie zapisać poświadczenia w zmiennych.</span><span class="sxs-lookup"><span data-stu-id="53a42-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="53a42-121">Polecenie ostatnie wykonuje sekwencję operacji, korzystając z następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53a42-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="53a42-122">**New-AzureHDInsightClusterConfig** , aby utworzyć konfigurację klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="53a42-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="53a42-123">**Set-AzureHDInsightDefaultStorage** , aby ustawić domyślne konto magazynu dla konfiguracji na MyBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="53a42-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="53a42-124">**Add-AzureHDInsightStorage** , aby dodać do konfiguracji drugie konto magazynu o nazwie MySecondBlobStorage.blob.Core.Windows.NET.</span><span class="sxs-lookup"><span data-stu-id="53a42-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="53a42-125">**Add-AzureHDInsightMetastore** , aby dodać do konfiguracji element magazynu dla Oozie i magazynu.</span><span class="sxs-lookup"><span data-stu-id="53a42-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="53a42-126">**New-AzureHDInsightCluster** , aby utworzyć klaster usługi HDInsight z nową konfiguracją.</span><span class="sxs-lookup"><span data-stu-id="53a42-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="53a42-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53a42-127">PARAMETERS</span></span>

### <span data-ttu-id="53a42-128">-Config</span><span class="sxs-lookup"><span data-stu-id="53a42-128">-Config</span></span>
<span data-ttu-id="53a42-129">Określa obiekt konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="53a42-129">Specifies a configuration object.</span></span>
<span data-ttu-id="53a42-130">To polecenie cmdlet umożliwia dodanie informacji o sklepie do obiektu konfiguracji, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="53a42-130">This cmdlet adds metastore information to the configuration object that this parameter specifies.</span></span>

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

### <span data-ttu-id="53a42-131">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="53a42-131">-Credential</span></span>
<span data-ttu-id="53a42-132">Określa poświadczenia, które są używane do uzyskiwania dostępu do bazy danych programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="53a42-132">Specifies the credentials that are used to access a SQL Server database.</span></span>

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

### <span data-ttu-id="53a42-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="53a42-133">-DatabaseName</span></span>
<span data-ttu-id="53a42-134">Określa nazwę bazy danych, w której mają być przechowywane gałęzie lub metadane Oozie.</span><span class="sxs-lookup"><span data-stu-id="53a42-134">Specifies the name of the database to store Hive or Oozie metadata.</span></span>

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

### <span data-ttu-id="53a42-135">-Unstoretype</span><span class="sxs-lookup"><span data-stu-id="53a42-135">-MetastoreType</span></span>
<span data-ttu-id="53a42-136">Określa typ magazynu.</span><span class="sxs-lookup"><span data-stu-id="53a42-136">Specifies the metastore type.</span></span>
<span data-ttu-id="53a42-137">Dopuszczalne wartości tego parametru to: HiveMetaStore lub OozieMetaStore.</span><span class="sxs-lookup"><span data-stu-id="53a42-137">The acceptable values for this parameter are: HiveMetaStore or OozieMetaStore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a42-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="53a42-138">-Profile</span></span>
<span data-ttu-id="53a42-139">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53a42-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53a42-140">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="53a42-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53a42-141">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="53a42-141">-SqlAzureServerName</span></span>
<span data-ttu-id="53a42-142">Określa w pełni kwalifikowaną nazwę domeny (FQDN) serwera SQL, który zawiera bazę danych do przechowywania metadanych.</span><span class="sxs-lookup"><span data-stu-id="53a42-142">Specifies the fully qualified domain name (FQDN) of the SQL Server that contains the database to store metadata.</span></span>

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

### <span data-ttu-id="53a42-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a42-143">CommonParameters</span></span>
<span data-ttu-id="53a42-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a42-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a42-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53a42-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a42-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53a42-146">INPUTS</span></span>

## <span data-ttu-id="53a42-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53a42-147">OUTPUTS</span></span>

## <span data-ttu-id="53a42-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53a42-148">NOTES</span></span>

## <span data-ttu-id="53a42-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53a42-149">RELATED LINKS</span></span>

[<span data-ttu-id="53a42-150">Dodaj-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="53a42-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="53a42-151">Nowe — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="53a42-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="53a42-152">Nowe — AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="53a42-152">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="53a42-153">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="53a42-153">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
