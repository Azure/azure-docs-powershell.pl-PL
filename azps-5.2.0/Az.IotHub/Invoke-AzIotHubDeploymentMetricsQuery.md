---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338662"
---
# <span data-ttu-id="17640-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="17640-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="17640-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17640-102">SYNOPSIS</span></span>
<span data-ttu-id="17640-103">Wywołanie zapytania metryki wdrażania programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="17640-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="17640-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17640-104">SYNTAX</span></span>

### <span data-ttu-id="17640-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="17640-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17640-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="17640-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17640-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="17640-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17640-108">Opis</span><span class="sxs-lookup"><span data-stu-id="17640-108">DESCRIPTION</span></span>
<span data-ttu-id="17640-109">Oceń niestandardową metrykę docelową lub systemową zdefiniowaną w rozmieszczeniu programu IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="17640-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="17640-110">Istnieją wstępnie zdefiniowane metryki systemowe, które są obliczane przez Centrum IoT i nie można ich dostosowywać.</span><span class="sxs-lookup"><span data-stu-id="17640-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="17640-111">"Docelowy" przedstawia urządzenia IoT Edge, które pasują do warunku określania wartości docelowej wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="17640-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="17640-112">"Zastosowano" pokazuje docelowe urządzenia IoT Edge, które nie są ukierunkowane na inne wdrożenie o wyższym priorytecie.</span><span class="sxs-lookup"><span data-stu-id="17640-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="17640-113">"Powodzenie raportowania" przedstawia urządzenia IoT Edge, które zgłosiły, że moduły zostały pomyślnie wdrożone.</span><span class="sxs-lookup"><span data-stu-id="17640-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="17640-114">"Błąd raportowania" przedstawia urządzenia IoT Edge, które zgłosiły, że nie został pomyślnie wdrożony jeden lub więcej modułów.</span><span class="sxs-lookup"><span data-stu-id="17640-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="17640-115">Aby dokładniej zbadać błąd, Połącz się zdalnie z tymi urządzeniami i Przejrzyj pliki dziennika.</span><span class="sxs-lookup"><span data-stu-id="17640-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="17640-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17640-116">EXAMPLES</span></span>

### <span data-ttu-id="17640-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="17640-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="17640-118">Oceń niestandardową zdefiniowaną metryczną wartość "warningLimit".</span><span class="sxs-lookup"><span data-stu-id="17640-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="17640-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="17640-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="17640-120">Oceń metrykę "sukces raportowania" systemu.</span><span class="sxs-lookup"><span data-stu-id="17640-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="17640-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17640-121">PARAMETERS</span></span>

### <span data-ttu-id="17640-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17640-122">-DefaultProfile</span></span>
<span data-ttu-id="17640-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17640-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17640-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="17640-124">-InputObject</span></span>
<span data-ttu-id="17640-125">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="17640-125">IotHub object</span></span>

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

### <span data-ttu-id="17640-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="17640-126">-IotHubName</span></span>
<span data-ttu-id="17640-127">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="17640-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="17640-128">-Metricname</span><span class="sxs-lookup"><span data-stu-id="17640-128">-MetricName</span></span>
<span data-ttu-id="17640-129">Docelowa Metryka dla oceny.</span><span class="sxs-lookup"><span data-stu-id="17640-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="17640-130">-Metrictype</span><span class="sxs-lookup"><span data-stu-id="17640-130">-MetricType</span></span>
<span data-ttu-id="17640-131">Wskazuje, która kolekcja metryk powinna być używana do wyszukiwania metryki.</span><span class="sxs-lookup"><span data-stu-id="17640-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="17640-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="17640-132">-Name</span></span>
<span data-ttu-id="17640-133">Identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="17640-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="17640-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17640-134">-ResourceGroupName</span></span>
<span data-ttu-id="17640-135">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="17640-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="17640-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17640-136">-ResourceId</span></span>
<span data-ttu-id="17640-137">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="17640-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="17640-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17640-138">-Confirm</span></span>
<span data-ttu-id="17640-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17640-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17640-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17640-140">-WhatIf</span></span>
<span data-ttu-id="17640-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17640-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17640-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="17640-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17640-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17640-143">CommonParameters</span></span>
<span data-ttu-id="17640-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17640-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17640-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17640-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17640-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17640-146">INPUTS</span></span>

### <span data-ttu-id="17640-147">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="17640-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="17640-148">System. String</span><span class="sxs-lookup"><span data-stu-id="17640-148">System.String</span></span>

## <span data-ttu-id="17640-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17640-149">OUTPUTS</span></span>

### <span data-ttu-id="17640-150">Microsoft. Azure. Commands. Management. IotHub. models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="17640-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="17640-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17640-151">NOTES</span></span>

## <span data-ttu-id="17640-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17640-152">RELATED LINKS</span></span>
