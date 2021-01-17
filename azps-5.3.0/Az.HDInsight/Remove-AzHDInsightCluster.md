---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: ab97162fb2651bce8e242ca0cef7b497ffcf1bef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489597"
---
# <span data-ttu-id="91f38-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="91f38-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="91f38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91f38-102">SYNOPSIS</span></span>
<span data-ttu-id="91f38-103">Umożliwia usunięcie określonego klastra usługi HDInsight z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="91f38-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="91f38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91f38-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91f38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="91f38-105">DESCRIPTION</span></span>
<span data-ttu-id="91f38-106">Polecenie cmdlet **Remove-AzHDInsightCluster** umożliwia usunięcie określonego klastra usługi HDInsight z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="91f38-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="91f38-107">Ta operacja usuwa również wszystkie dane przechowywane w systemie plików HDFS (Distributed File System) usługi Hadoop w klastrze.</span><span class="sxs-lookup"><span data-stu-id="91f38-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="91f38-108">Dane przechowywane na skojarzonym koncie usługi Azure Storage nie są usuwane.</span><span class="sxs-lookup"><span data-stu-id="91f38-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="91f38-109">Dane przechowywane w zewnętrznych magazynach strumieniowych nie są usuwane.</span><span class="sxs-lookup"><span data-stu-id="91f38-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="91f38-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91f38-110">EXAMPLES</span></span>

### <span data-ttu-id="91f38-111">Przykład 1: usuwanie klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="91f38-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="91f38-112">To polecenie powoduje usunięcie klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="91f38-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="91f38-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91f38-113">PARAMETERS</span></span>

### <span data-ttu-id="91f38-114">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="91f38-114">-ClusterName</span></span>
<span data-ttu-id="91f38-115">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="91f38-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="91f38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f38-116">-DefaultProfile</span></span>
<span data-ttu-id="91f38-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="91f38-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91f38-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91f38-118">-PassThru</span></span>
<span data-ttu-id="91f38-119">Jeśli PassThru jest obecny, wynik</span><span class="sxs-lookup"><span data-stu-id="91f38-119">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="91f38-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f38-120">-ResourceGroupName</span></span>
<span data-ttu-id="91f38-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91f38-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="91f38-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f38-122">CommonParameters</span></span>
<span data-ttu-id="91f38-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f38-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f38-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91f38-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f38-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91f38-125">INPUTS</span></span>

### <span data-ttu-id="91f38-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="91f38-126">None</span></span>
## <span data-ttu-id="91f38-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91f38-127">OUTPUTS</span></span>

### <span data-ttu-id="91f38-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91f38-128">System.Boolean</span></span>
## <span data-ttu-id="91f38-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91f38-129">NOTES</span></span>

## <span data-ttu-id="91f38-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91f38-130">RELATED LINKS</span></span>

[<span data-ttu-id="91f38-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="91f38-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="91f38-132">Użyj — AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="91f38-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


