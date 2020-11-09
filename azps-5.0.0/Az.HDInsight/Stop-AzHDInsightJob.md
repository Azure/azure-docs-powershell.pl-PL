---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: d5e38cf3edb89801b630735dee1ce0dbd1d62d41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304039"
---
# <span data-ttu-id="e3a57-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e3a57-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="e3a57-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3a57-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a57-103">Zatrzymuje określone uruchomione zadanie w klastrze.</span><span class="sxs-lookup"><span data-stu-id="e3a57-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="e3a57-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3a57-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3a57-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3a57-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a57-106">Polecenie cmdlet **stop-AzHDInsightJob** zatrzymuje określone uruchomione zadanie w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e3a57-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e3a57-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3a57-107">EXAMPLES</span></span>

### <span data-ttu-id="e3a57-108">Przykład 1: Zatrzymywanie zadania w określonym klastrze</span><span class="sxs-lookup"><span data-stu-id="e3a57-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="e3a57-109">To polecenie zatrzymuje zadanie w klastrze o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="e3a57-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e3a57-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3a57-110">PARAMETERS</span></span>

### <span data-ttu-id="e3a57-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="e3a57-111">-ClusterName</span></span>
<span data-ttu-id="e3a57-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="e3a57-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e3a57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a57-113">-DefaultProfile</span></span>
<span data-ttu-id="e3a57-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e3a57-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3a57-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e3a57-115">-HttpCredential</span></span>
<span data-ttu-id="e3a57-116">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="e3a57-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="e3a57-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="e3a57-117">-JobId</span></span>
<span data-ttu-id="e3a57-118">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="e3a57-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="e3a57-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a57-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3a57-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e3a57-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e3a57-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a57-121">CommonParameters</span></span>
<span data-ttu-id="e3a57-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a57-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a57-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a57-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a57-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3a57-124">INPUTS</span></span>

### <span data-ttu-id="e3a57-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e3a57-125">System.String</span></span>

## <span data-ttu-id="e3a57-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3a57-126">OUTPUTS</span></span>

### <span data-ttu-id="e3a57-127">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e3a57-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="e3a57-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3a57-128">NOTES</span></span>

## <span data-ttu-id="e3a57-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3a57-129">RELATED LINKS</span></span>

[<span data-ttu-id="e3a57-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e3a57-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="e3a57-131">Start — AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e3a57-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="e3a57-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e3a57-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


