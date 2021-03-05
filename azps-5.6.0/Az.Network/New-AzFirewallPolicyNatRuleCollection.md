---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 4dd93dec5aad6fe0e77e92e44884c687d5841e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960410"
---
# <span data-ttu-id="6a3bf-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="6a3bf-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="6a3bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3bf-103">Tworzenie nowej kolekcji reguł zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6a3bf-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="6a3bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a3bf-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a3bf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a3bf-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3bf-106">Polecenie **cmdlet New-AzFirewallPolicyNatRuleCollection** tworzy kolekcję reguł Nat dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3bf-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="6a3bf-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a3bf-107">EXAMPLES</span></span>

### <span data-ttu-id="6a3bf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6a3bf-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="6a3bf-109">W tym przykładzie jest tworzyna kolekcja reguł nat z regułą sieciową</span><span class="sxs-lookup"><span data-stu-id="6a3bf-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="6a3bf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a3bf-110">PARAMETERS</span></span>

### <span data-ttu-id="6a3bf-111">- ActionType</span><span class="sxs-lookup"><span data-stu-id="6a3bf-111">-ActionType</span></span>
<span data-ttu-id="6a3bf-112">Typ akcji reguły</span><span class="sxs-lookup"><span data-stu-id="6a3bf-112">The type of the rule action</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Dnat

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3bf-113">-DefaultProfile</span></span>
<span data-ttu-id="6a3bf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bf-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6a3bf-115">-Name</span></span>
<span data-ttu-id="6a3bf-116">Nazwa zbioru reguł sieciowych</span><span class="sxs-lookup"><span data-stu-id="6a3bf-116">The name of the Network Rule Collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bf-117">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="6a3bf-117">-Priority</span></span>
<span data-ttu-id="6a3bf-118">Priorytet zbioru reguł</span><span class="sxs-lookup"><span data-stu-id="6a3bf-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bf-119">— reguła</span><span class="sxs-lookup"><span data-stu-id="6a3bf-119">-Rule</span></span>
<span data-ttu-id="6a3bf-120">Lista reguł sieciowych</span><span class="sxs-lookup"><span data-stu-id="6a3bf-120">The list of network rules</span></span>

```yaml
Type: PSAzureFirewallPolicyNetworkRule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bf-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="6a3bf-121">-TranslatedAddress</span></span>
<span data-ttu-id="6a3bf-122">Przetłumaczony adres tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="6a3bf-122">The translated address for this NAT rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bf-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="6a3bf-123">-TranslatedPort</span></span>
<span data-ttu-id="6a3bf-124">Przetłumaczony port tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="6a3bf-124">The translated port for this NAT rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bf-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a3bf-125">-Confirm</span></span>
<span data-ttu-id="6a3bf-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6a3bf-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a3bf-127">-WhatIf</span></span>
<span data-ttu-id="6a3bf-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a3bf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a3bf-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6a3bf-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3bf-130">CommonParameters</span></span>
<span data-ttu-id="6a3bf-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a3bf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3bf-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a3bf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3bf-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a3bf-133">INPUTS</span></span>

### <span data-ttu-id="6a3bf-134">Brak</span><span class="sxs-lookup"><span data-stu-id="6a3bf-134">None</span></span>

## <span data-ttu-id="6a3bf-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a3bf-135">OUTPUTS</span></span>

### <span data-ttu-id="6a3bf-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="6a3bf-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="6a3bf-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a3bf-137">NOTES</span></span>

## <span data-ttu-id="6a3bf-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a3bf-138">RELATED LINKS</span></span>
