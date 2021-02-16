---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184507"
---
# <span data-ttu-id="c1c93-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c1c93-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="c1c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1c93-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c93-103">Tworzy regułę sieciową zapory.</span><span class="sxs-lookup"><span data-stu-id="c1c93-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="c1c93-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c1c93-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1c93-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c1c93-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c93-106">Polecenie **cmdlet New-AzFirewallNetworkRule** tworzy regułę sieciową dla Zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c1c93-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="c1c93-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c1c93-107">EXAMPLES</span></span>

### <span data-ttu-id="c1c93-108">Przykład 1. Tworzenie reguły dla całego ruchu TCP</span><span class="sxs-lookup"><span data-stu-id="c1c93-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="c1c93-109">W tym przykładzie jest organizacji tworzącej regułę dla całego ruchu TCP.</span><span class="sxs-lookup"><span data-stu-id="c1c93-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="c1c93-110">Użytkownik wymusza, czy ruch dla reguły będzie dozwolony lub odrzucony na podstawie zbioru reguł, z które jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="c1c93-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="c1c93-111">Przykład 2. Tworzenie reguły dla całego ruchu TCP od 10.0.0.0 do 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="c1c93-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="c1c93-112">W tym przykładzie jest utworzenie reguły dla całego ruchu TCP z od 10.0.0.0 do 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="c1c93-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="c1c93-113">Użytkownik wymusza, czy ruch dla reguły będzie dozwolony lub odrzucony na podstawie zbioru reguł, z który jest skojarzony.</span><span class="sxs-lookup"><span data-stu-id="c1c93-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="c1c93-114">Przykład 3. Tworzenie reguły dla całego ruchu TCP i ICMP z dowolnego źródła do 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="c1c93-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="c1c93-115">W tym przykładzie jest organizacji tworzącej regułę dla całego ruchu TCP z dowolnego źródła do 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="c1c93-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="c1c93-116">Użytkownik wymusza, czy ruch dla reguły będzie dozwolony lub odrzucony na podstawie zbioru reguł, z które jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="c1c93-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="c1c93-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1c93-117">PARAMETERS</span></span>

### <span data-ttu-id="c1c93-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c93-118">-DefaultProfile</span></span>
<span data-ttu-id="c1c93-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1c93-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1c93-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="c1c93-120">-Description</span></span>
<span data-ttu-id="c1c93-121">Określa opcjonalny opis tej reguły.</span><span class="sxs-lookup"><span data-stu-id="c1c93-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="c1c93-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="c1c93-122">-DestinationAddress</span></span>
<span data-ttu-id="c1c93-123">Adresy docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="c1c93-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="c1c93-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="c1c93-124">-DestinationFqdn</span></span>
<span data-ttu-id="c1c93-125">Docelowa fqdn reguły</span><span class="sxs-lookup"><span data-stu-id="c1c93-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="c1c93-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="c1c93-126">-DestinationIpGroup</span></span>
<span data-ttu-id="c1c93-127">Docelowa grupa ipgroup reguły</span><span class="sxs-lookup"><span data-stu-id="c1c93-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="c1c93-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="c1c93-128">-DestinationPort</span></span>
<span data-ttu-id="c1c93-129">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="c1c93-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="c1c93-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c1c93-130">-Name</span></span>
<span data-ttu-id="c1c93-131">Określa nazwę tej reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="c1c93-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="c1c93-132">Nazwa musi być unikatowa w zbiorze reguł.</span><span class="sxs-lookup"><span data-stu-id="c1c93-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="c1c93-133">— Protokół</span><span class="sxs-lookup"><span data-stu-id="c1c93-133">-Protocol</span></span>
<span data-ttu-id="c1c93-134">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="c1c93-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="c1c93-135">Dopuszczalne wartości to TCP, UDP, ICMP i Any.</span><span class="sxs-lookup"><span data-stu-id="c1c93-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="c1c93-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="c1c93-136">-SourceAddress</span></span>
<span data-ttu-id="c1c93-137">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="c1c93-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="c1c93-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="c1c93-138">-SourceIpGroup</span></span>
<span data-ttu-id="c1c93-139">Źródłowa grupa ipgroup reguły</span><span class="sxs-lookup"><span data-stu-id="c1c93-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="c1c93-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1c93-140">-Confirm</span></span>
<span data-ttu-id="c1c93-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c1c93-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c93-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c93-142">-WhatIf</span></span>
<span data-ttu-id="c1c93-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1c93-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c93-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c1c93-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c93-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c93-145">CommonParameters</span></span>
<span data-ttu-id="c1c93-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c93-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c93-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c93-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c93-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1c93-148">INPUTS</span></span>

### <span data-ttu-id="c1c93-149">Brak</span><span class="sxs-lookup"><span data-stu-id="c1c93-149">None</span></span>

## <span data-ttu-id="c1c93-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c1c93-150">OUTPUTS</span></span>

### <span data-ttu-id="c1c93-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c1c93-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="c1c93-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c1c93-152">NOTES</span></span>

## <span data-ttu-id="c1c93-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1c93-153">RELATED LINKS</span></span>

[<span data-ttu-id="c1c93-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c1c93-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="c1c93-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c1c93-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="c1c93-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c1c93-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
