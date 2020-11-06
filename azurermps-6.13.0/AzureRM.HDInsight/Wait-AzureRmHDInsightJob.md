---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/wait-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: de7df9417e617f88c61e75c64dd42f32b83fc66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546619"
---
# <span data-ttu-id="d5e9f-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d5e9f-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="d5e9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e9f-103">Oczekuje na zakończenie lub niepowodzenie określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="d5e9f-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5e9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5e9f-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5e9f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5e9f-105">DESCRIPTION</span></span>
<span data-ttu-id="d5e9f-106">Polecenie cmdlet **wait-AzureRmHDInsightJob** oczekuje na zakończenie lub niepowodzenie zadania usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5e9f-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="d5e9f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5e9f-107">EXAMPLES</span></span>

### <span data-ttu-id="d5e9f-108">Przykład 1. oczekiwanie na zakończenie lub niepowodzenie zadania</span><span class="sxs-lookup"><span data-stu-id="d5e9f-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="d5e9f-109">To polecenie czeka na zakończenie lub niepowodzenie zadania.</span><span class="sxs-lookup"><span data-stu-id="d5e9f-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="d5e9f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5e9f-110">PARAMETERS</span></span>

### <span data-ttu-id="d5e9f-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d5e9f-111">-ClusterName</span></span>
<span data-ttu-id="d5e9f-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d5e9f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d5e9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e9f-113">-DefaultProfile</span></span>
<span data-ttu-id="d5e9f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d5e9f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5e9f-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d5e9f-115">-HttpCredential</span></span>
<span data-ttu-id="d5e9f-116">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="d5e9f-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="d5e9f-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="d5e9f-117">-JobId</span></span>
<span data-ttu-id="d5e9f-118">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="d5e9f-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="d5e9f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e9f-119">-ResourceGroupName</span></span>
<span data-ttu-id="d5e9f-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d5e9f-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d5e9f-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="d5e9f-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="d5e9f-122">Całkowity czas oczekiwania na ukończenie zadania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="d5e9f-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="d5e9f-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d5e9f-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="d5e9f-124">Czas oczekiwania między sprawdzeniem stanu zadania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="d5e9f-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="d5e9f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e9f-125">CommonParameters</span></span>
<span data-ttu-id="d5e9f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5e9f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e9f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5e9f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e9f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5e9f-128">INPUTS</span></span>

### <span data-ttu-id="d5e9f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d5e9f-129">System.String</span></span>
<span data-ttu-id="d5e9f-130">Parametry: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5e9f-130">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="d5e9f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5e9f-131">OUTPUTS</span></span>

### <span data-ttu-id="d5e9f-132">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d5e9f-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="d5e9f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5e9f-133">NOTES</span></span>

## <span data-ttu-id="d5e9f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5e9f-134">RELATED LINKS</span></span>

[<span data-ttu-id="d5e9f-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d5e9f-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="d5e9f-136">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d5e9f-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="d5e9f-137">Zatrzymaj — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d5e9f-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


