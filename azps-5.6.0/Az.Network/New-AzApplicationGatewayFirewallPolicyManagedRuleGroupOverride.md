---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 6b105ab242f9ffb64d1d523cad5930c48714c724
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001162"
---
# <span data-ttu-id="4e513-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4e513-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="4e513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e513-102">SYNOPSIS</span></span>
<span data-ttu-id="4e513-103">Tworzy wpis RuleGroupOverride w zestawach managedRuleSets dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="4e513-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="4e513-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4e513-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e513-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4e513-105">DESCRIPTION</span></span>
<span data-ttu-id="4e513-106">Wpis **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** tworzy wpis ruleGroupOverride w zarządzanym zestawie RuleSet dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="4e513-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="4e513-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4e513-107">EXAMPLES</span></span>

### <span data-ttu-id="4e513-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4e513-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="4e513-109">Tworzy wpis RuleGroupOverride z nazwą grupy jako $ruleName i reguł jako $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="4e513-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="4e513-110">Przypisuje to samo do $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="4e513-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="4e513-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e513-111">PARAMETERS</span></span>

### <span data-ttu-id="4e513-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e513-112">-DefaultProfile</span></span>
<span data-ttu-id="4e513-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e513-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e513-114">— reguła</span><span class="sxs-lookup"><span data-stu-id="4e513-114">-Rule</span></span>
<span data-ttu-id="4e513-115">Lista reguł.</span><span class="sxs-lookup"><span data-stu-id="4e513-115">List of Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e513-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="4e513-116">-RuleGroupName</span></span>
<span data-ttu-id="4e513-117">Określ wartość ruleGroupName w pozycji zastępowania RuleGroup.</span><span class="sxs-lookup"><span data-stu-id="4e513-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="4e513-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e513-118">CommonParameters</span></span>
<span data-ttu-id="4e513-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e513-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e513-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e513-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e513-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e513-121">INPUTS</span></span>

### <span data-ttu-id="4e513-122">Brak</span><span class="sxs-lookup"><span data-stu-id="4e513-122">None</span></span>

## <span data-ttu-id="4e513-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e513-123">OUTPUTS</span></span>

### <span data-ttu-id="4e513-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4e513-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="4e513-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4e513-125">NOTES</span></span>

## <span data-ttu-id="4e513-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e513-126">RELATED LINKS</span></span>
