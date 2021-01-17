---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bb22bda0f22ae128942e6e1d5a7aed9b0b646875
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328328"
---
# <span data-ttu-id="19dd3-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="19dd3-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="19dd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="19dd3-103">Ustawia konfigurację autoskalowania klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="19dd3-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="19dd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19dd3-104">SYNTAX</span></span>

### <span data-ttu-id="19dd3-105">LoadAutoscaleByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="19dd3-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd3-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dd3-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd3-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dd3-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd3-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dd3-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19dd3-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dd3-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd3-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dd3-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd3-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dd3-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd3-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dd3-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd3-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dd3-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19dd3-114">Opis</span><span class="sxs-lookup"><span data-stu-id="19dd3-114">DESCRIPTION</span></span>
<span data-ttu-id="19dd3-115">Ten aplet polecenia **Set-AzHDInsightClusterAutoscaleConfiguration** ustawia konfigurację autoskalowania klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="19dd3-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="19dd3-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19dd3-116">EXAMPLES</span></span>

### <span data-ttu-id="19dd3-117">Przykład 1: Ustawianie konfiguracji automatycznej skalowania klastra usługi HDInsight opartego na ładowaniu</span><span class="sxs-lookup"><span data-stu-id="19dd3-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="19dd3-118">To polecenie ustawia konfigurację autoskalowania opartą na ładowaniu klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="19dd3-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="19dd3-119">Przykład 2: ustawianie automatycznego skalowania klastra usługi HDInsight opartego na harmonogramie</span><span class="sxs-lookup"><span data-stu-id="19dd3-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="19dd3-120">To polecenie ustawia konfigurację autoskalowania opartą na harmonogramie klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="19dd3-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="19dd3-121">Przykład 3: Ustawianie konfiguracji autoskalowania klastra usługi HDInsight na podstawie innego klastra z ustawioną konfiguracją skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="19dd3-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

<span data-ttu-id="19dd3-122">To polecenie ustawia konfigurację autoskalowania klastra usługi HDInsight opartego na innym klastrze.</span><span class="sxs-lookup"><span data-stu-id="19dd3-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="19dd3-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19dd3-123">PARAMETERS</span></span>

### <span data-ttu-id="19dd3-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19dd3-124">-AsJob</span></span>
<span data-ttu-id="19dd3-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="19dd3-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="19dd3-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="19dd3-127">Pobiera lub ustawia konfigurację skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="19dd3-127">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-128">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="19dd3-128">-ClusterName</span></span>
<span data-ttu-id="19dd3-129">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="19dd3-129">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-130">-Warunek</span><span class="sxs-lookup"><span data-stu-id="19dd3-130">-Condition</span></span>
<span data-ttu-id="19dd3-131">Pobiera lub ustawia warunek skalowania automatycznego opartego na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="19dd3-131">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dd3-132">-DefaultProfile</span></span>
<span data-ttu-id="19dd3-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19dd3-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19dd3-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="19dd3-134">-InputObject</span></span>
<span data-ttu-id="19dd3-135">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="19dd3-135">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="19dd3-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="19dd3-137">Pobiera lub ustawia maksymalną liczbę workernode dla funkcji automatycznego skalowania opartego na ładowaniu.</span><span class="sxs-lookup"><span data-stu-id="19dd3-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="19dd3-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="19dd3-139">Pobiera lub ustawia minimalną liczbę workernode dla funkcji automatycznego skalowania opartego na ładowaniu.</span><span class="sxs-lookup"><span data-stu-id="19dd3-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19dd3-140">-ResourceGroupName</span></span>
<span data-ttu-id="19dd3-141">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="19dd3-141">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19dd3-142">-ResourceId</span></span>
<span data-ttu-id="19dd3-143">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="19dd3-143">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-144">-Schedule</span><span class="sxs-lookup"><span data-stu-id="19dd3-144">-Schedule</span></span>
<span data-ttu-id="19dd3-145">Ustawianie parametrów opartych na harmonogramie</span><span class="sxs-lookup"><span data-stu-id="19dd3-145">Set schedule-based parameters</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="19dd3-146">-TimeZone</span></span>
<span data-ttu-id="19dd3-147">Pobiera lub ustawia strefę czasową skalowania automatycznego opartego na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="19dd3-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19dd3-148">-Confirm</span></span>
<span data-ttu-id="19dd3-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19dd3-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19dd3-150">-WhatIf</span></span>
<span data-ttu-id="19dd3-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19dd3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19dd3-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19dd3-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dd3-153">CommonParameters</span></span>
<span data-ttu-id="19dd3-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19dd3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dd3-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19dd3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dd3-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19dd3-156">INPUTS</span></span>

### <span data-ttu-id="19dd3-157">System. String</span><span class="sxs-lookup"><span data-stu-id="19dd3-157">System.String</span></span>

### <span data-ttu-id="19dd3-158">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="19dd3-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="19dd3-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19dd3-159">OUTPUTS</span></span>

### <span data-ttu-id="19dd3-160">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="19dd3-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="19dd3-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19dd3-161">NOTES</span></span>

## <span data-ttu-id="19dd3-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19dd3-162">RELATED LINKS</span></span>

<span data-ttu-id="19dd3-163">[Nowe — AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="19dd3-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
