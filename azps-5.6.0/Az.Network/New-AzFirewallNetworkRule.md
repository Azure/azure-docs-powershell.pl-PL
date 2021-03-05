---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 7b2c78793f5a5e5ae6de8c67ffc214ed5c9b9076
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984432"
---
# <span data-ttu-id="09f20-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="09f20-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="09f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09f20-102">SYNOPSIS</span></span>
<span data-ttu-id="09f20-103">Tworzy regułę sieciową zapory.</span><span class="sxs-lookup"><span data-stu-id="09f20-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="09f20-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09f20-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09f20-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="09f20-105">DESCRIPTION</span></span>
<span data-ttu-id="09f20-106">Polecenie **cmdlet New-AzFirewallNetworkRule** tworzy regułę sieciową dla zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="09f20-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="09f20-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09f20-107">EXAMPLES</span></span>

### <span data-ttu-id="09f20-108">Przykład 1. Tworzenie reguły dla całego ruchu TCP</span><span class="sxs-lookup"><span data-stu-id="09f20-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="09f20-109">W tym przykładzie jest organizacji tworzącej regułę dla całego ruchu TCP.</span><span class="sxs-lookup"><span data-stu-id="09f20-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="09f20-110">Użytkownik wymusza, czy ruch dla reguły będzie dozwolony lub odrzucony na podstawie zbioru reguł, z które jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="09f20-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="09f20-111">Przykład 2. Tworzenie reguły dla całego ruchu TCP od 10.0.0.0 do 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="09f20-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="09f20-112">W tym przykładzie jest utworzenie reguły dla całego ruchu TCP z od 10.0.0.0 do 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="09f20-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="09f20-113">Użytkownik wymusza, czy ruch dla reguły będzie dozwolony lub odrzucony na podstawie zbioru reguł, z które jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="09f20-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="09f20-114">Przykład 3. Tworzenie reguły dla całego ruchu TCP i ICMP z dowolnego źródła do 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="09f20-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="09f20-115">W tym przykładzie jest organizacji tworzącej regułę dla całego ruchu TCP z dowolnego źródła do 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="09f20-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="09f20-116">Użytkownik wymusza, czy ruch dla reguły będzie dozwolony lub odrzucony na podstawie zbioru reguł, z które jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="09f20-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="09f20-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09f20-117">PARAMETERS</span></span>

### <span data-ttu-id="09f20-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f20-118">-DefaultProfile</span></span>
<span data-ttu-id="09f20-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="09f20-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09f20-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="09f20-120">-Description</span></span>
<span data-ttu-id="09f20-121">Określa opcjonalny opis tej reguły.</span><span class="sxs-lookup"><span data-stu-id="09f20-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="09f20-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="09f20-122">-DestinationAddress</span></span>
<span data-ttu-id="09f20-123">Adresy docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="09f20-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="09f20-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="09f20-124">-DestinationFqdn</span></span>
<span data-ttu-id="09f20-125">Docelowa fqdn reguły</span><span class="sxs-lookup"><span data-stu-id="09f20-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="09f20-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="09f20-126">-DestinationIpGroup</span></span>
<span data-ttu-id="09f20-127">Docelowa grupa ipgroup reguły</span><span class="sxs-lookup"><span data-stu-id="09f20-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="09f20-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="09f20-128">-DestinationPort</span></span>
<span data-ttu-id="09f20-129">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="09f20-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="09f20-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="09f20-130">-Name</span></span>
<span data-ttu-id="09f20-131">Określa nazwę tej reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="09f20-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="09f20-132">Nazwa musi być unikatowa w zbiorze reguł.</span><span class="sxs-lookup"><span data-stu-id="09f20-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="09f20-133">— Protokół</span><span class="sxs-lookup"><span data-stu-id="09f20-133">-Protocol</span></span>
<span data-ttu-id="09f20-134">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="09f20-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="09f20-135">Dopuszczalne wartości to TCP, UDP, ICMP i Any.</span><span class="sxs-lookup"><span data-stu-id="09f20-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="09f20-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="09f20-136">-SourceAddress</span></span>
<span data-ttu-id="09f20-137">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="09f20-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="09f20-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="09f20-138">-SourceIpGroup</span></span>
<span data-ttu-id="09f20-139">Źródłowa grupa ipgroup reguły</span><span class="sxs-lookup"><span data-stu-id="09f20-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="09f20-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09f20-140">-Confirm</span></span>
<span data-ttu-id="09f20-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09f20-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09f20-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09f20-142">-WhatIf</span></span>
<span data-ttu-id="09f20-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09f20-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09f20-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="09f20-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09f20-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f20-145">CommonParameters</span></span>
<span data-ttu-id="09f20-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f20-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f20-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f20-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f20-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09f20-148">INPUTS</span></span>

### <span data-ttu-id="09f20-149">Brak</span><span class="sxs-lookup"><span data-stu-id="09f20-149">None</span></span>

## <span data-ttu-id="09f20-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09f20-150">OUTPUTS</span></span>

### <span data-ttu-id="09f20-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="09f20-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="09f20-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09f20-152">NOTES</span></span>

## <span data-ttu-id="09f20-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09f20-153">RELATED LINKS</span></span>

[<span data-ttu-id="09f20-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="09f20-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="09f20-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="09f20-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="09f20-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="09f20-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
