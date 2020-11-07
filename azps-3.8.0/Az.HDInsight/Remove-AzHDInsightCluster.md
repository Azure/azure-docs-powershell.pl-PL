---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896681"
---
# <span data-ttu-id="dd8ad-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dd8ad-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="dd8ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8ad-103">Umożliwia usunięcie określonego klastra usługi HDInsight z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dd8ad-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="dd8ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd8ad-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd8ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd8ad-105">DESCRIPTION</span></span>
<span data-ttu-id="dd8ad-106">Polecenie cmdlet **Remove-AzHDInsightCluster** umożliwia usunięcie określonego klastra usługi HDInsight z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dd8ad-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="dd8ad-107">Ta operacja usuwa również wszystkie dane przechowywane w systemie plików HDFS (Distributed File System) usługi Hadoop w klastrze.</span><span class="sxs-lookup"><span data-stu-id="dd8ad-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="dd8ad-108">Dane przechowywane na skojarzonym koncie usługi Azure Storage nie są usuwane.</span><span class="sxs-lookup"><span data-stu-id="dd8ad-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="dd8ad-109">Dane przechowywane w zewnętrznych magazynach strumieniowych nie są usuwane.</span><span class="sxs-lookup"><span data-stu-id="dd8ad-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="dd8ad-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd8ad-110">EXAMPLES</span></span>

### <span data-ttu-id="dd8ad-111">Przykład 1: usuwanie klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="dd8ad-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="dd8ad-112">To polecenie powoduje usunięcie klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="dd8ad-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="dd8ad-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd8ad-113">PARAMETERS</span></span>

### <span data-ttu-id="dd8ad-114">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="dd8ad-114">-ClusterName</span></span>
<span data-ttu-id="dd8ad-115">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="dd8ad-115">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8ad-116">-DefaultProfile</span></span>
<span data-ttu-id="dd8ad-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dd8ad-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8ad-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8ad-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd8ad-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd8ad-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8ad-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd8ad-120">-PassThru</span></span>
<span data-ttu-id="dd8ad-121">Jeśli PassThru jest obecny, wynik</span><span class="sxs-lookup"><span data-stu-id="dd8ad-121">If PassThru is present, output the result</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8ad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8ad-122">CommonParameters</span></span>
<span data-ttu-id="dd8ad-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8ad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8ad-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd8ad-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8ad-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd8ad-125">INPUTS</span></span>

### <span data-ttu-id="dd8ad-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dd8ad-126">None</span></span>
## <span data-ttu-id="dd8ad-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd8ad-127">OUTPUTS</span></span>

### <span data-ttu-id="dd8ad-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd8ad-128">System.Boolean</span></span>
## <span data-ttu-id="dd8ad-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd8ad-129">NOTES</span></span>

## <span data-ttu-id="dd8ad-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd8ad-130">RELATED LINKS</span></span>

[<span data-ttu-id="dd8ad-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dd8ad-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="dd8ad-132">Użyj — AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dd8ad-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


