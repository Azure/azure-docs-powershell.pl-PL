---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219489"
---
# <span data-ttu-id="7d94d-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7d94d-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="7d94d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d94d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d94d-103">Utwórz nową regułę sieciową zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="7d94d-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="7d94d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d94d-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d94d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d94d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d94d-106">Polecenie cmdlet **New-AzFirewallPolicyNetworkRule** tworzy regułę sieciową dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7d94d-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="7d94d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d94d-107">EXAMPLES</span></span>

### <span data-ttu-id="7d94d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d94d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="7d94d-109">W tym przykładzie jest tworzona reguła sieci zawierająca adres źródłowy, protokół, adres docelowy i port docelowy.</span><span class="sxs-lookup"><span data-stu-id="7d94d-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="7d94d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d94d-110">PARAMETERS</span></span>

### <span data-ttu-id="7d94d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d94d-111">-DefaultProfile</span></span>
<span data-ttu-id="7d94d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d94d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d94d-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="7d94d-113">-Description</span></span>
<span data-ttu-id="7d94d-114">Opis reguły</span><span class="sxs-lookup"><span data-stu-id="7d94d-114">The description of the rule</span></span>

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

### <span data-ttu-id="7d94d-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7d94d-115">-DestinationAddress</span></span>
<span data-ttu-id="7d94d-116">Adresy docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="7d94d-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="7d94d-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="7d94d-117">-DestinationFqdn</span></span>
<span data-ttu-id="7d94d-118">Docelowa nazwa FQDN reguły</span><span class="sxs-lookup"><span data-stu-id="7d94d-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="7d94d-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="7d94d-119">-DestinationIpGroup</span></span>
<span data-ttu-id="7d94d-120">Ipgroups docelowy reguły</span><span class="sxs-lookup"><span data-stu-id="7d94d-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="7d94d-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7d94d-121">-DestinationPort</span></span>
<span data-ttu-id="7d94d-122">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="7d94d-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="7d94d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d94d-123">-Name</span></span>
<span data-ttu-id="7d94d-124">Nazwa reguły sieci</span><span class="sxs-lookup"><span data-stu-id="7d94d-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="7d94d-125">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="7d94d-125">-Protocol</span></span>
<span data-ttu-id="7d94d-126">Protokoły reguły</span><span class="sxs-lookup"><span data-stu-id="7d94d-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="7d94d-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="7d94d-127">-SourceAddress</span></span>
<span data-ttu-id="7d94d-128">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="7d94d-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="7d94d-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="7d94d-129">-SourceIpGroup</span></span>
<span data-ttu-id="7d94d-130">Ipgroups źródłowa reguły</span><span class="sxs-lookup"><span data-stu-id="7d94d-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="7d94d-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d94d-131">-Confirm</span></span>
<span data-ttu-id="7d94d-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d94d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d94d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d94d-133">-WhatIf</span></span>
<span data-ttu-id="7d94d-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d94d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d94d-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d94d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d94d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d94d-136">CommonParameters</span></span>
<span data-ttu-id="7d94d-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d94d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d94d-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d94d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d94d-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d94d-139">INPUTS</span></span>

### <span data-ttu-id="7d94d-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7d94d-140">None</span></span>

## <span data-ttu-id="7d94d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d94d-141">OUTPUTS</span></span>

### <span data-ttu-id="7d94d-142">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7d94d-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="7d94d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d94d-143">NOTES</span></span>

## <span data-ttu-id="7d94d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d94d-144">RELATED LINKS</span></span>
