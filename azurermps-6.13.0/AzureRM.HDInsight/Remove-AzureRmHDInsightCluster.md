---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: aba2f1d2b5162e84c4765939195ce64214161a79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718881"
---
# <span data-ttu-id="8e6bd-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8e6bd-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="8e6bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="8e6bd-103">Umożliwia usunięcie określonego klastra usługi HDInsight z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e6bd-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e6bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e6bd-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e6bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8e6bd-105">DESCRIPTION</span></span>
<span data-ttu-id="8e6bd-106">Polecenie cmdlet **Remove-AzureRmHDInsightCluster** umożliwia usunięcie określonego klastra usługi HDInsight z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e6bd-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="8e6bd-107">Ta operacja usuwa również wszystkie dane przechowywane w systemie plików HDFS (Distributed File System) usługi Hadoop w klastrze.</span><span class="sxs-lookup"><span data-stu-id="8e6bd-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="8e6bd-108">Dane przechowywane na skojarzonym koncie usługi Azure Storage nie są usuwane.</span><span class="sxs-lookup"><span data-stu-id="8e6bd-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="8e6bd-109">Dane przechowywane w zewnętrznych magazynach strumieniowych nie są usuwane.</span><span class="sxs-lookup"><span data-stu-id="8e6bd-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="8e6bd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e6bd-110">EXAMPLES</span></span>

### <span data-ttu-id="8e6bd-111">Przykład 1: usuwanie klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="8e6bd-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="8e6bd-112">To polecenie powoduje usunięcie klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="8e6bd-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="8e6bd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e6bd-113">PARAMETERS</span></span>

### <span data-ttu-id="8e6bd-114">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="8e6bd-114">-ClusterName</span></span>
<span data-ttu-id="8e6bd-115">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="8e6bd-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8e6bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e6bd-116">-DefaultProfile</span></span>
<span data-ttu-id="8e6bd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8e6bd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e6bd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e6bd-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e6bd-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8e6bd-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8e6bd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e6bd-120">CommonParameters</span></span>
<span data-ttu-id="8e6bd-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e6bd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e6bd-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e6bd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e6bd-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e6bd-123">INPUTS</span></span>

### <span data-ttu-id="8e6bd-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8e6bd-124">None</span></span>

## <span data-ttu-id="8e6bd-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e6bd-125">OUTPUTS</span></span>

### <span data-ttu-id="8e6bd-126">Microsoft. Azure. Management. HDInsight. MODELES. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="8e6bd-126">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="8e6bd-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e6bd-127">NOTES</span></span>

## <span data-ttu-id="8e6bd-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e6bd-128">RELATED LINKS</span></span>

[<span data-ttu-id="8e6bd-129">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8e6bd-129">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="8e6bd-130">Użyj — AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8e6bd-130">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


