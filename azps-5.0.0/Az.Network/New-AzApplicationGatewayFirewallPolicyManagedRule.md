---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224223"
---
# <span data-ttu-id="99dee-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="99dee-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="99dee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99dee-102">SYNOPSIS</span></span>
<span data-ttu-id="99dee-103">Utwórz ManagedRules dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="99dee-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="99dee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99dee-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99dee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99dee-105">DESCRIPTION</span></span>
<span data-ttu-id="99dee-106">**Nowy-AzApplicationGatewayFirewallPolicyManagedRule** tworzy reguły zarządzane dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="99dee-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="99dee-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99dee-107">EXAMPLES</span></span>

### <span data-ttu-id="99dee-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99dee-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="99dee-109">Polecenie tworzy reguły zarządzane lista ManagedRuleSet z $managedRuleSet i listą wykluczeń z pozycjami $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="99dee-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="99dee-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99dee-110">PARAMETERS</span></span>

### <span data-ttu-id="99dee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99dee-111">-DefaultProfile</span></span>
<span data-ttu-id="99dee-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99dee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99dee-113">-Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="99dee-113">-Exclusion</span></span>
<span data-ttu-id="99dee-114">Lista pozycji wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="99dee-114">List of Exclusion Entry.</span></span>

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

### <span data-ttu-id="99dee-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="99dee-115">-ManagedRuleSet</span></span>
<span data-ttu-id="99dee-116">Lista zestawów zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="99dee-116">List of Managed ruleSets.</span></span>

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

### <span data-ttu-id="99dee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99dee-117">CommonParameters</span></span>
<span data-ttu-id="99dee-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99dee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99dee-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99dee-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99dee-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99dee-120">INPUTS</span></span>

### <span data-ttu-id="99dee-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="99dee-121">None</span></span>

## <span data-ttu-id="99dee-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99dee-122">OUTPUTS</span></span>

### <span data-ttu-id="99dee-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="99dee-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="99dee-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99dee-124">NOTES</span></span>

## <span data-ttu-id="99dee-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99dee-125">RELATED LINKS</span></span>
