---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: b4cbc404139cd56e75f03c5cb19cb9b761576e39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050783"
---
# <span data-ttu-id="ec2f7-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ec2f7-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="ec2f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec2f7-103">Utwórz nową regułę sieciową zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ec2f7-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="ec2f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec2f7-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec2f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec2f7-105">DESCRIPTION</span></span>
<span data-ttu-id="ec2f7-106">Polecenie cmdlet **New-AzFirewallPolicyNetworkRule** tworzy regułę sieciową dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ec2f7-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="ec2f7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec2f7-107">EXAMPLES</span></span>

### <span data-ttu-id="ec2f7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec2f7-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="ec2f7-109">W tym przykładzie jest tworzona reguła sieci zawierająca adres źródłowy, protokół, adres docelowy i port docelowy.</span><span class="sxs-lookup"><span data-stu-id="ec2f7-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="ec2f7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec2f7-110">PARAMETERS</span></span>

### <span data-ttu-id="ec2f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec2f7-111">-DefaultProfile</span></span>
<span data-ttu-id="ec2f7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec2f7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec2f7-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="ec2f7-113">-Description</span></span>
<span data-ttu-id="ec2f7-114">Opis reguły</span><span class="sxs-lookup"><span data-stu-id="ec2f7-114">The description of the rule</span></span>

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

### <span data-ttu-id="ec2f7-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ec2f7-115">-DestinationAddress</span></span>
<span data-ttu-id="ec2f7-116">Adresy docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="ec2f7-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="ec2f7-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ec2f7-117">-DestinationPort</span></span>
<span data-ttu-id="ec2f7-118">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="ec2f7-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="ec2f7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec2f7-119">-Name</span></span>
<span data-ttu-id="ec2f7-120">Nazwa reguły sieci</span><span class="sxs-lookup"><span data-stu-id="ec2f7-120">The name of the Network Rule</span></span>

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

### <span data-ttu-id="ec2f7-121">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="ec2f7-121">-Protocols</span></span>
<span data-ttu-id="ec2f7-122">Protokoły reguły</span><span class="sxs-lookup"><span data-stu-id="ec2f7-122">The protocols of the rule</span></span>

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

### <span data-ttu-id="ec2f7-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="ec2f7-123">-SourceAddress</span></span>
<span data-ttu-id="ec2f7-124">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="ec2f7-124">The source addresses of the rule</span></span>

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

### <span data-ttu-id="ec2f7-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec2f7-125">-Confirm</span></span>
<span data-ttu-id="ec2f7-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec2f7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec2f7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec2f7-127">-WhatIf</span></span>
<span data-ttu-id="ec2f7-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec2f7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec2f7-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ec2f7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec2f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec2f7-130">CommonParameters</span></span>
<span data-ttu-id="ec2f7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec2f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec2f7-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec2f7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec2f7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec2f7-133">INPUTS</span></span>

### <span data-ttu-id="ec2f7-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ec2f7-134">None</span></span>

## <span data-ttu-id="ec2f7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec2f7-135">OUTPUTS</span></span>

### <span data-ttu-id="ec2f7-136">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ec2f7-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="ec2f7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec2f7-137">NOTES</span></span>

## <span data-ttu-id="ec2f7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec2f7-138">RELATED LINKS</span></span>
