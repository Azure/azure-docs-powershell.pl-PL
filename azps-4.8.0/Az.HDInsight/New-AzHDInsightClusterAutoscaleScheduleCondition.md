---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063546"
---
# <span data-ttu-id="17bf3-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="17bf3-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="17bf3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="17bf3-103">Tworzy warunek autoskalowania na podstawie harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="17bf3-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="17bf3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17bf3-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17bf3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="17bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="17bf3-106">Polecenie cmdlet **New-AzHDInsightClusterAutoscaleScheduleCondition** umożliwia utworzenie warunku automatycznego skalowania opartego na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="17bf3-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="17bf3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="17bf3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="17bf3-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="17bf3-109">To polecenie tworzy warunek, w którym klaster automatycznie przeskaluje się do 5 węzłów roboczych o godzinie 09:00 co poniedziałek, środa.</span><span class="sxs-lookup"><span data-stu-id="17bf3-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="17bf3-110">Przykład 2: włączenie automatycznego skalowania klastra na podstawie harmonogramu za pomocą warunku automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="17bf3-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="17bf3-111">To polecenie tworzy warunek, w którym klaster automatycznie przeskaluje się do 5 węzłów roboczych o godzinie 09:00 co poniedziałek, środa.</span><span class="sxs-lookup"><span data-stu-id="17bf3-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="17bf3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17bf3-112">PARAMETERS</span></span>

### <span data-ttu-id="17bf3-113">-Day</span><span class="sxs-lookup"><span data-stu-id="17bf3-113">-Day</span></span>
<span data-ttu-id="17bf3-114">Pobiera lub ustawia liczbę dni warunku harmonogramu autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="17bf3-114">Gets or sets the days of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="17bf3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bf3-115">-DefaultProfile</span></span>
<span data-ttu-id="17bf3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17bf3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17bf3-117">-Time (czas)</span><span class="sxs-lookup"><span data-stu-id="17bf3-117">-Time</span></span>
<span data-ttu-id="17bf3-118">Pobiera lub ustawia godzinę warunku harmonogramu autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="17bf3-118">Gets or sets the time of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="17bf3-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="17bf3-119">-WorkerNodeCount</span></span>
<span data-ttu-id="17bf3-120">Pobiera lub ustawia liczbę workernode harmonogramu o warunku harmonogramu automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="17bf3-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="17bf3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bf3-121">CommonParameters</span></span>
<span data-ttu-id="17bf3-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17bf3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bf3-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17bf3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bf3-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17bf3-124">INPUTS</span></span>

### <span data-ttu-id="17bf3-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="17bf3-125">None</span></span>

## <span data-ttu-id="17bf3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17bf3-126">OUTPUTS</span></span>

### <span data-ttu-id="17bf3-127">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="17bf3-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="17bf3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17bf3-128">NOTES</span></span>

## <span data-ttu-id="17bf3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17bf3-129">RELATED LINKS</span></span>

<span data-ttu-id="17bf3-130">[Nowe — AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="17bf3-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
