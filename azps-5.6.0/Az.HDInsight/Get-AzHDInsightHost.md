---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 5b58e535acae8d6d0845b6be8c838f8372af9c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012113"
---
# <span data-ttu-id="e1dbd-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="e1dbd-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="e1dbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e1dbd-103">Wyświetla listę hostów klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="e1dbd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1dbd-104">SYNTAX</span></span>

### <span data-ttu-id="e1dbd-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e1dbd-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1dbd-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1dbd-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1dbd-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1dbd-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1dbd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1dbd-108">DESCRIPTION</span></span>
<span data-ttu-id="e1dbd-109">Polecenie **cmdlet Get-AzHDInsightHost** wyświetla listę hostów klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="e1dbd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1dbd-110">EXAMPLES</span></span>

### <span data-ttu-id="e1dbd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e1dbd-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="e1dbd-112">To polecenie zawiera listę hostów klastrów z nazwą klastrów.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="e1dbd-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e1dbd-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="e1dbd-114">To polecenie zawiera listę hostów klastrów z potokiem.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="e1dbd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1dbd-115">PARAMETERS</span></span>

### <span data-ttu-id="e1dbd-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e1dbd-116">-ClusterName</span></span>
<span data-ttu-id="e1dbd-117">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dbd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1dbd-118">-DefaultProfile</span></span>
<span data-ttu-id="e1dbd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1dbd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1dbd-120">-InputObject</span></span>
<span data-ttu-id="e1dbd-121">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1dbd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1dbd-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1dbd-123">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dbd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1dbd-124">-ResourceId</span></span>
<span data-ttu-id="e1dbd-125">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1dbd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1dbd-126">CommonParameters</span></span>
<span data-ttu-id="e1dbd-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1dbd-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1dbd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1dbd-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1dbd-129">INPUTS</span></span>

### <span data-ttu-id="e1dbd-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e1dbd-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="e1dbd-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1dbd-131">OUTPUTS</span></span>

### <span data-ttu-id="e1dbd-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="e1dbd-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="e1dbd-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1dbd-133">NOTES</span></span>

## <span data-ttu-id="e1dbd-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1dbd-134">RELATED LINKS</span></span>
