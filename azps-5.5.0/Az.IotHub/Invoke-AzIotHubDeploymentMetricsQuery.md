---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200115"
---
# <span data-ttu-id="8cc42-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="8cc42-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="8cc42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cc42-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc42-103">Wywołaj zapytanie metryczne wdrożenia IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="8cc42-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="8cc42-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8cc42-104">SYNTAX</span></span>

### <span data-ttu-id="8cc42-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8cc42-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc42-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8cc42-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cc42-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8cc42-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cc42-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8cc42-108">DESCRIPTION</span></span>
<span data-ttu-id="8cc42-109">Oceń docelową metrykę niestandardową lub metrykę systemu zdefiniowaną we wdrożeniu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="8cc42-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="8cc42-110">Istnieją wstępnie zdefiniowane metryki systemu, które są obliczane przez centrum Iot i nie można ich dostosować.</span><span class="sxs-lookup"><span data-stu-id="8cc42-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="8cc42-111">"Kierowane" pokazuje urządzenia Edge IoT, które są zgodne z warunkiem określania docelowych celów wdrażania.</span><span class="sxs-lookup"><span data-stu-id="8cc42-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="8cc42-112">"Zastosowane" pokazuje kierowane urządzenia Edge IoT, które nie są kierowane przez inne wdrożenie o wyższym priorytecie.</span><span class="sxs-lookup"><span data-stu-id="8cc42-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="8cc42-113">"Raportowanie sukcesu" pokazuje urządzenia Edge IoT, które zgłosiły, że moduły zostały wdrożone pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="8cc42-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="8cc42-114">"Błąd raportowania" pokazuje urządzenia edge IoT, które zgłosiły, że co najmniej jeden moduł nie został pomyślnie wdrożony.</span><span class="sxs-lookup"><span data-stu-id="8cc42-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="8cc42-115">Aby dokładniej zbadać błąd, połącz się zdalnie z tymi urządzeniami i wyświetl pliki dziennika.</span><span class="sxs-lookup"><span data-stu-id="8cc42-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="8cc42-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8cc42-116">EXAMPLES</span></span>

### <span data-ttu-id="8cc42-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8cc42-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="8cc42-118">Oceń metrykę "warningLimit" zdefiniowaną niestandardową.</span><span class="sxs-lookup"><span data-stu-id="8cc42-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="8cc42-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8cc42-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="8cc42-120">Oceń metrykę "Raportowanie sukcesu".</span><span class="sxs-lookup"><span data-stu-id="8cc42-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="8cc42-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cc42-121">PARAMETERS</span></span>

### <span data-ttu-id="8cc42-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc42-122">-DefaultProfile</span></span>
<span data-ttu-id="8cc42-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc42-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc42-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cc42-124">-InputObject</span></span>
<span data-ttu-id="8cc42-125">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="8cc42-125">IotHub object</span></span>

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

### <span data-ttu-id="8cc42-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8cc42-126">-IotHubName</span></span>
<span data-ttu-id="8cc42-127">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="8cc42-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8cc42-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="8cc42-128">-MetricName</span></span>
<span data-ttu-id="8cc42-129">Metryka docelowa oceny.</span><span class="sxs-lookup"><span data-stu-id="8cc42-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="8cc42-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="8cc42-130">-MetricType</span></span>
<span data-ttu-id="8cc42-131">Wskazuje, która kolekcja metryki powinna być używana do wyszukiwania metryki.</span><span class="sxs-lookup"><span data-stu-id="8cc42-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="8cc42-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8cc42-132">-Name</span></span>
<span data-ttu-id="8cc42-133">Identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8cc42-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="8cc42-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc42-134">-ResourceGroupName</span></span>
<span data-ttu-id="8cc42-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8cc42-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8cc42-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cc42-136">-ResourceId</span></span>
<span data-ttu-id="8cc42-137">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="8cc42-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8cc42-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8cc42-138">-Confirm</span></span>
<span data-ttu-id="8cc42-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8cc42-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc42-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc42-140">-WhatIf</span></span>
<span data-ttu-id="8cc42-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc42-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc42-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8cc42-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc42-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc42-143">CommonParameters</span></span>
<span data-ttu-id="8cc42-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc42-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc42-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc42-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc42-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cc42-146">INPUTS</span></span>

### <span data-ttu-id="8cc42-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8cc42-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8cc42-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8cc42-148">System.String</span></span>

## <span data-ttu-id="8cc42-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cc42-149">OUTPUTS</span></span>

### <span data-ttu-id="8cc42-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="8cc42-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="8cc42-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8cc42-151">NOTES</span></span>

## <span data-ttu-id="8cc42-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cc42-152">RELATED LINKS</span></span>
