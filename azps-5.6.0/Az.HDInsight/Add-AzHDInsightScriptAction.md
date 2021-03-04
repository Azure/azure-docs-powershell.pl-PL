---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: f80ac8dda086910cf83e1d010f2878b6e4ba9362
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990158"
---
# <span data-ttu-id="5c527-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="5c527-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="5c527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c527-102">SYNOPSIS</span></span>
<span data-ttu-id="5c527-103">Dodaje akcję skryptu do obiektu konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="5c527-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="5c527-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5c527-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c527-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5c527-105">DESCRIPTION</span></span>
<span data-ttu-id="5c527-106">Polecenie **cmdlet Add-AzHDInsightScriptAction** dodaje akcje skryptów do obiektu konfiguracji usługi HDInsight utworzonego przez New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c527-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="5c527-107">Akcje skryptów zapewniają funkcje służące do instalowania dodatkowego oprogramowania lub zmieniania konfiguracji aplikacji uruchamianych w klastrze Usługi Hadoop przy użyciu skryptów Windows PowerShell lub Bash (odpowiednio dla klastrów systemu Windows lub Systemu Linux).</span><span class="sxs-lookup"><span data-stu-id="5c527-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="5c527-108">Akcja skryptu jest uruchamiana w węzłach klastrów po wdrożeniu klastrów HDInsight i jest uruchamiana po węzłach w pełnej konfiguracji usługi HDInsight klastrów.</span><span class="sxs-lookup"><span data-stu-id="5c527-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="5c527-109">Akcja skryptu jest uruchamiana administrator systemu uprawnień konta i zapewnia pełne prawa dostępu do węzłów klastrów.</span><span class="sxs-lookup"><span data-stu-id="5c527-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="5c527-110">Każdemu klastrowi można udostępnić listę akcji skryptów do uruchomienia w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="5c527-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="5c527-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5c527-111">EXAMPLES</span></span>

### <span data-ttu-id="5c527-112">Przykład 1. Dodawanie akcji skryptu do obiektu konfiguracji klastrów</span><span class="sxs-lookup"><span data-stu-id="5c527-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="5c527-113">To polecenie dodaje akcję skryptu dla węzłów Head and Worker w klastrze Twoja-hadoop-001, która zostanie uruchamiana po zakończeniu tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="5c527-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="5c527-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c527-114">PARAMETERS</span></span>

### <span data-ttu-id="5c527-115">-Config</span><span class="sxs-lookup"><span data-stu-id="5c527-115">-Config</span></span>
<span data-ttu-id="5c527-116">Określa obiekt konfiguracji klastrów HDInsight, który modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c527-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="5c527-117">Ten obiekt jest tworzony przez polecenie cmdlet **New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="5c527-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="5c527-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c527-118">-DefaultProfile</span></span>
<span data-ttu-id="5c527-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5c527-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c527-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5c527-120">-Name</span></span>
<span data-ttu-id="5c527-121">Określa nazwę akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="5c527-121">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="5c527-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="5c527-122">-NodeType</span></span>
<span data-ttu-id="5c527-123">Określa typ węzła, w którym ma być uruchamiana akcja skryptu.</span><span class="sxs-lookup"><span data-stu-id="5c527-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="5c527-124">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5c527-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c527-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="5c527-125">HeadNode</span></span>
- <span data-ttu-id="5c527-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="5c527-126">WorkerNode</span></span>
- <span data-ttu-id="5c527-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="5c527-127">ZookeeperNode</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c527-128">— Parametry</span><span class="sxs-lookup"><span data-stu-id="5c527-128">-Parameters</span></span>
<span data-ttu-id="5c527-129">Określa parametry akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="5c527-129">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c527-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="5c527-130">-Uri</span></span>
<span data-ttu-id="5c527-131">Określa publiczny URI dla akcji skryptu (skryptu PowerShell lub Bash).</span><span class="sxs-lookup"><span data-stu-id="5c527-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c527-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c527-132">CommonParameters</span></span>
<span data-ttu-id="5c527-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c527-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c527-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c527-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c527-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c527-135">INPUTS</span></span>

### <span data-ttu-id="5c527-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="5c527-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="5c527-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c527-137">OUTPUTS</span></span>

### <span data-ttu-id="5c527-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="5c527-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="5c527-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5c527-139">NOTES</span></span>

## <span data-ttu-id="5c527-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c527-140">RELATED LINKS</span></span>

[<span data-ttu-id="5c527-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5c527-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


