---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: e3cfd7978ecd7f8395a0c499d3d194f133960a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717585"
---
# <span data-ttu-id="0455a-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0455a-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="0455a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0455a-102">SYNOPSIS</span></span>
<span data-ttu-id="0455a-103">Pobiera listę zadań z klastra i wyświetla listę w odwrotnym porządku chronologicznym lub pobiera określone zadanie.</span><span class="sxs-lookup"><span data-stu-id="0455a-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0455a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0455a-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0455a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0455a-105">DESCRIPTION</span></span>
<span data-ttu-id="0455a-106">Polecenie cmdlet **Get-AzureRmHDInsightJob** pobiera ostatnie zadania dla określonego klastra usługi Azure HDInsight w odwrotnej kolejności chronologicznej z ostatnim zadaniem u góry listy.</span><span class="sxs-lookup"><span data-stu-id="0455a-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="0455a-107">Uzyskiwanie określonego zadania przez podanie parametru *JobID* .</span><span class="sxs-lookup"><span data-stu-id="0455a-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="0455a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0455a-108">EXAMPLES</span></span>

### <span data-ttu-id="0455a-109">Przykład 1: pobieranie ostatnich zadań dla określonego klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="0455a-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="0455a-110">To polecenie pobiera wszystkie ostatnie zadania dla klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="0455a-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0455a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0455a-111">PARAMETERS</span></span>

### <span data-ttu-id="0455a-112">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="0455a-112">-ClusterName</span></span>
<span data-ttu-id="0455a-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="0455a-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0455a-114">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="0455a-114">-HttpCredential</span></span>
<span data-ttu-id="0455a-115">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="0455a-115">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="0455a-116">-JobId</span><span class="sxs-lookup"><span data-stu-id="0455a-116">-JobId</span></span>
<span data-ttu-id="0455a-117">Określa identyfikator zadania, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="0455a-117">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="0455a-118">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="0455a-118">-NumOfJobs</span></span>
<span data-ttu-id="0455a-119">Określa liczbę zadań do pobrania.</span><span class="sxs-lookup"><span data-stu-id="0455a-119">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="0455a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0455a-120">-ResourceGroupName</span></span>
<span data-ttu-id="0455a-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0455a-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0455a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0455a-122">-DefaultProfile</span></span>
<span data-ttu-id="0455a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0455a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0455a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0455a-124">CommonParameters</span></span>
<span data-ttu-id="0455a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0455a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0455a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0455a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0455a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0455a-127">INPUTS</span></span>

## <span data-ttu-id="0455a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0455a-128">OUTPUTS</span></span>

### <span data-ttu-id="0455a-129">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0455a-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="0455a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0455a-130">NOTES</span></span>

## <span data-ttu-id="0455a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0455a-131">RELATED LINKS</span></span>

[<span data-ttu-id="0455a-132">Nowe — AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0455a-132">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="0455a-133">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0455a-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="0455a-134">Zatrzymaj — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0455a-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="0455a-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0455a-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


