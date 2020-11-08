---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050778"
---
# <span data-ttu-id="cb9b9-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="cb9b9-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="cb9b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9b9-103">Tworzenie nowej grupy kolekcji reguł zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cb9b9-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="cb9b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb9b9-104">SYNTAX</span></span>

### <span data-ttu-id="cb9b9-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb9b9-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb9b9-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb9b9-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb9b9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cb9b9-107">DESCRIPTION</span></span>
<span data-ttu-id="cb9b9-108">Polecenie cmdlet **New-AzFirewallPolicyRuleCollectionGroup** tworzy grupę kolekcji reguł w zasadach zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9b9-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="cb9b9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb9b9-109">EXAMPLES</span></span>

### <span data-ttu-id="cb9b9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb9b9-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="cb9b9-111">W tym przykładzie przedstawiono tworzenie grupy kolekcji reguł w $fp zasad zapory</span><span class="sxs-lookup"><span data-stu-id="cb9b9-111">This example creates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="cb9b9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb9b9-112">PARAMETERS</span></span>

### <span data-ttu-id="cb9b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9b9-113">-DefaultProfile</span></span>
<span data-ttu-id="cb9b9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb9b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb9b9-115">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="cb9b9-115">-FirewallPolicyName</span></span>
<span data-ttu-id="cb9b9-116">Nazwa zasad zapory</span><span class="sxs-lookup"><span data-stu-id="cb9b9-116">The name of the firewall policy</span></span>

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

### <span data-ttu-id="cb9b9-117">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="cb9b9-117">-FirewallPolicyObject</span></span>
<span data-ttu-id="cb9b9-118">Zasady zapory.</span><span class="sxs-lookup"><span data-stu-id="cb9b9-118">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9b9-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cb9b9-119">-Name</span></span>
<span data-ttu-id="cb9b9-120">Nazwa grupy reguł</span><span class="sxs-lookup"><span data-stu-id="cb9b9-120">The name of the Rule Group</span></span>

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

### <span data-ttu-id="cb9b9-121">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="cb9b9-121">-Priority</span></span>
<span data-ttu-id="cb9b9-122">Priorytet grupy reguł</span><span class="sxs-lookup"><span data-stu-id="cb9b9-122">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb9b9-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb9b9-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9b9-125">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="cb9b9-125">-RuleCollection</span></span>
<span data-ttu-id="cb9b9-126">Lista reguł</span><span class="sxs-lookup"><span data-stu-id="cb9b9-126">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb9b9-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb9b9-127">-Confirm</span></span>
<span data-ttu-id="cb9b9-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb9b9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb9b9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb9b9-129">-WhatIf</span></span>
<span data-ttu-id="cb9b9-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb9b9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb9b9-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cb9b9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb9b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9b9-132">CommonParameters</span></span>
<span data-ttu-id="cb9b9-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9b9-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb9b9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9b9-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb9b9-135">INPUTS</span></span>

### <span data-ttu-id="cb9b9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cb9b9-136">System.String</span></span>

### <span data-ttu-id="cb9b9-137">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cb9b9-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="cb9b9-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb9b9-138">OUTPUTS</span></span>

### <span data-ttu-id="cb9b9-139">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="cb9b9-139">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="cb9b9-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb9b9-140">NOTES</span></span>

## <span data-ttu-id="cb9b9-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb9b9-141">RELATED LINKS</span></span>
