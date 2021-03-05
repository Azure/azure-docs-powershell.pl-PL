---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
ms.openlocfilehash: b14d834e005f8a81666fd98b40d276825f04c0e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984572"
---
# <span data-ttu-id="76fba-101">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="76fba-101">New-AzDataCollectionRule</span></span>

## <span data-ttu-id="76fba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76fba-102">SYNOPSIS</span></span>
<span data-ttu-id="76fba-103">Utwórz regułę zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="76fba-103">Create a data collection rule.</span></span>

## <span data-ttu-id="76fba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76fba-104">SYNTAX</span></span>

### <span data-ttu-id="76fba-105">ByFile (Default)</span><span class="sxs-lookup"><span data-stu-id="76fba-105">ByFile (Default)</span></span>
```
New-AzDataCollectionRule
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

## <span data-ttu-id="76fba-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="76fba-106">DESCRIPTION</span></span>
<span data-ttu-id="76fba-107">Polecenie **cmdlet New-AzDataCollectionRule** tworzy regułę zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="76fba-107">The **New-AzDataCollectionRule** cmdlet creates a data collection rule.</span></span>

<span data-ttu-id="76fba-108">Reguły zbierania danych (DCR, Data Collection Rules) definiują dane trafiace do usługi Azure Monitor i określają, gdzie te dane mają być wysyłane lub przechowywane.</span><span class="sxs-lookup"><span data-stu-id="76fba-108">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="76fba-109">Oto pełny artykuł [z omówieniem funkcji DCR.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="76fba-109">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="76fba-110">Aby użyć parametru -RuleFile, skonstruuj plik json zawierający trzy właściwości: dataSources, destinations, dataFlows (zobacz przykład #1)</span><span class="sxs-lookup"><span data-stu-id="76fba-110">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1)</span></span>

<span data-ttu-id="76fba-111">Tutaj możesz znaleźć [szczegóły schematu.](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="76fba-111">You may find here the [schema detail](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="76fba-112">Dane wyjściowe dcr serializowane za pomocą polecenia cmdlet ConvertTo-Json (zobacz przykład #2).</span><span class="sxs-lookup"><span data-stu-id="76fba-112">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (see Example #2).</span></span>

## <span data-ttu-id="76fba-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76fba-113">EXAMPLES</span></span>

### <span data-ttu-id="76fba-114">Przykład 1. Tworzenie reguły zbierania danych, JSON z interfejsu API rest</span><span class="sxs-lookup"><span data-stu-id="76fba-114">Example 1: Create data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx1' -RuleFile 'C:\samples\dcrEx1.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx1
Name              : newDcrEx1
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx1.json
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

<span data-ttu-id="76fba-115">To polecenie tworzy reguły zbierania danych dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="76fba-115">This command creates a data collection rules for the current subscription.</span></span>

### <span data-ttu-id="76fba-116">Przykład 2. Tworzenie reguły zbierania danych, JSON z usługi PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="76fba-116">Example 2: Create data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx2' -RuleFile 'C:\samples\dcrEx2.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx2
Name              : newDcrEx2
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx2.json
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

<span data-ttu-id="76fba-117">To polecenie tworzy reguły zbierania danych dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="76fba-117">This command creates a data collection rules for the current subscription.</span></span>

## <span data-ttu-id="76fba-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76fba-118">PARAMETERS</span></span>

### <span data-ttu-id="76fba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fba-119">-DefaultProfile</span></span>
<span data-ttu-id="76fba-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="76fba-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76fba-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="76fba-121">-Location</span></span>
<span data-ttu-id="76fba-122">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="76fba-122">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76fba-123">-ResourceGroupName</span></span>
<span data-ttu-id="76fba-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="76fba-124">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fba-125">-RuleName</span><span class="sxs-lookup"><span data-stu-id="76fba-125">-RuleName</span></span>
<span data-ttu-id="76fba-126">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="76fba-126">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fba-127">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="76fba-127">-RuleFile</span></span>
<span data-ttu-id="76fba-128">Ścieżka pliku JSON</span><span class="sxs-lookup"><span data-stu-id="76fba-128">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fba-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="76fba-129">-Description</span></span>
<span data-ttu-id="76fba-130">Opis zasobu</span><span class="sxs-lookup"><span data-stu-id="76fba-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fba-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="76fba-131">-Tag</span></span>
<span data-ttu-id="76fba-132">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="76fba-132">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fba-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76fba-133">-Confirm</span></span>
<span data-ttu-id="76fba-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="76fba-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76fba-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76fba-135">-WhatIf</span></span>
<span data-ttu-id="76fba-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76fba-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76fba-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="76fba-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76fba-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fba-138">CommonParameters</span></span>
<span data-ttu-id="76fba-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76fba-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fba-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76fba-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fba-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76fba-141">INPUTS</span></span>

### <span data-ttu-id="76fba-142">System.String</span><span class="sxs-lookup"><span data-stu-id="76fba-142">System.String</span></span>

## <span data-ttu-id="76fba-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76fba-143">OUTPUTS</span></span>

### <span data-ttu-id="76fba-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="76fba-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="76fba-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76fba-145">NOTES</span></span>

## <span data-ttu-id="76fba-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76fba-146">RELATED LINKS</span></span>

<span data-ttu-id="76fba-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="76fba-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>