---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
ms.openlocfilehash: a655ac87dcc99eca1a8c5a5329d2073d54614ceb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190066"
---
# <span data-ttu-id="ecc75-101">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="ecc75-101">Update-AzDataCollectionRule</span></span>

## <span data-ttu-id="ecc75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecc75-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc75-103">Aktualizuje właściwość tagów reguł zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="ecc75-103">Updates a data collection rule tags property.</span></span>

## <span data-ttu-id="ecc75-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ecc75-104">SYNTAX</span></span>

### <span data-ttu-id="ecc75-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="ecc75-105">ByName (Default)</span></span>
```
Update-AzDataCollectionRule 
      -ResourceGroupName <string> 
      -RuleName <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="ecc75-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecc75-106">ByResourceId</span></span>
```
Update-AzDataCollectionRule 
      -RuleId <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="ecc75-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ecc75-107">ByInputObject</span></span>
```
Update-AzDataCollectionRule 
      -InputObject <PSDataCollectionRuleResource> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="ecc75-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ecc75-108">DESCRIPTION</span></span>
<span data-ttu-id="ecc75-109">Polecenie **cmdlet Update-AzDataCollectionRule** aktualizuje właściwość tagów reguły zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="ecc75-109">The **Update-AzDataCollectionRule** cmdlet updates a data collection rule Tags property.</span></span>

<span data-ttu-id="ecc75-110">Reguły zbierania danych (DCR, Data Collection Rules) definiują dane trafiace do usługi Azure Monitor i określają, gdzie te dane mają być wysyłane lub przechowywane.</span><span class="sxs-lookup"><span data-stu-id="ecc75-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="ecc75-111">Oto pełny artykuł [z omówieniem funkcji DCR.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="ecc75-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="ecc75-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ecc75-112">EXAMPLES</span></span>

### <span data-ttu-id="ecc75-113">Przykład 1. Aktualizowanie tagów reguł zbierania danych</span><span class="sxs-lookup"><span data-stu-id="ecc75-113">Example 1: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleName 'newDcr'
                                   -ResourceGroupName 'testdcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="ecc75-114">To polecenie aktualizuje właściwość tagów dla danej reguły zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="ecc75-114">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="ecc75-115">Przykład 2. Aktualizowanie tagów reguł zbierania danych</span><span class="sxs-lookup"><span data-stu-id="ecc75-115">Example 2: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="ecc75-116">To polecenie aktualizuje właściwość tagów dla danej reguły zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="ecc75-116">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="ecc75-117">Przykład 3. Aktualizowanie tagów reguł zbierania danych</span><span class="sxs-lookup"><span data-stu-id="ecc75-117">Example 3: Update data collection rule tags</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr | Update-AzDataCollectionRule -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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

<span data-ttu-id="ecc75-118">To polecenie aktualizuje właściwość tagów dla danej reguły zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="ecc75-118">This command updates the tags property for the given data collection rule.</span></span>

## <span data-ttu-id="ecc75-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecc75-119">PARAMETERS</span></span>

### <span data-ttu-id="ecc75-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc75-120">-DefaultProfile</span></span>
<span data-ttu-id="ecc75-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ecc75-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecc75-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecc75-122">-ResourceGroupName</span></span>
<span data-ttu-id="ecc75-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ecc75-123">The resource group name</span></span>

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

### <span data-ttu-id="ecc75-124">-RuleName</span><span class="sxs-lookup"><span data-stu-id="ecc75-124">-RuleName</span></span>
<span data-ttu-id="ecc75-125">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="ecc75-125">The resource name</span></span>

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

### <span data-ttu-id="ecc75-126">-RuleId</span><span class="sxs-lookup"><span data-stu-id="ecc75-126">-RuleId</span></span>
<span data-ttu-id="ecc75-127">Identyfikator zasobu reguły zbierania danych</span><span class="sxs-lookup"><span data-stu-id="ecc75-127">The resource ID of the data collection rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="ecc75-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecc75-128">-InputObject</span></span>
<span data-ttu-id="ecc75-129">Obiekt PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="ecc75-129">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="ecc75-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="ecc75-130">-Tag</span></span>
<span data-ttu-id="ecc75-131">Właściwość tagów reguły zbierania danych</span><span class="sxs-lookup"><span data-stu-id="ecc75-131">The tags property of the data collection rule</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: Falose
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc75-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ecc75-132">-Confirm</span></span>
<span data-ttu-id="ecc75-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ecc75-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecc75-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecc75-134">-WhatIf</span></span>
<span data-ttu-id="ecc75-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc75-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecc75-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ecc75-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecc75-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc75-137">CommonParameters</span></span>
<span data-ttu-id="ecc75-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc75-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc75-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecc75-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc75-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecc75-140">INPUTS</span></span>

### <span data-ttu-id="ecc75-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ecc75-141">System.String</span></span>

## <span data-ttu-id="ecc75-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecc75-142">OUTPUTS</span></span>

### <span data-ttu-id="ecc75-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="ecc75-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="ecc75-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ecc75-144">NOTES</span></span>

## <span data-ttu-id="ecc75-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecc75-145">RELATED LINKS</span></span>

<span data-ttu-id="ecc75-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="ecc75-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span></span>