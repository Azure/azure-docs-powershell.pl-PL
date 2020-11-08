---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063950"
---
# <span data-ttu-id="996f6-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="996f6-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="996f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="996f6-102">SYNOPSIS</span></span>
<span data-ttu-id="996f6-103">Tworzy wpis managedRuleOverride dla wpisu RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="996f6-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="996f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="996f6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="996f6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="996f6-105">DESCRIPTION</span></span>
<span data-ttu-id="996f6-106">**Nowy — AzApplicationGatewayFirewallPolicyManagedRuleOverride** tworzy wpis ruleOverride.</span><span class="sxs-lookup"><span data-stu-id="996f6-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="996f6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="996f6-107">EXAMPLES</span></span>

### <span data-ttu-id="996f6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="996f6-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="996f6-109">Tworzy wpis ruleOverride z RuleId jako $ruleId i stan jako wyłączony.</span><span class="sxs-lookup"><span data-stu-id="996f6-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="996f6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="996f6-110">PARAMETERS</span></span>

### <span data-ttu-id="996f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996f6-111">-DefaultProfile</span></span>
<span data-ttu-id="996f6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="996f6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="996f6-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="996f6-113">-RuleId</span></span>
<span data-ttu-id="996f6-114">Określ RuleId w polu reguła zastąpienia.</span><span class="sxs-lookup"><span data-stu-id="996f6-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="996f6-115">-State</span><span class="sxs-lookup"><span data-stu-id="996f6-115">-State</span></span>
<span data-ttu-id="996f6-116">Określ RuleId w polu reguła zastąpienia.</span><span class="sxs-lookup"><span data-stu-id="996f6-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="996f6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996f6-117">CommonParameters</span></span>
<span data-ttu-id="996f6-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="996f6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996f6-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="996f6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996f6-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="996f6-120">INPUTS</span></span>

### <span data-ttu-id="996f6-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="996f6-121">None</span></span>

## <span data-ttu-id="996f6-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="996f6-122">OUTPUTS</span></span>

### <span data-ttu-id="996f6-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="996f6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="996f6-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="996f6-124">NOTES</span></span>

## <span data-ttu-id="996f6-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="996f6-125">RELATED LINKS</span></span>
