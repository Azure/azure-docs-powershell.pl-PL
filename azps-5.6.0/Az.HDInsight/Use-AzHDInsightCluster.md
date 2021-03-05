---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: c9b95a1f16c90eb3c6e057707dbf63d431b9a1ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013553"
---
# <span data-ttu-id="d3ec0-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d3ec0-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="d3ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ec0-103">Wybiera klaster, który ma być używany z Invoke-RmAzureHDInsightHiveJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3ec0-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="d3ec0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3ec0-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3ec0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3ec0-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ec0-106">Polecenie **cmdlet Use-AzHDInsightCluster** wybiera klaster usługi Azure HDInsight dla polecenia cmdlet Invoke-AzHDInsightHiveJob, które będzie używać do przesyłania zadań Wiewisko.</span><span class="sxs-lookup"><span data-stu-id="d3ec0-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="d3ec0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3ec0-107">EXAMPLES</span></span>

### <span data-ttu-id="d3ec0-108">Przykład 1. Wybieranie klastrów dla przesyłania zapytań Przez program Gałąź</span><span class="sxs-lookup"><span data-stu-id="d3ec0-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="d3ec0-109">To polecenie wybiera klaster na przesyłanie zapytania w programie Sqle.</span><span class="sxs-lookup"><span data-stu-id="d3ec0-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="d3ec0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3ec0-110">PARAMETERS</span></span>

### <span data-ttu-id="d3ec0-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d3ec0-111">-ClusterName</span></span>
<span data-ttu-id="d3ec0-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d3ec0-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ec0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ec0-113">-DefaultProfile</span></span>
<span data-ttu-id="d3ec0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d3ec0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3ec0-115">- HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d3ec0-115">-HttpCredential</span></span>
<span data-ttu-id="d3ec0-116">Określa poświadczenia logowania klastrów (HTTP) dla tego klastra.</span><span class="sxs-lookup"><span data-stu-id="d3ec0-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ec0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3ec0-117">-ResourceGroupName</span></span>
<span data-ttu-id="d3ec0-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3ec0-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ec0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ec0-119">CommonParameters</span></span>
<span data-ttu-id="d3ec0-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ec0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ec0-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3ec0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ec0-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3ec0-122">INPUTS</span></span>

### <span data-ttu-id="d3ec0-123">Brak</span><span class="sxs-lookup"><span data-stu-id="d3ec0-123">None</span></span>

## <span data-ttu-id="d3ec0-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3ec0-124">OUTPUTS</span></span>

### <span data-ttu-id="d3ec0-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d3ec0-125">System.String</span></span>

## <span data-ttu-id="d3ec0-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3ec0-126">NOTES</span></span>

## <span data-ttu-id="d3ec0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3ec0-127">RELATED LINKS</span></span>

[<span data-ttu-id="d3ec0-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d3ec0-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="d3ec0-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d3ec0-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


