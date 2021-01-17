---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348838"
---
# <span data-ttu-id="949d4-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="949d4-101">Get-AzActionRule</span></span>

## <span data-ttu-id="949d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="949d4-102">SYNOPSIS</span></span>
<span data-ttu-id="949d4-103">Uzyskiwanie informacji o regułach akcji</span><span class="sxs-lookup"><span data-stu-id="949d4-103">Get Action Rules Information</span></span>

## <span data-ttu-id="949d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="949d4-104">SYNTAX</span></span>

### <span data-ttu-id="949d4-105">ListActionRules (domyślny)</span><span class="sxs-lookup"><span data-stu-id="949d4-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="949d4-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="949d4-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="949d4-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="949d4-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="949d4-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="949d4-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="949d4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="949d4-109">DESCRIPTION</span></span>
<span data-ttu-id="949d4-110">Polecenie cmdlet **Get-AzActionRule** pobiera reguły akcji.</span><span class="sxs-lookup"><span data-stu-id="949d4-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="949d4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="949d4-111">EXAMPLES</span></span>

### <span data-ttu-id="949d4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="949d4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="949d4-113">Lista wszystkich reguł akcji skonfigurowanych w obszarze test grupy zasobów — RG filtrowane w usłudze Sev2 wskaźnik ważności i monitorowania platformy.</span><span class="sxs-lookup"><span data-stu-id="949d4-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="949d4-114">Użyj Format-List, aby wyświetlić szczegóły poszczególnych reguł akcji na liście.</span><span class="sxs-lookup"><span data-stu-id="949d4-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="949d4-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="949d4-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="949d4-116">Pobierz regułę akcji z opcją test nazwy-Action (reguła) w grupie test-RG.</span><span class="sxs-lookup"><span data-stu-id="949d4-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="949d4-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="949d4-117">PARAMETERS</span></span>

### <span data-ttu-id="949d4-118">-Action</span><span class="sxs-lookup"><span data-stu-id="949d4-118">-ActionGroup</span></span>
<span data-ttu-id="949d4-119">Grupa akcji</span><span class="sxs-lookup"><span data-stu-id="949d4-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="949d4-120">-AlertRuleId</span></span>
<span data-ttu-id="949d4-121">Filtrowanie według identyfikatora reguły alertu</span><span class="sxs-lookup"><span data-stu-id="949d4-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="949d4-122">-DefaultProfile</span></span>
<span data-ttu-id="949d4-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="949d4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="949d4-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="949d4-124">-Description</span></span>
<span data-ttu-id="949d4-125">Filtrowanie wszystkich alertów o identyfikatorze grupy inteligentnej</span><span class="sxs-lookup"><span data-stu-id="949d4-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="949d4-126">-ImpactedScope</span></span>
<span data-ttu-id="949d4-127">Filtrowanie według zakresu objętego wpływem</span><span class="sxs-lookup"><span data-stu-id="949d4-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="949d4-128">-MonitorService</span></span>
<span data-ttu-id="949d4-129">Filtrowanie w usłudze moniter</span><span class="sxs-lookup"><span data-stu-id="949d4-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="949d4-130">-Name</span></span>
<span data-ttu-id="949d4-131">Nazwa reguły akcji.</span><span class="sxs-lookup"><span data-stu-id="949d4-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="949d4-132">-ResourceGroupName</span></span>
<span data-ttu-id="949d4-133">Nazwa grupy zasobów, w której znajduje się reguła akcji.</span><span class="sxs-lookup"><span data-stu-id="949d4-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="949d4-134">-ResourceId</span></span>
<span data-ttu-id="949d4-135">Pobierz regułę akcji według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="949d4-135">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-136">— Ważność</span><span class="sxs-lookup"><span data-stu-id="949d4-136">-Severity</span></span>
<span data-ttu-id="949d4-137">Filtrowanie według dotkliwości alertu</span><span class="sxs-lookup"><span data-stu-id="949d4-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="949d4-138">-TargetResourceGroup</span></span>
<span data-ttu-id="949d4-139">Filtruj według nazwy grupy zasobów dla zasobu docelowego alertu.</span><span class="sxs-lookup"><span data-stu-id="949d4-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="949d4-140">-TargetResourceId</span></span>
<span data-ttu-id="949d4-141">Filtrowanie identyfikatora zasobu dla docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="949d4-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="949d4-142">-TargetResourceType</span></span>
<span data-ttu-id="949d4-143">Filtrowanie według typu zasobu docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="949d4-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949d4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="949d4-144">CommonParameters</span></span>
<span data-ttu-id="949d4-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="949d4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="949d4-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="949d4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="949d4-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="949d4-147">INPUTS</span></span>

### <span data-ttu-id="949d4-148">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="949d4-148">None</span></span>

## <span data-ttu-id="949d4-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="949d4-149">OUTPUTS</span></span>

### <span data-ttu-id="949d4-150">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="949d4-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="949d4-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="949d4-151">NOTES</span></span>

## <span data-ttu-id="949d4-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="949d4-152">RELATED LINKS</span></span>
