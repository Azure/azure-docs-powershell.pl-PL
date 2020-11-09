---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317958"
---
# <span data-ttu-id="e64cb-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="e64cb-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="e64cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e64cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e64cb-103">Tworzenie nowej reguły NAT zasad usługi Zapora Azure</span><span class="sxs-lookup"><span data-stu-id="e64cb-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="e64cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e64cb-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e64cb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e64cb-105">DESCRIPTION</span></span>
<span data-ttu-id="e64cb-106">Polecenie cmdlet **New-AzFirewallPolicyNatRule** tworzy regułę NAT dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e64cb-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="e64cb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e64cb-107">EXAMPLES</span></span>

### <span data-ttu-id="e64cb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e64cb-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="e64cb-109">W tym przykładzie przedstawiono tworzenie reguły NAT z adresem źródłowym, protokołem, adresem docelowym, portem docelowym, adresem przetłumaczonym i przetłumaczonym portem.</span><span class="sxs-lookup"><span data-stu-id="e64cb-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="e64cb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e64cb-110">PARAMETERS</span></span>

### <span data-ttu-id="e64cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e64cb-111">-DefaultProfile</span></span>
<span data-ttu-id="e64cb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e64cb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e64cb-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e64cb-113">-Name</span></span>
<span data-ttu-id="e64cb-114">Nazwa kolekcji reguł NAT</span><span class="sxs-lookup"><span data-stu-id="e64cb-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="e64cb-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="e64cb-115">-Description</span></span>
<span data-ttu-id="e64cb-116">Opis reguły</span><span class="sxs-lookup"><span data-stu-id="e64cb-116">The description of the rule</span></span>

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

### <span data-ttu-id="e64cb-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e64cb-117">-DestinationAddress</span></span>
<span data-ttu-id="e64cb-118">Adresy docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="e64cb-118">The destination addresses of the rule.</span></span> <span data-ttu-id="e64cb-119">Ten adres musi być publicznym adresem IP zapory.</span><span class="sxs-lookup"><span data-stu-id="e64cb-119">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="e64cb-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e64cb-120">-DestinationPort</span></span>
<span data-ttu-id="e64cb-121">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="e64cb-121">The destination ports of the rule</span></span>

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

### <span data-ttu-id="e64cb-122">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="e64cb-122">-Protocols</span></span>
<span data-ttu-id="e64cb-123">Protokoły reguły</span><span class="sxs-lookup"><span data-stu-id="e64cb-123">The protocols of the rule</span></span>

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

### <span data-ttu-id="e64cb-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e64cb-124">-SourceAddress</span></span>
<span data-ttu-id="e64cb-125">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="e64cb-125">The source addresses of the rule</span></span>

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

### <span data-ttu-id="e64cb-126">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="e64cb-126">-SourceIpGroup</span></span>
<span data-ttu-id="e64cb-127">Ipgroups źródłowa reguły</span><span class="sxs-lookup"><span data-stu-id="e64cb-127">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="e64cb-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="e64cb-128">-TranslatedAddress</span></span>
<span data-ttu-id="e64cb-129">Adres przetłumaczony tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="e64cb-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="e64cb-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="e64cb-130">-TranslatedPort</span></span>
<span data-ttu-id="e64cb-131">Przetłumaczony port dla tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="e64cb-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="e64cb-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e64cb-132">-Confirm</span></span>
<span data-ttu-id="e64cb-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e64cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e64cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e64cb-134">-WhatIf</span></span>
<span data-ttu-id="e64cb-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e64cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e64cb-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e64cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e64cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e64cb-137">CommonParameters</span></span>
<span data-ttu-id="e64cb-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e64cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e64cb-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e64cb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e64cb-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e64cb-140">INPUTS</span></span>

### <span data-ttu-id="e64cb-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e64cb-141">None</span></span>

## <span data-ttu-id="e64cb-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e64cb-142">OUTPUTS</span></span>

### <span data-ttu-id="e64cb-143">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="e64cb-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="e64cb-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e64cb-144">NOTES</span></span>

## <span data-ttu-id="e64cb-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e64cb-145">RELATED LINKS</span></span>
