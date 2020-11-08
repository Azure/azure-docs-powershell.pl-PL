---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063547"
---
# <span data-ttu-id="c298f-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c298f-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="c298f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c298f-102">SYNOPSIS</span></span>
<span data-ttu-id="c298f-103">Tworzy nieutrwalony obiekt, który opisuje konfigurację autoskalowania klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c298f-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c298f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c298f-104">SYNTAX</span></span>

### <span data-ttu-id="c298f-105">LoadAutoscaleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c298f-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c298f-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="c298f-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c298f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c298f-107">DESCRIPTION</span></span>
<span data-ttu-id="c298f-108">Polecenie cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** tworzy nieutrwalony obiekt, który opisuje konfigurację autoskalowania klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c298f-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c298f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c298f-109">EXAMPLES</span></span>

### <span data-ttu-id="c298f-110">Przykład 1. Tworzenie obiektu opisującego konfigurację autoskalowania opartego na ładowaniu</span><span class="sxs-lookup"><span data-stu-id="c298f-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="c298f-111">To polecenie tworzy obiekt opisujący konfigurację autoskalowania opartego na ładowaniu.</span><span class="sxs-lookup"><span data-stu-id="c298f-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="c298f-112">Przykład 2: Tworzenie obiektu opisującego konfigurację autoskalowania na podstawie harmonogramu</span><span class="sxs-lookup"><span data-stu-id="c298f-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="c298f-113">To polecenie tworzy obiekt opisujący konfigurację autoskalowania na podstawie harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="c298f-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="c298f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c298f-114">PARAMETERS</span></span>

### <span data-ttu-id="c298f-115">-Warunek</span><span class="sxs-lookup"><span data-stu-id="c298f-115">-Condition</span></span>
<span data-ttu-id="c298f-116">Pobiera lub ustawia warunek skalowania automatycznego opartego na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="c298f-116">Gets or sets the condition of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="c298f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c298f-117">-DefaultProfile</span></span>
<span data-ttu-id="c298f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c298f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c298f-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="c298f-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="c298f-120">Pobiera lub ustawia maksymalną liczbę workernode dla funkcji automatycznego skalowania opartego na ładowaniu.</span><span class="sxs-lookup"><span data-stu-id="c298f-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="c298f-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="c298f-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="c298f-122">Pobiera lub ustawia minimalną liczbę workernode dla funkcji automatycznego skalowania opartego na ładowaniu.</span><span class="sxs-lookup"><span data-stu-id="c298f-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="c298f-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="c298f-123">-TimeZone</span></span>
<span data-ttu-id="c298f-124">Pobiera lub ustawia strefę czasową skalowania automatycznego opartego na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="c298f-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="c298f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c298f-125">CommonParameters</span></span>
<span data-ttu-id="c298f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c298f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c298f-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c298f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c298f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c298f-128">INPUTS</span></span>

### <span data-ttu-id="c298f-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c298f-129">None</span></span>

## <span data-ttu-id="c298f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c298f-130">OUTPUTS</span></span>

### <span data-ttu-id="c298f-131">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="c298f-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="c298f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c298f-132">NOTES</span></span>

## <span data-ttu-id="c298f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c298f-133">RELATED LINKS</span></span>

<span data-ttu-id="c298f-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c298f-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
