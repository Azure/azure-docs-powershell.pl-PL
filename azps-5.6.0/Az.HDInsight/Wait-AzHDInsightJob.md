---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 4d4b3ff71142540ff5c5635938d31a16e3fd9603
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975793"
---
# <span data-ttu-id="a86c1-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a86c1-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="a86c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a86c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a86c1-103">Czeka na ukończenie lub niepowodzenie określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="a86c1-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="a86c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a86c1-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a86c1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a86c1-105">DESCRIPTION</span></span>
<span data-ttu-id="a86c1-106">Polecenie cmdlet **Wait-AzHDInsightJob** oczekuje na ukończenie lub niepowodzenie zadania usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a86c1-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="a86c1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a86c1-107">EXAMPLES</span></span>

### <span data-ttu-id="a86c1-108">Przykład 1. Oczekiwanie na ukończenie lub niepowodzenie zadania</span><span class="sxs-lookup"><span data-stu-id="a86c1-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="a86c1-109">To polecenie czeka na ukończenie lub niepowodzenie zadania.</span><span class="sxs-lookup"><span data-stu-id="a86c1-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="a86c1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a86c1-110">PARAMETERS</span></span>

### <span data-ttu-id="a86c1-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a86c1-111">-ClusterName</span></span>
<span data-ttu-id="a86c1-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="a86c1-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a86c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86c1-113">-DefaultProfile</span></span>
<span data-ttu-id="a86c1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a86c1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a86c1-115">- HttpCredential</span><span class="sxs-lookup"><span data-stu-id="a86c1-115">-HttpCredential</span></span>
<span data-ttu-id="a86c1-116">Określa poświadczenia logowania klastrów (HTTP) dla tego klastra.</span><span class="sxs-lookup"><span data-stu-id="a86c1-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="a86c1-117">- JobId</span><span class="sxs-lookup"><span data-stu-id="a86c1-117">-JobId</span></span>
<span data-ttu-id="a86c1-118">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="a86c1-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a86c1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a86c1-119">-ResourceGroupName</span></span>
<span data-ttu-id="a86c1-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a86c1-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a86c1-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="a86c1-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="a86c1-122">Całkowity czas oczekiwania na ukończenie zadania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="a86c1-122">The total time to wait for job completion, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86c1-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a86c1-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="a86c1-124">Czas oczekiwania między sprawdzaniem stanu zadań (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="a86c1-124">The time to wait between job status checks, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86c1-125">CommonParameters</span></span>
<span data-ttu-id="a86c1-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a86c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86c1-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a86c1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86c1-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a86c1-128">INPUTS</span></span>

### <span data-ttu-id="a86c1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a86c1-129">System.String</span></span>

## <span data-ttu-id="a86c1-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a86c1-130">OUTPUTS</span></span>

### <span data-ttu-id="a86c1-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a86c1-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="a86c1-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a86c1-132">NOTES</span></span>

## <span data-ttu-id="a86c1-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a86c1-133">RELATED LINKS</span></span>

[<span data-ttu-id="a86c1-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a86c1-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="a86c1-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a86c1-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="a86c1-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a86c1-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


