---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500397"
---
# <span data-ttu-id="6082c-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6082c-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="6082c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6082c-102">SYNOPSIS</span></span>
<span data-ttu-id="6082c-103">Tworzy regułę sieciową zapory.</span><span class="sxs-lookup"><span data-stu-id="6082c-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="6082c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6082c-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6082c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6082c-105">DESCRIPTION</span></span>
<span data-ttu-id="6082c-106">Polecenie cmdlet **New-AzFirewallNetworkRule** tworzy regułę sieciową dla zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6082c-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="6082c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6082c-107">EXAMPLES</span></span>

### <span data-ttu-id="6082c-108">Przykład 1. Tworzenie reguły dla całego ruchu TCP</span><span class="sxs-lookup"><span data-stu-id="6082c-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="6082c-109">W tym przykładzie tworzona jest reguła dla całego ruchu TCP.</span><span class="sxs-lookup"><span data-stu-id="6082c-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="6082c-110">Użytkownik wymusza, czy ruch będzie dozwolony lub odmówiony dla reguły na podstawie kolekcji reguł, z którą jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="6082c-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="6082c-111">Przykład 2: Tworzenie reguły dla całego ruchu TCP od 10.0.0.0 do 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="6082c-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="6082c-112">W tym przykładzie tworzona jest reguła dla całego ruchu TCP z 10.0.0.0 na 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="6082c-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="6082c-113">Użytkownik wymusza, czy ruch będzie dozwolony lub odmówiony dla reguły na podstawie kolekcji reguł, z którą jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="6082c-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="6082c-114">Przykład 3: Tworzenie reguły dla całego ruchu TCP i ICMP z dowolnego źródła do 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="6082c-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="6082c-115">W tym przykładzie tworzona jest reguła dla całego ruchu TCP z dowolnego źródła do 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="6082c-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="6082c-116">Użytkownik wymusza, czy ruch będzie dozwolony lub odmówiony dla reguły na podstawie kolekcji reguł, z którą jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="6082c-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="6082c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6082c-117">PARAMETERS</span></span>

### <span data-ttu-id="6082c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6082c-118">-DefaultProfile</span></span>
<span data-ttu-id="6082c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6082c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6082c-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="6082c-120">-Description</span></span>
<span data-ttu-id="6082c-121">Umożliwia określenie opcjonalnego opisu tej reguły.</span><span class="sxs-lookup"><span data-stu-id="6082c-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6082c-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6082c-122">-DestinationAddress</span></span>
<span data-ttu-id="6082c-123">Adresy docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="6082c-123">The destination addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6082c-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="6082c-124">-DestinationFqdn</span></span>
<span data-ttu-id="6082c-125">Docelowa nazwa FQDN reguły</span><span class="sxs-lookup"><span data-stu-id="6082c-125">The destination FQDN of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6082c-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="6082c-126">-DestinationIpGroup</span></span>
<span data-ttu-id="6082c-127">Ipgroup docelowy reguły</span><span class="sxs-lookup"><span data-stu-id="6082c-127">The destination ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6082c-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6082c-128">-DestinationPort</span></span>
<span data-ttu-id="6082c-129">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="6082c-129">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6082c-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6082c-130">-Name</span></span>
<span data-ttu-id="6082c-131">Określa nazwę reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="6082c-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="6082c-132">Nazwa musi być unikatowa w kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="6082c-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="6082c-133">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="6082c-133">-Protocol</span></span>
<span data-ttu-id="6082c-134">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="6082c-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="6082c-135">Możliwe wartości to protokoły TCP, UDP, ICMP i any.</span><span class="sxs-lookup"><span data-stu-id="6082c-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6082c-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="6082c-136">-SourceAddress</span></span>
<span data-ttu-id="6082c-137">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="6082c-137">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6082c-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="6082c-138">-SourceIpGroup</span></span>
<span data-ttu-id="6082c-139">Ipgroup źródłowa reguły</span><span class="sxs-lookup"><span data-stu-id="6082c-139">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6082c-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6082c-140">-Confirm</span></span>
<span data-ttu-id="6082c-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6082c-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6082c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6082c-142">-WhatIf</span></span>
<span data-ttu-id="6082c-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6082c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6082c-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6082c-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6082c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6082c-145">CommonParameters</span></span>
<span data-ttu-id="6082c-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6082c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6082c-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6082c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6082c-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6082c-148">INPUTS</span></span>

### <span data-ttu-id="6082c-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6082c-149">None</span></span>

## <span data-ttu-id="6082c-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6082c-150">OUTPUTS</span></span>

### <span data-ttu-id="6082c-151">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6082c-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="6082c-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6082c-152">NOTES</span></span>

## <span data-ttu-id="6082c-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6082c-153">RELATED LINKS</span></span>

[<span data-ttu-id="6082c-154">Nowe — AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="6082c-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="6082c-155">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6082c-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="6082c-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6082c-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
