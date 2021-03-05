---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: 5baf67bfec2c4e18e718241dbb973bb8b2050bbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965898"
---
# <span data-ttu-id="5bf62-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5bf62-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="5bf62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bf62-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf62-103">Usuwa określony klaster USŁUGI HDInsight z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5bf62-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="5bf62-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5bf62-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bf62-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5bf62-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf62-106">Polecenie **cmdlet Remove-AzHDInsightCluster** usuwa określony klaster usługi HDInsight z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5bf62-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="5bf62-107">Ta operacja powoduje również usunięcie wszystkich danych przechowywanych w systemie plików HDFS (Hadoop Distributed File System) w klastrze.</span><span class="sxs-lookup"><span data-stu-id="5bf62-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="5bf62-108">Dane przechowywane na skojarzonym koncie usługi Azure Storage nie są usuwane.</span><span class="sxs-lookup"><span data-stu-id="5bf62-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="5bf62-109">Dane przechowywane w zewnętrznych metastorech nie są usuwane.</span><span class="sxs-lookup"><span data-stu-id="5bf62-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="5bf62-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5bf62-110">EXAMPLES</span></span>

### <span data-ttu-id="5bf62-111">Przykład 1. Usuwanie klastrów usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="5bf62-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="5bf62-112">To polecenie usuwa klaster o nazwie Twoja-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="5bf62-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="5bf62-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bf62-113">PARAMETERS</span></span>

### <span data-ttu-id="5bf62-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5bf62-114">-ClusterName</span></span>
<span data-ttu-id="5bf62-115">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="5bf62-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5bf62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf62-116">-DefaultProfile</span></span>
<span data-ttu-id="5bf62-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5bf62-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bf62-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bf62-118">-PassThru</span></span>
<span data-ttu-id="5bf62-119">Jeśli passthru jest obecne, wyeksymuj wynik</span><span class="sxs-lookup"><span data-stu-id="5bf62-119">If PassThru is present, output the result</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf62-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf62-120">-ResourceGroupName</span></span>
<span data-ttu-id="5bf62-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5bf62-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5bf62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf62-122">CommonParameters</span></span>
<span data-ttu-id="5bf62-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf62-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bf62-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf62-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bf62-125">INPUTS</span></span>

### <span data-ttu-id="5bf62-126">Brak</span><span class="sxs-lookup"><span data-stu-id="5bf62-126">None</span></span>
## <span data-ttu-id="5bf62-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bf62-127">OUTPUTS</span></span>

### <span data-ttu-id="5bf62-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bf62-128">System.Boolean</span></span>
## <span data-ttu-id="5bf62-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5bf62-129">NOTES</span></span>

## <span data-ttu-id="5bf62-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bf62-130">RELATED LINKS</span></span>

[<span data-ttu-id="5bf62-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5bf62-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="5bf62-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5bf62-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


