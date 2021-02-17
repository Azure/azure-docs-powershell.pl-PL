---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180587"
---
# <span data-ttu-id="b62c8-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b62c8-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="b62c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b62c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b62c8-103">Tworzy nietrwale obiekt opisujący konfigurację automatycznego skalowania klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b62c8-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b62c8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b62c8-104">SYNTAX</span></span>

### <span data-ttu-id="b62c8-105">LoadAutoscaleParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b62c8-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b62c8-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="b62c8-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b62c8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b62c8-107">DESCRIPTION</span></span>
<span data-ttu-id="b62c8-108">Polecenie cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** tworzy nietrwale obiekt opisujący konfigurację skalowania automatycznego klastrów usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b62c8-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b62c8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b62c8-109">EXAMPLES</span></span>

### <span data-ttu-id="b62c8-110">Przykład 1. Tworzenie obiektu opisujące konfigurację skalowania automatycznego na podstawie obciążenia</span><span class="sxs-lookup"><span data-stu-id="b62c8-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="b62c8-111">To polecenie tworzy obiekt opisujący konfigurację skalowania automatycznego oparta na ładowaniu.</span><span class="sxs-lookup"><span data-stu-id="b62c8-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="b62c8-112">Przykład 2. Tworzenie obiektu opisujące konfigurację skalowania automatycznego opartą na harmonogramie</span><span class="sxs-lookup"><span data-stu-id="b62c8-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="b62c8-113">To polecenie tworzy obiekt opisujący konfigurację skalowania automatycznego opartą na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="b62c8-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="b62c8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b62c8-114">PARAMETERS</span></span>

### <span data-ttu-id="b62c8-115">— Warunek</span><span class="sxs-lookup"><span data-stu-id="b62c8-115">-Condition</span></span>
<span data-ttu-id="b62c8-116">Pobiera lub ustawia warunek autoskalowania oparty na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="b62c8-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b62c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62c8-117">-DefaultProfile</span></span>
<span data-ttu-id="b62c8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b62c8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b62c8-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="b62c8-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="b62c8-120">Pobiera lub ustawia maksymalną liczbę pracowników na podstawie obciążenia automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="b62c8-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b62c8-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="b62c8-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="b62c8-122">Pobiera lub ustawia minimalną liczbę pracowników w przypadku skalowania automatycznego opartego na ładowanych danych.</span><span class="sxs-lookup"><span data-stu-id="b62c8-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b62c8-123">- Strefa czasowa</span><span class="sxs-lookup"><span data-stu-id="b62c8-123">-TimeZone</span></span>
<span data-ttu-id="b62c8-124">Pobiera lub ustawia strefę czasową automatycznego skalowania opartego na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="b62c8-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b62c8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62c8-125">CommonParameters</span></span>
<span data-ttu-id="b62c8-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b62c8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62c8-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b62c8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62c8-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b62c8-128">INPUTS</span></span>

### <span data-ttu-id="b62c8-129">Brak</span><span class="sxs-lookup"><span data-stu-id="b62c8-129">None</span></span>

## <span data-ttu-id="b62c8-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b62c8-130">OUTPUTS</span></span>

### <span data-ttu-id="b62c8-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="b62c8-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="b62c8-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b62c8-132">NOTES</span></span>

## <span data-ttu-id="b62c8-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b62c8-133">RELATED LINKS</span></span>

<span data-ttu-id="b62c8-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b62c8-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
