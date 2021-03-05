---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 316ac2671fe60271ad0d994855189071e3da2b95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964714"
---
# <span data-ttu-id="2ba04-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2ba04-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="2ba04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ba04-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba04-103">Uruchamia zdefiniowane zadanie usługi Azure HDInsight w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="2ba04-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="2ba04-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ba04-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ba04-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ba04-105">DESCRIPTION</span></span>
<span data-ttu-id="2ba04-106">Polecenie **cmdlet Start-AzHDInsightJob** uruchamia zdefiniowane zadanie usługi Azure HDInsight w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="2ba04-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="2ba04-107">Może to być zadanie MapReduce, zadanie MapReduce przesyłania strumieniowego, zadanie Gałąź lub zadanie Świnka.</span><span class="sxs-lookup"><span data-stu-id="2ba04-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="2ba04-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ba04-108">EXAMPLES</span></span>

### <span data-ttu-id="2ba04-109">Przykład 1. Uruchamianie zadania w określonym klastrze</span><span class="sxs-lookup"><span data-stu-id="2ba04-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="2ba04-110">To polecenie uruchamia zadanie w klastrze o nazwie Twoja-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2ba04-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2ba04-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ba04-111">PARAMETERS</span></span>

### <span data-ttu-id="2ba04-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2ba04-112">-ClusterName</span></span>
<span data-ttu-id="2ba04-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="2ba04-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2ba04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba04-114">-DefaultProfile</span></span>
<span data-ttu-id="2ba04-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2ba04-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ba04-116">- HttpCredential</span><span class="sxs-lookup"><span data-stu-id="2ba04-116">-HttpCredential</span></span>
<span data-ttu-id="2ba04-117">Określa poświadczenia logowania klastrów (HTTP) dla tego klastra.</span><span class="sxs-lookup"><span data-stu-id="2ba04-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba04-118">— JobDefinition</span><span class="sxs-lookup"><span data-stu-id="2ba04-118">-JobDefinition</span></span>
<span data-ttu-id="2ba04-119">Określa zadanie, które ma być rozpoczynane w klastrze HDInsight platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba04-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba04-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba04-120">-ResourceGroupName</span></span>
<span data-ttu-id="2ba04-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2ba04-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2ba04-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba04-122">CommonParameters</span></span>
<span data-ttu-id="2ba04-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba04-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba04-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ba04-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba04-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ba04-125">INPUTS</span></span>

### <span data-ttu-id="2ba04-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2ba04-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="2ba04-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ba04-127">OUTPUTS</span></span>

### <span data-ttu-id="2ba04-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2ba04-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="2ba04-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ba04-129">NOTES</span></span>

## <span data-ttu-id="2ba04-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ba04-130">RELATED LINKS</span></span>

[<span data-ttu-id="2ba04-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2ba04-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="2ba04-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2ba04-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="2ba04-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2ba04-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="2ba04-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2ba04-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


