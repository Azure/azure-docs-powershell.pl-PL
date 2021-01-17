---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: 2759059da9bc37f942eaa733319539bc1fa53b5b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350221"
---
# <span data-ttu-id="45f6b-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="45f6b-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="45f6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="45f6b-103">Umożliwia dodanie akcji skryptu do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="45f6b-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="45f6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45f6b-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45f6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45f6b-105">DESCRIPTION</span></span>
<span data-ttu-id="45f6b-106">Polecenie cmdlet **Add-AzHDInsightScriptAction** umożliwia dodanie akcji skryptu do obiektu konfiguracji usługi HDInsight utworzonego za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="45f6b-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="45f6b-107">Akcje skryptu umożliwiają korzystanie z funkcji, które są używane w celu zainstalowania dodatkowego oprogramowania lub zmieniania konfiguracji aplikacji uruchomionych w klastrze usługi Hadoop przy użyciu programu Windows PowerShell lub skryptów bash (odpowiednio dla klastrów systemu Windows lub Linux).</span><span class="sxs-lookup"><span data-stu-id="45f6b-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="45f6b-108">Akcja skryptu uruchamia się w węzłach klastra, gdy są wdrożone klastry usługi HDInsight i są uruchamiane po zakończeniu konfigurowania usługi HDInsight w klastrze.</span><span class="sxs-lookup"><span data-stu-id="45f6b-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="45f6b-109">Akcja skryptu jest uruchamiana w obszarze uprawnienia konta administratora systemu i zapewnia pełne prawa dostępu do węzłów klastra.</span><span class="sxs-lookup"><span data-stu-id="45f6b-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="45f6b-110">Możesz udostępnić każdemu klastrowi listę akcji skryptów do uruchomienia w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="45f6b-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="45f6b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45f6b-111">EXAMPLES</span></span>

### <span data-ttu-id="45f6b-112">Przykład 1: Dodawanie akcji skryptu do obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="45f6b-112">Example 1: Add a script action to the cluster configuration object</span></span>
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

<span data-ttu-id="45f6b-113">To polecenie umożliwia dodanie akcji skryptu dotyczącej węzłów głowy i procesu roboczego klastra programu-Hadoop-001, który ma być uruchomiony na końcu tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="45f6b-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="45f6b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45f6b-114">PARAMETERS</span></span>

### <span data-ttu-id="45f6b-115">-Config</span><span class="sxs-lookup"><span data-stu-id="45f6b-115">-Config</span></span>
<span data-ttu-id="45f6b-116">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45f6b-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="45f6b-117">Ten obiekt jest tworzony przez polecenie cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="45f6b-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="45f6b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45f6b-118">-DefaultProfile</span></span>
<span data-ttu-id="45f6b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="45f6b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45f6b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45f6b-120">-Name</span></span>
<span data-ttu-id="45f6b-121">Określa nazwę akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="45f6b-121">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="45f6b-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="45f6b-122">-NodeType</span></span>
<span data-ttu-id="45f6b-123">Określa typ węzła, na którym ma zostać uruchomiona akcja skryptu.</span><span class="sxs-lookup"><span data-stu-id="45f6b-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="45f6b-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="45f6b-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45f6b-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="45f6b-125">HeadNode</span></span>
- <span data-ttu-id="45f6b-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="45f6b-126">WorkerNode</span></span>
- <span data-ttu-id="45f6b-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="45f6b-127">ZookeeperNode</span></span>

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

### <span data-ttu-id="45f6b-128">— Parametry</span><span class="sxs-lookup"><span data-stu-id="45f6b-128">-Parameters</span></span>
<span data-ttu-id="45f6b-129">Określa parametry akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="45f6b-129">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="45f6b-130">-URI</span><span class="sxs-lookup"><span data-stu-id="45f6b-130">-Uri</span></span>
<span data-ttu-id="45f6b-131">Określa publiczny identyfikator URI akcji skryptu (programu PowerShell lub skryptu bash).</span><span class="sxs-lookup"><span data-stu-id="45f6b-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="45f6b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45f6b-132">CommonParameters</span></span>
<span data-ttu-id="45f6b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45f6b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45f6b-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45f6b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45f6b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45f6b-135">INPUTS</span></span>

### <span data-ttu-id="45f6b-136">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="45f6b-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="45f6b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45f6b-137">OUTPUTS</span></span>

### <span data-ttu-id="45f6b-138">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="45f6b-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="45f6b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45f6b-139">NOTES</span></span>

## <span data-ttu-id="45f6b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45f6b-140">RELATED LINKS</span></span>

[<span data-ttu-id="45f6b-141">Nowe — AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="45f6b-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


