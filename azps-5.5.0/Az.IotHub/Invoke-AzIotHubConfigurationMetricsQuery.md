---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203902"
---
# <span data-ttu-id="8c4e1-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="8c4e1-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="8c4e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4e1-103">Wywołaj zapytanie metryczne konfiguracji urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="8c4e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c4e1-104">SYNTAX</span></span>

### <span data-ttu-id="8c4e1-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8c4e1-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c4e1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8c4e1-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c4e1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8c4e1-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c4e1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c4e1-108">DESCRIPTION</span></span>
<span data-ttu-id="8c4e1-109">Oceń docelową metrykę niestandardową lub metrykę systemu zdefiniowaną w konfiguracji urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="8c4e1-110">Istnieją wstępnie zdefiniowane metryki systemu, które są obliczane przez centrum Iot i nie można ich dostosować.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="8c4e1-111">"Targeted" określa liczbę urządzeń, które pasują do warunku docelowego.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="8c4e1-112">"Zastosowano" określa liczbę urządzeń zmodyfikowanych przez konfigurację.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="8c4e1-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c4e1-113">EXAMPLES</span></span>

### <span data-ttu-id="8c4e1-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c4e1-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="8c4e1-115">Oceń metrykę "warningLimit" zdefiniowaną niestandardową.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="8c4e1-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8c4e1-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="8c4e1-117">Oceń metrykę "zastosowanego" systemu.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="8c4e1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c4e1-118">PARAMETERS</span></span>

### <span data-ttu-id="8c4e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c4e1-119">-DefaultProfile</span></span>
<span data-ttu-id="8c4e1-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c4e1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c4e1-121">-InputObject</span></span>
<span data-ttu-id="8c4e1-122">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="8c4e1-122">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e1-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8c4e1-123">-IotHubName</span></span>
<span data-ttu-id="8c4e1-124">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="8c4e1-124">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e1-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="8c4e1-125">-MetricName</span></span>
<span data-ttu-id="8c4e1-126">Metryka docelowa oceny.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-126">Target metric for evaluation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e1-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="8c4e1-127">-MetricType</span></span>
<span data-ttu-id="8c4e1-128">Wskazuje, która kolekcja metryki powinna być używana do wyszukiwania metryki.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-128">Indicates which metric collection should be used to lookup a metric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricType
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e1-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c4e1-129">-Name</span></span>
<span data-ttu-id="8c4e1-130">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-130">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c4e1-131">-ResourceGroupName</span></span>
<span data-ttu-id="8c4e1-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8c4e1-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c4e1-133">-ResourceId</span></span>
<span data-ttu-id="8c4e1-134">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="8c4e1-134">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4e1-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c4e1-135">-Confirm</span></span>
<span data-ttu-id="8c4e1-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c4e1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c4e1-137">-WhatIf</span></span>
<span data-ttu-id="8c4e1-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c4e1-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c4e1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4e1-140">CommonParameters</span></span>
<span data-ttu-id="8c4e1-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c4e1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4e1-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c4e1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4e1-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c4e1-143">INPUTS</span></span>

### <span data-ttu-id="8c4e1-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8c4e1-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8c4e1-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8c4e1-145">System.String</span></span>

## <span data-ttu-id="8c4e1-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c4e1-146">OUTPUTS</span></span>

### <span data-ttu-id="8c4e1-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="8c4e1-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="8c4e1-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c4e1-148">NOTES</span></span>

## <span data-ttu-id="8c4e1-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c4e1-149">RELATED LINKS</span></span>
