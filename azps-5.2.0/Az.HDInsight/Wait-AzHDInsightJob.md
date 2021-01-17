---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 6b87b7f6e3482aad974c5f7d334724f5d2f99e7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328249"
---
# <span data-ttu-id="cda3c-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cda3c-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="cda3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cda3c-102">SYNOPSIS</span></span>
<span data-ttu-id="cda3c-103">Oczekuje na zakończenie lub niepowodzenie określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="cda3c-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="cda3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cda3c-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cda3c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cda3c-105">DESCRIPTION</span></span>
<span data-ttu-id="cda3c-106">Polecenie cmdlet **wait-AzHDInsightJob** oczekuje na zakończenie lub niepowodzenie zadania usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cda3c-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="cda3c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cda3c-107">EXAMPLES</span></span>

### <span data-ttu-id="cda3c-108">Przykład 1. oczekiwanie na zakończenie lub niepowodzenie zadania</span><span class="sxs-lookup"><span data-stu-id="cda3c-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="cda3c-109">To polecenie czeka na zakończenie lub niepowodzenie zadania.</span><span class="sxs-lookup"><span data-stu-id="cda3c-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="cda3c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cda3c-110">PARAMETERS</span></span>

### <span data-ttu-id="cda3c-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="cda3c-111">-ClusterName</span></span>
<span data-ttu-id="cda3c-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="cda3c-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="cda3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda3c-113">-DefaultProfile</span></span>
<span data-ttu-id="cda3c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cda3c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cda3c-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="cda3c-115">-HttpCredential</span></span>
<span data-ttu-id="cda3c-116">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="cda3c-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="cda3c-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="cda3c-117">-JobId</span></span>
<span data-ttu-id="cda3c-118">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="cda3c-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="cda3c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda3c-119">-ResourceGroupName</span></span>
<span data-ttu-id="cda3c-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cda3c-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cda3c-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="cda3c-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="cda3c-122">Całkowity czas oczekiwania na ukończenie zadania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="cda3c-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="cda3c-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="cda3c-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="cda3c-124">Czas oczekiwania między sprawdzeniem stanu zadania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="cda3c-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="cda3c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda3c-125">CommonParameters</span></span>
<span data-ttu-id="cda3c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda3c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda3c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cda3c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda3c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cda3c-128">INPUTS</span></span>

### <span data-ttu-id="cda3c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cda3c-129">System.String</span></span>

## <span data-ttu-id="cda3c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cda3c-130">OUTPUTS</span></span>

### <span data-ttu-id="cda3c-131">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cda3c-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="cda3c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cda3c-132">NOTES</span></span>

## <span data-ttu-id="cda3c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cda3c-133">RELATED LINKS</span></span>

[<span data-ttu-id="cda3c-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cda3c-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="cda3c-135">Start — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cda3c-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="cda3c-136">Zatrzymaj — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cda3c-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


