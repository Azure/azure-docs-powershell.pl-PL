---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/stop-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 7247a4f5e23bc4f0f3c520f909cec221ee03e1ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543836"
---
# <span data-ttu-id="7b320-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7b320-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="7b320-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b320-102">SYNOPSIS</span></span>
<span data-ttu-id="7b320-103">Zatrzymuje określone uruchomione zadanie w klastrze.</span><span class="sxs-lookup"><span data-stu-id="7b320-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b320-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b320-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b320-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b320-105">DESCRIPTION</span></span>
<span data-ttu-id="7b320-106">Polecenie cmdlet **stop-AzureRmHDInsightJob** zatrzymuje określone uruchomione zadanie w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7b320-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7b320-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b320-107">EXAMPLES</span></span>

### <span data-ttu-id="7b320-108">Przykład 1: Zatrzymywanie zadania w określonym klastrze</span><span class="sxs-lookup"><span data-stu-id="7b320-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="7b320-109">To polecenie zatrzymuje zadanie w klastrze o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="7b320-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="7b320-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b320-110">PARAMETERS</span></span>

### <span data-ttu-id="7b320-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="7b320-111">-ClusterName</span></span>
<span data-ttu-id="7b320-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="7b320-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="7b320-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b320-113">-DefaultProfile</span></span>
<span data-ttu-id="7b320-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7b320-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b320-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="7b320-115">-HttpCredential</span></span>
<span data-ttu-id="7b320-116">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="7b320-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="7b320-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="7b320-117">-JobId</span></span>
<span data-ttu-id="7b320-118">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="7b320-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="7b320-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b320-119">-ResourceGroupName</span></span>
<span data-ttu-id="7b320-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b320-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7b320-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b320-121">CommonParameters</span></span>
<span data-ttu-id="7b320-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b320-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b320-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b320-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b320-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b320-124">INPUTS</span></span>

### <span data-ttu-id="7b320-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7b320-125">System.String</span></span>
<span data-ttu-id="7b320-126">Parametry: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b320-126">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="7b320-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b320-127">OUTPUTS</span></span>

### <span data-ttu-id="7b320-128">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7b320-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="7b320-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b320-129">NOTES</span></span>

## <span data-ttu-id="7b320-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b320-130">RELATED LINKS</span></span>

[<span data-ttu-id="7b320-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7b320-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="7b320-132">Start — AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7b320-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="7b320-133">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7b320-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


