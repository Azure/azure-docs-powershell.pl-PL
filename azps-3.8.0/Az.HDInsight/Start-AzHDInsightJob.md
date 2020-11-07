---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 6eab5c80fa8c21d5b592f0e194a5aba50c4d3002
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895426"
---
# <span data-ttu-id="ed039-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ed039-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="ed039-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed039-102">SYNOPSIS</span></span>
<span data-ttu-id="ed039-103">Rozpoczynanie zdefiniowanego zadania usługi Azure HDInsight w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="ed039-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="ed039-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed039-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed039-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ed039-105">DESCRIPTION</span></span>
<span data-ttu-id="ed039-106">Polecenie cmdlet **Start-AzHDInsightJob** uruchamia zdefiniowane zadanie usługi Azure HDInsight dla określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="ed039-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="ed039-107">Może to być zadanie MapReduce, strumieniowe zadanie MapReduce, zadanie gałęzi lub zadanie wieprzowe.</span><span class="sxs-lookup"><span data-stu-id="ed039-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="ed039-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed039-108">EXAMPLES</span></span>

### <span data-ttu-id="ed039-109">Przykład 1. Uruchom zadanie w określonym klastrze</span><span class="sxs-lookup"><span data-stu-id="ed039-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="ed039-110">To polecenie uruchamia zadanie w klastrze o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="ed039-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ed039-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed039-111">PARAMETERS</span></span>

### <span data-ttu-id="ed039-112">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="ed039-112">-ClusterName</span></span>
<span data-ttu-id="ed039-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="ed039-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ed039-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed039-114">-DefaultProfile</span></span>
<span data-ttu-id="ed039-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ed039-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed039-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="ed039-116">-HttpCredential</span></span>
<span data-ttu-id="ed039-117">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="ed039-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="ed039-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="ed039-118">-JobDefinition</span></span>
<span data-ttu-id="ed039-119">Określa zadanie, które ma zostać uruchomione w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed039-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="ed039-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed039-120">-ResourceGroupName</span></span>
<span data-ttu-id="ed039-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed039-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ed039-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed039-122">CommonParameters</span></span>
<span data-ttu-id="ed039-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed039-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed039-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed039-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed039-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed039-125">INPUTS</span></span>

### <span data-ttu-id="ed039-126">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ed039-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="ed039-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed039-127">OUTPUTS</span></span>

### <span data-ttu-id="ed039-128">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ed039-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="ed039-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed039-129">NOTES</span></span>

## <span data-ttu-id="ed039-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed039-130">RELATED LINKS</span></span>

[<span data-ttu-id="ed039-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ed039-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="ed039-132">Nowe — AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ed039-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="ed039-133">Zatrzymaj — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ed039-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="ed039-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ed039-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


