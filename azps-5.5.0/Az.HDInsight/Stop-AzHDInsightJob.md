---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: bff9b9d44d8afcbc315293dc07be3592172f1a4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185866"
---
# <span data-ttu-id="d546a-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d546a-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="d546a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d546a-102">SYNOPSIS</span></span>
<span data-ttu-id="d546a-103">Zatrzymuje określone zadanie uruchomione w klastrze.</span><span class="sxs-lookup"><span data-stu-id="d546a-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="d546a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d546a-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d546a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d546a-105">DESCRIPTION</span></span>
<span data-ttu-id="d546a-106">Polecenie **cmdlet Stop-AzHDInsightJob** zatrzymuje określone uruchomione zadanie w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d546a-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d546a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d546a-107">EXAMPLES</span></span>

### <span data-ttu-id="d546a-108">Przykład 1. Zatrzymywanie zadania w określonym klastrze</span><span class="sxs-lookup"><span data-stu-id="d546a-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="d546a-109">To polecenie zatrzymuje zadanie w klastrze o nazwie Twoja-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="d546a-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d546a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d546a-110">PARAMETERS</span></span>

### <span data-ttu-id="d546a-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d546a-111">-ClusterName</span></span>
<span data-ttu-id="d546a-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d546a-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d546a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d546a-113">-DefaultProfile</span></span>
<span data-ttu-id="d546a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d546a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d546a-115">- HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d546a-115">-HttpCredential</span></span>
<span data-ttu-id="d546a-116">Określa poświadczenia logowania klastrów (HTTP) dla tego klastra.</span><span class="sxs-lookup"><span data-stu-id="d546a-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="d546a-117">- JobId</span><span class="sxs-lookup"><span data-stu-id="d546a-117">-JobId</span></span>
<span data-ttu-id="d546a-118">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="d546a-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="d546a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d546a-119">-ResourceGroupName</span></span>
<span data-ttu-id="d546a-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d546a-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d546a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d546a-121">CommonParameters</span></span>
<span data-ttu-id="d546a-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d546a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d546a-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d546a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d546a-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d546a-124">INPUTS</span></span>

### <span data-ttu-id="d546a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d546a-125">System.String</span></span>

## <span data-ttu-id="d546a-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d546a-126">OUTPUTS</span></span>

### <span data-ttu-id="d546a-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d546a-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="d546a-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d546a-128">NOTES</span></span>

## <span data-ttu-id="d546a-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d546a-129">RELATED LINKS</span></span>

[<span data-ttu-id="d546a-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d546a-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="d546a-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d546a-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="d546a-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d546a-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


