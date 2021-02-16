---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179771"
---
# <span data-ttu-id="a4cdf-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="a4cdf-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="a4cdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cdf-103">Utwórz usługi ManagedRules dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="a4cdf-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="a4cdf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4cdf-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4cdf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4cdf-105">DESCRIPTION</span></span>
<span data-ttu-id="a4cdf-106">Reguła **New-AzApplicationGatewayFirewallPolicyManagedRule** tworzy reguły zarządzane dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="a4cdf-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="a4cdf-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4cdf-107">EXAMPLES</span></span>

### <span data-ttu-id="a4cdf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4cdf-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="a4cdf-109">Polecenie tworzy reguły zarządzane, listę zestawu ManagedRuleSet z $managedRuleSet i listę wykluczeń z wpisami jako $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="a4cdf-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="a4cdf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4cdf-110">PARAMETERS</span></span>

### <span data-ttu-id="a4cdf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4cdf-111">-DefaultProfile</span></span>
<span data-ttu-id="a4cdf-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4cdf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4cdf-113">— Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="a4cdf-113">-Exclusion</span></span>
<span data-ttu-id="a4cdf-114">Lista pozycji wykluczeń.</span><span class="sxs-lookup"><span data-stu-id="a4cdf-114">List of Exclusion Entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cdf-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4cdf-115">-ManagedRuleSet</span></span>
<span data-ttu-id="a4cdf-116">Lista zarządzanych zestawów reguł.</span><span class="sxs-lookup"><span data-stu-id="a4cdf-116">List of Managed ruleSets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cdf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cdf-117">CommonParameters</span></span>
<span data-ttu-id="a4cdf-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4cdf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cdf-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4cdf-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cdf-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4cdf-120">INPUTS</span></span>

### <span data-ttu-id="a4cdf-121">Brak</span><span class="sxs-lookup"><span data-stu-id="a4cdf-121">None</span></span>

## <span data-ttu-id="a4cdf-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4cdf-122">OUTPUTS</span></span>

### <span data-ttu-id="a4cdf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="a4cdf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="a4cdf-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4cdf-124">NOTES</span></span>

## <span data-ttu-id="a4cdf-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4cdf-125">RELATED LINKS</span></span>
