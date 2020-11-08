---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234153"
---
# <span data-ttu-id="3cdc4-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="3cdc4-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="3cdc4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cdc4-102">SYNOPSIS</span></span>
<span data-ttu-id="3cdc4-103">Tworzy ManagedRuleSet dla firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3cdc4-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="3cdc4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cdc4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cdc4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3cdc4-105">DESCRIPTION</span></span>
<span data-ttu-id="3cdc4-106">**Nowy-AzApplicationGatewayFirewallPolicyManagedRuleSet** tworzy reguły zarządzane dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="3cdc4-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="3cdc4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cdc4-107">EXAMPLES</span></span>

### <span data-ttu-id="3cdc4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3cdc4-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="3cdc4-109">Tworzy ManagedRuleSet z zestawem reguł jako $ruleSetType, ruleSetVersion jako $ruleSetVersion i RuleGroupOverrides jako listę ze wszystkimi jako $ruleGroupOverride 1, $ruleGroupOverride 2, do którego jest przypisana nowa ManagedRuleSet $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="3cdc4-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="3cdc4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cdc4-110">PARAMETERS</span></span>

### <span data-ttu-id="3cdc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cdc4-111">-DefaultProfile</span></span>
<span data-ttu-id="3cdc4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cdc4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cdc4-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="3cdc4-113">-RuleGroupOverride</span></span>
<span data-ttu-id="3cdc4-114">Zastąpienia grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="3cdc4-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="3cdc4-115">-Zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="3cdc4-115">-RuleSetType</span></span>
<span data-ttu-id="3cdc4-116">Określanie typu reguł w managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="3cdc4-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="3cdc4-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="3cdc4-117">-RuleSetVersion</span></span>
<span data-ttu-id="3cdc4-118">Określanie RuleSetVersion w managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="3cdc4-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="3cdc4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cdc4-119">CommonParameters</span></span>
<span data-ttu-id="3cdc4-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cdc4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cdc4-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cdc4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cdc4-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cdc4-122">INPUTS</span></span>

### <span data-ttu-id="3cdc4-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3cdc4-123">None</span></span>

## <span data-ttu-id="3cdc4-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cdc4-124">OUTPUTS</span></span>

### <span data-ttu-id="3cdc4-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="3cdc4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="3cdc4-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cdc4-126">NOTES</span></span>

## <span data-ttu-id="3cdc4-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cdc4-127">RELATED LINKS</span></span>
