---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192626"
---
# <span data-ttu-id="6b717-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="6b717-101">Get-AzActionRule</span></span>

## <span data-ttu-id="6b717-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b717-102">SYNOPSIS</span></span>
<span data-ttu-id="6b717-103">Uzyskiwanie informacji o zasadach akcji</span><span class="sxs-lookup"><span data-stu-id="6b717-103">Get Action Rules Information</span></span>

## <span data-ttu-id="6b717-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6b717-104">SYNTAX</span></span>

### <span data-ttu-id="6b717-105">ListActionRules (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6b717-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b717-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b717-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b717-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="6b717-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b717-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6b717-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b717-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="6b717-109">DESCRIPTION</span></span>
<span data-ttu-id="6b717-110">**Polecenie cmdlet Get-AzActionRule** pobiera skonfigurowane reguły akcji.</span><span class="sxs-lookup"><span data-stu-id="6b717-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="6b717-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6b717-111">EXAMPLES</span></span>

### <span data-ttu-id="6b717-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6b717-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="6b717-113">Lista wszystkich reguł akcji skonfigurowanych w teście grupy zasobów filtrowanych według istotności Sev2 i usługi monitora platformy.</span><span class="sxs-lookup"><span data-stu-id="6b717-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="6b717-114">Użyj Format-List, aby uzyskać szczegółowe informacje dotyczące każdej reguły akcji na liście.</span><span class="sxs-lookup"><span data-stu-id="6b717-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="6b717-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6b717-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="6b717-116">Pobierz regułę akcji z nazwą Reguła akcji testowej w grupie zasobów test-rg.</span><span class="sxs-lookup"><span data-stu-id="6b717-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="6b717-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b717-117">PARAMETERS</span></span>

### <span data-ttu-id="6b717-118">- ActionGroup</span><span class="sxs-lookup"><span data-stu-id="6b717-118">-ActionGroup</span></span>
<span data-ttu-id="6b717-119">Grupa akcja</span><span class="sxs-lookup"><span data-stu-id="6b717-119">Action group</span></span>

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

### <span data-ttu-id="6b717-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="6b717-120">-AlertRuleId</span></span>
<span data-ttu-id="6b717-121">Filtruj według identyfikatora reguły alertu</span><span class="sxs-lookup"><span data-stu-id="6b717-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="6b717-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b717-122">-DefaultProfile</span></span>
<span data-ttu-id="6b717-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b717-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b717-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="6b717-124">-Description</span></span>
<span data-ttu-id="6b717-125">Filtrowanie wszystkich alertów z identyfikatorem grupy inteligentnej</span><span class="sxs-lookup"><span data-stu-id="6b717-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="6b717-126">- ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="6b717-126">-ImpactedScope</span></span>
<span data-ttu-id="6b717-127">Filtrowanie według zakresu objętego wpływem</span><span class="sxs-lookup"><span data-stu-id="6b717-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="6b717-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="6b717-128">-MonitorService</span></span>
<span data-ttu-id="6b717-129">Filtr w usłudze Moniter</span><span class="sxs-lookup"><span data-stu-id="6b717-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="6b717-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6b717-130">-Name</span></span>
<span data-ttu-id="6b717-131">Nazwa reguły akcji.</span><span class="sxs-lookup"><span data-stu-id="6b717-131">Name of action rule.</span></span>

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

### <span data-ttu-id="6b717-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b717-132">-ResourceGroupName</span></span>
<span data-ttu-id="6b717-133">Nazwa grupy zasobów, w której znajduje się reguła akcji.</span><span class="sxs-lookup"><span data-stu-id="6b717-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="6b717-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b717-134">-ResourceId</span></span>
<span data-ttu-id="6b717-135">Pobierz regułę akcji według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="6b717-135">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="6b717-136">— Ważność</span><span class="sxs-lookup"><span data-stu-id="6b717-136">-Severity</span></span>
<span data-ttu-id="6b717-137">Filtruj według ważności alertu</span><span class="sxs-lookup"><span data-stu-id="6b717-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="6b717-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b717-138">-TargetResourceGroup</span></span>
<span data-ttu-id="6b717-139">Filtruj według nazwy grupy zasobów docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="6b717-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="6b717-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6b717-140">-TargetResourceId</span></span>
<span data-ttu-id="6b717-141">Filtruj według identyfikatora zasobu docelowego zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="6b717-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="6b717-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="6b717-142">-TargetResourceType</span></span>
<span data-ttu-id="6b717-143">Filtruj według typu zasobu docelowego alertu.</span><span class="sxs-lookup"><span data-stu-id="6b717-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="6b717-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b717-144">CommonParameters</span></span>
<span data-ttu-id="6b717-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b717-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b717-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b717-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b717-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b717-147">INPUTS</span></span>

### <span data-ttu-id="6b717-148">Brak</span><span class="sxs-lookup"><span data-stu-id="6b717-148">None</span></span>

## <span data-ttu-id="6b717-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b717-149">OUTPUTS</span></span>

### <span data-ttu-id="6b717-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="6b717-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="6b717-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6b717-151">NOTES</span></span>

## <span data-ttu-id="6b717-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b717-152">RELATED LINKS</span></span>
