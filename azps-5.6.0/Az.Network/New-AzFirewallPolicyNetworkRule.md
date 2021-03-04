---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 86e15e54a0091839bdce6a66f891c12e6c0376f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007738"
---
# <span data-ttu-id="5bea8-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5bea8-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="5bea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bea8-102">SYNOPSIS</span></span>
<span data-ttu-id="5bea8-103">Tworzenie nowej reguły sieciowej zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5bea8-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="5bea8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5bea8-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bea8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5bea8-105">DESCRIPTION</span></span>
<span data-ttu-id="5bea8-106">Polecenie **cmdlet New-AzFirewallPolicyNetworkRule** tworzy regułę sieciową dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bea8-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="5bea8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5bea8-107">EXAMPLES</span></span>

### <span data-ttu-id="5bea8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5bea8-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="5bea8-109">W tym przykładzie jest tworzyna reguła sieciowa z adresem źródłowym, protokołem, adresem docelowym i portem docelowym.</span><span class="sxs-lookup"><span data-stu-id="5bea8-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="5bea8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bea8-110">PARAMETERS</span></span>

### <span data-ttu-id="5bea8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bea8-111">-DefaultProfile</span></span>
<span data-ttu-id="5bea8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bea8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bea8-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="5bea8-113">-Description</span></span>
<span data-ttu-id="5bea8-114">Opis reguły</span><span class="sxs-lookup"><span data-stu-id="5bea8-114">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="5bea8-115">-DestinationAddress</span></span>
<span data-ttu-id="5bea8-116">Adresy docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="5bea8-116">The destination addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="5bea8-117">-DestinationFqdn</span></span>
<span data-ttu-id="5bea8-118">Docelowa fqdn reguły</span><span class="sxs-lookup"><span data-stu-id="5bea8-118">The destination FQDN of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="5bea8-119">-DestinationIpGroup</span></span>
<span data-ttu-id="5bea8-120">Docelowe grupy ip grupy reguły</span><span class="sxs-lookup"><span data-stu-id="5bea8-120">The destination ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="5bea8-121">-DestinationPort</span></span>
<span data-ttu-id="5bea8-122">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="5bea8-122">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5bea8-123">-Name</span></span>
<span data-ttu-id="5bea8-124">Nazwa reguły sieciowej</span><span class="sxs-lookup"><span data-stu-id="5bea8-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="5bea8-125">— Protokół</span><span class="sxs-lookup"><span data-stu-id="5bea8-125">-Protocol</span></span>
<span data-ttu-id="5bea8-126">Protokoły reguły</span><span class="sxs-lookup"><span data-stu-id="5bea8-126">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="5bea8-127">-SourceAddress</span></span>
<span data-ttu-id="5bea8-128">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="5bea8-128">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="5bea8-129">-SourceIpGroup</span></span>
<span data-ttu-id="5bea8-130">Źródłowe grupy ipgroup reguły</span><span class="sxs-lookup"><span data-stu-id="5bea8-130">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bea8-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5bea8-131">-Confirm</span></span>
<span data-ttu-id="5bea8-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5bea8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bea8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bea8-133">-WhatIf</span></span>
<span data-ttu-id="5bea8-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bea8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bea8-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5bea8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bea8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bea8-136">CommonParameters</span></span>
<span data-ttu-id="5bea8-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bea8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bea8-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bea8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bea8-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bea8-139">INPUTS</span></span>

### <span data-ttu-id="5bea8-140">Brak</span><span class="sxs-lookup"><span data-stu-id="5bea8-140">None</span></span>

## <span data-ttu-id="5bea8-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bea8-141">OUTPUTS</span></span>

### <span data-ttu-id="5bea8-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5bea8-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="5bea8-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5bea8-143">NOTES</span></span>

## <span data-ttu-id="5bea8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bea8-144">RELATED LINKS</span></span>
