---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338674"
---
# <span data-ttu-id="621f3-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="621f3-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="621f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="621f3-102">SYNOPSIS</span></span>
<span data-ttu-id="621f3-103">Wywołaj zapytanie metryki konfiguracji urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="621f3-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="621f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="621f3-104">SYNTAX</span></span>

### <span data-ttu-id="621f3-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="621f3-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="621f3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="621f3-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="621f3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="621f3-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="621f3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="621f3-108">DESCRIPTION</span></span>
<span data-ttu-id="621f3-109">Oceń niestandardową wartość docelową lub metrykę systemową zdefiniowaną w konfiguracji urządzenia IoT.</span><span class="sxs-lookup"><span data-stu-id="621f3-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="621f3-110">Istnieją wstępnie zdefiniowane metryki systemowe, które są obliczane przez Centrum IoT i nie można ich dostosowywać.</span><span class="sxs-lookup"><span data-stu-id="621f3-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="621f3-111">"Cel" określa liczbę Twins urządzenia, które pasują do warunku docelowego.</span><span class="sxs-lookup"><span data-stu-id="621f3-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="621f3-112">W polu "zastosowano" określono liczbę Twins urządzenia, które zostały zmodyfikowane przez konfigurację.</span><span class="sxs-lookup"><span data-stu-id="621f3-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="621f3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="621f3-113">EXAMPLES</span></span>

### <span data-ttu-id="621f3-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="621f3-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="621f3-115">Oceń niestandardową zdefiniowaną metryczną wartość "warningLimit".</span><span class="sxs-lookup"><span data-stu-id="621f3-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="621f3-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="621f3-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="621f3-117">Oceń metryczną "zastosowaną przez system".</span><span class="sxs-lookup"><span data-stu-id="621f3-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="621f3-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="621f3-118">PARAMETERS</span></span>

### <span data-ttu-id="621f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621f3-119">-DefaultProfile</span></span>
<span data-ttu-id="621f3-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="621f3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="621f3-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="621f3-121">-InputObject</span></span>
<span data-ttu-id="621f3-122">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="621f3-122">IotHub object</span></span>

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

### <span data-ttu-id="621f3-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="621f3-123">-IotHubName</span></span>
<span data-ttu-id="621f3-124">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="621f3-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="621f3-125">-Metricname</span><span class="sxs-lookup"><span data-stu-id="621f3-125">-MetricName</span></span>
<span data-ttu-id="621f3-126">Docelowa Metryka dla oceny.</span><span class="sxs-lookup"><span data-stu-id="621f3-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="621f3-127">-Metrictype</span><span class="sxs-lookup"><span data-stu-id="621f3-127">-MetricType</span></span>
<span data-ttu-id="621f3-128">Wskazuje, która kolekcja metryk powinna być używana do wyszukiwania metryki.</span><span class="sxs-lookup"><span data-stu-id="621f3-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="621f3-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="621f3-129">-Name</span></span>
<span data-ttu-id="621f3-130">Identyfikator konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="621f3-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="621f3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="621f3-131">-ResourceGroupName</span></span>
<span data-ttu-id="621f3-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="621f3-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="621f3-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="621f3-133">-ResourceId</span></span>
<span data-ttu-id="621f3-134">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="621f3-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="621f3-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="621f3-135">-Confirm</span></span>
<span data-ttu-id="621f3-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="621f3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="621f3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="621f3-137">-WhatIf</span></span>
<span data-ttu-id="621f3-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="621f3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="621f3-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="621f3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="621f3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621f3-140">CommonParameters</span></span>
<span data-ttu-id="621f3-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="621f3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621f3-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="621f3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621f3-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="621f3-143">INPUTS</span></span>

### <span data-ttu-id="621f3-144">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="621f3-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="621f3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="621f3-145">System.String</span></span>

## <span data-ttu-id="621f3-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="621f3-146">OUTPUTS</span></span>

### <span data-ttu-id="621f3-147">Microsoft. Azure. Commands. Management. IotHub. models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="621f3-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="621f3-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="621f3-148">NOTES</span></span>

## <span data-ttu-id="621f3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="621f3-149">RELATED LINKS</span></span>
