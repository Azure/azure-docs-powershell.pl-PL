---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: f43e484d4e4ced7aadcc1fc7916cefb6e34784df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705350"
---
# <span data-ttu-id="7e0f9-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="7e0f9-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="7e0f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0f9-103">Dodaje bazę danych SQL do obiektu konfiguracji klastra jako gałąź lub Oozie datastore.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="7e0f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e0f9-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e0f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7e0f9-105">DESCRIPTION</span></span>
<span data-ttu-id="7e0f9-106">Polecenie cmdlet **Add-AzHDInsightMetastore** powoduje dodanie gałęzi lub Oozie w obiekcie konfiguracji usługi HDInsight utworzonego przez polecenie cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="7e0f9-107">Metadata to baza danych SQL, która może służyć do przechowywania metadanych gałęzi, Oozie lub obu.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="7e0f9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e0f9-108">EXAMPLES</span></span>

### <span data-ttu-id="7e0f9-109">Przykład 1: Dodawanie magazynu bazy danych SQL do obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="7e0f9-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
            | New-AzHDInsightCluster `
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

<span data-ttu-id="7e0f9-110">To polecenie umożliwia dodanie magazynu bazy danych SQL do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="7e0f9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e0f9-111">PARAMETERS</span></span>

### <span data-ttu-id="7e0f9-112">-Config</span><span class="sxs-lookup"><span data-stu-id="7e0f9-112">-Config</span></span>
<span data-ttu-id="7e0f9-113">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="7e0f9-114">Ten obiekt jest tworzony przez polecenie cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="7e0f9-114">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0f9-115">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="7e0f9-115">-Credential</span></span>
<span data-ttu-id="7e0f9-116">Określa poświadczenia, które mają być używane dla bazy danych serwera AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0f9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e0f9-117">-DatabaseName</span></span>
<span data-ttu-id="7e0f9-118">Określa bazę danych w wystąpieniu serwera AzureSQL, która ma być używana dla tego magazynu.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0f9-119">-DefaultProfile</span></span>
<span data-ttu-id="7e0f9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7e0f9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0f9-121">-Unstoretype</span><span class="sxs-lookup"><span data-stu-id="7e0f9-121">-MetastoreType</span></span>
<span data-ttu-id="7e0f9-122">Umożliwia określenie typu magazynu.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="7e0f9-123">Możliwe wartości to HiveMetastore lub OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0f9-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="7e0f9-124">-SqlAzureServerName</span></span>
<span data-ttu-id="7e0f9-125">Określa wystąpienie serwera AzureSQL, które ma być używane dla tego magazynu.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0f9-126">CommonParameters</span></span>
<span data-ttu-id="7e0f9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0f9-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e0f9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0f9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e0f9-129">INPUTS</span></span>

### <span data-ttu-id="7e0f9-130">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="7e0f9-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="7e0f9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e0f9-131">OUTPUTS</span></span>

### <span data-ttu-id="7e0f9-132">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="7e0f9-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="7e0f9-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e0f9-133">NOTES</span></span>

## <span data-ttu-id="7e0f9-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e0f9-134">RELATED LINKS</span></span>

[<span data-ttu-id="7e0f9-135">Nowe — AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="7e0f9-135">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


