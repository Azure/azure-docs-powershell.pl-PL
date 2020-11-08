---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 15d93d6dbdc7b231d47d5372864883f915e66ae9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064086"
---
# <span data-ttu-id="1f088-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1f088-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="1f088-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f088-102">SYNOPSIS</span></span>
<span data-ttu-id="1f088-103">Umożliwia wybranie klastra do użycia z poleceniem cmdlet Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="1f088-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="1f088-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f088-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f088-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f088-105">DESCRIPTION</span></span>
<span data-ttu-id="1f088-106">Polecenie cmdlet **use-AzHDInsightCluster** umożliwia wybranie klastra usługi Azure HDInsight dla Invoke-AzHDInsightHiveJob polecenia cmdlet służącego do przesyłania zadań w usłudze Hive.</span><span class="sxs-lookup"><span data-stu-id="1f088-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="1f088-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f088-107">EXAMPLES</span></span>

### <span data-ttu-id="1f088-108">Przykład 1: Wybieranie klastra na potrzeby przesyłania zapytań dotyczących gałęzi</span><span class="sxs-lookup"><span data-stu-id="1f088-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="1f088-109">To polecenie umożliwia wybranie klastra do przesyłania zapytań dotyczących gałęzi.</span><span class="sxs-lookup"><span data-stu-id="1f088-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="1f088-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f088-110">PARAMETERS</span></span>

### <span data-ttu-id="1f088-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="1f088-111">-ClusterName</span></span>
<span data-ttu-id="1f088-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="1f088-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="1f088-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f088-113">-DefaultProfile</span></span>
<span data-ttu-id="1f088-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1f088-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f088-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="1f088-115">-HttpCredential</span></span>
<span data-ttu-id="1f088-116">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="1f088-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="1f088-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f088-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f088-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f088-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1f088-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f088-119">CommonParameters</span></span>
<span data-ttu-id="1f088-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f088-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f088-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f088-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f088-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f088-122">INPUTS</span></span>

### <span data-ttu-id="1f088-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1f088-123">None</span></span>

## <span data-ttu-id="1f088-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f088-124">OUTPUTS</span></span>

### <span data-ttu-id="1f088-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1f088-125">System.String</span></span>

## <span data-ttu-id="1f088-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f088-126">NOTES</span></span>

## <span data-ttu-id="1f088-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f088-127">RELATED LINKS</span></span>

[<span data-ttu-id="1f088-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1f088-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="1f088-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1f088-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


