---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: 31c12fd53c8aa6c886ab5e26a8c35996045335e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992643"
---
# <span data-ttu-id="ddaad-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="ddaad-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="ddaad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddaad-102">SYNOPSIS</span></span>
<span data-ttu-id="ddaad-103">Tworzy wpis managedRuleOverride dla wpisu RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="ddaad-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="ddaad-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ddaad-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddaad-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ddaad-105">DESCRIPTION</span></span>
<span data-ttu-id="ddaad-106">Wpis **"New-AzApplicationGatewayFirewallPolicyManagedRuleOverride" (Nowa-AzApplicationGatewayFirewallPolicyManagedRuleOverride)** tworzy wpis ruleOverride.</span><span class="sxs-lookup"><span data-stu-id="ddaad-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="ddaad-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ddaad-107">EXAMPLES</span></span>

### <span data-ttu-id="ddaad-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ddaad-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="ddaad-109">Tworzy wpis ruleOverride z regułą RuleId jako $ruleId stan jako wyłączony.</span><span class="sxs-lookup"><span data-stu-id="ddaad-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="ddaad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddaad-110">PARAMETERS</span></span>

### <span data-ttu-id="ddaad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddaad-111">-DefaultProfile</span></span>
<span data-ttu-id="ddaad-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ddaad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddaad-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="ddaad-113">-RuleId</span></span>
<span data-ttu-id="ddaad-114">Określanie reguły RuleId we wpisie reguły zastępowania.</span><span class="sxs-lookup"><span data-stu-id="ddaad-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="ddaad-115">— województwo</span><span class="sxs-lookup"><span data-stu-id="ddaad-115">-State</span></span>
<span data-ttu-id="ddaad-116">Określanie reguły RuleId we wpisie reguły zastępowania.</span><span class="sxs-lookup"><span data-stu-id="ddaad-116">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled

Required: False
Position: Named
Default value: Disabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddaad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddaad-117">CommonParameters</span></span>
<span data-ttu-id="ddaad-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddaad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddaad-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddaad-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddaad-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddaad-120">INPUTS</span></span>

### <span data-ttu-id="ddaad-121">Brak</span><span class="sxs-lookup"><span data-stu-id="ddaad-121">None</span></span>

## <span data-ttu-id="ddaad-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddaad-122">OUTPUTS</span></span>

### <span data-ttu-id="ddaad-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="ddaad-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="ddaad-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ddaad-124">NOTES</span></span>

## <span data-ttu-id="ddaad-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddaad-125">RELATED LINKS</span></span>
