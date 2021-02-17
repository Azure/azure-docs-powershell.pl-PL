---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: ad2060a399b5781e18c9d8b7fc1c8a37b5d467b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243498"
---
# <span data-ttu-id="98dd5-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="98dd5-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="98dd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="98dd5-103">Uruchamia zdefiniowane zadanie usługi Azure HDInsight w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="98dd5-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="98dd5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="98dd5-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98dd5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="98dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="98dd5-106">Polecenie **cmdlet Start-AzHDInsightJob** uruchamia zdefiniowane zadanie usługi Azure HDInsight w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="98dd5-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="98dd5-107">Może to być zadanie MapReduce, zadanie MapReduce przesyłania strumieniowego, zadanie Gałąź lub zadanie Świnka.</span><span class="sxs-lookup"><span data-stu-id="98dd5-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="98dd5-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="98dd5-108">EXAMPLES</span></span>

### <span data-ttu-id="98dd5-109">Przykład 1. Uruchamianie zadania w określonym klastrze</span><span class="sxs-lookup"><span data-stu-id="98dd5-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="98dd5-110">To polecenie uruchamia zadanie w klastrze o nazwie Twoja-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="98dd5-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="98dd5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98dd5-111">PARAMETERS</span></span>

### <span data-ttu-id="98dd5-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="98dd5-112">-ClusterName</span></span>
<span data-ttu-id="98dd5-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="98dd5-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="98dd5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98dd5-114">-DefaultProfile</span></span>
<span data-ttu-id="98dd5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="98dd5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98dd5-116">- HttpCredential</span><span class="sxs-lookup"><span data-stu-id="98dd5-116">-HttpCredential</span></span>
<span data-ttu-id="98dd5-117">Określa poświadczenia logowania klastrów (HTTP) dla tego klastra.</span><span class="sxs-lookup"><span data-stu-id="98dd5-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="98dd5-118">- JobDefinition</span><span class="sxs-lookup"><span data-stu-id="98dd5-118">-JobDefinition</span></span>
<span data-ttu-id="98dd5-119">Określa zadanie, które ma być rozpoczynane w klastrze HDInsight platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="98dd5-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="98dd5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98dd5-120">-ResourceGroupName</span></span>
<span data-ttu-id="98dd5-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="98dd5-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="98dd5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98dd5-122">CommonParameters</span></span>
<span data-ttu-id="98dd5-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98dd5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98dd5-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98dd5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98dd5-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98dd5-125">INPUTS</span></span>

### <span data-ttu-id="98dd5-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="98dd5-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="98dd5-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98dd5-127">OUTPUTS</span></span>

### <span data-ttu-id="98dd5-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="98dd5-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="98dd5-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="98dd5-129">NOTES</span></span>

## <span data-ttu-id="98dd5-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98dd5-130">RELATED LINKS</span></span>

[<span data-ttu-id="98dd5-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="98dd5-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="98dd5-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="98dd5-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="98dd5-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="98dd5-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="98dd5-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="98dd5-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


