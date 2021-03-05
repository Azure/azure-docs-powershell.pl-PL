---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: c2fcc4112bb2fb62b73531bd6bd580ba3bcd7648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009034"
---
# <span data-ttu-id="d7005-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="d7005-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="d7005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7005-102">SYNOPSIS</span></span>
<span data-ttu-id="d7005-103">Tworzy warunek autoskalowania oparty na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="d7005-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="d7005-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7005-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7005-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7005-105">DESCRIPTION</span></span>
<span data-ttu-id="d7005-106">Polecenie **cmdlet New-AzHDInsightClusterAutoscaleScheduleCondition** tworzy warunek skalowania automatycznego oparty na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="d7005-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="d7005-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7005-107">EXAMPLES</span></span>

### <span data-ttu-id="d7005-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7005-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="d7005-109">To polecenie tworzy warunek, w którym automatyczne skalowanie klastrów do 5 węzłów pracowników o godzinie 09:00 w każdy poniedziałek, środa.</span><span class="sxs-lookup"><span data-stu-id="d7005-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="d7005-110">Przykład 2. Włączanie automatycznego skalowania klastrów opartego na harmonogramie przy użyciu warunku automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="d7005-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="d7005-111">To polecenie tworzy warunek, w którym automatyczne skalowanie klastrów do 5 węzłów pracowników o godzinie 09:00 w każdy poniedziałek, środa.</span><span class="sxs-lookup"><span data-stu-id="d7005-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="d7005-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7005-112">PARAMETERS</span></span>

### <span data-ttu-id="d7005-113">— Dzień</span><span class="sxs-lookup"><span data-stu-id="d7005-113">-Day</span></span>
<span data-ttu-id="d7005-114">Pobiera lub ustawia warunek harmonogramu automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="d7005-114">Gets or sets the days of Autoscale schedule condition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7005-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7005-115">-DefaultProfile</span></span>
<span data-ttu-id="d7005-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7005-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7005-117">— czas</span><span class="sxs-lookup"><span data-stu-id="d7005-117">-Time</span></span>
<span data-ttu-id="d7005-118">Pobiera lub ustawia czas warunku harmonogramu automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="d7005-118">Gets or sets the time of Autoscale schedule condition.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7005-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="d7005-119">-WorkerNodeCount</span></span>
<span data-ttu-id="d7005-120">Pobiera lub ustawia liczbę pracowników harmonogramu w warunku harmonogramu automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="d7005-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7005-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7005-121">CommonParameters</span></span>
<span data-ttu-id="d7005-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7005-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7005-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7005-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7005-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7005-124">INPUTS</span></span>

### <span data-ttu-id="d7005-125">Brak</span><span class="sxs-lookup"><span data-stu-id="d7005-125">None</span></span>

## <span data-ttu-id="d7005-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7005-126">OUTPUTS</span></span>

### <span data-ttu-id="d7005-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="d7005-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="d7005-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7005-128">NOTES</span></span>

## <span data-ttu-id="d7005-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7005-129">RELATED LINKS</span></span>

<span data-ttu-id="d7005-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d7005-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
