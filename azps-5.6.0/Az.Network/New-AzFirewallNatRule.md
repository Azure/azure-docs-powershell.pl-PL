---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: 2bbac9bebd79f1ca51a7defd4c57589764b2c34e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985797"
---
# <span data-ttu-id="bc0be-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="bc0be-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="bc0be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc0be-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0be-103">Tworzy regułę nat nat zapory.</span><span class="sxs-lookup"><span data-stu-id="bc0be-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="bc0be-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc0be-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc0be-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc0be-105">DESCRIPTION</span></span>
<span data-ttu-id="bc0be-106">Polecenie **cmdlet New-AzFirewallNatRule** tworzy regułę NAT dla Zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0be-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="bc0be-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc0be-107">EXAMPLES</span></span>

### <span data-ttu-id="bc0be-108">Przykład 1. Tworzenie reguły dla ruchu TCP z 10.0.0.0/24 z miejscem docelowym 10.1.2.2.3:80 do miejsca docelowego 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="bc0be-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="bc0be-109">W tym przykładzie jest serwerze tworzącym regułę, która spowoduje, że program PROC.PRZYT wszystkich ruchu pochodzących z 10.0.0.0/24 z miejscem docelowym od 10.1.2.3:80 do 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="bc0be-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="bc0be-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc0be-110">PARAMETERS</span></span>

### <span data-ttu-id="bc0be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc0be-111">-DefaultProfile</span></span>
<span data-ttu-id="bc0be-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc0be-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="bc0be-113">-Description</span></span>
<span data-ttu-id="bc0be-114">Określa opcjonalny opis tej reguły.</span><span class="sxs-lookup"><span data-stu-id="bc0be-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="bc0be-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="bc0be-115">-DestinationAddress</span></span>
<span data-ttu-id="bc0be-116">Adresy docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="bc0be-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="bc0be-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="bc0be-117">-DestinationPort</span></span>
<span data-ttu-id="bc0be-118">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="bc0be-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="bc0be-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bc0be-119">-Name</span></span>
<span data-ttu-id="bc0be-120">Określa nazwę tej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="bc0be-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="bc0be-121">Nazwa musi być unikatowa w zbiorze reguł.</span><span class="sxs-lookup"><span data-stu-id="bc0be-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="bc0be-122">— Protokół</span><span class="sxs-lookup"><span data-stu-id="bc0be-122">-Protocol</span></span>
<span data-ttu-id="bc0be-123">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="bc0be-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="bc0be-124">Obsługiwane protokoły to TCP i UDP.</span><span class="sxs-lookup"><span data-stu-id="bc0be-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="bc0be-125">Dozwolona jest specjalna wartość "Dowolna", co oznacza, że będzie ona do siebie dorównana zarówno TCP, jak i UDP, ale nie będzie zawierała żadnych innych protokołów.</span><span class="sxs-lookup"><span data-stu-id="bc0be-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc0be-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="bc0be-126">-SourceAddress</span></span>
<span data-ttu-id="bc0be-127">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="bc0be-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="bc0be-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="bc0be-128">-SourceIpGroup</span></span>
<span data-ttu-id="bc0be-129">Źródłowa grupa ipgroup reguły</span><span class="sxs-lookup"><span data-stu-id="bc0be-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="bc0be-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="bc0be-130">-TranslatedAddress</span></span>
<span data-ttu-id="bc0be-131">Określa żądany wynik tłumaczenia adresu.</span><span class="sxs-lookup"><span data-stu-id="bc0be-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="bc0be-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="bc0be-132">-TranslatedFqdn</span></span>
<span data-ttu-id="bc0be-133">Przetłumaczona fqdn tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="bc0be-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="bc0be-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="bc0be-134">-TranslatedPort</span></span>
<span data-ttu-id="bc0be-135">Określa żądany wynik tłumaczenia portu.</span><span class="sxs-lookup"><span data-stu-id="bc0be-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="bc0be-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bc0be-136">-Confirm</span></span>
<span data-ttu-id="bc0be-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bc0be-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc0be-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc0be-138">-WhatIf</span></span>
<span data-ttu-id="bc0be-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc0be-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc0be-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bc0be-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc0be-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0be-141">CommonParameters</span></span>
<span data-ttu-id="bc0be-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc0be-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0be-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc0be-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0be-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc0be-144">INPUTS</span></span>

### <span data-ttu-id="bc0be-145">Brak</span><span class="sxs-lookup"><span data-stu-id="bc0be-145">None</span></span>

## <span data-ttu-id="bc0be-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc0be-146">OUTPUTS</span></span>

### <span data-ttu-id="bc0be-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="bc0be-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="bc0be-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc0be-148">NOTES</span></span>

## <span data-ttu-id="bc0be-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc0be-149">RELATED LINKS</span></span>

[<span data-ttu-id="bc0be-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bc0be-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="bc0be-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bc0be-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="bc0be-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bc0be-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
