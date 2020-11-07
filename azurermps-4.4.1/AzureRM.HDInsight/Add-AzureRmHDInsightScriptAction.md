---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 51bfee17e33afcb93b90c36198e9352c3fca5fc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716692"
---
# <span data-ttu-id="c4bf7-101">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="c4bf7-101">Add-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="c4bf7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bf7-103">Umożliwia dodanie akcji skryptu do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-103">Adds a script action to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4bf7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4bf7-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4bf7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c4bf7-105">DESCRIPTION</span></span>
<span data-ttu-id="c4bf7-106">Polecenie cmdlet **Add-AzureRmHDInsightScriptAction** umożliwia dodanie akcji skryptu do obiektu konfiguracji usługi HDInsight utworzonego za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-106">The **Add-AzureRmHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

<span data-ttu-id="c4bf7-107">Akcje skryptu umożliwiają korzystanie z funkcji, które są używane w celu zainstalowania dodatkowego oprogramowania lub zmieniania konfiguracji aplikacji uruchomionych w klastrze usługi Hadoop przy użyciu programu Windows PowerShell lub skryptów bash (odpowiednio dla klastrów systemu Windows lub Linux).</span><span class="sxs-lookup"><span data-stu-id="c4bf7-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>

<span data-ttu-id="c4bf7-108">Akcja skryptu uruchamia się w węzłach klastra, gdy są wdrożone klastry usługi HDInsight i są uruchamiane po zakończeniu konfigurowania usługi HDInsight w klastrze.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="c4bf7-109">Akcja skryptu jest uruchamiana w obszarze uprawnienia konta administratora systemu i zapewnia pełne prawa dostępu do węzłów klastra.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="c4bf7-110">Możesz udostępnić każdemu klastrowi listę akcji skryptów do uruchomienia w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="c4bf7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4bf7-111">EXAMPLES</span></span>

### <span data-ttu-id="c4bf7-112">Przykład 1: Dodawanie akcji skryptu do obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="c4bf7-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


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
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
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

<span data-ttu-id="c4bf7-113">To polecenie umożliwia dodanie akcji skryptu dotyczącej węzłów głowy i procesu roboczego klastra programu-Hadoop-001, który ma być uruchomiony na końcu tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="c4bf7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4bf7-114">PARAMETERS</span></span>

### <span data-ttu-id="c4bf7-115">-Config</span><span class="sxs-lookup"><span data-stu-id="c4bf7-115">-Config</span></span>
<span data-ttu-id="c4bf7-116">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="c4bf7-117">Ten obiekt jest tworzony przez polecenie cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="c4bf7-117">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="c4bf7-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4bf7-118">-Name</span></span>
<span data-ttu-id="c4bf7-119">Określa nazwę akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-119">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="c4bf7-120">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c4bf7-120">-NodeType</span></span>
<span data-ttu-id="c4bf7-121">Określa typ węzła, na którym ma zostać uruchomiona akcja skryptu.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-121">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="c4bf7-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c4bf7-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4bf7-123">HeadNode</span><span class="sxs-lookup"><span data-stu-id="c4bf7-123">HeadNode</span></span>
- <span data-ttu-id="c4bf7-124">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="c4bf7-124">WorkerNode</span></span>
- <span data-ttu-id="c4bf7-125">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="c4bf7-125">ZookeeperNode</span></span>

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

### <span data-ttu-id="c4bf7-126">— Parametry</span><span class="sxs-lookup"><span data-stu-id="c4bf7-126">-Parameters</span></span>
<span data-ttu-id="c4bf7-127">Określa parametry akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-127">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="c4bf7-128">-URI</span><span class="sxs-lookup"><span data-stu-id="c4bf7-128">-Uri</span></span>
<span data-ttu-id="c4bf7-129">Określa publiczny identyfikator URI akcji skryptu (programu PowerShell lub skryptu bash).</span><span class="sxs-lookup"><span data-stu-id="c4bf7-129">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="c4bf7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bf7-130">-DefaultProfile</span></span>
<span data-ttu-id="c4bf7-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bf7-132">CommonParameters</span></span>
<span data-ttu-id="c4bf7-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4bf7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bf7-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4bf7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bf7-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4bf7-135">INPUTS</span></span>

### <span data-ttu-id="c4bf7-136">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c4bf7-136">AzureHDInsightConfig</span></span>
<span data-ttu-id="c4bf7-137">Parametr "config" akceptuje wartość typu "AzureHDInsightConfig" z procesu</span><span class="sxs-lookup"><span data-stu-id="c4bf7-137">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="c4bf7-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4bf7-138">OUTPUTS</span></span>

### <span data-ttu-id="c4bf7-139">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c4bf7-139">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c4bf7-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4bf7-140">NOTES</span></span>

## <span data-ttu-id="c4bf7-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4bf7-141">RELATED LINKS</span></span>

[<span data-ttu-id="c4bf7-142">Nowe — AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c4bf7-142">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


