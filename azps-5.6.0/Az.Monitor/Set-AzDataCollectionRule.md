---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
ms.openlocfilehash: e51e43d2555decaa3f37509a89ebe9d55ba2ac96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964321"
---
# <span data-ttu-id="d6761-101">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="d6761-101">Set-AzDataCollectionRule</span></span>

## <span data-ttu-id="d6761-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6761-102">SYNOPSIS</span></span>
<span data-ttu-id="d6761-103">Aktualizuje (zastępuje) regułę zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="d6761-103">Updates (full replacement) a data collection rule.</span></span>

## <span data-ttu-id="d6761-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6761-104">SYNTAX</span></span>

### <span data-ttu-id="d6761-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="d6761-105">ByName (Default)</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -ResourceGroupName <string>
   -RuleName <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="d6761-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6761-106">ByResourceId</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -RuleId <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="d6761-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d6761-107">ByInputObject</span></span>
```
Set-AzDataCollectionRule 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="d6761-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6761-108">DESCRIPTION</span></span>
<span data-ttu-id="d6761-109">Polecenie **cmdlet Set-AzDataCollectionRule** zastępuje istniejącą regułę zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="d6761-109">The **Set-AzDataCollectionRule** cmdlet replaces an existing data collection rule.</span></span>

<span data-ttu-id="d6761-110">Reguły zbierania danych (DCR, Data Collection Rules) definiują dane trafiace do usługi Azure Monitor i określają, gdzie te dane mają być wysyłane lub przechowywane.</span><span class="sxs-lookup"><span data-stu-id="d6761-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="d6761-111">Oto pełny artykuł [z omówieniem funkcji DCR.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="d6761-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="d6761-112">Aby użyć parametru -RuleFile, skonstruuj plik json zawierający trzy właściwości: dataSources, destinations, dataFlows (zobacz przykład #1).</span><span class="sxs-lookup"><span data-stu-id="d6761-112">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1).</span></span>

<span data-ttu-id="d6761-113">Tutaj możesz znaleźć [szczegóły schematu.](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="d6761-113">You may find here the [schema detail](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="d6761-114">Dane wyjściowe dcr serializowane za pomocą polecenia cmdlet ConvertTo-Json (przykład #2).</span><span class="sxs-lookup"><span data-stu-id="d6761-114">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (Example #2).</span></span>

## <span data-ttu-id="d6761-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6761-115">EXAMPLES</span></span>

### <span data-ttu-id="d6761-116">Przykład 1. Aktualizowanie reguły zbierania danych, JSON z interfejsu API rest</span><span class="sxs-lookup"><span data-stu-id="d6761-116">Example 1: Update data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -ResourceGroupName 'testdcr' 
                                -RuleName 'newDcr' 
                                -RuleFile 'C:\samples\dcr1.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr1.json
{
  "properties": {
    "dataSources": {
      "performanceCounters": [
        {
          "streams": [
            "Microsoft-InsightsMetrics"
          ],
          "scheduledTransferPeriod": "PT1M",
          "samplingFrequencyInSeconds": 10,
          "counterSpecifiers": [
            "\\Processor Information(_Total)\\% Processor Time"
          ],
          "name": "perfCounter01"
        }
      ]
    },
    "destinations": {
      "azureMonitorMetrics": {
        "name": "azureMonitorMetrics-default"
      }
    },
    "dataFlows": [
      {
        "streams": [
          "Microsoft-InsightsMetrics"
        ],
        "destinations": [
          "azureMonitorMetrics-default"
        ]
      }
    ]
  }
}
```

<span data-ttu-id="d6761-117">To polecenie zastępuje istniejące reguły zbierania danych dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d6761-117">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="d6761-118">Przykład 2. Aktualizowanie reguły zbierania danych, JSON z usługi PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="d6761-118">Example 2: Update data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr' 
                                -RuleFile 'C:\samples\dcr2.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr2.json
{
  "DataSources": {
    "PerformanceCounters": [
      {
        "Streams": [
          "Microsoft-InsightsMetrics"
        ],
        "ScheduledTransferPeriod": "PT1M",
        "SamplingFrequencyInSeconds": 10,
        "CounterSpecifiers": [
          "\\Processor Information(_Total)\\% Processor Time"
        ],
        "Name": "perfCounter01"
      }
    ]
  },
  "Destinations": {
    "AzureMonitorMetrics": {
      "Name": "azureMonitorMetrics-default"
    }
  },
  "DataFlows": [
    {
      "Streams": [
        "Microsoft-InsightsMetrics"
      ],
      "Destinations": [
        "azureMonitorMetrics-default"
      ]
    }
  ]
}
```

<span data-ttu-id="d6761-119">To polecenie zastępuje istniejące reguły zbierania danych dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d6761-119">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="d6761-120">Przykład 3. Aktualizowanie reguły zbierania danych z obiektu</span><span class="sxs-lookup"><span data-stu-id="d6761-120">Example 3: Update data collection rule from object</span></span>
```powershell
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr.Description = 'This is a test'
PS C:\>$dcr | Set-AzDataCollectionRule

Description       : This is a test
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : {provState}
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

## <span data-ttu-id="d6761-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6761-121">PARAMETERS</span></span>

### <span data-ttu-id="d6761-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6761-122">-DefaultProfile</span></span>
<span data-ttu-id="d6761-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d6761-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6761-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d6761-124">-Location</span></span>
<span data-ttu-id="d6761-125">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="d6761-125">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6761-126">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="d6761-126">-RuleFile</span></span>
<span data-ttu-id="d6761-127">Ścieżka pliku JSON</span><span class="sxs-lookup"><span data-stu-id="d6761-127">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6761-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6761-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6761-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d6761-129">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6761-130">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d6761-130">-RuleName</span></span>
<span data-ttu-id="d6761-131">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="d6761-131">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6761-132">-RuleId</span><span class="sxs-lookup"><span data-stu-id="d6761-132">-RuleId</span></span>
<span data-ttu-id="d6761-133">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="d6761-133">The resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6761-134">— Opis</span><span class="sxs-lookup"><span data-stu-id="d6761-134">-Description</span></span>
<span data-ttu-id="d6761-135">Opis zasobu</span><span class="sxs-lookup"><span data-stu-id="d6761-135">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6761-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="d6761-136">-Tag</span></span>
<span data-ttu-id="d6761-137">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="d6761-137">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6761-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6761-138">-InputObject</span></span>
<span data-ttu-id="d6761-139">Obiekt PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="d6761-139">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="d6761-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6761-140">-Confirm</span></span>
<span data-ttu-id="d6761-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6761-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6761-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6761-142">-WhatIf</span></span>
<span data-ttu-id="d6761-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6761-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6761-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d6761-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6761-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6761-145">CommonParameters</span></span>
<span data-ttu-id="d6761-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6761-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6761-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6761-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6761-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6761-148">INPUTS</span></span>

### <span data-ttu-id="d6761-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d6761-149">System.String</span></span>

## <span data-ttu-id="d6761-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6761-150">OUTPUTS</span></span>

### <span data-ttu-id="d6761-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="d6761-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="d6761-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6761-152">NOTES</span></span>

## <span data-ttu-id="d6761-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6761-153">RELATED LINKS</span></span>

<span data-ttu-id="d6761-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="d6761-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>