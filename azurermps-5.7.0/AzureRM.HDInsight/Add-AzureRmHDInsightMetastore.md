---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
ms.openlocfilehash: bc9b5a05111fff64b41400093d1f9c1ba3c2df8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544323"
---
# <span data-ttu-id="3029e-101">Add-AzureRmHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="3029e-101">Add-AzureRmHDInsightMetastore</span></span>

## <span data-ttu-id="3029e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3029e-102">SYNOPSIS</span></span>
<span data-ttu-id="3029e-103">Dodaje bazę danych SQL do obiektu konfiguracji klastra jako gałąź lub Oozie datastore.</span><span class="sxs-lookup"><span data-stu-id="3029e-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3029e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3029e-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3029e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3029e-105">DESCRIPTION</span></span>
<span data-ttu-id="3029e-106">Polecenie cmdlet **Add-AzureRmHDInsightMetastore** powoduje dodanie gałęzi lub Oozie w obiekcie konfiguracji usługi HDInsight utworzonego przez polecenie cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="3029e-106">The **Add-AzureRmHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="3029e-107">Metadata to baza danych SQL, która może służyć do przechowywania metadanych gałęzi, Oozie lub obu.</span><span class="sxs-lookup"><span data-stu-id="3029e-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="3029e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3029e-108">EXAMPLES</span></span>

### <span data-ttu-id="3029e-109">Przykład 1: Dodawanie magazynu bazy danych SQL do obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="3029e-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="3029e-110">To polecenie umożliwia dodanie magazynu bazy danych SQL do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="3029e-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="3029e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3029e-111">PARAMETERS</span></span>

### <span data-ttu-id="3029e-112">-Config</span><span class="sxs-lookup"><span data-stu-id="3029e-112">-Config</span></span>
<span data-ttu-id="3029e-113">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3029e-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3029e-114">Ten obiekt jest tworzony przez polecenie cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="3029e-114">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3029e-115">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="3029e-115">-Credential</span></span>
<span data-ttu-id="3029e-116">Określa poświadczenia, które mają być używane dla bazy danych serwera AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="3029e-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3029e-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3029e-117">-DatabaseName</span></span>
<span data-ttu-id="3029e-118">Określa bazę danych w wystąpieniu serwera AzureSQL, która ma być używana dla tego magazynu.</span><span class="sxs-lookup"><span data-stu-id="3029e-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3029e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3029e-119">-DefaultProfile</span></span>
<span data-ttu-id="3029e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3029e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3029e-121">-Unstoretype</span><span class="sxs-lookup"><span data-stu-id="3029e-121">-MetastoreType</span></span>
<span data-ttu-id="3029e-122">Umożliwia określenie typu magazynu.</span><span class="sxs-lookup"><span data-stu-id="3029e-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="3029e-123">Możliwe wartości to HiveMetastore lub OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="3029e-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3029e-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="3029e-124">-SqlAzureServerName</span></span>
<span data-ttu-id="3029e-125">Określa wystąpienie serwera AzureSQL, które ma być używane dla tego magazynu.</span><span class="sxs-lookup"><span data-stu-id="3029e-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3029e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3029e-126">CommonParameters</span></span>
<span data-ttu-id="3029e-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3029e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3029e-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3029e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3029e-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3029e-129">INPUTS</span></span>

### <span data-ttu-id="3029e-130">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3029e-130">AzureHDInsightConfig</span></span>
<span data-ttu-id="3029e-131">Parametr "config" akceptuje wartość typu "AzureHDInsightConfig" z procesu</span><span class="sxs-lookup"><span data-stu-id="3029e-131">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="3029e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3029e-132">OUTPUTS</span></span>

### <span data-ttu-id="3029e-133">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3029e-133">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3029e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3029e-134">NOTES</span></span>

## <span data-ttu-id="3029e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3029e-135">RELATED LINKS</span></span>

[<span data-ttu-id="3029e-136">Nowe — AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3029e-136">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


