---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
ms.openlocfilehash: 864b3c8abe2411316edf155c49757c1082a863a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190090"
---
# <span data-ttu-id="3b89d-101">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="3b89d-101">Set-AzDataCollectionRule</span></span>

## <span data-ttu-id="3b89d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b89d-102">SYNOPSIS</span></span>
<span data-ttu-id="3b89d-103">Aktualizuje (zastępuje) regułę zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="3b89d-103">Updates (full replacement) a data collection rule.</span></span>

## <span data-ttu-id="3b89d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3b89d-104">SYNTAX</span></span>

### <span data-ttu-id="3b89d-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="3b89d-105">ByName (Default)</span></span>
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

### <span data-ttu-id="3b89d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b89d-106">ByResourceId</span></span>
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

### <span data-ttu-id="3b89d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3b89d-107">ByInputObject</span></span>
```
Set-AzDataCollectionRule 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="3b89d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3b89d-108">DESCRIPTION</span></span>
<span data-ttu-id="3b89d-109">Polecenie **cmdlet Set-AzDataCollectionRule** zastępuje istniejącą regułę zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="3b89d-109">The **Set-AzDataCollectionRule** cmdlet replaces an existing data collection rule.</span></span>

<span data-ttu-id="3b89d-110">Reguły zbierania danych (DCR, Data Collection Rules) definiują dane przesyłane do usługi Azure Monitor i określają, gdzie te dane mają być wysyłane lub przechowywane.</span><span class="sxs-lookup"><span data-stu-id="3b89d-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="3b89d-111">Oto pełny artykuł [z omówieniem funkcji DCR.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="3b89d-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="3b89d-112">Aby użyć parametru -RuleFile, skonstruuj plik json zawierający trzy właściwości: dataSources, destinations, dataFlows (zobacz przykład #1).</span><span class="sxs-lookup"><span data-stu-id="3b89d-112">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1).</span></span>

<span data-ttu-id="3b89d-113">Tutaj możesz znaleźć [szczegóły schematu.](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="3b89d-113">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="3b89d-114">Dane wyjściowe dcr serializowane za pomocą polecenia cmdlet ConvertTo-Json (przykład #2).</span><span class="sxs-lookup"><span data-stu-id="3b89d-114">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (Example #2).</span></span>

## <span data-ttu-id="3b89d-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3b89d-115">EXAMPLES</span></span>

### <span data-ttu-id="3b89d-116">Przykład 1. Aktualizowanie reguły zbierania danych, JSON z interfejsu API rest</span><span class="sxs-lookup"><span data-stu-id="3b89d-116">Example 1: Update data collection rule, JSON from Rest API</span></span>
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

<span data-ttu-id="3b89d-117">To polecenie zastępuje istniejące reguły zbierania danych dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3b89d-117">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="3b89d-118">Przykład 2. Aktualizowanie reguły zbierania danych, JSON z usługi PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="3b89d-118">Example 2: Update data collection rule, JSON from PSDataCollectionRuleResource</span></span>
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

<span data-ttu-id="3b89d-119">To polecenie zastępuje istniejące reguły zbierania danych dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3b89d-119">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="3b89d-120">Przykład 3. Aktualizowanie reguły zbierania danych z obiektu</span><span class="sxs-lookup"><span data-stu-id="3b89d-120">Example 3: Update data collection rule from object</span></span>
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

## <span data-ttu-id="3b89d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b89d-121">PARAMETERS</span></span>

### <span data-ttu-id="3b89d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b89d-122">-DefaultProfile</span></span>
<span data-ttu-id="3b89d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3b89d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b89d-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3b89d-124">-Location</span></span>
<span data-ttu-id="3b89d-125">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="3b89d-125">The resource location</span></span>

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

### <span data-ttu-id="3b89d-126">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="3b89d-126">-RuleFile</span></span>
<span data-ttu-id="3b89d-127">Ścieżka pliku JSON</span><span class="sxs-lookup"><span data-stu-id="3b89d-127">The JSON file path</span></span>

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

### <span data-ttu-id="3b89d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b89d-128">-ResourceGroupName</span></span>
<span data-ttu-id="3b89d-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3b89d-129">The resource group name</span></span>

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

### <span data-ttu-id="3b89d-130">-RuleName</span><span class="sxs-lookup"><span data-stu-id="3b89d-130">-RuleName</span></span>
<span data-ttu-id="3b89d-131">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="3b89d-131">The resource name</span></span>

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

### <span data-ttu-id="3b89d-132">-RuleId</span><span class="sxs-lookup"><span data-stu-id="3b89d-132">-RuleId</span></span>
<span data-ttu-id="3b89d-133">Identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="3b89d-133">The resource ID</span></span>

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

### <span data-ttu-id="3b89d-134">— Opis</span><span class="sxs-lookup"><span data-stu-id="3b89d-134">-Description</span></span>
<span data-ttu-id="3b89d-135">Opis zasobu</span><span class="sxs-lookup"><span data-stu-id="3b89d-135">The resource description</span></span>

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

### <span data-ttu-id="3b89d-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="3b89d-136">-Tag</span></span>
<span data-ttu-id="3b89d-137">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="3b89d-137">The resource tags</span></span>

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

### <span data-ttu-id="3b89d-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b89d-138">-InputObject</span></span>
<span data-ttu-id="3b89d-139">Obiekt PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="3b89d-139">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="3b89d-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b89d-140">-Confirm</span></span>
<span data-ttu-id="3b89d-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3b89d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b89d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b89d-142">-WhatIf</span></span>
<span data-ttu-id="3b89d-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b89d-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b89d-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3b89d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b89d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b89d-145">CommonParameters</span></span>
<span data-ttu-id="3b89d-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b89d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b89d-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b89d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b89d-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b89d-148">INPUTS</span></span>

### <span data-ttu-id="3b89d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3b89d-149">System.String</span></span>

## <span data-ttu-id="3b89d-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b89d-150">OUTPUTS</span></span>

### <span data-ttu-id="3b89d-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="3b89d-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="3b89d-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3b89d-152">NOTES</span></span>

## <span data-ttu-id="3b89d-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b89d-153">RELATED LINKS</span></span>

<span data-ttu-id="3b89d-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="3b89d-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>