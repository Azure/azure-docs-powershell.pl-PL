---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 2e9e8858e79521c32cdf08b980584fd2b77dd955
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224339"
---
# <span data-ttu-id="f458c-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="f458c-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="f458c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f458c-102">SYNOPSIS</span></span>
<span data-ttu-id="f458c-103">Wyświetla listę hostów klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f458c-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="f458c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f458c-104">SYNTAX</span></span>

### <span data-ttu-id="f458c-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f458c-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f458c-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f458c-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f458c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f458c-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [[-DefaultProfile] <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f458c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f458c-108">DESCRIPTION</span></span>
<span data-ttu-id="f458c-109">Polecenie cmdlet **Get-AzHDInsightHost** zawiera listę hostów klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f458c-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="f458c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f458c-110">EXAMPLES</span></span>

### <span data-ttu-id="f458c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f458c-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="f458c-112">To polecenie wyświetla listę hostów klastra z nazwą klastra.</span><span class="sxs-lookup"><span data-stu-id="f458c-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="f458c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f458c-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="f458c-114">To polecenie wyświetla listę hostów klastra z potokiem.</span><span class="sxs-lookup"><span data-stu-id="f458c-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="f458c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f458c-115">PARAMETERS</span></span>

### <span data-ttu-id="f458c-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="f458c-116">-ClusterName</span></span>
<span data-ttu-id="f458c-117">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="f458c-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="f458c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f458c-118">-DefaultProfile</span></span>
<span data-ttu-id="f458c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f458c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f458c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f458c-120">-InputObject</span></span>
<span data-ttu-id="f458c-121">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="f458c-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="f458c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f458c-122">-ResourceGroupName</span></span>
<span data-ttu-id="f458c-123">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f458c-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="f458c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f458c-124">-ResourceId</span></span>
<span data-ttu-id="f458c-125">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f458c-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="f458c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f458c-126">CommonParameters</span></span>
<span data-ttu-id="f458c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f458c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f458c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f458c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f458c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f458c-129">INPUTS</span></span>

### <span data-ttu-id="f458c-130">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f458c-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="f458c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f458c-131">OUTPUTS</span></span>

### <span data-ttu-id="f458c-132">Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="f458c-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="f458c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f458c-133">NOTES</span></span>

## <span data-ttu-id="f458c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f458c-134">RELATED LINKS</span></span>
