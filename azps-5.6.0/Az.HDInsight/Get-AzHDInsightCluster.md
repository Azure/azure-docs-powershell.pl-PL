---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: c89293ee071aba3fcec2d58d071714193cc44a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010481"
---
# <span data-ttu-id="253d6-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="253d6-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="253d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="253d6-102">SYNOPSIS</span></span>
<span data-ttu-id="253d6-103">Pobiera i wyświetla wszystkie klastry usługi Azure HDInsight skojarzone z bieżącą subskrypcją lub określoną grupą zasobów albo pobiera określony klaster.</span><span class="sxs-lookup"><span data-stu-id="253d6-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="253d6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="253d6-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="253d6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="253d6-105">DESCRIPTION</span></span>
<span data-ttu-id="253d6-106">Polecenie **cmdlet Get-AzHDInsightCluster** wyświetla listę klastrów usługi Azure HDInsight dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="253d6-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="253d6-107">Użyj *parametru ClusterName,* aby uzyskać szczegółowe informacje dotyczące określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="253d6-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="253d6-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="253d6-108">EXAMPLES</span></span>

### <span data-ttu-id="253d6-109">Przykład 1. Lista wszystkich grup usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="253d6-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="253d6-110">To polecenie zawiera listę wszystkich klastrów usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="253d6-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="253d6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="253d6-111">PARAMETERS</span></span>

### <span data-ttu-id="253d6-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="253d6-112">-ClusterName</span></span>
<span data-ttu-id="253d6-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="253d6-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="253d6-114">-DefaultProfile</span></span>
<span data-ttu-id="253d6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="253d6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="253d6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="253d6-116">-ResourceGroupName</span></span>
<span data-ttu-id="253d6-117">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="253d6-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253d6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="253d6-118">CommonParameters</span></span>
<span data-ttu-id="253d6-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="253d6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="253d6-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="253d6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="253d6-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="253d6-121">INPUTS</span></span>

### <span data-ttu-id="253d6-122">Brak</span><span class="sxs-lookup"><span data-stu-id="253d6-122">None</span></span>

## <span data-ttu-id="253d6-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="253d6-123">OUTPUTS</span></span>

### <span data-ttu-id="253d6-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="253d6-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="253d6-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="253d6-125">NOTES</span></span>

## <span data-ttu-id="253d6-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="253d6-126">RELATED LINKS</span></span>

[<span data-ttu-id="253d6-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="253d6-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="253d6-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="253d6-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


