---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 430c2aa7f38e6246c13ef6045f52346b580d20fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194347"
---
# <span data-ttu-id="677ad-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="677ad-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="677ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="677ad-102">SYNOPSIS</span></span>
<span data-ttu-id="677ad-103">Wyświetla listę hostów klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="677ad-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="677ad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="677ad-104">SYNTAX</span></span>

### <span data-ttu-id="677ad-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="677ad-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="677ad-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="677ad-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="677ad-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="677ad-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="677ad-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="677ad-108">DESCRIPTION</span></span>
<span data-ttu-id="677ad-109">Polecenie **cmdlet Get-AzHDInsightHost** wyświetla listę hostów klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="677ad-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="677ad-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="677ad-110">EXAMPLES</span></span>

### <span data-ttu-id="677ad-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="677ad-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="677ad-112">To polecenie zawiera listę hostów klastrów z nazwą klastrów.</span><span class="sxs-lookup"><span data-stu-id="677ad-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="677ad-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="677ad-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="677ad-114">To polecenie zawiera listę hostów klastrów z potokiem.</span><span class="sxs-lookup"><span data-stu-id="677ad-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="677ad-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="677ad-115">PARAMETERS</span></span>

### <span data-ttu-id="677ad-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="677ad-116">-ClusterName</span></span>
<span data-ttu-id="677ad-117">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="677ad-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="677ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677ad-118">-DefaultProfile</span></span>
<span data-ttu-id="677ad-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="677ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="677ad-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="677ad-120">-InputObject</span></span>
<span data-ttu-id="677ad-121">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="677ad-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="677ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="677ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="677ad-123">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="677ad-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="677ad-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="677ad-124">-ResourceId</span></span>
<span data-ttu-id="677ad-125">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="677ad-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="677ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677ad-126">CommonParameters</span></span>
<span data-ttu-id="677ad-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677ad-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="677ad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677ad-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="677ad-129">INPUTS</span></span>

### <span data-ttu-id="677ad-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="677ad-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="677ad-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="677ad-131">OUTPUTS</span></span>

### <span data-ttu-id="677ad-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="677ad-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="677ad-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="677ad-133">NOTES</span></span>

## <span data-ttu-id="677ad-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="677ad-134">RELATED LINKS</span></span>
