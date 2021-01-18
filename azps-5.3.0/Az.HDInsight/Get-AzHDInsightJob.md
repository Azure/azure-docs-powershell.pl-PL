---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: dc7f69ef29d7e5396ad57346380decc672f83db5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500995"
---
# <span data-ttu-id="14eb5-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="14eb5-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="14eb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="14eb5-103">Pobiera listę zadań z klastra i wyświetla listę w odwrotnym porządku chronologicznym lub pobiera określone zadanie.</span><span class="sxs-lookup"><span data-stu-id="14eb5-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="14eb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14eb5-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14eb5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="14eb5-105">DESCRIPTION</span></span>
<span data-ttu-id="14eb5-106">Polecenie cmdlet **Get-AzHDInsightJob** pobiera ostatnie zadania dla określonego klastra usługi Azure HDInsight w odwrotnej kolejności chronologicznej z ostatnim zadaniem u góry listy.</span><span class="sxs-lookup"><span data-stu-id="14eb5-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="14eb5-107">Uzyskiwanie określonego zadania przez podanie parametru *JobID* .</span><span class="sxs-lookup"><span data-stu-id="14eb5-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="14eb5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14eb5-108">EXAMPLES</span></span>

### <span data-ttu-id="14eb5-109">Przykład 1: pobieranie ostatnich zadań dla określonego klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="14eb5-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="14eb5-110">To polecenie pobiera wszystkie ostatnie zadania dla klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="14eb5-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="14eb5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14eb5-111">PARAMETERS</span></span>

### <span data-ttu-id="14eb5-112">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="14eb5-112">-ClusterName</span></span>
<span data-ttu-id="14eb5-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="14eb5-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="14eb5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14eb5-114">-DefaultProfile</span></span>
<span data-ttu-id="14eb5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="14eb5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14eb5-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="14eb5-116">-HttpCredential</span></span>
<span data-ttu-id="14eb5-117">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="14eb5-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="14eb5-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="14eb5-118">-JobId</span></span>
<span data-ttu-id="14eb5-119">Określa identyfikator zadania, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="14eb5-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14eb5-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="14eb5-120">-NumOfJobs</span></span>
<span data-ttu-id="14eb5-121">Określa liczbę zadań do pobrania.</span><span class="sxs-lookup"><span data-stu-id="14eb5-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="14eb5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14eb5-122">-ResourceGroupName</span></span>
<span data-ttu-id="14eb5-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14eb5-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="14eb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14eb5-124">CommonParameters</span></span>
<span data-ttu-id="14eb5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14eb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14eb5-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14eb5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14eb5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14eb5-127">INPUTS</span></span>

### <span data-ttu-id="14eb5-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="14eb5-128">None</span></span>

## <span data-ttu-id="14eb5-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14eb5-129">OUTPUTS</span></span>

### <span data-ttu-id="14eb5-130">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="14eb5-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="14eb5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14eb5-131">NOTES</span></span>

## <span data-ttu-id="14eb5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14eb5-132">RELATED LINKS</span></span>

[<span data-ttu-id="14eb5-133">Nowe — AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="14eb5-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="14eb5-134">Start — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="14eb5-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="14eb5-135">Zatrzymaj — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="14eb5-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="14eb5-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="14eb5-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


