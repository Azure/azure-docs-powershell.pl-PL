---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179747"
---
# <span data-ttu-id="bf4b9-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="bf4b9-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="bf4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="bf4b9-103">Tworzy wpis RuleGroupOverride w zestawach managedRuleSets dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="bf4b9-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="bf4b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bf4b9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf4b9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bf4b9-105">DESCRIPTION</span></span>
<span data-ttu-id="bf4b9-106">Wpis **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** tworzy wpis ruleGroupOverride w zarządzanym zestawie RuleSet dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="bf4b9-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="bf4b9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bf4b9-107">EXAMPLES</span></span>

### <span data-ttu-id="bf4b9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf4b9-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="bf4b9-109">Tworzy wpis RuleGroupOverride z nazwą grupy jako $ruleName i reguł jako $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="bf4b9-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="bf4b9-110">Przypisuje to samo do $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="bf4b9-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="bf4b9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf4b9-111">PARAMETERS</span></span>

### <span data-ttu-id="bf4b9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf4b9-112">-DefaultProfile</span></span>
<span data-ttu-id="bf4b9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf4b9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf4b9-114">— Reguła</span><span class="sxs-lookup"><span data-stu-id="bf4b9-114">-Rule</span></span>
<span data-ttu-id="bf4b9-115">Lista reguł.</span><span class="sxs-lookup"><span data-stu-id="bf4b9-115">List of Rules.</span></span>

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

### <span data-ttu-id="bf4b9-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="bf4b9-116">-RuleGroupName</span></span>
<span data-ttu-id="bf4b9-117">Określ wartość ruleGroupName w pozycji zastępowania RuleGroup.</span><span class="sxs-lookup"><span data-stu-id="bf4b9-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="bf4b9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf4b9-118">CommonParameters</span></span>
<span data-ttu-id="bf4b9-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf4b9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf4b9-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf4b9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf4b9-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf4b9-121">INPUTS</span></span>

### <span data-ttu-id="bf4b9-122">Brak</span><span class="sxs-lookup"><span data-stu-id="bf4b9-122">None</span></span>

## <span data-ttu-id="bf4b9-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bf4b9-123">OUTPUTS</span></span>

### <span data-ttu-id="bf4b9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="bf4b9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="bf4b9-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bf4b9-125">NOTES</span></span>

## <span data-ttu-id="bf4b9-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf4b9-126">RELATED LINKS</span></span>
