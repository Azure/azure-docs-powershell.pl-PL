---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053781"
---
# <span data-ttu-id="18a2e-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="18a2e-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="18a2e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="18a2e-103">Tworzy wpis RuleGroupOverride w ManagedRuleSets dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="18a2e-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="18a2e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18a2e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18a2e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18a2e-105">DESCRIPTION</span></span>
<span data-ttu-id="18a2e-106">**Nowy-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** tworzy wpis RuleGroupOverride w managedRuleSet dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="18a2e-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="18a2e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18a2e-107">EXAMPLES</span></span>

### <span data-ttu-id="18a2e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="18a2e-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="18a2e-109">Tworzy wpis RuleGroupOverride z nazwą grupy jako $ruleName i regułami $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="18a2e-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="18a2e-110">Przypisuje te same $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="18a2e-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="18a2e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18a2e-111">PARAMETERS</span></span>

### <span data-ttu-id="18a2e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a2e-112">-DefaultProfile</span></span>
<span data-ttu-id="18a2e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18a2e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a2e-114">— Reguła</span><span class="sxs-lookup"><span data-stu-id="18a2e-114">-Rule</span></span>
<span data-ttu-id="18a2e-115">Lista reguł.</span><span class="sxs-lookup"><span data-stu-id="18a2e-115">List of Rules.</span></span>

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

### <span data-ttu-id="18a2e-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="18a2e-116">-RuleGroupName</span></span>
<span data-ttu-id="18a2e-117">Określ ruleGroupName w pozycji zastąpienia reguły.</span><span class="sxs-lookup"><span data-stu-id="18a2e-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="18a2e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a2e-118">CommonParameters</span></span>
<span data-ttu-id="18a2e-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a2e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a2e-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18a2e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a2e-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18a2e-121">INPUTS</span></span>

### <span data-ttu-id="18a2e-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="18a2e-122">None</span></span>

## <span data-ttu-id="18a2e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18a2e-123">OUTPUTS</span></span>

### <span data-ttu-id="18a2e-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="18a2e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="18a2e-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18a2e-125">NOTES</span></span>

## <span data-ttu-id="18a2e-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18a2e-126">RELATED LINKS</span></span>
