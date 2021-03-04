---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: d8cb1e6f36433168d830c79c2bcbf8b5c259cf32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962689"
---
# <span data-ttu-id="71a2d-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="71a2d-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="71a2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="71a2d-103">Tworzy zestaw managedRuleSet dla ustawienia firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="71a2d-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="71a2d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71a2d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71a2d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="71a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="71a2d-106">Ustawienie **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** tworzy reguły zarządzane dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="71a2d-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="71a2d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71a2d-107">EXAMPLES</span></span>

### <span data-ttu-id="71a2d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71a2d-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="71a2d-109">Tworzy zestaw managedRuleSet z typem ruleSetType jako $ruleSetType, ruleSetVersion jako $ruleSetVersion i RuleGroupOverrides jako listą z całościami jako $ruleGroupOverride 1, $ruleGroupOverride 2 Nowy zestaw ManagedRuleSet jest przypisany do $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="71a2d-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="71a2d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71a2d-110">PARAMETERS</span></span>

### <span data-ttu-id="71a2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a2d-111">-DefaultProfile</span></span>
<span data-ttu-id="71a2d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="71a2d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71a2d-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="71a2d-113">-RuleGroupOverride</span></span>
<span data-ttu-id="71a2d-114">Zastępowanie grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="71a2d-114">Rule Group Overrides.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a2d-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="71a2d-115">-RuleSetType</span></span>
<span data-ttu-id="71a2d-116">Określanie typu RuleSetType w a managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="71a2d-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="71a2d-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="71a2d-117">-RuleSetVersion</span></span>
<span data-ttu-id="71a2d-118">Określanie ustawienia RuleSetVersion w zarządzanym zestawie reguł</span><span class="sxs-lookup"><span data-stu-id="71a2d-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="71a2d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a2d-119">CommonParameters</span></span>
<span data-ttu-id="71a2d-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71a2d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a2d-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71a2d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a2d-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71a2d-122">INPUTS</span></span>

### <span data-ttu-id="71a2d-123">Brak</span><span class="sxs-lookup"><span data-stu-id="71a2d-123">None</span></span>

## <span data-ttu-id="71a2d-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71a2d-124">OUTPUTS</span></span>

### <span data-ttu-id="71a2d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="71a2d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="71a2d-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71a2d-126">NOTES</span></span>

## <span data-ttu-id="71a2d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71a2d-127">RELATED LINKS</span></span>
