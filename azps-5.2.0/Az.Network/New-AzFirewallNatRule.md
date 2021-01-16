---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334909"
---
# <span data-ttu-id="b6f79-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="b6f79-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="b6f79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6f79-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f79-103">Tworzy regułę NAT dla zapory.</span><span class="sxs-lookup"><span data-stu-id="b6f79-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="b6f79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6f79-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f79-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6f79-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f79-106">Polecenie cmdlet **New-AzFirewallNatRule** umożliwia utworzenie reguły NAT dla zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f79-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="b6f79-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6f79-107">EXAMPLES</span></span>

### <span data-ttu-id="b6f79-108">Przykład 1: Utwórz regułę DNAT całego ruchu TCP z 10.0.0.0/24 na 10.1.2.3 docelowy: 80 do lokalizacji docelowej 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="b6f79-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="b6f79-109">W tym przykładzie jest tworzona reguła, która będzie DNAT cały ruch pochodzący z adresu 10.0.0.0/24 z docelowym 10.1.2.3:80 do 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="b6f79-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="b6f79-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6f79-110">PARAMETERS</span></span>

### <span data-ttu-id="b6f79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f79-111">-DefaultProfile</span></span>
<span data-ttu-id="b6f79-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f79-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6f79-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="b6f79-113">-Description</span></span>
<span data-ttu-id="b6f79-114">Umożliwia określenie opcjonalnego opisu tej reguły.</span><span class="sxs-lookup"><span data-stu-id="b6f79-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="b6f79-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b6f79-115">-DestinationAddress</span></span>
<span data-ttu-id="b6f79-116">Adresy docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="b6f79-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="b6f79-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b6f79-117">-DestinationPort</span></span>
<span data-ttu-id="b6f79-118">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="b6f79-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="b6f79-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6f79-119">-Name</span></span>
<span data-ttu-id="b6f79-120">Określa nazwę tej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="b6f79-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="b6f79-121">Nazwa musi być unikatowa w kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="b6f79-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="b6f79-122">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="b6f79-122">-Protocol</span></span>
<span data-ttu-id="b6f79-123">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="b6f79-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="b6f79-124">Obsługiwane protokoły to TCP i UDP.</span><span class="sxs-lookup"><span data-stu-id="b6f79-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="b6f79-125">Dozwolona jest specjalna wartość "any", co oznacza, że jest zgodna z portami TCP i UDP, ale nie innymi protokołami.</span><span class="sxs-lookup"><span data-stu-id="b6f79-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="b6f79-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="b6f79-126">-SourceAddress</span></span>
<span data-ttu-id="b6f79-127">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="b6f79-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="b6f79-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="b6f79-128">-SourceIpGroup</span></span>
<span data-ttu-id="b6f79-129">Ipgroup źródłowa reguły</span><span class="sxs-lookup"><span data-stu-id="b6f79-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="b6f79-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="b6f79-130">-TranslatedAddress</span></span>
<span data-ttu-id="b6f79-131">Określa żądany wynik translacji adresów</span><span class="sxs-lookup"><span data-stu-id="b6f79-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="b6f79-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="b6f79-132">-TranslatedFqdn</span></span>
<span data-ttu-id="b6f79-133">Przetłumaczona nazwa FQDN dla tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="b6f79-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="b6f79-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="b6f79-134">-TranslatedPort</span></span>
<span data-ttu-id="b6f79-135">Określa wymagany wynik translacji portów.</span><span class="sxs-lookup"><span data-stu-id="b6f79-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="b6f79-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6f79-136">-Confirm</span></span>
<span data-ttu-id="b6f79-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6f79-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f79-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f79-138">-WhatIf</span></span>
<span data-ttu-id="b6f79-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6f79-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f79-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6f79-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f79-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f79-141">CommonParameters</span></span>
<span data-ttu-id="b6f79-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6f79-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f79-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f79-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f79-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6f79-144">INPUTS</span></span>

### <span data-ttu-id="b6f79-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b6f79-145">None</span></span>

## <span data-ttu-id="b6f79-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6f79-146">OUTPUTS</span></span>

### <span data-ttu-id="b6f79-147">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="b6f79-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="b6f79-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6f79-148">NOTES</span></span>

## <span data-ttu-id="b6f79-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6f79-149">RELATED LINKS</span></span>

[<span data-ttu-id="b6f79-150">Nowe — AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b6f79-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="b6f79-151">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6f79-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b6f79-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b6f79-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
