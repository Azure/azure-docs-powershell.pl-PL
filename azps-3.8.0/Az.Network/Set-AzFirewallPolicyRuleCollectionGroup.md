---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8e1260a636a1be5a42888fcc6cc12cb8b228859c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051475"
---
# <span data-ttu-id="57f15-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="57f15-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="57f15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57f15-102">SYNOPSIS</span></span>
<span data-ttu-id="57f15-103">zapisuje zmodyfikowaną grupę kolekcji reguł zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57f15-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="57f15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57f15-104">SYNTAX</span></span>

### <span data-ttu-id="57f15-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="57f15-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57f15-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57f15-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57f15-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57f15-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57f15-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57f15-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57f15-109">Opis</span><span class="sxs-lookup"><span data-stu-id="57f15-109">DESCRIPTION</span></span>
<span data-ttu-id="57f15-110">Polecenie cmdlet **Set-AzFirewallPolicyRuleCollectionGroup** aktualizuje grupy kolekcji reguł w zasadach zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="57f15-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="57f15-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57f15-111">EXAMPLES</span></span>

### <span data-ttu-id="57f15-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57f15-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="57f15-113">W tym przykładzie jest aktualizowana Grupa kolekcji reguł w $fp zasad zapory</span><span class="sxs-lookup"><span data-stu-id="57f15-113">This example updates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="57f15-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57f15-114">PARAMETERS</span></span>

### <span data-ttu-id="57f15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f15-115">-DefaultProfile</span></span>
<span data-ttu-id="57f15-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57f15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f15-117">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="57f15-117">-FirewallPolicyName</span></span>
<span data-ttu-id="57f15-118">Nazwa zasad zapory</span><span class="sxs-lookup"><span data-stu-id="57f15-118">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f15-119">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="57f15-119">-FirewallPolicyObject</span></span>
<span data-ttu-id="57f15-120">Zasady zapory.</span><span class="sxs-lookup"><span data-stu-id="57f15-120">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f15-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="57f15-121">-InputObject</span></span>
<span data-ttu-id="57f15-122">Lista reguł</span><span class="sxs-lookup"><span data-stu-id="57f15-122">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f15-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57f15-123">-Name</span></span>
<span data-ttu-id="57f15-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="57f15-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f15-125">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="57f15-125">-Priority</span></span>
<span data-ttu-id="57f15-126">Priorytet grupy reguł</span><span class="sxs-lookup"><span data-stu-id="57f15-126">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f15-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f15-127">-ResourceGroupName</span></span>
<span data-ttu-id="57f15-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57f15-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f15-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57f15-129">-ResourceId</span></span>
<span data-ttu-id="57f15-130">Identyfikator zasobu grupy kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="57f15-130">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f15-131">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="57f15-131">-RuleCollection</span></span>
<span data-ttu-id="57f15-132">Lista kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="57f15-132">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f15-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57f15-133">-Confirm</span></span>
<span data-ttu-id="57f15-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57f15-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f15-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f15-135">-WhatIf</span></span>
<span data-ttu-id="57f15-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57f15-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f15-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57f15-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f15-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f15-138">CommonParameters</span></span>
<span data-ttu-id="57f15-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f15-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f15-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57f15-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f15-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57f15-141">INPUTS</span></span>

### <span data-ttu-id="57f15-142">System. String</span><span class="sxs-lookup"><span data-stu-id="57f15-142">System.String</span></span>

### <span data-ttu-id="57f15-143">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="57f15-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="57f15-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57f15-144">OUTPUTS</span></span>

### <span data-ttu-id="57f15-145">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="57f15-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="57f15-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57f15-146">NOTES</span></span>

## <span data-ttu-id="57f15-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57f15-147">RELATED LINKS</span></span>
