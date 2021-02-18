---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240778"
---
# <span data-ttu-id="ceef9-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ceef9-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="ceef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceef9-102">SYNOPSIS</span></span>
<span data-ttu-id="ceef9-103">Tworzenie nowej reguły sieciowej zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ceef9-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="ceef9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ceef9-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceef9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ceef9-105">DESCRIPTION</span></span>
<span data-ttu-id="ceef9-106">Polecenie **cmdlet New-AzFirewallPolicyNetworkRule** tworzy regułę sieciową dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ceef9-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="ceef9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ceef9-107">EXAMPLES</span></span>

### <span data-ttu-id="ceef9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ceef9-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="ceef9-109">W tym przykładzie jest tworzyna reguła sieciowa z adresem źródłowym, protokołem, adresem docelowym i portem docelowym.</span><span class="sxs-lookup"><span data-stu-id="ceef9-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="ceef9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceef9-110">PARAMETERS</span></span>

### <span data-ttu-id="ceef9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceef9-111">-DefaultProfile</span></span>
<span data-ttu-id="ceef9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ceef9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceef9-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="ceef9-113">-Description</span></span>
<span data-ttu-id="ceef9-114">Opis reguły</span><span class="sxs-lookup"><span data-stu-id="ceef9-114">The description of the rule</span></span>

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

### <span data-ttu-id="ceef9-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ceef9-115">-DestinationAddress</span></span>
<span data-ttu-id="ceef9-116">Adresy docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="ceef9-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="ceef9-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="ceef9-117">-DestinationFqdn</span></span>
<span data-ttu-id="ceef9-118">Docelowa fqdn reguły</span><span class="sxs-lookup"><span data-stu-id="ceef9-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="ceef9-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="ceef9-119">-DestinationIpGroup</span></span>
<span data-ttu-id="ceef9-120">Docelowe grupy ip grupy reguły</span><span class="sxs-lookup"><span data-stu-id="ceef9-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="ceef9-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ceef9-121">-DestinationPort</span></span>
<span data-ttu-id="ceef9-122">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="ceef9-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="ceef9-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ceef9-123">-Name</span></span>
<span data-ttu-id="ceef9-124">Nazwa reguły sieciowej</span><span class="sxs-lookup"><span data-stu-id="ceef9-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="ceef9-125">— Protokół</span><span class="sxs-lookup"><span data-stu-id="ceef9-125">-Protocol</span></span>
<span data-ttu-id="ceef9-126">Protokoły reguły</span><span class="sxs-lookup"><span data-stu-id="ceef9-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="ceef9-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="ceef9-127">-SourceAddress</span></span>
<span data-ttu-id="ceef9-128">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="ceef9-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="ceef9-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="ceef9-129">-SourceIpGroup</span></span>
<span data-ttu-id="ceef9-130">Źródłowe grupy ipgroup reguły</span><span class="sxs-lookup"><span data-stu-id="ceef9-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="ceef9-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ceef9-131">-Confirm</span></span>
<span data-ttu-id="ceef9-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ceef9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceef9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceef9-133">-WhatIf</span></span>
<span data-ttu-id="ceef9-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceef9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceef9-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ceef9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceef9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceef9-136">CommonParameters</span></span>
<span data-ttu-id="ceef9-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceef9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceef9-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ceef9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceef9-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ceef9-139">INPUTS</span></span>

### <span data-ttu-id="ceef9-140">Brak</span><span class="sxs-lookup"><span data-stu-id="ceef9-140">None</span></span>

## <span data-ttu-id="ceef9-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ceef9-141">OUTPUTS</span></span>

### <span data-ttu-id="ceef9-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ceef9-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="ceef9-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ceef9-143">NOTES</span></span>

## <span data-ttu-id="ceef9-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ceef9-144">RELATED LINKS</span></span>
