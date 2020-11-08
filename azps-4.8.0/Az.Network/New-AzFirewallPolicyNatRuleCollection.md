---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220544"
---
# <span data-ttu-id="3d4df-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3d4df-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="3d4df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d4df-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4df-103">Tworzenie nowej kolekcji reguł NAT dla zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3d4df-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="3d4df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d4df-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d4df-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d4df-105">DESCRIPTION</span></span>
<span data-ttu-id="3d4df-106">Polecenie cmdlet **New-AzFirewallPolicyNatRuleCollection** tworzy kolekcję reguł NAT dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4df-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="3d4df-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d4df-107">EXAMPLES</span></span>

### <span data-ttu-id="3d4df-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3d4df-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="3d4df-109">W tym przykładzie przedstawiono tworzenie kolekcji reguł NAT przy użyciu reguły sieci</span><span class="sxs-lookup"><span data-stu-id="3d4df-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="3d4df-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d4df-110">PARAMETERS</span></span>

### <span data-ttu-id="3d4df-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="3d4df-111">-ActionType</span></span>
<span data-ttu-id="3d4df-112">Typ akcji reguły</span><span class="sxs-lookup"><span data-stu-id="3d4df-112">The type of the rule action</span></span>

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

### <span data-ttu-id="3d4df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4df-113">-DefaultProfile</span></span>
<span data-ttu-id="3d4df-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d4df-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d4df-115">-Name</span></span>
<span data-ttu-id="3d4df-116">Nazwa kolekcji reguł sieci</span><span class="sxs-lookup"><span data-stu-id="3d4df-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="3d4df-117">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="3d4df-117">-Priority</span></span>
<span data-ttu-id="3d4df-118">Priorytet kolekcji reguł</span><span class="sxs-lookup"><span data-stu-id="3d4df-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="3d4df-119">— Reguła</span><span class="sxs-lookup"><span data-stu-id="3d4df-119">-Rule</span></span>
<span data-ttu-id="3d4df-120">Lista reguł sieciowych</span><span class="sxs-lookup"><span data-stu-id="3d4df-120">The list of network rules</span></span>

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

### <span data-ttu-id="3d4df-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="3d4df-121">-TranslatedAddress</span></span>
<span data-ttu-id="3d4df-122">Adres przetłumaczony tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="3d4df-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="3d4df-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="3d4df-123">-TranslatedPort</span></span>
<span data-ttu-id="3d4df-124">Przetłumaczony port dla tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="3d4df-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="3d4df-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d4df-125">-Confirm</span></span>
<span data-ttu-id="3d4df-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d4df-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d4df-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d4df-127">-WhatIf</span></span>
<span data-ttu-id="3d4df-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d4df-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d4df-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d4df-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d4df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4df-130">CommonParameters</span></span>
<span data-ttu-id="3d4df-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d4df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4df-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d4df-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4df-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d4df-133">INPUTS</span></span>

### <span data-ttu-id="3d4df-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3d4df-134">None</span></span>

## <span data-ttu-id="3d4df-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d4df-135">OUTPUTS</span></span>

### <span data-ttu-id="3d4df-136">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3d4df-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="3d4df-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d4df-137">NOTES</span></span>

## <span data-ttu-id="3d4df-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d4df-138">RELATED LINKS</span></span>
