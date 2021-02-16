---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 8826dfdf8fe0152035319c576210088bcd5521e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180194"
---
# <span data-ttu-id="33e60-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="33e60-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="33e60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33e60-102">SYNOPSIS</span></span>
<span data-ttu-id="33e60-103">Pobiera reguły zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="33e60-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="33e60-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33e60-104">SYNTAX</span></span>

### <span data-ttu-id="33e60-105">BySubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="33e60-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="33e60-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="33e60-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="33e60-107">ByName</span><span class="sxs-lookup"><span data-stu-id="33e60-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="33e60-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="33e60-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="33e60-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="33e60-109">DESCRIPTION</span></span>
<span data-ttu-id="33e60-110">Polecenie **cmdlet Get-AzDataCollectionRule** pobiera jedną lub więcej reguł zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="33e60-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="33e60-111">Reguły zbierania danych (DCR, Data Collection Rules) definiują dane przesyłane do usługi Azure Monitor i określają, gdzie te dane mają być wysyłane lub przechowywane.</span><span class="sxs-lookup"><span data-stu-id="33e60-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="33e60-112">Oto pełny artykuł [z omówieniem funkcji DCR.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="33e60-112">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="33e60-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33e60-113">EXAMPLES</span></span>

### <span data-ttu-id="33e60-114">Przykład 1. Pobieranie reguł zbierania danych według identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="33e60-114">Example 1: Get data collection rules by subscription ID</span></span>
```
PS C:\>Get-AzDataCollectionRule

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="33e60-115">To polecenie zawiera listę wszystkich reguł zbierania danych dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="33e60-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="33e60-116">Przykład 2. Pobieranie reguł zbierania danych dla danej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="33e60-116">Example 2: Get data collection rules for the given resource group</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="33e60-117">To polecenie zawiera listę reguł zbierania danych dla danej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="33e60-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="33e60-118">Przykład 3. Pobieranie reguły zbierania danych</span><span class="sxs-lookup"><span data-stu-id="33e60-118">Example 3: Get a data collection rule</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup" -RuleName "testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="33e60-119">To polecenie wyświetla jedną regułę zbierania danych (listę z jednym elementem).</span><span class="sxs-lookup"><span data-stu-id="33e60-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="33e60-120">Przykład 4. Pobieranie reguły zbierania danych według identyfikatora reguły</span><span class="sxs-lookup"><span data-stu-id="33e60-120">Example 4: Get a data collection rule by Rule ID</span></span>
```
PS C:\>Get-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="33e60-121">To polecenie wyświetla jedną regułę zbierania danych (listę z jednym elementem).</span><span class="sxs-lookup"><span data-stu-id="33e60-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="33e60-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33e60-122">PARAMETERS</span></span>

### <span data-ttu-id="33e60-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e60-123">-DefaultProfile</span></span>
<span data-ttu-id="33e60-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="33e60-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33e60-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e60-125">-ResourceGroupName</span></span>
<span data-ttu-id="33e60-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="33e60-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e60-127">-RuleName</span><span class="sxs-lookup"><span data-stu-id="33e60-127">-RuleName</span></span>
<span data-ttu-id="33e60-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="33e60-128">The name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e60-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="33e60-129">-RuleId</span></span>
<span data-ttu-id="33e60-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="33e60-130">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e60-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e60-131">CommonParameters</span></span>
<span data-ttu-id="33e60-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33e60-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e60-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33e60-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e60-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33e60-134">INPUTS</span></span>

### <span data-ttu-id="33e60-135">System.String</span><span class="sxs-lookup"><span data-stu-id="33e60-135">System.String</span></span>

## <span data-ttu-id="33e60-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="33e60-136">OUTPUTS</span></span>

### <span data-ttu-id="33e60-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="33e60-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="33e60-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33e60-138">NOTES</span></span>

## <span data-ttu-id="33e60-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33e60-139">RELATED LINKS</span></span>

<span data-ttu-id="33e60-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="33e60-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
